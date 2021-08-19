---
title: MpUpdateStart-Funktion (MpClient.h)
description: Startet einen Signaturaktualisierungsvorgang.
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- Features der MpUpdateStart-Funktion "Legacy Windows Environment"
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
ms.openlocfilehash: a61cda213ecfbb23c9ef366fcce7b5c91e806f26f0f4ebe8b45dc596b63d1b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975890"
---
# <a name="mpupdatestart-function"></a>MpUpdateStart-Funktion

Startet einen Signaturaktualisierungsvorgang.

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

*hMpHandle* \[ In\]
</dt> <dd>

Typ: **MPHANDLE**

Behandeln Sie die Schnittstelle des Schadsoftwareschutz-Managers. Dieses Handle wird von der [**MpManagerOpen-Funktion**](mpmanageropen.md) zurückgegeben.

</dd> <dt>

*dwUpdateOptions* \[ In\]
</dt> <dd>

Typ: **DWORD**

Gibt die Option für den Signaturaktualisierungsvorgang an. Es kann sich um einen der folgenden Werte handeln:



| Wert                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <dt>**MPUPDATE \_ OPTION \_ NONE**</dt> </dl>                | Es wird keine bestimmte Option angefordert.<br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <dt>**MPUPDATE \_ OPTION \_ ASYNC**</dt> </dl>             | Der Aktualisierungsvorgang muss asynchron sein, wobei **MpUpdateStart** unmittelbar nach der erfolgreichen Initiierung des Signaturupdates zurückgegeben wird. (Standardmäßig ist der Updatevorgang synchron, d.h. **MpUpdateStart** gibt erst nach Abschluss des Signaturupdates zurück.)<br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <dt>**STATUS DER \_ MPUPDATE-OPTION \_**</dt> </dl>    | Der Aufrufer ist daran interessiert, Statusinformationen zur Signaturaktualisierung über einen Rückruf zu erhalten.<br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <dt>**MPUPDATE \_ OPTION \_ HTTP**</dt> </dl>                | Das Signaturupdate wird durchgeführt, indem das vollständige Signaturpaket von der Microsoft-Sicherheitsportalwebsite heruntergeladen wird. Dies kann als Fallbackoption verwendet werden, wenn beim Client über Microsoft Update ein Problem beim Herunterladen von Signaturen auftritt.<br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <dt>**MPUPDATE \_ OPTION \_ UNC**</dt> </dl>                   | Führt signaturupdates mithilfe des direkten Downloads von UNC-Freigaben durch.<br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <dt>**MPUPDATE \_ OPTION \_ MANAGED**</dt> </dl>       | Führt signaturupdates mithilfe des verwalteten Diensts WSUS aus.<br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <dt>**\_MPUPDATE-OPTION \_ NICHT VERWALTET**</dt> </dl> | Führt die Signaturaktualisierung mithilfe des nicht verwalteten Diensts MU/WU durch.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

*pCallbackInfo* \[ in, optional\]
</dt> <dd>

Typ: **PMPCALLBACK \_ INFO**

Ein Zeiger auf die Rückrufinformationen, die verwendet werden, um dem Client Aktualisierungsstatusänderungen der Signatur (z. B. Start und Abschluss) und Statusinformationen zu übermitteln. Die in der Rückruffunktion übergebenen [**MPCALLBACK \_ DATA-Daten**](mpcallback-data.md) berichten über den tatsächlichen Updatestatus und statusbezogene Informationen. Im Folgenden sind mögliche Rückrufe aufgeführt:



| Wert                                                                                                                                                                                                                                | Bedeutung                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ START**</dt> </dl>                                      | Der Aktualisierungsvorgang wurde gestartet.<br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ COMPLETE**</dt> </dl>                             | Der Aktualisierungsvorgang wurde abgeschlossen.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ SEARCH \_ START**</dt> </dl>                | Suche nach gestarteten Updates.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ SEARCH \_ COMPLETE**</dt> </dl>       | Suchen Sie nach abgeschlossenen Updates. Weitere Informationen sind über [**die MPSIGUPDATE \_ DATA-Struktur**](mpsigupdate-data.md) verfügbar.<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ DOWNLOAD \_ START**</dt> </dl>          | Laden Sie herunter, um das Update zu starten.<br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <dt>**MPNOTIFY \_ \_ SIGUPDATE-DOWNLOADFORTSCHRITT \_**</dt> </dl> | Herunterladen von Statusinformationen. Weitere Informationen sind über [**die MPSIGUPDATE \_ DATA-Struktur**](mpsigupdate-data.md) verfügbar.<br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ DOWNLOAD \_ ABGESCHLOSSEN**</dt> </dl> | Laden Sie herunter, um das Update abzuschließen. Weitere Informationen sind über [**die MPSIGUPDATE \_ DATA-Struktur**](mpsigupdate-data.md) verfügbar.<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ INSTALL \_ START**</dt> </dl>             | Installation des Updates gestartet.<br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <dt>**MPNOTIFY \_ \_ SIGUPDATE– \_ INSTALLATIONSFORTSCHRITT**</dt> </dl>    | Informationen zum Installationsfortschritt. Weitere Informationen sind über [**die MPSIGUPDATE \_ DATA-Struktur**](mpsigupdate-data.md) verfügbar.<br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ INSTALL \_ COMPLETE**</dt> </dl>    | Installation des Updates abgeschlossen. Weitere Informationen sind über [**die MPSIGUPDATE \_ DATA-Struktur**](mpsigupdate-data.md) verfügbar.<br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <dt>**VERARBEITETE MPNOTIFY \_ \_ SIGUPDATE-ANFORDERUNG \_**</dt> </dl> | Der Antischadsoftwaredienst hat eine Signaturupdateanforderung verarbeitet. Fehler oder Erfolg wird durch *hResult* in [**MPCALLBACK \_ DATA**](mpcallback-data.md)angegeben.<br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ REBOOT \_ ERFORDERLICH**</dt> </dl>       | Erfordert einen Neustart, um den Updatevorgang abzuschließen. Fehler oder Erfolg wird durch *hResult* in [**MPCALLBACK \_ DATA**](mpcallback-data.md)angegeben.<br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**\_INTERNER \_ MPNOTIFY-FEHLER**</dt> </dl>                                   | Beim Signaturaktualisierungsvorgang ist ein generischer Fehler aufgetreten. Das *hResult* in [**MPCALLBACK \_ DATA**](mpcallback-data.md) weist den spezifischen Fehlercode auf.<br/>    |



 

</dd> <dt>

*phUpdateHandle* \[ out\]
</dt> <dd>

Typ: **PMPHANDLE**

Das zurückgegebene Updatehandle identifiziert den derzeit initiierten Signaturaktualisierungsvorgang. Dieses Handle kann in nachfolgenden Funktionsaufrufen verwendet werden, z. B. zum Steuern des Signaturaktualisierungsvorgangs. Das Handle muss mit der [**MpHandleClose-Funktion**](mphandleclose.md) geschlossen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert **S \_ OK.**

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT-Code.** Der Aufrufer kann die [**MpErrorMessageFormat-Funktion**](mperrormessageformat.md) verwenden, um eine generische Beschreibung der Fehlermeldung abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpHandleClose**](mphandleclose.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**\_MPCALLBACK-DATEN**](mpcallback-data.md)
</dt> <dt>

[**\_MPSIGUPDATE-DATEN**](mpsigupdate-data.md)
</dt> </dl>

 

 





