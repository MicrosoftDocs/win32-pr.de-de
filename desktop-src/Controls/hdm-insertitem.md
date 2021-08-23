---
title: HDM_INSERTITEM Meldung (Commctrl.h)
description: Fügt ein neues Element in ein Headersteuerelement ein. Sie können diese Nachricht explizit senden oder das \_ Header InsertItem-Makro verwenden.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- HDM_INSERTITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e30a07637afae1a3efcf71b3b556c32bebf96775bb2a5cbdf6e92513d33ec5c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544740"
---
# <a name="hdm_insertitem-message"></a>HDM \_ INSERTITEM-Nachricht

Fügt ein neues Element in ein Headersteuerelement ein. Sie können diese Nachricht explizit senden oder das [**Header \_ InsertItem-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Elements, nach dem das neue Element eingefügt werden soll. Das neue Element wird am Ende des Headersteuerelements eingefügt, wenn *wParam* größer oder gleich der Anzahl der Elemente im Steuerelement ist. Wenn *wParam 0* (null) ist, wird das neue Element am Anfang des Headersteuerelements eingefügt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**HDITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-hditema) die Informationen zum neuen Element enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Index des neuen Elements zurück, andernfalls -1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **HDM \_ INSERTITEMW** (Unicode) und **HDM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





