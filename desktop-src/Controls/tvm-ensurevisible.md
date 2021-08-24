---
title: TVM_ENSUREVISIBLE (Commctrl.h)
description: Stellt sicher, dass ein Strukturansichtselement sichtbar ist, das übergeordnete Element erweitert oder das Strukturansichtssteuerelement bei Bedarf scrollt. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ EnsureVisible-Makros senden.
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- TVM_ENSUREVISIBLE meldungssteuerelemente Windows
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
ms.openlocfilehash: c1072c7213eb2172896980662bcd7a22a3c41fccf34eea2f7a107ab7ff894b32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797250"
---
# <a name="tvm_ensurevisible-message"></a>TVM \_ ENSUREVISIBLE-Meldung

Stellt sicher, dass ein Strukturansichtselement sichtbar ist, das übergeordnete Element erweitert oder das Strukturansichtssteuerelement bei Bedarf scrollt. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ EnsureVisible-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn das System einen Bildlauf für die Elemente im Strukturansicht-Steuerelement durchführen und keine Elemente erweitert wurden. Andernfalls gibt die Meldung 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Wenn die NACHRICHT TVM ENSUREVISIBLE das übergeordnete Element erweitert, empfängt das übergeordnete Fenster die \_ Benachrichtigungscodes [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) und [TVN \_ ITEMEXPANDED.](tvn-itemexpanded.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





