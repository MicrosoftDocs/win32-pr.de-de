---
description: Meldet an den Druckspoolerdienst, ob sich ein XPS-Druckauftrag in der spoolingphase oder der Renderingphase befindet und welcher Teil der Verarbeitung derzeit ausgeführt wird.
ms.assetid: 66f7483d-be98-410d-b0c7-430743397de2
title: Reportjobprocessingprogress-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportJobProcessingProgress
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 327d2f7cffe2f90a5719de38cef4cd3fde17e086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960189"
---
# <a name="reportjobprocessingprogress-function"></a>Reportjobprocessingprogress-Funktion

Meldet an den Druckspoolerdienst, ob sich ein XPS-Druckauftrag in der spoolingphase oder der Renderingphase befindet und welcher Teil der Verarbeitung derzeit ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReportJobProcessingProgress(
  _In_ HANDLE                printerHandle,
  _In_ ULONG                 jobId,
       EPrintXPSJobOperation jobOperation,
       EPrintXPSJobProgress  jobProgress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*printerhandle* \[ in\]
</dt> <dd>

Ein Drucker handle, für das die Funktion Informationen abrufen soll. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*jobId* \[in\]
</dt> <dd>

Identifiziert den Druckauftrag, für den Daten abgerufen werden sollen. Verwenden Sie die [**AddJob**](addjob.md) -Funktion oder die [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) -Funktion, um einen Druckauftrags Bezeichner zu erhalten.

</dd> <dt>

*joboperation* 
</dt> <dd>

Gibt an, ob sich der Auftrag in der spoolingphase oder der Renderingphase befindet.

</dd> <dt>

*jobprogress* 
</dt> <dd>

Gibt an, welcher Teil der Verarbeitung derzeit ausgeführt wird. Dieser Wert bezieht sich abhängig vom Wert von *joboperation* auf Ereignisse in der spoolingphase oder der Renderingphase.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert S \_ OK; andernfalls enthält das **HRESULT** einen Fehlercode.

Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

> [!Note]  
> **Reportjobprocessingprogress** meldet nur den Fortschritt des XPS-Druckauftrags, wenn sich der Druckauftrag in der spoolingphase oder der Renderingphase befindet. **Reportjobprocessingprogress** schlägt fehl, wenn Sie aufgerufen wird, wenn sich der XPS-Druckauftrag nicht in der spoolingphase oder der Renderingphase befindet.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Eprintxpsjoboperation**](eprintxpsjoboperation.md)
</dt> <dt>

[**Eprintxpsjobprogress**](eprintxpsjobprogress.md)
</dt> </dl>

 

