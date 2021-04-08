---
title: PGN_CALCSIZE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Pager-Steuerelement gesendet, um die scrollbaren Dimensionen des enthaltenen Fensters abzurufen.
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- Windows-Steuerelemente für PGN_CALCSIZE Benachrichtigungs
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee6de1c45402f8bdc154f9f10be00140d7c766c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741217"
---
# <a name="pgn_calcsize-notification-code"></a>PGN \_ calcsize-Benachrichtigungs Code

Wird von einem Pager-Steuerelement gesendet, um die scrollbaren Dimensionen des enthaltenen Fensters abzurufen. Diese Dimensionen werden vom Pager-Steuerelement zum Bestimmen der scrollbaren Größe des enthaltenen Fensters verwendet. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmpgcalcsize**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) -Struktur, die Informationen über den Benachrichtigungs Code enthält und empfängt. Der **dwFlag** -Member dieser Struktur gibt an, welche Dimension berechnet wird. Abhängig vom Wert von **dwFlag** sollten Sie die gewünschte Dimension im **iWidth** -oder **iHeight** -Member dieser Struktur platzieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





