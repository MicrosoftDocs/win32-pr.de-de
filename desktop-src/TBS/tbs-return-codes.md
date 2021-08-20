---
title: TBS-Rückgabecodes (Tbs.h)
description: TBS verwendet die folgenden Codes, um das Ergebnis eines Funktionsaufrufs anzugeben.
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
ms.openlocfilehash: e3b05e711ec99c78fbb2d5129999f0cc7f8247706b8737aef0c155f826b10141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954281"
---
# <a name="tbs-return-codes"></a>TBS-Rückgabecodes

TBS verwendet die folgenden Codes, um das Ergebnis eines Funktionsaufrufs anzugeben.



| Konstante/Wert                                                                                                                                                                                                                                                                                   | Beschreibung                                                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_SUCCESS"></span><span id="tbs_success"></span><dl> <dt>**TBS \_ SUCCESS**</dt> <dt>0 (0x0)</dt> </dl>                                                                             | Die Funktion wurde erfolgreich ausgeführt.<br/>                                                                                                                                                                                                         |
| <span id="TBS_E_INTERNAL_ERROR"></span><span id="tbs_e_internal_error"></span><dl> <dt>**TBS \_ E \_ INTERNAL \_ ERROR**</dt> <dt>2150121473 (0x80284001)</dt> </dl>                                | Interner Softwarefehler.<br/>                                                                                                                                                                                            |
| <span id="TBS_E_BAD_PARAMETER"></span><span id="tbs_e_bad_parameter"></span><dl> <dt>**TBS \_ E \_ BAD \_ PARAMETER**</dt> <dt>2150121474 (0x80284002)</dt> </dl>                                   | Mindestens ein Parameterwert ist ungültig.<br/>                                                                                                                                                                                     |
| <span id="TBS_E_INVALID_OUTPUT_POINTER"></span><span id="tbs_e_invalid_output_pointer"></span><dl> <dt>**TBS \_ E \_ INVALID \_ OUTPUT \_ POINTER**</dt> <dt>2150121475 (0x80284003)</dt> </dl>       | Ein angegebener Ausgabezeiger ist schlecht.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_INVALID_CONTEXT"></span><span id="tbs_e_invalid_context"></span><dl> <dt>**TBS \_ E \_ INVALID \_ CONTEXT**</dt> <dt>2150121476 (0x80284004)</dt> </dl>                             | Das angegebene Kontexthand handle bezieht sich nicht auf einen gültigen Kontext.<br/>                                                                                                                                                                 |
| <span id="TBS_E_INSUFFICIENT_BUFFER"></span><span id="tbs_e_insufficient_buffer"></span><dl> <dt>**TBS \_ E \_ INSUFFICIENT \_ BUFFER**</dt> <dt>2150121477 (0x80284005)</dt> </dl>                 | Der angegebene Ausgabepuffer ist zu klein.<br/>                                                                                                                                                                                       |
| <span id="TBS_E_IOERROR"></span><span id="tbs_e_ioerror"></span><dl> <dt>**TBS \_ E \_ IOERROR**</dt> <dt>2150121478 (0x80284006)</dt> </dl>                                                      | Fehler bei der Kommunikation mit dem TPM.<br/>                                                                                                                                                                             |
| <span id="TBS_E_INVALID_CONTEXT_PARAM"></span><span id="tbs_e_invalid_context_param"></span><dl> <dt>**TBS \_ E \_ INVALID \_ CONTEXT \_ PARAM**</dt> <dt>2150121479 (0x80284007)</dt> </dl>          | Beim Versuch, einen TBS-Kontext zu erstellen, wurde ein ungültiger Kontextparameter übergeben.<br/>                                                                                                                                       |
| <span id="TBS_E_SERVICE_NOT_RUNNING"></span><span id="tbs_e_service_not_running"></span><dl> <dt>**TBS \_ E \_ SERVICE NOT RUNNING \_ \_ 2150121480**</dt> <dt>(0x80284008)</dt> </dl>                | Der TBS-Dienst wird nicht ausgeführt und konnte nicht gestartet werden.<br/>                                                                                                                                                                        |
| <span id="TBS_E_TOO_MANY_TBS_CONTEXTS"></span><span id="tbs_e_too_many_tbs_contexts"></span><dl> <dt>**TBS \_ E \_ TOO \_ MANY \_ TBS \_ CONTEXTS**</dt> <dt>2150121481 (0x80284009)</dt> </dl>         | Ein neuer Kontext konnte nicht erstellt werden, da zu viele offene Kontexte sind.<br/>                                                                                                                                                    |
| <span id="TBS_E_TOO_MANY_RESOURCES"></span><span id="tbs_e_too_many_resources"></span><dl> <dt>**TBS \_ E \_ TOO \_ MANY \_ RESOURCES**</dt> <dt>2150121482 (0x8028400A)</dt> </dl>                   | Eine neue virtuelle Ressource konnte nicht erstellt werden, da zu viele virtuelle Ressourcen geöffnet sind.<br/>                                                                                                                                  |
| <span id="TBS_E_SERVICE_START_PENDING"></span><span id="tbs_e_service_start_pending"></span><dl> <dt>**TBS \_ E \_ SERVICE \_ START \_ PENDING**</dt> <dt>2150121483 (0x8028400B)</dt> </dl>          | Der TBS-Dienst wurde gestartet, wird aber noch nicht ausgeführt.<br/>                                                                                                                                                                        |
| <span id="TBS_E_PPI_NOT_SUPPORTED"></span><span id="tbs_e_ppi_not_supported"></span><dl> <dt>**TBS \_ E \_ EPI WIRD NICHT \_ \_ 2150121484**</dt> <dt>(0x8028400C)</dt> </dl>                      | Die Physische Anwesenheitsschnittstelle wird nicht unterstützt.<br/>                                                                                                                                                                               |
| <span id="TBS_E_COMMAND_CANCELED"></span><span id="tbs_e_command_canceled"></span><dl> <dt>**TBS \_ E \_ COMMAND \_ CANCELED**</dt> <dt>2150121485 (0x8028400D)</dt> </dl>                          | Der Befehl wurde abgebrochen.<br/>                                                                                                                                                                                                       |
| <span id="TBS_E_BUFFER_TOO_LARGE"></span><span id="tbs_e_buffer_too_large"></span><dl> <dt>**TBS \_ E \_ BUFFER \_ TOO \_ LARGE**</dt> <dt>2150121486 (0x8028400E)</dt> </dl>                         | Der Eingabe- oder Ausgabepuffer ist zu groß.<br/>                                                                                                                                                                                        |
| <span id="TBS_E_TPM_NOT_FOUND"></span><span id="tbs_e_tpm_not_found"></span><dl> <dt>**TBS \_ E \_ TPM NOT FOUND \_ \_ 2150121487**</dt> <dt>(0x8028400F)</dt> </dl>                                  | Ein kompatibles Trusted Platform Module -Sicherheitsgerät (TPM) wurde auf diesem Computer nicht gefunden.<br/>                                                                                                                                    |
| <span id="TBS_E_SERVICE_DISABLED"></span><span id="tbs_e_service_disabled"></span><dl> <dt>**TBS \_ E \_ SERVICE \_ DISABLED**</dt> <dt>2150121488 (0x80284010)</dt> </dl>                          | Der TBS-Dienst wurde deaktiviert.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_NO_EVENT_LOG"></span><span id="tbs_e_no_event_log"></span><dl> <dt>**TBS \_ E \_ NO \_ EVENT \_ LOG**</dt> <dt>2150121489 (0x80284011)</dt> </dl>                                     | Das TBS-Ereignisprotokoll ist nicht verfügbar.<br/>                                                                                                                                                                                             |
| <span id="TBS_E_ACCESS_DENIED"></span><span id="tbs_e_access_denied"></span><dl> <dt>**TBS \_ E \_ ACCESS \_ DENIED**</dt> <dt>2150121490 (0x80284012)</dt> </dl>                                   | Der Aufrufer verfügt nicht über die entsprechenden Rechte zum Ausführen des angeforderten Vorgangs.<br/>                                                                                                                                             |
| <span id="TBS_E_PROVISIONING_NOT_ALLOWED"></span><span id="tbs_e_provisioning_not_allowed"></span><dl> <dt>**TBS \_ E \_ PROVISIONING \_ NOT ALLOWED \_ 2150121491**</dt> <dt>(0x80284013)</dt> </dl> | Die TPM-Bereitstellungsaktion ist von den angegebenen Flags nicht zulässig.<br/>                                                                                                                                                              |
| <span id="TBS_E_PPI_FUNCTION_UNSUPPORTED"></span><span id="tbs_e_ppi_function_unsupported"></span><dl> <dt>**TBS \_ E \_ PPI \_ FUNCTION \_ UNSUPPORTED**</dt> <dt>2150121492 (0x80284014)</dt> </dl> | Die Physical Presence Interface dieser Firmware unterstützt die angeforderte Methode nicht.<br/>                                                                                                                                         |
| <span id="TBS_E_OWNERAUTH_NOT_FOUND"></span><span id="tbs_e_ownerauth_not_found"></span><dl> <dt>**TBS \_ E \_ OWNERAUTH \_ NOT FOUND \_ 2150121493**</dt> <dt>(0x80284015)</dt> </dl>                | Der angeforderte TPM OwnerAuth-Wert wurde nicht gefunden.<br/>                                                                                                                                                                                |
| <span id="TBS_E_PROVISIONING_INCOMPLETE"></span><span id="tbs_e_provisioning_incomplete"></span><dl> <dt>**TBS \_ E \_ PROVISIONING \_ INCOMPLETE**</dt> <dt>2150121493 (0x80284015)</dt> </dl>     | Die TPM-Bereitstellung wurde nicht abgeschlossen. Um weitere Informationen zum Abschließen der Bereitstellung zu erhalten, rufen Sie die [**Win32 \_ Tpm-WMI-Methode**](/windows/desktop/SecProv/win32-tpm) für die Bereitstellung des TPM ("Provision") auf, und überprüfen Sie die zurückgegebenen Informationen.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Tbs.h</dt> </dl> |



 

