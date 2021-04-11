---
title: RBN_GETOBJECT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, das mit dem Register Drop-Stil von RB erstellt \_ wird, wenn ein Objekt über ein Band im-Steuerelement gezogen wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- Windows-Steuerelemente für RBN_GETOBJECT Benachrichtigungs
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
ms.openlocfilehash: 9a390bc5c5f74a577805ca8ae1128fbb24e6b10b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104775"
---
# <a name="rbn_getobject-notification-code"></a>RBN- \_ GetObject-Benachrichtigungs Code

Wird von einem Grund leisten-Steuerelement gesendet, das mit dem [**\_ Register Drop**](rebar-control-styles.md) -Stil von RB erstellt wird, wenn ein Objekt über ein Band im-Steuerelement gezogen wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmujectnotify**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) -Struktur, die Informationen über das Band enthält, über das das Objekt gezogen wird. Außerdem werden die Daten, die von der empfangenden Anwendung als Reaktion auf diesen Benachrichtigungs Code bereitgestellt werden, empfangen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diesen Benachrichtigungs Code muss NULL sein.

## <a name="remarks"></a>Bemerkungen

Um den RBN- \_ GetObject-Benachrichtigungs Code zu erhalten, initialisieren Sie OLE mit einem Aufrufen von [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) oder [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

