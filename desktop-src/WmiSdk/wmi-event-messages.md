---
description: In der folgenden Liste sind Ereignisse aufgelistet, die von WMI-Protokollen in Windows Vista und neueren Betriebssystemen unterstützt werden.
ms.assetid: ad8891cc-0b76-404d-81fc-961bcdbfae32
ms.tgt_platform: multiple
title: WMI-Ereignismeldungen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 543e7131ac0c73a9f1e0f111dafe90197989a33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348301"
---
# <a name="wmi-event-messages"></a><span data-ttu-id="1d6cb-103">WMI-Ereignismeldungen</span><span class="sxs-lookup"><span data-stu-id="1d6cb-103">WMI Event Messages</span></span>

<span data-ttu-id="1d6cb-104">In der folgenden Liste sind Ereignisse aufgelistet, die von WMI-Protokollen in Windows Vista und neueren Betriebssystemen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-104">The following list lists events supported by WMI logs in Windows Vista and later operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="1d6cb-105">Die folgende Dokumentation ist für Entwickler und IT-Administratoren konzipiert.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-105">The following documentation is designed for developers and IT administrators.</span></span> <span data-ttu-id="1d6cb-106">Wenn Sie versuchen, eine WMI-Fehlermeldung auf Ihrem Heimsystem aufzulösen, finden Sie weitere Informationen auf der [Microsoft-Support](https://support.microsoft.com/) -Website.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-106">If you are attempting to resolve a WMI error message on your home system, please refer to the [Microsoft Support](https://support.microsoft.com/) website.</span></span>

 

<dl> <dt>

<span data-ttu-id="1d6cb-107"><span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**WBEM \_ MC- \_ Repository \_ inkonsistent**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-107"><span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**WBEM\_MC\_REPOSITORY\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-108">1073747424 (0x400015e0)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-108">1073747424 (0x400015E0)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-109">Der Windows-Verwaltungsinstrumentation Dienst hat eine Inkonsistenz mit dem WMI-Repository im Verzeichnis *% windir% \\ system32 \\ WBEM \\ Repository* festgestellt und konnte es nicht wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-109">The Windows Management Instrumentation Service detected an inconsistency with the WMI repository in the directory *%windir%\\system32\\wbem\\repository* and was not able to recover it.</span></span> <span data-ttu-id="1d6cb-110">Das WMI-Repository wird nun gelöscht. basierend auf dem Mechanismus für die automatische Wiederherstellung wird ein neues Repository erstellt.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-110">The WMI repository will now be deleted, A new repository will be created based on the auto-recovery mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-111"><span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**Last des \_ \_ \_ \_ LocalSystem- \_ Anbieters \_ des WBEM MC-Anbieters**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-111"><span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**WBEM\_MC\_PROVIDER\_SUBSYSTEM\_LOCALSYSTEM\_PROVIDER\_LOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-112">2147483711 (0x8000003f)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-112">2147483711 (0x8000003F)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-113">Der Anbieter "%1" wurde im Windows-Verwaltungsinstrumentation Namespace "%2" registriert, um das Konto "LocalSystem" zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-113">A provider, %1, has been registered in the Windows Management Instrumentation namespace %2 to use the LocalSystem account.</span></span> <span data-ttu-id="1d6cb-114">Dieses Konto ist privilegiert, und der Anbieter kann zu einer Sicherheitsverletzung führen, wenn die Identität von Benutzer Anforderungen nicht ordnungsgemäß angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-114">This account is privileged and the provider may cause a security violation if it does not correctly impersonate user requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-115"><span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**WBEM \_ MC \_ MOF \_ wurde \_ \_ bei der \_ Wiederherstellung nicht geladen.**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-115"><span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**WBEM\_MC\_MOF\_NOT\_LOADED\_AT\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-116">3221225476 (0xc0000004)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-116">3221225476 (0xC0000004)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-117">Fehler "%1" beim Versuch, MOF "%2" bei der Wiederherstellung zu laden. MOF-Datei, die mit AutoRecover gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-117">Error %1 encountered when trying to load MOF %2 while recovering .MOF file marked with autorecover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-118"><span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM \_ MC \_ kann \_ Filter nicht aktivieren \_**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-118"><span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM\_MC\_CANNOT\_ACTIVATE\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-119">3221225482 (0xc000000a)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-119">3221225482 (0xC000000A)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-120">Der Ereignis Filter mit der Abfrage "%2" konnte aufgrund von Fehler "%3" im Namespace "%1" nicht erneut aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-120">Event filter with query "%2" could not be reactivated in namespace "%1" because of error %3.</span></span> <span data-ttu-id="1d6cb-121">Ereignisse können erst über diesen Filter übermittelt werden, wenn das Problem behoben wurde.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-121">Events cannot be delivered through this filter until the problem is corrected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-122"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**WBEM \_ MC- \_ Abfrage mit ungültigem \_ Ereignis \_ Anbieter \_**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-122"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**WBEM\_MC\_INVALID\_EVENT\_PROVIDER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-123">3221225493 (0xc0000015)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-123">3221225493 (0xC0000015)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-124">Der Ereignis Anbieter %1 hat versucht, eine syntaktisch ungültige Abfrage "%2" zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-124">Event provider %1 attempted to register a syntactically invalid query "%2".</span></span> <span data-ttu-id="1d6cb-125">Die Abfrage wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-125">The query will be ignored.</span></span> <span data-ttu-id="1d6cb-126">Die Abfrage kann korrigiert werden, indem das WMI-Repository mit CIM Studio untersucht und die permanenten Abonnements für den aufgelisteten Anbieter und die Abfrage aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-126">The query can be corrected by examining the WMI repository with CIM studio and updating the permanent subscriptions for the listed provider and query.</span></span> <span data-ttu-id="1d6cb-127">Wenn das permanente Abonnement mit einer MOF-Datei erstellt wird, die mit einem installierten Produkt stammt, muss der Hersteller der Anwendung kontaktiert werden, um die fehlerhafte Registrierung zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-127">If the permanent subscription is created with MOF file coming with an installed product, the application vendor must be contacted to correct the faulty registration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-128"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**systeminterne Abfrage für WBEM \_ MC- \_ \_ Ereignis \_ Anbieter \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-128"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**WBEM\_MC\_INVALID\_EVENT\_PROVIDER\_INTRINSIC\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-129">3221225494 (0xc0000016)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-129">3221225494 (0xC0000016)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-130">Der Ereignis Anbieter %1 hat versucht, eine intrinsische Ereignis Abfrage "%2" im Namespace "%3" zu registrieren, für den der Satz von Zielobjekt Klassen nicht bestimmt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-130">Event provider %1 attempted to register an intrinsic event query "%2" in %3 namespace for which the set of target object classes could not be determined.</span></span> <span data-ttu-id="1d6cb-131">Die Abfrage wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-131">The query will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-132"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**WBEM \_ MC- \_ Ereignis \_ Anbieter \_ Abfrage \_ zu \_ breit**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-132"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_TOO\_BROAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-133">3221225495 (0xc0000017)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-133">3221225495 (0xC0000017)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-134">Der Ereignis Anbieter %1 hat versucht, die Abfrage "%2" im Namespace "%3" zu registrieren, der zu breit ist.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-134">Event provider %1 attempted to register query "%2" in %3 namespace which is too broad.</span></span> <span data-ttu-id="1d6cb-135">Ereignis Anbieter können keine Ereignisse bereitstellen, die vom System bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-135">Event providers cannot provide events that are provided by the system.</span></span> <span data-ttu-id="1d6cb-136">Die Abfrage wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-136">The query will be ignored.</span></span> <span data-ttu-id="1d6cb-137">Wenden Sie sich an den Anwendungshersteller.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-137">Contact the application vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-138"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**die WBEM \_ MC- \_ Ereignis \_ Anbieter \_ Abfrage wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-138"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-139">3221225496 (0xc0000018)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-139">3221225496 (0xC0000018)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-140">Der Ereignis Anbieter %1 hat versucht, die Abfrage "%2" zu registrieren, deren Zielklasse "%3" im %4-Namespace nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-140">Event provider %1 attempted to register query "%2" whose target class "%3" in %4 namespace does not exist.</span></span> <span data-ttu-id="1d6cb-141">Die Abfrage wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-141">The query will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-142"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**WBEM \_ MC- \_ Ereignis \_ Anbieter \_ Abfrage \_ nicht \_ Ereignis**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-142"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_NOT\_EVENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-143">3221225497 (0xc0000019)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-143">3221225497 (0xC0000019)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-144">Der Ereignis Anbieter %1 hat versucht, die Abfrage %2 zu registrieren, &quot; &quot; deren Zielklasse &quot; %3 &quot; keine Ereignisklasse ist.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-144">Event provider %1 attempted to register query &quot;%2&quot; whose target class &quot;%3&quot; is not an event class.</span></span> <span data-ttu-id="1d6cb-145">Die Abfrage wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-145">The query will be ignored.</span></span> <span data-ttu-id="1d6cb-146">Wenden Sie sich an den Anwendungshersteller.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-146">Contact the application vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-147"><span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**WBEM \_ MC \_ WBEM \_ Core- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-147"><span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**WBEM\_MC\_WBEM\_CORE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-148">3221225500 (0xc000001c)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-148">3221225500 (0xC000001C)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-149">Fehler beim Initialisieren des WMI-Core-oder Anbieter Subsystems oder des-Ereignis Subsystems mit der Fehlernummer %1.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-149">Failed to Initialize WMI Core or Provider SubSystem or Event SubSystem with error number %1.</span></span> <span data-ttu-id="1d6cb-150">Dies kann auf eine fehlerhafte Version von WMI, eine fehlerhafte WMI-Repository-Aktualisierung, unzureichenden Speicherplatz oder unzureichenden Arbeitsspeicher zurückzuführen sein.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-150">This could be due to a badly installed version of WMI, WMI repository upgrade failure, insufficient disk space or insufficient memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-151"><span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**Fehler beim \_ \_ ADAP- \_ Verbindungs \_ Fehler in WBEM MC.**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-151"><span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**WBEM\_MC\_ADAP\_CONNECTION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-152">3221225515 (0xc000002b)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-152">3221225515 (0xC000002B)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-153">Fehler beim Herstellen einer Verbindung mit dem Namespace "%1" Windows-Verwaltungsinstrumentation ADAP mit dem folgenden Fehler: %2.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-153">Windows Management Instrumentation ADAP failed to connect to namespace %1 with the following error %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-154"><span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**WBEM \_ MC \_ ADAP \_ Perflib \_ putclass- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-154"><span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**WBEM\_MC\_ADAP\_PERFLIB\_PUTCLASS\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-155">3221225520 (0xc0000030)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-155">3221225520 (0xC0000030)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-156">Windows-Verwaltungsinstrumentation ADAP konnte das Objekt "%1" im Namespace "%2" aufgrund des folgenden Fehlers nicht speichern: %3.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-156">Windows Management Instrumentation ADAP was unable to save object %1 in namespace %2 because of the following error %3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-157"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ ADAP \_ kann \_ \_ WIN32PERF nicht hinzufügen \_**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-157"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM\_MC\_ADAP\_UNABLE\_TO\_ADD\_WIN32PERF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-158">3221225530 (0xc000003a)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-158">3221225530 (0xC000003A)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-159">Windows-Verwaltungsinstrumentation ADAP konnte die Win32 \_ perf-Basisklasse in "%1" nicht erstellen: Ergebnis = %2.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-159">Windows Management Instrumentation ADAP was unable to create the Win32\_Perf base class in %1:Result=%2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-160"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ ADAP \_ kann \_ \_ WIN32PERFRAWDATA nicht hinzufügen \_**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-160"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM\_MC\_ADAP\_UNABLE\_TO\_ADD\_WIN32PERFRAWDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-161">3221225531 (0xc000003b)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-161">3221225531 (0xC000003B)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-162">Windows-Verwaltungsinstrumentation ADAP konnte die Win32 \_ perfrawdata-Basisklasse "%1" nicht erstellen.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-162">Windows Management Instrumentation ADAP was unable to create the Win32\_PerfRawData base class %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-163"><span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**WBEM \_ MC \_ - \_ Repository \_ konnte nicht \_ gestartet werden**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-163"><span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**WBEM\_MC\_REPOSITORY\_FAILED\_TO\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-164">3221231073 (0xc00015e1)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-164">3221231073 (0xC00015E1)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-165">Der Windows-Verwaltungsinstrumentation-Dienst konnte die Repository-Dateien nicht in das Verzeichnis *% windir% \\ system32 \\ WBEM \\ Repository* laden.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-165">The Windows Management Instrumentation Service failed to load the repository files under the directory *%windir%\\system32\\wbem\\repository*.</span></span> <span data-ttu-id="1d6cb-166">Dies kann durch eine Beschädigung der Repository-Dateien, Sicherheitseinstellungen für dieses Verzeichnis, unzureichenden Speicherplatz oder andere Systemressourcen Probleme, wie z. b. unzureichenden Arbeitsspeicher, verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-166">This can be caused by a corruption in the repository files, security settings on this directory, lack of disk space, or other system resource issues such as lack of memory.</span></span> <span data-ttu-id="1d6cb-167">Tritt dieser Fehler immer dann auf, wenn der Computer neu gestartet wird, muss der Administrator auf diesem Computer ggf. den WMI-Dienst unterbinden, die Sicherheitseinstellungen für diesen Ordner und die Dateien in diesem Ordner überprüfen und WMIDiag ausführen, um den Zustand der Windows-Verwaltungsinstrumentation zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-167">If this error occurs each time the computer is restarted then the administrator on this computer may need to stop WMI Service, review the security setting on this folder and files under this folder, and run WMIDiag to validate the health of Windows Management Instrumentation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-168"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM \_ MC \_ WBEM \_ erfordert \_ Verschlüsselung \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-168"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM\_MC\_WBEM\_REQUIRES\_ENCRYPTION\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-169">3221231077 (0xc00015e5)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-169">3221231077 (0xC00015E5)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-170">Der Zugriff auf den %1-Namespace wurde verweigert, da der Namespace mit "Requirements" gekennzeichnet ist, das Skript oder die Anwendung jedoch versucht hat, eine Verbindung mit diesem Namespace mit einer Authentifizierungs Ebene unterhalb des **Pkt- \_ Datenschutzes** herzustellen.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-170">Access to the %1 namespace was denied because the namespace is marked with RequiresEncryption but the script or application attempted to connect to this namespace with an authentication level below **Pkt\_Privacy**.</span></span> <span data-ttu-id="1d6cb-171">Ändern Sie die Authentifizierungs Ebene in **Pkt \_ Privacy** , und führen Sie das Skript oder die Anwendung erneut aus.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-171">Change the authentication level to **Pkt\_Privacy** and run the script or application again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-172"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM \_ MC \_ WBEM \_ erfordert \_ Verschlüsselung \_ Async \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-172"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM\_MC\_WBEM\_REQUIRES\_ENCRYPTION\_ASYNC\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-173">3221231078 (0xc00015e6)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-173">3221231078 (0xC00015E6)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-174">Windows-Verwaltungsinstrumentation Dienst konnte die Ergebnisse für den %1-Namespace nicht asynchron bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-174">Windows Management Instrumentation Service could not deliver results asynchronously for %1 namespace.</span></span> <span data-ttu-id="1d6cb-175">Der Namespace ist mit "Requirements sencryption" gekennzeichnet, aber WinMgmt konnte keine sichere Verbindung mit dem Client Computer herstellen.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-175">The namespace is marked with RequiresEncryption but WinMgmt could not establish a secure connection back to the client computer.</span></span> <span data-ttu-id="1d6cb-176">Stellen Sie sicher, dass zwischen den Client-und Server Computern eine Vertrauensstellung besteht, sodass der Client das Server Computer Konto erkennt.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-176">Ensure there is a trust relationship between the client and server computers so that the client recognizes the server computer account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-177"><span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**WBEM \_ MC \_ WBEM- \_ Host \_ wurde abgebrochen.**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-177"><span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**WBEM\_MC\_WBEM\_HOST\_KILLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-178">3221231084 (0xc00015ec)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-178">3221231084 (0xC00015EC)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-179">Windows-Verwaltungsinstrumentation wurde WMIPRVSE.EXE beendet, weil ein Kontingent einen Warnungs Wert erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-179">Windows Management Instrumentation has stopped WMIPRVSE.EXE because a quota reached a warning value.</span></span> <span data-ttu-id="1d6cb-180">Kontingent: %1, Wert: %2, Maximalwert: %3, wmiprvse-PID: %4.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-180">Quota: %1 Value: %2 Maximum value: %3 WMIPRVSE PID: %4.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-181"><span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM \_ MC \_ WBEM \_ repfilesnotfound**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-181"><span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM\_MC\_WBEM\_REPFILESNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-182">3221231086 (0xc00015ee)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-182">3221231086 (0xC00015EE)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-183">Während des Dienst Starts konnte der Windows-Verwaltungsinstrumentation-Dienst die Repository-Dateien nicht finden.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-183">During the service startup, the Windows Management Instrumentation service was unable to locate the repository files.</span></span> <span data-ttu-id="1d6cb-184">Basierend auf dem Mechanismus für die automatische Wiederherstellung wird ein neues Repository erstellt.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-184">A new repository will be created based on the auto-recovery mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-185"><span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM \_ MC \_ WBEM wurde erfolgreich \_ gestartet \_ .**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-185"><span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM\_MC\_WBEM\_STARTED\_SUCESSFULLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-186">3221231087 (0xc00015ef)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-186">3221231087 (0xC00015EF)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-187">Windows-Verwaltungsinstrumentation Dienst wurde erfolgreich gestartet.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-187">Windows Management Instrumentation Service started successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-188"><span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM \_ MC \_ WBEM \_ Core \_ PSS \_ ESS \_ Initialisiert**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-188"><span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM\_MC\_WBEM\_CORE\_PSS\_ESS\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-189">3221231089 (0xc00015, f 1)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-189">3221231089 (0xC00015F1)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-190">Windows-Verwaltungsinstrumentation Dienst Subsysteme wurden erfolgreich initialisiert.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-190">Windows Management Instrumentation Service subsystems initialized successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-191"><span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**Fehler beim Initialisierungs Dienst von WBEM \_ MC \_ WBEM. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-191"><span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**WBEM\_MC\_WBEM\_SERVICE\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-192">3221225501 (0xc000001d)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-192">3221225501 (0xC000001D)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-193">Fehlernummer %1 wurde bei dem Versuch zurückgegeben, Windows-Verwaltungsinstrumentation Dienst zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-193">Error number %1 was returned in trying to initialize Windows Management Instrumentation Service.</span></span> <span data-ttu-id="1d6cb-194">Dies kann auf eine fehlerhafte Version von WMI, eine fehlerhafte WMI-Repository-Aktualisierung, unzureichenden Speicherplatz oder unzureichenden Arbeitsspeicher zurückzuführen sein.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-194">This could be due to a badly installed version of WMI, WMI repository upgrade failure, insufficient disk space or insufficient memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d6cb-195"><span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**WBEM \_ MC \_ WBEM- \_ Repository \_ neu erstellt**</span><span class="sxs-lookup"><span data-stu-id="1d6cb-195"><span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**WBEM\_MC\_WBEM\_REPOSITORY\_RECREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d6cb-196">3221231088 (0xc00015, f 0)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-196">3221231088 (0xC00015F0)</span></span>
</dt> <dt>



<span data-ttu-id="1d6cb-197">Windows-Verwaltungsinstrumentation Repository wurde mit dem AutoRecovery-Mechanismus erfolgreich neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-197">Windows Management Instrumentation Repository successfully recreated using Autorecovery mechanism.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d6cb-198">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d6cb-198">Requirements</span></span>



| <span data-ttu-id="1d6cb-199">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d6cb-199">Requirement</span></span> | <span data-ttu-id="1d6cb-200">Wert</span><span class="sxs-lookup"><span data-stu-id="1d6cb-200">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1d6cb-201">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-201">Minimum supported client</span></span><br/> | <span data-ttu-id="1d6cb-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d6cb-202">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1d6cb-203">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d6cb-203">Minimum supported server</span></span><br/> | <span data-ttu-id="1d6cb-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d6cb-204">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d6cb-205">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d6cb-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d6cb-206">WMI-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="1d6cb-206">WMI Events</span></span>](wmi-events.md)
</dt> <dt>

[<span data-ttu-id="1d6cb-207">WMI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="1d6cb-207">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> </dl>

 

 




