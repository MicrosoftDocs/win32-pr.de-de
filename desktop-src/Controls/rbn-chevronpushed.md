---
title: RBN_CHEVRONPUSHED Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, wenn ein Chevron gepusht wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84
keywords:
- Windows-Steuerelemente für RBN_CHEVRONPUSHED Benachrichtigungs
topic_type:
- apiref
api_name:
- RBN_CHEVRONPUSHED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab28d992b6d4a617b7aa7ee144eb50aef3b0e834
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040588"
---
# <a name="rbn_chevronpushed-notification-code"></a>RBN \_ chevronpushbenachrichtigungen-Benachrichtigungs Code

Wird von einem Grund leisten-Steuerelement gesendet, wenn ein Chevron gepusht wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
RBN_CHEVRONPUSHED

    lpnm = (NMREBARCHEVRON) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf die [**nmrebarchevron**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) -Struktur des Bands.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Wenn eine Anwendung diesen Benachrichtigungs Code empfängt, ist Sie für die Anzeige eines Popup Menüs mit Elementen für jedes ausgeblendete Tool verantwortlich. Verwenden Sie das **RC** -Element der [**nmrebarchevron**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) -Struktur, um die richtige Position für das Popup Menü zu suchen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





