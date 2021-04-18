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
# <a name="adapter-workflow"></a>Adapter Workflow

In diesem Abschnitt wird der Registrierungs Workflow aus der Perspektive der Adapter-Plug-Ins beschrieben.

In Windows 10 haben wir eine v4-Engine-Schnittstelle implementiert, die zwei neue Engine-Adapter Funktionen bereitstellt: [**engineadapterkreatekey**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn) und [**engineadapteridentifyfeaturesetsecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn). Diese neuen Funktionen ermöglichen die Unterstützung sicherer Biometrie mithilfe von TPM 2,0. Die folgende Tabelle zeigt den Adapter seitigen Registrierungs Workflow.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Client-API</td>
<td>Adapter Methoden</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>Winbiogetproperty (EXTENDED_ENGINE_INFO)</strong></a></td>
<td><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn"><strong>Engineadapterqueryextendedinfo</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin"><strong>Winbioeinschreibung</strong></a></td>
<td><ol>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn"><strong>Storageadapterquerybysubject</strong></a></li>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn"><strong>Sensoradapterclearcontext</strong></a></li>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>Engineadapterclearcontext</strong></a></li>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>Storageadapterclearcontext</strong></a></li>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn"><strong>Engineadapterkreateeinschreibung</strong></a></li>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn"><strong>Engineadaptersetenrollmentparameters</strong></a></li>
</ol></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture"><strong>Winbioregistrierungs Erfassung</strong></a></td>
<td><ol>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn"><strong>Sensoradapterstartcapture</strong></a></li>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn"><strong>Sensoradapterfinishcapture</strong></a></li>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn"><strong>Sensoradapterpushdatatoengine</strong></a><strong>[-#b0 </strong> <a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn"><strong>engineadapterakzeptsampledata</strong></a>]</li>
<li>Wenn S_OK oder WINBIO_I_MORE_DATA
<ol>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn"><strong>Engineadapterupdateregistrierung</strong></a></li>
<li>[Aufrufer setzt die Registrierung fort]</li>
</ol></li>
<li>Andernfalls wenn WINBIO_E_BAD_CAPTURE [Aufrufer den Ablehnungs Feedback anzeigt, setzt die Registrierung fort] <br/></li>
<li>Andernfalls andernfalls
<ol>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>Engineadapterclearcontext</strong></a></li>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>Storageadapterclearcontext</strong></a></li>
<li>[Die Registrierung wird von einem Bio-Dienst abgebrochen]</li>
</ol></li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>Winbiogetproperty (EXTENDED_ENROLLMENT_STATUS)</strong></a></td>
<td><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn"><strong>Engineadapterqueryextendedenrollmentstatus</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit"><strong>Winbioregistricommit</strong></a></td>
<td><ol>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn"><strong>Engineadaptercheckforduplicate</strong></a></li>
<li>Wenn eine Wechsel Datenbank
<ol>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn"><strong>Engineadaptergetenrollmenthash</strong></a></li>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>Engineadaptercommitenrollment</strong></a></li>
</ol></li>
<li>Else<a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>engineadaptercommitenrollment</strong></a><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard"><strong>Winbioeinschreibung verwerfen</strong></a></td>
<td><ol>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn"><strong>Engineadapterverwerdenrollment</strong></a></li>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>Engineadapterclearcontext</strong></a></li>
<li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>Storageadapterclearcontext</strong></a></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 





