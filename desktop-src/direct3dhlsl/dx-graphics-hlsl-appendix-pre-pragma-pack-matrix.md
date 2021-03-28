---
title: pack_matrix pragma-Direktive
description: Pragma-Direktive, die die Verpackungs Ausrichtung für Matrizen angibt.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix pragma-Direktive HLSL
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bb5474702a1caba3f772002c34677601715caff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037987"
---
# <a name="pack_matrix-pragma-directive"></a>packmatrix- \_ pragma-Direktive

Pragma-Direktive, die die Verpackungs Ausrichtung für Matrizen angibt.



| \#Pragma Pack- \_ Matrix ( *Ausrichtung* ) |
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
<td><span id="alignment"></span><span id="ALIGNMENT"></span><em>Richt</em><br/></td>
<td>Ausrichtung, die für Matrizen festgelegt wird. Dieser Parameter kann einen der in der folgenden Tabelle aufgeführten Werte annehmen. <br/> 
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
<td>Standard. Legt die Ausrichtung der Matrix Verpackung auf den Spalten Hauptwert fest.</td>
</tr>
<tr class="even">
<td>row_major</td>
<td>Legt die Ausrichtung der Matrix Verpackung auf den Hauptabschnitt der Zeile fest.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Ausrichtung der Matrix Verpackung auf Zeilen Hauptwert festgelegt.


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#pragma-Direktive (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





