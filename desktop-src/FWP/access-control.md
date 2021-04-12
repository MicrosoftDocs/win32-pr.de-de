---
title: Access Control (Windows-Filter Plattform)
description: In der Windows-Filter Plattform (WFP) implementiert der Dienst für die Basis Filter-Engine (BFE) das standardmäßige Windows-Zugriffs Steuerungsmodell, das auf Zugriffs Token und Sicherheits Beschreibungen basiert.
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0df63b6fe92b18614a7ccf205ccf826927664ee
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104350988"
---
# <a name="access-control-windows-filtering-platform"></a><span data-ttu-id="da7b3-103">Access Control (Windows-Filter Plattform)</span><span class="sxs-lookup"><span data-stu-id="da7b3-103">Access Control (Windows Filtering Platform)</span></span>

<span data-ttu-id="da7b3-104">In der Windows-Filter Plattform (WFP) implementiert der Dienst für die Basis Filter-Engine (BFE) das standardmäßige [Windows-Zugriffs Steuerungsmodell](/windows/desktop/SecAuthZ/access-control-model) , das auf Zugriffs Token und Sicherheits Beschreibungen basiert.</span><span class="sxs-lookup"><span data-stu-id="da7b3-104">In Windows Filtering Platform (WFP), the Base Filtering Engine (BFE) service implements the standard [Windows access control model](/windows/desktop/SecAuthZ/access-control-model) based on access tokens and security descriptors.</span></span>

## <a name="access-control-model"></a><span data-ttu-id="da7b3-105">Access Control Modell</span><span class="sxs-lookup"><span data-stu-id="da7b3-105">Access Control Model</span></span>

<span data-ttu-id="da7b3-106">Sicherheits Beschreibungen können beim Hinzufügen neuer WFP-Objekte, z. b. Filter und Unterebenen, angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="da7b3-106">Security descriptors can be specified when adding new WFP objects, such as filters and sub-layers.</span></span> <span data-ttu-id="da7b3-107">Sicherheits Deskriptoren werden mithilfe der WFP-Verwaltungsfunktionen " **swpm \* GetSecurityInfo0** " und " **\* SetSecurityInfo0**" verwaltet, wobei "\* *\** _" für den Namen des WFP-Objekts steht.</span><span class="sxs-lookup"><span data-stu-id="da7b3-107">Security descriptors are managed using the WFP management functions **Fwpm\*GetSecurityInfo0** and **Fwpm\*SetSecurityInfo0**, where \**\** _ stands for the WFP object's name.</span></span> <span data-ttu-id="da7b3-108">Diese Funktionen sind semantisch identisch mit den Funktionen Windows [_ *GetSecurityInfo* \*](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) und [**setsecurityinfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="da7b3-108">These functions are semantically identical to the Windows [_ *GetSecurityInfo*\*](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

> [!Note]  
> <span data-ttu-id="da7b3-109">Die **fwpm \* SetSecurityInfo0** -Funktionen können nicht innerhalb einer expliziten Transaktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="da7b3-109">The **Fwpm\*SetSecurityInfo0** functions cannot be called from within an explicit transaction.</span></span>

 

> [!Note]  
> <span data-ttu-id="da7b3-110">Die **fwpm \* SetSecurityInfo0** -Funktionen können nur innerhalb einer dynamischen Sitzung aufgerufen werden, wenn Sie zum Verwalten eines dynamischen Objekts verwendet werden, das innerhalb derselben Sitzung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="da7b3-110">The **Fwpm\*SetSecurityInfo0** functions can only be called from within a dynamic session if they are being used to manage a dynamic object created within the same session.</span></span>

 

<span data-ttu-id="da7b3-111">Die Standard Sicherheits Beschreibung für die Filter-Engine (das Stamm-Engine-Objekt im folgenden Diagramm) lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="da7b3-111">The default security descriptor for the filter engine (the root Engine object in the diagram below) is as follows.</span></span>

