---
title: CBEN_DRAGBEGIN Benachrichtigungs Code (kommctrl. h)
description: Wird gesendet, wenn der Benutzer mit dem Ziehen des Bilds des Elements beginnt, das im Bearbeitungsbereich des Steuer Elements angezeigt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- Windows-Steuerelemente für CBEN_DRAGBEGIN Benachrichtigungs
topic_type:
- apiref
api_name:
- CBEN_DRAGBEGIN
- CBEN_DRAGBEGINA
- CBEN_DRAGBEGINW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910e6ac494b49f685a55e77b432e96b4fb22bd29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105758"
---
# <a name="cben_dragbegin-notification-code"></a>Cben \_ dragbegin-Benachrichtigungs Code

Wird gesendet, wenn der Benutzer mit dem Ziehen des Bilds des Elements beginnt, das im Bearbeitungsbereich des Steuer Elements angezeigt wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmcbedragbegin**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) -Struktur, die Informationen über den Benachrichtigungs Code enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Wenn die empfangende Anwendung die Drag & Drop-Funktionalität aus dem Steuerelement implementiert, startet die Anwendung den Drag & Drop-Vorgang als Reaktion auf diesen Benachrichtigungs Code.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Cben \_ Dragbeginw** (Unicode) und **cben \_ dragbegina** (ANSI)<br/>             |



 

 





