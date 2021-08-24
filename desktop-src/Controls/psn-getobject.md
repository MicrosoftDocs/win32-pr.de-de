---
title: PSN_GETOBJECT Benachrichtigungscode (Prsht.h)
description: Wird von einem Eigenschaftenblatt gesendet, um ein Absturzzielobjekt an fordern, wenn der Cursor über eine der Schaltflächen des Registerkarten-Steuerelements übergeht. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- PSN_GETOBJECT Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- PSN_GETOBJECT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e81803a950c7b8eb9a41d31178c8f57d7e4199f802538616d4ced20c5a5cb4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798630"
---
# <a name="psn_getobject-notification-code"></a>PSN \_ GETOBJECT-Benachrichtigungscode

Wird von einem Eigenschaftenblatt gesendet, um ein Absturzzielobjekt an fordern, wenn der Cursor über eine der Schaltflächen des Registerkarten-Steuerelements übergeht. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMOBJECTNOTIFY-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) die beim Eintrag Informationen zum Benachrichtigungscode enthält. Wenn dieser Benachrichtigungscode verarbeitet wird, müssen Sie Objektinformationen in diese Struktur einfügen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung, die diesen Benachrichtigungscode verarbeitet, muss 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Um ein Objekt bereitstellen zu können, muss eine Anwendung Werte in einigen Membern der [**NMOBJECTNOTIFY-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) in *lParam festlegen.* Das **pObject-Member** muss auf einen gültigen Objektzeiger und das **hResult-Member** auf ein Erfolgsflag festgelegt werden. Zur Einhaltung Component Object Model (COM)-Standards erhöhen Sie immer die Verweisanzahl des Objekts, wenn Sie einen Objektzeiger bereitstellen.

Wenn eine Anwendung kein Objekt angibt, muss **sie pObject** auf **NULL** und **hResult** auf ein Fehlerflag festlegen.

> [!Note]  
> Dieser Benachrichtigungscode wird nicht unterstützt, wenn der Stil des Assistenten von Assistenten verwendet wird ([**\_ PSHWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





