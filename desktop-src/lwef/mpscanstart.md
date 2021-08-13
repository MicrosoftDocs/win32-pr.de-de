---
title: MpScanStart-Funktion (MpClient.h)
description: Startet einen Überprüfungsvorgang.
ms.assetid: 3AF147C8-A41F-4193-AE28-72C1FBD18BA2
keywords:
- MpScanStart-Funktion – Legacy Windows Umgebungsfeatures
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
ms.openlocfilehash: 34d56f6814ecdd13b2db4f698e8cc122d4d15e325bda17d82d56a5796d8590fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450240"
---
# <a name="mpscanstart-function"></a>MpScanStart-Funktion

Startet einen Überprüfungsvorgang.

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

*hMpHandle* \[ In\]
</dt> <dd>

Typ: **MPHANDLE**

Handle für die Benutzeroberfläche des Schadsoftwareschutz-Managers. Dieses Handle wird von der [**MpManagerOpen-Funktion**](mpmanageropen.md) zurückgegeben.

</dd> <dt>

*ScanType* \[ In\]
</dt> <dd>

Typ: **[ **MPSCAN \_ TYPE**](mpscan-type.md)**

Gibt den Typ der Überprüfung an. Dieser Parameter muss einer der Member der [**MPSCAN \_ TYPE-Enueration**](mpscan-type.md) sein.

</dd> <dt>

*dwScanOptions* \[ In\]
</dt> <dd>

Typ: **DWORD**

Gibt verschiedene Optionen für den Überprüfungsvorgang an.



| Wert                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <dt>**\_MPSCAN-OPTION \_ NONE**</dt> </dl>                               | Es wird keine bestimmte Option angefordert.<br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <dt>**\_MPSCAN-OPTION \_ ASYNC**</dt> </dl>                            | Der Scanvorgang soll asynchron sein, wobei **MpScanStart** unmittelbar nach der erfolgreichen Initiierung der Überprüfung zurückgegeben wird. (Standardmäßig ist der Scanvorgang synchron, was bedeutet, **dass MpScanStart** erst nach Abschluss der Überprüfung zurücksucht.)<br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <dt>**FORTSCHRITT DER \_ \_ MPSCAN-OPTION**</dt> </dl>                   | Der Aufrufer ist daran interessiert, Informationen zum Überprüfungsfortschritt über einen Rückruf zu erhalten.<br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <dt>**\_MPSCAN-OPTION \_ LOWPRIORITY**</dt> </dl>          | Führen Sie die Überprüfung mit niedriger Priorität aus. (Standardmäßig wird der Scanvorgang mit normaler Priorität ausgeführt.)<br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <dt>**\_MPSCAN-OPTION \_ "PACKEDEXES"**</dt> </dl>             | Überprüfen Sie gepackte ausführbare Dateien auf mögliche Bedrohungen.<br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <dt>**ARCHIV DER \_ \_ MPSCAN-OPTION**</dt> </dl>                   | Archivinhalte auf mögliche Bedrohungen überprüfen. Archive sind Dateien mit Erweiterungen wie .zip, .cab oder TAR.<br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <dt>**\_MPSCAN-OPTION \_ HEURISTICS**</dt> </dl>             | Aktivieren Sie heuristische Scans. Dadurch wird nach Bedrohungen durchsucht, bei denen der Erkennungstyp auf Heuristik festgelegt ist.<br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <dt>**\_MPSCAN-OPTION \_ REPORTFRIENDLY**</dt> </dl> | Melden von benutzerfreundlichen Elementen in einem Ressourcenscan. Dies ist nur für die interne Verwendung vorgesehen.<br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <dt>**\_MPSCAN-OPTION \_ REPORTUNKNOWN**</dt> </dl>    | Melden unbekannter Elemente in einem Ressourcenscan. Dies ist nur für die interne Verwendung vorgesehen.<br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <dt>**\_MPSCAN-OPTION \_ NOCONSOLIDATE**</dt> </dl>    | Konsolidieren Sie die Überprüfungsergebnisse nicht mit der globalen Bedrohungsansicht. Dies ist nützlich für einen Client (z. B. einen E-Mail-Client), der die Bereinigung der Bereinigungs-UX selbst steuern möchte, anstatt standardmäßige Bereinigungs-UX für Ansoftware zu ermöglichen. Dies ist nur für die interne Verwendung vorgesehen.<br/> |



 

</dd> <dt>

*pScanResources* \[ in, optional\]
</dt> <dd>

Typ: **PMPSCAN \_ RESOURCES**

