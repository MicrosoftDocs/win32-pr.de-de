---
title: TBN_DROPDOWN Benachrichtigungscode (Commctrl.h)
description: Wird von einem Symbolleistensteuerelement gesendet, wenn der Benutzer auf eine Dropdownschaltfläche klickt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- TBN_DROPDOWN Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- TBN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e2cdee38176b2ed72d42aaa29ca685a5e73dd30ceb7e315b5cbe0971161dc13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077924"
---
# <a name="tbn_dropdown-notification-code"></a>\_TBN-DROPDOWN-Benachrichtigungscode

Wird von einem Symbolleistensteuerelement gesendet, wenn der Benutzer auf eine Dropdownschaltfläche klickt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTOOLBAR-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) die Informationen zu diesem Benachrichtigungscode enthält. Für diesen Benachrichtigungscode sind nur die **HDR-** und **iItem-Member** dieser Struktur gültig.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück:



| Rückgabecode                                                                                          | Beschreibung                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**TBDDRET \_ DEFAULT**</dt> </dl>      | Das Dropdown wurde verarbeitet.<br/>                                             |
| <dl> <dt>**TBDDRET \_ NODEFAULT**</dt> </dl>    | Das Dropdown wurde nicht behandelt.<br/>                                         |
| <dl> <dt>**TBDDRET \_ TREATPRESSED**</dt> </dl> | Die Dropdown-Schaltfläche wurde behandelt, behandelt die Schaltfläche jedoch wie eine reguläre Schaltfläche.<br/> |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dropdownschaltflächen können einfach sein [**(BTNS-DROPDOWN-Stil), \_**](toolbar-control-and-button-styles.md) einen Pfeil neben dem [**Schaltflächenbild anzeigen (BTNS \_ WHOLEDROPDOWN-Stil)**](toolbar-control-and-button-styles.md) oder einen Pfeil anzeigen, der vom Bild getrennt ist [**(TBSTYLE \_ EX \_ DRAWDDARROWS-Stil).**](toolbar-extended-styles.md) Wenn ein separater Pfeil verwendet wird, wird TBN \_ DROPDOWN nur gesendet, wenn der Benutzer auf den Pfeilteil der Schaltfläche klickt. Wenn der Benutzer auf den Hauptteil der Schaltfläche klickt, wird wie bei einer Standardschaltfläche eine [**WM \_ COMMAND-Meldung**](/windows/desktop/menurc/wm-command) mit der ID der Schaltfläche gesendet. Für die anderen beiden Stile der Dropdown-Schaltfläche wird TBN \_ DROPDOWN gesendet, wenn der Benutzer auf einen Beliebigen Teil der Schaltfläche klickt.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

