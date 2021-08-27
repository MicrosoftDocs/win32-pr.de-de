---
description: Ruft die Autohide- und Always On-Top-Zustände der Windows Taskleiste ab.
title: ABM_GETSTATE-Nachricht (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 18e16752-16be-492b-a4fa-c951e18dc86c
api_name:
- ABM_GETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1ced01e3f8186a82e99f408f91546ebcbb117ed9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466387"
---
# <a name="abm_getstate-message"></a>ABM \_ GETSTATE-Nachricht

Ruft die Autohide- und Always On-Top-Zustände der Windows Taskleiste ab.


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Zeiger auf eine [**APPBARDATA-Struktur.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) Sie müssen den **cbSize-Member** angeben, wenn Sie diese Nachricht senden. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn sich die Taskleiste weder im autohide- noch always-on-top-Zustand befindet. Andernfalls ist der Rückgabewert einer oder beide der folgenden Werte:




| Rückgabecode | Beschreibung | 
|-------------|-------------|
| <dl><dt><strong>ABS_ALWAYSONTOP</strong></dt></dl> | Die Taskleiste befindet sich im Always On-Top-Zustand. <br /><blockquote>[!Note]<br />Ab Windows 7 wird ABS_ALWAYSONTOP nicht mehr zurückgegeben, da sich die Taskleiste immer in diesem Zustand befindet. Älterer Code sollte aktualisiert werden, um das Fehlen dieses Werts in zu ignorieren und nicht davon auszugehen, dass der Rückgabewert bedeutet, dass sich die Taskleiste nicht im Always On-Top-Zustand befindet.</blockquote><br /> | 
| <dl><dt><strong>ABS_AUTOHIDE</strong></dt></dl> | Die Taskleiste befindet sich im Autohide-Zustand.<br /> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




