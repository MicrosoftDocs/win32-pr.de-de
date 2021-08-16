---
description: Registriert die Shell-dynamische Daten Exchange -Dienste (DDE) im aktuellen Prozess und benachrichtigt das System, dass der aktuelle Prozess DDE-Objekte hosten möchte.
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: ShellDDEInit-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellDDEInit
api_type:
- DllExport
api_location:
- Shdocvw.dll
ms.openlocfilehash: 27d2e304cf3a67f522bbeec4835f5faa98b24d1509363873bb51387391f94b1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676712"
---
# <a name="shellddeinit-function"></a>ShellDDEInit-Funktion

Registriert die Shell-dynamische Daten Exchange -Dienste (DDE) im aktuellen Prozess und benachrichtigt das System, dass der aktuelle Prozess DDE-Objekte hosten möchte.

## <a name="syntax"></a>Syntax


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*init* \[ In\]
</dt> <dd>

Typ: **BOOL**

**TRUE,** um den aktuellen Prozess als DDE-Host zu registrieren; **FALSE,** um die Registrierung zu aufheben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Prozess, der diese Funktion aufruft, fungiert als Shell und wird verwendet, um den Inhalt von Ordnern anzuzeigen, die mit dem [**ShellExecute-Verb**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) "open" geöffnet wurden.

Diese Funktion verfügt nicht über einen zugeordneten Header oder eine Bibliotheksdatei, daher muss sie nach Ordinalwert aufgerufen werden. Rufen [**Sie LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen (Shdocvw.dll) auf, um ein Modulhand handle zu erhalten. Rufen Sie [**dann GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modulhandle und der Ordnungszahl 118 der Funktion auf, um die Adresse der Funktion zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Xp, Windows 2000 Professional \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shdocvw.dll (Version 6.0 oder höher)</dt> </dl> |



 

 
