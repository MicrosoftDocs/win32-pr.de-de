---
description: Registriert die shelldienste (shelldynamischer Datenaustausch) im aktuellen Prozess und benachrichtigt das System, dass der aktuelle Prozess DDE-Objekte hosten möchte.
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: Shellddeingeit-Funktion
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
ms.openlocfilehash: cb2f4639d97a99cd063f372e303fd48b7a1d6e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980441"
---
# <a name="shellddeinit-function"></a>Shellddeingeit-Funktion

Registriert die shelldienste (shelldynamischer Datenaustausch) im aktuellen Prozess und benachrichtigt das System, dass der aktuelle Prozess DDE-Objekte hosten möchte.

## <a name="syntax"></a>Syntax


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Init* \[ in\]
</dt> <dd>

Typ: **bool**

**True** , wenn der aktuelle Prozess als DDE-Host registriert werden soll. " **False** ", um die Registrierung aufzuheben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Prozess, der diese Funktion aufruft, fungiert als Shell und wird verwendet, um den Inhalt der Ordner anzuzeigen, die mit dem [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) -Verb geöffnet wurden.

Diese Funktion verfügt über keine zugeordnete Header-oder Bibliotheksdatei, sodass Sie von Ordinalwerten aufgerufen werden muss. Rufen Sie [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen (Shdocvw.dll) auf, um ein Modul Handle zu erhalten. Anschließend können Sie [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modul Handle und der Ordnungszahl 118 der Funktion aufrufen, um die Adresse der Funktion abzurufen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP, Windows 2000 Professional \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shdocvw.dll (Version 6,0 oder höher)</dt> </dl> |



 

 
