---
title: BN_DOUBLECLICKED Benachrichtigungscode (Winuser.h)
description: 'BN_DOUBLECLICKED Benachrichtigungscode: Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt.'
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- BN_DOUBLECLICKED Benachrichtigungscode Windows Controls
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
ms.openlocfilehash: 8ce43cebee93516f929f9a763c14dd51d9d486470eeb93818b9605c3f23a1914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674124"
---
# <a name="bn_doubleclicked-notification-code"></a>BN \_ DOUBLECLICKED-Benachrichtigungscode

Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt. Dieser Benachrichtigungscode wird automatisch für die Schaltflächen [**BS \_ USERBUTTON,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)und [**BS \_ OWNERDRAW**](button-styles.md) gesendet. Andere Schaltflächentypen senden BN \_ DOUBLECLICKED nur, wenn sie den [**BS \_ NOTIFY-Stil**](button-styles.md) aufweisen.

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

[**LowORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelementbezeichner der Schaltfläche. [**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für die Schaltfläche.

</dd> </dl>

## <a name="remarks"></a>Hinweise

BN \_ DOUBLECLICKED entspricht dem [BN DBLCLK-Benachrichtigungscode. \_ ](bn-dblclk.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



 

