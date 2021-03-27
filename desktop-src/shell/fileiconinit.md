---
description: Initialisiert oder initialisiert die System Abbild Liste neu.
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: "\"Fleieninit\"-Funktion"
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
ms.openlocfilehash: 090f35cc576caf6f99a8d5822a0304f15383e8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345418"
---
# <a name="fileiconinit-function"></a>"Fleieninit"-Funktion

Initialisiert oder initialisiert die System Abbild Liste neu.

## <a name="syntax"></a>Syntax


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*frestorecache* \[ in\]
</dt> <dd>

Typ: **bool**

**True** , um den System Abbild Cache von der Festplatte wiederherzustellen. Andernfalls **false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **bool**

**True** , wenn der Cache erfolgreich aktualisiert wurde, **false** , wenn die Initialisierung fehlgeschlagen ist.

## <a name="remarks"></a>Bemerkungen

Wenn Sie System Abbild Listen in Ihrem eigenen Prozess verwenden, müssen Sie in den folgenden Zeitpunkten " **fleieninit** " anrufen:

-   Beim Start.
-   Als Antwort auf eine [**WM- \_ settingchange**](../winmsg/wm-settingchange.md) -Nachricht, wenn das [**SPI- \_ setnonclientmetrics**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Flag festgelegt ist.

" **Fleideinit** " ist nicht in einer Header Datei enthalten. Sie müssen es direkt aus Shell32.dll mit der Ordnungszahl 660 abrufen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
