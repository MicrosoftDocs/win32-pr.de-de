---
description: Die ScheduleJob-Funktion fordert an, dass der Druckspooler einen angegebenen Druckauftrag für den Druck plant.
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
title: ScheduleJob-Funktion (Winspool.h)
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
ms.openlocfilehash: 9a09d3e67b4be422f10db7761f28a2aa873e9bd0d84ec2c09de23ae20c7cea4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470225"
---
# <a name="schedulejob-function"></a>ScheduleJob-Funktion

Die **ScheduleJob-Funktion** fordert an, dass der Druckspooler einen angegebenen Druckauftrag für den Druck plant.

## <a name="syntax"></a>Syntax


```C++
BOOL ScheduleJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  dwJobID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker für den Druckauftrag. Dies muss ein lokaler Drucker sein, der als Spooldrucker konfiguriert ist. Wenn *hPrinter* ein Handle für eine Remotedruckerverbindung ist oder der Drucker für den direkten Druck konfiguriert ist, schlägt die **ScheduleJob-Funktion** fehl. Verwenden Sie die [**OpenPrinter-**](openprinter.md) oder [**AddPrinter-Funktion,**](addprinter.md) um ein Druckerhandle abzurufen.

*hPrinter* muss das gleiche Druckerhandle sein, das im Aufruf von [**AddJob**](addjob.md) angegeben wurde und den DwJobID-Druckauftragsbezeichner abgerufen hat. 

</dd> <dt>

*dwJobID* \[ In\]
</dt> <dd>

Der druckauftrag, der geplant werden soll. Sie erhalten diesen Druckauftragsbezeichner, indem Sie die [**AddJob-Funktion**](addjob.md) aufrufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Sie müssen die [**AddJob-Funktion**](addjob.md) erfolgreich aufrufen, bevor Sie die **ScheduleJob-Funktion** aufrufen. **AddJob** ruft den Bezeichner des Druckauftrags ab, den Sie als *dwJobID* an **ScheduleJob** übergeben. Beide Aufrufe müssen den gleichen Wert für *hPrinter* verwenden.

Die **ScheduleJob-Funktion** sucht nach einer gültigen Spooldatei. Wenn eine ungültige Spooldatei vorhanden ist oder sie leer ist, löscht **ScheduleJob** sowohl die Spooldatei als auch den entsprechenden Druckauftragseintrag im Druckspooler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addjob**](addjob.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




