---
description: Die DllMain-Exportfunktion für den Parser identifiziert das Vorhandensein des Parsers und gibt Ressourcen frei, Netzwerkmonitor parser verwenden. DllMain muss in allen Parser-DLLs implementiert werden.
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: DllMain Parser-Rückruffunktion (Process.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 5df58ef86971fcf60e79fbae8e92313dbd0b0371e2311cc30b494950e4f37dd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890840"
---
# <a name="dllmain-parser-callback-function"></a>DllMain Parser-Rückruffunktion

Die **DllMain-Exportfunktion** für den Parser identifiziert das Vorhandensein des Parsers und gibt Ressourcen frei, die Netzwerkmonitor parser verwenden. **DllMain** muss in allen Parser-DLLs implementiert werden.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI DllMain(
  _In_ HANDLE hInstance,
  _In_ ULONG  Command,
       LPVOID Reserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hInstance* \[ In\]
</dt> <dd>

Handle für eine Instanz des Parsers.

</dd> <dt>

*Befehl* \[ In\]
</dt> <dd>

Indikator, um zu bestimmen, warum die Funktion aufgerufen wird. Eine Liste aller möglichen Flags finden Sie unter [DllMain](/windows/desktop/Dlls/dllmain). Die Parserimplementierung muss die folgenden Werte verarbeiten.



| Wert                                                                                                                                                                         | Bedeutung                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**ANFÜGEN \_ DES \_ DLL-PROZESSES**</dt> </dl> | Wenn **DllMain** zum ersten Mal aufgerufen wird, muss die DLL [CreateProtocol](createprotocol.md) aufrufen, um Informationen für die Netzwerkmonitor. <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**\_ \_ DLL-PROZESSTRENNVORGANG**</dt> </dl> | Wenn **DllMain** zum letzten Mal aufgerufen wird, muss die DLL [DestroyProtocol](destroyprotocol.md) aufrufen, um die von der DLL verwendeten Ressourcen frei zu geben. <br/> |



 

</dd> <dt>

*Reserved* 
</dt> <dd>

Wird jetzt nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Parser-DLL gibt immer **TRUE zurück.**

## <a name="remarks"></a>Hinweise

Das Betriebssystem ruft **DllMain auf,** um die Parser-DLL zu laden und zu entladen. Diese Funktion basiert auf der [DllMain-Funktion](/windows/desktop/Dlls/dllmain) der Dynamic Link Library.

Sie können auch die Implementierung von **DllMain** verwenden, um eine Instanz eines Parsers für die zukünftige Verwendung zu speichern. Beispielsweise können Sie eine Parser-DLL-Instanz speichern und sie dann in Zukunft für einen Systemaufruf verwenden.



| Für Informationen zu                                        | Siehe                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Was Parser sind und wie sie mit Netzwerkmonitor. | [Parser](parsers.md)                                  |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.        | [Parser-DLL-Architektur](parser-dll-architecture.md)  |
| Die Implementierung von **DllMain enthält**  ein Beispiel.        | [Implementieren von DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Process.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[CreateProtocol](createprotocol.md)
</dt> <dt>

[DestroyProtocol](destroyprotocol.md)
</dt> <dt>

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

