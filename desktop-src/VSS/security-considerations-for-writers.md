---
description: Die VSS-Infrastruktur erfordert, dass Writer-Prozesse sowohl als com-Clients als auch als Server fungieren können.
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: Sicherheitsüberlegungen für Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6f88243adbd62d928170a86ed57b91cbebe134
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347107"
---
# <a name="security-considerations-for-writers"></a><span data-ttu-id="467fb-103">Sicherheitsüberlegungen für Writer</span><span class="sxs-lookup"><span data-stu-id="467fb-103">Security Considerations for Writers</span></span>

<span data-ttu-id="467fb-104">Die VSS-Infrastruktur erfordert, dass Writer-Prozesse sowohl als com-Clients als auch als Server fungieren können.</span><span class="sxs-lookup"><span data-stu-id="467fb-104">The VSS infrastructure requires writer processes to be able to function both as COM clients and as servers.</span></span>

<span data-ttu-id="467fb-105">Wenn Sie als Server fungieren, machen VSS Writer com-Schnittstellen verfügbar (z. b. die VSS-Ereignishandler wie [**CVssWriter: onidentifizieren**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) und empfangen von eingehenden com-Aufrufen von VSS-Prozessen (z. b. anfordernde Personen und VSS-Dienst) oder RPC-Aufrufen von Prozessen, die sich außerhalb von VSS befinden, normalerweise wenn diese Prozesse VSS-Ereignisse generieren (z. b. Wenn ein Anforderer [**IVssBackupComponents:: gatherbeschreimetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)aufruft)</span><span class="sxs-lookup"><span data-stu-id="467fb-105">When acting as servers, VSS writers expose COM interfaces (for example, the VSS event handlers such as [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) and receive incoming COM calls from VSS processes (such as requesters and the VSS service) or RPC calls from processes that are external to VSS, typically when these processes generate VSS events (for example, when a requester calls [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)).</span></span> <span data-ttu-id="467fb-106">Aus diesem Grund muss ein VSS Writer sicher verwalten, welche com-Clients eingehende com-Aufrufe in seinem Prozess durchführen können.</span><span class="sxs-lookup"><span data-stu-id="467fb-106">Therefore, a VSS writer needs to securely manage which COM clients are able to make incoming COM calls into its process.</span></span>

<span data-ttu-id="467fb-107">Ebenso können VSS-Writer auch als com-Clients fungieren und ausgehende com-Aufrufe von Rückrufen, die von der VSS-Infrastruktur bereitgestellt werden, oder RPC-Aufrufe an externe Prozesse von VSS ausführen.</span><span class="sxs-lookup"><span data-stu-id="467fb-107">Similarly, VSS writers may also act as COM clients, making outgoing COM calls to callbacks supplied by the VSS infrastructure or RPC calls to processes that are external to VSS.</span></span> <span data-ttu-id="467fb-108">Diese Rückrufe, die entweder von einer Sicherungs Anwendung oder vom VSS-Dienst bereitgestellt werden, ermöglichen es dem Writer, Aufgaben auszuführen, z. b. das Aktualisieren des Sicherungs Komponenten Dokuments über die [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="467fb-108">These callbacks that are provided either by a backup application or by the VSS service allow the writer to perform tasks such as updating the Backup Components Document through the [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface.</span></span> <span data-ttu-id="467fb-109">Daher müssen die VSS-Sicherheitseinstellungen Writer das Ausführen von ausgehenden com-aufrufen in andere VSS-Prozesse ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="467fb-109">Therefore, VSS security settings must allow writers to make outgoing COM calls into other VSS processes.</span></span>

<span data-ttu-id="467fb-110">Der einfachste Mechanismus zum Verwalten von Writer-Sicherheitsproblemen umfasst die richtige Auswahl des Benutzerkontos, unter dem es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="467fb-110">The simplest mechanism for managing writer security issues involves the proper selection of the user account under which it runs.</span></span> <span data-ttu-id="467fb-111">Ein Writer muss in der Regel unter einem Benutzer ausgeführt werden, der Mitglied der Gruppe "Administratoren" oder der Gruppe "Sicherungs-Operatoren" ist, oder er muss als lokales System Konto ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="467fb-111">A writer typically needs to run under a user who is a member of either the Administrators group or the Backup Operators group, or it needs to run as the Local System account.</span></span>

<span data-ttu-id="467fb-112">Wenn ein Writer als com-Client fungiert und dieser nicht unter diesen Konten ausgeführt wird, wird ein beliebiger com-Befehl standardmäßig automatisch mit **E \_ AccessDenied** abgelehnt, ohne dass die Implementierung der com-Methode erfolgt.</span><span class="sxs-lookup"><span data-stu-id="467fb-112">By default, when a writer is acting as a COM client, if it does not run under these accounts, any COM call it makes is automatically rejected with **E\_ACCESSDENIED** without even getting to the COM method implementation.</span></span>

## <a name="disabling-com-exception-handling"></a><span data-ttu-id="467fb-113">Deaktivieren der com-Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="467fb-113">Disabling COM Exception Handling</span></span>

<span data-ttu-id="467fb-114">Wenn Sie einen Writer entwickeln, legen Sie das Flag com comglb \_ Exception \_ donot \_ handle Global Options fest, um die com-Ausnahmebehandlung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="467fb-114">When developing a writer, set the COM COMGLB\_EXCEPTION\_DONOT\_HANDLE global options flag to disable COM exception handling.</span></span> <span data-ttu-id="467fb-115">Dies ist wichtig, da durch die com-Ausnahmebehandlung schwerwiegende Fehler in einer VSS-Anwendung maskiert werden können.</span><span class="sxs-lookup"><span data-stu-id="467fb-115">It is important to do this because COM exception handling can mask fatal errors in a VSS application.</span></span> <span data-ttu-id="467fb-116">Der Fehler, der maskiert wird, kann den Prozess in einem instabilen und unvorhersehbaren Zustand belassen, was zu Beschädigungen und hängen von Beschädigungen führen kann.</span><span class="sxs-lookup"><span data-stu-id="467fb-116">The error that is masked can leave the process in an unstable and unpredictable state, which can lead to corruptions and hangs.</span></span> <span data-ttu-id="467fb-117">Weitere Informationen zu diesem Flag finden Sie unter [iglobaloptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span><span class="sxs-lookup"><span data-stu-id="467fb-117">For more information about this flag, see [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span></span>

## <a name="setting-writer-default-com-access-check-permission"></a><span data-ttu-id="467fb-118">Festlegen der com-Standard Zugriffs Überprüfung-Berechtigung für Writer</span><span class="sxs-lookup"><span data-stu-id="467fb-118">Setting Writer Default COM Access Check Permission</span></span>

<span data-ttu-id="467fb-119">Writer müssen sich bewusst sein, dass Sie, wenn Ihre Prozesse als Server fungieren (z. b. zum Verarbeiten von VSS-Ereignissen), eingehende Aufrufe von anderen VSS-Teilnehmern zulassen müssen, z. b. Anforderer oder VSS-Dienst.</span><span class="sxs-lookup"><span data-stu-id="467fb-119">Writers need to be aware that when their processes act as a server (for example, to handle VSS events), they must allow incoming calls from other VSS participants, such as requesters or the VSS service.</span></span>

<span data-ttu-id="467fb-120">Standardmäßig lässt ein Prozess jedoch nur com-Clients zu, die in derselben Anmelde Sitzung ausgeführt werden, oder unter dem lokalen System Konto.</span><span class="sxs-lookup"><span data-stu-id="467fb-120">However, by default, a process will allow only COM clients that are running under the same logon session the SELF SID) or running under the Local System account.</span></span> <span data-ttu-id="467fb-121">Dies ist ein potenzielles Problem, da diese Standardwerte nicht ausreichen, um die VSS-Infrastruktur zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="467fb-121">This is a potential problem because these defaults are not sufficient to support the VSS infrastructure.</span></span> <span data-ttu-id="467fb-122">Beispielsweise können Anforderer als Benutzerkonto "Sicherungs Operator" ausgeführt werden, das sich weder in derselben Anmelde Sitzung wie der Schreiber Prozess noch in einem lokalen System Konto befindet.</span><span class="sxs-lookup"><span data-stu-id="467fb-122">For example, requesters may run as a "Backup Operator" user account that is neither in the same logon session as the writer process nor a Local System account.</span></span>

<span data-ttu-id="467fb-123">Um diese Art von Problem zu behandeln, kann jeder com-Server Prozess besser steuern, ob ein RPC-oder com-Client eine com-Methode ausführen darf (in diesem Fall ein Writer), indem er [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) zum Festlegen einer Prozess weiten Standard-com-Zugriffs Überprüfung-Berechtigung verwendet.</span><span class="sxs-lookup"><span data-stu-id="467fb-123">To handle this type of problem, every COM server process can exercise further control over whether an RPC or COM client is allowed to perform a COM method the server (a writer in this case) implements by using [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set a process-wide default COM access check permission.</span></span>

<span data-ttu-id="467fb-124">Writer können explizit folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="467fb-124">Writers can explicitly do the following:</span></span>

-   <span data-ttu-id="467fb-125">Ermöglicht allen Prozessen den Zugriff, um den Schreibprozess aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="467fb-125">Allow all processes access to call into the writer process.</span></span>

    <span data-ttu-id="467fb-126">Diese Option ist möglicherweise für viele Writer geeignet und wird von anderen com-Servern verwendet – z. b. werden alle svchost-basierten Windows-Dienste diese Option bereits verwenden, ebenso wie alle com+-Dienste standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="467fb-126">This option may be adequate for many writers, and is used by other COM servers—for example, all SVCHOST-based Windows services are already using this option, as are all COM+ Services by default.</span></span>

    <span data-ttu-id="467fb-127">Das zulassen, dass alle Prozesse eingehende com-Aufrufe durchführen, ist nicht notwendigerweise eine Sicherheits Schwachstelle.</span><span class="sxs-lookup"><span data-stu-id="467fb-127">Allowing all processes to perform incoming COM calls is not necessarily a security weakness.</span></span> <span data-ttu-id="467fb-128">Ein Writer, der als com-Server fungiert, wie alle anderen com-Server, behält immer die Option bei, seine Clients für jede in seinem Prozess implementierte com-Methode zu autorialisieren.</span><span class="sxs-lookup"><span data-stu-id="467fb-128">A writer acting as a COM server, like all other COM servers, always retains the option of authorizing its clients on every COM method implemented in its process.</span></span>

    <span data-ttu-id="467fb-129">Um allen Prozessen den com-Zugriff auf einen Writer zu ermöglichen, können Sie einen **null** -Sicherheits Deskriptor als ersten Parameter von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)übergeben.</span><span class="sxs-lookup"><span data-stu-id="467fb-129">To allow all processes COM access to a writer, you can pass a **NULL** security descriptor as the first parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="467fb-130">(Beachten Sie, dass **CoInitializeSecurity** höchstens einmal für den gesamten Prozess aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="467fb-130">(Note that **CoInitializeSecurity** must be called at most once for the entire process.</span></span> <span data-ttu-id="467fb-131">Weitere Informationen zu **CoInitializeSecurity** finden Sie in der com-Dokumentation.)</span><span class="sxs-lookup"><span data-stu-id="467fb-131">Please see the COM documentation for more details on **CoInitializeSecurity**.)</span></span>

    <span data-ttu-id="467fb-132">Im folgenden finden Sie ein Codebeispiel, das einen [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)-aufrufswert enthält:</span><span class="sxs-lookup"><span data-stu-id="467fb-132">The following is a code example that includes a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):</span></span>

    ``` syntax
    // Initialize COM security.
    hr = CoInitializeSecurity(
           NULL,                          // PSECURITY_DESCRIPTOR          pSecDesc,
           -1,                            // LONG                          cAuthSvc,
           NULL,                          // SOLE_AUTHENTICATION_SERVICE  *asAuthSvc,
           NULL,                          // void                         *pReserved1,
           RPC_C_AUTHN_LEVEL_PKT_PRIVACY, // DWORD                         dwAuthnLevel,
           RPC_C_IMP_LEVEL_IDENTIFY,      // DWORD                         dwImpLevel,
           NULL,                          // void                         *pAuthList,
           EOAC_NONE,                     // DWORD                         dwCapabilities,
           NULL                           // void                         *pReserved3
        );
    ```

    <span data-ttu-id="467fb-133">Wenn Sie die Sicherheit eines Writers auf com-Ebene mit [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)explizit festlegen, sollten Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="467fb-133">When explicitly setting a writer's COM-level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="467fb-134">Legen Sie die Authentifizierungs Ebene auf mindestens **RPC \_ C \_ authn \_ Level \_ Connect** fest.</span><span class="sxs-lookup"><span data-stu-id="467fb-134">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_CONNECT**.</span></span>

        <span data-ttu-id="467fb-135">Um die Sicherheit zu erhöhen, sollten Sie die Verwendung von **RPC \_ C \_ authn \_ Level \_ Pkt \_ Privacy** in Erwägung gezogen</span><span class="sxs-lookup"><span data-stu-id="467fb-135">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>

    -   <span data-ttu-id="467fb-136">Legen Sie die Identitätswechsel Ebene auf **RPC \_ C \_ IMP- \_ Ebene \_ identifizieren** fest, es sei denn, der Schreiber Prozess muss den Identitätswechsel für bestimmte RPC-oder COM-Aufrufe zulassen, die nicht mit VSS verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="467fb-136">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IDENTIFY** unless the writer process needs to allow impersonation for specific RPC or COM calls that are unrelated to VSS.</span></span>

-   <span data-ttu-id="467fb-137">Erlauben Sie nur angegebenen Prozessen den Zugriff, um den Writer-Prozess aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="467fb-137">Allow only specified processes access to call into the writer process.</span></span>

    <span data-ttu-id="467fb-138">Ein com-Server (z. b. ein Writer), der [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) mit einem Sicherheits Deskriptor ungleich **null** aufruft, kann den Deskriptor verwenden, um nur eingehende Aufrufe von Benutzern zu akzeptieren, die zu einem bestimmten Satz von Konten gehören.</span><span class="sxs-lookup"><span data-stu-id="467fb-138">A COM server (such as a writer) that is calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) with a non-**NULL** security descriptor can use the descriptor to configure itself to accept incoming calls only from users that belong to a specific set of accounts.</span></span>

    <span data-ttu-id="467fb-139">Ein Writer muss sicherstellen, dass com-Clients, die unter gültigen Benutzern ausgeführt werden, autorisiert sind, den Prozess aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="467fb-139">A writer must ensure that COM clients running under valid users are authorized to call into its process.</span></span> <span data-ttu-id="467fb-140">Ein Writer, der eine Sicherheits Beschreibung im ersten Parameter angibt, muss den folgenden Benutzern erlauben, eingehende Aufrufe in den requestprozess auszuführen:</span><span class="sxs-lookup"><span data-stu-id="467fb-140">A writer that specifies a Security Descriptor in the first parameter must allow the following users to perform incoming calls into the requester process:</span></span>

    -   <span data-ttu-id="467fb-141">Lokales System</span><span class="sxs-lookup"><span data-stu-id="467fb-141">Local System</span></span>
    -   <span data-ttu-id="467fb-142">Mitglieder der lokalen Gruppe "Administratoren"</span><span class="sxs-lookup"><span data-stu-id="467fb-142">Members of the local Administrators group</span></span>
    -   <span data-ttu-id="467fb-143">Mitglieder der Gruppe der lokalen Sicherungs Operatoren</span><span class="sxs-lookup"><span data-stu-id="467fb-143">Members of the local Backup Operators group</span></span>
    -   <span data-ttu-id="467fb-144">Das Konto, unter dem der Writer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="467fb-144">The account under which the writer is running</span></span>

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a><span data-ttu-id="467fb-145">Explizites Steuern des Benutzerkonto Zugriffs auf einen Writer</span><span class="sxs-lookup"><span data-stu-id="467fb-145">Explicitly Controlling User Account Access to a Writer</span></span>

<span data-ttu-id="467fb-146">Es gibt Fälle, in denen der Zugriff auf einen Writer auf Prozesse beschränkt wird, die als lokales System oder unter den lokalen Gruppen Administratoren oder lokale Sicherungs Operatoren ausgeführt werden, möglicherweise zu restriktiv.</span><span class="sxs-lookup"><span data-stu-id="467fb-146">There are cases where restricting access to a writer to processes running as Local System, or under the local Administrators or local Backup Operators local groups, may be too restrictive.</span></span>

<span data-ttu-id="467fb-147">Ein Writer-Prozess (z. b. ein nicht-System-Writer von Drittanbietern) muss normalerweise nicht unter einem Administrator-oder Sicherungs Operator Konto ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="467fb-147">For example, a writer process (perhaps a third-party non-system writer) might not ordinarily need to be run under an Administrator or Backup Operator account.</span></span> <span data-ttu-id="467fb-148">Aus Sicherheitsgründen wäre es am besten, die Berechtigungen des Prozesses zur Unterstützung von VSS nicht künstlich zu fördern.</span><span class="sxs-lookup"><span data-stu-id="467fb-148">For security reasons, it would be best not to artificially promote the process's privileges to support VSS.</span></span>

<span data-ttu-id="467fb-149">In diesen Fällen muss der **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** -Registrierungsschlüssel geändert werden, um VSS anzuweisen, dass ein bestimmter Benutzer sicher eine VSS Writer ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="467fb-149">In these cases, the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**VSS**\\**VssAccessControl** registry key must be modified to instruct VSS that a specified user is safe to run a VSS writer.</span></span>

<span data-ttu-id="467fb-150">Unter diesem Schlüssel müssen Sie einen Unterschlüssel erstellen, der denselben Namen hat wie das Konto, dem der Zugriff gewährt oder verweigert werden soll.</span><span class="sxs-lookup"><span data-stu-id="467fb-150">Under this key, you must create a subkey that has the same name as the account that is to be granted or denied access.</span></span> <span data-ttu-id="467fb-151">Dieser Unterschlüssel muss auf einen der Werte in der folgenden Tabelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="467fb-151">This subkey must be set to one of the values in the following table.</span></span>

| <span data-ttu-id="467fb-152">Wert</span><span class="sxs-lookup"><span data-stu-id="467fb-152">Value</span></span> | <span data-ttu-id="467fb-153">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="467fb-153">Meaning</span></span>                                             |
|-------|-----------------------------------------------------|
| <span data-ttu-id="467fb-154">0</span><span class="sxs-lookup"><span data-stu-id="467fb-154">0</span></span>     | <span data-ttu-id="467fb-155">Verweigern Sie dem Benutzer den Zugriff auf Ihren Writer und den Anforderer.</span><span class="sxs-lookup"><span data-stu-id="467fb-155">Deny the user access to your writer and requester.</span></span>  |
| <span data-ttu-id="467fb-156">1</span><span class="sxs-lookup"><span data-stu-id="467fb-156">1</span></span>     | <span data-ttu-id="467fb-157">Gewähren Sie dem Benutzer Zugriff auf Ihren Writer.</span><span class="sxs-lookup"><span data-stu-id="467fb-157">Grant the user access to your writer.</span></span>               |
| <span data-ttu-id="467fb-158">2</span><span class="sxs-lookup"><span data-stu-id="467fb-158">2</span></span>     | <span data-ttu-id="467fb-159">Gewähren Sie dem Benutzer Zugriff auf Ihre Anforderer.</span><span class="sxs-lookup"><span data-stu-id="467fb-159">Grant the user access to your requester.</span></span>            |
| <span data-ttu-id="467fb-160">3</span><span class="sxs-lookup"><span data-stu-id="467fb-160">3</span></span>     | <span data-ttu-id="467fb-161">Gewähren Sie dem Benutzer Zugriff auf Ihren Writer und Anforderer.</span><span class="sxs-lookup"><span data-stu-id="467fb-161">Grant the user access to your writer and requester.</span></span> |



 

<span data-ttu-id="467fb-162">Im folgenden Beispiel wird der Zugriff auf das Konto "mydomain \\ myuser" gewährt:</span><span class="sxs-lookup"><span data-stu-id="467fb-162">The following example grants access to the "MyDomain\\MyUser" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 1<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="467fb-163">Dieser Mechanismus kann auch verwendet werden, um einen anderweitig zugelassenen Benutzer explizit auf die Ausführung einer VSS Writer zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="467fb-163">This mechanism can also be used to explicitly restrict an otherwise permitted user from running a VSS writer.</span></span> <span data-ttu-id="467fb-164">Im folgenden Beispiel wird der Zugriff auf das Konto "das Domänen \\ Administrator Konto" beschränkt:</span><span class="sxs-lookup"><span data-stu-id="467fb-164">The following example will restrict access from the "ThatDomain\\Administrator" account:</span></span>

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

<span data-ttu-id="467fb-165">Der Benutzer, der Domänen \\ Administrator ist, kann keine VSS Writer ausführen.</span><span class="sxs-lookup"><span data-stu-id="467fb-165">The user ThatDomain\\Administrator would not be able to run a VSS writer.</span></span>

 

 
