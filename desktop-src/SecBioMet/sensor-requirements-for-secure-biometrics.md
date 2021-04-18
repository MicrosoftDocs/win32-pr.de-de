---
title: Sensor Anforderungen für sichere Biometrie
description: Sensor Anforderungen für sichere Biometrie
ms.assetid: 6D5709E9-7B6B-4D6C-BF85-C6FB5DF5A7EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f4e41f8300a124115c2b6cd380f904f216f491
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337443"
---
# <a name="sensor-requirements-for-secure-biometrics"></a><span data-ttu-id="3116c-103">Sensor Anforderungen für sichere Biometrie</span><span class="sxs-lookup"><span data-stu-id="3116c-103">Sensor requirements for secure biometrics</span></span>

<span data-ttu-id="3116c-104">Microsoft nutzt Trusted Platform Module (TPM) 2,0, um sicherzustellen, dass auf der entsprechenden Hardware Software (bis auf Kernel Ebene) keine gültige biometrische Authentifizierung erzeugt, wenn der biometrische Benutzer des Benutzers zum Zeitpunkt der Authentifizierung nicht zur Verfügung gestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3116c-104">Microsoft leverages Trusted Platform Module (TPM) 2.0 to ensure that on appropriate hardware, software (up to and including kernel-level malware) cannot produce a valid biometric authentication if the user’s biometric was not provided at the time of authentication.</span></span>

<span data-ttu-id="3116c-105">Zu diesem Zweck verwenden wir Sitzungs basierte TPM 2,0-Autorisierungen und den Sensor zum Extrahieren und Abgleichen von Features in einer vertrauenswürdigen Ausführungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="3116c-105">To do this, we use TPM 2.0 session-based authorizations and the sensor performing feature extraction and matching in a trusted execution environment.</span></span> <span data-ttu-id="3116c-106">Beim ersten Mal, wenn das Windows-Biometrieframework einen sicheren Sensor sieht (wie von der sicheren Sensor Funktion gemeldet), wird ein geheimer Schlüssel bereitgestellt, der zwischen dem sicheren biometrischen Sensor und dem TPM gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="3116c-106">The first time the Windows Biometric Framework sees a secure sensor (as reported by the secure sensor capability), it provisions a secret that is shared between the secure biometric sensor and the TPM.</span></span> <span data-ttu-id="3116c-107">Dieser geheime Schlüssel wird nie wieder für das Betriebssystem verfügbar gemacht und ist für jeden Sensor eindeutig.</span><span class="sxs-lookup"><span data-stu-id="3116c-107">That secret is never again exposed to the OS, and it is unique to each sensor.</span></span>

<span data-ttu-id="3116c-108">Zum Durchführen einer Authentifizierung wird vom Windows-Biometrieframework eine Sitzung mit dem TPM geöffnet und eine Nonce abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3116c-108">To perform an authentication, the Windows Biometric Framework opens a session with the TPM and obtains a nonce.</span></span> <span data-ttu-id="3116c-109">Die Nonce wird als Teil eines sicheren Vergleichs Vorgangs an den sicheren Sensor übermittelt.</span><span class="sxs-lookup"><span data-stu-id="3116c-109">The nonce is passed into the secure sensor as part of a secure match operation.</span></span> <span data-ttu-id="3116c-110">Der Sensor führt die Entsprechung in der vertrauenswürdigen Ausführungsumgebung aus. ist er erfolgreich, berechnet er einen HMAC über diese Nonce und die Identität des identifizierten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="3116c-110">The sensor performs the match in the trusted execution environment, and if it is successful, calculates an HMAC over that nonce and the identity of the user who was identified.</span></span>

<span data-ttu-id="3116c-111">Dieser HMAC kann vom Windows-Biometrieframework verwendet werden, um für den identifizierten Benutzer Kryptografievorgänge im TPM auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3116c-111">This HMAC can be used by the Windows Biometric Framework to perform cryptographic operations in the TPM for the user who was identified.</span></span> <span data-ttu-id="3116c-112">Der HMAC ist kurzlebig und läuft nach einigen Sekunden ab.</span><span class="sxs-lookup"><span data-stu-id="3116c-112">The HMAC is short-lived, and expires after a few seconds.</span></span>

<span data-ttu-id="3116c-113">Mithilfe dieses Protokolls sind nach der anfänglichen Bereitstellung keine sensiblen Daten im Betriebssystem enthalten.</span><span class="sxs-lookup"><span data-stu-id="3116c-113">Using this protocol, after the initial provisioning, no sensitive data is contained in the OS.</span></span> <span data-ttu-id="3116c-114">Geheimnisse werden von TPM und dem sicheren Sensor gehalten, und das einzige, was während der Authentifizierung verfügbar gemacht wird, ist der kurzlebige HMAC.</span><span class="sxs-lookup"><span data-stu-id="3116c-114">Secrets are held by the TPM and the secure sensor, and the only thing that is exposed during the authentication is the short-lived HMAC.</span></span>

