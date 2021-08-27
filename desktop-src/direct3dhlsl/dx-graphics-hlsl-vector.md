---
title: Vektortyp (HLSL)
description: Ein Vektor enthält zwischen einer und vier Skalarkomponenten. jede Komponente eines Vektors muss denselben Typ haben.
ms.assetid: 16e66f3c-c513-4d03-8adf-463dc8d83e12
keywords:
- Vektortyp HLSL
topic_type:
- apiref
api_name:
- Vector Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c1ed55fb60e3e7f42418e5bdfea48c1e298af34e9a7d76df17dfa7a021b3f50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024240"
---
# <a name="vector-type"></a>Vektortyp

Ein Vektor enthält zwischen einer und vier Skalarkomponenten. jede Komponente eines Vektors muss denselben Typ haben.



|                     |
|---------------------|
| **TypeNumber-Name** |



 


```
TypeComponents Name
```



## <a name="components"></a>Komponenten



| Element                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**<br/> | Ein einzelner Name, der zwei Teile enthält. Der erste Teil ist einer der [Skalartypen.](dx-graphics-hlsl-data-types.md) Der zweite Teil ist die Anzahl der Komponenten, die zwischen 1 und 4 einschließlich liegen müssen.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Namen**<br/>                                         | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                                                                                                                                                |



 

## <a name="examples"></a>Beispiele

Hier sind einige Beispiele:


```
bool    bVector;   // scalar containing 1 Boolean
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
```



Ein Vektor kann auch mit dieser Syntax deklariert werden:


```
vector <Type, Number> VariableName
```



Hier sind einige Beispiele:


```
vector <int,    1> iVector = 1;
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





