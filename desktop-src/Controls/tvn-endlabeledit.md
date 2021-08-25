---
title: TVN_ENDLABELEDIT Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements über das Ende der Bearbeitung der Bezeichnung für ein Element. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- TVN_ENDLABELEDIT Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TVN_ENDLABELEDIT
- TVN_ENDLABELEDITA
- TVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38be7b9fde4b96f3510cd59683ee9df471cc4d77342fe375d9b1818b8ae7da46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408200"
---
# <a name="tvn_endlabeledit-notification-code"></a>TVN \_ ENDLABELEDIT-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements über das Ende der Bearbeitung der Bezeichnung für ein Element. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTVDISPINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) Der **Elementmember** dieser Struktur ist eine [**TVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tvitema) deren **hItem-,** **lParam-** und **pszText-Member** gültige Informationen über das bearbeitete Element enthalten. Wenn die Bearbeitung der Bezeichnung abgebrochen wurde, ist der **pszText-Member** der **TVITEM-Struktur** **NULL.** Andernfalls ist **pszText** die Adresse des bearbeiteten Texts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der **pszText-Member** ungleich **NULL** ist, wird **TRUE** zurückgegeben, um die Bezeichnung des Elements auf den bearbeiteten Text festzulegen. Gibt **FALSE** zurück, um den bearbeiteten Text abzulehnen und zur ursprünglichen Bezeichnung zurückzukehren.

## <a name="remarks"></a>Hinweise

Wenn der **pszText-Member** **NULL** ist, wird der Rückgabewert ignoriert.

Wenn Sie den LPSTR \_ TEXTCALLBACK-Wert für dieses Element angegeben haben und der **pszText-Member** ungleich **NULL** ist, sollte ihr TVN \_ ENDLABELEDIT-Handler den Text aus **pszText** in Ihren lokalen Speicher kopieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ ENDLABELEDITW** (Unicode) und **TVN \_ ENDLABELEDITA** (ANSI)<br/>         |



 

 





