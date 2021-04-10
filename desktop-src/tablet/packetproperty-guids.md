---
description: In der folgenden Tabelle werden die von der Paket Eigenschafts Struktur verwendeten Paket Eigenschaften-GUIDs aufgelistet \_ .
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: PacketProperty-GUIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94591ccda5cd1f40b79c5cbb4fe80ca3ef99d2e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868928"
---
# <a name="packetproperty-guids"></a>PacketProperty-GUIDs

In der folgenden Tabelle werden die von der [**Paket \_ Eigenschafts**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) Struktur verwendeten Paket Eigenschaften-GUIDs aufgelistet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GUID_ALTITUDE_ORIENTATION<br/></td>
<td>Der Winkel zwischen der Achse des Stifts und der Oberfläche des Tablets. Der Wert ist 0 (null), wenn der Stift parallel zur Oberfläche und 90 ist, wenn der Stift senkrecht zur Oberfläche ist. Die Werte sind negativ, wenn der Stift invertiert wird.<br/></td>
</tr>
<tr class="even">
<td>GUID_AZIMUTH_ORIENTATION<br/></td>
<td>Drehung im Uhrzeigersinn um die z-Achse um die z-Achse durch einen vollständigen kreisförmigen Bereich.<br/></td>
</tr>
<tr class="odd">
<td>GUID_BOXNUMBER<br/></td>
<td>Die GUID, die verwendet wird, um die Box-Nummer für eine frei Handerkennung abzurufen, wenn die Erkennung im Box-Modus ausgeführt wird.<br/></td>
</tr>
<tr class="even">
<td>GUID_BUTTON_PRESSURE<br/></td>
<td>Druck auf eine druckempfindliche Schaltfläche.<br/></td>
</tr>
<tr class="odd">
<td>GUID_NORMAL_PRESSURE<br/></td>
<td>Die GUID für das PacketProperty-Objekt, das den Druck der Stift Spitze senkrecht zur Tablet-Oberfläche darstellt. Je größer der Druck der Stift Spitze ist, desto mehr frei Hand Eingaben werden gezeichnet.<br/></td>
</tr>
<tr class="even">
<td>GUID_PACKET_STATUS<br/></td>
<td>Enthält mindestens einen der folgenden Flagwerte:<br/>
<ul>
<li>Der Cursor berührt die Zeichen Oberfläche (Wert = 1).</li>
<li>Der Cursor wird umgekehrt. Beispielsweise zeigt das Ende des Stifts auf die Oberfläche (Wert = 2).</li>
<li>Nicht verwendet (Wert = 4).</li>
<li>Die Schaltfläche "Barrel" wird gedrückt (Wert = 8).</li>
</ul></td>
</tr>
<tr class="odd">
<td>GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID<br/></td>
<td>Der Bezeichner des Geräte Kontakts für ein Paket.<br/></td>
</tr>
<tr class="even">
<td>GUID_SERIAL_NUMBER<br/></td>
<td>Identifiziert das Paket. Dies ist derselbe Wert, den Sie verwenden, um das Paket aus der Paket Warteschlange abzurufen.<br/></td>
</tr>
<tr class="odd">
<td>GUID_TANGENT_PRESSURE<br/></td>
<td>Die GUID für das PacketProperty-Objekt, das den Druck der Stift Spitze auf der Ebene der Tablet-Oberfläche darstellt.<br/></td>
</tr>
<tr class="even">
<td>GUID_TIMER_TICK<br/></td>
<td>Zeitpunkt, zu dem das Paket generiert wurde.<br/></td>
</tr>
<tr class="odd">
<td>GUID_TWIST_ORIENTATION<br/></td>
<td>Drehung des Cursors im Uhrzeigersinn um die eigene Achse.<br/></td>
</tr>
<tr class="even">
<td>GUID_X<br/></td>
<td>Die x-Koordinate im tablettkoordinatenbereich. Jedes Paket enthält diese Eigenschaft standardmäßig. Der Ursprung (0,0) des Tablets ist die linke obere Ecke.<br/></td>
</tr>
<tr class="odd">
<td>GUID_X_TILT_ORIENTATION<br/></td>
<td>Bei einem Stift Cursor ist die x-Neigungs Ausrichtung der Winkel zwischen der y-, z-und der Stift-und der y-Achsen Ebene. Der Wert ist 0 (null), wenn der Stift senkrecht zur Zeichen Oberfläche ist und positiv ist, wenn sich der Stift rechts von senkrecht befindet.<br/></td>
</tr>
<tr class="even">
<td>GUID_Y<br/></td>
<td>Die y-Koordinate im tablettkoordinatenbereich. Jedes Paket enthält diese Eigenschaft standardmäßig. Der Ursprung (0,0) des Tablets ist die linke obere Ecke.<br/></td>
</tr>
<tr class="odd">
<td>GUID_Y_TILT_ORIENTATION<br/></td>
<td>Bei einem Stift Cursor ist die y-Neigungs Ausrichtung der Winkel zwischen der x-, der z-Ebene und der Ebene des Stifts und der x-Achse. Der Wert ist 0 (null), wenn der Stift senkrecht zur Zeichnungs Oberfläche ist und positiv ist, wenn sich der Stift nach oben oder vom Benutzer entfernt.<br/></td>
</tr>
<tr class="even">
<td>GUID_Z<br/></td>
<td>Die z-Koordinate oder den Abstand der Stift Spitze von der Tablet-Oberfläche. Der <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> Enumerationstyp bestimmt die Maßeinheit für diese Eigenschaft. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Das TangentPressure-Feld stellt den Druck auf der Ebene der Tablet-Oberfläche dar. das Feld für den normalen Druck steht für den Druck senkrecht zur Ebene der Tablet-Oberfläche.

 

 

 




