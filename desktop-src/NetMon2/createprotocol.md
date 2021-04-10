---
description: Mit der Funktion "-Funktion" wird Netzwerkmonitor benachrichtigt, dass ein bestimmter Protokoll Parser vorhanden ist.
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: Funktion "up Protocol" (Netmon. h)
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
ms.openlocfilehash: 0b35f9505758256750ae02d24d6c2a84ed0646b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131857"
---
# <a name="createprotocol-function"></a>Funktion "up Protocol"

Mit **der Funktion** "-Funktion" wird Netzwerkmonitor benachrichtigt, dass ein bestimmter Protokoll Parser vorhanden ist.

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

*ProtocolName* \[ in\]
</dt> <dd>

Der Name des Protokolls, das vom Parser erkannt wird.

</dd> <dt>

*lpentrypoints* \[ in\]
</dt> <dd>

Eine [entryPoints](entrypoints.md) -Struktur, die die verbleibenden Parser-DLL-Einstiegspunkte enthält. In den Hinweisen finden Sie eine Liste der Exportfunktionen, auf die jeder Einstiegspunkt verweist. Einstiegspunkte müssen in der Reihenfolge angegeben werden, in der die **entryPoints** -Struktur angegeben ist.

</dd> <dt>

*cbentrypoints* \[ in\]
</dt> <dd>

Die Größe der **entryPoints** -Struktur. Netzwerkmonitor stellt ein Makro der entryPoints- \_ Größe bereit, mit dem Sie die Größe der Struktur angeben können.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für das Protokoll.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Die Parser-DLL ruft während der Implementierung von [DllMain](dllmain-parser.md)" **kreateprotocol** " auf. Die **Funktion "** Funktion" wird aufgerufen, wenn das Betriebssystem die Parser-DLL zum ersten Mal lädt.

Die Einstiegspunkte, auf die im *lpentrypoints* -Parameter verwiesen wird, enthalten Verweise auf die folgenden Exportfunktionen, die in der hier dargestellten Reihenfolge bereitgestellt werden müssen.

-   [Registrieren](register-parser.md)
-   [Registrierung aufheben](deregister.md)
-   [Erkenzeframe](recognizeframe.md)
-   [Attachproperties](attachproperties.md)
-   [Formatproperties](formatproperties.md)



| Für Informationen zu                                                                                 | Siehe                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.                                          | [Parser](parsers.md)                                  |
| Zum Implementieren von **DllMain** ist ein Beispiel für das Aufrufen von **createprotocol** in **DllMain** enthalten. | [Implementieren von DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

