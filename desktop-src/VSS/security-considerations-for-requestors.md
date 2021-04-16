---
description: Die VSS-Infrastruktur erfordert, dass VSS-Anforderer (z. b. Sicherungs Anwendungen) sowohl als com-Clients als auch als Server fungieren kann.
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: Sicherheitsüberlegungen für anfordernde Personen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e989793dbf5a5dd1fac3224cf6f06958564de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345009"
---
# <a name="security-considerations-for-requesters"></a><span data-ttu-id="d614a-103">Sicherheitsüberlegungen für anfordernde Personen</span><span class="sxs-lookup"><span data-stu-id="d614a-103">Security Considerations for Requesters</span></span>

<span data-ttu-id="d614a-104">Die VSS-Infrastruktur erfordert, dass VSS-Anforderer (z. b. Sicherungs Anwendungen) sowohl als com-Clients als auch als Server fungieren kann.</span><span class="sxs-lookup"><span data-stu-id="d614a-104">The VSS infrastructure requires VSS requesters, such as backup applications, to be able to function both as COM clients and as a server.</span></span>

<span data-ttu-id="d614a-105">Wenn ein Anforderer als Server fungiert, macht er einen Satz von com-Rückruf Schnittstellen verfügbar, die von externen Prozessen (z. b. Writer oder VSS-Dienst) aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="d614a-105">When acting as a server, a requester exposes a set of COM callback interfaces that can be invoked from external processes (such as writers or the VSS service).</span></span> <span data-ttu-id="d614a-106">Daher müssen Anforderer sicher verwalten, welche com-Clients eingehende com-Aufrufe in seinem Prozess durchführen können.</span><span class="sxs-lookup"><span data-stu-id="d614a-106">Therefore, requesters need to securely manage which COM clients are able to make incoming COM calls into its process.</span></span>

<span data-ttu-id="d614a-107">Ebenso können Anforderer als com-Client für die COM-APIs fungieren, die von einem VSS Writer oder vom VSS-Dienst bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d614a-107">Similarly, requesters can act as a COM client for the COM APIs supplied by a VSS writer or by the VSS service.</span></span> <span data-ttu-id="d614a-108">Die requestspezifischen Sicherheitseinstellungen müssen ausgehende com-Aufrufe von der anfordernden Person an diese anderen Prozesse zulassen.</span><span class="sxs-lookup"><span data-stu-id="d614a-108">The requester-specific security settings must allow outgoing COM calls from the requester to these other processes.</span></span>

<span data-ttu-id="d614a-109">Der einfachste Mechanismus zur Verwaltung der Sicherheitsprobleme eines Anforderers umfasst die richtige Auswahl des Benutzerkontos, unter dem es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d614a-109">The simplest mechanism for managing a requester's security issues involves proper selection of the user account under which it runs.</span></span>

<span data-ttu-id="d614a-110">Ein Anforderer muss in der Regel unter einem Benutzer ausgeführt werden, der Mitglied der Gruppe "Administratoren" oder der Gruppe "Sicherungs-Operatoren" ist oder als lokales System Konto ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d614a-110">A requester typically needs to run under a user that is a member of either the Administrators group or the Backup Operators group, or run as the Local System account.</span></span>

<span data-ttu-id="d614a-111">Wenn eine anfordernde Person als com-Client fungiert und diese nicht unter diesen Konten ausgeführt wird, wird jeder com-Befehl standardmäßig automatisch mit **E \_ AccessDenied** abgelehnt, ohne dass die Implementierung der com-Methode erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d614a-111">By default, when a requester is acting as a COM client, if it does not run under these accounts, any COM call is automatically rejected with **E\_ACCESSDENIED**, without even getting to the COM method implementation.</span></span>

## <a name="disabling-com-exception-handling"></a><span data-ttu-id="d614a-112">Deaktivieren der com-Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="d614a-112">Disabling COM Exception Handling</span></span>

