---
title: EM_GETSELTEXT Nachricht (Richedit.h)
description: Ruft den aktuell ausgewählten Text in einem Rich Edit-Steuerelement ab.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- EM_GETSELTEXT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETSELTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 540567f1b52c936ad085acac8e0374fdb0a912bae06480632263f9676f2948e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019498"
---
# <a name="em_getseltext-message"></a>EM \_ GETSELTEXT-Nachricht

Ruft den aktuell ausgewählten Text in einem Rich Edit-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Puffer, der den ausgewählten Text empfängt. Die aufrufende Anwendung muss sicherstellen, dass der Puffer groß genug ist, um den ausgewählten Text zu speichern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die Anzahl der kopierten Zeichen zurück, ohne das abschließende NULL-Zeichen zu enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