## <a name="secure-sensor-capability"></a><span data-ttu-id="3116c-115">Funktion des sicheren Sensors</span><span class="sxs-lookup"><span data-stu-id="3116c-115">Secure sensor capability</span></span>

<span data-ttu-id="3116c-116">Die Funktion für den sicheren Windows-Funktions \_ \_ \_ Sensor muss vom Sensor gemeldet werden, wenn Sie die neuen Engine-Adapter Methoden in v 4,0 der Engine-Adapter Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3116c-116">The WINBIO\_CAPABILITY\_SECURE\_SENSOR capability must be reported by the sensor if it supports the new engine adapter methods in v 4.0 of the engine adapter interface.</span></span>

<span data-ttu-id="3116c-117">Um zu beanspruchen, dass ein Sensor ein sicherer Sensor ist, muss er die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="3116c-117">To claim that a sensor is a secure sensor it must meet the following requirements:</span></span>

-   <span data-ttu-id="3116c-118">Die passende Engine des Sensors muss vom normalen Betriebssystem isoliert werden (z. b. mithilfe einer vertrauenswürdigen Ausführungsumgebung).</span><span class="sxs-lookup"><span data-stu-id="3116c-118">The matching engine of the sensor must be isolated from the normal OS (for example, using a trusted execution environment)</span></span>
-   <span data-ttu-id="3116c-119">Der Sensor muss eine sichere Eingabe von Beispielen für das isolierte übereinstimmende Modul unterstützen. der Inhalt der Beispiele darf niemals dem normalen Betriebssystem verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="3116c-119">The sensor must support secure input of samples to the isolated matching engine; the content of the samples must never be exposed to the normal OS</span></span>
-   <span data-ttu-id="3116c-120">Die entsprechende Engine muss die Freigabe sicherer Anmelde Informationen unterstützen, indem die unten aufgeführten neuen V4-Methoden implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="3116c-120">The matching engine must support secure credential release by implementing the new v4 methods outlined below</span></span>
-   <span data-ttu-id="3116c-121">Der Sensor muss die Erkennung von Präsentations Angriffen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3116c-121">The sensor must support presentation attack detection.</span></span>

<span data-ttu-id="3116c-122">Der Wert für den sicheren winbio- \_ Fähigkeits \_ \_ Sensor ist in der Struktur der [**winbio- \_ Funktionen**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) enthalten.</span><span class="sxs-lookup"><span data-stu-id="3116c-122">The WINBIO\_CAPABILITY\_SECURE\_SENSOR value is contained in the [**WINBIO\_CAPABILITIES**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) structure.</span></span> <span data-ttu-id="3116c-123">Im folgenden finden Sie ein Beispiel dafür, wie Sie es definieren.</span><span class="sxs-lookup"><span data-stu-id="3116c-123">Here's an example of how to define it.</span></span>


```
#define WINBIO_CAPABILITY_SECURE_SENSOR     ((WINBIO_CAPABILITIES)0x00000100)
```



## <a name="error-codes"></a><span data-ttu-id="3116c-124">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3116c-124">Error Codes</span></span>


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



## <a name="engine-adapter-interface-v-40"></a><span data-ttu-id="3116c-125">Engine-Adapter Schnittstelle v 4,0</span><span class="sxs-lookup"><span data-stu-id="3116c-125">Engine adapter interface v 4.0</span></span>

<span data-ttu-id="3116c-126">Die Engine-Adapter Schnittstellen Version wurde auf 4,0 erhöht.</span><span class="sxs-lookup"><span data-stu-id="3116c-126">The engine adapter interface version has been incremented to 4.0.</span></span> <span data-ttu-id="3116c-127">Die zusätzlichen Funktionen in der neuen Schnittstelle ermöglichen es dem Sensor, an TPM 2,0 teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="3116c-127">The additional functions in the new interface allow the sensor to participate in TPM 2.0.</span></span> <span data-ttu-id="3116c-128">Sie lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3116c-128">They are:</span></span>

-   [<span data-ttu-id="3116c-129">**Engineadapterkreatekey**</span><span class="sxs-lookup"><span data-stu-id="3116c-129">**EngineAdapterCreateKey**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn)
-   [<span data-ttu-id="3116c-130">**Engineadapteridentifyfeaturesetsecure**</span><span class="sxs-lookup"><span data-stu-id="3116c-130">**EngineAdapterIdentifyFeatureSetSecure**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn)


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



## <a name="requirements"></a><span data-ttu-id="3116c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3116c-131">Requirements</span></span>

<span data-ttu-id="3116c-132">Windows 10</span><span class="sxs-lookup"><span data-stu-id="3116c-132">Windows 10</span></span>

 

 