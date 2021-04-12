---
description: Definiert Werte, die die Paket Eigenschaften angeben.
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: Packetpropertyguids-Konstanten (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadb664cb3783932dc2e7063d7cfab07133ad9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218359"
---
# <a name="packetpropertyguids-constants"></a>Packetpropertyguids-Konstanten

Definiert Werte, die die Paket Eigenschaften angeben. Das Tablet pcapi verwendet Global Unique Identifier (GUIDs), um Paket Eigenschaften zu identifizieren, die in com Konstante Zeichen folgen sind.

In C++ können Sie auf diese Konstanten in der Header Datei "msink AUT. h" zugreifen, die sich im <systemdrive> \\ Verzeichnis "Programme \\ Microsoft SDKs \\ Windows \\ v 6.0 include" befindet, \\ Wenn Sie das SDK am Standard Speicherort installiert haben. In C++ sind diese Konstanten WCHARs, nicht bstrins. Konvertieren Sie diese vor der Verwendung in bstraus. Weitere Informationen zum BSTR-Datentyp finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).

In der folgenden Tabelle sind die verfügbaren Felder der Paket Eigenschaften Globally Unique Identifier (GUID) aufgelistet. Verwenden Sie diese GUIDs, um anzugeben, welche Eigenschaften das Paket enthält, wenn Sie den Tablet-Kontext erstellen. Um den Bereich und die Auflösung einer Eigenschaft zu ermitteln, müssen Sie die [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) -Methode aufrufen. Die Konstanten in der Tabelle unten, beginnend mit "Str \_ ", sind Zeichen folgen Darstellungen der entsprechenden binären Konstanten, die in derselben Tabellenzelle angezeigt werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl> <dt><strong>STR_GUID_X oder GUID_PACKETPROPERTY_GUID_X</strong></dt> </dl></td>
<td style="text-align: left;">Die x-Koordinate im tablettkoordinatenbereich. Jedes Paket enthält diese Eigenschaft standardmäßig. Der Ursprung (0,0) des Tablets ist die linke obere Ecke.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <dt><strong>STR_GUID_Y oder GUID_PACKETPROPERTY_GUID_Y</strong></dt> </dl></td>
<td style="text-align: left;">Die y-Koordinate im tablettkoordinatenbereich. Jedes Paket enthält diese Eigenschaft standardmäßig. Der Ursprung (0,0) des Tablets ist die linke obere Ecke.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <dt><strong>STR_GUID_Y oder GUID_PACKETPROPERTY_GUID_Y</strong></dt> </dl></td>
<td style="text-align: left;">Die y-Koordinate im tablettkoordinatenbereich. Jedes Paket enthält diese Eigenschaft standardmäßig. Der Ursprung (0,0) des Tablets ist die linke obere Ecke.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl> <dt><strong>STR_GUID_Z oder GUID_PACKETPROPERTY_GUID_Z</strong></dt> </dl></td>
<td style="text-align: left;">Die z-Koordinate oder den Abstand der Stift Spitze von der Tablet-Oberfläche. Der <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> -Enumerationstyp bestimmt die Maßeinheit für diese Eigenschaft.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl> <dt><strong>STR_GUID_PAKETSTATUS oder GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </dl></td>
<td style="text-align: left;">Enthält mindestens einen der folgenden Flagwerte:<br/>
<ul>
<li>Der Cursor berührt die Zeichen Oberfläche (Wert = 1).</li>
<li>Der Cursor wird umgekehrt. Beispielsweise zeigt das Ende des Stifts auf die Oberfläche (Wert = 2).</li>
<li>Nicht verwendet (Wert = 4).</li>
<li>Die Schaltfläche "Barrel" wird gedrückt (Wert = 8).</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <dt><strong>STR_GUID_TIMERTICK oder GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </dl></td>
<td style="text-align: left;">Der Zeitpunkt, zu dem das Paket generiert wurde.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <dt><strong>STR_GUID_TIMERTICK oder GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </dl></td>
<td style="text-align: left;">Der Zeitpunkt, zu dem das Paket generiert wurde.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl> <dt><strong>STR_GUID_SERIALNUMBER oder GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </dl></td>
<td style="text-align: left;">Die Paket Eigenschaft zum Identifizieren des Pakets.<br/> Dies ist derselbe Wert, den Sie verwenden, um das Paket aus der Paket Warteschlange abzurufen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl> <dt><strong>STR_GUID_NORMALPRESSURE oder GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </dl></td>
<td style="text-align: left;">Der Druck der Stift Spitze senkrecht zur Tablet-Oberfläche.<br/> Je größer der Druck der Stift Spitze ist, desto mehr frei Hand Eingaben werden gezeichnet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl> <dt><strong>STR_GUID_TANGENTPRESSURE oder GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </dl></td>
<td style="text-align: left;">Der Druck der Stift Spitze auf der Ebene der Tablet-Oberfläche.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl> <dt><strong>STR_GUID_BUTTONPRESSURE oder GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </dl></td>
<td style="text-align: left;">Der Druck auf eine Druck Schaltfläche.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl> <dt><strong>STR_GUID_XTILTORIENTATION oder GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Der Winkel zwischen der y-, der z-Ebene und dem Stift und der y-Achsen Ebene.<br/> Gilt für einen Stift Cursor.<br/> Der Wert ist 0 (null), wenn der Stift senkrecht zur Zeichen Oberfläche ist und positiv ist, wenn sich der Stift rechts von senkrecht befindet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl> <dt><strong>STR_GUID_YTILTORIENTATION oder GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Der Winkel zwischen der x-, der z-Ebene und der Ebene des Stifts und der x-Achse.<br/> Gilt für einen Stift Cursor.<br/> Der Wert ist 0 (null), wenn der Stift senkrecht zur Zeichnungs Oberfläche ist und positiv ist, wenn sich der Stift über dem Benutzer befindet oder nicht.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl> <dt><strong>STR_GUID_AZIMUTHORIENTATION oder GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Die Drehung des Cursors im Uhrzeigersinn um die z-Achse durch einen vollständigen kreisförmigen Bereich.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl> <dt><strong>STR_GUID_ALTITUDEORIENTATION oder GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Der Winkel zwischen der Achse des Stifts und der Oberfläche des Tablets.<br/> Der Wert ist 0 (null), wenn der Stift parallel zur Oberfläche und 90 ist, wenn der Stift senkrecht zur Oberfläche ist.<br/> Die Werte sind negativ, wenn der Stift invertiert wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl> <dt><strong>STR_GUID_TWISTORIENTATION oder GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Die Drehung des Cursors im Uhrzeigersinn um die eigene Achse.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl> <dt><strong>STR_GUID_PITCHROTATION oder GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </dl></td>
<td style="text-align: left;">Die Paket Eigenschaft, die angibt, ob die Spitze oberhalb oder unterhalb einer horizontalen Linie liegt, die senkrecht zur Schreibfläche ist.<br/>
<blockquote>
[!Note]<br />
Hierfür ist ein 3D-Digitalisierer erforderlich.
</blockquote>
<br/> Der Wert ist positiv, wenn sich die Spitze oberhalb der Linie befindet, und negativ, wenn Sie sich unterhalb der Linie befindet. Wenn Sie z. b. den Stift vor Ihnen halten und auf eine imaginäre Wand schreiben, ist die Tonhöhe positiv, wenn der Tipp über einer Linie liegt, die von Ihnen bis zur Wand reicht.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl> <dt><strong>STR_GUID_ROLLROTATION oder GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </dl></td>
<td style="text-align: left;">Die Drehung im Uhrzeigersinn um die eigene Achse. <br/>
<blockquote>
[!Note]<br />
Hierfür ist ein 3D-Digitalisierer erforderlich.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <dt><strong>STR_GUID_YAWROTATION oder GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </dl></td>
<td style="text-align: left;">Der Winkel des Stifts links oder rechts um den Mittelpunkt der horizontalen Achse, wenn der Stift horizontal ist.<br/>
<blockquote>
[!Note]<br />
Hierfür ist ein 3D-Digitalisierer erforderlich.
</blockquote>
<br/> Wenn Sie den Stift vor Ihnen halten und auf eine imaginäre Wand schreiben, gibt 0 (null), dass der Stift senkrecht zur Wand ist. Der Wert ist negativ, wenn der Tipp Links von senkrecht und positiv ist, wenn der Tipp rechts von senkrecht ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <dt><strong>STR_GUID_YAWROTATION oder GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </dl></td>
<td style="text-align: left;">Der Winkel des Stifts links oder rechts um den Mittelpunkt der horizontalen Achse, wenn der Stift horizontal ist.<br/>
<blockquote>
[!Note]<br />
Hierfür ist ein 3D-Digitalisierer erforderlich.
</blockquote>
<br/> Wenn Sie den Stift vor Ihnen halten und auf eine imaginäre Wand schreiben, gibt 0 (null), dass der Stift senkrecht zur Wand ist. Der Wert ist negativ, wenn der Tipp Links von senkrecht und positiv ist, wenn der Tipp rechts von senkrecht ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl> <dt><strong>STR_GUID_WIDTH oder GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </dl></td>
<td style="text-align: left;">Die Breite des Kontakt Bereichs für einen Fingerabdruck-Digitalisierer.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl> <dt><strong>STR_GUID_HEIGHT oder GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </dl></td>
<td style="text-align: left;">Die Höhe des Kontakt Bereichs für einen Fingerabdruck-Digitalisierer.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl> <dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE oder GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </dl></td>
<td style="text-align: left;">Das Maß an Vertrauen, dass es Fingerkontakt für einen Touch-Digitalisierer gab.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl> <dt><strong>STR_GUID_DEVICE_CONTACT_ID oder GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </dl></td>
<td style="text-align: left;">Der Bezeichner des Geräte Kontakts für ein Paket.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Alle Paket Werte, die von der Tablet-Hardware stammen, sind 32-Bit-Ganzzahlen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IsPacketPropertySupported-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[**GetPropertyMetrics-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[**Iinktablet-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