-   <span data-ttu-id="da7b3-112">Erteilen Sie der integrierten Gruppe "Administratoren" allgemeine Zugriffsrechte ( **Allgemein \_** verfügbar).</span><span class="sxs-lookup"><span data-stu-id="da7b3-112">Grant **GENERIC\_ALL** (GA) access rights to the built-in Administrators group.</span></span>
-   <span data-ttu-id="da7b3-113">Erteilen von **generischen \_ Read** (GR) generic **\_ Write** ( **GW \_ )-** Zugriffsrechten für Netzwerk Konfigurations Operatoren.</span><span class="sxs-lookup"><span data-stu-id="da7b3-113">Grant **GENERIC\_READ** (GR) **GENERIC\_WRITE** (GW) **GENERIC\_EXECUTE** (GX) access rights to network configuration operators.</span></span>
-   <span data-ttu-id="da7b3-114">Erteilen Sie den folgenden Dienst Sicherheits-IDs (SSIDs) **grgwgx** -Zugriffsrechte: mpssvc (Windows-Firewall), NAPAgent (Netzwerk Zugriffsschutz-Agent), policyagent (IPSec-Richtlinien-Agent), RPCSS (Remote Prozedur Aufrufe) und wdiservicehost (Diagnosedienst Host).</span><span class="sxs-lookup"><span data-stu-id="da7b3-114">Grant **GRGWGX** access rights to the following service security identifiers (SSIDs): MpsSvc (Windows Firewall), NapAgent (Network Access Protection Agent), PolicyAgent (IPsec Policy Agent), RpcSs (Remote Procedure Call), and WdiServiceHost (Diagnostic Service Host).</span></span>
-   <span data-ttu-id="da7b3-115">Gewähren Sie **fwpm \_ actrl \_ Open** und **fwpm \_ actrl \_** für jeden.</span><span class="sxs-lookup"><span data-stu-id="da7b3-115">Grant **FWPM\_ACTRL\_OPEN** and **FWPM\_ACTRL\_CLASSIFY** to everyone.</span></span> <span data-ttu-id="da7b3-116">(Hierbei handelt es sich um WFP-spezifische Zugriffsrechte, die in der folgenden Tabelle beschrieben werden.)</span><span class="sxs-lookup"><span data-stu-id="da7b3-116">(These are WFP-specific access rights, described in table below.)</span></span>

<span data-ttu-id="da7b3-117">Die übrigen Standard Sicherheits Deskriptoren werden durch Vererbung abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="da7b3-117">The remaining default security descriptors are derived through inheritance.</span></span>

<span data-ttu-id="da7b3-118">Es gibt einige Zugriffs Überprüfungen, wie z. b. für die Funktion "Add0", "f", "f", "", "f", " **\* f** ", die Funktionsaufrufe von " **\***", **\***</span><span class="sxs-lookup"><span data-stu-id="da7b3-118">There are some access checks, such as for **Fwpm\*Add0**, **Fwpm\*CreateEnumHandle0**, **Fwpm\*SubscribeChanges0** function calls, that cannot be done at the individual object level.</span></span> <span data-ttu-id="da7b3-119">Für diese Funktionen gibt es Containerobjekte für jeden Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="da7b3-119">For these functions, there are container objects for each object type.</span></span> <span data-ttu-id="da7b3-120">Bei den Standard Objekttypen (z. b. Anbietern, Legenden, Filtern) werden die vorhandenen Funktionen für die Funktion " **\* GetSecurityInfo0** " und " **\* SetSecurityInfo0** " überlastet, sodass ein NULL- **GUID** -Parameter den zugeordneten Container identifiziert.</span><span class="sxs-lookup"><span data-stu-id="da7b3-120">For the standard object types (for example, providers, callouts, filters), the existing **Fwpm\*GetSecurityInfo0** and **Fwpm\*SetSecurityInfo0** functions are overloaded, such that a null **GUID** parameter identifies the associated container.</span></span> <span data-ttu-id="da7b3-121">Für die anderen Objekttypen (z. b. Netzwerkereignisse und IPSec-Sicherheits Zuordnungen) gibt es explizite Funktionen zum Verwalten der Sicherheitsinformationen des Containers.</span><span class="sxs-lookup"><span data-stu-id="da7b3-121">For the other object types (for example, network events and IPsec security associations), there are explicit functions for managing the container's security information.</span></span>

