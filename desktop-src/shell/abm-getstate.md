---
description: Ruft die Zustände "automatisch ausblenden" und "Always on-Top" der Windows-Taskleiste ab.
title: ABM_GETSTATE Meldung (shellapi. h)
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
ms.openlocfilehash: 71225cd8d93de09a07cb0049066e52be08c18a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342869"
---
# <a name="abm_getstate-message"></a>ABM \_ GetState-Nachricht

Ruft die Zustände "automatisch ausblenden" und "Always on-Top" der Windows-Taskleiste ab.


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur. Beim Senden dieser Nachricht muss das **CBSIZE** -Element angegeben werden. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn sich die Taskleiste weder im automatisch ausblenden-noch bei Always on-Top-Zustand befindet. Andernfalls ist der Rückgabewert eine oder beide der folgenden:



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
<td>Die Taskleiste befindet sich im Status "Always on-Top". <br/>
<blockquote>
[!Note]<br />
Ab Windows 7 wird ABS_ALWAYSONTOP nicht mehr zurückgegeben, da sich die Taskleiste immer in diesem Zustand befindet. Der ältere Code sollte aktualisiert werden, damit das Fehlen dieses Werts ignoriert wird. angenommen, der Rückgabewert bedeutet, dass sich die Taskleiste nicht im Status "Always on-Top" befindet.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>ABS_AUTOHIDE</strong></dt> </dl></td>
<td>Die Taskleiste befindet sich im Zustand "automatisch ausblenden".<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




