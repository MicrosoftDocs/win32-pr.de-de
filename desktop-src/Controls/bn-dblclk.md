---
title: BN_DBLCLK Benachrichtigungscode (Winuser.h)
description: 'BN_DBLCLK Benachrichtigungscode: Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt.'
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- windows-Steuerelemente für BN_DBLCLK Benachrichtigungscode
topic_type:
- apiref
api_name:
- BN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb403f37b8fee9ea36023a7cd2511bbaaa2af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096848"
---
# <a name="bn_dblclk-notification-code"></a>BN \_ DBLCLK-Benachrichtigungscode

Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt. Dieser Benachrichtigungscode wird automatisch für die Schaltflächen [**BS \_ USERBUTTON,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)und [**BS \_ OWNERDRAW**](button-styles.md) gesendet. Andere Schaltflächentypen senden BN \_ DBLCLK nur, wenn sie den [**BS \_ NOTIFY-Stil**](button-styles.md) aufweisen.

Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelementbezeichner der Schaltfläche. [**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für die Schaltfläche.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

BN \_ DBLCLK ist identisch mit dem [BN DOUBLECLICKED-Benachrichtigungscode. \_ ](bn-doubleclicked.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (windows.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Verweis**
</dt> <dt>

[BN \_ GEKLICKT](bn-clicked.md)
</dt> <dt>

[BN \_ DOUBLECLICKED](bn-doubleclicked.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

