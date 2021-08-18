---
title: Sensoranforderungen für sichere Biometrie
description: Sensoranforderungen für sichere Biometrie
ms.assetid: 6D5709E9-7B6B-4D6C-BF85-C6FB5DF5A7EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba76ee3b114f79d3c60adfa252f59cd2b8f98aa135e50faf93cf5ecf7314ad99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911792"
---
# <a name="sensor-requirements-for-secure-biometrics"></a>Sensoranforderungen für sichere Biometrie

Microsoft nutzt Trusted Platform Module (TPM) 2.0, um sicherzustellen, dass software (bis zu und einschließlich Schadsoftware auf Kernelebene) auf geeigneter Hardware keine gültige biometrische Authentifizierung erzeugen kann, wenn die biometrischen Daten des Benutzers zum Zeitpunkt der Authentifizierung nicht bereitgestellt wurden.

Hierzu verwenden wir sitzungsbasierte TPM 2.0-Autorisierungen und den Sensor, der die Featureextraktion und den Abgleich in einer vertrauenswürdigen Ausführungsumgebung vorträgt. Wenn das Windows Biometric Framework zum ersten Mal einen sicheren Sensor erkennt (wie von der Funktion für den sicheren Sensor gemeldet), wird ein Geheimnis bereitgestellt, das vom sicheren biometrischen Sensor und dem TPM gemeinsam genutzt wird. Dieses Geheimnis wird nie wieder für das Betriebssystem verfügbar gemacht und ist für jeden Sensor eindeutig.

Um eine Authentifizierung durchzuführen, öffnet das Windows Biometric Framework eine Sitzung mit dem TPM und erhält eine Nonce. Die Nonce wird im Rahmen eines Secure Match-Vorgangs an den sicheren Sensor übergeben. Der Sensor führt die Übereinstimmung in der vertrauenswürdigen Ausführungsumgebung aus und berechnet bei Erfolg einen HMAC über diese Nonce und die Identität des identifizierten Benutzers.

Dieser HMAC kann vom Windows Biometric Framework verwendet werden, um kryptografische Vorgänge im TPM für den identifizierten Benutzer durchzuführen. Der HMAC ist kurzlebig und läuft nach einigen Sekunden ab.

Bei Verwendung dieses Protokolls sind nach der ersten Bereitstellung keine vertraulichen Daten im Betriebssystem enthalten. Geheimnisse werden vom TPM und vom sicheren Sensor gespeichert, und während der Authentifizierung wird nur der kurzlebige HMAC verfügbar gemacht.

## <a name="secure-sensor-capability"></a>Sichere Sensorfunktion

Die WINBIO CAPABILITY SECURE SENSOR-Funktion muss vom Sensor gemeldet werden, wenn sie die neuen Engine-Adaptermethoden \_ \_ in Version \_ 4.0 der Engine-Adapterschnittstelle unterstützt.

Um zu beanspruchen, dass ein Sensor ein sicherer Sensor ist, muss er die folgenden Anforderungen erfüllen:

-   Die übereinstimmende Engine des Sensors muss vom normalen Betriebssystem isoliert werden (z. B. mithilfe einer vertrauenswürdigen Ausführungsumgebung).
-   Der Sensor muss die sichere Eingabe von Stichproben für die isolierte Abgleichs-Engine unterstützen. Der Inhalt der Beispiele darf nie für das normale Betriebssystem verfügbar gemacht werden.
-   Die Abgleichs-Engine muss die Freigabe sicherer Anmeldeinformationen unterstützen, indem die unten beschriebenen neuen v4-Methoden implementieren.
-   Der Sensor muss die Erkennung von Präsentationsangriffen unterstützen.

Der WINBIO \_ CAPABILITY \_ SECURE \_ SENSOR-Wert ist in der [**WINBIO \_ CAPABILITIES-Struktur**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) enthalten. Hier ist ein Beispiel für die Definition.


```
#define WINBIO_CAPABILITY_SECURE_SENSOR     ((WINBIO_CAPABILITIES)0x00000100)
```



## <a name="error-codes"></a>Fehlercodes


```C++
//
// MessageId: WINBIO_E_INVALID_KEY_IDENTIFIER
//
// MessageText:
//
// The key identifier is invalid.
//
#define WINBIO_E_INVALID_KEY_IDENTIFIER ((HRESULT)0x80098052L)

//
// MessageId: WINBIO_E_KEY_CREATION_FAILED
//
// MessageText:
//
// The key cannot be created.
//
#define WINBIO_E_KEY_CREATION_FAILED ((HRESULT)0x80098053L)

// 
// MessageId: WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL 
//
// MessageText: 
// 
// The key identifier buffer is too small. 
// 
#define WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL ((HRESULT)0x80098054L)
```



## <a name="engine-adapter-interface-v-40"></a>Engine-Adapterschnittstelle v 4.0

Die Version der Engine-Adapterschnittstelle wurde auf 4.0 erhöht. Die zusätzlichen Funktionen in der neuen Schnittstelle ermöglichen dem Sensor die Teilnahme an TPM 2.0. Sie lauten wie folgt:

-   [**EngineAdapterCreateKey**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn)
-   [**EngineAdapterIdentifyFeatureSetSecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn)