<span data-ttu-id="d614a-113">Legen Sie beim Entwickeln eines Anforderers das Flag com-comglb \_ Exception \_ donot \_ handle Global Options fest, um die com-Ausnahmebehandlung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d614a-113">When developing a requester, set the COM COMGLB\_EXCEPTION\_DONOT\_HANDLE global options flag to disable COM exception handling.</span></span> <span data-ttu-id="d614a-114">Dies ist wichtig, da durch die com-Ausnahmebehandlung schwerwiegende Fehler in einer VSS-Anwendung maskiert werden können.</span><span class="sxs-lookup"><span data-stu-id="d614a-114">It is important to do this because COM exception handling can mask fatal errors in a VSS application.</span></span> <span data-ttu-id="d614a-115">Der Fehler, der maskiert wird, kann den Prozess in einem instabilen und unvorhersehbaren Zustand belassen, was zu Beschädigungen und hängen von Beschädigungen führen kann.</span><span class="sxs-lookup"><span data-stu-id="d614a-115">The error that is masked can leave the process in an unstable and unpredictable state, which can lead to corruptions and hangs.</span></span> <span data-ttu-id="d614a-116">Weitere Informationen zu diesem Flag finden Sie unter [iglobaloptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span><span class="sxs-lookup"><span data-stu-id="d614a-116">For more information about this flag, see [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span></span>

## <a name="setting-requester-default-com-access-check-permission"></a><span data-ttu-id="d614a-117">Festlegen der Berechtigung "Requester default com Access Check"</span><span class="sxs-lookup"><span data-stu-id="d614a-117">Setting Requester Default COM Access Check Permission</span></span>

<span data-ttu-id="d614a-118">Die anfordernde Person muss beachten, dass bei Ihrem Prozess als Server (z. b. zum Ändern des Dokuments der Sicherungs Komponenten) eingehende Anrufe von anderen VSS-Teilnehmern (z. b. Writer oder VSS-Dienst) zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="d614a-118">Requesters need to be aware that when their process acts as a server (for example, allowing writers to modify the Backup Components Document), they must allow incoming calls from other VSS participants, such as writers or the VSS service.</span></span>

<span data-ttu-id="d614a-119">Standardmäßig lässt ein Windows-Prozess jedoch nur com-Clients zu, die in derselben Anmelde Sitzung (der Self-sid) ausgeführt werden oder unter dem lokalen System Konto ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d614a-119">However, by default, a Windows process will allow only COM clients that are running under the same logon session (the SELF SID) or running under the Local System account.</span></span> <span data-ttu-id="d614a-120">Dies ist ein potenzielles Problem, da diese Standardwerte für die VSS-Infrastruktur nicht ausreichen.</span><span class="sxs-lookup"><span data-stu-id="d614a-120">This is a potential problem because these defaults are not adequate for the VSS infrastructure.</span></span> <span data-ttu-id="d614a-121">Writer können z. b. als "Sicherungs Operator"-Benutzerkonto ausgeführt werden, das sich weder in derselben Anmelde Sitzung wie der requestprozess noch in einem lokalen System Konto befindet.</span><span class="sxs-lookup"><span data-stu-id="d614a-121">For example, writers might run as a "Backup Operator" user account that is neither in the same logon session as the requester process nor a Local System account.</span></span>

