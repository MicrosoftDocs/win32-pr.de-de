---
title: PSN_GETOBJECT Benachrichtigungs Code (prsht. h)
description: Wird von einem Eigenschaften Blatt gesendet, um ein Ablage Zielobjekt anzufordern, wenn der Cursor über eine der Schaltflächen des Registerkarten-Steuer Elements weitergeleitet wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- Windows-Steuerelemente für PSN_GETOBJECT Benachrichtigungs
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
ms.openlocfilehash: d0a039cf97dee1d1f1168894bb167c06de10d38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040312"
---
# <a name="psn_getobject-notification-code"></a>PSN- \_ GetObject-Benachrichtigungs Code

Wird von einem Eigenschaften Blatt gesendet, um ein Ablage Zielobjekt anzufordern, wenn der Cursor über eine der Schaltflächen des Registerkarten-Steuer Elements weitergeleitet wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmujectnotify**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) -Struktur, die bei einem Eintrag Informationen über den Benachrichtigungs Code enthält. Wenn dieser Benachrichtigungs Code verarbeitet wird, müssen Sie Objektinformationen in diese Struktur einfügen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung, die diesen Benachrichtigungs Code verarbeitet, muss NULL zurückgeben.

## <a name="remarks"></a>Bemerkungen

Um ein Objekt bereitzustellen, muss eine Anwendung Werte in einigen Membern der [**nmujectnotify**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) -Struktur bei *LPARAM* festlegen. Das **pObject** -Element muss auf einen gültigen Objekt Zeiger festgelegt werden, und das **HRESULT** -Element muss auf ein Success-Flag festgelegt werden. Um die Component Object Model (com)-Standards einzuhalten, erhöhen Sie immer den Verweis Zähler des Objekts, wenn Sie einen Objekt Zeiger bereitstellen.

Wenn eine Anwendung kein Objekt bereitstellt, muss **pObject** auf **null** und **HRESULT** auf ein Fehlerflag festgelegt werden.

> [!Note]  
> Dieser Benachrichtigungs Code wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





