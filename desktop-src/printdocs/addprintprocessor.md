---
description: Die AddPrintProcessor-Funktion installiert einen Druckprozessor auf dem angegebenen Server und fügt den Namen des Druckprozessors der Liste der unterstützten Druckprozessoren hinzu.
ms.assetid: 99899cee-f74d-4405-8ea5-616e3769aba9
title: AddPrintProcessor-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProcessor
- AddPrintProcessorA
- AddPrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 83de05dd6aa0ef6541322a45894dcf24cffa3cc6bebcbbd3b42e6c48941360b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868745"
---
# <a name="addprintprocessor-function"></a>AddPrintProcessor-Funktion

Die **AddPrintProcessor-Funktion** installiert einen Druckprozessor auf dem angegebenen Server und fügt den Namen des Druckprozessors der Liste der unterstützten Druckprozessoren hinzu.

## <a name="syntax"></a>Syntax


```C++
BOOL AddPrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPathName,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Servers angibt, auf dem der Druckprozessor installiert werden soll. Wenn dieser Parameter **NULL ist,** wird der Druckprozessor lokal installiert.

</dd> <dt>

*pUmgebung* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die die Umgebung angibt (z. B. Windows x86, Windows IA64 oder Windows x64). Wenn dieser Parameter **NULL ist,** wird die aktuelle Umgebung des Aufrufers/Clients (nicht des Ziels/Servers) verwendet.

</dd> <dt>

*pPathName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen der Datei angibt, die den Druckprozessor enthält. Diese Datei muss sich im Systemverzeichnis für den Druckprozessor befinden.

</dd> <dt>

*pPrintProcessorName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Druckprozessors angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Der Aufrufer muss über [seLoadDriverPrivilege verfügen.](/windows/desktop/SecAuthZ/authorization-constants)

Vor dem Aufrufen **der AddPrintProcessor-Funktion** sollte eine Anwendung überprüfen, ob die Datei mit dem Druckprozessor im Druckprozessorverzeichnis des Systems gespeichert ist. Eine Anwendung kann den Namen des Druckprozessorverzeichnisses des Systems abrufen, indem die [**GetPrintProcessorDirectory-Funktion aufgerufen**](getprintprocessordirectory.md) wird.

Eine Anwendung kann den Namen vorhandener Druckprozessoren ermitteln, indem sie die [**EnumPrintProcessors-Funktion**](enumprintprocessors.md) aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **AddPrintProcessorW** (Unicode) und **AddPrintProcessorA** (ANSI)<br/>                             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> <dt>

[**GetPrintProcessorDirectory**](getprintprocessordirectory.md)
</dt> </dl>

 

