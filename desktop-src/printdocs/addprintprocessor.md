---
description: Die addprintprocessor-Funktion installiert einen Druck Prozessor auf dem angegebenen Server und fügt der Liste der unterstützten Druck Prozessoren den Druck Prozessor Namen hinzu.
ms.assetid: 99899cee-f74d-4405-8ea5-616e3769aba9
title: Addprintprocessor-Funktion (winspool. h)
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
ms.openlocfilehash: 871df9fee211ae13e1552978ce651840d7f542f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351492"
---
# <a name="addprintprocessor-function"></a>Addprintprocessor-Funktion

Die **addprintprocessor** -Funktion installiert einen Druck Prozessor auf dem angegebenen Server und fügt der Liste der unterstützten Druck Prozessoren den Druck Prozessor Namen hinzu.

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

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, auf dem der Druck Prozessor installiert werden soll. Wenn dieser Parameter **null** ist, wird der Druck Prozessor lokal installiert.

</dd> <dt>

nach-oben  \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt (z. b. Windows x86, Windows ia64 oder Windows x64). Wenn dieser Parameter **null** ist, wird die aktuelle Umgebung des Aufrufers/Clients (nicht des Ziels/Servers) verwendet.

</dd> <dt>

*ppathname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen der Datei angibt, die den Druck Prozessor enthält. Diese Datei muss sich im Systemdruck Prozessor Verzeichnis befinden.

</dd> <dt>

*pprintprocessorname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druck Prozessors angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Der [Aufrufer muss über die SeLoadDriverPrivilege-Berechtigung](/windows/desktop/SecAuthZ/authorization-constants)verfügen.

Vor dem Aufrufen der **addprintprocessor** -Funktion muss eine Anwendung überprüfen, ob die Datei, in der der Druck Prozessor enthalten ist, im Systemdruck Prozessor Verzeichnis gespeichert wird. Eine Anwendung kann den Namen des Systemdruck Prozessor-Verzeichnisses abrufen, indem Sie die [**getprintprocessordirectory**](getprintprocessordirectory.md) -Funktion aufrufen.

Eine Anwendung kann den Namen vorhandener Druck Prozessoren ermitteln, indem die [**enumprintprocessor**](enumprintprocessors.md) -Funktion aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Addprintprocessorw** (Unicode) und **addprintprocessora** (ANSI)<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Enumprintprozessoren**](enumprintprocessors.md)
</dt> <dt>

[**Getprintprocessordirectory**](getprintprocessordirectory.md)
</dt> </dl>

 

