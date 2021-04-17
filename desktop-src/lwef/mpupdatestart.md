---
title: Mpupdatestart-Funktion (mpclient. h)
description: Startet einen Signatur Aktualisierungs Vorgang.
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- Mpupdatestart-Funktion Legacy Funktionen der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpUpdateStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39867525529339c6b354ae771b070589ca52acfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478735"
---
# <a name="mpupdatestart-function"></a>Mpupdatestart-Funktion

Startet einen Signatur Aktualisierungs Vorgang.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpUpdateStart(
  _In_     MPHANDLE         hMpHandle,
  _In_     DWORD            dwUpdateOptions,
  _In_opt_ PMPCALLBACK_INFO pCallbackInfo,
  _Out_    PMPHANDLE        phUpdateHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hmphandle* \[ in\]
</dt> <dd>

Typ: **mphandle**

Handle für die Malware Protection Manager-Schnittstelle. Dieses Handle wird von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegeben.

</dd> <dt>

*dwupdateoptions* \[ in\]
</dt> <dd>

Typ: **DWORD**

Gibt die Option für den Signatur Aktualisierungs Vorgang an. Es kann sich um einen der folgenden Werte handeln:



| Wert                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <dt>**MPUpdate- \_ Option " \_ None"**</dt> </dl>                | Eine bestimmte Option wird nicht angefordert.<br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <dt>**MPUpdate- \_ Option \_ Async**</dt> </dl>             | Der Aktualisierungs Vorgang wird asynchron ausgeführt, wobei " **mpupdatestart** " unmittelbar nach der erfolgreichen Initiierung des Signatur Updates zurückgegeben wird. (Standardmäßig ist der Aktualisierungs Vorgang synchron, d. h. **mpupdatestart** wird erst zurückgegeben, wenn das Signatur Update abgeschlossen ist.)<br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <dt>**Status der MPUpdate- \_ Option \_**</dt> </dl>    | Der Aufrufer ist daran interessiert, Statusinformationen zur Signatur Aktualisierung über einen Rückruf zu empfangen.<br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <dt>**MPUpdate- \_ Option \_ http**</dt> </dl>                | Das Signatur Update wird ausgeführt, indem das vollständige Signatur Paket von der Microsoft Security Portal-Website heruntergeladen wird. Dies kann als Fall Back Option verwendet werden, wenn der Client über Microsoft Update ein Problem mit der Signatur herunterladen hat.<br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <dt>**MPUpdate- \_ Option \_ UNC**</dt> </dl>                   | Führt eine Signatur Aktualisierung mithilfe von direktem Download von UNC-Freigaben durch.<br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <dt>**MPUpdate- \_ Option \_ verwaltet**</dt> </dl>       | Führt eine Signatur Aktualisierung mithilfe des verwalteten Dienstanbieter-WSUS aus.<br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <dt>**MPUpdate- \_ Option \_ nicht verwaltet**</dt> </dl> | Führt ein Signatur Update mit dem nicht verwalteten Dienst mu/Wu aus.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

*pcallbackinfo* \[ in, optional\]
</dt> <dd>

Typ: **pmpcallback- \_ Informationen**

Ein Zeiger auf die Rückruf Informationen, die verwendet werden, um den Client mit Änderungen des Signatur Update Zustands (z. b. Start und Complete) und Fortschrittsinformationen zu Feeds. Die [**mpcallback- \_ Daten**](mpcallback-data.md) , die in der Rückruffunktion zurückgegeben werden, melden den tatsächlichen Update Status und die Status bezogenen Informationen. Im folgenden finden Sie eine Liste möglicher Rückrufe:



| Wert                                                                                                                                                                                                                                | Bedeutung                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <dt>**mpnotify \_ sigupdate \_ Start**</dt> </dl>                                      | Der Aktualisierungs Vorgang wurde gestartet.<br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <dt>**mpnotify \_ sigupdate ist fertiggestellt. \_**</dt> </dl>                             | Der Aktualisierungs Vorgang wurde abgeschlossen.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <dt>**mpnotify \_ sigupdate- \_ Suche \_ starten**</dt> </dl>                | Suche nach Updates gestartet.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <dt>**mpnotify \_ sigupdate- \_ Suche ist \_ beendet**</dt> </dl>       | Suche nach Updates wurde abgeschlossen. Zusätzliche Informationen sind über die [**mpsigupdate- \_ Daten**](mpsigupdate-data.md) Struktur verfügbar.<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <dt>**mpnotify \_ sigupdate \_ Download \_ starten**</dt> </dl>          | Der Download für das Update wurde gestartet.<br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <dt>**mpnotify \_ sigupdate- \_ Download \_ Fortschritt**</dt> </dl> | Statusinformationen herunterladen. Zusätzliche Informationen sind über die [**mpsigupdate- \_ Daten**](mpsigupdate-data.md) Struktur verfügbar.<br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <dt>**mpnotify \_ sigupdate- \_ Download ist \_ fertiggestellt.**</dt> </dl> | Der Download für das Update ist beendet. Zusätzliche Informationen sind über die [**mpsigupdate- \_ Daten**](mpsigupdate-data.md) Struktur verfügbar.<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <dt>**mpnotify \_ sigupdate \_ Installation \_ starten**</dt> </dl>             | Die Installation des Updates wurde gestartet.<br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <dt>**mpnotify \_ sigupdate- \_ Installations \_ Fortschritt**</dt> </dl>    | Informationen zum Installationsfortschritt. Zusätzliche Informationen sind über die [**mpsigupdate- \_ Daten**](mpsigupdate-data.md) Struktur verfügbar.<br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <dt>**mpnotify \_ sigupdate- \_ Installation ist \_ fertiggestellt.**</dt> </dl>    | Die Installation des Updates ist abgeschlossen. Zusätzliche Informationen sind über die [**mpsigupdate- \_ Daten**](mpsigupdate-data.md) Struktur verfügbar.<br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <dt>**mpnotify \_ sigupdate- \_ Anforderung \_ verarbeitet**</dt> </dl> | Der antischadsoftwaredienst hat eine Signatur Aktualisierungs Anforderung verarbeitet. Fehler oder Erfolg wird von *HRESULT* in [**mpcallback- \_ Daten**](mpcallback-data.md)angegeben.<br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <dt>**mpnotify- \_ sigupdate- \_ Neustart \_ erforderlich**</dt> </dl>       | Zum Abschluss des Aktualisierungs Vorgangs ist ein Neustart erforderlich. Fehler oder Erfolg wird von *HRESULT* in [**mpcallback- \_ Daten**](mpcallback-data.md)angegeben.<br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**Interner mpnotify- \_ \_ Fehler**</dt> </dl>                                   | Generischer Fehler beim Signatur Aktualisierungs Vorgang. Das *HRESULT* in [**mpcallback- \_ Daten**](mpcallback-data.md) enthält den spezifischen Fehlercode.<br/>    |



 

</dd> <dt>

*phupdatehandle* \[ vorgenommen\]
</dt> <dd>

Typ: **pmphandle**

Zurück gegebenes Aktualisierungs handle, das den derzeit initiierten Signatur Aktualisierungs Vorgang identifiziert. Dieses Handle kann in nachfolgenden Funktionsaufrufen verwendet werden, z. b. um den Signatur Aktualisierungs Vorgang zu steuern. Das Handle muss mit der [**mplenker close**](mphandleclose.md) -Funktion geschlossen werden.

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

[**mpsigupdate- \_ Daten**](mpsigupdate-data.md)
</dt> </dl>

 

 





