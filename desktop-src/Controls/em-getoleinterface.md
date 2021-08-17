---
title: EM_GETOLEINTERFACE Nachricht (Richedit.h)
description: Ruft ein IRichEditOle-Objekt ab, mit dem ein Client auf die COM-Funktionalität (Component Object Model) eines Rich Edit-Steuerelements zugreifen kann.
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- EM_GETOLEINTERFACE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETOLEINTERFACE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4e1799039081ed8250cb062aa3d1348a2fe8a8dbdcfa768fab74855d18d8e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831671"
---
# <a name="em_getoleinterface-message"></a>EM \_ GETOLEINTERFACE-Nachricht

Ruft ein [**IRichEditOle-Objekt**](/windows/desktop/api/Richole/nn-richole-iricheditole) ab, mit dem ein Client auf die COM-Funktionalität (Component Object Model) eines Rich Edit-Steuerelements zugreifen kann.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Zeiger, der das [**IRichEditOle-Objekt**](/windows/desktop/api/Richole/nn-richole-iricheditole) empfängt. Das Steuerelement ruft die [**AddRef-Methode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) für das -Objekt vor der Rückgabe auf, sodass die aufrufende Anwendung die [**Release-Methode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) aufrufen muss, wenn sie mit dem -Objekt fertig ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

