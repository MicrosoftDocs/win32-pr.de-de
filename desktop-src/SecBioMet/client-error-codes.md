---
title: Client Fehler Codes (winbio \_ Err. h)
description: Fehlercodes, die in der winbio \_ Err. h-Header Datei definiert sind.
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
ms.openlocfilehash: 000723612a2f7f9f5575fc767924d4d6c697468a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040912"
---
# <a name="client-error-codes"></a>Client Fehler Codes

Die folgenden Fehlercodes sind in der Header Datei "winbio \_ Err. h" definiert.



| Konstante/Wert                                                                                                                                                                                                                                                                                         | BESCHREIBUNG                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_E_UNSUPPORTED_FACTOR"></span><span id="winbio_e_unsupported_factor"></span><dl> <dt>**Winbio \_ E \_ nicht unterstützter \_ Faktor**</dt> <dt>0x80098001</dt> </dl>                              | Der angegebene biometrische Faktor wird nicht unterstützt.<br/>                                                       |
| <span id="WINBIO_E_INVALID_UNIT"></span><span id="winbio_e_invalid_unit"></span><dl> <dt>**Winbio \_ E \_ ungültige \_ Einheit**</dt> <dt>0x80098002</dt> </dl>                                                | Die ID-Nummer der Einheit entspricht keinem gültigen biometrischen Gerät.<br/>                                    |
| <span id="WINBIO_E_UNKNOWN_ID"></span><span id="winbio_e_unknown_id"></span><dl> <dt>**Winbio \_ E \_ unbekannte \_ ID**</dt> <dt>0x80098003</dt> </dl>                                                      | Das biometrische Beispiel stimmt mit keiner bekannten Identität identisch.<br/>                                                |
| <span id="WINBIO_E_CANCELED"></span><span id="winbio_e_canceled"></span><dl> <dt>**Winbio \_ E \_ abgebrochen**</dt> <dt>0x80098004</dt> </dl>                                                             | Der biometrische Vorgang wurde abgebrochen, bevor er beendet werden konnte.<br/>                                         |
| <span id="WINBIO_E_NO_MATCH"></span><span id="winbio_e_no_match"></span><dl> <dt>**Winbio \_ E \_ keine \_**</dt> Entsprechung <dt>0x80098005</dt> </dl>                                                            | Das biometrische Beispiel entspricht nicht der angegebenen Identität oder dem untergeordneten Faktor.<br/>                              |
| <span id="WINBIO_E_CAPTURE_ABORTED"></span><span id="winbio_e_capture_aborted"></span><dl> <dt>**Winbio \_ E- \_ Erfassung \_ abgebrochen**</dt> <dt>0x80098006</dt> </dl>                                       | Ein biometrisches Beispiel konnte nicht erfasst werden, da der Aufzeichnungs Vorgang abgebrochen wurde.<br/>                    |
| <span id="WINBIO_E_ENROLLMENT_IN_PROGRESS"></span><span id="winbio_e_enrollment_in_progress"></span><dl> <dt>**Winbio \_ E Registrierung \_ \_ in \_**</dt> Bearbeitung <dt>0x80098007</dt> </dl>                 | Eine Registrierungs Transaktion konnte nicht gestartet werden, da bereits eine andere Registrierung ausgeführt wird.<br/>      |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**Winbio \_ E ungültige \_ \_ Erfassung**</dt> <dt>0x80098008</dt> </dl>                                                   | Das erfasste Beispiel kann nicht für weitere biometrische Vorgänge verwendet werden.<br/>                                   |
| <span id="WINBIO_E_INVALID_CONTROL_CODE"></span><span id="winbio_e_invalid_control_code"></span><dl> <dt>**Winbio \_ E \_ ungültiger \_ Steuerungs \_ Code**</dt> <dt>0x80098009</dt> </dl>                       | Der angegebene Einheits Steuerungs Code wird von der biometrischen Einheit nicht unterstützt.<br/>                                   |
| <span id="WINBIO_E_DATA_COLLECTION_IN_PROGRESS"></span><span id="winbio_e_data_collection_in_progress"></span><dl> <dt>**Winbio \_ E \_ Daten \_ Sammlung \_ in \_**</dt> Bearbeitung <dt>0x8009800b</dt> </dl> | Ein ausstehender Daten Sammlungs Vorgang wird bereits ausgeführt.<br/>                                            |
| <span id="WINBIO_E_UNSUPPORTED_DATA_FORMAT"></span><span id="winbio_e_unsupported_data_format"></span><dl> <dt>**Winbio \_ E \_ nicht unterstütztes \_ Daten \_ Format**</dt> <dt>0x8009800c</dt> </dl>              | Das angeforderte Datenformat wird vom biometrischen Sensor Treiber nicht unterstützt.<br/>                                |
| <span id="WINBIO_E_UNSUPPORTED_DATA_TYPE"></span><span id="winbio_e_unsupported_data_type"></span><dl> <dt>**Winbio \_ E \_ nicht unterstützter \_ \_ Datentyp**</dt> <dt>0x8009800d</dt> </dl>                    | Der biometrische Sensor-Treiber unterstützt den angeforderten Datentyp nicht.<br/>                                  |
| <span id="WINBIO_E_UNSUPPORTED_PURPOSE"></span><span id="winbio_e_unsupported_purpose"></span><dl> <dt>**Winbio \_ E \_ nicht unterstützter \_ Zweck**</dt> <dt>0x8009800e</dt> </dl>                           | Der biometrische Sensor-Treiber unterstützt den angeforderten Daten Zweck nicht.<br/>                               |
| <span id="WINBIO_E_INVALID_DEVICE_STATE"></span><span id="winbio_e_invalid_device_state"></span><dl> <dt>**Winbio \_ E \_ ungültiger \_ Geräte \_ Status**</dt> <dt>0x8009800f</dt> </dl>                       | Die biometrische Einheit weist nicht den richtigen Status auf, um den angegebenen Vorgang auszuführen.<br/>                      |
| <span id="WINBIO_E_DEVICE_BUSY"></span><span id="winbio_e_device_busy"></span><dl> <dt>**Winbio \_ E- \_ Gerät \_ ausgelastet**</dt> <dt>0x80098010</dt> </dl>                                                   | Der Vorgang konnte nicht ausgeführt werden, da das Sensorgerät ausgelastet war.<br/>                               |
| <span id="WINBIO_E_DATABASE_CANT_CREATE"></span><span id="winbio_e_database_cant_create"></span><dl> <dt>**Winbio \_ E \_ Database \_ cant \_ Create**</dt> <dt>0x80098011</dt> </dl>                       | Der Speicher Adapter war nicht in der Lage, eine neue Datenbank zu erstellen.<br/>                                             |
| <span id="WINBIO_E_DATABASE_CANT_OPEN"></span><span id="winbio_e_database_cant_open"></span><dl> <dt>**Winbio \_ E \_ Database \_ cant \_ Open**</dt> <dt>0x80098012</dt> </dl>                             | Der Speicher Adapter konnte eine vorhandene Datenbank nicht öffnen.<br/>                                         |
| <span id="WINBIO_E_DATABASE_CANT_CLOSE"></span><span id="winbio_e_database_cant_close"></span><dl> <dt>**Winbio \_ E \_ Database \_ 't \_ Close**</dt> <dt>0x80098013</dt> </dl>                          | Der Speicher Adapter war nicht in der Lage, eine Datenbank zu schließen.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_ERASE"></span><span id="winbio_e_database_cant_erase"></span><dl> <dt>**Winbio \_ E \_ Datenbank \_ \_**</dt> konnte <dt>0x80098014</dt> nicht löschen </dl>                          | Der Speicher Adapter konnte eine Datenbank nicht löschen.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_FIND"></span><span id="winbio_e_database_cant_find"></span><dl> <dt>**Winbio \_ E \_ Database \_ nicht \_ gefunden**</dt> <dt>0x80098015</dt> </dl>                             | Der Speicher Adapter konnte keine Datenbank finden.<br/>                                                   |
| <span id="WINBIO_E_DATABASE_ALREADY_EXISTS"></span><span id="winbio_e_database_already_exists"></span><dl> <dt>**Winbio \_ E \_ Database ist \_ bereits \_ vorhanden**</dt> <dt>0x80098016</dt> </dl>              | Der Speicher Adapter konnte eine Datenbank nicht erstellen, da die angegebene Datenbank bereits vorhanden ist.<br/>   |
| <span id="WINBIO_E_DATABASE_FULL"></span><span id="winbio_e_database_full"></span><dl> <dt>**Winbio \_ E \_ Database \_ Full**</dt> <dt>0x80098018</dt> </dl>                                             | Der Speicher Adapter konnte der Datenbank keinen Datensatz hinzufügen, da die Datenbank voll ist.<br/>         |
| <span id="WINBIO_E_DATABASE_LOCKED"></span><span id="winbio_e_database_locked"></span><dl> <dt>**Winbio \_ E \_ Datenbank \_ gesperrt**</dt> <dt>0x80098019</dt> </dl>                                       | Die Datenbank ist gesperrt, und auf ihren Inhalt kann nicht zugegriffen werden.<br/>                                              |
| <span id="WINBIO_E_DATABASE_CORRUPTED"></span><span id="winbio_e_database_corrupted"></span><dl> <dt>**Winbio \_ E \_ Datenbank \_ beschädigt**</dt> <dt>0x8009801a</dt> </dl>                              | Der Inhalt der Datenbank ist beschädigt und kann nicht aufgerufen werden.<br/>                               |
| <span id="WINBIO_E_DATABASE_NO_SUCH_RECORD"></span><span id="winbio_e_database_no_such_record"></span><dl> <dt>**Winbio \_ E \_ Database \_ No \_ this \_ Record**</dt> <dt>0x8009801b</dt> </dl>             | Es wurden keine Datensätze gelöscht, weil die angegebene Identität und der unter Faktor nicht in der Datenbank vorhanden sind.<br/> |
| <span id="WINBIO_E_DUPLICATE_ENROLLMENT"></span><span id="winbio_e_duplicate_enrollment"></span><dl> <dt>**Winbio \_ E \_ doppelte \_**</dt> Registrierung <dt>0x8009801c</dt> </dl>                        | Die angegebene Identität und der untergeordnete Faktor sind bereits in der Datenbank registriert.<br/>                            |
| <span id="WINBIO_E_DATABASE_READ_ERROR"></span><span id="winbio_e_database_read_error"></span><dl> <dt>**Winbio \_ E \_ Datenbank- \_ Lese \_ Fehler**</dt> <dt>0x8009801d</dt> </dl>                          | Fehler beim Lesen aus der Datenbank.<br/>                                              |
| <span id="WINBIO_E_DATABASE_WRITE_ERROR"></span><span id="winbio_e_database_write_error"></span><dl> <dt>**Winbio \_ E \_ Daten Bank \_ Schreib \_ Fehler**</dt> <dt>0x8009801e</dt> </dl>                       | Fehler beim Schreiben in die Datenbank.<br/>                                               |
| <span id="WINBIO_E_DATABASE_NO_RESULTS"></span><span id="winbio_e_database_no_results"></span><dl> <dt>**Winbio \_ E \_ Database \_ No \_ results**</dt> <dt>0x8009801f</dt> </dl>                          | Keine Datensätze in der Datenbank stimmen mit der Abfrage überein.<br/>                                                          |
| <span id="WINBIO_E_DATABASE_NO_MORE_RECORDS"></span><span id="winbio_e_database_no_more_records"></span><dl> <dt>**Winbio \_ E \_ Database \_ keine \_ weiteren \_ Datensätze**</dt> <dt>0x80098020</dt> </dl>          | Alle Datensätze aus der letzten Datenbankabfrage wurden abgerufen.<br/>                                   |
| <span id="WINBIO_E_DATABASE_EOF"></span><span id="winbio_e_database_eof"></span><dl> <dt>**Winbio \_ E \_ Database \_ EOF**</dt> <dt>0x80098021</dt> </dl>                                                | Ein Daten Bank Vorgang hat unerwartet das Ende der Datei gefunden.<br/>                                     |
| <span id="WINBIO_E_DATABASE_BAD_INDEX_VECTOR"></span><span id="winbio_e_database_bad_index_vector"></span><dl> <dt>**Winbio \_ E \_ Datenbank ungültiger \_ \_ Index \_ Vektor**</dt> <dt>0x80098022</dt> </dl>       | Fehler beim Daten Bank Vorgang aufgrund eines falsch formatierten Index Vektors.<br/>                                           |
| <span id="WINBIO_E_INCORRECT_BSP"></span><span id="winbio_e_incorrect_bsp"></span><dl> <dt>**Winbio \_ E \_ falsche \_ BSP**</dt> <dt>0x80098024</dt> </dl>                                             | Die biometrische Einheit gehört nicht zum angegebenen Dienstanbieter.<br/>                                  |
| <span id="WINBIO_E_INCORRECT_SENSOR_POOL"></span><span id="winbio_e_incorrect_sensor_pool"></span><dl> <dt>**Winbio \_ E \_ falscher \_ Sensor \_ Pool**</dt> <dt>0x80098025</dt> </dl>                    | Die biometrische Einheit gehört nicht zum angegebenen Sensor Pool.<br/>                                       |
| <span id="WINBIO_E_NO_CAPTURE_DATA"></span><span id="winbio_e_no_capture_data"></span><dl> <dt>**Winbio \_ E \_ No \_ Capture \_ Data**</dt> <dt>0x80098026</dt> </dl>                                      | Der Sensor Adapter Erfassungs Puffer ist leer.<br/>                                                            |
| <span id="WINBIO_E_INVALID_SENSOR_MODE"></span><span id="winbio_e_invalid_sensor_mode"></span><dl> <dt>**Winbio \_ E \_ ungültiger \_ Sensor \_ Modus**</dt> <dt>0x80098027</dt> </dl>                          | Der Sensor Adapter unterstützt den in der Konfiguration angegebenen Sensor Modus nicht.<br/>                    |
| <span id="WINBIO_E_LOCK_VIOLATION"></span><span id="winbio_e_lock_violation"></span><dl> <dt>**Winbio \_ E \_ Sperr \_ Verletzung**</dt> <dt>0x8009802a</dt> </dl>                                          | Der angeforderte Vorgang kann aufgrund eines Sperr Konflikts nicht ausgeführt werden.<br/>                                 |
| <span id="WINBIO_E_DUPLICATE_TEMPLATE"></span><span id="winbio_e_duplicate_template"></span><dl> <dt>**Winbio \_ E \_ doppelte \_ Vorlage**</dt> <dt>0x8009802b</dt> </dl>                              | Die Daten in einer biometrischen Vorlage entsprechen denen einer anderen Vorlage, die bereits in der Datenbank vorhanden ist.<br/>             |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**Winbio \_ E \_ ungültiger \_ Vorgang**</dt> <dt>0x8009802c</dt> </dl>                                 | Der angeforderte Vorgang ist für den aktuellen Status der Sitzung oder der biometrischen Einheit ungültig.<br/>       |
| <span id="WINBIO_E_SESSION_BUSY"></span><span id="winbio_e_session_busy"></span><dl> <dt>**Winbio \_ E \_ Sitzung \_ beschäftigt**</dt> <dt>0x8009802d</dt> </dl>                                                | Die Sitzung kann keinen neuen Vorgang starten, da bereits ein anderer Vorgang ausgeführt wird.<br/>             |
| <span id="WINBIO_E_CRED_PROV_DISABLED"></span><span id="winbio_e_cred_prov_disabled"></span><dl> <dt>**Winbio \_ E \_ Kred \_ Prov \_**</dt> hat <dt>0x80098030</dt> deaktiviert </dl>                             | Die System Richtlinien Einstellungen haben den Anbieter für biometrische Anmelde Informationen deaktiviert.<br/>                                |
| <span id="WINBIO_E_CRED_PROV_NO_CREDENTIAL"></span><span id="winbio_e_cred_prov_no_credential"></span><dl> <dt>**Winbio \_ E \_ Kred \_ Prov \_ No \_ Credential**</dt> <dt>0x80098031</dt> </dl>             | Die angeforderten Anmelde Informationen wurden nicht gefunden.<br/>                                                                |
| <span id="WINBIO_E_DISABLED"></span><span id="winbio_e_disabled"></span><dl> <dt>**Winbio \_ E \_ deaktiviert**</dt> <dt>0x80098032</dt> </dl>                                                             | Die System Richtlinien Einstellungen haben den biometrischen Dienst deaktiviert.<br/>                                            |
| <span id="WINBIO_E_CONFIGURATION_FAILURE"></span><span id="winbio_e_configuration_failure"></span><dl> <dt>**Winbio \_ E- \_ Konfigurations \_ Fehler**</dt> <dt>0x80098033</dt> </dl>                     | Die biometrische Einheit konnte nicht konfiguriert werden.<br/>                                                            |
| <span id="WINBIO_E_SENSOR_UNAVAILABLE"></span><span id="winbio_e_sensor_unavailable"></span><dl> <dt>**Winbio \_ E- \_ Sensor nicht \_ verfügbar**</dt> <dt>0x80098034</dt> </dl>                              | Ein privater Pool kann nicht erstellt werden, da eine oder mehrere biometrische Einheiten nicht verfügbar sind.<br/>                |
| <span id="WINBIO_E_SAS_ENABLED"></span><span id="winbio_e_sas_enabled"></span><dl> <dt>**Winbio \_ E \_ SAS \_ aktiviert**</dt> <dt>0x80098035</dt> </dl>                                                   | Für die Anmeldung ist eine Sicherheits Sequenz (Strg + Alt + Delete) erforderlich.<br/>                                   |
| <span id="WINBIO_E_DEVICE_FAILURE"></span><span id="winbio_e_device_failure"></span><dl> <dt>**Winbio \_ E- \_ Geräte \_ Fehler**</dt> <dt>0x80098036</dt> </dl>                                          | Ein biometrischer Sensor ist fehlgeschlagen.<br/>                                                                         |
| <span id="WINBIO_E_FAST_USER_SWITCH_DISABLED"></span><span id="winbio_e_fast_user_switch_disabled"></span><dl> <dt>**Winbio \_ E \_ fast \_ User \_ Switch \_ deaktiviert**</dt> <dt>0x80098037</dt> </dl>       | >schnelle Benutzerumschaltung ist deaktiviert.<br/>                                                                   |
| <span id="WINBIO_E_NOT_ACTIVE_CONSOLE"></span><span id="winbio_e_not_active_console"></span><dl> <dt>**Winbio \_ E \_ nicht \_ aktiv- \_ Konsole**</dt> <dt>0x80098038</dt> </dl>                             | Der System Sensor Pool kann nicht über Terminal Server-Client Sitzungen geöffnet werden.<br/>                          |
| <span id="WINBIO_E_EVENT_MONITOR_ACTIVE"></span><span id="winbio_e_event_monitor_active"></span><dl> <dt>**Winbio \_ E- \_ Ereignis \_ Überwachung \_ aktiv**</dt> <dt>0x80098039</dt> </dl>                      | Der angegebenen Sitzung ist bereits ein aktiver Ereignis Monitor zugeordnet.<br/>                        |
| <span id="WINBIO_E_INVALID_PROPERTY_TYPE"></span><span id="winbio_e_invalid_property_type"></span><dl> <dt>**Winbio \_ E \_ ungültiger \_ \_ Eigenschaftentyp**</dt> <dt>0x8009803a</dt> </dl>                    | Der angegebene Wert ist kein gültiger Eigenschaftentyp.<br/>                                                      |
| <span id="WINBIO_E_INVALID_PROPERTY_ID"></span><span id="winbio_e_invalid_property_id"></span><dl> <dt>**Winbio \_ E \_ ungültige \_ Eigenschaften- \_ ID**</dt> <dt>0x8009803b</dt> </dl>                          | Der angegebene Wert ist keine gültige eigen schafts-ID.<br/>                                                        |
| <span id="WINBIO_E_UNSUPPORTED_PROPERTY"></span><span id="winbio_e_unsupported_property"></span><dl> <dt>**Winbio \_ E \_ nicht unterstützte \_ Eigenschaft**</dt> <dt>0x8009803c</dt> </dl>                        | Die biometrische Einheit unterstützt die angegebene Eigenschaft nicht.<br/>                                            |
| <span id="WINBIO_E_ADAPTER_INTEGRITY_FAILURE"></span><span id="winbio_e_adapter_integrity_failure"></span><dl> <dt>**Winbio \_ E- \_ Adapter- \_ Integritäts \_ Fehler**</dt> <dt>0x8009803d</dt> </dl>        | Der Adapter hat seine Integritätsprüfung nicht bestanden.<br/>                                                          |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**Winbio \_ \_Weitere \_ Daten**</dt> <dt>0x00090001</dt> </dl>                                                         | Ein weiteres Beispiel ist für die aktuelle Registrierungs Vorlage erforderlich.<br/>                                          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Winbio \_ Err. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Konstanten](client-application-constants.md)
</dt> </dl>

 

 





