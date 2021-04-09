---
title: TVM_ENSUREVISIBLE Meldung (kommstrg. h)
description: Stellt sicher, dass ein Struktur Ansichts Element sichtbar ist, erweitert das übergeordnete Element und führt ggf. einen Bildlauf im Strukturansicht-Steuerelement aus. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ EnsureVisible-Makros senden.
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- Windows-Steuerelemente für TVM_ENSUREVISIBLE Meldung
topic_type:
- apiref
api_name:
- TVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06100ee33106736076608aa216d2aebc03b76ebe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949691"
---
# <a name="tvm_ensurevisible-message"></a>TVM \_ EnsureVisible-Meldung

Stellt sicher, dass ein Struktur Ansichts Element sichtbar ist, erweitert das übergeordnete Element und führt ggf. einen Bildlauf im Strukturansicht-Steuerelement aus. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn das System die Elemente im Strukturansicht-Steuerelement aufscrollt und keine Elemente erweitert wurden. Andernfalls gibt die Meldung 0 (null) zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die TVM- \_ Meldung "ensureVisible" das übergeordnete Element erweitert, empfängt das übergeordnete Fenster die [TVN \_ itemexpandeing](tvn-itemexpanding.md) -und [TVN \_ itemexpanded](tvn-itemexpanded.md) -Benachrichtigungs Codes.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





