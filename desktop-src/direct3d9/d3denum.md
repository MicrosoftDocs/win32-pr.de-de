---
description: Treiberfunktionsflag.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829d03bf596c24bfb6b3443ace859629f723a664
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343256"
---
# <a name="d3denum"></a>D3DENUM

Treiberfunktionsflag.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definieren</td>
<td>Wert</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>D3DENUM_WHQL_LEVEL</td>
<td>0x00000002L</td>
<td>Testen von Microsoft Windows Hardware Quality Labs-Treibern (WHQL). Dies ist ein zeitaufwändiger Test, der eine Zeiteinbuße von einer Sekunde oder zwei Sekunden erfordert. Diese Konstante wird vom WHQLLevel-Member von <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>verwendet.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> D3DENUM_WHQL_LEVEL ist für Direct3D9Ex unter Windows Vista, Windows Server 2008, Windows 7 und Windows Server 2008 R2 (oder einem aktuelleren Betriebssystem) veraltet. Jedes dieser Betriebssysteme gibt 1 für die WHQL-Ebene zurück, ohne den Status des Treibers zu überprüfen. <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a>Konstanteninformationen



| Anforderung                         | Wert           |
|--------------------------|------------|
| Header                   | d3d9.h     |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




