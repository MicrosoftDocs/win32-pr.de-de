---
description: Die EnumJobs-Funktion ruft Informationen zu einem angegebenen Satz von Druckaufträgen für einen angegebenen Drucker ab.
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: EnumJobs-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumJobs
- EnumJobsA
- EnumJobsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 57c8416b1c1f5820f632271b0ef0973c76a14be9ef08f24b217ebee441fb29d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118056510"
---
# <a name="enumjobs-function"></a>EnumJobs-Funktion

Die **EnumJobs-Funktion** ruft Informationen zu einem angegebenen Satz von Druckaufträgen für einen angegebenen Drucker ab.

## <a name="syntax"></a>Syntax


```C++
BOOL EnumJobs(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   FirstJob,
  _In_  DWORD   NoJobs,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für das Druckerobjekt, dessen Druckaufträge die Funktion aufzählt. Verwenden Sie [**die OpenPrinter-**](openprinter.md) [**oder AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> <dt>

*FirstJob* \[ In\]
</dt> <dd>

Die nullbasierte Position innerhalb der Druckwarteschlange des ersten aufzählten Druckauftrags. Beispielsweise gibt der Wert 0 an, dass die Enumeration beim ersten Druckauftrag in der Druckwarteschlange beginnen soll. Der Wert 9 gibt an, dass die Enumeration beim zehnten Druckauftrag in der Druckwarteschlange beginnen soll.

</dd> <dt>

*NoJobs* \[ In\]
</dt> <dd>

Die Gesamtanzahl der aufzählten Druckaufträge.

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Der Typ der im *pJob-Puffer zurückgegebenen* Informationen.



| Wert                                                                                                | Bedeutung                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | *pJob* empfängt ein Array von [**JOB \_ INFO \_ 1-Strukturen**](job-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | *pJob* empfängt ein Array von [**JOB \_ INFO \_ 2-Strukturen**](job-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | *pJob* empfängt ein Array von [**JOB \_ INFO \_ 3-Strukturen**](job-info-3.md)<br/> |



 

</dd> <dt>

*pJob* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der ein Array von [**JOB \_ INFO \_ 1-,**](job-info-1.md) [**JOB INFO \_ \_ 2-**](job-info-2.md)oder [**JOB INFO \_ \_ 3-Strukturen empfängt.**](job-info-3.md) Der Puffer muss groß genug sein, um das Array von Strukturen und alle Zeichenfolgen oder andere Daten zu empfangen, auf die die Strukturmitglieder zeigen.

Um die erforderliche Puffergröße zu bestimmen, rufen Sie **EnumJobs** mit *cbBuf* auf 0 (null) auf. **Bei EnumJobs** tritt ein Fehler auf, [**getLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR INSUFFICIENT BUFFER zurück, und der \_ Parameter \_ *"enumJobs"* gibt die Größe des Puffers in Bytes zurück, der zum Speichern des Arrays von Strukturen und deren Daten erforderlich ist.

</dd> <dt>

*cbBuf* \[ In\]
</dt> <dd>

Die Größe des *pJob-Puffers* in Bytes.

</dd> <dt>

*-Needed* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der kopierten Bytes empfängt, wenn die Funktion erfolgreich ist. Wenn die Funktion fehlschlägt, empfängt die Variable die erforderliche Anzahl von Bytes.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der im pJob-Puffer zurückgegebenen [**JOB INFO \_ \_ 1-,**](job-info-1.md) [**JOB INFO \_ \_ 2-**](job-info-2.md)oder [**JOB INFO \_ \_ 3-Strukturen**](job-info-3.md) empfängt. 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Die [**JOB \_ INFO \_ 1-Struktur**](job-info-1.md) enthält allgemeine Druckauftragsinformationen. Die [**STRUKTUR JOB INFO \_ \_ 2**](job-info-2.md) enthält viel ausführlichere Informationen. Die [**JOB \_ INFO \_ 3-Struktur**](job-info-3.md) enthält Informationen dazu, wie Aufträge verknüpft werden.

Um die Anzahl der Druckaufträge in der Druckerwarteschlange zu bestimmen, rufen Sie die [**GetPrinter-Funktion**](getprinter.md) auf, und legen Sie dabei *den Level-Parameter* auf 2 fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **EnumJobsW** (Unicode) und **EnumJobsA** (ANSI)<br/>                                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**AUFTRAGSINFORMATIONEN \_ \_ 1**](job-info-1.md)
</dt> <dt>

[**AUFTRAGSINFORMATIONEN \_ \_ 2**](job-info-2.md)
</dt> <dt>

[**AUFTRAGSINFORMATIONEN \_ \_ 3**](job-info-3.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

