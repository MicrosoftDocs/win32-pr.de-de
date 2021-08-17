---
title: pack_matrix Pragmadirektive
description: Pragma-Direktive, die die Komprimierungsausrichtung für Matrizen angibt.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix Pragma-Direktive HLSL
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c12129b6840197b21d1d259cc13bd07e75620176bdc797e6828c10d71e1c95d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514783"
---
# <a name="pack_matrix-pragma-directive"></a>\_Paketmatrix-Pragmadirektive

Pragma-Direktive, die die Komprimierungsausrichtung für Matrizen angibt.



| \#pragma pack \_ matrix( *alignment* ) |
|--------------------------------------|



 

## <a name="parameters"></a>Parameter



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="alignment"></span><span id="ALIGNMENT"></span><em>Ausrichtung</em><br/></td>
<td>Ausrichtung, die für Matrizen festgelegt werden soll. Dieser Parameter kann einen der in der folgenden Tabelle aufgeführten Werte annehmen. <br/> 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>column_major</td>
<td>Standard. Legt die Matrix-Komprimierungsausrichtung auf die Spaltenhauptspalte fest.</td>
</tr>
<tr class="even">
<td>row_major</td>
<td>Legt die Matrix-Komprimierungsausrichtung auf Zeilenmatrizen fest.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Matrixpackungsausrichtung auf Zeilenmatrizen festgelegt.


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#pragma-Direktive (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





