---
description: Die Registrierung einer App-Leiste wird aufgehoben, indem sie aus der internen Liste des Systems entfernt wird. Das System sendet keine Benachrichtigungen mehr an die App-Leiste oder verhindert, dass andere Anwendungen den von der App-Leiste verwendeten Bildschirmbereich verwenden.
title: ABM_REMOVE (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3da73a52-3dbb-4133-a9bd-86540e1c4154
api_name:
- ABM_REMOVE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c32fd2c7a12fc8146a01d3722b31b46bad01f61b526397806a5121b7381b069e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861707"
---
# <a name="abm_remove-message"></a>ABM \_ REMOVE-Nachricht

Die Registrierung einer App-Leiste wird aufgehoben, indem sie aus der internen Liste des Systems entfernt wird. Das System sendet keine Benachrichtigungen mehr an die App-Leiste oder verhindert, dass andere Anwendungen den von der App-Leiste verwendeten Bildschirmbereich verwenden.


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**APPBARDATA-Struktur,**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) die das Handle für die App-Leiste enthält, deren Registrierung aufgehoben werden soll. Sie müssen beim Senden **dieser Nachricht die Member cbSize** und **hWnd** angeben. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **TRUE zurück.**

## <a name="remarks"></a>Hinweise

Diese Meldung bewirkt, dass das System die [**ABN \_ POSCHANGED-Benachrichtigungsnachricht**](abn-poschanged.md) an alle App-Leisten sendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




