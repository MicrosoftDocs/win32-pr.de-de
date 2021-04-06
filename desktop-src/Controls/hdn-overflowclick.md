---
title: HDN_OVERFLOWCLICK Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Header Steuerelement an das übergeordnete Element gesendet, wenn auf die Überlauf Schaltfläche des Headers geklickt wird Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- Windows-Steuerelemente für HDN_OVERFLOWCLICK Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911953fcbea785cb7024bc9d0670c8ed33239524
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858943"
---
# <a name="hdn_overflowclick-notification-code"></a>\_Benachrichtigungs Code für den über Fluss von Hdn

Wird von einem Header Steuerelement an das übergeordnete Element gesendet, wenn auf die Überlauf Schaltfläche des Headers geklickt wird Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die den Benachrichtigungs Code beschreibt. Der Aufrufprozess ist dafür verantwortlich, diese Struktur zuzuordnen, einschließlich der enthaltenen [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur. Legen Sie die Member der **NMHDR** -Struktur fest, einschließlich des *Code* Members, der auf den Hdn-overflowclick festgelegt werden muss \_ .

Legen Sie den **iItem** -Member der [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur auf den Index des ersten Header Elements fest, das nicht sichtbar ist und daher bei einem Überlauf angezeigt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Der Benachrichtigungs Empfänger wandelt **LPARAM** ein, um die [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur abzurufen. **WParam** enthält die ID des Steuer Elements, das die Benachrichtigung sendet.

Diese Meldung wird nur gesendet, wenn für das Header Steuerelement Style [**HDS \_ Overflow**](header-control-styles.md) festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





