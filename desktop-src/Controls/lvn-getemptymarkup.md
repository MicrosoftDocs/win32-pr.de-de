---
title: LVN_GETEMPTYMARKUP Benachrichtigungs Code (kommctrl. h)
description: Wird vom Listenansicht-Steuerelement an das übergeordnete Fenster gesendet, wenn das Steuerelement keine Elemente aufweist. Der LVN \_ getemptymarkup-Benachrichtigungs Code ist eine Anforderung für das übergeordnete Fenster, einen Markup Text bereitzustellen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- Windows-Steuerelemente für LVN_GETEMPTYMARKUP Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_GETEMPTYMARKUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea693475ca42f962be07936f980cd3f5d52479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859346"
---
# <a name="lvn_getemptymarkup-notification-code"></a>LVN \_ getemptymarkup-Benachrichtigungs Code

Wird vom Listenansicht-Steuerelement an das übergeordnete Fenster gesendet, wenn das Steuerelement keine Elemente aufweist. Der LVN \_ getemptymarkup-Benachrichtigungs Code ist eine Anforderung für das übergeordnete Fenster, einen Markup Text bereitzustellen. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_GETEMPTYMARKUP
        
    pnmMarkup = (NMLVEMPTYMARKUP*) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmlvemptymarkup**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) -Struktur. Legen Sie die Elemente dieser Struktur so fest, dass Sie Markup Text für das Listenansicht-Steuerelement bereitstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, um den Markup Text im Listenansicht-Steuerelement festzulegen, andernfalls " **false** ".

## <a name="remarks"></a>Bemerkungen

Der Benachrichtigungs Empfänger wandelt *LPARAM* ein, um die [**nmlvemptymarkup**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) -Struktur abzurufen. Der *wParam* -Parameter enthält die ID des Steuer Elements, das diese Nachricht sendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





