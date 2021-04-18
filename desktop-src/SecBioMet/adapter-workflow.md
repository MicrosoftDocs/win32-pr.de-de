---
title: Adapter Workflow
description: In diesem Abschnitt wird der Registrierungs Workflow aus der Perspektive der Adapter-Plug-Ins beschrieben.
ms.assetid: 0392124A-78CF-49E3-A52A-1E2E3A100E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68f93146e1d6cedd42094876547bfe0c945d6a7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337807"
---
# <a name="adapter-workflow"></a><span data-ttu-id="27fbd-103">Adapter Workflow</span><span class="sxs-lookup"><span data-stu-id="27fbd-103">Adapter Workflow</span></span>

<span data-ttu-id="27fbd-104">In diesem Abschnitt wird der Registrierungs Workflow aus der Perspektive der Adapter-Plug-Ins beschrieben.</span><span class="sxs-lookup"><span data-stu-id="27fbd-104">This section describes the enrollment workflow from the perspective of the adapter plugins.</span></span>

<span data-ttu-id="27fbd-105">In Windows 10 haben wir eine v4-Engine-Schnittstelle implementiert, die zwei neue Engine-Adapter Funktionen bereitstellt: [**engineadapterkreatekey**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn) und [**engineadapteridentifyfeaturesetsecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn).</span><span class="sxs-lookup"><span data-stu-id="27fbd-105">In Windows 10, we ve implemented a V4 engine interface that provides 2 new engine adapter functions, [**EngineAdapterCreateKey**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn) and [**EngineAdapterIdentifyFeatureSetSecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn).</span></span> <span data-ttu-id="27fbd-106">Diese neuen Funktionen ermöglichen die Unterstützung sicherer Biometrie mithilfe von TPM 2,0.</span><span class="sxs-lookup"><span data-stu-id="27fbd-106">These new functions allow support for secure biometrics using TPM 2.0.</span></span> <span data-ttu-id="27fbd-107">Die folgende Tabelle zeigt den Adapter seitigen Registrierungs Workflow.</span><span class="sxs-lookup"><span data-stu-id="27fbd-107">The following table shows the adapter-side enrollment workflow.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27fbd-108">Client-API</span><span class="sxs-lookup"><span data-stu-id="27fbd-108">Client API</span></span></td>
<td><span data-ttu-id="27fbd-109">Adapter Methoden</span><span class="sxs-lookup"><span data-stu-id="27fbd-109">Adapter Methods</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27fbd-110"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>Winbiogetproperty (EXTENDED_ENGINE_INFO)</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-110"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty(EXTENDED_ENGINE_INFO)</strong></a></span></span></td>
<td><span data-ttu-id="27fbd-111"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn"><strong>Engineadapterqueryextendedinfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-111"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn"><strong>EngineAdapterQueryExtendedInfo</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27fbd-112"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin"><strong>Winbioeinschreibung</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-112"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin"><strong>WinBioEnrollBegin</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="27fbd-113"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn"><strong>Storageadapterquerybysubject</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-113"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn"><strong>StorageAdapterQueryBySubject</strong></a></span></span></li>
<li><span data-ttu-id="27fbd-114"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn"><strong>Sensoradapterclearcontext</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-114"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn"><strong>SensorAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="27fbd-115"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>Engineadapterclearcontext</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-115"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="27fbd-116"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>Storageadapterclearcontext</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-116"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="27fbd-117"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn"><strong>Engineadapterkreateeinschreibung</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-117"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn"><strong>EngineAdapterCreateEnrollment</strong></a></span></span></li>
<li><span data-ttu-id="27fbd-118"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn"><strong>Engineadaptersetenrollmentparameters</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-118"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn"><strong>EngineAdapterSetEnrollmentParameters</strong></a></span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27fbd-119"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture"><strong>Winbioregistrierungs Erfassung</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-119"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture"><strong>WinBioEnrollCapture</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="27fbd-120"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn"><strong>Sensoradapterstartcapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-120"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn"><strong>SensorAdapterStartCapture</strong></a></span></span></li>
<li><span data-ttu-id="27fbd-121"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn"><strong>Sensoradapterfinishcapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-121"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn"><strong>SensorAdapterFinishCapture</strong></a></span></span></li>
<li><span data-ttu-id="27fbd-122"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn"><strong>Sensoradapterpushdatatoengine</strong></a><strong>[-#b0 </strong> <a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn"><strong>engineadapterakzeptsampledata</strong></a>]</span><span class="sxs-lookup"><span data-stu-id="27fbd-122"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn"><strong>SensorAdapterPushDataToEngine</strong></a><strong>[-></strong><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn"><strong>EngineAdapterAcceptSampleData</strong></a>]</span></span></li>
<li><span data-ttu-id="27fbd-123">Wenn S_OK oder WINBIO_I_MORE_DATA</span><span class="sxs-lookup"><span data-stu-id="27fbd-123">If S_OK or WINBIO_I_MORE_DATA</span></span>
<ol>
<li><span data-ttu-id="27fbd-124"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn"><strong>Engineadapterupdateregistrierung</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-124"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn"><strong>EngineAdapterUpdateEnrollment</strong></a></span></span></li>
<li><span data-ttu-id="27fbd-125">[Aufrufer setzt die Registrierung fort]</span><span class="sxs-lookup"><span data-stu-id="27fbd-125">[Caller continues enrollment]</span></span></li>
</ol></li>
<li><span data-ttu-id="27fbd-126">Andernfalls wenn WINBIO_E_BAD_CAPTURE [Aufrufer den Ablehnungs Feedback anzeigt, setzt die Registrierung fort]</span><span class="sxs-lookup"><span data-stu-id="27fbd-126">Else if WINBIO_E_BAD_CAPTURE [Caller displays reject feedback, continues enrollment]</span></span> <br/></li>
<li><span data-ttu-id="27fbd-127">Andernfalls andernfalls</span><span class="sxs-lookup"><span data-stu-id="27fbd-127">Else if other ERROR</span></span>
<ol>
<li><span data-ttu-id="27fbd-128"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>Engineadapterclearcontext</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-128"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="27fbd-129"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>Storageadapterclearcontext</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-129"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="27fbd-130">[Die Registrierung wird von einem Bio-Dienst abgebrochen]</span><span class="sxs-lookup"><span data-stu-id="27fbd-130">[Bio service aborts enrollment]</span></span></li>
</ol></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27fbd-131"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>Winbiogetproperty (EXTENDED_ENROLLMENT_STATUS)</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-131"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty (EXTENDED_ENROLLMENT_STATUS)</strong></a></span></span></td>
<td><span data-ttu-id="27fbd-132"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn"><strong>Engineadapterqueryextendedenrollmentstatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-132"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn"><strong>EngineAdapterQueryExtendedEnrollmentStatus</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27fbd-133"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit"><strong>Winbioregistricommit</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-133"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit"><strong>WinBioEnrollCommit</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="27fbd-134"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn"><strong>Engineadaptercheckforduplicate</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-134"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn"><strong>EngineAdapterCheckForDuplicate</strong></a></span></span></li>
<li><span data-ttu-id="27fbd-135">Wenn eine Wechsel Datenbank</span><span class="sxs-lookup"><span data-stu-id="27fbd-135">If REMOVABLE DATABASE</span></span>
<ol>
<li><span data-ttu-id="27fbd-136"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn"><strong>Engineadaptergetenrollmenthash</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-136"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn"><strong>EngineAdapterGetEnrollmentHash</strong></a></span></span></li>
<li><span data-ttu-id="27fbd-137"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>Engineadaptercommitenrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-137"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span></span></li>
</ol></li>
<li><span data-ttu-id="27fbd-138">Else<a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>engineadaptercommitenrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-138">Else<a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27fbd-139"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard"><strong>Winbioeinschreibung verwerfen</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-139"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard"><strong>WinBioEnrollDiscard</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="27fbd-140"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn"><strong>Engineadapterverwerdenrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-140"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn"><strong>EngineAdapterDiscardEnrollment</strong></a></span></span></li>
<li><span data-ttu-id="27fbd-141"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>Engineadapterclearcontext</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-141"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="27fbd-142"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>Storageadapterclearcontext</strong></a></span><span class="sxs-lookup"><span data-stu-id="27fbd-142"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 





