---
description: Die GetJob-Funktion Ruft Informationen zu einem angegebenen Druckauftrag ab.
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
title: GetJob-Funktion (winspool. h)
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
ms.openlocfilehash: 73ae36ebab4530bf21eb86918fdbbbe941ed0741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215973"
---
# <a name="getjob-function"></a>GetJob-Funktion

Die **GetJob** -Funktion Ruft Informationen zu einem angegebenen Druckauftrag ab.

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

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker, für den die Druckauftrags Daten abgerufen werden. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*JobID* \[ in\]
</dt> <dd>

Identifiziert den Druckauftrag, für den Daten abgerufen werden sollen. Verwenden Sie die [**AddJob**](addjob.md) -Funktion oder die [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) -Funktion, um einen Druckauftrags Bezeichner zu erhalten.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Der Typ der Informationen, die im *pjob* -Puffer zurückgegeben werden. Wenn *Level den Wert* 1 hat, empfängt *pjob* die Struktur [**Job \_ Info \_ 1**](job-info-1.md) . Wenn *Level* 2 ist, empfängt *pjob* eine Struktur mit [**Auftrags \_ Informationen \_ 2**](job-info-2.md) .

</dd> <dt>

*pjob* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine [**Auftrags \_ Info \_ 1**](job-info-1.md) oder eine [**Auftrags \_ Info \_ 2**](job-info-2.md) -Struktur mit Informationen über den Auftrag empfängt. Der Puffer muss groß genug sein, um die Zeichen folgen zu speichern, auf die von den Strukturmembern verwiesen wird.

Um die erforderliche Puffergröße zu ermitteln, nennen Sie **GetJob** , bei dem *cbbuf* auf NULL festgelegt ist. **GetJob** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt fehlerhaften \_ Puffer zurück \_ , und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.

</dd> <dt>

*cbbuf* \[ in\]
</dt> <dd>

Die Größe des Arrays in Bytes.

</dd> <dt>

*pcbbenötigte* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen-Wert, der die Anzahl der kopierten Bytes angibt, wenn die Funktion erfolgreich ist, oder die Anzahl der Bytes, die erforderlich sind, wenn *cbbuf* zu klein ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Getjobw** (Unicode) und **getjoba** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**Auftrags \_ Informationen \_ 1**](job-info-1.md)
</dt> <dt>

[**Auftrags \_ Informationen \_ 2**](job-info-2.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**Setjob**](setjob.md)
</dt> </dl>

 

