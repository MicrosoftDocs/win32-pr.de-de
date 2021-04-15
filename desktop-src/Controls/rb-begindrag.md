---
title: RB_BEGINDRAG Meldung (kommstrg. h)
description: Versetzt das Grund leisten-Steuerelement in den Drag & Drop-Modus. Diese Meldung bewirkt nicht, dass eine RBN- \_ BeginDrag-Benachrichtigung gesendet wird.
ms.assetid: 1e3e4928-cb84-4fd4-8056-84de1f791d1c
keywords:
- Windows-Steuerelemente für RB_BEGINDRAG Meldung
topic_type:
- apiref
api_name:
- RB_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41865baa2bf6c640595296be9c157201d0cc16d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477889"
---
# <a name="rb_begindrag-message"></a>RB \_ BeginDrag-Nachricht

Versetzt das Grund leisten-Steuerelement in den Drag & Drop-Modus. Diese Meldung bewirkt nicht, dass eine [RBN- \_ BeginDrag](rbn-begindrag.md) -Benachrichtigung gesendet wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des Bands, auf den sich der Drag & Drop-Vorgang auswirkt.

</dd> <dt>

*lParam* 
</dt> <dd>

**DWORD** -Wert, der die Start Maus Koordinaten enthält. Die horizontale Koordinate ist im LoWord enthalten, und die vertikale Koordinate ist im HIWORD enthalten. Wenn Sie (**DWORD**)-1 übergeben, verwendet das Grund leisten-Steuerelement die Position des Mauszeigers, wenn der Thread des Steuer Elements das letzte Mal den Thread [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) oder [**Peer-Message**](/windows/desktop/api/winuser/nf-winuser-peekmessagea)aufgerufen hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Mit den [**\_ EndDrag**](rb-enddrag.md) -Meldungen " **RB \_ BeginDrag**", "RB [**\_ DragMove**](rb-dragmove.md)" und "RB" können Sie eine [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle für ein Grund leisten-Steuerelement implementieren. Sie senden die **RB \_ BeginDrag** -Nachricht als Antwort [**auf IDropTarget::D ragenter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), senden **die \_ RB DragMove** -Nachricht als Antwort auf [**IDropTarget::D ragover**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover)und die **RB- \_ EndDrag** -Nachricht als Antwort auf [**IDropTarget::D ROP**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) und [**IDropTarget::D ragleave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

