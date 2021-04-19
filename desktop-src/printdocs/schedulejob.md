---
description: Die schedulejob-Funktion fordert an, dass der Druck Spooler einen angegebenen Druckauftrag zum Drucken plant.
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
title: Schedulejob-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScheduleJob
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 1ef938cc2a9b1893a4825255325457d5c210842a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363231"
---
# <a name="schedulejob-function"></a>Schedulejob-Funktion

Die **schedulejob** -Funktion fordert an, dass der Druck Spooler einen angegebenen Druckauftrag zum Drucken plant.

## <a name="syntax"></a>Syntax


```C++
BOOL ScheduleJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  dwJobID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker für den Druckauftrag. Dabei muss es sich um einen lokalen Drucker handeln, der als Druck Drucker konfiguriert ist. Wenn *hprinter* ein Handle für eine Remote Druckerverbindung ist oder wenn der Drucker für den direkten Druck konfiguriert ist, tritt bei der **schedulejob** -Funktion ein Fehler auf. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

*hprinter* muss das gleiche Drucker Handle sein, das im [**AddJob**](addjob.md) -Rückruf angegeben wurde, der den *dwjobid* -Druckauftrags Bezeichner abgerufen hat.

</dd> <dt>

*dwjobid* \[ in\]
</dt> <dd>

Der Druckauftrag, der geplant werden soll. Sie erhalten diese Druckauftrags Kennung durch Aufrufen der [**AddJob**](addjob.md) -Funktion.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Sie müssen die [**AddJob**](addjob.md) -Funktion erfolgreich aufrufen, bevor Sie die **schedulejob** -Funktion aufrufen. **AddJob** erhält den Druckauftrags Bezeichner, den Sie als *dwjobid* an **schedulejob** übergeben. Beide Aufrufe müssen den gleichen Wert für *hprinter* verwenden.

Die **schedulejob** -Funktion prüft auf eine gültige Spooldatei. Wenn eine Spooldatei ungültig ist oder leer ist, löscht **schedulejob** sowohl die Spooldatei als auch den entsprechenden Druckauftrags Eintrag im Druck Spooler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




