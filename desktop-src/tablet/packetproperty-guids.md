---
description: In der folgenden Tabelle sind die paketeigenschafts-GUIDs aufgeführt, die von der PACKET \_ PROPERTY-Struktur verwendet werden.
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: PacketProperty-GUIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb7db9f2d5e05000bdccd5a09b2b799f38aa1bb692fea110ea153a57912cfc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449370"
---
# <a name="packetproperty-guids"></a>PacketProperty-GUIDs

In der folgenden Tabelle sind die paketeigenschafts-GUIDs aufgeführt, die von der [**PACKET \_ PROPERTY-Struktur**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) verwendet werden.



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
<td>Winkel zwischen der Achse des Stifts und der Oberfläche des Tabletts. Der Wert ist 0, wenn der Stift parallel zur Oberfläche ist, und 90, wenn der Stift zur Oberfläche durchdringt wird. Die Werte sind negativ, wenn der Stift invertiert wird.<br/></td>
</tr>
<tr class="even">
<td>GUID_AZIMUTH_ORIENTATION<br/></td>
<td>Drehung des Cursors im Uhrzeigersinn um die Z-Achse durch einen vollständigen kreisförmigen Bereich.<br/></td>
</tr>
<tr class="odd">
<td>GUID_BOXNUMBER<br/></td>
<td>Die GUID, die verwendet wird, um die Feldnummer für eine Ink-Erkennungs-Alternative abzurufen, wenn die Erkennung im Feldmodus ausgeführt wird.<br/></td>
</tr>
<tr class="even">
<td>GUID_BUTTON_PRESSURE<br/></td>
<td>Druck auf einer druckempfindlichen Schaltfläche.<br/></td>
</tr>
<tr class="odd">
<td>GUID_NORMAL_PRESSURE<br/></td>
<td>Die GUID für das PacketProperty-Objekt, das den Druck der Stiftspitze auf die Tablettoberfläche darstellt. Je größer der Druck auf die Stiftspitze, desto mehr Druck wird gezeichnet.<br/></td>
</tr>
<tr class="even">
<td>GUID_PACKET_STATUS<br/></td>
<td>Enthält mindestens einen der folgenden Flagwerte:<br/>
<ul>
<li>Der Cursor berührt die Zeichenoberfläche (Wert = 1).</li>
<li>Der Cursor wird invertiert. Beispielsweise verweist das Radiererende des Stifts auf die Oberfläche (Wert = 2).</li>
<li>Nicht verwendet (Wert = 4).</li>
<li>Die Schaltfläche "Fass" wird gedrückt (Wert = 8).</li>
</ul></td>
</tr>
<tr class="odd">
<td>GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID<br/></td>
<td>Die Gerätekontakt-ID für ein Paket.<br/></td>
</tr>
<tr class="even">
<td>GUID_SERIAL_NUMBER<br/></td>
<td>Identifiziert das Paket. Dies ist der gleiche Wert, den Sie zum Abrufen des Pakets aus der Paketwarteschlange verwenden.<br/></td>
</tr>
<tr class="odd">
<td>GUID_TANGENT_PRESSURE<br/></td>
<td>Die GUID für das PacketProperty-Objekt, das den Druck der Stiftspitze entlang der Ebene der Tablettoberfläche darstellt.<br/></td>
</tr>
<tr class="even">
<td>GUID_TIMER_TICK<br/></td>
<td>Zeitpunkt, zu dem das Paket generiert wurde.<br/></td>
</tr>
<tr class="odd">
<td>GUID_TWIST_ORIENTATION<br/></td>
<td>Drehung des Cursors um die eigene Achse im Uhrzeigersinn.<br/></td>
</tr>
<tr class="even">
<td>GUID_X<br/></td>
<td>Die x-Koordinate im Tabletkoordinatenraum. Jedes Paket enthält diese Eigenschaft standardmäßig. Der Ursprung (0,0) des Tablets ist die obere linke Ecke.<br/></td>
</tr>
<tr class="odd">
<td>GUID_X_TILT_ORIENTATION<br/></td>
<td>Bei einem Stiftcursor ist die x-Neigungsausrichtung der Winkel zwischen der y-, z-Ebene und dem Stift und der y-Achsenebene. Der Wert ist 0, wenn der Stift zur Zeichenoberfläche passt, und ist positiv, wenn sich der Stift rechts von perpendlike befindet.<br/></td>
</tr>
<tr class="even">
<td>GUID_Y<br/></td>
<td>Die y-Koordinate im Tabletkoordinatenraum. Jedes Paket enthält diese Eigenschaft standardmäßig. Der Ursprung (0,0) des Tablets ist die obere linke Ecke.<br/></td>
</tr>
<tr class="odd">
<td>GUID_Y_TILT_ORIENTATION<br/></td>
<td>Bei einem Stiftcursor ist die y-Neigungsausrichtung der Winkel zwischen der x-, z-Ebene und dem Stift und der x-Achsenebene. Der Wert ist 0, wenn der Stift auf die Zeichnungsoberfläche eingedrückt ist, und ist positiv, wenn der Stift aufwärts oder vom Benutzer entfernt ist.<br/></td>
</tr>
<tr class="even">
<td>GUID_Z<br/></td>
<td>Die Z-Koordinate oder der Abstand der Stiftspitze von der Tablettoberfläche. Der <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> Enumerationstyp bestimmt die Maßeinheit für diese Eigenschaft. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Das TangentPressure-Feld stellt den Druck auf der Ebene der Tablettoberfläche dar. Das Feld NormalPressure stellt den Druck auf die Ebene der Tablettoberfläche dar.

 

 

 




