---
title: BN_DOUBLECLICKED Benachrichtigungscode (Winuser.h)
description: 'BN_DOUBLECLICKED Benachrichtigungscode: Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt.'
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- BN_DOUBLECLICKED Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- BN_DOUBLECLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64a11a4dec91a7a2f1d200c4c86c6989d846604a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104188"
---
# <a name="bn_doubleclicked-notification-code"></a>BN \_ DOUBLECLICKED-Benachrichtigungscode

Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt. Dieser Benachrichtigungscode wird automatisch für [**die Schaltflächen BS \_ USERBUTTON,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)und [**BS \_ OWNERDRAW**](button-styles.md) gesendet. Andere Schaltflächentypen senden BN \_ DOUBLECLICKED nur, wenn sie den [**Stil BS \_ NOTIFY**](button-styles.md) haben.

Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
BN_DOUBLECLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LOWORD enthält**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) den Steuerelementbezeichner der Schaltfläche. Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für die Schaltfläche.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

BN \_ DOUBLECLICKED ist mit dem [BN \_ DBLCLK-Benachrichtigungscode](bn-dblclk.md) identisch.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (einschließlich Windows.h)</dt> </dl> |



 

