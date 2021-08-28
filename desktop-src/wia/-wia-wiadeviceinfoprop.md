---
description: 'Geräteinformationseigenschaftskonstten : Geräteinformationseigenschaften sind Eigenschaften, die das Setup und die Installation des Geräts beschreiben.'
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: Geräteinformationseigenschaftskonst constants (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DIP_DEV_ID
- WIA_DIP_VEND_DESC
- WIA_DIP_DEV_DESC
- WIA_DIP_DEV_TYPE
- WIA_DIP_PORT_NAME
- WIA_DIP_DEV_NAME
- WIA_DIP_SERVER_NAME
- WIA_DIP_REMOTE_DEV_ID
- WIA_DIP_UI_CLSID
- WIA_DIP_HW_CONFIG
- WIA_DIP_BAUDRATE
- WIA_DIP_STI_GEN_CAPABILITIES
- WIA_DIP_WIA_VERSION
- WIA_DIP_DRIVER_VERSION
- WIA_DIP_PNP_ID
- WIA_DIP_STI_DRIVER_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 29db0a527146218e19b3fe583fd48936f71dac29
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623696"
---
# <a name="device-information-property-constants"></a>Eigenschaftenkonst constants für Geräteinformationen

Geräteinformationseigenschaften sind Eigenschaften, die das Setup und die Installation des Geräts beschreiben. Diese Eigenschaften sind über die [**Schnittstellen IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) oder [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) sowie über das Stammelement verfügbar. Geräteinformationseigenschaften haben das Präfix "WIA DIP" (Device Information Property) und werden von Windows \_ \_ Image Acquisition (WIA) bereitgestellt. Zu Skriptzwecken verwenden diese Konstanten das Präfix "DeviceInfo" und sind Teil des [aufzählten WiaDeviceInfoPropertyId-Typs.](-wia-wiadeviceinfopropertyid.md) Der entsprechende Membername aus dieser Skriptenumeration wird in Klammern neben dem C/C++-Konstantennamen in der folgenden Liste angezeigt.



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
<td ><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </dl></td>
<td >Die Geräte-ID-Zeichenfolge für den WIA-Minitreiber. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.<br/> Typ: VT_BSTR, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </dl></td>
<td >Die Herstellerbeschreibungszeichenfolge für den WIA-Minitreiber. Die Herstellerbeschreibung wird aus der INF-Datei ermittelt. Eine Anwendung liest diese Eigenschaft, um eine Beschreibung des Geräteanbieters zu erhalten. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.<br/> Typ: VT_BSTR, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </dl></td>
<td >Die Gerätebeschreibungszeichenfolge für den WIA-Minitreiber. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Die gerätebeschreibungszeichenfolge, die diese Eigenschaft enthält, wird aus der INF-Datei ermittelt. Eine Anwendung liest diese Eigenschaft, um eine Beschreibung des Geräts zu erhalten.<br/> Typ: VT_BSTR, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </dl></td>
<td >Der Gerätetyp und der Geräteuntertyp. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Verwenden Sie GET_STIDEVICE_TYPE Makro , um den Gerätetyp zu erhalten. Der Gerätetyp und der Untertyp werden aus der INF-Datei ermittelt. Eine Anwendung liest diese Eigenschaft, um zu bestimmen, ob sie einen Scanner, eine Kamera oder ein Videogerät verwendet.<br/> Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> Derzeit werden Gerätetypen wie folgt definiert. Das Sternchen * gibt an, dass der Gerätetyp von Windows Vista und höher nicht unterstützt wird. Das doppelte Sternchen ** gibt an, dass der Gerätetyp von Windows Server 2003, Windows Vista oder höher nicht unterstützt wird. <br/> 
<table>
<thead>
<tr class="header">
<th>Typ</th>
<th>Wert</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>StiDeviceTypeDefault</td>
<td>0x0000</td>
<td>Standardgerät</td>
</tr>
<tr class="even">
<td>StiDeviceTypeScanner</td>
<td>0x0001</td>
<td>Scannergerät (siehe <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES,</strong></a> um zu ermitteln, ob der Scanner flach oder mit Blättern ausgestattet ist.)</td>
</tr>
<tr class="odd">
<td>StiDeviceTypeDigitalCamera*</td>
<td>0x0002</td>
<td>Kameragerät</td>
</tr>
<tr class="even">
<td>StiDeviceTypeStreamingVideo**</td>
<td>0x0003</td>
<td>Videogerät</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </dl></td>
<td ><p>Der Portname des installierten Geräts, der vom Kernelmodustreiber zugewiesen wird, der das Gerät betreibt. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Eine Anwendung liest diese Eigenschaft, um den Portnamen zu bestimmen.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </dl></td>
<td ><p>Der Name des Geräts. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Der in dieser Eigenschaft enthaltene Gerätename wird aus der INF-Datei ermittelt. Eine Anwendung liest diese Eigenschaft, um den Namen des Geräts zu erhalten.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </dl></td>
<td ><p>Der Name des Servers, auf dem der WIA-Minitreiber ausgeführt wird. Diese Eigenschaft ist optional für Windows XP und höher.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </dl></td>
<td ><p>Die Geräte-ID des WIA-Geräts, das auf einem Remotecomputer installiert ist. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Sie wird nur intern vom WIA-Dienst verwendet.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </dl></td>
<td ><p>Die vom Anbieter bereitgestellte CLSID für jedes COM-Objekt der Benutzeroberflächenerweiterung, das mit dem WIA-Minitreiber installiert wird. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Der in dieser Eigenschaft enthaltene CLSID-Wert der Benutzeroberfläche wird aus der INF-Datei ermittelt. Wenn keine UI-CLSID angegeben ist, stellt der WIA-Dienst einen Standardwert zur Verfügung. Diese Eigenschaft wird nur intern vom WIA-Dienst verwendet, wenn die Benutzeroberfläche angezeigt wird.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </dl></td>
<td ><p>Der Verbindungstyp, den das Gerät verwendet. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft, und nur der WIA-Dienst kann sie ändern.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die -Eigenschaft kann die folgenden möglichen Werte haben.</p>

<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Generisches WDM-Gerät</td>
</tr>
<tr class="even">
<td>2</td>
<td>SCSI-Gerät</td>
</tr>
<tr class="odd">
<td>4</td>
<td>USB-Gerät</td>
</tr>
<tr class="even">
<td>8</td>
<td>Serielles Gerät</td>
</tr>
<tr class="odd">
<td>16</td>
<td>Paralleles Gerät</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </dl></td>
<td ><p>Die aktuelle Baudrateneinstellung für das Gerät. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Der Wert sollte Leer &quot; &quot; sein, wenn das Gerät nicht über ein serielles Kabel verbunden ist.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </dl></td>
<td ><p>Die generischen STI-Funktionen für das Gerät, die aus der INF-Datei abgerufen wurden. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Eine Anwendung liest diese Eigenschaft, um die generischen STI-Funktionen des Geräts zu bestimmen.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </dl></td>
<td ><p>Die Nummer (als Zeichenfolge) der aktuellen WIA-Version, die auf dem System installiert ist. Eine Anwendung liest diese Eigenschaft, um die version von WIA zu bestimmen, die auf dem System installiert ist. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft ist in Windows XP und höher verfügbar.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </dl></td>
<td ><p>Die aktuelle DLL-Version des WIA-Minitreibers. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft ist in Windows XP und höher verfügbar.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </dl></td>
<td ><p>Die aktuelle PnP-ID für das Gerät. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft ist in Windows Vista und höher verfügbar.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </dl></td>
<td ><p>Die generische Version des STI-Treibers. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Eine Anwendung liest diese Eigenschaft, um die generische Version des STI-Treibers zu bestimmen. Diese Eigenschaft ist in Windows Vista und höher verfügbar.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




