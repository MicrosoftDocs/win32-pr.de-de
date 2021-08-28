---
description: Definiert Werte, die die Paketeigenschaften angeben.
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: PacketPropertyGuids-Konstanten (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b88a59d63bc8b45ea04e133f0d002fa86e35e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481076"
---
# <a name="packetpropertyguids-constants"></a>PacketPropertyGuids-Konstanten

Definiert Werte, die die Paketeigenschaften angeben. Die Tablet PCAPI verwendet GUIDs (Globally Unique Identifiers), um Paketeigenschaften zu identifizieren, bei denen es sich in COM um konstante Zeichenfolgen handelt.

In C++ können Sie auf diese Konstanten in der Headerdatei Msinkaut.h zugreifen, die sich im Verzeichnis <systemdrive> Programme \\ Microsoft \\ SDKs Windows \\ \\ v6.0 \\ Include befindet, wenn Sie das SDK am Standardspeicherort installiert haben. In C++ sind diese Konstanten WCHARs, nicht BSTRs. Konvertieren Sie sie vor der Verwendung in BSTRs. Weitere Informationen zum BSTR-Datentyp finden Sie unter [Verwenden der COM-Bibliothek](using-the-com-library.md).

In der folgenden Tabelle sind die verfügbaren Felder für die Paketeigenschaft globally unique identifier (GUID) aufgeführt. Verwenden Sie diese GUIDs, um anzugeben, welche Eigenschaften das Paket enthält, wenn Sie den Tablet-Kontext erstellen. Um den Bereich und die Auflösung einer Eigenschaft zu bestimmen, rufen Sie die [**GetPropertyMetrics-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) auf. Die Konstanten in der folgenden Tabelle, die mit "STR" beginnen, sind Zeichenfolgendarstellungen der entsprechenden binären Konstanten, die \_ in derselben Tabellenzelle angezeigt werden.




| Konstante | BESCHREIBUNG | 
|----------|-------------|
| <span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl><dt><strong>STR_GUID_X oder GUID_PACKETPROPERTY_GUID_X</strong></dt></dl> | Die x-Koordinate im Tabletkoordinatenraum. Jedes Paket enthält diese Eigenschaft standardmäßig. Der Ursprung (0,0) des Tablets ist die linke obere Ecke.<br /> | 
| <span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl><dt><strong>STR_GUID_Y oder GUID_PACKETPROPERTY_GUID_Y</strong></dt></dl> | Die y-Koordinate im Tablettkoordinatenraum. Jedes Paket enthält diese Eigenschaft standardmäßig. Der Ursprung (0,0) des Tablets ist die linke obere Ecke.<br /> | 
| <span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl><dt><strong>STR_GUID_Y oder GUID_PACKETPROPERTY_GUID_Y</strong></dt></dl> | Die y-Koordinate im Tablettkoordinatenraum. Jedes Paket enthält diese Eigenschaft standardmäßig. Der Ursprung (0,0) des Tablets ist die linke obere Ecke.<br /> | 
| <span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl><dt><strong>STR_GUID_Z oder GUID_PACKETPROPERTY_GUID_Z</strong></dt></dl> | Die Z-Koordinate oder der Abstand der Stiftspitze von der Tablettoberfläche. Der <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit-Enumerationstyp</strong></a> bestimmt die Maßeinheit für diese Eigenschaft.<br /> | 
| <span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl><dt><strong>STR_GUID_PAKETSTATUS oder GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt></dl> | Enthält mindestens einen der folgenden Flagwerte:<br /><ul><li>Der Cursor berührt die Zeichenoberfläche (Wert = 1).</li><li>Der Cursor ist invertiert. Beispielsweise zeigt das Radiererende des Stifts auf die Oberfläche (Wert = 2).</li><li>Nicht verwendet (Wert = 4).</li><li>Die Schaltfläche "Button" wird gedrückt (Wert = 8).</li></ul> | 
| <span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl><dt><strong>STR_GUID_TIMERTICK oder GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt></dl> | Die Zeit, zu der das Paket generiert wurde.<br /> | 
| <span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl><dt><strong>STR_GUID_TIMERTICK oder GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt></dl> | Die Zeit, zu der das Paket generiert wurde.<br /> | 
| <span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl><dt><strong>STR_GUID_SERIALNUMBER oder GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt></dl> | Die Paketeigenschaft zum Identifizieren des Pakets.<br /> Dies ist der gleiche Wert, den Sie zum Abrufen des Pakets aus der Paketwarteschlange verwenden.<br /> | 
| <span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl><dt><strong>STR_GUID_NORMALPRESSURE oder GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt></dl> | Der Druck der Stiftspitze auf der Tablettoberfläche.<br /> Je größer der Druck auf der Stiftspitze ist, desto mehr Ink wird gezeichnet.<br /> | 
| <span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl><dt><strong>STR_GUID_TANGENTPRESSURE oder GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt></dl> | Der Druck der Stiftspitze entlang der Ebene der Tablettoberfläche.<br /> | 
| <span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl><dt><strong>STR_GUID_BUTTONPRESSURE oder GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt></dl> | Der Druck auf einer druckempfindlichen Schaltfläche.<br /> | 
| <span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl><dt><strong>STR_GUID_XTILTORIENTATION oder GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt></dl> | Der Winkel zwischen der y-, z-Ebene und dem Stift und der y-Achsenebene.<br /> Gilt für einen Stiftcursor.<br /> Der Wert ist 0, wenn der Stift an der Zeichenoberfläche liegt, und ist positiv, wenn sich der Stift rechts von perpendular befindet.<br /> | 
| <span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl><dt><strong>STR_GUID_YTILTORIENTATION oder GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt></dl> | Der Winkel zwischen der x-, z-Ebene und dem Stift und der X-Achsenebene.<br /> Gilt für einen Stiftcursor.<br /> Der Wert ist 0, wenn der Stift an die Zeichenoberfläche gerichtet ist, und ist positiv, wenn der Stift aufwärts oder vom Benutzer entfernt ist.<br /> | 
| <span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl><dt><strong>STR_GUID_AZIMUTHORIENTATION oder GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt></dl> | Die Drehung des Cursors im Uhrzeigersinn um die Z-Achse durch einen vollständigen kreisförmigen Bereich.<br /> | 
| <span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl><dt><strong>STR_GUID_ALTITUDEORIENTATION oder GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt></dl> | Der Winkel zwischen der Achse des Stifts und der Oberfläche des Tablets.<br /> Der Wert ist 0, wenn der Stift parallel zur Oberfläche ist, und 90, wenn der Stift an der Oberfläche durchlässig ist.<br /> Die Werte sind negativ, wenn der Stift invertiert wird.<br /> | 
| <span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl><dt><strong>STR_GUID_TWISTORIENTATION oder GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt></dl> | Die Drehung des Cursors im Uhrzeigersinn um seine eigene Achse.<br /> | 
| <span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl><dt><strong>STR_GUID_PITCHROTATION oder GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt></dl> | Die Paketeigenschaft, die angibt, ob sich die Spitze über oder unter einer horizontalen Linie befindet, die an der Schreiboberfläche ausgerichtet ist.<br /><blockquote>[!Note]<br />Dies erfordert einen 3D-Digitizer.</blockquote><br /> Der Wert ist positiv, wenn sich der Trinkgeldwert über der Zeile befindet, und negativ, wenn er unter der Linie liegt. Wenn Sie z. B. den Stift vor sich halten und auf eine imaginäre Wand schreiben, ist die Tonhöhe positiv, wenn sich der Tipp über einer Linie befindet, die sich von Ihnen bis zur Wand erstreckt.<br /> | 
| <span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl><dt><strong>STR_GUID_ROLLROTATION oder GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt></dl> | Die Drehung des Stifts um seine eigene Achse im Uhrzeigersinn. <br /><blockquote>[!Note]<br />Dies erfordert einen 3D-Digitizer.</blockquote><br /> | 
| <span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl><dt><strong>STR_GUID_YAWROTATION oder GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt></dl> | Der Winkel des Stifts links oder rechts um die Mitte der horizontalen Achse, wenn der Stift horizontal ist.<br /><blockquote>[!Note]<br />Dies erfordert einen 3D-Digitizer.</blockquote><br /> Wenn Sie den Stift vor sich halten und auf eine imaginäre Wand schreiben, zeigt null yaw an, dass der Stift an der Wand liegt. Der Wert ist negativ, wenn sich der Trinkgeld links von perpendular befindet, und positiv, wenn sich der Trinkgeld rechts von perpendular befindet.<br /> | 
| <span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl><dt><strong>STR_GUID_YAWROTATION oder GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt></dl> | Der Winkel des Stifts links oder rechts um die Mitte der horizontalen Achse, wenn der Stift horizontal ist.<br /><blockquote>[!Note]<br />Dies erfordert einen 3D-Digitizer.</blockquote><br /> Wenn Sie den Stift vor sich halten und auf eine imaginäre Wand schreiben, zeigt null yaw an, dass der Stift an der Wand liegt. Der Wert ist negativ, wenn sich der Trinkgeld links von perpendular befindet, und positiv, wenn sich der Trinkgeld rechts von perpendular befindet.<br /> | 
| <span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl><dt><strong>STR_GUID_WIDTH oder GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt></dl> | Die Breite des Kontaktbereichs auf einem Touch-Digitizer.<br /> | 
| <span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl><dt><strong>STR_GUID_HEIGHT oder GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt></dl> | Die Höhe des Kontaktbereichs auf einem Touch-Digitizer.<br /> | 
| <span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE oder GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt></dl> | Das Maß an Vertrauen, das ein Fingerkontakt auf einem Touch-Digitizer auftippte.<br /> | 
| <span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl><dt><strong>STR_GUID_DEVICE_CONTACT_ID oder GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt></dl> | Die Gerätekontakt-ID für ein Paket.<br /> | 




## <a name="remarks"></a>Hinweise

> [!Note]  
> Alle Paketwerte, die von der Tablethardware kommen, sind ganze Zahlen der Größe 32 Bit.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IsPacketPropertySupported-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[**GetPropertyMetrics-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[**IInkTablet-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




