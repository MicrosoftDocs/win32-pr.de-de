---
title: TBN_GETOBJECT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem ToolBar-Steuerelement gesendet, das den tbstyle \_ registerdrop-Stil verwendet, um ein Ablage Zielobjekt anzufordern, wenn der Zeiger über eine seiner Schaltflächen weitergeleitet wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- Windows-Steuerelemente für TBN_GETOBJECT Benachrichtigungs
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
ms.openlocfilehash: 1ed144245e351ca4e872128e68fe658bde7c0066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102859"
---
# <a name="tbn_getobject-notification-code"></a>TBN- \_ GetObject-Benachrichtigungs Code

Wird von einem ToolBar-Steuerelement gesendet, das den [**tbstyle \_ registerdrop**](toolbar-control-and-button-styles.md) -Stil verwendet, um ein Ablage Zielobjekt anzufordern, wenn der Zeiger über eine seiner Schaltflächen weitergeleitet wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmujectnotify**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) -Struktur, die Informationen über die Schaltfläche enthält, über die der Zeiger übergeben wurde und die Daten empfängt, die die Anwendung als Reaktion auf diesen Benachrichtigungs Code bereitstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung, die diesen Benachrichtigungs Code verarbeitet, muss NULL zurückgeben.

## <a name="remarks"></a>Bemerkungen

Um ein Objekt bereitzustellen, muss eine Anwendung Werte in einigen Membern der [**nmujectnotify**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) -Struktur bei *LPARAM* festlegen. Das **pObject** -Element muss auf einen gültigen Objekt Zeiger festgelegt werden, und das **HRESULT** -Element muss auf ein Success-Flag festgelegt werden. Um die Component Object Model (com)-Standards einzuhalten, erhöhen Sie immer den Verweis Zähler des Objekts, wenn Sie einen Objekt Zeiger bereitstellen.

Wenn eine Anwendung kein Objekt bereitstellt, muss **pObject** auf **null** und **HRESULT** auf ein Fehlerflag festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