```
// 

// Additional methods available in V4.0 and later 

// 


typedef HRESULT 

(WINAPI *PIBIO_ENGINE_CREATE_KEY_FN)( 

    _Inout_ PWINBIO_PIPELINE Pipeline, 

    _In_reads_(KeySize) const UCHAR* Key, 

    _In_ SIZE_T KeySize, 

    _Out_writes_bytes_to_(KeyIdentifierSize, *ResultSize) PUCHAR KeyIdentifier, 

    _In_ SIZE_T KeyIdentifierSize, 

    _Out_ PSIZE_T ResultSize 

    ); 


typedef HRESULT 

(WINAPI *PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN)( 

    _Inout_ PWINBIO_PIPELINE Pipeline, 

    _In_reads_(NonceSize) const UCHAR* Nonce, 

    _In_ SIZE_T NonceSize, 

    _In_reads_(KeyIdentifierSize) const UCHAR* KeyIdentifier, 

    _In_ SIZE_T KeyIdentifierSize, 

    _Out_ PWINBIO_IDENTITY Identity, 

    _Out_ PWINBIO_BIOMETRIC_SUBTYPE SubFactor, 

 _Out_ PWINBIO_REJECT_DETAIL RejectDetail, 

    _Outptr_result_bytebuffer_(*AuthorizationSize) PUCHAR *Authorization, 

    _Out_ PSIZE_T AuthorizationSize 

    ); 


#define WINBIO_ENGINE_INTERFACE_VERSION_4   WINBIO_MAKE_INTERFACE_VERSION(4,0) 


typedef struct _WINBIO_ENGINE_INTERFACE { 

    WINBIO_ADAPTER_INTERFACE_VERSION            Version; 

    WINBIO_ADAPTER_TYPE                         Type; 

    SIZE_T                                      Size; 

    GUID                                        AdapterId; 


    PIBIO_ENGINE_ATTACH_FN                      Attach; 

    PIBIO_ENGINE_DETACH_FN                      Detach; 


    PIBIO_ENGINE_CLEAR_CONTEXT_FN               ClearContext; 


    PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN      QueryPreferredFormat; 

    PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN     QueryIndexVectorSize; 

    PIBIO_ENGINE_QUERY_HASH_ALGORITHMS_FN       QueryHashAlgorithms; 

    PIBIO_ENGINE_SET_HASH_ALGORITHM_FN          SetHashAlgorithm; 


    PIBIO_ENGINE_QUERY_SAMPLE_HINT_FN           QuerySampleHint; 


    PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN          AcceptSampleData;       // PROCESSES CURRENT BUFFER FROM PIPELINE AND GENERATES A FEATURE SET IN THE PIPELINE 

    PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN          ExportEngineData;       // EXPORTS FEATURE SET OR TEMPLATE 


    PIBIO_ENGINE_VERIFY_FEATURE_SET_FN          VerifyFeatureSet; 

    PIBIO_ENGINE_IDENTIFY_FEATURE_SET_FN        IdentifyFeatureSet; 


    PIBIO_ENGINE_CREATE_ENROLLMENT_FN           CreateEnrollment;       // ATTACHES AN EMPTY ENROLLMENT TEMPLATE TO THE PIPELINE 

    PIBIO_ENGINE_UPDATE_ENROLLMENT_FN           UpdateEnrollment;       // CONVERTS CURRENT PIPELINE FEATURE SET INTO SOMETHING THAT CAN BE ADDED TO A TEMPLATE 

    PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN       GetEnrollmentStatus;    // QUERIES TEMPLATE ATTACHED TO THE PIPELINE TO SEE IF IT IS READY TO COMMIT 

    PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN         GetEnrollmentHash; 

    PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN         CheckForDuplicate;      // DETERMINES WHETHER TEMPLATE IS ALREADY ENROLLED 

    PIBIO_ENGINE_COMMIT_ENROLLMENT_FN           CommitEnrollment; 

    PIBIO_ENGINE_DISCARD_ENROLLMENT_FN          DiscardEnrollment; 


    PIBIO_ENGINE_CONTROL_UNIT_FN                ControlUnit; 

    PIBIO_ENGINE_CONTROL_UNIT_PRIVILEGED_FN     ControlUnitPrivileged; 


#if (NTDDI_VERSION >= NTDDI_WIN8) 

    // 

    // V2.0 methods begin here... 

    // 

    PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN         NotifyPowerChange; 

    PIBIO_ENGINE_RESERVED_1_FN                  Reserved_1; 

#endif 


#if (NTDDI_VERSION >= NTDDI_WINTHRESHOLD) 

    // 

    // V3.0 methods begin here... 

    // 

    PIBIO_ENGINE_PIPELINE_INIT_FN                       PipelineInit; 

    PIBIO_ENGINE_PIPELINE_CLEANUP_FN                    PipelineCleanup; 

    PIBIO_ENGINE_ACTIVATE_FN                            Activate; 

    PIBIO_ENGINE_DEACTIVATE_FN                          Deactivate; 

    PIBIO_ENGINE_QUERY_EXTENDED_INFO_FN                 QueryExtendedInfo; 

    PIBIO_ENGINE_IDENTIFY_ALL_FN                        IdentifyAll; 

    PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN             SetEnrollmentSelector; 

    PIBIO_ENGINE_SET_ENROLLMENT_PARAMETERS_FN           SetEnrollmentParameters; 

    PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN    QueryExtendedEnrollmentStatus; 

    PIBIO_ENGINE_REFRESH_CACHE_FN                       RefreshCache;  

    PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN           SelectCalibrationFormat; 

    PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN              QueryCalibrationData; 

    PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN                  SetAccountPolicy; 

#endif 


#if (NTDDI_VERSION >= NTDDI_WIN10_RS1) 

    // 

    // V4.0 methods begin here... 

    // 

    PIBIO_ENGINE_CREATE_KEY_FN                     CreateKey; 

    PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN    IdentifyFeatureSetSecure; 

#endif 


} WINBIO_ENGINE_INTERFACE, *PWINBIO_ENGINE_INTERFACE; 
```



## <a name="requirements"></a>Anforderungen

Windows 10

 

 