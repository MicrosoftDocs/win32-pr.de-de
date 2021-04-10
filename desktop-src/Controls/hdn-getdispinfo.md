---
title: HDN_GETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Wird an den Besitzer eines Header Steuer Elements gesendet, wenn das Steuerelement Informationen zu einem Rückruf Header Element benötigt. Dieser Benachrichtigungs Code wird als WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- Windows-Steuerelemente für HDN_GETDISPINFO Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45fe753b610fae69956b89caadade394566d0dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040181"
---
# <a name="hdn_getdispinfo-notification-code"></a>Hdn \_ getdispinfo-Benachrichtigungs Code

Wird an den Besitzer eines Header Steuer Elements gesendet, wenn das Steuerelement Informationen zu einem Rückruf Header Element benötigt. Dieser Benachrichtigungs Code wird als [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmhddispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) -Struktur. Bei der Eingabe geben die Felder der Struktur an, welche Informationen erforderlich sind und welches Element von Interesse ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein LRESULT zurück.

## <a name="remarks"></a>Bemerkungen

Füllen Sie die entsprechenden Member der-Struktur aus, um die angeforderten Informationen an das Header Steuerelement zurückzugeben. Wenn Ihr Nachrichten Handler das **Masken** Element der [**nmhddispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) -Struktur auf HDI \_ di \_ SetItem festlegt, speichert das Header Steuerelement die Informationen und fordert Sie nicht erneut an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Hdn \_ Getdispinfow** (Unicode) und **Hdn \_ getdispinfoa** (ANSI)<br/>           |



 

 





