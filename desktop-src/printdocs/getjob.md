---
description: Die GetJob-Funktion ruft Informationen zu einem angegebenen Druckauftrag ab.
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
title: GetJob-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetJob
- GetJobA
- GetJobW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 26665d6141ea36adbe8aeeca0555bc6a5e918cb5213a4fb7a6dbd315eac92a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949081"
---
# <a name="getjob-function"></a>GetJob-Funktion

Die **GetJob-Funktion** ruft Informationen zu einem angegebenen Druckauftrag ab.

## <a name="syntax"></a>Syntax


```C++
BOOL GetJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   JobId,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker, für den die Druckauftragsdaten abgerufen werden. Verwenden Sie die [**OpenPrinter-**](openprinter.md) oder [**AddPrinter-Funktion,**](addprinter.md) um ein Druckerhandle abzurufen.

</dd> <dt>

*JobId* \[ In\]
</dt> <dd>

Identifiziert den Druckauftrag, für den Daten abgerufen werden sollen. Verwenden Sie die [**AddJob-Funktion**](addjob.md) oder die [**StartDoc-Funktion,**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) um einen Druckauftragsbezeichner abzurufen.

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Der Im *pJob-Puffer* zurückgegebene Informationstyp. Wenn *Level* 1 ist, empfängt *pJob* eine [**JOB INFO \_ \_ 1-Struktur.**](job-info-1.md) Wenn *Level* gleich 2 ist, empfängt *pJob* eine [**JOB INFO \_ \_ 2-Struktur.**](job-info-2.md)

</dd> <dt>

*pJob* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine [**JOB \_ INFO \_ 1-**](job-info-1.md) oder [**JOB INFO \_ \_ 2-Struktur**](job-info-2.md) empfängt, die Informationen zum Auftrag enthält. Der Puffer muss groß genug sein, um die Zeichenfolgen zu speichern, auf die die Strukturmember verweisen.

Um die erforderliche Puffergröße zu bestimmen, rufen **Sie GetJob** auf, wobei *cbBuf* auf 0 (null) festgelegt ist. **GetJob** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ INSUFFICIENT BUFFER \_ zurück, und der parameter *pwNeeded* gibt die Größe des Puffers in Bytes zurück, der zum Speichern des Arrays von Strukturen und deren Daten erforderlich ist.

</dd> <dt>

*cbBuf* \[ In\]
</dt> <dd>

Die Größe des Arrays in Bytes.

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
| Unicode- und ANSI-Name<br/>   | **GetJobW** (Unicode) und **GetJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addjob**](addjob.md)
</dt> <dt>

[**AUFTRAGSINFORMATIONEN \_ \_ 1**](job-info-1.md)
</dt> <dt>

[**AUFTRAGSINFORMATIONEN \_ \_ 2**](job-info-2.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

