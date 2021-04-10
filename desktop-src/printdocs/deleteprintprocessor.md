---
description: Die deleteprintprocessor-Funktion entfernt einen von der addprintprocessor-Funktion hinzugefügten Druck Prozessor.
ms.assetid: 65c77874-aa2c-4b4c-b218-fad361270a3e
title: Deleteprintprocessor-Funktion (winspool. h)
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
ms.openlocfilehash: 241efaad91e1587209f2ef2a905bc0e095c6b40c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215861"
---
# <a name="deleteprintprocessor-function"></a>Deleteprintprocessor-Funktion

Die **deleteprintprocessor** -Funktion entfernt einen von der [**addprintprocessor**](addprintprocessor.md) -Funktion hinzugefügten Druck Prozessor.

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

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, von dem der Prozessor entfernt werden soll. Wenn dieser Parameter **null** ist, wird der Drucker Prozessor lokal entfernt.

</dd> <dt>

nach-oben  \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, aus der der Prozessor entfernt werden soll (z. b. Windows NT x86, Windows ia64 oder Windows x64). Wenn dieser Parameter **null** ist, wird der Prozessor aus der aktuellen Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) entfernt. **Null** ist der empfohlene Wert, da er eine maximale Portabilität ermöglicht.

</dd> <dt>

*pprintprocessorname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu entfernenden Prozessors angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Der [Aufrufer muss über die SeLoadDriverPrivilege-Berechtigung](/windows/desktop/SecAuthZ/authorization-constants)verfügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Deleteprintprocessorw** (Unicode) und **deleteprintprocessora** (ANSI)<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprintprocessor**](addprintprocessor.md)
</dt> </dl>

 

