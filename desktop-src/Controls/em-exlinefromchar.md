---
title: EM_EXLINEFROMCHAR Nachricht (Richedit.h)
description: Bestimmt, welche Zeile das angegebene Zeichen in einem Rich-Edit-Steuerelement enthält.
ms.assetid: 497482fb-9640-4063-a9f5-e0691b65225d
keywords:
- EM_EXLINEFROMCHAR Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_EXLINEFROMCHAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c41f5fbe540a4d765a48292d4ffd5b4af5849681dd1a82f4512b79348a6249d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915640"
---
# <a name="em_exlinefromchar-message"></a>EM \_ EXLINEFROMCHAR-Nachricht

Bestimmt, welche Zeile das angegebene Zeichen in einem Rich-Edit-Steuerelement enthält.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nullbasierter Index des Zeichens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt den nullbasierten Index der Zeile zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