<span data-ttu-id="d614a-122">Um diese Art von Problem zu behandeln, kann jeder com-Server Prozess besser steuern, ob ein RPC-oder com-Client eine durch den Server implementierte com-Methode (in diesem Fall eine anfordernde Person) ausführen darf (in diesem Fall ein Anforderer), indem er [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) verwendet, um eine Prozess weite "Standard-com-Zugriffs Überprüfung"</span><span class="sxs-lookup"><span data-stu-id="d614a-122">To handle this type of problem, every COM server process can exercise further control over whether an RPC or COM client is allowed to perform a COM method implemented by the server (a requester in this case) by using [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set a process-wide "Default COM Access Check Permission".</span></span>

<span data-ttu-id="d614a-123">Anforderer kann explizit folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="d614a-123">Requesters can explicitly do the following:</span></span>

-   <span data-ttu-id="d614a-124">Ermöglicht allen Prozessen den Zugriff, um den Anforderer Prozess aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d614a-124">Allow all processes access to call into the requester process.</span></span>

    <span data-ttu-id="d614a-125">Diese Option ist möglicherweise für die Mehrheit der Anforderer geeignet und wird von anderen com-Servern verwendet – beispielsweise verwenden alle svchost-basierten Windows-Dienste diese Option bereits, ebenso wie alle com+-Dienste standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="d614a-125">This option may be adequate for the vast majority of requesters, and is used by other COM servers—for example, all SVCHOST-based Windows services are already using this option, as are all COM+ Services by default.</span></span>

    <span data-ttu-id="d614a-126">Das zulassen, dass alle Prozesse eingehende com-Aufrufe durchführen, ist nicht notwendigerweise eine Sicherheits Schwachstelle.</span><span class="sxs-lookup"><span data-stu-id="d614a-126">Allowing all processes to perform incoming COM calls is not necessarily a security weakness.</span></span> <span data-ttu-id="d614a-127">Ein Anforderer, der als com-Server fungiert, wie alle anderen com-Server, behält immer die Option bei, seine Clients für jede com-Methode zu autorisieren, die in seinem Prozess implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="d614a-127">A requester acting as a COM server, like all other COM servers, always retains the option to authorize its clients on every COM method implemented in its process.</span></span>

    <span data-ttu-id="d614a-128">Beachten Sie, dass die von VSS implementierten internen com-Rückrufe standardmäßig gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="d614a-128">Note that internal COM callbacks implemented by VSS are secured by default.</span></span>

    <span data-ttu-id="d614a-129">Um allen Prozessen den com-Zugriff auf einen Anforderer zuzulassen, können Sie einen **null** -Sicherheits Deskriptor als ersten Parameter von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)übergeben.</span><span class="sxs-lookup"><span data-stu-id="d614a-129">To allow all processes COM access to a requester, you can pass a **NULL** security descriptor as the first parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="d614a-130">(Beachten Sie, dass **CoInitializeSecurity** höchstens einmal für den gesamten Prozess aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="d614a-130">(Note that **CoInitializeSecurity** must be called at most once for the entire process.</span></span> <span data-ttu-id="d614a-131">Weitere Informationen zu **CoInitializeSecurity** -aufrufen finden Sie in der com-Dokumentation oder in MSDN.</span><span class="sxs-lookup"><span data-stu-id="d614a-131">Please see the COM documentation or MSDN for more information on **CoInitializeSecurity** calls.)</span></span>

    <span data-ttu-id="d614a-132">Im folgenden Codebeispiel wird gezeigt, wie ein Anforderer [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 8 und Windows Server 2012 und höher aufruft, um mit VSS für Remote Dateifreigaben (rvss) kompatibel zu sein:</span><span class="sxs-lookup"><span data-stu-id="d614a-132">The following code example shows how a requester should call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 8 and Windows Server 2012 and later, in order to be compatible with VSS for remote file shares (RVSS):</span></span>

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IMPERSONATE,   //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_STATIC,                   //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    <span data-ttu-id="d614a-133">Wenn Sie die Sicherheit der com-Ebene eines Anforderers mit [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)explizit festlegen, sollten Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="d614a-133">When explicitly setting a requester's COM level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="d614a-134">Legen Sie für die Authentifizierungs Stufe mindestens **die \_ \_ \_ \_ Pkt- \_ Integrität der RPC-C-authn-Ebene** fest.</span><span class="sxs-lookup"><span data-stu-id="d614a-134">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**.</span></span> <span data-ttu-id="d614a-135">Um die Sicherheit zu erhöhen, sollten Sie die Verwendung von **RPC \_ C \_ authn \_ Level \_ Pkt \_ Privacy** in Erwägung gezogen</span><span class="sxs-lookup"><span data-stu-id="d614a-135">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>
    -   <span data-ttu-id="d614a-136">Legen Sie die Identitätswechsel Ebene auf **RPC- \_ C- \_ IMP- \_ Ebene \_** Identitätswechsel fest.</span><span class="sxs-lookup"><span data-stu-id="d614a-136">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IMPERSONATE**.</span></span>
    -   <span data-ttu-id="d614a-137">Legen Sie die Sicherheitsfunktionen für die Sicherheit auf " **eoac \_ static**" fest.</span><span class="sxs-lookup"><span data-stu-id="d614a-137">Set the cloaking security capabilities to **EOAC\_STATIC**.</span></span> <span data-ttu-id="d614a-138">Weitere Informationen zum verzippen der Sicherheit finden Sie unter [Cloaking (Cloaking](../com/cloaking.md)).</span><span class="sxs-lookup"><span data-stu-id="d614a-138">For more information about cloaking security, see [Cloaking](../com/cloaking.md).</span></span>

    <span data-ttu-id="d614a-139">Im folgenden Codebeispiel wird gezeigt, wie ein Anforderer [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 7 und Windows Server 2008 R2 und früher aufruft (oder in Windows 8 und Windows Server 2012 und höher, wenn keine rvss-Kompatibilität erforderlich ist):</span><span class="sxs-lookup"><span data-stu-id="d614a-139">The following code example shows how a requester should call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 7 and Windows Server 2008 R2 and earlier (or in Windows 8 and Windows Server 2012 and later, if RVSS compatibility is not needed):</span></span>

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IDENTIFY,      //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_NONE,                     //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    <span data-ttu-id="d614a-140">Wenn Sie die Sicherheit der com-Ebene eines Anforderers mit [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)explizit festlegen, sollten Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="d614a-140">When explicitly setting a requester's COM level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="d614a-141">Legen Sie die Authentifizierungs Ebene auf mindestens **RPC \_ C \_ authn \_ Level \_ Connect** fest.</span><span class="sxs-lookup"><span data-stu-id="d614a-141">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_CONNECT**.</span></span> <span data-ttu-id="d614a-142">Um die Sicherheit zu erhöhen, sollten Sie die Verwendung von **RPC \_ C \_ authn \_ Level \_ Pkt \_ Privacy** in Erwägung gezogen</span><span class="sxs-lookup"><span data-stu-id="d614a-142">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>
    -   <span data-ttu-id="d614a-143">Legen Sie die Identitätswechsel Ebene auf **RPC \_ C \_ IMP- \_ Ebene \_ identifizieren** fest, es sei denn, der requestprozess muss den Identitätswechsel für bestimmte RPC-oder COM-Aufrufe zulassen, die nicht mit VSS verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="d614a-143">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IDENTIFY** unless the requester process needs to allow impersonation for specific RPC or COM calls that are unrelated to VSS.</span></span>

-   <span data-ttu-id="d614a-144">Erlauben Sie nur angegebenen Prozessen den Zugriff, um den requestprozess aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d614a-144">Allow only specified processes access to call into the requester process.</span></span>

    <span data-ttu-id="d614a-145">Ein com-Server (z. b. ein Anforderer), der [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) mit einem Sicherheits Deskriptor ungleich **null** als ersten Parameter aufruft, kann den Deskriptor verwenden, um nur eingehende Aufrufe von Benutzern zu akzeptieren, die zu einem bestimmten Satz von Konten gehören.</span><span class="sxs-lookup"><span data-stu-id="d614a-145">A COM server (such as a requester) that is calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) with a non-**NULL** security descriptor as the first parameter can use the descriptor to configure itself to accept incoming calls only from users that belong to a specific set of accounts.</span></span>

    <span data-ttu-id="d614a-146">Ein Anforderer muss sicherstellen, dass com-Clients, die unter gültigen Benutzern ausgeführt werden, autorisiert sind, seinen Prozess aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d614a-146">A requester must ensure that COM clients running under valid users are authorized to call into its process.</span></span> <span data-ttu-id="d614a-147">Ein Anforderer, der eine Sicherheits Beschreibung im ersten Parameter angibt, muss den folgenden Benutzern erlauben, eingehende Aufrufe in den requestprozess auszuführen:</span><span class="sxs-lookup"><span data-stu-id="d614a-147">A requester that specifies a Security Descriptor in the first parameter must allow the following users to perform incoming calls into the requester process:</span></span>

    -   <span data-ttu-id="d614a-148">Lokales System</span><span class="sxs-lookup"><span data-stu-id="d614a-148">Local System</span></span>
    -   <span data-ttu-id="d614a-149">Lokaler Dienst</span><span class="sxs-lookup"><span data-stu-id="d614a-149">Local Service</span></span>

        <span data-ttu-id="d614a-150">**Windows XP:** Dieser Wert wird bis Windows Server 2003 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d614a-150">**Windows XP:** This value is not supported until Windows Server 2003.</span></span>

    -   <span data-ttu-id="d614a-151">Netzwerkdienst</span><span class="sxs-lookup"><span data-stu-id="d614a-151">Network Service</span></span>

        <span data-ttu-id="d614a-152">**Windows XP:** Dieser Wert wird bis Windows Server 2003 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d614a-152">**Windows XP:** This value is not supported until Windows Server 2003.</span></span>

    -   <span data-ttu-id="d614a-153">Mitglieder der lokalen Gruppe "Administratoren"</span><span class="sxs-lookup"><span data-stu-id="d614a-153">Members of the local Administrators group</span></span>
    -   <span data-ttu-id="d614a-154">Mitglieder der Gruppe der lokalen Sicherungs Operatoren</span><span class="sxs-lookup"><span data-stu-id="d614a-154">Members of the local Backup Operators group</span></span>
    -   <span data-ttu-id="d614a-155">Besondere Benutzer, die am folgenden Registrierungs Speicherort angegeben sind, mit "1" als reg \_ DWORD-Wert</span><span class="sxs-lookup"><span data-stu-id="d614a-155">Special users that are specified in the registry location below, with "1" as their REG\_DWORD value</span></span>

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a><span data-ttu-id="d614a-156">Explizites Steuern des Benutzerkonto Zugriffs auf einen Anforderer</span><span class="sxs-lookup"><span data-stu-id="d614a-156">Explicitly Controlling User Account Access to a Requester</span></span>

<span data-ttu-id="d614a-157">Es gibt Fälle, in denen der Zugriff auf einen Anforderer auf Prozesse beschränkt wird, die als lokales System oder unter den Gruppen "lokale Administratoren" oder "lokale Sicherungs Operatoren" ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d614a-157">There are cases where restricting access to a requester to processes running as Local System, or under the local Administrators or local Backup Operators groups, may be too restrictive.</span></span>

<span data-ttu-id="d614a-158">Beispielsweise muss ein angegebener Anforderer Prozess normalerweise nicht unter einem Administrator Konto oder einem Sicherungs Operator Konto ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d614a-158">For example, a specified requester process might not ordinarily need to be run under an Administrator or Backup Operator account.</span></span> <span data-ttu-id="d614a-159">Aus Sicherheitsgründen wäre es am besten, die Prozess Privilegien nicht künstlich herauf zusetzen, um VSS zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d614a-159">For security reasons, it would be best not to artificially promote the processes privileges to support VSS.</span></span>

<span data-ttu-id="d614a-160">In diesen Fällen muss der **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** -Registrierungsschlüssel geändert werden, um VSS anzuweisen, dass ein angegebener Benutzer sicher ist, einen VSS-Anforderer auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d614a-160">In these cases, the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**VSS**\\**VssAccessControl** registry key must be modified to instruct VSS that a specified user is safe to run a VSS requester.</span></span>

<span data-ttu-id="d614a-161">Unter diesem Schlüssel müssen Sie einen Unterschlüssel erstellen, der denselben Namen hat wie das Konto, dem der Zugriff gewährt oder verweigert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d614a-161">Under this key, you must create a subkey that has the same name as the account that is to be granted or denied access.</span></span> <span data-ttu-id="d614a-162">Dieser Unterschlüssel muss auf einen der Werte in der folgenden Tabelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d614a-162">This subkey must be set to one of the values in the following table.</span></span>

| <span data-ttu-id="d614a-163">Wert</span><span class="sxs-lookup"><span data-stu-id="d614a-163">Value</span></span> | <span data-ttu-id="d614a-164">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d614a-164">Meaning</span></span>                                             |
|-------|-----------------------------------------------------|
| <span data-ttu-id="d614a-165">0</span><span class="sxs-lookup"><span data-stu-id="d614a-165">0</span></span>     | <span data-ttu-id="d614a-166">Verweigern Sie dem Benutzer den Zugriff auf Ihren Writer und den Anforderer.</span><span class="sxs-lookup"><span data-stu-id="d614a-166">Deny the user access to your writer and requester.</span></span>  |
| <span data-ttu-id="d614a-167">1</span><span class="sxs-lookup"><span data-stu-id="d614a-167">1</span></span>     | <span data-ttu-id="d614a-168">Gewähren Sie dem Benutzer Zugriff auf Ihren Writer.</span><span class="sxs-lookup"><span data-stu-id="d614a-168">Grant the user access to your writer.</span></span>               |
| <span data-ttu-id="d614a-169">2</span><span class="sxs-lookup"><span data-stu-id="d614a-169">2</span></span>     | <span data-ttu-id="d614a-170">Gewähren Sie dem Benutzer Zugriff auf Ihre Anforderer.</span><span class="sxs-lookup"><span data-stu-id="d614a-170">Grant the user access to your requester.</span></span>            |
| <span data-ttu-id="d614a-171">3</span><span class="sxs-lookup"><span data-stu-id="d614a-171">3</span></span>     | <span data-ttu-id="d614a-172">Gewähren Sie dem Benutzer Zugriff auf Ihren Writer und Anforderer.</span><span class="sxs-lookup"><span data-stu-id="d614a-172">Grant the user access to your writer and requester.</span></span> |



 

<span data-ttu-id="d614a-173">Im folgenden Beispiel wird der Zugriff auf das Konto "mydomain \\ myuser" gewährt:</span><span class="sxs-lookup"><span data-stu-id="d614a-173">The following example grants access to the "MyDomain\\MyUser" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 2<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="d614a-174">Dieser Mechanismus kann auch verwendet werden, um einen anderweitig zugelassenen Benutzer explizit daran zu hindern, eine VSS-Anforderer zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d614a-174">This mechanism can also be used to explicitly restrict an otherwise permitted user from running a VSS requester.</span></span> <span data-ttu-id="d614a-175">Im folgenden Beispiel wird der Zugriff auf das Konto "das Domänen \\ Administrator Konto" beschränkt:</span><span class="sxs-lookup"><span data-stu-id="d614a-175">The following example will restrict access from the "ThatDomain\\Administrator" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  ThatDomain\Administrator = 0<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="d614a-176">Der Benutzer, der Domänen \\ Administrator ist, kann keine VSS-Anforderer ausführen.</span><span class="sxs-lookup"><span data-stu-id="d614a-176">The user ThatDomain\\Administrator would not be able to run a VSS requester.</span></span>

## <a name="performing-a-file-backup-of-the-system-state"></a><span data-ttu-id="d614a-177">Ausführen einer Datei Sicherung des System Status</span><span class="sxs-lookup"><span data-stu-id="d614a-177">Performing a File Backup of the System State</span></span>

<span data-ttu-id="d614a-178">Wenn ein Anforderer die Systemstatus Sicherung durch Sicherung einzelner Dateien durchführt, anstatt ein Volumeabbild für die Sicherung zu verwenden, muss er die Funktionen [**findfirstdateinamew**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) und [**FindNextFile amew**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) zum Auflisten von festen Links für Dateien, die sich in den folgenden Verzeichnissen befinden, aufzählen:</span><span class="sxs-lookup"><span data-stu-id="d614a-178">If a requester performs system-state backup by backing up individual files instead of using a volume image for the backup, it must call the [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) and [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) functions to enumerate hard links on files that are located in the following directories:</span></span>

-   <span data-ttu-id="d614a-179">Windows \\ system32 \\ WDI \\ perftrack</span><span class="sxs-lookup"><span data-stu-id="d614a-179">Windows\\system32\\WDI\\perftrack</span></span>\\
-   <span data-ttu-id="d614a-180">Windows- \\ WinSxS</span><span class="sxs-lookup"><span data-stu-id="d614a-180">Windows\\WINSXS</span></span>\\

<span data-ttu-id="d614a-181">Auf diese Verzeichnisse kann nur von Mitgliedern der Gruppe "Administratoren" zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="d614a-181">These directories can only be accessed by members of the Administrators group.</span></span> <span data-ttu-id="d614a-182">Aus diesem Grund muss ein solcher Anforderer unter dem Systemkonto oder einem Benutzerkonto ausgeführt werden, das Mitglied der Gruppe "Administratoren" ist.</span><span class="sxs-lookup"><span data-stu-id="d614a-182">For this reason, such a requester must run under the system account or a user account that is a member of the Administrators group.</span></span>

<span data-ttu-id="d614a-183">**Windows XP und Windows Server 2003:** Die Funktionen [**findfirstdateinamew**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) und [**FindNextFile amew**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) werden bis Windows Vista und Windows Server 2008 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d614a-183">**Windows XP and Windows Server 2003:** The [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) and [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) functions are not supported until Windows Vista and Windows Server 2008.</span></span>

 

 
