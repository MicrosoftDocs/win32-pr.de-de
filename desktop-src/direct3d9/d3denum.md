---
description: Treiberfunktionsflag.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 059c2f9f1bf32275423bb9f2a9f484c12824bcda
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340119"
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
<td>#definieren</td>
<td>Wert</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>D3DENUM_WHQL_LEVEL</td>
<td>0x00000002L</td>
<td>Microsoft Windows Hardware Quality Labs (WHQL)-Treiber Tests. Dabei handelt es sich um einen zeitaufwändigen Test, der eine einsekunde oder zwei Sekunden Zeitstrafen erfordert. Diese Konstante wird vom whqllevel-Member von <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>verwendet.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> D3DENUM_WHQL_LEVEL ist für Direct3D9Ex, die unter Windows Vista, Windows Server 2008, Windows 7 und Windows Server 2008 R2 (oder einem höheren Betriebssystem) ausgeführt werden, veraltet. Eines dieser Betriebssysteme gibt 1 für den WHQL-Grad zurück, ohne den Status des Treibers zu überprüfen. <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9. h     |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




