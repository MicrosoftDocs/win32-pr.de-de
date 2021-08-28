---
description: Treiberfunktionsflag.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb3ed10a4a12602e8586bbd0e941641287346a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627996"
---
# <a name="d3denum"></a>D3DENUM

Treiberfunktionsflag.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definieren</td>
<td>Wert</td>
<td>Beschreibung</td>
</tr>
<tr class="even">
<td>D3DENUM_WHQL_LEVEL</td>
<td>0x00000002L</td>
<td>Microsoft Windows Hardware Quality Labs -Treibertests (WHQL). Dies ist ein zeitaufwändiger Test, der eine Zeitstrafe von einer Sekunde oder zwei Sekunden erfordert. Diese Konstante wird vom WHQLLevel-Member <a href="d3dadapter-identifier9.md"><strong>von</strong></a>D3DADAPTER_IDENTIFIER9.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> D3DENUM_WHQL_LEVEL ist für Direct3D9Ex unter Windows Vista, Windows Server 2008, Windows 7 und Windows Server 2008 R2 (oder mehr aktuelles Betriebssystem) veraltet. Jedes dieser Betriebssysteme gibt 1 für die WHQL-Ebene zurück, ohne den Status des Treibers zu überprüfen. <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a>Konstante Informationen



| Anforderung                         | Wert           |
|--------------------------|------------|
| Header                   | d3d9.h     |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




