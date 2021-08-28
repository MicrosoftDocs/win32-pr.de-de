---
title: Clientfehlercodes (Winbio \_ err.h)
description: Fehlercodes, die in der Winbio \_ err.h-Headerdatei definiert sind.
ms.assetid: fc1565d2-43f1-45cd-ab84-4e557cf78107
topic_type:
- apiref
api_name:
- WINBIO_E_UNSUPPORTED_FACTOR
- WINBIO_E_INVALID_UNIT
- WINBIO_E_UNKNOWN_ID
- WINBIO_E_CANCELED
- WINBIO_E_NO_MATCH
- WINBIO_E_CAPTURE_ABORTED
- WINBIO_E_ENROLLMENT_IN_PROGRESS
- WINBIO_E_BAD_CAPTURE
- WINBIO_E_INVALID_CONTROL_CODE
- WINBIO_E_DATA_COLLECTION_IN_PROGRESS
- WINBIO_E_UNSUPPORTED_DATA_FORMAT
- WINBIO_E_UNSUPPORTED_DATA_TYPE
- WINBIO_E_UNSUPPORTED_PURPOSE
- WINBIO_E_INVALID_DEVICE_STATE
- WINBIO_E_DEVICE_BUSY
- WINBIO_E_DATABASE_CANT_CREATE
- WINBIO_E_DATABASE_CANT_OPEN
- WINBIO_E_DATABASE_CANT_CLOSE
- WINBIO_E_DATABASE_CANT_ERASE
- WINBIO_E_DATABASE_CANT_FIND
- WINBIO_E_DATABASE_ALREADY_EXISTS
- WINBIO_E_DATABASE_FULL
- WINBIO_E_DATABASE_LOCKED
- WINBIO_E_DATABASE_CORRUPTED
- WINBIO_E_DATABASE_NO_SUCH_RECORD
- WINBIO_E_DUPLICATE_ENROLLMENT
- WINBIO_E_DATABASE_READ_ERROR
- WINBIO_E_DATABASE_WRITE_ERROR
- WINBIO_E_DATABASE_NO_RESULTS
- WINBIO_E_DATABASE_NO_MORE_RECORDS
- WINBIO_E_DATABASE_EOF
- WINBIO_E_DATABASE_BAD_INDEX_VECTOR
- WINBIO_E_INCORRECT_BSP
- WINBIO_E_INCORRECT_SENSOR_POOL
- WINBIO_E_NO_CAPTURE_DATA
- WINBIO_E_INVALID_SENSOR_MODE
- WINBIO_E_LOCK_VIOLATION
- WINBIO_E_DUPLICATE_TEMPLATE
- WINBIO_E_INVALID_OPERATION
- WINBIO_E_SESSION_BUSY
- WINBIO_E_CRED_PROV_DISABLED
- WINBIO_E_CRED_PROV_NO_CREDENTIAL
- WINBIO_E_DISABLED
- WINBIO_E_CONFIGURATION_FAILURE
- WINBIO_E_SENSOR_UNAVAILABLE
- WINBIO_E_SAS_ENABLED
- WINBIO_E_DEVICE_FAILURE
- WINBIO_E_FAST_USER_SWITCH_DISABLED
- WINBIO_E_NOT_ACTIVE_CONSOLE
- WINBIO_E_EVENT_MONITOR_ACTIVE
- WINBIO_E_INVALID_PROPERTY_TYPE
- WINBIO_E_INVALID_PROPERTY_ID
- WINBIO_E_UNSUPPORTED_PROPERTY
- WINBIO_E_ADAPTER_INTEGRITY_FAILURE
- WINBIO_I_MORE_DATA
api_location:
- Winbio_err.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcb8450b85eaa6c49b66a3a86789c126cc04b9a661a7e4c5074784f8cba6bf72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993840"
---
# <a name="client-error-codes"></a>Clientfehlercodes

Die folgenden Fehlercodes werden in der Headerdatei Winbio \_ err.h definiert.



