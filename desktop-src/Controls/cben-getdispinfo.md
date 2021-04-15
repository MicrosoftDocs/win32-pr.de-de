---
title: CBEN_GETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Wird gesendet, um Anzeigeinformationen zu einem Rückruf Element abzurufen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: a181be28-0001-4953-8e59-77aff2dc40be
keywords:
- Windows-Steuerelemente für CBEN_GETDISPINFO Benachrichtigungs
topic_type:
- apiref
api_name:
- CBEN_GETDISPINFO
- CBEN_GETDISPINFOA
- CBEN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3121d15b1482bdedf19a814a42e3309265909f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517384"
---
# <a name="cben_getdispinfo-notification-code"></a>Cben \_ getdispinfo-Benachrichtigungs Code

Wird gesendet, um Anzeigeinformationen zu einem Rückruf Element abzurufen. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
CBEN_GETDISPINFO

    pDispInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmcomboboxex**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) -Struktur, die Informationen über den Benachrichtigungs Code enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung, die diesen Benachrichtigungs Code verarbeitet, muss NULL zurückgeben.

## <a name="remarks"></a>Bemerkungen

Die [**nmcomboboxex**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) -Struktur enthält eine [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur. Der **Mask** -Member gibt die Informationen an, die vom Steuerelement angefordert werden.

Füllen Sie die entsprechenden Member der Struktur aus, um die angeforderten Informationen an das Steuerelement zurückzugeben. Wenn Ihr Nachrichten Handler das **Masken** Element der [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur auf cbeif \_ di \_ SetItem festlegt, speichert das Steuerelement die Informationen und fordert Sie nicht erneut an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Cben \_ Getdispinfow** (Unicode) und **cben \_ getdispinfoa** (ANSI)<br/>         |



 

 





