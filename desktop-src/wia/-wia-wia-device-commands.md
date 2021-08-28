---
description: Die folgenden Konstanten bilden den Satz gültiger WIA-Hardwaregerätebefehle (Windows Image Acquisition).
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: WIA-Gerätebefehle (Wiadef.h)
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
ms.openlocfilehash: eed0cb3e01850ebdce87c026176da9fe2c637eaf7fc532383bbe4582d3b5824c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813240"
---
# <a name="wia-device-commands"></a>WIA-Gerätebefehle

Die folgenden Konstanten bilden den Satz gültiger WIA-Hardwaregerätebefehle (Windows Image Acquisition).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante</th>
<th style="text-align: left;">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl> <dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </dl></td>
<td style="text-align: left;">Bewirkt, dass der Minitreiber des Geräts zwischengespeicherte Elemente mit dem Hardwaregerät synchronisiert. Wenn das Gerät die <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem::AnalyzeItem-Methode</strong></a> unterstützt, bewirkt die Ausgabe dieses Befehls, dass der Minitreiber die Analyseergebnisse verwirft und das Element auf seinen ursprünglichen Zustand zurücksetzt. Dieser Befehl muss von allen Treibern unterstützt werden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl> <dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </dl></td>
<td style="text-align: left;">Bewirkt, dass ein WIA-Gerät ein Image erhält.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl> <dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </dl></td>
<td style="text-align: left;">Weist das Gerät an, alle Elemente zu löschen, die aus der Struktur der <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem-Objekte</strong></a> gelöscht werden können, die das Gerät darstellen. Das Löschen von Element wird verhindert, indem die Eigenschaften des Elements festgelegt werden. Weitere Informationen finden Sie unter <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage::SetPropertyStream</strong></a> und <a href="-wia-property-attributes.md">Eigenschaftenattribute.</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl> <dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">Wird für Dokumentscanner verwendet. Bewirkt, dass der Scanner die nächste Seite im Dokumenthandler lädt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl> <dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">Wird für Dokumentscanner verwendet. Weist das Gerät an, alle verbleibenden Seiten im Dokumenthandler zu entladen. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl> <dt><strong>WIA_CMD_START_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Wird für Dokumentscanner verwendet, die über einen Seitenfeeder verfügen. Weist das Gerät an, den Feeder-Motor zu starten. Dieses Feature ist ab Windows 8 verfügbar.<br/>
<blockquote>
[!Note]<br />
Der WIA-Minitreiber muss diesen Befehl ablehnen und <strong>WIA_ERROR_INVALID_COMMAND</strong> zurückgeben, wenn die <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL-Eigenschaft</strong></a> nicht unterstützt wird oder auf WIA_FEEDER_CONTROL_AUTO festgelegt ist.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl> <dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Wird für Dokumentscanner verwendet, die über einen Seitenfeeder verfügen. Weist das Gerät an, den Feeder-Motor zu beenden. Dieses Feature ist ab Windows 8 verfügbar.<br/>
<blockquote>
[!Note]<br />
Der WIA-Minitreiber muss diesen Befehl ablehnen und <strong>WIA_ERROR_INVALID_COMMAND</strong> zurückgeben, wenn die <strong>WIA_IPS_FEEDER_CONTROL-Eigenschaft</strong> nicht unterstützt wird oder auf WIA_FEEDER_CONTROL_AUTO festgelegt ist.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl> <dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Wird für Dokumentscanner verwendet, die über einen Seitenfeeder verfügen. Weist das Gerät an, den Feeder-Motor anzuhalten. Dieses Feature ist ab Windows 8 verfügbar.<br/>
<blockquote>
[!Note]<br />
Der WIA-Minitreiber muss diesen Befehl ablehnen und <strong>WIA_ERROR_INVALID_COMMAND</strong> zurückgeben, wenn die <strong>WIA_IPS_FEEDER_CONTROL-Eigenschaft</strong> nicht unterstützt wird oder auf WIA_FEEDER_CONTROL_AUTO festgelegt ist.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 
