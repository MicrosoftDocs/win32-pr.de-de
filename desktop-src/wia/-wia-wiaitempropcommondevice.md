---
description: Zusätzlich zu den Eigenschaften von Geräteinformationen verfügen Windows-Abbild Erfassungsgeräte (WIA) über Eigenschaftswerte, die in der Registrierung gespeichert sind und von Anwendungen gelesen und geschrieben werden.
ms.assetid: 9948318b-7171-45fa-b46f-48f9357fdb32
title: Allgemeine Geräte Eigenschafts Konstanten (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPA_CONNECT_STATUS
- WIA_DPA_DEVICE_TIME
- WIA_DPA_FIRMWARE_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 23c8faf8317fa7bf2008baffe3e6bf0e89a27a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526399"
---
# <a name="common-device-property-constants"></a>Allgemeine Geräte Eigenschafts Konstanten

Zusätzlich zu den Eigenschaften von Geräteinformationen verfügen Windows-Abbild Erfassungsgeräte (WIA) über Eigenschaftswerte, die in der Registrierung gespeichert sind und von Anwendungen gelesen und geschrieben werden. Sie sind dem [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Objekt oder dem [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt zugeordnet. Geräteeigenschaften stellen Geräteinformationen dar, z. b. Verbindungsstatus und Geräte Zeit. Jede Geräte Eigenschaft verfügt über eine zugeordnete Geräteeigenschaften Zeichenfolge.

Die hier aufgeführten Geräteeigenschaften Konstanten gelten für die meisten oder alle WIA-Hardware Geräte.

Das Präfix "WIA \_ DPA \_ " gibt eine Geräte Eigenschaft für alle Geräte an und ist die Benennungs Konvention, die in C/C++ verwendet wird. Bei der Skripterstellung verwenden diese Konstanten das Präfix "Device" und sind Teil des enumerierten Typs [wiaitempropertyid](-wia-wiaitempropertyid.md) . Der entsprechende Elementname aus dieser Skript Enumeration wird in Klammern neben dem Konstanten Namen C/C++ in der folgenden Liste angezeigt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante/Wert</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <dt><strong></strong></dt> <dt>Deviceconnectstatus</dt> WIA_DPA_CONNECT_STATUS </dl></td>
<td style="text-align: left;">Der aktuelle Verbindungsstatus für das Gerät. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.<br/> Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> Die-Eigenschaft kann die folgenden möglichen Werte aufweisen.<br/> 
<table>
<thead>
<tr class="header">
<th>Verbindungs Status</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DEVICE_NOT_CONNECTED</td>
<td>Das Gerät ist nicht verbunden.</td>
</tr>
<tr class="even">
<td>WIA_DEVICE_CONNECTED</td>
<td>Das Gerät ist verbunden und betriebsbereit.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>devicedevicetime</dt> </dl></td>
<td style="text-align: left;"><p>Die aktuelle Uhrzeit, die auf dem Gerät gespeichert ist. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>, Zugriff: Lese-/Schreibzugriff oder schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Diese Eigenschaft wird nur von Geräten mit einer internen Uhr unterstützt. Wenn die Geräteuhr festgelegt werden kann, lautet diese Eigenschaft Lese-/Schreibzugriff. Andernfalls ist sie schreibgeschützt.</p>
<p>WIA-Geräte melden Zeit in einer <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> -Struktur.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>devicefirmwareversion</dt> </dl></td>
<td style="text-align: left;"><p>Die Firmwareversion des Geräts. Dieser Wert muss ein Zeichen folgen Wert sein, z &quot; &quot; . b. 1.0.4 oder &quot; 1.0 ABC &quot; . Der Mini Treiber erstellt und verwaltet diese Eigenschaft. Wenn der WIA-Mini Treiber keine Versions Ressource bereitstellt, liefert der WIA-Dienst den Wert &quot; 0.0.0.0 &quot; als Standardwert. Eine Anwendung liest diese Eigenschaft, um die Version der WIA Mini Treiber-DLL zu ermitteln.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
