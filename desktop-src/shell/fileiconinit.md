---
description: Initialisiert oder initialisiert die Systemimageliste erneut.
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: FileIconInit-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIconInit
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 1771e1f0bde83f0fc7d070787b7a19f87007e26bd1ad42dcaa88e230e61a60af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111810"
---
# <a name="fileiconinit-function"></a>FileIconInit-Funktion

Initialisiert oder initialisiert die Systemimageliste erneut.

## <a name="syntax"></a>Syntax


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fRestoreCache* \[ In\]
</dt> <dd>

Typ: **BOOL**

**TRUE,** um den Systemimagecache vom Datenträger wiederherzustellen; **Andernfalls FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **BOOL**

**TRUE,** wenn der Cache erfolgreich aktualisiert wurde, **FALSE,** wenn die Initialisierung fehlgeschlagen ist.

## <a name="remarks"></a>Hinweise

Wenn Sie Systemimagelisten in Ihrem eigenen Prozess verwenden, müssen Sie **FileIconInit** zu den folgenden Zeiten aufrufen:

-   Beim Start.
-   Als Reaktion auf eine [**WM \_ SETTINGCHANGE-Meldung,**](../winmsg/wm-settingchange.md) wenn das [**SPI \_ SETNONCLIENTMETRICS-Flag**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) festgelegt ist.

**FileIconInit** ist nicht in einer Headerdatei enthalten. Sie müssen sie direkt über Shell32.dll aufrufen, indem Sie die Ordnungszahl 660 verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