<span data-ttu-id="da7b3-122">BFE unterstützt die automatische Vererbung von DACL-Zugriffs Steuerungs Einträgen (diskret Access Control List).</span><span class="sxs-lookup"><span data-stu-id="da7b3-122">BFE supports automatic inheritance of Discretionary Access Control List (DACL) access control entries (ACEs).</span></span> <span data-ttu-id="da7b3-123">BFE unterstützt keine SACL-ACEs (System Access Control List).</span><span class="sxs-lookup"><span data-stu-id="da7b3-123">BFE does not support System Access Control List (SACL) ACEs.</span></span> <span data-ttu-id="da7b3-124">-Objekte erben ACEs von Ihrem Container.</span><span class="sxs-lookup"><span data-stu-id="da7b3-124">Objects inherit ACEs from their container.</span></span> <span data-ttu-id="da7b3-125">Container erben ACEs von der Filter-Engine.</span><span class="sxs-lookup"><span data-stu-id="da7b3-125">Containers inherit ACEs from the filter engine.</span></span> <span data-ttu-id="da7b3-126">Die weitergabepfade werden im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="da7b3-126">The propagation paths are shown in the diagram below.</span></span>

![Diagramm, das die ACE-propagierungs Pfade anzeigt, beginnend mit "Engine".](images/access-control.jpg)

<span data-ttu-id="da7b3-128">Für die Standard Objekttypen erzwingt BFE alle allgemeinen und standardmäßigen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="da7b3-128">For the standard object types, BFE enforces all the generic and standard access rights.</span></span> <span data-ttu-id="da7b3-129">Außerdem definiert WFP die folgenden spezifischen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="da7b3-129">In addition, WFP defines the following specific access rights.</span></span>



