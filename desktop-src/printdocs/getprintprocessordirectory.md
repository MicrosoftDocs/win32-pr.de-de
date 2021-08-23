---
description: Die GetPrintProcessorDirectory-Funktion ruft den Pfad zum Druckprozessorverzeichnis auf dem angegebenen Server ab.
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
title: GetPrintProcessorDirectory-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintProcessorDirectory
- GetPrintProcessorDirectoryA
- GetPrintProcessorDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 27e79305295d078912169a2a12a99aa516372486f9b5dcd1997161a030103dee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719250"
---
# <a name="getprintprocessordirectory-function"></a>GetPrintProcessorDirectory-Funktion

Die **GetPrintProcessorDirectory-Funktion** ruft den Pfad zum Druckprozessorverzeichnis auf dem angegebenen Server ab.

## <a name="syntax"></a>Syntax


```C++
BOOL GetPrintProcessorDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt. Wenn dieser Parameter **NULL** ist, wird ein lokaler Pfad zurückgegeben.

</dd> <dt>

*pEnvironment* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt (z. B. Windows x86, Windows IA64 oder Windows x64). Wenn dieser Parameter **NULL** ist, wird die aktuelle Umgebung der aufrufenden Anwendung und des Clientcomputers (nicht der Zielanwendung und des Druckerservers) verwendet.

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Die Strukturebene. Dieser Wert muss 1 sein.

</dd> <dt>

*pPrintProcessorInfo* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Pfad empfängt. Beachten Sie, dass der Pfad für Betriebssysteme vor Windows Server 2003 SP 1 im lokalen Format für den Server und nicht im echten Remoteformat vorliegt. Beispielsweise wird der Pfad als "%Windir% \\ System32 \\ Spool \\ Prtprocs \\ %Environment%" anstelle von \\ \\ "ServerName \\ Print$ \\ Prtprocs \\ %Environment%" angegeben, auch wenn er für einen Remoteserver aufgerufen wird. Für die Betriebssysteme Windows Server 2003 SP 1 und höher wird der echte Remotepfad zurückgegeben.

</dd> <dt>

*cbBuf* \[ In\]
</dt> <dd>

Die Größe des Puffers, auf den *pPrintProcessorInfo* zeigt.

</dd> <dt>

*"Needed"* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Wert, der die Anzahl der kopierten Bytes angibt, wenn die Funktion erfolgreich ausgeführt wird, oder die Anzahl der Bytes, die erforderlich sind, wenn *cbBuf* zu klein ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **GetPrintProcessorDirectoryW** (Unicode) und **GetPrintProcessorDirectoryA** (ANSI)<br/>           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> </dl>

 

 




