---
description: Die CreateProtocol-Funktion benachrichtigt Netzwerkmonitor, dass ein bestimmter Protokollparser vorhanden ist.
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: CreateProtocol-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 173f744406ef2b360c0af7158e397c2001f146b9f2339bf6aaf3468b9a1465dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796351"
---
# <a name="createprotocol-function"></a>CreateProtocol-Funktion

Die **CreateProtocol-Funktion** benachrichtigt Netzwerkmonitor, dass ein bestimmter Protokollparser vorhanden ist.

## <a name="syntax"></a>Syntax


```C++
HPROTOCOL WINAPI CreateProtocol(
  _In_ LPSTR         ProtocolName,
  _In_ LPENTRYPOINTS lpEntryPoints,
  _In_ DWORD         cbEntryPoints
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProtocolName* \[ In\]
</dt> <dd>

Der Name des Protokolls, das der Parser erkennt.

</dd> <dt>

*lpEntryPoints* \[ In\]
</dt> <dd>

Eine [ENTRYPOINTS-Struktur,](entrypoints.md) die die verbleibenden Parser-DLL-Einstiegspunkte enthält. Eine Liste der Exportfunktionen, auf die jeder Einstiegspunkt verweist, finden Sie unter Hinweise. Einstiegspunkte müssen in der Von der **ENTRYPOINTS-Struktur angegebenen** Reihenfolge bereitgestellt werden.

</dd> <dt>

*cbEntryPoints* \[ In\]
</dt> <dd>

Die Größe der **ENTRYPOINTS-Struktur.** Netzwerkmonitor stellt ein ENTRYPOINTS SIZE-Makro zur Angabe der Größe \_ der Struktur zur Anwendung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für das Protokoll.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **NULL.**

## <a name="remarks"></a>Hinweise

Die Parser-DLL ruft **CreateProtocol während** der Implementierung von [DllMain auf.](dllmain-parser.md) Die **CreateProtocol-Funktion** wird aufgerufen, wenn das Betriebssystem die Parser-DLL zum ersten Mal lädt.

Die Einstiegspunkte, auf die im *lpEntryPoints-Parameter* verwiesen wird, enthalten Zeiger auf die folgenden Exportfunktionen, die in der hier dargestellten Reihenfolge bereitgestellt werden müssen.

-   [Registrieren](register-parser.md)
-   [Registrierung aufheben](deregister.md)
-   [RecognizeFrame](recognizeframe.md)
-   [AttachProperties](attachproperties.md)
-   [FormatProperties](formatproperties.md)



| Für Informationen zu                                                                                 | Siehe                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Was Parser sind und wie sie mit Netzwerkmonitor.                                          | [Parser](parsers.md)                                  |
| Die Implementierung von **DllMain enthält** ein Beispiel für den Aufruf **von CreateProtocol** in **DllMain.** | [Implementieren von DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

