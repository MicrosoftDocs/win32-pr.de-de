---
title: TVN_ENDLABELEDIT Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements über das Ende der Bezeichnungs Bearbeitung für ein Element. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- Windows-Steuerelemente für TVN_ENDLABELEDIT Benachrichtigungs
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
ms.openlocfilehash: 7c30d494ad90b3d55f85b1ad154aed0f814a1eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103899"
---
# <a name="tvn_endlabeledit-notification-code"></a>TVN \_ endlabeledit-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements über das Ende der Bezeichnungs Bearbeitung für ein Element. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) -Struktur. Das **Element Element** dieser Struktur ist eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, deren **Hitem**-, **LPARAM**-und **pszText** -Member gültige Informationen über das Element enthalten, das bearbeitet wurde. Wenn die Bezeichnungs Bearbeitung abgebrochen wurde, ist der **pszText** -Member der **tvitem** -Struktur **null**. Andernfalls ist **pszText** die Adresse des bearbeiteten Texts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn das **pszText** -Element nicht **null** ist, wird **true** zurückgegeben, um die Bezeichnung des Elements auf den bearbeiteten Text festzulegen. Gibt **false** zurück, um den bearbeiteten Text abzulehnen und zur ursprünglichen Bezeichnung zurückzukehren.

## <a name="remarks"></a>Bemerkungen

Wenn der **pszText** -Member **null** ist, wird der Rückgabewert ignoriert.

Wenn Sie den LPSTR \_ -textcallback-Wert für dieses Element angegeben haben und das **pszText** -Element nicht **null** ist, \_ sollte der TVN endlabeledit-Handler den Text aus **pszText** in den lokalen Speicher kopieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ Endlabeleditw** (Unicode) und **TVN \_ endlabeledita** (ANSI)<br/>         |



 

 





