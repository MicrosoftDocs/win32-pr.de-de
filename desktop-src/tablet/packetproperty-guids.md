---
description: In der folgenden Tabelle sind die paketeigenschafts-GUIDs aufgeführt, die von der PACKET \_ PROPERTY-Struktur verwendet werden.
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: PacketProperty-GUIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c897e19aea30db6e5dfa026fbdcfec77de5afa4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481646"
---
# <a name="packetproperty-guids"></a>PacketProperty-GUIDs

In der folgenden Tabelle sind die paketeigenschafts-GUIDs aufgeführt, die von der [**PACKET \_ PROPERTY-Struktur verwendet**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) werden.




| GUID | Beschreibung | 
|------|-------------|
| GUID_ALTITUDE_ORIENTATION<br /> | Winkel zwischen der Achse des Stifts und der Oberfläche des Tablets. Der Wert ist 0, wenn der Stift parallel zur Oberfläche ist, und 90, wenn der Stift an der Oberfläche durchlässig ist. Die Werte sind negativ, wenn der Stift invertiert wird.<br /> | 
| GUID_AZIMUTH_ORIENTATION<br /> | Drehung des Cursors im Uhrzeigersinn um die Z-Achse durch einen vollständigen kreisförmigen Bereich.<br /> | 
| GUID_BOXNUMBER<br /> | Die GUID, mit der die Feldnummer für eine Alternative zur Ink-Erkennung abgerufen wird, wenn die Erkennung im Feldmodus ausgeführt wird.<br /> | 
| GUID_BUTTON_PRESSURE<br /> | Druck auf einer druckempfindlichen Schaltfläche.<br /> | 
| GUID_NORMAL_PRESSURE<br /> | Die GUID für das PacketProperty-Objekt, das den Druck der Stiftspitze darstellt, die sich an der Tablettoberfläche durchdringt. Je größer der Druck auf der Stiftspitze ist, desto mehr Ink wird gezeichnet.<br /> | 
| GUID_PACKET_STATUS<br /> | Enthält mindestens einen der folgenden Flagwerte:<br /><ul><li>Der Cursor berührt die Zeichenoberfläche (Wert = 1).</li><li>Der Cursor ist invertiert. Beispielsweise zeigt das Radiererende des Stifts auf die Oberfläche (Wert = 2).</li><li>Nicht verwendet (Wert = 4).</li><li>Die Schaltfläche "Button" wird gedrückt (Wert = 8).</li></ul> | 
| GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID<br /> | Die Gerätekontakt-ID für ein Paket.<br /> | 
| GUID_SERIAL_NUMBER<br /> | Identifiziert das Paket. Dies ist der gleiche Wert, den Sie zum Abrufen des Pakets aus der Paketwarteschlange verwenden.<br /> | 
| GUID_TANGENT_PRESSURE<br /> | Die GUID für das PacketProperty-Objekt, das den Druck der Stiftspitze entlang der Ebene der Tablettoberfläche darstellt.<br /> | 
| GUID_TIMER_TICK<br /> | Zeitpunkt, zu dem das Paket generiert wurde.<br /> | 
| GUID_TWIST_ORIENTATION<br /> | Drehung des Cursors im Uhrzeigersinn um seine eigene Achse.<br /> | 
| GUID_X<br /> | Die x-Koordinate im Tabletkoordinatenraum. Jedes Paket enthält diese Eigenschaft standardmäßig. Der Ursprung (0,0) des Tablets ist die linke obere Ecke.<br /> | 
| GUID_X_TILT_ORIENTATION<br /> | Bei einem Stiftcursor ist die x-Neigungsausrichtung der Winkel zwischen der y-, z-Ebene und dem Stift und der y-Achsenebene. Der Wert ist 0, wenn der Stift an der Zeichenoberfläche liegt, und ist positiv, wenn sich der Stift rechts von perpendular befindet.<br /> | 
| GUID_Y<br /> | Die y-Koordinate im Tablettkoordinatenraum. Jedes Paket enthält diese Eigenschaft standardmäßig. Der Ursprung (0,0) des Tablets ist die linke obere Ecke.<br /> | 
| GUID_Y_TILT_ORIENTATION<br /> | Bei einem Stiftcursor ist die y-Neigungsausrichtung der Winkel zwischen der x,z-Ebene und dem Stift und der X-Achsenebene. Der Wert ist 0, wenn der Stift an die Zeichenoberfläche gerichtet ist, und ist positiv, wenn der Stift nach oben oder vom Benutzer entfernt ist.<br /> | 
| GUID_Z<br /> | Die Z-Koordinate oder der Abstand der Stiftspitze von der Tablettoberfläche. Der <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong></strong></a> PROPERTY_UNITS-Enumerationstyp bestimmt die Maßeinheit für diese Eigenschaft. <br /> | 




 

> [!Note]  
> Das TangentPressure-Feld stellt den Druck entlang der Ebene der Tablettoberfläche dar. Das Feld NormalPressure stellt den Druck dar, der der Ebene der Tablettoberfläche entspricht.

 

 

 




