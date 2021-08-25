---
title: TBN_GETOBJECT Benachrichtigungscode (Commctrl.h)
description: Wird von einem Symbolleistensteuerelement gesendet, das den TBSTYLE \_ REGISTERDROP-Stil verwendet, um ein Ablagezielobjekt anzufordern, wenn der Zeiger eine seiner Schaltflächen übergibt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- TBN_GETOBJECT Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- TBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c50f3d403089ca7db42ab89232e57d68121424c066914c534ba13a826adb8ea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876730"
---
# <a name="tbn_getobject-notification-code"></a>TBN \_ GETOBJECT-Benachrichtigungscode

Wird von einem Symbolleistensteuerelement gesendet, das den [**TBSTYLE \_ REGISTERDROP-Stil**](toolbar-control-and-button-styles.md) verwendet, um ein Ablagezielobjekt anzufordern, wenn der Zeiger eine seiner Schaltflächen übergibt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMOBJECTNOTIFY-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) die Informationen über die Schaltfläche enthält, die der Zeiger übergibt und Daten empfängt, die die Anwendung als Reaktion auf diesen Benachrichtigungscode bereitstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung, die diesen Benachrichtigungscode verarbeitet, muss null zurückgeben.

## <a name="remarks"></a>Hinweise

Um ein Objekt bereitzustellen, muss eine Anwendung Werte in einigen Membern der [**NMOBJECTNOTIFY-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) in *lParam* festlegen. Der **pObject-Member** muss auf einen gültigen Objektzeiger und der **hResult-Member** auf ein Erfolgsflag festgelegt werden. Um den COM-Standards (Component Object Model) zu entsprechen, erhöhen Sie immer den Verweiszähler des Objekts, wenn Sie einen Objektzeiger bereitstellen.

Wenn eine Anwendung kein Objekt bereitstellt, muss **pObject** auf **NULL** und **hResult** auf ein Fehlerflag festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





