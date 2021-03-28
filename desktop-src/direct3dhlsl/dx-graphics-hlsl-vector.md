---
title: Vector Type (HLSL)
description: Ein Vektor enthält zwischen einer und vier skalare Komponenten. jede Komponente eines Vektors muss denselben Typ aufweisen.
ms.assetid: 16e66f3c-c513-4d03-8adf-463dc8d83e12
keywords:
- Vector Type HLSL
topic_type:
- apiref
api_name:
- Vector Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d07da5d22dfb44215f70a7620d6519b5c8a802
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "104995262"
---
# <a name="vector-type"></a>Vektortyp

Ein Vektor enthält zwischen einer und vier skalare Komponenten. jede Komponente eines Vektors muss denselben Typ aufweisen.



|                     |
|---------------------|
| **Name der Typnummer** |



 


```
TypeComponents Name
```



## <a name="components"></a>Komponenten



| Element                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**Typecomponents**<br/> | Ein einzelner Name, der zwei Teile enthält. Der erste Teil ist einer der [skalaren](dx-graphics-hlsl-data-types.md) Typen. Der zweite Teil ist die Anzahl der Komponenten, die zwischen 1 und 4 einschließlich liegen muss.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**<br/>                                         | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                                                                                                                                                |



 

## <a name="examples"></a>Beispiele

Hier einige Beispiele:


```
bool    bVector;   // scalar containing 1 Boolean
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
```



Ein Vektor kann auch mit der folgenden Syntax deklariert werden:


```
vector <Type, Number> VariableName
```



Hier einige Beispiele:


```
vector <int,    1> iVector = 1;
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





