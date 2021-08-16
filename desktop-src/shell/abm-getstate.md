---
description: Ruft die Zustände autohide und always on-top der Windows Taskleiste ab.
title: ABM_GETSTATE Meldung (Shellapi.h)
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
ms.openlocfilehash: b1a3618be793f4728dc6184b50b7a4e0e57c3ffd2c4d2cd8acde17372aa031f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225229"
---
# <a name="abm_getstate-message"></a>ABM \_ GETSTATE-Nachricht

Ruft die Zustände autohide und always on-top der Windows Taskleiste ab.


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



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rückgabecode</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>ABS_ALWAYSONTOP</strong></dt> </dl></td>
<td>Die Taskleiste befindet sich im Always On-Top-Zustand. <br/>
<blockquote>
[!Note]<br />
Ab Windows 7 wird ABS_ALWAYSONTOP nicht mehr zurückgegeben, da sich die Taskleiste immer in diesem Zustand befindet. Älterer Code sollte aktualisiert werden, um das Fehlen dieses Werts in zu ignorieren und nicht davon auszugehen, dass der Rückgabewert bedeutet, dass sich die Taskleiste nicht im Always On-Top-Zustand befindet.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>ABS_AUTOHIDE</strong></dt> </dl></td>
<td>Die Taskleiste befindet sich im Autohide-Zustand.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




