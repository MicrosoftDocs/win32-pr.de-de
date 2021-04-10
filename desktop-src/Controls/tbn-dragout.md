---
title: TBN_DRAGOUT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer auf eine Schaltfläche klickt, und verschiebt den Cursor dann von der Schaltfläche. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- Windows-Steuerelemente für TBN_DRAGOUT Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_DRAGOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54fa61ef183b56b882c6ecdcb9d0d59edbf13e80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040355"
---
# <a name="tbn_dragout-notification-code"></a>TBN- \_ dragout-Benachrichtigungs Code

Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer auf eine Schaltfläche klickt, und verschiebt den Cursor dann von der Schaltfläche. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält. Bei diesem Benachrichtigungs Code sind nur die **HDR** -und **iItem** -Member dieser Struktur gültig. Der **iItem** -Member dieser Struktur enthält den Befehls Bezeichner der gezogenen Schaltfläche.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Mit diesem Benachrichtigungs Code kann eine Anwendung Drag & amp; Drop-Funktionen für Symbolleisten Schaltflächen implementieren. Bei der Verarbeitung dieses Benachrichtigungs Codes startet die Anwendung den Drag & Drop-Vorgang.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