Ein Zeiger auf die Scanressourceninformationen. Dieser Parameter muss für **eine Schnellprüfung NULL** sein. Dies ist ein optionaler Parameter für eine vollständige Überprüfung. Für einen Ressourcenscan muss dieser Parameter mit mindestens einer Ressourceninformationsstruktur angegeben werden. Um bestimmte Ressourcen zu überprüfen, muss der Aufrufer über die **\_ GENERIC READ-Berechtigung** für die Ressource verfügen. Weitere Informationen [**finden Sie unter MPSCAN \_ RESOURCES**](mpscan-resources.md).

</dd> <dt>

*pCallbackInfo* \[ in, optional\]
</dt> <dd>

Typ: **PMPCALLBACK \_ INFO**

Ein Zeiger auf die Rückrufinformationen, die verwendet werden, um dem Client Überprüfungsstatusänderungen (z. B. Start und Abschluss) und Statusinformationen zu geben. Die in der Rückruffunktion übergebenen [**MPCALLBACK-DATEN \_**](mpcallback-data.md) geben den tatsächlichen Scanzustand und statusbezogene Informationen an. Im Folgenden finden Sie eine Liste möglicher Rückrufe:



| Wert                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ START**</dt> </dl>                            | Der Überprüfungsvorgang wurde gestartet.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ COMPLETE**</dt> </dl>                   | Scanvorgang abgeschlossen. Zusätzliche Informationen sind über die [**MPSCAN \_ DATA-Struktur**](mpscan-data.md) verfügbar.<br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <dt>**\_MPNOTIFY-ÜBERPRÜFUNG \_ ANGEHALTEN**</dt> </dl>                         | Der Scanvorgang wurde angehalten.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <dt>**\_MPNOTIFY-ÜBERPRÜFUNG \_ FORTGESETZT**</dt> </dl>                      | Der Überprüfungsvorgang wurde nach der Pause fortgesetzt.<br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ CANCEL**</dt> </dl>                         | Der Scanvorgang wurde abgebrochen.<br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <dt>**\_MPNOTIFY-ÜBERPRÜFUNGSFORTSCHRITT \_**</dt> </dl>                   | Informationen zum Überprüfungsfortschritt. Zusätzliche Informationen (z. B. Ressourcenstatistiken) sind über die [**MPSCAN \_ DATA-Struktur**](mpscan-data.md) verfügbar.<br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <dt>**\_MPNOTIFY-SCANFEHLER \_**</dt> </dl>                            | Überprüfen sie die Fehlerinformationen für eine bestimmte Ressource. Die spezifischen Ressourceninformationen sind über die [**MPSCAN \_ DATA-Struktur**](mpscan-data.md) verfügbar.<br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ INFECTED**</dt> </dl>                   | Scan hat eine infizierte Ressource gefunden. Beachten Sie, dass dies in den meisten Fällen dazu führt, dass am Ende der Überprüfung eine Bedrohung gemeldet wird. Manchmal wird sie aufgrund von Ausschlüssen möglicherweise nicht als Bedrohung materialisiert. Zusätzliche Informationen zu infizierten Ressourcen sind über die [**MPSCAN \_ DATA-Struktur**](mpscan-data.md) verfügbar.<br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ MEMORYSTART**</dt> </dl>          | Der Schnellscanteil der vollständigen Überprüfung wurde gestartet.<br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ MEMORYCOMPLETE**</dt> </dl> | Der Schnellscanteil der vollständigen Überprüfung wurde abgeschlossen.<br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**INTERNER \_ MPNOTIFY-FEHLER \_**</dt> </dl>          | Beim Scanvorgang ist ein generischer Fehler aufgetreten. Das *hResult* in [**MPCALLBACK \_ DATA**](mpcallback-data.md) enthält den spezifischen Fehlercode.<br/>                                                                                                                                                                   |



 

</dd> <dt>

*phScanHandle* \[ out\]
</dt> <dd>

Typ: **PMPHANDLE**

Zurückgegebenes Scanhand handle, das den derzeit initiierten Scan identifiziert. Dieses Handle kann in nachfolgenden Funktionsaufrufen verwendet werden, z. B. zum Abrufen eines Scanergebnis. Das Handle muss mit der [**MpHandleClose-Funktion geschlossen**](mphandleclose.md) werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert **S \_ OK.**

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT-Code.** Der Aufrufer kann die [**MpErrorMessageFormat-Funktion**](mperrormessageformat.md) verwenden, um eine generische Beschreibung der Fehlermeldung abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpHandleClose**](mphandleclose.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**\_MPCALLBACK-DATEN**](mpcallback-data.md)
</dt> <dt>

[**\_MPSCAN-DATEN**](mpscan-data.md)
</dt> <dt>

[**\_MPSCAN-RESSOURCEN**](mpscan-resources.md)
</dt> <dt>

[**\_MPSCAN-TYP**](mpscan-type.md)
</dt> </dl>

 

 