| <span data-ttu-id="da7b3-130">WFP-Zugriffsrecht</span><span class="sxs-lookup"><span data-stu-id="da7b3-130">WFP Access Right</span></span>                                                                                                                        | <span data-ttu-id="da7b3-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da7b3-131">Description</span></span>                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da7b3-132"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**Hinzufügen von "f"- \_ actrl \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-132"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM\_ACTRL\_ADD**</span></span><br/>                                       | <span data-ttu-id="da7b3-133">Erforderlich zum Hinzufügen eines Objekts zu einem Container.</span><span class="sxs-lookup"><span data-stu-id="da7b3-133">Required to add an object to a container.</span></span><br/>                                                                                                                     |
| <span data-ttu-id="da7b3-134"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**\_ \_ Link zum Hinzufügen von "f"-actrl \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-134"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/>                       | <span data-ttu-id="da7b3-135">Erforderlich, um eine Zuordnung zu einem Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="da7b3-135">Required to create an association to an object.</span></span> <span data-ttu-id="da7b3-136">Wenn Sie z. b. einen Filter hinzufügen möchten, der auf eine Legende verweist, muss der Aufrufer über die Berechtigung Link hinzufügen \_ für die Legende verfügen.</span><span class="sxs-lookup"><span data-stu-id="da7b3-136">For example, to add a filter that references a callout, the caller must have ADD\_LINK access to the callout.</span></span><br/> |
| <span data-ttu-id="da7b3-137"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**f- \_ v-actrl \_ Begin \_ Read \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-137"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM\_ACTRL\_BEGIN\_READ\_TXN**</span></span><br/>    | <span data-ttu-id="da7b3-138">Erforderlich, um eine explizite Lese Transaktion zu starten.</span><span class="sxs-lookup"><span data-stu-id="da7b3-138">Required to begin an explicit read transaction.</span></span><br/>                                                                                                               |
| <span data-ttu-id="da7b3-139"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**f/a- \_ \_ \_ Schreibvorgänge starten \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-139"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span><br/> | <span data-ttu-id="da7b3-140">Erforderlich, um eine explizite Schreib Transaktion zu starten.</span><span class="sxs-lookup"><span data-stu-id="da7b3-140">Required to begin an explicit write transaction.</span></span><br/>                                                                                                              |
| <span data-ttu-id="da7b3-141"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_kwpm-actrl- \_ Klassifizierung**</span><span class="sxs-lookup"><span data-stu-id="da7b3-141"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM\_ACTRL\_CLASSIFY**</span></span><br/>                        | <span data-ttu-id="da7b3-142">Erforderlich, um eine Klassifizierung mit einer benutzermodusebene durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="da7b3-142">Required to classify against a user-mode layer.</span></span><br/>                                                                                                               |
| <span data-ttu-id="da7b3-143"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**WPM- \_ actrl-Aufzählung \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-143"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM\_ACTRL\_ENUM**</span></span><br/>                                    | <span data-ttu-id="da7b3-144">Erforderlich, um die-Objekte in einem Container aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="da7b3-144">Required to enumerate the objects in a container.</span></span> <span data-ttu-id="da7b3-145">Der Enumerator gibt jedoch nur Objekte zurück, für die der Aufrufer über fwpm \_ actrl \_ Lesezugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="da7b3-145">However, the enumerator only returns objects to which the caller has FWPM\_ACTRL\_READ access.</span></span><br/>              |
| <span data-ttu-id="da7b3-146"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**geöffnetes WPM- \_ actrl \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-146"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM\_ACTRL\_OPEN**</span></span><br/>                                    | <span data-ttu-id="da7b3-147">Erforderlich, um eine Sitzung mit BFE zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="da7b3-147">Required to open a session with BFE.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="da7b3-148"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**\_Lesezugriff auf die Datei \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-148"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM\_ACTRL\_READ**</span></span><br/>                                    | <span data-ttu-id="da7b3-149">Erforderlich, um die Eigenschaften eines Objekts zu lesen.</span><span class="sxs-lookup"><span data-stu-id="da7b3-149">Required to read an object's properties.</span></span><br/>                                                                                                                      |
| <span data-ttu-id="da7b3-150"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**Lese Statistik für das awpm- \_ actrl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-150"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM\_ACTRL\_READ\_STATS**</span></span><br/>                 | <span data-ttu-id="da7b3-151">Erforderlich zum Lesen von Statistiken.</span><span class="sxs-lookup"><span data-stu-id="da7b3-151">Required to read statistics.</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="da7b3-152"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**Konto für die \_ Anmeldung mit dem \_ Anmelde Namen**</span><span class="sxs-lookup"><span data-stu-id="da7b3-152"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM\_ACTRL\_SUBSCRIBE**</span></span><br/>                     | <span data-ttu-id="da7b3-153">Erforderlich zum Abonnieren von Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="da7b3-153">Required to subscribe for notifications.</span></span> <span data-ttu-id="da7b3-154">Abonnenten erhalten nur dann Benachrichtigungen für Objekte, auf die Sie über fwpm- \_ actrl- \_ Lesezugriff verfügen.</span><span class="sxs-lookup"><span data-stu-id="da7b3-154">Subscribers will only receive notifications for objects to which they have FWPM\_ACTRL\_READ access.</span></span><br/>                 |
| <span data-ttu-id="da7b3-155"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**f- \_ \_ /Schreibzugriff**</span><span class="sxs-lookup"><span data-stu-id="da7b3-155"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM\_ACTRL\_WRITE**</span></span><br/>                                 | <span data-ttu-id="da7b3-156">Erforderlich, um Engine-Optionen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="da7b3-156">Required to set engine options.</span></span><br/>                                                                                                                               |



 

<span data-ttu-id="da7b3-157">BFE überspringt alle Zugriffs Überprüfungen für Aufrufer im Kernel Modus.</span><span class="sxs-lookup"><span data-stu-id="da7b3-157">BFE skips all access checks for kernel-mode callers.</span></span>

