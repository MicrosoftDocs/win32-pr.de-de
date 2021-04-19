---
title: Engine-Adapter Wrapper
description: Funktionen, die Sie verwenden können, um Funktionen für den Engine-Adapter aufzurufen. Diese Funktionen sind in winbio \_ Adapter. h definiert.
ms.assetid: b3d6d617-e423-4ed5-9d29-be72c5dd8b49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5ec0fcc3b6ea358e8238061bc74e2933d8bf87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337385"
---
# <a name="engine-adapter-wrappers"></a>Engine-Adapter Wrapper

Die folgenden Wrapper Funktionen sind in winbio \_ Adapter. h definiert. Sie können Sie verwenden, um Funktionen auf dem Engine-Adapter aufzurufen.



| Funktion                                           | BESCHREIBUNG                                                                                                                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wbioengineakzeptsampledata<br/>              | Ruft die [**engineadapterakzeptsampledata**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn) -Funktion auf.<br/>                                                                                                 |
| Wbioengineaktivierungs<br/>                      | Ruft die [**engineadapteraktivierungs**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_activate_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>                                           |
| Wbioengineattach<br/>                        | Ruft die [**engineadapterattach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_attach_fn) -Funktion auf.<br/>                                                                                                                     |
| Wbioenginecheckforduplicate<br/>             | Ruft die [**engineadaptercheckforduplicate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn) -Funktion auf.<br/>                                                                                               |
| Wbioengineclearcontext<br/>                  | Ruft die [**engineadapterclearcontext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn) -Funktion auf.<br/>                                                                                                         |
| Wbioenginecommitenrollment<br/>              | Ruft die [**engineadaptercommitenrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn) -Funktion auf.<br/>                                                                                                 |
| Wbioenginecontrolunit<br/>                   | Ruft die [**engineadaptercontrolunit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_fn) -Funktion auf.<br/>                                                                                                           |
| Wbioenginecontrolunitprivilegiert<br/>         | Ruft die [**engineadaptercontrolunitprivilegierte**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_privileged_fn) -Funktion auf.<br/>                                                                                       |
| Wbioenginecreateeinschreibung<br/>              | Ruft die [**engineadapterup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn) -Registrierungsfunktion auf.<br/>                                                                                                 |
| Wbioenginedeaktiviert<br/>                    | Ruft die [**engineadapterdeaktivieren**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_deactivate_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>                                       |
| Wbioenginedetach<br/>                        | Ruft die [**engineadapterdetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_detach_fn) -Funktion auf.<br/>                                                                                                                     |
| Wbioengineverwerdenrollment<br/>             | Ruft die [**engineadapterverwerdenrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn) -Funktion auf.<br/>                                                                                               |
| Wbioengineexportenginedata<br/>              | Ruft die [**engineadapterexportenginedata**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_export_engine_data_fn) -Funktion auf.<br/>                                                                                                 |
| Wbioenginegetenrollmenthash<br/>             | Ruft die [**engineadaptergetenrollmenthash**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn) -Funktion auf.<br/>                                                                                               |
| Wbioenginegetenrollmentstatus<br/>           | Ruft die [**engineadaptergetenrollmentstatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_status_fn) -Funktion auf.<br/>                                                                                           |
| Wbioengineidentifyall<br/>                   | Ruft die [**engineadapteridentifyall**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>                                     |
| Wbioengineidentifyfeatureset<br/>            | Ruft die [**engineadapteridentifyfeatureset**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_fn) -Funktion auf.<br/>                                                                                             |
| Wbioenginenotifypowerchange<br/>             | Ruft die [*engineadapternotifypowerchange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_notify_power_change_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 8 unterstützt.<br/>                            |
| Wbioenginepipelinecleanup<br/>               | Ruft die [**engineadapterpipelinecleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_cleanup_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>                             |
| Wbioenginepipelineinit<br/>                  | Ruft die [**engineadapterpipelineinit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_init_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>                                   |
| Wbioenginequerycalibrationdata<br/>          | Ruft die [**engineadapterquerycalibrationdata**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_calibration_data_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>                   |
| Wbioenginequeryextendedenrollmentstatus<br/> | Ruft die [**engineadapterqueryextendedenrollmentstatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/> |
| Wbioenginequeryextendedinfo<br/>             | Ruft die [**engineadapterqueryextendedinfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>                         |
| Wbioenginequeryhashalgorithms<br/>           | Ruft die [**engineadapterqueryhashalgorithms**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_hash_algorithms_fn) -Funktion auf.<br/>                                                                                           |
| Wbioenginequeryindexvector size<br/>          | Ruft die [**engineadapterqueryindexvectorsize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_index_vector_size_fn) -Funktion auf.<br/>                                                                                         |
| Wbioenginequerypreferredformat<br/>          | Ruft die [**engineadapterquerypreferredformat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_preferred_format_fn) -Funktion auf.<br/>                                                                                         |
| Wbioenginequerysamplehint<br/>               | Ruft die [**engineadapterquerysamplehint**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_sample_hint_fn) -Funktion auf.<br/>                                                                                                   |
| Wbioenginerefreshcache<br/>                  | Ruft die [**engineadaptererfrischendes Cache**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_refresh_cache_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>                                   |
| Wbioengineselectcalibrationformat<br/>       | Ruft die [**engineadapterselectcalibrationformat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_select_calibration_format_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>             |
| Wbioenginesetaccountpolicy<br/>              | Ruft die [**engineadaptersetaccountpolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>                           |
| Wbioenginesetenrollmentparameters<br/>       | Ruft die [**engineadaptersetenrollmentparameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>             |
| Wbioenginesetenrollmentselector<br/>         | Ruft die [**engineadaptersetenrollmentselector**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_selector_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>                 |
| Wbioenginesethashalgorithm<br/>              | Ruft die [**engineadaptersethashalgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) -Funktion auf.<br/>                                                                                                 |
| Wbioengineupdateregistrierungen<br/>              | Ruft die [**engineadapterupdateregistriment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn) -Funktion auf.<br/>                                                                                                 |
| Wbioengineverifyfeatureset<br/>              | Ruft die [**engineadapterverifyfeatureset**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_verify_feature_set_fn) -Funktion auf.<br/>                                                                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Engine-Adapter Funktionen](engine-adapter-functions.md)
</dt> <dt>

[Plug-in-Funktionen](plug-in-functions.md)
</dt> </dl>

 

 





