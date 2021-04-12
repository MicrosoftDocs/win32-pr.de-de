---
description: In diesem Thema werden die \_ von NLS verwendeten Gebiets Schema-InEG- \* Konstanten definiert.
ms.assetid: 3a1e4a63-31bd-4ff9-a3ca-af357389e179
title: LOCALE_INEG *-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b17c61f0ca769206f30b84aa73cc3548ad9b915
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343989"
---
# <a name="locale_ineg-constants"></a>Gebiets Schema- \_ InEG- \* Konstanten

In diesem Thema werden die \_ von NLS verwendeten Gebiets Schema-InEG- \* Konstanten definiert.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LOCALE_INEGCURR</td>
<td>Negativer Währungs Modus. 
<table>
<thead>
<tr class="header">
<th>Mode</th>
<th>Format für negative Währung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Linke Klammer, Währungssymbol, Zahl, Rechte Klammer; Beispiel: ($1,1)</td>
</tr>
<tr class="even">
<td>1</td>
<td>Negatives Vorzeichen, Währungssymbol, Zahl; Beispiel:-$1,1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Währungssymbol, negatives Vorzeichen, Zahl; Beispiel: $-1,1</td>
</tr>
<tr class="even">
<td>3</td>
<td>Währungssymbol, Zahl, negatives Vorzeichen; Beispiel: $1,1-</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Linke Klammer, Zahl, Währungssymbol, Rechte Klammer; Beispiel: ($1,1)</td>
</tr>
<tr class="even">
<td>5</td>
<td>Negatives Vorzeichen, Zahl, Währungssymbol; Beispiel:-$1,1</td>
</tr>
<tr class="odd">
<td>6</td>
<td>Zahl, negatives Vorzeichen, Währungssymbol; Beispiel: 1,1-$</td>
</tr>
<tr class="even">
<td>7</td>
<td>Zahl, Währungssymbol, negatives Vorzeichen; Beispiel: $1,1-</td>
</tr>
<tr class="odd">
<td>8</td>
<td>Negatives Zeichen, Zahl, Leerzeichen, Währungssymbol (z. b. #5, aber mit einem Leerzeichen vor dem Währungssymbol); Beispiel:-$1,1</td>
</tr>
<tr class="even">
<td>9</td>
<td>Negatives Vorzeichen, Währungssymbol, Leerzeichen, Zahl (z. b. #1, aber mit einem Leerzeichen nach dem Währungssymbol); Beispiel:-$1,1</td>
</tr>
<tr class="odd">
<td>10</td>
<td>Anzahl, Leerraum, Währungssymbol, negatives Vorzeichen (z. b. #7, aber mit einem Leerzeichen vor dem Währungssymbol); Beispiel: $1,1-</td>
</tr>
<tr class="even">
<td>11</td>
<td>Währungssymbol, Leerzeichen, Zahl, negatives Vorzeichen (z. b. #3, aber mit einem Leerzeichen nach dem Währungssymbol); Beispiel: $1,1-</td>
</tr>
<tr class="odd">
<td>12</td>
<td>Währungssymbol, Leerzeichen, negatives Vorzeichen, Zahl (z. b. #2, aber mit einem Leerzeichen nach dem Währungssymbol); Beispiel: $-1,1</td>
</tr>
<tr class="even">
<td>13</td>
<td>Zahl, Minuszeichen, Leerzeichen, Währungssymbol (z. b. #6, aber mit einem Leerzeichen vor dem Währungssymbol); Beispiel: 1,1-$</td>
</tr>
<tr class="odd">
<td>14</td>
<td>Linke Klammer, Währungssymbol, Leerzeichen, Zahl, Rechte Klammer (z. b. #0, aber mit einem Leerzeichen nach dem Währungssymbol); Beispiel: ($1,1)</td>
</tr>
<tr class="even">
<td>15</td>
<td>Linke Klammer, Zahl, Leerzeichen, Währungssymbol, Rechte Klammer (wie #4, aber mit einem Leerzeichen vor dem Währungssymbol); Beispiel: ($1,1)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>LOCALE_INEGNUMBER</td>
<td>Negativer Zahlen Modus, d. h. das Format für eine negative Zahl. 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Format</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Linke Klammer, Zahl, Rechte Klammer; Beispiel: (1,1)</td>
</tr>
<tr class="even">
<td>1</td>
<td>Negatives Vorzeichen, Zahl; Beispiel:-1,1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Negatives Zeichen, Leerzeichen, Zahl; Beispiel:-1,1</td>
</tr>
<tr class="even">
<td>3</td>
<td>Zahl, negatives Vorzeichen; Beispiel: 1,1-</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Zahl, Leerraum, negatives Vorzeichen; Beispiel: 1,1-</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>LOCALE_INEGSEPBYSPACE</td>
<td>Trennung des negativen Zeichens in einem monetären Wert. Dieser Wert ist 1, wenn das Währungssymbol durch ein Leerzeichen von der negativen Menge getrennt ist, oder 0, wenn dies nicht der Fall ist.</td>
</tr>
<tr class="even">
<td>LOCALE_INEGSIGNPOSN</td>
<td>Formatierungs Index für die negativen Zeichen Währungswerte. 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Klammern umschließen den Betrag und das Währungssymbol.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Das Vorzeichen liegt vor der Zahl.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Das Vorzeichen folgt auf die Zahl.</td>
</tr>
<tr class="even">
<td>3</td>
<td>Das Vorzeichen liegt vor dem Währungssymbol.</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Das Vorzeichen folgt dem Währungssymbol.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>LOCALE_INEGSYMPRECEDES</td>
<td>Die Position des Währungs Symbols in einem negativen monetären Wert. Dieser Wert ist 1, wenn das Währungssymbol der negativen Menge vorangestellt ist, oder 0, wenn das Symbol dem Betrag folgt.</td>
</tr>
</tbody>
</table>



 

 

 



