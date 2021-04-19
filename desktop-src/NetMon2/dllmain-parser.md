---
description: Die DllMain-Exportfunktion für den Parser identifiziert das vorhanden sein des Parsers und gibt Ressourcen frei, die von Netzwerkmonitor für den Parser verwendet werden. DllMain muss in allen Parser-DLLs implementiert werden.
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: DllMain-Parser-Rückruffunktion (Process. h)
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
ms.openlocfilehash: 1db69d51f3a46bbe219ef7f7bdea67e8e8970e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360646"
---
# <a name="dllmain-parser-callback-function"></a>DllMain-Parser-Rückruffunktion

Die **DllMain** -Exportfunktion für den Parser identifiziert das vorhanden sein des Parsers und gibt Ressourcen frei, die von Netzwerkmonitor für den Parser verwendet werden. **DllMain** muss in allen Parser-DLLs implementiert werden.

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

*HINSTANCE* \[ in\]
</dt> <dd>

Handle für eine Instanz des Parsers.

</dd> <dt>

*Befehl* \[ in\]
</dt> <dd>

Indikator, um zu bestimmen, warum die Funktion aufgerufen wird. Eine Liste aller möglichen Flags finden Sie unter [DllMain](/windows/desktop/Dlls/dllmain). Die Parser-Implementierung muss die folgenden Werte verarbeiten.



| Wert                                                                                                                                                                         | Bedeutung                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**DLL- \_ Prozess \_ Anfügen**</dt> </dl> | Wenn **DllMain** zum ersten Mal aufgerufen wird, muss die dll "up [Protocol](createprotocol.md) " aufrufen, um Informationen für Netzwerkmonitor bereitzustellen. <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**Trennen des DLL- \_ Prozesses \_**</dt> </dl> | Wenn **DllMain** zum letzten Mal aufgerufen wird, muss die DLL [destroyprotocol](destroyprotocol.md) aufrufen, um die von der dll verwendeten Ressourcen freizugeben. <br/> |



 

</dd> <dt>

*Reserved* 
</dt> <dd>

Wird jetzt nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Parser-DLL gibt immer **true** zurück.

## <a name="remarks"></a>Bemerkungen

Das Betriebssystem ruft **DllMain** auf, um die Parser-DLL zu laden und zu entladen. Diese Funktion basiert auf der [DllMain](/windows/desktop/Dlls/dllmain) -Funktion der Dynamic-Link Library.

Sie können auch die Implementierung von **DllMain** verwenden, um eine Instanz eines Parsers für die spätere Verwendung zu speichern. Beispielsweise können Sie eine Parser-DLL-Instanz speichern und diese dann für einen System Aufrufvorgang in Zukunft verwenden.



| Für Informationen zu                                        | Siehe                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren. | [Parser](parsers.md)                                  |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.        | [Architektur der Parser-DLL](parser-dll-architecture.md)  |
| Zur Implementierung von **DllMain**  gehört ein Beispiel.        | [Implementieren von DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Process. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

["Kreateprotocol"](createprotocol.md)
</dt> <dt>

[Destroyprotocol](destroyprotocol.md)
</dt> <dt>

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

