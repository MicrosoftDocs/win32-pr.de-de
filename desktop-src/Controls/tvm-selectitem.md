---
title: TVM_SELECTITEM Meldung (kommstrg. h)
description: Wählt das angegebene Struktur Ansichts Element aus, führt einen Bildlauf durch das Element durch oder zeichnet das Element im Stil neu, mit dem das Ziel eines Drag & Drop-Vorgangs angegeben wird.
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- Windows-Steuerelemente für TVM_SELECTITEM Meldung
topic_type:
- apiref
api_name:
- TVM_SELECTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94862b64a02cd8972e3da38a75282d99bbc1cbc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858730"
---
# <a name="tvm_selectitem-message"></a>TVM \_ SelectItem-Meldung

Wählt das angegebene Struktur Ansichts Element aus, führt einen Bildlauf durch das Element durch oder zeichnet das Element im Stil neu, mit dem das Ziel eines Drag & Drop-Vorgangs angegeben wird. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select)-, [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)-oder [**TreeView \_ selectdroptarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Aktionsflag. Dieser Parameter kann einen der folgenden Werte aufweisen:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt><strong>TVGN_CARET</strong></dt> </dl></td>
<td>Legt die Auswahl auf das angegebene Element fest. Das übergeordnete Fenster des Strukturansicht-Steuer Elements empfängt die <a href="tvn-selchanging.md">TVN_SELCHANGING</a> -und <a href="tvn-selchanged.md">TVN_SELCHANGED</a> -Benachrichtigungs Codes. <br/></td>
</tr>
<tr class="even">
<td><span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt><strong>TVGN_DROPHILITE</strong></dt> </dl></td>
<td>Zeichnet das angegebene Element im Stil neu, mit dem das Ziel eines Drag & Drop-Vorgangs angegeben wird.<br/></td>
</tr>
<tr class="odd">
<td><span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </dl></td>
<td>Stellt sicher, dass das angegebene Element sichtbar ist, und zeigt es, wenn möglich, oben im Fenster des Steuer Elements an. Strukturansicht-Steuerelemente zeigen so viele Elemente an, wie Sie in das Fenster passen. Wenn sich das angegebene Element am unteren Rand der Hierarchie der Elemente des Steuer Elements befindet, wird es möglicherweise nicht zum ersten sichtbaren Element, abhängig von der Anzahl der Elemente, die in das Fenster passen.<br/></td>
</tr>
<tr class="even">
<td><span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl> <dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </dl></td>
<td>Wenn ein einzelnes Element ausgewählt ist, wird von sichergestellt, dass die untergeordneten Elemente dieses Elements nicht von der TreeView-Ansicht erweitert werden. Dieser Wert ist nur gültig, wenn er mit dem TVGN_CARET-Flag verwendet wird. <br/>
<blockquote>
[!Note]<br />
Um dieses Flag zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen</a>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für ein Element. Wenn *LPARAM* den Wert **null** hat, wird für das Steuerelement festgelegt, dass kein Element ausgewählt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Wenn das angegebene Element das untergeordnete Element eines reduzierten übergeordneten Elements ist, wird die Liste der untergeordneten Elemente des übergeordneten Elements erweitert, um das angegebene Element anzuzeigen. In diesem Fall empfängt das übergeordnete Fenster des Steuer Elements die [TVN \_ itemexpandeing](tvn-itemexpanding.md) -und [TVN \_ itemexpanded](tvn-itemexpanded.md) -Benachrichtigungs Codes.

Die Verwendung des [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) -Makros entspricht dem Senden der **TVM \_ SelectItem** -Nachricht mit *wParam* -Wert, der auf den Tvgn-Caretzeichen Wert festgelegt ist \_ . Das Verwenden des [**TreeView \_ selectdroptarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) -Makros entspricht dem Senden der **TVM \_ SelectItem** -Nachricht mit *wParam* -Wert, der auf den Wert der Tvgn-drophitefunktion festgelegt ist \_ . Die Verwendung von [**TreeView \_ selectsetfirstvisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) entspricht dem Senden der **TVM \_ SelectItem** -Nachricht mit *wParam* , die auf den Wert der Tvgn firstvisible festgelegt ist \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





