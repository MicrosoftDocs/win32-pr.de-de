---
description: Die folgenden Konstanten bilden den Satz gültiger Hardware Geräte Befehle zur Windows-Abbild Beschaffung (WIA).
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: WIA-Geräte Befehle (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CMD_SYNCHRONIZE
- WIA_CMD_TAKE_PICTURE
- WIA_CMD_DELETE_ALL_ITEMS
- WIA_CMD_CHANGE_DOCUMENT
- WIA_CMD_UNLOAD_DOCUMENT
- WIA_CMD_START_FEEDER
- WIA_CMD_STOP_FEEDER
- WIA_CMD_PAUSE_FEEDER
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 6e9e732520a256519ebcb21da84eac7ca8d8b630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862667"
---
# <a name="wia-device-commands"></a>WIA-Geräte Befehle

Die folgenden Konstanten bilden den Satz gültiger Hardware Geräte Befehle zur Windows-Abbild Beschaffung (WIA).



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
<td style="text-align: left;"><span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl> <dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </dl></td>
<td style="text-align: left;">Bewirkt, dass der Mini Treiber des Geräts zwischengespeicherte Elemente mit dem Hardware Gerät synchronisiert. Wenn das Gerät die <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>iwiaitem:: analyzeitem</strong></a> -Methode unterstützt, bewirkt die Ausgabe dieses Befehls, dass der Mini Treiber die Analyseergebnisse verworfen und das Element in seinen ursprünglichen Zustand zurücksetzt. Alle Treiber müssen diesen Befehl unterstützen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl> <dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </dl></td>
<td style="text-align: left;">Bewirkt, dass ein WIA-Gerät ein Image aberhält.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl> <dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </dl></td>
<td style="text-align: left;">Weist das Gerät an, alle Elemente zu löschen, die aus der Struktur von <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>iwiaitem</strong></a> -Objekten, die das Gerät darstellen, gelöscht werden können. Das Löschen von Elementen wird verhindert, indem die Eigenschaften des Elements festgelegt werden. Weitere Informationen finden Sie unter <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>iwiapropertystorage:: setpropertystream</strong></a> und <a href="-wia-property-attributes.md">Property-Attribute</a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl> <dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">Wird für Dokument Scanner verwendet. Bewirkt, dass der Scanner die nächste Seite in seinem Dokument Handler lädt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl> <dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">Wird für Dokument Scanner verwendet. Weist das Gerät an, alle verbleibenden Seiten im Dokument Handler zu entladen. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl> <dt><strong>WIA_CMD_START_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Wird für Dokument Scanner verwendet, die über einen Seiten feedertyp verfügen. Weist das Gerät an, den feedermotor zu starten. Diese Funktion ist ab Windows 8 verfügbar.<br/>
<blockquote>
[!Note]<br />
Der WIA-Mini Treiber muss diesen Befehl ablehnen und <strong>WIA_ERROR_INVALID_COMMAND</strong> zurückgeben, wenn die <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> -Eigenschaft nicht unterstützt wird oder auf WIA_FEEDER_CONTROL_AUTO festgelegt ist.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl> <dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Wird für Dokument Scanner verwendet, die über einen Seiten feedertyp verfügen. Weist das Gerät an, den feedermotor anzuhalten. Diese Funktion ist ab Windows 8 verfügbar.<br/>
<blockquote>
[!Note]<br />
Der WIA-Mini Treiber muss diesen Befehl ablehnen und <strong>WIA_ERROR_INVALID_COMMAND</strong> zurückgeben, wenn die <strong>WIA_IPS_FEEDER_CONTROL</strong> -Eigenschaft nicht unterstützt wird oder auf WIA_FEEDER_CONTROL_AUTO festgelegt ist.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl> <dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Wird für Dokument Scanner verwendet, die über einen Seiten feedertyp verfügen. Weist das Gerät an, den feedermotor anzuhalten. Diese Funktion ist ab Windows 8 verfügbar.<br/>
<blockquote>
[!Note]<br />
Der WIA-Mini Treiber muss diesen Befehl ablehnen und <strong>WIA_ERROR_INVALID_COMMAND</strong> zurückgeben, wenn die <strong>WIA_IPS_FEEDER_CONTROL</strong> -Eigenschaft nicht unterstützt wird oder auf WIA_FEEDER_CONTROL_AUTO festgelegt ist.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
