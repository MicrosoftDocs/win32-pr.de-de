---
title: RB_HITTEST (Commctrl.h)
description: Bestimmt, welcher Teil eines Leistenbands sich an einem bestimmten Punkt auf dem Bildschirm befindet, wenn an diesem Punkt ein Rebarband vorhanden ist.
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- RB_HITTEST von Windows Steuerelementen
topic_type:
- apiref
api_name:
- RB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d45f2ca2c5c6cf8de61c14404ac3bb541a8c61741896cf1b2803db29332d75e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078673"
---
# <a name="rb_hittest-message"></a>RB \_ HITTEST-Nachricht

Bestimmt, welcher Teil eines Leistenbands sich an einem bestimmten Punkt auf dem Bildschirm befindet, wenn an diesem Punkt ein Rebarband vorhanden ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**RBHITTESTINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) Vor dem Senden der Nachricht muss **der pt-Member** dieser -Struktur auf den Punkt initialisiert werden, der in Clientkoordinaten getestet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den nullbasierten Index des Bandes am angegebenen Punkt zurück, oder -1, wenn sich an dem Punkt kein Rebarband auft hatte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