| Konstante/Wert                                                                                                                                                                                                                                                                                         | Beschreibung                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_E_UNSUPPORTED_FACTOR"></span><span id="winbio_e_unsupported_factor"></span><dl> <dt>**WINBIO \_ E \_ NICHT \_ UNTERSTÜTZTER FAKTOR**</dt> <dt>0X80098001</dt> </dl>                              | Der angegebene biometrische Faktor wird nicht unterstützt.<br/>                                                       |
| <span id="WINBIO_E_INVALID_UNIT"></span><span id="winbio_e_invalid_unit"></span><dl> <dt>**WINBIO \_ E \_ INVALID \_ UNIT**</dt> <dt>0x80098002</dt> </dl>                                                | Die Nummer der Geräte-ID entspricht keinem gültigen biometrischen Gerät.<br/>                                    |
| <span id="WINBIO_E_UNKNOWN_ID"></span><span id="winbio_e_unknown_id"></span><dl> <dt>**WINBIO \_ E \_ UNKNOWN \_ ID**</dt> <dt>0x80098003</dt> </dl>                                                      | Das biometrische Beispiel passt nicht zu einer bekannten Identität.<br/>                                                |
| <span id="WINBIO_E_CANCELED"></span><span id="winbio_e_canceled"></span><dl> <dt>**WINBIO \_ E \_ CANCELED**</dt> <dt>0x80098004</dt> </dl>                                                             | Der biometrische Vorgang wurde abgebrochen, bevor er abgeschlossen werden konnte.<br/>                                         |
| <span id="WINBIO_E_NO_MATCH"></span><span id="winbio_e_no_match"></span><dl> <dt>**WINBIO \_ E \_ NO \_ MATCH**</dt> <dt>0x80098005</dt> </dl>                                                            | Die biometrische Stichprobe ist nicht mit der angegebenen Identität oder dem angegebenen Unterfaktor übereinstimmen.<br/>                              |
| <span id="WINBIO_E_CAPTURE_ABORTED"></span><span id="winbio_e_capture_aborted"></span><dl> <dt>**WINBIO \_ E \_ CAPTURE \_ ABORTED**</dt> <dt>0x80098006</dt> </dl>                                       | Eine biometrische Stichprobe konnte nicht erfasst werden, da der Erfassungsvorgang abgebrochen wurde.<br/>                    |
| <span id="WINBIO_E_ENROLLMENT_IN_PROGRESS"></span><span id="winbio_e_enrollment_in_progress"></span><dl> <dt>**WINBIO \_ \_ \_ E-REGISTRIERUNG \_ WIRD**</dt> <dt>0X80098007</dt> </dl>                 | Eine Registrierungstransaktion konnte nicht gestartet werden, da bereits eine andere Registrierung ausgeführt wird.<br/>      |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**WINBIO \_ E \_ BAD \_ CAPTURE**</dt> <dt>0x80098008</dt> </dl>                                                   | Die erfasste Stichprobe kann nicht für weitere biometrische Vorgänge verwendet werden.<br/>                                   |
| <span id="WINBIO_E_INVALID_CONTROL_CODE"></span><span id="winbio_e_invalid_control_code"></span><dl> <dt>**WINBIO \_ E \_ \_ UNGÜLTIGER \_ STEUERCODE**</dt> <dt>0X80098009</dt> </dl>                       | Die biometrische Einheit unterstützt den angegebenen Komponentenkontrollcode nicht.<br/>                                   |
| <span id="WINBIO_E_DATA_COLLECTION_IN_PROGRESS"></span><span id="winbio_e_data_collection_in_progress"></span><dl> <dt>**WINBIO \_ E \_ DATA COLLECTION IN PROGRESS \_ \_ \_ 0X8009800B**</dt> <dt></dt> </dl> | Ein ausstehender Datensammlungsvorgang wird bereits durchgeführt.<br/>                                            |
| <span id="WINBIO_E_UNSUPPORTED_DATA_FORMAT"></span><span id="winbio_e_unsupported_data_format"></span><dl> <dt>**WINBIO \_ E \_ NICHT UNTERSTÜTZTE \_ \_ DATENFORMAT-0X8009800C**</dt> <dt></dt> </dl>              | Der Biometrische Sensortreiber unterstützt das angeforderte Datenformat nicht.<br/>                                |
| <span id="WINBIO_E_UNSUPPORTED_DATA_TYPE"></span><span id="winbio_e_unsupported_data_type"></span><dl> <dt>**WINBIO \_ E \_ NICHT \_ UNTERSTÜTZTER \_ DATENTYP**</dt> <dt>0X8009800D</dt> </dl>                    | Der biometrische Sensortreiber unterstützt den angeforderten Datentyp nicht.<br/>                                  |
| <span id="WINBIO_E_UNSUPPORTED_PURPOSE"></span><span id="winbio_e_unsupported_purpose"></span><dl> <dt>**WINBIO \_ E \_ NICHT \_ UNTERSTÜTZTER**</dt> <dt>0X8009800E</dt> </dl>                           | Der biometrische Sensortreiber unterstützt den angeforderten Datenzweck nicht.<br/>                               |
| <span id="WINBIO_E_INVALID_DEVICE_STATE"></span><span id="winbio_e_invalid_device_state"></span><dl> <dt>**WINBIO \_ E \_ INVALID DEVICE STATE \_ \_ 0X8009800F**</dt> <dt></dt> </dl>                       | Die biometrische Einheit befindet sich nicht im richtigen Zustand, um den angegebenen Vorgang durchzuführen.<br/>                      |
| <span id="WINBIO_E_DEVICE_BUSY"></span><span id="winbio_e_device_busy"></span><dl> <dt>**WINBIO \_ E \_ GERÄT \_ AUSGELASTET**</dt> <dt>0X80098010</dt> </dl>                                                   | Der Vorgang konnte nicht ausgeführt werden, da das Sensorgerät ausgelastet war.<br/>                               |
| <span id="WINBIO_E_DATABASE_CANT_CREATE"></span><span id="winbio_e_database_cant_create"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CANT CREATE \_ 0X80098011**</dt> <dt></dt> </dl>                       | Der Speicheradapter konnte keine neue Datenbank erstellen.<br/>                                             |
| <span id="WINBIO_E_DATABASE_CANT_OPEN"></span><span id="winbio_e_database_cant_open"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CANT OPEN \_ 0X80098012**</dt> <dt></dt> </dl>                             | Der Speicheradapter konnte keine vorhandene Datenbank öffnen.<br/>                                         |
| <span id="WINBIO_E_DATABASE_CANT_CLOSE"></span><span id="winbio_e_database_cant_close"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CANT CLOSE \_ 0X80098013**</dt> <dt></dt> </dl>                          | Der Speicheradapter konnte eine Datenbank nicht schließen.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_ERASE"></span><span id="winbio_e_database_cant_erase"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CANT ERASE \_ 0X80098014**</dt> <dt></dt> </dl>                          | Der Speicheradapter konnte eine Datenbank nicht löschen.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_FIND"></span><span id="winbio_e_database_cant_find"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CANT \_ FIND**</dt> <dt>0X80098015</dt> </dl>                             | Der Speicheradapter konnte keine Datenbank finden.<br/>                                                   |
| <span id="WINBIO_E_DATABASE_ALREADY_EXISTS"></span><span id="winbio_e_database_already_exists"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ ALREADY \_ EXISTS**</dt> <dt>0X80098016</dt> </dl>              | Der Speicheradapter konnte keine Datenbank erstellen, da die angegebene Datenbank bereits vorhanden ist.<br/>   |
| <span id="WINBIO_E_DATABASE_FULL"></span><span id="winbio_e_database_full"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ FULL**</dt> <dt>0x80098018</dt> </dl>                                             | Der Speicheradapter konnte der Datenbank keinen Datensatz hinzufügen, da die Datenbank voll ist.<br/>         |
| <span id="WINBIO_E_DATABASE_LOCKED"></span><span id="winbio_e_database_locked"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ LOCKED**</dt> <dt>0x80098019</dt> </dl>                                       | Die Datenbank ist gesperrt, und auf deren Inhalt kann nicht zugegriffen werden.<br/>                                              |
| <span id="WINBIO_E_DATABASE_CORRUPTED"></span><span id="winbio_e_database_corrupted"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CORRUPTED**</dt> <dt>0x8009801A</dt> </dl>                              | Der Inhalt der Datenbank ist beschädigt und kann nicht mehr zugegriffen werden.<br/>                               |
| <span id="WINBIO_E_DATABASE_NO_SUCH_RECORD"></span><span id="winbio_e_database_no_such_record"></span><dl> <dt>**WINBIO \_ E \_ DATABASE NO SUCH \_ \_ \_ RECORD**</dt> <dt>0X8009801B</dt> </dl>             | Es wurden keine Datensätze gelöscht, da die angegebene Identität und der untere Faktor nicht in der Datenbank vorhanden sind.<br/> |
| <span id="WINBIO_E_DUPLICATE_ENROLLMENT"></span><span id="winbio_e_duplicate_enrollment"></span><dl> <dt>**WINBIO \_ E \_ DOPPELTE \_ REGISTRIERUNG**</dt> <dt>0X8009801C</dt> </dl>                        | Die angegebene Identität und der untere Faktor sind bereits in der Datenbank registriert.<br/>                            |
| <span id="WINBIO_E_DATABASE_READ_ERROR"></span><span id="winbio_e_database_read_error"></span><dl> <dt>**WINBIO \_ E \_ DATABASE READ ERROR \_ \_ 0X8009801D**</dt> <dt></dt> </dl>                          | Fehler beim Lesen aus der Datenbank.<br/>                                              |
| <span id="WINBIO_E_DATABASE_WRITE_ERROR"></span><span id="winbio_e_database_write_error"></span><dl> <dt>**WINBIO \_ E \_ DATABASE WRITE ERROR \_ \_ 0X8009801E**</dt> <dt></dt> </dl>                       | Fehler beim Schreiben in die Datenbank.<br/>                                               |
| <span id="WINBIO_E_DATABASE_NO_RESULTS"></span><span id="winbio_e_database_no_results"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ NO \_ RESULTS**</dt> <dt>0x8009801F</dt> </dl>                          | Es wurden keine Datensätze in der Datenbank mit der Abfrage übereinstimmen.<br/>                                                          |
| <span id="WINBIO_E_DATABASE_NO_MORE_RECORDS"></span><span id="winbio_e_database_no_more_records"></span><dl> <dt>**WINBIO \_ E \_ DATABASE NO MORE \_ \_ \_ RECORDS**</dt> <dt>0x80098020</dt> </dl>          | Alle Datensätze aus der letzten Datenbankabfrage wurden abgerufen.<br/>                                   |
| <span id="WINBIO_E_DATABASE_EOF"></span><span id="winbio_e_database_eof"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ EOF**</dt> <dt>0x80098021</dt> </dl>                                                | Ein Datenbankvorgang hat unerwartet das Ende der Datei gefunden.<br/>                                     |
| <span id="WINBIO_E_DATABASE_BAD_INDEX_VECTOR"></span><span id="winbio_e_database_bad_index_vector"></span><dl> <dt>**WINBIO \_ E \_ DATABASE BAD INDEX VECTOR \_ \_ \_ 0X80098022**</dt> <dt></dt> </dl>       | Ein Datenbankvorgang ist aufgrund eines falsch formatierten Indexvektors fehlgeschlagen.<br/>                                           |
| <span id="WINBIO_E_INCORRECT_BSP"></span><span id="winbio_e_incorrect_bsp"></span><dl> <dt>**WINBIO \_ E \_ FALSCHE \_ BSP-0x80098024**</dt> <dt></dt> </dl>                                             | Die biometrische Einheit gehört nicht zum angegebenen Dienstanbieter.<br/>                                  |
| <span id="WINBIO_E_INCORRECT_SENSOR_POOL"></span><span id="winbio_e_incorrect_sensor_pool"></span><dl> <dt>**WINBIO \_ E \_ FALSCHE \_ \_ SENSORPOOL-0X80098025**</dt> <dt></dt> </dl>                    | Die biometrische Einheit gehört nicht zum angegebenen Sensorpool.<br/>                                       |
| <span id="WINBIO_E_NO_CAPTURE_DATA"></span><span id="winbio_e_no_capture_data"></span><dl> <dt>**WINBIO \_ E \_ NO \_ CAPTURE \_ DATA**</dt> <dt>0X80098026</dt> </dl>                                      | Der Erfassungspuffer des Sensoradapters ist leer.<br/>                                                            |
| <span id="WINBIO_E_INVALID_SENSOR_MODE"></span><span id="winbio_e_invalid_sensor_mode"></span><dl> <dt>**WINBIO \_ E \_ \_ UNGÜLTIGER \_ SENSORMODUS**</dt> <dt>0X80098027</dt> </dl>                          | Der Sensoradapter unterstützt den in der Konfiguration angegebenen Sensormodus nicht.<br/>                    |
| <span id="WINBIO_E_LOCK_VIOLATION"></span><span id="winbio_e_lock_violation"></span><dl> <dt>**WINBIO \_ E \_ \_ SPERRVERLETZUNG**</dt> <dt>0X8009802A</dt> </dl>                                          | Der angeforderte Vorgang kann aufgrund eines Sperrkonflikts nicht ausgeführt werden.<br/>                                 |
| <span id="WINBIO_E_DUPLICATE_TEMPLATE"></span><span id="winbio_e_duplicate_template"></span><dl> <dt>**WINBIO \_ E \_ DOPPELTE \_ VORLAGE**</dt> <dt>0X8009802B</dt> </dl>                              | Die Daten in einer biometrischen Vorlage sind mit denen einer anderen Vorlage, die bereits in der Datenbank vorhanden ist, identifizieren.<br/>             |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**WINBIO \_ E \_ INVALID \_ OPERATION**</dt> <dt>0x8009802C</dt> </dl>                                 | Der angeforderte Vorgang ist für den aktuellen Status der Sitzung oder der biometrischen Einheit ungültig.<br/>       |
| <span id="WINBIO_E_SESSION_BUSY"></span><span id="winbio_e_session_busy"></span><dl> <dt>**WINBIO \_ E \_ SESSION \_ BUSY**</dt> <dt>0x8009802D</dt> </dl>                                                | Die Sitzung kann keinen neuen Vorgang starten, da bereits ein anderer Vorgang durchgeführt wird.<br/>             |
| <span id="WINBIO_E_CRED_PROV_DISABLED"></span><span id="winbio_e_cred_prov_disabled"></span><dl> <dt>**WINBIO \_ E \_ CRED \_ PROV \_ DISABLED**</dt> <dt>0x80098030</dt> </dl>                             | Systemrichtlinieneinstellungen haben den Anbieter biometrischer Anmeldeinformationen deaktiviert.<br/>                                |
| <span id="WINBIO_E_CRED_PROV_NO_CREDENTIAL"></span><span id="winbio_e_cred_prov_no_credential"></span><dl> <dt>**WINBIO \_ E \_ CRED \_ PROV \_ NO \_ CREDENTIAL**</dt> <dt>0X80098031</dt> </dl>             | Die angeforderten Anmeldeinformationen wurden nicht gefunden.<br/>                                                                |
| <span id="WINBIO_E_DISABLED"></span><span id="winbio_e_disabled"></span><dl> <dt>**WINBIO \_ E \_ DISABLED**</dt> <dt>0x80098032</dt> </dl>                                                             | Systemrichtlinieneinstellungen haben den biometrischen Dienst deaktiviert.<br/>                                            |
| <span id="WINBIO_E_CONFIGURATION_FAILURE"></span><span id="winbio_e_configuration_failure"></span><dl> <dt>**WINBIO \_ \_ \_ E-KONFIGURATIONSFEHLER**</dt> <dt>0X80098033</dt> </dl>                     | Die biometrische Einheit konnte nicht konfiguriert werden.<br/>                                                            |
| <span id="WINBIO_E_SENSOR_UNAVAILABLE"></span><span id="winbio_e_sensor_unavailable"></span><dl> <dt>**WINBIO \_ E \_ SENSOR \_ UNAVAILABLE**</dt> <dt>0x80098034</dt> </dl>                              | Ein privater Pool kann nicht erstellt werden, da mindestens eine biometrische Einheit nicht verfügbar ist.<br/>                |
| <span id="WINBIO_E_SAS_ENABLED"></span><span id="winbio_e_sas_enabled"></span><dl> <dt>**WINBIO \_ E \_ SAS \_ ENABLED**</dt> <dt>0x80098035</dt> </dl>                                                   | Für die Anmeldung ist eine Sichere Aufmerksamkeitssequenz (STRG+ALT-DELETE) erforderlich.<br/>                                   |
| <span id="WINBIO_E_DEVICE_FAILURE"></span><span id="winbio_e_device_failure"></span><dl> <dt>**WINBIO \_ E \_ \_ GERÄTEFEHLER**</dt> <dt>0X80098036</dt> </dl>                                          | Ein biometrischer Sensor ist ausgefallen.<br/>                                                                         |
| <span id="WINBIO_E_FAST_USER_SWITCH_DISABLED"></span><span id="winbio_e_fast_user_switch_disabled"></span><dl> <dt>**WINBIO \_ E \_ FAST \_ \_ BENUTZERSCHALTER \_ DEAKTIVIERT**</dt> <dt>0x80098037</dt> </dl>       | >schnelle Benutzerwechsel ist deaktiviert.<br/>                                                                   |
| <span id="WINBIO_E_NOT_ACTIVE_CONSOLE"></span><span id="winbio_e_not_active_console"></span><dl> <dt>**WINBIO \_ E \_ NOT ACTIVE CONSOLE \_ \_ 0x80098038**</dt> <dt></dt> </dl>                             | Der Systemsensorpool kann nicht über Terminalserver-Clientsitzungen geöffnet werden.<br/>                          |
| <span id="WINBIO_E_EVENT_MONITOR_ACTIVE"></span><span id="winbio_e_event_monitor_active"></span><dl> <dt>**WINBIO \_ E \_ EVENT \_ MONITOR \_ ACTIVE**</dt> <dt>0x80098039</dt> </dl>                      | Der angegebenen Sitzung ist bereits ein aktiver Ereignismonitor zugeordnet.<br/>                        |
| <span id="WINBIO_E_INVALID_PROPERTY_TYPE"></span><span id="winbio_e_invalid_property_type"></span><dl> <dt>**WINBIO \_ E \_ \_ UNGÜLTIGER \_ EIGENSCHAFTENTYP**</dt> <dt>0X8009803A</dt> </dl>                    | Der angegebene Wert ist kein gültiger Eigenschaftentyp.<br/>                                                      |
| <span id="WINBIO_E_INVALID_PROPERTY_ID"></span><span id="winbio_e_invalid_property_id"></span><dl> <dt>**WINBIO \_ E \_ \_ UNGÜLTIGE \_ EIGENSCHAFTEN-ID**</dt> <dt>0x8009803B</dt> </dl>                          | Der angegebene Wert ist keine gültige Eigenschaften-ID.<br/>                                                        |
| <span id="WINBIO_E_UNSUPPORTED_PROPERTY"></span><span id="winbio_e_unsupported_property"></span><dl> <dt>**WINBIO \_ E \_ UNSUPPORTED \_ PROPERTY**</dt> <dt>0x8009803C</dt> </dl>                        | Die biometrische Einheit unterstützt die angegebene Eigenschaft nicht.<br/>                                            |
| <span id="WINBIO_E_ADAPTER_INTEGRITY_FAILURE"></span><span id="winbio_e_adapter_integrity_failure"></span><dl> <dt>**WINBIO \_ FEHLER \_ BEI \_ \_ E-ADAPTERINTEGRITÄT**</dt> <dt>0X8009803D</dt> </dl>        | Die Integritätsprüfung des Adapters wurde nicht bestehen.<br/>                                                          |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_ I \_ MORE \_ DATA**</dt> <dt>0x00090001</dt> </dl>                                                         | Ein weiteres Beispiel ist für die aktuelle Registrierungsvorlage erforderlich.<br/>                                          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Winbio \_ err.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungskonstant](client-application-constants.md)
</dt> </dl>

 

 





