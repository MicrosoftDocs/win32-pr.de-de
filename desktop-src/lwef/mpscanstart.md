---
title: Mpscanstart-Funktion (mpclient. h)
description: Startet einen Scanvorgang.
ms.assetid: 3AF147C8-A41F-4193-AE28-72C1FBD18BA2
keywords:
- Mpscanstart-Funktion Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MpScanStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d343787edc85a18dc7471d19165999a7252d18a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956735"
---
# <a name="mpscanstart-function"></a>Mpscanstart-Funktion

Startet einen Scanvorgang.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpScanStart(
  _In_     MPHANDLE          hMpHandle,
  _In_     MPSCAN_TYPE       ScanType,
  _In_     DWORD             dwScanOptions,
  _In_opt_ PMPSCAN_RESOURCES pScanResources,
  _In_opt_ PMPCALLBACK_INFO  pCallbackInfo,
  _Out_    PMPHANDLE         phScanHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hmphandle* \[ in\]
</dt> <dd>

Typ: **mphandle**

Handle für die Malware Protection Manager-Schnittstelle. Dieses Handle wird von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegeben.

</dd> <dt>

*ScanType* \[ in\]
</dt> <dd>

Typ: **[ **mpscan- \_ Typ**](mpscan-type.md)**

Gibt den Typ des Scanvorgangs an. Dieser Parameter muss einer der Member der [**mpscan- \_ Typenumeration**](mpscan-type.md) sein.

</dd> <dt>

*dwscanoptions* \[ in\]
</dt> <dd>

Typ: **DWORD**

Gibt verschiedene Optionen für den Scanvorgang an.



| Wert                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <dt>**mpscan- \_ Option " \_ None"**</dt> </dl>                               | Eine bestimmte Option wird nicht angefordert.<br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <dt>**mpscan- \_ Option " \_ Async"**</dt> </dl>                            | Der Scanvorgang wird asynchron ausgeführt, wobei **mpscanstart** sofort nach der erfolgreichen Initiierung des Scans zurückgegeben wird. (Der Scanvorgang ist standardmäßig synchron, was bedeutet, dass **mpscanstart** erst zurückgegeben wird, nachdem die Überprüfung abgeschlossen ist.)<br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <dt>**mpscan- \_ options Status \_**</dt> </dl>                   | Der Aufrufer ist daran interessiert, Informationen über den Scan Status über einen Rückruf zu empfangen.<br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <dt>**mpscan- \_ Option \_ LowPriority**</dt> </dl>          | Führen Sie die Überprüfung mit niedriger Priorität aus. (Standardmäßig wird der Scanvorgang mit normaler Priorität ausgeführt.)<br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <dt>**mpscan- \_ Option \_ packedexes**</dt> </dl>             | Scannen Sie gepackte ausführbare Dateien auf mögliche Bedrohungen.<br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <dt>**mpscan- \_ options \_ Archive**</dt> </dl>                   | Scannen Sie Archivinhalte auf mögliche Bedrohungen. Archive sind Dateien mit Erweiterungen wie ZIP, CAB oder tar.<br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <dt>**mpscan- \_ options \_ Heuristik**</dt> </dl>             | Aktivieren der Heuristik-basierten Überprüfung. Dadurch wird nach Bedrohungen gesucht, deren Erkennungstyp auf Heuristik festgelegt ist.<br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <dt>**mpscan- \_ Option \_ Report Friendly**</dt> </dl> | Melden Sie freundliche Elemente in einem Ressourcen Scan. Dies ist nur für die interne Verwendung vorgesehen.<br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <dt>**mpscan- \_ Option \_ Report Unknown**</dt> </dl>    | Unbekannte Elemente in einem Ressourcen Scan melden. Dies ist nur für die interne Verwendung vorgesehen.<br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <dt>**mpscan- \_ Option \_ nokonsolidieren**</dt> </dl>    | Konsolidieren Sie die Scanergebnisse nicht mit der globalen Bedrohungs Ansicht. Dies ist nützlich für einen Client (z. b. einen e-Mail-Client), der die Bereinigungs-UX allein steuern möchte, anstatt die standardmäßige Antischadsoftware-Reinigungs UX zuzulassen Dies ist nur für die interne Verwendung vorgesehen.<br/> |



 

</dd> <dt>

*pscanresources* \[ in, optional\]
</dt> <dd>

Typ: **pmpscan- \_ Ressourcen**

Ein Zeiger auf die Scan Ressourcen Informationen. Dieser Parameter muss für eine schnell Überprüfung **null** sein. Dies ist ein optionaler Parameter für eine vollständige Überprüfung. Für einen Ressourcen Scan muss dieser Parameter mit mindestens einer Ressourcen Informationsstruktur angegeben werden. Um bestimmte Ressourcen zu scannen, muss der Aufrufer über eine **generische \_ Lese** Berechtigung für die Ressource verfügen. Siehe [**mpscan- \_ Ressourcen**](mpscan-resources.md).

</dd> <dt>

*pcallbackinfo* \[ in, optional\]
</dt> <dd>

Typ: **pmpcallback- \_ Informationen**

Ein Zeiger auf die Rückruf Informationen, die verwendet werden, um den Client mit Änderungen des Scan Zustands (z. b. Start und Complete) und Statusinformationen zu Feeds. Die [**mpcallback- \_ Daten**](mpcallback-data.md) , die in der Rückruffunktion zurückgegeben werden, melden den tatsächlichen Überprüfungs Zustand und die Status bezogenen Informationen. Im folgenden finden Sie eine Liste möglicher Rückrufe:



| Wert                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <dt>**mpnotify- \_ Scan \_ Start**</dt> </dl>                            | Der Scan Vorgang wurde gestartet.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <dt>**mpnotify- \_ Scan ist \_ beendet**</dt> </dl>                   | Der Scan Vorgang wurde abgeschlossen. Zusätzliche Informationen sind über die [**mpscan- \_ Daten**](mpscan-data.md) Struktur verfügbar.<br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <dt>**mpnotify- \_ Scan \_ angehalten**</dt> </dl>                         | Der Scan Vorgang wurde angehalten.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <dt>**mpnotify-Scan wird fortgesetzt \_ \_**</dt> </dl>                      | Der Scan Vorgang wurde von der Pause fortgesetzt.<br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <dt>**mpnotify- \_ Scan \_ Abbruch**</dt> </dl>                         | Der Scan Vorgang wurde abgebrochen.<br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <dt>**mpnotify- \_ Scan Status \_**</dt> </dl>                   | Statusinformationen überprüfen. Zusätzliche Informationen (z. b. Ressourcen Statistiken) sind über die [**mpscan- \_ Daten**](mpscan-data.md) Struktur verfügbar.<br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <dt>**mpnotify- \_ Scan \_ Fehler**</dt> </dl>                            | Überprüfen Sie die Fehlerinformationen für eine bestimmte Ressource. Die spezifischen Ressourcen Informationen sind über die [**mpscan- \_ Daten**](mpscan-data.md) Struktur verfügbar.<br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <dt>**mpnotify- \_ Scan \_ infiziert**</dt> </dl>                   | Der Scan hat eine infizierte Ressource gefunden. Beachten Sie, dass dies in den meisten Fällen dazu führt, dass eine Bedrohung am Ende des Scans gemeldet wird. Manchmal kann es aufgrund von Ausschlüssen nicht als Bedrohung materialisiert werden. Weitere Informationen zu infizierten Ressourcen sind über die [**mpscan- \_ Daten**](mpscan-data.md) Struktur verfügbar.<br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <dt>**mpnotify- \_ Scan \_ memorystart**</dt> </dl>          | Der schnell Scan Abschnitt der vollständigen Überprüfung wurde gestartet.<br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <dt>**mpnotify- \_ Scan \_ memorycomplete**</dt> </dl> | Der schnell Scan Abschnitt der vollständigen Überprüfung wurde abgeschlossen.<br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**Interner mpnotify- \_ \_ Fehler**</dt> </dl>          | Generischer Fehler beim Scan Vorgang. Das *HRESULT* in [**mpcallback- \_ Daten**](mpcallback-data.md) enthält den spezifischen Fehlercode.<br/>                                                                                                                                                                   |



 

</dd> <dt>

*phscanhandle* \[ vorgenommen\]
</dt> <dd>

Typ: **pmphandle**

Rückgabe Überprüfungs handle, das den derzeit initiierten Scan bezeichnet. Dieses Handle kann in nachfolgenden Funktionsaufrufen verwendet werden, z. b., um ein Scanergebnis abzurufen. Das Handle muss mit der [**mplenker close**](mphandleclose.md) -Funktion geschlossen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code. Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mperrormessageformat**](mperrormessageformat.md)
</dt> <dt>

[**Mplenker schließen**](mphandleclose.md)
</dt> <dt>

[**Mpmanageropen**](mpmanageropen.md)
</dt> <dt>

[**mpcallback- \_ Daten**](mpcallback-data.md)
</dt> <dt>

[**mpscan- \_ Daten**](mpscan-data.md)
</dt> <dt>

[**mpscan- \_ Ressourcen**](mpscan-resources.md)
</dt> <dt>

[**mpscan- \_ Typ**](mpscan-type.md)
</dt> </dl>

 

 





