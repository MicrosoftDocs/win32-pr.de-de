---
description: Die EnumJobs-Funktion Ruft Informationen zu einem angegebenen Satz von Druckaufträgen für einen angegebenen Drucker ab.
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: EnumJobs-Funktion (winspool. h)
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
ms.openlocfilehash: 174f58ba3fb1012e6ff46612fe312579969e6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217019"
---
# <a name="enumjobs-function"></a>EnumJobs-Funktion

Die **EnumJobs** -Funktion Ruft Informationen zu einem angegebenen Satz von Druckaufträgen für einen angegebenen Drucker ab.

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

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für das Drucker Objekt, dessen Druckaufträge die Funktion auflistet. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*Firstjob* \[ in\]
</dt> <dd>

Die null basierte Position innerhalb der Druck Warteschlange des ersten aufzuzählenden Druckauftrags. Der Wert 0 gibt beispielsweise an, dass die Enumeration beim ersten Druckauftrag in der Druck Warteschlange beginnen soll. der Wert 9 gibt an, dass die Enumeration mit dem zehnten Druckauftrag in der Druck Warteschlange beginnen soll.

</dd> <dt>

*Nojobs* \[ in\]
</dt> <dd>

Die Gesamtanzahl der aufzuzählenden Druckaufträge.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Der Typ der Informationen, die im *pjob* -Puffer zurückgegeben werden.



| Wert                                                                                                | Bedeutung                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | *pjob* empfängt ein Array von [**Auftrags \_ Informationen \_ 1**](job-info-1.md) -Strukturen<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | *pjob* empfängt ein Array von [**Auftrags \_ Informationen \_ 2**](job-info-2.md) -Strukturen.<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | *pjob* empfängt ein Array von [**Auftrags \_ Informationen \_ 3**](job-info-3.md) -Strukturen.<br/> |



 

</dd> <dt>

*pjob* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der ein Array mit den Strukturen Job [**\_ Info \_ 1**](job-info-1.md), [**Job \_ Info \_ 2**](job-info-2.md)oder [**Job \_ Info \_ 3**](job-info-3.md) empfängt. Der Puffer muss groß genug sein, um das Array von Strukturen und Zeichen folgen oder andere Daten zu erhalten, auf die die Strukturmember zeigen.

Um die erforderliche Puffergröße zu ermitteln, muss **EnumJobs** aufgerufen werden, wobei *cbbuf* auf NULL festgelegt ist. **EnumJobs** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt fehlerhaften \_ Puffer zurück \_ , und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.

</dd> <dt>

*cbbuf* \[ in\]
</dt> <dd>

Die Größe des *pjob* -Puffers in Bytes.

</dd> <dt>

*pcbbenötigte* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der kopierten Bytes empfängt, wenn die Funktion erfolgreich ausgeführt wird. Wenn die Funktion fehlschlägt, erhält die Variable die erforderliche Anzahl von Bytes.

</dd> <dt>

*pkreturned* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der im *pjob* -Puffer zurückgegebenen Struktur von [**Auftrags \_ Informationen \_ 1**](job-info-1.md), [**Auftrags \_ Informationen \_ 2**](job-info-2.md)oder [**Auftrags \_ Informationen \_ 3**](job-info-3.md) empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Die Struktur der [**Auftrags \_ Informationen \_ 1**](job-info-1.md) enthält allgemeine Druckauftrags Informationen. die Struktur der [**Auftrags \_ Informationen \_ 2**](job-info-2.md) enthält wesentlich ausführlichere Informationen. Die [**Auftrags \_ Info \_ 3**](job-info-3.md) -Struktur enthält Informationen darüber, wie Aufträge verknüpft werden.

Um die Anzahl der Druckaufträge in der Drucker Warteschlange zu ermitteln, müssen Sie die [**GetPrinter**](getprinter.md) -Funktion mit dem auf 2 festgelegten *Level* -Parameter aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Enumjobsw** (Unicode) und **enumjobsa** (ANSI)<br/>                                               |



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

[**Auftrags \_ Informationen \_ 1**](job-info-1.md)
</dt> <dt>

[**Auftrags \_ Informationen \_ 2**](job-info-2.md)
</dt> <dt>

[**Auftrags \_ Informationen \_ 3**](job-info-3.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Setjob**](setjob.md)
</dt> </dl>

 

