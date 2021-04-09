---
title: WINBIO_BIR_PURPOSE Konstanten (winbio \_ types. h)
description: Geben Sie den Zweck an, für den der biometrische Informationsdaten Satz (BIR) vorgesehen ist oder für den er geeignet ist.
ms.assetid: AAFD3203-4D3D-43B5-A833-1258E1E281D3
topic_type:
- apiref
api_name:
- WINBIO_NO_PURPOSE_AVAILABLE
- WINBIO_PURPOSE_VERIFY
- WINBIO_PURPOSE_IDENTIFY
- WINBIO_PURPOSE_ENROLL
- WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION
- WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION
- WINBIO_PURPOSE_AUDIT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a662a5ae045d3afc631f93cdf296508dabccf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956524"
---
# <a name="winbio_bir_purpose-constants"></a><span data-ttu-id="f1b01-103">Winbio-und- \_ \_ Zweck-Konstanten</span><span class="sxs-lookup"><span data-stu-id="f1b01-103">WINBIO\_BIR\_PURPOSE Constants</span></span>

<span data-ttu-id="f1b01-104">Die folgenden Flags werden vom **Purpose** -Member der [**winbio- \_ \_ Header**](winbio-bir-header.md) Struktur verwendet, um den Zweck anzugeben, für den der biometrische Informationsdaten Satz (BIR) vorgesehen ist oder für den er geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="f1b01-104">The following flags are used by the **Purpose** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure to specify the purpose for which the biometric information record (BIR) is intended or for which it is suitable.</span></span>



| <span data-ttu-id="f1b01-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="f1b01-105">Constant</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="f1b01-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1b01-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <span data-ttu-id="f1b01-107"><dt>**winbio \_ ist \_ nicht \_ verfügbar.**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b01-107"><dt>**WINBIO\_NO\_PURPOSE\_AVAILABLE**</dt></span></span> </dl>                                         | <span data-ttu-id="f1b01-108">Es wurde kein Zweck angegeben.</span><span class="sxs-lookup"><span data-stu-id="f1b01-108">No purpose is specified.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <span data-ttu-id="f1b01-109"><dt>**Überprüfung von winbio- \_ Zwecken \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b01-109"><dt>**WINBIO\_PURPOSE\_VERIFY**</dt></span></span> </dl>                                                            | <span data-ttu-id="f1b01-110">Überprüfen Sie die Identität eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f1b01-110">Verify the identity of a user.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <span data-ttu-id="f1b01-111"><dt>**Zweck der winbio- \_ \_ Identifizierung**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b01-111"><dt>**WINBIO\_PURPOSE\_IDENTIFY**</dt></span></span> </dl>                                                      | <span data-ttu-id="f1b01-112">Identifizieren Sie einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f1b01-112">Identify a user.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <span data-ttu-id="f1b01-113"><dt>**winbio- \_ Aufgabe \_ registrieren**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b01-113"><dt>**WINBIO\_PURPOSE\_ENROLL**</dt></span></span> </dl>                                                            | <span data-ttu-id="f1b01-114">Registrieren Sie einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f1b01-114">Enroll a user.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <span data-ttu-id="f1b01-115"><dt>**winbio- \_ Zweck \_ für die \_ über \_ Prüfung**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b01-115"><dt>**WINBIO\_PURPOSE\_ENROLL\_FOR\_VERIFICATION**</dt></span></span> </dl>       | <span data-ttu-id="f1b01-116">Erfassen Sie ein biometrisches Beispiel, und bestimmen Sie, ob das Beispiel der angegebenen Benutzeridentität entspricht.</span><span class="sxs-lookup"><span data-stu-id="f1b01-116">Capture a biometric sample and determine whether the sample corresponds to the specified user identity.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <span data-ttu-id="f1b01-117"><dt>**winbio- \_ Zweck \_ \_ zur \_ Identifizierung registrieren**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b01-117"><dt>**WINBIO\_PURPOSE\_ENROLL\_FOR\_IDENTIFICATION**</dt></span></span> </dl> | <span data-ttu-id="f1b01-118">Erfassen eines biometrischen Beispiels und ermitteln, ob es mit einer vorhandenen biometrischen Vorlage übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f1b01-118">Capture a biometric sample and determine whether it matches an existing biometric template.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <span data-ttu-id="f1b01-119"><dt>**Überprüfung von winbio- \_ Zwecken \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b01-119"><dt>**WINBIO\_PURPOSE\_AUDIT**</dt></span></span> </dl>                                                               | <span data-ttu-id="f1b01-120">Zusätzliche Informationen, die für die Protokollierung oder die Anzeige verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f1b01-120">Extra information that can be used for logging or for display.</span></span> <span data-ttu-id="f1b01-121">Dieser Wert wird bei der Eingabe von allen Funktionen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f1b01-121">This value is ignored on input by all functions.</span></span> <span data-ttu-id="f1b01-122">Bei der Ausgabe ist Sie nur verfügbar, wenn Sie von der biometrischen Einheit unterstützt wird, und Sie geben das **winbio \_ Data \_ Flag \_ RAW** im *Flags* -Parameter der [**winbiocapturesample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="f1b01-122">On output, it will only be available if supported by the biometric unit and you specify **WINBIO\_DATA\_FLAG\_RAW** in the *Flags* parameter of the [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) function.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f1b01-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1b01-123">Requirements</span></span>



| <span data-ttu-id="f1b01-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1b01-124">Requirement</span></span> | <span data-ttu-id="f1b01-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f1b01-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b01-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1b01-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f1b01-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1b01-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="f1b01-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1b01-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f1b01-129">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1b01-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f1b01-130">Header</span><span class="sxs-lookup"><span data-stu-id="f1b01-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1b01-131"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1b01-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1b01-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1b01-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b01-133">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="f1b01-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="f1b01-134">**winbio- \_ Bir- \_ Header**</span><span class="sxs-lookup"><span data-stu-id="f1b01-134">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





