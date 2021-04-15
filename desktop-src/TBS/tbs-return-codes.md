---
title: TSB-Rückgabe Codes (TSB. h)
description: TSB verwendet die folgenden Codes, um das Ergebnis eines Funktions Aufrufes anzuzeigen.
ms.assetid: a3888263-aa00-4b31-b51d-c6d448c1edb7
topic_type:
- apiref
api_name:
- TBS_SUCCESS
- TBS_E_INTERNAL_ERROR
- TBS_E_BAD_PARAMETER
- TBS_E_INVALID_OUTPUT_POINTER
- TBS_E_INVALID_CONTEXT
- TBS_E_INSUFFICIENT_BUFFER
- TBS_E_IOERROR
- TBS_E_INVALID_CONTEXT_PARAM
- TBS_E_SERVICE_NOT_RUNNING
- TBS_E_TOO_MANY_TBS_CONTEXTS
- TBS_E_TOO_MANY_RESOURCES
- TBS_E_SERVICE_START_PENDING
- TBS_E_PPI_NOT_SUPPORTED
- TBS_E_COMMAND_CANCELED
- TBS_E_BUFFER_TOO_LARGE
- TBS_E_TPM_NOT_FOUND
- TBS_E_SERVICE_DISABLED
- TBS_E_NO_EVENT_LOG
- TBS_E_ACCESS_DENIED
- TBS_E_PROVISIONING_NOT_ALLOWED
- TBS_E_PPI_FUNCTION_UNSUPPORTED
- TBS_E_OWNERAUTH_NOT_FOUND
- TBS_E_PROVISIONING_INCOMPLETE
api_location:
- Tbs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0271c323e4ea300f45817aa59d4f5f9779f9981
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391933"
---
# <a name="tbs-return-codes"></a>TSB-Rückgabe Codes

TSB verwendet die folgenden Codes, um das Ergebnis eines Funktions Aufrufes anzuzeigen.