<span data-ttu-id="da7b3-158">Um zu verhindern, dass sich Administratoren selbst aus den BFE sperren, wird den Mitgliedern der integrierten Gruppe "Administratoren" immer die **fwpm-Zugriffs \_ \_ Berechtigung für** das Engine-Objekt erteilt.</span><span class="sxs-lookup"><span data-stu-id="da7b3-158">In order to prevent administrators from locking themselves out of BFE, members of the built-in administrators group are always granted **FWPM\_ACTRL\_OPEN** to the engine object.</span></span> <span data-ttu-id="da7b3-159">Daher kann ein Administrator mithilfe der folgenden Schritte wieder Zugriff erhalten.</span><span class="sxs-lookup"><span data-stu-id="da7b3-159">Thus, an administrator can regain access through the following steps.</span></span>

-   <span data-ttu-id="da7b3-160">Aktivieren Sie die Berechtigung zum **\_ Übernehmen des \_ Besitz Besitzes \_** .</span><span class="sxs-lookup"><span data-stu-id="da7b3-160">Enable the **SE\_TAKE\_OWNERSHIP\_NAME** privilege.</span></span>
-   <span data-ttu-id="da7b3-161">[**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)abrufen.</span><span class="sxs-lookup"><span data-stu-id="da7b3-161">Call [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span> <span data-ttu-id="da7b3-162">Der Aufruf ist erfolgreich, da der Aufrufer ein Member integrierter Administratoren ist.</span><span class="sxs-lookup"><span data-stu-id="da7b3-162">The call succeeds because the caller is a member of Built-in Administrators.</span></span>
-   <span data-ttu-id="da7b3-163">Übernimmt den Besitz des Engine-Objekts.</span><span class="sxs-lookup"><span data-stu-id="da7b3-163">Take ownership of the engine object.</span></span> <span data-ttu-id="da7b3-164">Dies ist erfolgreich, da der Aufrufer über die Berechtigung zum Akzeptieren des **\_ \_ Besitz Besitzes \_** verfügt.</span><span class="sxs-lookup"><span data-stu-id="da7b3-164">This succeeds because the caller has the **SE\_TAKE\_OWNERSHIP\_NAME** privilege.</span></span>
-   <span data-ttu-id="da7b3-165">Aktualisieren Sie die DACL.</span><span class="sxs-lookup"><span data-stu-id="da7b3-165">Update the DACL.</span></span> <span data-ttu-id="da7b3-166">Dies ist erfolgreich, weil der Besitzer immer über Schreibzugriff auf **\_ DAC** verfügt.</span><span class="sxs-lookup"><span data-stu-id="da7b3-166">This succeeds because the owner always has **WRITE\_DAC** access</span></span>

<span data-ttu-id="da7b3-167">Da BFE seine eigene benutzerdefinierte Überwachung unterstützt, werden keine generischen Objekt Zugriffs Überwachungen generiert.</span><span class="sxs-lookup"><span data-stu-id="da7b3-167">Since BFE supports its own custom auditing, it does not generate generic object access audits.</span></span> <span data-ttu-id="da7b3-168">Daher wird die SACL ignoriert.</span><span class="sxs-lookup"><span data-stu-id="da7b3-168">Thus, the SACL is ignored.</span></span>

## <a name="wfp-required-access-rights"></a><span data-ttu-id="da7b3-169">Erforderliche WFP-Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="da7b3-169">WFP Required Access Rights</span></span>

<span data-ttu-id="da7b3-170">Die folgende Tabelle zeigt die Zugriffsrechte, die für die WFP-Funktionen erforderlich sind, um auf verschiedene Filter Platt Form Objekte zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="da7b3-170">The table below shows the access rights required by the WFP functions in order to access various filtering platform objects.</span></span> <span data-ttu-id="da7b3-171">Die **Funktionen von "f wpmfilter \* *_" werden als Beispiel für den Zugriff auf die Standardobjekte aufgeführt. Alle anderen Funktionen, die auf Standardobjekte zugreifen, folgen dem* Zugriffs Modell für \* die _** -voll Zugriffs Filter-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="da7b3-171">The **FwpmFilter\**_ functions are listed as an example for accessing the standard objects. All the other functions that access standard objects follow the _\* FwpmFilter\**\* functions access model.</span></span>



<span data-ttu-id="da7b3-172">Funktion</span><span class="sxs-lookup"><span data-stu-id="da7b3-172">Function</span></span>

<span data-ttu-id="da7b3-173">Objekt geprüft</span><span class="sxs-lookup"><span data-stu-id="da7b3-173">Object Checked</span></span>

<span data-ttu-id="da7b3-174">Erforderlicher Zugriff</span><span class="sxs-lookup"><span data-stu-id="da7b3-174">Access Required</span></span>

[<span data-ttu-id="da7b3-175">**FwpmEngineOpen0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-175">**FwpmEngineOpen0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

<span data-ttu-id="da7b3-176">Engine</span><span class="sxs-lookup"><span data-stu-id="da7b3-176">Engine</span></span>

<span data-ttu-id="da7b3-177">**geöffnetes WPM- \_ actrl \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-177">**FWPM\_ACTRL\_OPEN**</span></span>

[<span data-ttu-id="da7b3-178">**FwpmEngineGetOption0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-178">**FwpmEngineGetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

<span data-ttu-id="da7b3-179">Engine</span><span class="sxs-lookup"><span data-stu-id="da7b3-179">Engine</span></span>

<span data-ttu-id="da7b3-180">**\_Lesezugriff auf die Datei \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-180">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="da7b3-181">**FwpmEngineSetOption0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-181">**FwpmEngineSetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

<span data-ttu-id="da7b3-182">Engine</span><span class="sxs-lookup"><span data-stu-id="da7b3-182">Engine</span></span>

<span data-ttu-id="da7b3-183">**f- \_ \_ /Schreibzugriff**</span><span class="sxs-lookup"><span data-stu-id="da7b3-183">**FWPM\_ACTRL\_WRITE**</span></span>

[<span data-ttu-id="da7b3-184">**FwpmSessionCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-184">**FwpmSessionCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

<span data-ttu-id="da7b3-185">Engine</span><span class="sxs-lookup"><span data-stu-id="da7b3-185">Engine</span></span>

<span data-ttu-id="da7b3-186">**WPM- \_ actrl-Aufzählung \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-186">**FWPM\_ACTRL\_ENUM**</span></span>

[<span data-ttu-id="da7b3-187">**FwpmTransactionBegin0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-187">**FwpmTransactionBegin0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

<span data-ttu-id="da7b3-188">Engine</span><span class="sxs-lookup"><span data-stu-id="da7b3-188">Engine</span></span>

<span data-ttu-id="da7b3-189">"F" **\_ actrl \_ Begin \_ Read \_ TXn**  &  **\_ BTRL \_ Begin \_ Write \_ TXn**</span><span class="sxs-lookup"><span data-stu-id="da7b3-189">**FWPM\_ACTRL\_BEGIN\_READ\_TXN** & **FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span>

[<span data-ttu-id="da7b3-190">**FwpmFilterAdd0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-190">**FwpmFilterAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

<span data-ttu-id="da7b3-191">Container Anbieter</span><span class="sxs-lookup"><span data-stu-id="da7b3-191">Container Provider</span></span><br/> <span data-ttu-id="da7b3-192">Ebene</span><span class="sxs-lookup"><span data-stu-id="da7b3-192">Layer</span></span><br/> <span data-ttu-id="da7b3-193">Sub-Layer</span><span class="sxs-lookup"><span data-stu-id="da7b3-193">Sub-Layer</span></span><br/> <span data-ttu-id="da7b3-194">Legende</span><span class="sxs-lookup"><span data-stu-id="da7b3-194">Callout</span></span><br/> <span data-ttu-id="da7b3-195">Anbieter Kontext</span><span class="sxs-lookup"><span data-stu-id="da7b3-195">Provider Context</span></span><br/>

<span data-ttu-id="da7b3-196">**Link zum Hinzufügen von "f. \_ actrl \_ addfwpm \_ actrl" \_ \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-196">**FWPM\_ACTRL\_ADDFWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="da7b3-197">**\_ \_ Link zum Hinzufügen von "f"-actrl \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-197">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="da7b3-198">**\_ \_ Link zum Hinzufügen von "f"-actrl \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-198">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="da7b3-199">**\_ \_ Link zum Hinzufügen von "f"-actrl \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-199">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="da7b3-200">**\_ \_ Link zum Hinzufügen von "f"-actrl \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-200">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/>

<span data-ttu-id="da7b3-201">[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)</span><span class="sxs-lookup"><span data-stu-id="da7b3-201">[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)</span></span><br/>

<span data-ttu-id="da7b3-202">Filter</span><span class="sxs-lookup"><span data-stu-id="da7b3-202">Filter</span></span>

<span data-ttu-id="da7b3-203">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="da7b3-203">**DELETE**</span></span>

<span data-ttu-id="da7b3-204">[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)</span><span class="sxs-lookup"><span data-stu-id="da7b3-204">[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)</span></span><br/>

<span data-ttu-id="da7b3-205">Filter</span><span class="sxs-lookup"><span data-stu-id="da7b3-205">Filter</span></span>

<span data-ttu-id="da7b3-206">**\_Lesezugriff auf die Datei \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-206">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="da7b3-207">**FwpmFilterCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-207">**FwpmFilterCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

<span data-ttu-id="da7b3-208">Container Filter</span><span class="sxs-lookup"><span data-stu-id="da7b3-208">Container Filter</span></span><br/>

<span data-ttu-id="da7b3-209">**Lesevorgänge für die Konto- \_ actrl- \_ aufzuruf \_ \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-209">**FWPM\_ACTRL\_ENUMFWPM\_ACTRL\_READ**</span></span><br/>

[<span data-ttu-id="da7b3-210">**FwpmFilterSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-210">**FwpmFilterSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

<span data-ttu-id="da7b3-211">Container</span><span class="sxs-lookup"><span data-stu-id="da7b3-211">Container</span></span>

<span data-ttu-id="da7b3-212">**Konto für die \_ Anmeldung mit dem \_ Anmelde Namen**</span><span class="sxs-lookup"><span data-stu-id="da7b3-212">**FWPM\_ACTRL\_SUBSCRIBE**</span></span>

[<span data-ttu-id="da7b3-213">**FwpmFilterSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-213">**FwpmFilterSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

<span data-ttu-id="da7b3-214">Container</span><span class="sxs-lookup"><span data-stu-id="da7b3-214">Container</span></span>

<span data-ttu-id="da7b3-215">**\_Lesezugriff auf die Datei \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-215">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="da7b3-216">**IPsecGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-216">**IPsecGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

<span data-ttu-id="da7b3-217">IPSec-SA-DB</span><span class="sxs-lookup"><span data-stu-id="da7b3-217">IPsec SA DB</span></span>

<span data-ttu-id="da7b3-218">**Lese Statistik für das awpm- \_ actrl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-218">**FWPM\_ACTRL\_READ\_STATS**</span></span>

<span data-ttu-id="da7b3-219">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)</span><span class="sxs-lookup"><span data-stu-id="da7b3-219">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)</span></span><br/> [<span data-ttu-id="da7b3-220">**IPsecSaContextAddInbound0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-220">**IPsecSaContextAddInbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [<span data-ttu-id="da7b3-221">**IPsecSaContextAddOutbound0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-221">**IPsecSaContextAddOutbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

<span data-ttu-id="da7b3-222">IPSec-SA-DB</span><span class="sxs-lookup"><span data-stu-id="da7b3-222">IPsec SA DB</span></span>

<span data-ttu-id="da7b3-223">**Hinzufügen von "f"- \_ actrl \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-223">**FWPM\_ACTRL\_ADD**</span></span>

<span data-ttu-id="da7b3-224">[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)</span><span class="sxs-lookup"><span data-stu-id="da7b3-224">[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)</span></span><br/>

<span data-ttu-id="da7b3-225">IPSec-SA-DB</span><span class="sxs-lookup"><span data-stu-id="da7b3-225">IPsec SA DB</span></span>

<span data-ttu-id="da7b3-226">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="da7b3-226">**DELETE**</span></span>

[<span data-ttu-id="da7b3-227">**IPsecSaContextGetById0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-227">**IPsecSaContextGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

<span data-ttu-id="da7b3-228">IPSec-SA-DB</span><span class="sxs-lookup"><span data-stu-id="da7b3-228">IPsec SA DB</span></span>

<span data-ttu-id="da7b3-229">**\_Lesezugriff auf die Datei \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-229">**FWPM\_ACTRL\_READ**</span></span>

<span data-ttu-id="da7b3-230">[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)</span><span class="sxs-lookup"><span data-stu-id="da7b3-230">[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)</span></span><br/>

<span data-ttu-id="da7b3-231">IPSec-SA-DB</span><span class="sxs-lookup"><span data-stu-id="da7b3-231">IPsec SA DB</span></span>

<span data-ttu-id="da7b3-232">"F" **\_ actrl \_**-Aufzählungs-  &  **f- \_ \_ Lese** Vorgänge</span><span class="sxs-lookup"><span data-stu-id="da7b3-232">**FWPM\_ACTRL\_ENUM** & **FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="da7b3-233">**IkeextGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-233">**IkeextGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

<span data-ttu-id="da7b3-234">IKE-SA-DB</span><span class="sxs-lookup"><span data-stu-id="da7b3-234">IKE SA DB</span></span>

<span data-ttu-id="da7b3-235">**Lese Statistik für das awpm- \_ actrl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-235">**FWPM\_ACTRL\_READ\_STATS**</span></span>

[<span data-ttu-id="da7b3-236">**IkeextSaDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-236">**IkeextSaDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

<span data-ttu-id="da7b3-237">IKE-SA-DB</span><span class="sxs-lookup"><span data-stu-id="da7b3-237">IKE SA DB</span></span>

<span data-ttu-id="da7b3-238">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="da7b3-238">**DELETE**</span></span>

[<span data-ttu-id="da7b3-239">**IkeextSaGetById0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-239">**IkeextSaGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

<span data-ttu-id="da7b3-240">IKE-SA-DB</span><span class="sxs-lookup"><span data-stu-id="da7b3-240">IKE SA DB</span></span>

<span data-ttu-id="da7b3-241">**\_Lesezugriff auf die Datei \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-241">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="da7b3-242">**IkeextSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-242">**IkeextSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

<span data-ttu-id="da7b3-243">IKE-SA-DB</span><span class="sxs-lookup"><span data-stu-id="da7b3-243">IKE SA DB</span></span>

<span data-ttu-id="da7b3-244">"F" **\_ actrl \_**-Aufzählungs-  &  **f- \_ \_ Lese** Vorgänge</span><span class="sxs-lookup"><span data-stu-id="da7b3-244">**FWPM\_ACTRL\_ENUM** & **FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="da7b3-245">**FwpmNetEventCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="da7b3-245">**FwpmNetEventCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

<span data-ttu-id="da7b3-246">Container</span><span class="sxs-lookup"><span data-stu-id="da7b3-246">Container</span></span>

<span data-ttu-id="da7b3-247">**WPM- \_ actrl-Aufzählung \_**</span><span class="sxs-lookup"><span data-stu-id="da7b3-247">**FWPM\_ACTRL\_ENUM**</span></span>

<span data-ttu-id="da7b3-248">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)</span><span class="sxs-lookup"><span data-stu-id="da7b3-248">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)</span></span><br/>

<span data-ttu-id="da7b3-249">Keine weiteren Zugriffs Überprüfungen außerhalb der einzelnen Filter und Anbieter Kontexte</span><span class="sxs-lookup"><span data-stu-id="da7b3-249">No additional access checks beyond those for the individual filters and provider contexts</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="da7b3-250">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="da7b3-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da7b3-251">**Standard Zugriffsrechte**</span><span class="sxs-lookup"><span data-stu-id="da7b3-251">**Standard Access Rights**</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[<span data-ttu-id="da7b3-252">Windows-Zugriffs Steuerungsmodell</span><span class="sxs-lookup"><span data-stu-id="da7b3-252">Windows access control model</span></span>](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[<span data-ttu-id="da7b3-253">**Windows-Filterungs Plattform-Zugriffsrechte Bezeichner**</span><span class="sxs-lookup"><span data-stu-id="da7b3-253">**Windows Filtering Platform Access Rights Identifiers**</span></span>](access-right-identifiers.md)
</dt> </dl>

 

