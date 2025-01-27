# 07 Homework 

# 7.1 Questions 

## Question 1
```SQL

SELECT ModelYear, Make, Model
FROM EVRegistry


```

## Question 2
```SQL

SELECT DISTINCT ElectricVehicleType
FROM EVRegistry

```

## Question 3
```SQL

SELECT *
FROM EVRegistry
WHERE ElectricVehicleType = 'Battery Electric Vehicle (BEV)'


```

## Question 4
```SQL

SELECT Make, Model
FROM EVRegistry
WHERE BaseMSRP BETWEEN 20000 and 35000


```
# 7.2 Questions 

## Question 1
```SQL

SELECT *
FROM EVRegistry
WHERE City is NULL


```
## Question 2
```SQL

SELECT Make, MODEL, ElectricVehicleType
FROM EVRegistry
WHERE VIN like'%3E1EA1J'



```
## Question 3
```SQL

SELECT ModelYear, Make, Model, ElectricVehicleType, ElectricRange
FROM EVRegistry
WHERE Make = 'TESLA' or Make = 'CHEVROLET'
ORDER by Make, ModelYear DESC


```
## Question 4
```SQL

SELECT stationId, count(*) as numUses
FROM EVCharging
GROUP BY stationId
ORDER BY count(*)
LIMIT 5


```
## Question 5
```SQL

SELECT min (chargeTimeHrs)as 'minTime', max (chargeTimeHrs)as 'maxTime', userId
FROM EVCharging
WHERE chargeTimeHrs > 0.5
Group by userId
ORDER BY 2,3


```
# 7.3 Questions 

## Question 1

### 1. With a chargeTimeHrs of 2.94 Wednesday has the highest average charging time

## Question 2
```SQL
SELECT round(SUM(kwhTotal),2) as 'totalpower', userId
FROM EVCharging
GROUP BY userId
order by 'totalpower' DESC
LIMIT 15


1006.11	98345808
736.67	97867440
6.86	95980995
81.64	95411349
258.41	94947534
238.64	93202560
99.5	92911698
399.48	92283246
52.47	92192265
870.92	90692118
118.7	90546786
492.52	88561539
41.38	87444027
383.24	86810130
34.19	85580550




```
