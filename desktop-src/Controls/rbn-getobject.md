---
title: RBN_GETOBJECT Benachrichtigungscode (Commctrl.h)
description: Wird von einem Rebar-Steuerelement gesendet, das mit dem RBS REGISTERDROP-Stil erstellt wurde, wenn ein Objekt über ein \_ Band im Steuerelement gezogen wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- RBN_GETOBJECT Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- RBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9709313a16d068e44b847f5e0862adf1e133b9f0ea92136a12e9aae24ffb14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985040"
---
# <a name="rbn_getobject-notification-code"></a>RBN \_ GETOBJECT-Benachrichtigungscode

Wird von einem Rebar-Steuerelement gesendet, das mit [**dem RBS \_ REGISTERDROP-Stil**](rebar-control-styles.md) erstellt wurde, wenn ein Objekt über ein Band im Steuerelement gezogen wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMOBJECTNOTIFY-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) die Informationen über das Band enthält, über das das Objekt gezogen wird, und empfängt auch die Daten, die von der empfangenden Anwendung als Antwort auf diesen Benachrichtigungscode bereitgestellt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diesen Benachrichtigungscode muss 0 (null) sein.

## <a name="remarks"></a>Hinweise

Initialisieren Sie OLE mit einem Aufruf von \_ [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) oder [**CoInitialize,**](/windows/desktop/api/objbase/nf-objbase-coinitialize)um den RBN GETOBJECT-Benachrichtigungscode zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

