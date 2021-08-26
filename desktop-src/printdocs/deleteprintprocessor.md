---
description: Die DeletePrintProcessor-Funktion entfernt einen Druckprozessor, der von der AddPrintProcessor-Funktion hinzugefügt wurde.
ms.assetid: 65c77874-aa2c-4b4c-b218-fad361270a3e
title: DeletePrintProcessor-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProcessor
- DeletePrintProcessorA
- DeletePrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: be88839ae51fc52d453e1171a8ed0489df7827dda9476bf5e27d9f3d6a16ee1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949990"
---
# <a name="deleteprintprocessor-function"></a>DeletePrintProcessor-Funktion

Die **DeletePrintProcessor-Funktion** entfernt einen Druckprozessor, der von der [**AddPrintProcessor-Funktion**](addprintprocessor.md) hinzugefügt wurde.

## <a name="syntax"></a>Syntax


```C++
BOOL DeletePrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, von dem der Prozessor entfernt werden soll. Wenn dieser Parameter **NULL** ist, wird der Druckerprozessor lokal entfernt.

</dd> <dt>

*pEnvironment* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, aus der der Prozessor entfernt werden soll (z. B. Windows NT x86, Windows IA64 oder Windows x64). Wenn dieser Parameter **NULL** ist, wird der Prozessor aus der aktuellen Umgebung der aufrufenden Anwendung und des Clientcomputers (nicht der Zielanwendung und des Druckerservers) entfernt. **NULL** ist der empfohlene Wert, da er maximale Portabilität bietet.

</dd> <dt>

*pPrintProcessorName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu entfernenden Prozessors angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Der Aufrufer muss über [seLoadDriverPrivilege verfügen.](/windows/desktop/SecAuthZ/authorization-constants)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **DeletePrintProcessorW** (Unicode) und **DeletePrintProcessorA** (ANSI)<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> </dl>

 

