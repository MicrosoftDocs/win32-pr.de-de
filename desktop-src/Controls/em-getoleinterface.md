---
title: EM_GETOLEINTERFACE Meldung (RichEdit. h)
description: Ruft ein iricheditole-Objekt ab, mit dem ein Client auf die Component Object Model (com)-Funktionalität eines Rich-Edit-Steuer Elements zugreifen kann.
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- Windows-Steuerelemente für EM_GETOLEINTERFACE Meldung
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
ms.openlocfilehash: 7d7557d40c6dcec38ce629d949a8db9915714821
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104817"
---
# <a name="em_getoleinterface-message"></a>EM \_ getoleinterface-Nachricht

Ruft ein [**iricheditole**](/windows/desktop/api/Richole/nn-richole-iricheditole) -Objekt ab, mit dem ein Client auf die Component Object Model (com)-Funktionalität eines Rich-Edit-Steuer Elements zugreifen kann.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Zeiger, der das [**iricheditole**](/windows/desktop/api/Richole/nn-richole-iricheditole) -Objekt empfängt. Das-Steuerelement ruft vor der Rückgabe die [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) -Methode für das-Objekt auf, sodass die aufrufende Anwendung die [**releasemethode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) aufrufen muss, wenn Sie mit dem-Objekt ausgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iricheditole**](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