| Konstante/Wert                                                                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_SUCCESS"></span><span id="tbs_success"></span><dl> <dt>**TSB \_ Erfolg**</dt> <dt>0 (0x0)</dt> </dl>                                                                             | Die Funktion wurde erfolgreich ausgeführt.<br/>                                                                                                                                                                                                         |
| <span id="TBS_E_INTERNAL_ERROR"></span><span id="tbs_e_internal_error"></span><dl> <dt>**TSB \_ E \_ interner \_ Fehler**</dt> <dt>2150121473 (0x80284001)</dt> </dl>                                | Interner Softwarefehler.<br/>                                                                                                                                                                                            |
| <span id="TBS_E_BAD_PARAMETER"></span><span id="tbs_e_bad_parameter"></span><dl> <dt>**TSB \_ E ungültiger \_ \_ Parameter**</dt> <dt>2150121474 (0x80284002)</dt> </dl>                                   | Mindestens ein Parameterwert ist ungültig.<br/>                                                                                                                                                                                     |
| <span id="TBS_E_INVALID_OUTPUT_POINTER"></span><span id="tbs_e_invalid_output_pointer"></span><dl> <dt>**TSB \_ E \_ ungültiger \_ Ausgabe \_ Zeiger**</dt> <dt>2150121475 (0x80284003)</dt> </dl>       | Ein angegebener Ausgabe Zeiger ist falsch.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_INVALID_CONTEXT"></span><span id="tbs_e_invalid_context"></span><dl> <dt>**TSB \_ E \_ ungültiger \_ Kontext**</dt> <dt>2150121476 (0x80284004)</dt> </dl>                             | Das angegebene Kontext Handle verweist nicht auf einen gültigen Kontext.<br/>                                                                                                                                                                 |
| <span id="TBS_E_INSUFFICIENT_BUFFER"></span><span id="tbs_e_insufficient_buffer"></span><dl> <dt>**TSB \_ E \_ nicht genügend \_ Puffer**</dt> <dt>2150121477 (0x80284005)</dt> </dl>                 | Der angegebene Ausgabepuffer ist zu klein.<br/>                                                                                                                                                                                       |
| <span id="TBS_E_IOERROR"></span><span id="tbs_e_ioerror"></span><dl> <dt>**TSB \_ E \_ IOError**</dt> <dt>2150121478 (0x80284006)</dt> </dl>                                                      | Fehler bei der Kommunikation mit dem TPM.<br/>                                                                                                                                                                             |
| <span id="TBS_E_INVALID_CONTEXT_PARAM"></span><span id="tbs_e_invalid_context_param"></span><dl> <dt>**TSB \_ E \_ ungültiger \_ Kontext \_**</dt> Parameter <dt>2150121479 (0x80284007)</dt> </dl>          | Bei dem Versuch, einen TSB-Kontext zu erstellen, wurde ein Ungültiger Kontext Parameter übergeben.<br/>                                                                                                                                       |
| <span id="TBS_E_SERVICE_NOT_RUNNING"></span><span id="tbs_e_service_not_running"></span><dl> <dt>**TSB \_ E- \_ Dienst wird \_ nicht \_ ausgeführt**</dt> <dt>2150121480 (0x80284008)</dt> </dl>                | Der TSB-Dienst wird nicht ausgeführt und konnte nicht gestartet werden.<br/>                                                                                                                                                                        |
| <span id="TBS_E_TOO_MANY_TBS_CONTEXTS"></span><span id="tbs_e_too_many_tbs_contexts"></span><dl> <dt>**TSB \_ E \_ zu \_ viele \_ TSB- \_ Kontexte**</dt> <dt>2150121481 (0x80284009)</dt> </dl>         | Ein neuer Kontext konnte nicht erstellt werden, da zu viele offene Kontexte vorhanden sind.<br/>                                                                                                                                                    |
| <span id="TBS_E_TOO_MANY_RESOURCES"></span><span id="tbs_e_too_many_resources"></span><dl> <dt>**TSB \_ E \_ zu \_ viele \_ Ressourcen**</dt> <dt>2150121482 (0x8028400a)</dt> </dl>                   | Eine neue virtuelle Ressource konnte nicht erstellt werden, da zu viele geöffnete virtuelle Ressourcen vorhanden sind.<br/>                                                                                                                                  |
| <span id="TBS_E_SERVICE_START_PENDING"></span><span id="tbs_e_service_start_pending"></span><dl> <dt>**TSB \_ E- \_ Dienst \_ Start steht \_ aus**</dt> <dt>2150121483 (0x8028400b)</dt> </dl>          | Der TSB-Dienst wurde gestartet, aber noch nicht ausgeführt.<br/>                                                                                                                                                                        |
| <span id="TBS_E_PPI_NOT_SUPPORTED"></span><span id="tbs_e_ppi_not_supported"></span><dl> <dt>**TSB \_ E- \_ ppi \_ wird 2150121484 nicht \_ unterstützt**</dt> <dt>(0x8028400c)</dt> </dl>                      | Die physische Anwesenheits Schnittstelle wird nicht unterstützt.<br/>                                                                                                                                                                               |
| <span id="TBS_E_COMMAND_CANCELED"></span><span id="tbs_e_command_canceled"></span><dl> <dt>**TSB \_ E- \_ Befehl \_ abgebrochen**</dt> <dt>2150121485 (0x8028400d)</dt> </dl>                          | Der Befehl wurde abgebrochen.<br/>                                                                                                                                                                                                       |
| <span id="TBS_E_BUFFER_TOO_LARGE"></span><span id="tbs_e_buffer_too_large"></span><dl> <dt>**TSB \_ E- \_ Puffer \_ zu \_ groß**</dt> <dt>2150121486 (0x8028400e)</dt> </dl>                         | Der Eingabe-oder Ausgabepuffer ist zu groß.<br/>                                                                                                                                                                                        |
| <span id="TBS_E_TPM_NOT_FOUND"></span><span id="tbs_e_tpm_not_found"></span><dl> <dt>**TSB \_ E \_ TPM \_ nicht \_ gefunden**</dt> <dt>2150121487 (0x8028400f)</dt> </dl>                                  | Ein kompatibles Trusted Platform Module (TPM)-Sicherheitsgerät kann auf diesem Computer nicht gefunden werden.<br/>                                                                                                                                    |
| <span id="TBS_E_SERVICE_DISABLED"></span><span id="tbs_e_service_disabled"></span><dl> <dt>**TSB \_ E- \_ Dienst \_ deaktiviert**</dt> <dt>2150121488 (0x80284010)</dt> </dl>                          | Der TSB-Dienst wurde deaktiviert.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_NO_EVENT_LOG"></span><span id="tbs_e_no_event_log"></span><dl> <dt>**TSB \_ E \_ No \_ Event \_ Log**</dt> <dt>2150121489 (0x80284011)</dt> </dl>                                     | Das TSB-Ereignisprotokoll ist nicht verfügbar.<br/>                                                                                                                                                                                             |
| <span id="TBS_E_ACCESS_DENIED"></span><span id="tbs_e_access_denied"></span><dl> <dt>**TSB \_ E \_ Access \_ verweigert**</dt> <dt>2150121490 (0x80284012)</dt> </dl>                                   | Der Aufrufer verfügt nicht über die erforderlichen Rechte zum Ausführen des angeforderten Vorgangs.<br/>                                                                                                                                             |
| <span id="TBS_E_PROVISIONING_NOT_ALLOWED"></span><span id="tbs_e_provisioning_not_allowed"></span><dl> <dt>**TSB \_ E-Bereitstellung \_ \_ nicht \_ zulässig**</dt> <dt>2150121491 (0x80284013)</dt> </dl> | Die TPM-Bereitstellungs Aktion ist durch die angegebenen Flags nicht zulässig.<br/>                                                                                                                                                              |
| <span id="TBS_E_PPI_FUNCTION_UNSUPPORTED"></span><span id="tbs_e_ppi_function_unsupported"></span><dl> <dt>**TSB \_ E \_ ppi- \_ Funktion \_ nicht unterstützt**</dt> <dt>2150121492 (0x80284014)</dt> </dl> | Die physische Anwesenheits Schnittstelle dieser Firmware unterstützt die angeforderte Methode nicht.<br/>                                                                                                                                         |
| <span id="TBS_E_OWNERAUTH_NOT_FOUND"></span><span id="tbs_e_ownerauth_not_found"></span><dl> <dt>**TSB \_ E Besitzer Authentifizierung \_ \_ nicht \_ gefunden**</dt> <dt>2150121493 (0x80284015)</dt> </dl>                | Der angeforderte TPM-Besitzer Wert wurde nicht gefunden.<br/>                                                                                                                                                                                |
| <span id="TBS_E_PROVISIONING_INCOMPLETE"></span><span id="tbs_e_provisioning_incomplete"></span><dl> <dt>**TSB \_ E- \_ Provisioning \_ unvollständig**</dt> <dt>2150121493 (0x80284015)</dt> </dl>     | Die TPM-Bereitstellung wurde nicht beendet. Weitere Informationen zum Abschließen der Bereitstellung erhalten Sie, wenn Sie die WMI-Methode [**Win32 \_ TPM**](/windows/desktop/SecProv/win32-tpm) für die Bereitstellung von TPM ("Bereitstellen") und die zurückgegebenen Informationen überprüfen.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>TSB. h</dt> </dl> |



 

