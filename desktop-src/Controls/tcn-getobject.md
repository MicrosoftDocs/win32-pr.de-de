---
title: TCN_GETOBJECT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Registerkarten-Steuerelement gesendet, wenn es den erweiterten TCS \_ \_ -registerdrop-Stil hat und ein Objekt über ein Registerkarten Element im-Steuerelement gezogen wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- Windows-Steuerelemente für TCN_GETOBJECT Benachrichtigungs
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e442a122397db717b25e71b17487866227476ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340304"
---
# <a name="tcn_getobject-notification-code"></a>TCN \_ GetObject-Benachrichtigungs Code

Wird von einem Registerkarten-Steuerelement gesendet, wenn es den erweiterten [**TCS- \_ \_ registerdrop**](tab-control-extended-styles.md) -Stil hat und ein Objekt über ein Registerkarten Element im-Steuerelement gezogen wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmujectnotify**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) -Struktur, die Informationen über das Registerkarten Element enthält, über das das Objekt gezogen wird, und empfängt Daten empfängt, die von der Anwendung als Reaktion auf diese Nachricht zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung, die diesen Benachrichtigungs Code verarbeitet, muss NULL zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





