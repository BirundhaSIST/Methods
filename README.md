# Methods
Class method instance method static method
class Movies:
    profit=1000
    def _init_(self, name, collection, producer, year):# instance variable
        self.name=name
        self.collection=collection
        self.producer=producer
        self.year=year
    @classmethod
    def change_profit(cls,amount):
        cls.profit=amount
        return cls.profit
    @classmethod
    def data_set(cls,data):
        name, collection, producer, year=data.split(",")
        return cls(name, collection, producer, year)
    @staticmethod
    def release_date(date):
        lis=[2008, 2004, 2010, 2011]
        if date in lis:
            return'True'
        return'False'

    
m1 = Movies('iron man', 580, 'kevin', 2008)
m2 = Movies('the incredible hulk', 680, 'gale', 2009)
data='thor,700,feige,2011'
print(Movies.releasse_date(12))
print(Movies.change_profit(2000))
print(Movies.data_set(data))
