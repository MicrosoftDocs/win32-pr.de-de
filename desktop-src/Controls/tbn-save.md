---
title: TBN_SAVE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass gerade eine Symbolleiste gespeichert wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- Windows-Steuerelemente für TBN_SAVE Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cd28cb9d5fa1804caa3fe0ca89823305725ddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743801"
---
# <a name="tbn_save-notification-code"></a>TBN- \_ Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass gerade eine Symbolleiste gespeichert wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtbsave**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die Anwendung empfängt diesen Benachrichtigungs Code einmal zu Beginn des Speicher Vorgangs und einmal für jede Schaltfläche. Dieser Benachrichtigungs Code bietet Ihnen die Möglichkeit, eigene Informationen hinzuzufügen, die von der Shell gespeichert wurden. Wenn Sie keine Informationen hinzufügen möchten, ignorieren Sie den Benachrichtigungs Code. Eine ausführlichere Erläuterung der Handhabung von TBN finden Sie unter Anpassen der [Symbolleiste](toolbar-controls-overview.md) \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TBN- \_ Wiederherstellung](tbn-restore.md)
</dt> </dl>

 

 





