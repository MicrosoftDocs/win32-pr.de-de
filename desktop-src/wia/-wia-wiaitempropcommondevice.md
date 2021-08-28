---
description: Zusätzlich zu den Geräteinformationseigenschaften verfügen Windows WIA-Geräte (Image Acquisition) über Eigenschaftswerte, die in der Registrierung gespeichert sind, die Anwendungen lesen und schreiben.
ms.assetid: 9948318b-7171-45fa-b46f-48f9357fdb32
title: Allgemeine Geräteeigenschaftskonstanten (Wiadef.h)
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
ms.openlocfilehash: c5eda1266c8c99f1125e03dfbacc3eb325a69d1d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632178"
---
# <a name="common-device-property-constants"></a>Allgemeine Geräteeigenschaftskonstanten

Zusätzlich zu den Geräteinformationseigenschaften verfügen Windows WIA-Geräte (Image Acquisition) über Eigenschaftswerte, die in der Registrierung gespeichert sind, die Anwendungen lesen und schreiben. Sie sind dem [**IWiaItem-Objekt**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) oder [**dem IWiaItem2-Objekt**](-wia-iwiaitem2.md) zugeordnet. Geräteeigenschaften stellen Geräteinformationen wie Verbindungsstatus und Gerätezeit dar. Jeder Geräteeigenschaft ist eine Geräteeigenschaftenzeichenfolge zugeordnet.

Die hier aufgeführten Geräteeigenschaftskonstanten gelten für die meisten oder alle WIA-Hardwaregeräte.

Das Präfix "WIA \_ \_ DPA" gibt eine Geräteeigenschaft für Alle Geräte an und ist die benennungskonvention, die in C/C++ verwendet wird. Zu Skriptzwecken verwenden diese Konstanten das Präfix "Device" und sind Teil des Aufzählungstyps [WiaItemPropertyId.](-wia-wiaitempropertyid.md) Der entsprechende Membername aus dieser Skriptenumeration wird in Klammern neben dem C/C++-Konstantennamen in der folgenden Liste angezeigt.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Konstante/Wert</th>
<th >Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </dl></td>
<td >Der aktuelle Verbindungsstatus für das Gerät. Der Minitreiber erstellt und verwaltet diese Eigenschaft.<br/> Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> Die -Eigenschaft kann die folgenden möglichen Werte aufweisen.<br/> 
<table>
<thead>
<tr class="header">
<th>Verbinden Status</th>
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
<td ><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </dl></td>
<td ><p>Die aktuelle Uhrzeit, die auf dem Gerät gespeichert ist. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>, Zugriff: Lesen/Schreiben oder Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Diese Eigenschaft wird nur von Geräten unterstützt, die über eine interne Uhr verfügen. Wenn die Geräteuhr festgelegt werden kann, lautet diese Eigenschaft Lese-/Schreibzugriff. Andernfalls ist sie schreibgeschützt.</p>
<p>WIA-Geräte melden die Zeit in einer <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME-Struktur.</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </dl></td>
<td ><p>Die Firmwareversion des Geräts. Dieser Wert muss ein Zeichenfolgenwert sein, &quot; z.B. 1.0.4 &quot; oder &quot; 1.0abc. &quot; Der Minitreiber erstellt und verwaltet diese Eigenschaft. Wenn der WIA-Minitreiber keine Versionsressource ansteuert, stellt der WIA-Dienst standardmäßig den Wert &quot; 0.0.0.0 zur &quot; Verfügung. Eine Anwendung liest diese Eigenschaft, um die Version der WIA-Minitreiber-DLL zu bestimmen.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 
