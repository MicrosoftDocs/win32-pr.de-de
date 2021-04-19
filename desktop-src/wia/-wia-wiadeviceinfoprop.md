---
description: Geräte Informations Eigenschaften sind Eigenschaften, die das Setup und die Installation des Geräts beschreiben.
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: Eigenschaften Konstanten für Geräteinformationen (wiadef. h)
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
ms.openlocfilehash: 18c44bb310c2dcee5bb227e0885a71b58f5b362e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353092"
---
# <a name="device-information-property-constants"></a>Eigenschaften Konstanten für Geräteinformationen

Geräte Informations Eigenschaften sind Eigenschaften, die das Setup und die Installation des Geräts beschreiben. Diese Eigenschaften sind über die [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) -oder [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) -Schnittstelle und auch über das root-Element verfügbar. Den Eigenschaften für Geräteinformationen wird das Präfix "WIA \_ DIP \_ " (Geräte Informations Eigenschaft) vorangestellt, die von der Windows-Abbild Beschaffung (WIA) bereitgestellt werden. Zu Skript Zwecken verwenden diese Konstanten das Präfix "deviceInfo" und sind Teil des Enumerationstyps [wiadeviceinf opropertyid](-wia-wiadeviceinfopropertyid.md) . Der entsprechende Elementname aus dieser Skript Enumeration wird in Klammern neben dem Konstanten Namen C/C++ in der folgenden Liste angezeigt.



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
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <dt><strong>WIA_DIP_DEV_ID</strong></dt> (Geräte <dt>-</dt> ID) </dl></td>
<td style="text-align: left;">Die Geräte-ID-Zeichenfolge für den WIA-Mini Treiber. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.<br/> Typ: VT_BSTR, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <dt><strong>WIA_DIP_VEND_DESC</strong></dt> "Geräte- <dt>fovendde</dt> " </dl></td>
<td style="text-align: left;">Die Hersteller Beschreibungs Zeichenfolge für den WIA-Mini Treiber. Die Herstellerbeschreibung wird aus der INF-Datei abgerufen. Diese Eigenschaft wird von einer Anwendung gelesen, um eine Beschreibung des Geräte Anbieters zu erhalten. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.<br/> Typ: VT_BSTR, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>deviceingefodevdesc</dt> </dl></td>
<td style="text-align: left;">Die Geräte Beschreibungs Zeichenfolge für den WIA-Mini Treiber. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Die Geräte Beschreibungs Zeichenfolge, die diese Eigenschaft enthält, wird aus der INF-Datei abgerufen. Diese Eigenschaft wird von einer Anwendung gelesen, um eine Beschreibung des Geräts zu erhalten.<br/> Typ: VT_BSTR, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <dt><strong>WIA_DIP_DEV_TYPE</strong></dt> " <dt>deviceinfodevtype</dt> " </dl></td>
<td style="text-align: left;">Der Gerätetyp und der Geräte Untertyp. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Verwenden Sie das GET_STIDEVICE_TYPE-Makro, um den Gerätetyp zu erhalten. Gerätetyp und Untertyp werden aus der INF-Datei abgerufen. Eine Anwendung liest diese Eigenschaft, um zu bestimmen, ob Sie einen Scanner, eine Kamera oder ein Videogerät verwendet.<br/> Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> Derzeit werden Gerätetypen wie folgt definiert. Das Sternchen * gibt an, dass der Gerätetyp von Windows Vista und höher nicht unterstützt wird. Das doppelte Sternchen * * gibt an, dass der Gerätetyp weder von Windows Server 2003 noch von Windows Vista oder höher unterstützt wird. <br/> 
<table>
<thead>
<tr class="header">
<th>type</th>
<th>Wert</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Stide vicetypeer default</td>
<td>0x0000</td>
<td>Standardgerät</td>
</tr>
<tr class="even">
<td>Stide vicetypescanner</td>
<td>0x0001</td>
<td>Überprüfungs Gerät (Weitere Informationen finden Sie in den <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> , um zu ermitteln, ob die Überprüfung ein flatsheet oder eine Blatt Überprüfung ist)</td>
</tr>
<tr class="odd">
<td>Stide vicetyetdigitalcamera *</td>
<td>0x0002</td>
<td>Kamera Gerät</td>
</tr>
<tr class="even">
<td>Stidebug-Video * *</td>
<td>0x0003</td>
<td>Video Gerät</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <dt><strong>WIA_DIP_PORT_NAME</strong></dt> "Geräte <dt>Name</dt> " </dl></td>
<td style="text-align: left;"><p>Der Port Name des installierten Geräts, der durch den Kernelmodustreiber zugewiesen wird, der das Gerät bedient. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Eine Anwendung liest diese Eigenschaft, um den Portnamen zu ermitteln.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <dt><strong></strong></dt> <dt>Deviceinfodevname</dt> WIA_DIP_DEV_NAME </dl></td>
<td style="text-align: left;"><p>Der Name des Geräts. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Der in dieser Eigenschaft enthaltene Gerätename wird aus der INF-Datei abgerufen. Diese Eigenschaft wird von einer Anwendung gelesen, um den Namen des Geräts zu erhalten.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <dt><strong>WIA_DIP_SERVER_NAME</strong></dt> Geräte <dt>Name</dt> </dl></td>
<td style="text-align: left;"><p>Der Name des Servers, auf dem der WIA-Mini Treiber ausgeführt wird. Diese Eigenschaft ist optional für Windows XP und höher.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> "Geräte <dt>-</dt> ID" </dl></td>
<td style="text-align: left;"><p>Die Geräte-ID des WIA-Geräts, das auf einem Remote Computer installiert ist. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Sie wird nur intern vom WIA-Dienst verwendet.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <dt><strong>WIA_DIP_UI_CLSID</strong></dt> "Geräte- <dt>CLSID</dt> " </dl></td>
<td style="text-align: left;"><p>Die vom Hersteller bereitgestellte CLSID für alle COM-Objekte der UI-Erweiterung, die mit dem WIA-Mini Treiber installiert werden. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Der in dieser Eigenschaft enthaltene Benutzeroberflächen-CLSID-Wert wird aus der INF-Datei abgerufen. Wenn keine Benutzeroberflächen-CLSID angegeben ist, stellt der WIA-Dienst einen Standardwert bereit. Diese Eigenschaft wird nur intern vom WIA-Dienst verwendet, wenn die Benutzeroberfläche angezeigt wird.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <dt><strong>WIA_DIP_HW_CONFIG</strong></dt> "Geräte- <dt>/Konfigurations-config</dt> " </dl></td>
<td style="text-align: left;"><p>Der Verbindungstyp, der vom Gerät verwendet wird. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft, und nur der WIA-Dienst kann Sie ändern.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die-Eigenschaft kann die folgenden möglichen Werte aufweisen.</p>

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
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <dt><strong>WIA_DIP_BAUDRATE</strong></dt> (Geräte <dt>Einstellungs</dt> Paket) </dl></td>
<td style="text-align: left;"><p>Die aktuelle Baudrate-Einstellung für das Gerät. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Der Wert sollte leer sein, &quot; &quot; Wenn das Gerät nicht mit einem seriellen Kabel verbunden ist.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>deviceingefostigenfunktionalitäten</dt> </dl></td>
<td style="text-align: left;"><p>Die generischen STI-Funktionen für das Gerät, wie Sie aus der INF-Datei abgerufen werden. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft wird von einer Anwendung gelesen, um die generischen Verwaltungsfunktionen des Geräts zu ermitteln.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <dt><strong>WIA_DIP_WIA_VERSION</strong></dt> "Geräte- <dt>fowiaversion</dt> " </dl></td>
<td style="text-align: left;"><p>Die Zahl (als Zeichenfolge) der aktuellen WIA-Version, die auf dem System installiert ist. Eine Anwendung liest diese Eigenschaft, um die Version von WIA zu bestimmen, die auf dem System installiert ist. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft ist in Windows XP und höher verfügbar.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <dt><strong></strong></dt> <dt>Deviceingefodriverversion</dt> WIA_DIP_DRIVER_VERSION </dl></td>
<td style="text-align: left;"><p>Die aktuelle dll-Version des WIA-Mini Treibers. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft ist in Windows XP und höher verfügbar.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt></dt> "Geräte-ID" </dl></td>
<td style="text-align: left;"><p>Die aktuelle PNP-ID für das Gerät. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft ist in Windows Vista und höher verfügbar.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <dt><strong></strong></dt> <dt>Deviceingefostidriverversion</dt> WIA_DIP_STI_DRIVER_VERSION </dl></td>
<td style="text-align: left;"><p>Die Version des generischen STI-Treibers. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft. Eine Anwendung liest diese Eigenschaft, um die Version des generischen STI-Treibers zu ermitteln. Diese Eigenschaft ist in Windows Vista und höher verfügbar.</p>
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



 

 




