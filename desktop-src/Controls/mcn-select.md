---
title: MCN_SELECT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Monatskalender-Steuerelement gesendet, wenn der Benutzer eine explizite Datumsauswahl innerhalb eines Monatskalender-Steuer Elements vornimmt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- Windows-Steuerelemente für MCN_SELECT Benachrichtigungs
topic_type:
- apiref
api_name:
- MCN_SELECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252133267b9c552542df17ed73caa8c34a69641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040239"
---
# <a name="mcn_select-notification-code"></a>MCN- \_ Benachrichtigungs Code auswählen

Wird von einem Monatskalender-Steuerelement gesendet, wenn der Benutzer eine explizite Datumsauswahl innerhalb eines Monatskalender-Steuer Elements vornimmt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
MCN_SELECT

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmselchange**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) -Struktur, die Informationen über den aktuell ausgewählten Datumsbereich enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Der **MCN- \_ Select** -Benachrichtigungs Code ähnelt [**MCN \_ selChange**](mcn-selchange.md), aber **MCN \_ Select** wird nur als Antwort auf die explizite Datumsauswahl eines Benutzers gesendet. **MCN \_ SelChange** gilt für beliebige Auswahl Änderungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





