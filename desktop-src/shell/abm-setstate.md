---
description: Legt den Zustand "automatisch ausblenden" und "Always on-Top" der Windows-Taskleiste fest.
title: ABM_SETSTATE Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a60e156d-19ef-49b9-83fc-138d1a2169f2
api_name:
- ABM_SETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cd21ca49d1a57d870c26e010420f978f1d9b88a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977441"
---
# <a name="abm_setstate-message"></a>ABM- \_ SetState-Meldung

Legt den Zustand "automatisch ausblenden" und "Always on-Top" der Windows-Taskleiste fest.


```C++
SHAppBarMessage(ABM_SETSTATE, pabd); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur. Beim Senden dieser Nachricht müssen Sie die **CBSIZE** -und **HWND** -Elemente angeben. Die Daten für den gewünschten Zustand werden im **LPARAM** -Member mit einem der folgenden Werte gesendet.

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Automatisch ausblenden und immer am oberen Rand

</dd> <dt>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**ABS \_ AlwaysOnTop**


</dt> <dd>

Always on-Top on, Automatisches Ausblenden Off

</dd> <dt>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**ABS \_ automatisch ausblenden**


</dt> <dd>

Automatisch ausblenden bei, immer am Anfang

</dd> <dt>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS \_ Autohide \| ABS \_ AlwaysOnTop**


</dt> <dd>

Automatisch ausblenden und immer am oberen Rand

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **true** zurück.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




