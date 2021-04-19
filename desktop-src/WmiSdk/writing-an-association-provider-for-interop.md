---
description: Ein Zuordnungs Anbieter bietet einen Mechanismus zum Registrieren von Profilen und zum Zuordnen von Profilen zu Profilen, die in verschiedenen Namespaces implementiert werden.
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: Schreiben eines Zuordnungs Anbieters für Interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f38f09a5c5771fe7fd04909f8247834b646ad1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106370482"
---
# <a name="writing-an-association-provider-for-interop"></a><span data-ttu-id="b6d1f-103">Schreiben eines Zuordnungs Anbieters für Interop</span><span class="sxs-lookup"><span data-stu-id="b6d1f-103">Writing an Association Provider for Interop</span></span>

<span data-ttu-id="b6d1f-104">Ein Zuordnungs Anbieter bietet einen Mechanismus zum Registrieren von Profilen und zum Zuordnen von Profilen zu Profilen, die in verschiedenen Namespaces implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-104">An association provider provides a mechanism to register profiles and associate them with profiles that are implemented in different namespaces.</span></span>

<span data-ttu-id="b6d1f-105">Zuordnungs Anbieter werden verwendet, um Standardprofile wie ein Power Profile verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-105">Association providers are used to expose standard profiles, like a power profile.</span></span> <span data-ttu-id="b6d1f-106">Dies erfolgt durch das Schreiben eines Zuordnungs Anbieters im Root/Interop-Namespace, der Zuordnungs Instanzen verfügbar macht, indem eine Klasse implementiert wird, die von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-106">This is accomplished by writing an association provider in the root/interop namespace that exposes association instances by implementing a class, which is derived from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span> <span data-ttu-id="b6d1f-107">Der Anbieter muss sowohl in root/Interop als auch in root/ <implemented> Namespace registriert werden, um die übergreifende übergreifende übergreifende Durchquerung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-107">The provider must be registered in both the root/interop and the root/<implemented> namespace to support cross namespace traversal.</span></span>

<span data-ttu-id="b6d1f-108">Der Zuordnungs Anbieter wird von Windows-Verwaltungsinstrumentation (WMI) geladen, wenn im Stamm-/Interop-Namespace eine Association-Abfrage ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-108">Windows Management Instrumentation (WMI) loads the association provider whenever an association query is run in the root/interop namespace.</span></span>

<span data-ttu-id="b6d1f-109">**So implementieren Sie einen Zuordnungs Anbieter für Interop**</span><span class="sxs-lookup"><span data-stu-id="b6d1f-109">**To implement an association provider for interop**</span></span>

1.  <span data-ttu-id="b6d1f-110">Leiten Sie eine Klasse von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)) ab, und erstellen Sie eine statische Instanz dieser abgeleiteten Klasse im \\ Namespace "root Interop".</span><span class="sxs-lookup"><span data-stu-id="b6d1f-110">Derive a class from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) and create a static instance of this derived class in the root\\interop namespace.</span></span> <span data-ttu-id="b6d1f-111">Die folgenden Eigenschaften müssen mindestens mit gültigen Werten weitergegeben werden:</span><span class="sxs-lookup"><span data-stu-id="b6d1f-111">At a minimum, the following properties must be propagated with valid values:</span></span>

    -   <span data-ttu-id="b6d1f-112">[**InstanceId**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6d1f-112">[**InstanceID**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="b6d1f-113">[**Registeredname**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6d1f-113">[**RegisteredName**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="b6d1f-114">[**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6d1f-114">[**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="b6d1f-115">[**Registeredversion**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6d1f-115">[**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))</span></span>

    <span data-ttu-id="b6d1f-116">Obwohl [**InstanceId**](/previous-versions//ee309375(v=vs.85)) die Instanz von **CIM \_ registeredprofile** eindeutig definiert, muss die Kombination von **registeredname**, **RegisteredOrganization** und **registeredversion** das registrierte Profil innerhalb des Bereichs der Organisation eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-116">Even though [**InstanceID**](/previous-versions//ee309375(v=vs.85)) uniquely defines the instance of the **CIM\_RegisteredProfile**, the combination of **RegisteredName**, **RegisteredOrganization**, and **RegisteredVersion** must uniquely identify the registered profile within the scope of the organization.</span></span> <span data-ttu-id="b6d1f-117">Weitere Informationen zu den einzelnen Eigenschaften finden Sie unter [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b6d1f-117">For more information about the individual properties, see [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

    <span data-ttu-id="b6d1f-118">Im folgenden Codebeispiel wird die Syntax für das Ableiten der **processprofile** -Klasse von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)) und Auffüllen der statischen Instanz beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-118">The following code example describes the syntax for deriving the **ProcessProfile** class from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) and populating the static instance.</span></span>

    ```syntax
    class ProcessProfile : CIM_RegisteredProfile
    {
    };

    instance of ProcessProfile as $PP
    {
         InstanceID = "Process";
         RegisteredName = "Process";
         RegisteredOrganization = "1"; // Set to "Other"
         OtherRegisteredOrganization = "Microsoft";
         RegisteredVersion = "1.0";
    };
    ```

    > [!Note]  
    > <span data-ttu-id="b6d1f-119">Für Windows-Clients muss die **RegisteredOrganization** -Eigenschaft auf 1 festgelegt sein, und die **otherregisteredorganization** -Eigenschaft muss auf "Microsoft" festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-119">For Windows clients, the **RegisteredOrganization** property must be set to 1 and the **OtherRegisteredOrganization** property set to "Microsoft".</span></span>

     

2.  <span data-ttu-id="b6d1f-120">Erstellen Sie einen Anbieter, der Zuordnungs Instanzen von [**CIM \_ elementanformstoprofile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-120">Create a provider that returns association instances of [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile).</span></span> <span data-ttu-id="b6d1f-121">Dieser Prozess umfasst zwei Schritte.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-121">This is a two-step process.</span></span>

    1.  <span data-ttu-id="b6d1f-122">Erstellen Sie eine Klasse, die von [**CIM \_ ElementConfiguration stoprofile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in den Interop-und Implementierungs Namespaces abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-122">Create a class that is derived from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in both the interop and implementation namespaces.</span></span> <span data-ttu-id="b6d1f-123">Da das gleiche Profil von verschiedenen Anbietern implementiert werden kann, sollte der Name der Klasse eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-123">Because the same profile can be implemented by different vendors, the name of the class should be unique.</span></span> <span data-ttu-id="b6d1f-124">Die empfohlene Benennungs Konvention ist " <Organization> \_ <ProductName> \_ <ClassName> \_ <Version> ".</span><span class="sxs-lookup"><span data-stu-id="b6d1f-124">The recommended naming convention is "<Organization>\_<ProductName>\_<ClassName>\_<Version>".</span></span> <span data-ttu-id="b6d1f-125">Entweder die **conformantstandard** -Eigenschaft oder die **managedelta** -Eigenschaft muss den **MSFT \_ targetNamespace** -Qualifizierer angeben, der den Namespace enthält, zu dem diese Klasse gehört.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-125">Either the **ConformantStandard** or the **ManagedElement** property must specify the **MSFT\_TargetNamespace** qualifier that contains the namespace to which this class belongs.</span></span>

        <span data-ttu-id="b6d1f-126">Im folgenden Codebeispiel wird die Syntax für das Ableiten der \_ Klasse "Microsoft Process \_ ElementConfiguration- \_ Klasse" von " [**CIM \_ ElementConfiguration stoprofile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) " im Namespace "root \\ Interop" beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-126">The following code example describes the syntax for deriving the Microsoft\_Process\_ElementConformsToProfile\_v1 class from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in the root\\interop namespace.</span></span> <span data-ttu-id="b6d1f-127">In diesem Beispiel verweist das von Win32- \_ Prozess verwaltete Element \\ mithilfe des **MSFT \_ targetNamespace** -Qualifizierers auf den root cimv2-Namespace.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-127">In this example, the Win32\_Process managed element references the root\\cimv2 namespace by using the **MSFT\_TargetNamespace** qualifier.</span></span>

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        <span data-ttu-id="b6d1f-128">Im folgenden Codebeispiel wird die Syntax für das Ableiten der Microsoft \_ Process \_ ElementConfiguration-Klasse "Element Configuration-Datei V1" \_ von [**CIM \_ ElementConfiguration Stop rofile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) im root \\ CIMV2-Namespace beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-128">The following code example describes the syntax for deriving the Microsoft\_Process\_ElementConformsToProfile\_v1 class from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in the root\\cimv2 namespace.</span></span> <span data-ttu-id="b6d1f-129">In diesem Beispiel verweist der standardmäßige [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)) -Standard mit dem \\ **MSFT \_ targetNamespace** -Qualifizierer auf den Stamm-Interop-Namespace.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-129">In this example, the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) conformant standard references the root\\interop namespace by using the **MSFT\_TargetNamespace** qualifier.</span></span>

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        <span data-ttu-id="b6d1f-130">Wenn der **MSFT \_ targetNamespace** -Qualifizierer für die Eigenschaft, die auf den implementierten Namespace verweist, nicht angegeben ist, funktioniert der **resultClass** -Filter der Anweisung "ASSOCIATORS of" nicht.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-130">If the **MSFT\_TargetNamespace** qualifier is not specified on the property that is referencing the implemented namespace, the **ResultClass** filter of "Associators of" statement will not work.</span></span> <span data-ttu-id="b6d1f-131">Wenn beispielsweise der **MSFT \_ targetNamespace** -Qualifizierer nicht angegeben ist, wird von der folgenden Windows PowerShell-Befehlszeile kein Objekt zurückgegeben: **Get-WMIObject-Query "ASSOCIATORS of {processprofile. InstanceId = ' Process '} WHERE resultClass = ' Win32 \_ Process '"**.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-131">For example, if the **MSFT\_TargetNamespace** qualifier is not specified, the following Windows PowerShell command-line will not return an object: **get-wmiobject -query "associators of {ProcessProfile.InstanceID='Process'} where resultclass='Win32\_Process'"**.</span></span>

        <span data-ttu-id="b6d1f-132">Der **MSFT \_ targetNamespace** -Qualifizierer kann nicht auf einen Namespace auf einem Remote Computer verweisen.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-132">The **MSFT\_TargetNamespace** qualifier cannot point to a namespace on a remote computer.</span></span> <span data-ttu-id="b6d1f-133">Der folgende Namespace wird z. b. nicht unterstützt: MSFT \_ targetNamespace ( \\ \\ \\ \\ <RemoteMachine> \\ \\ root \\ \\ Interop).</span><span class="sxs-lookup"><span data-stu-id="b6d1f-133">For example, the following namespace is not supported: MSFT\_TargetNamespace(\\\\\\\\<RemoteMachine>\\\\root\\\\interop).</span></span>

    2.  <span data-ttu-id="b6d1f-134">Schreiben Sie einen Anbieter, der Instanzen der erstellten abgeleiteten Klasse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-134">Write a provider that returns instances of the created derived class.</span></span> <span data-ttu-id="b6d1f-135">Weitere Informationen finden Sie unter [Schreiben eines Instanzanbieters](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b6d1f-135">For more information, see [Writing an Instance Provider](writing-an-instance-provider.md).</span></span> <span data-ttu-id="b6d1f-136">Wenn Sie auf Namespace übergreifende Instanzen zugreifen, müssen Sie möglicherweise auf die Sicherheitsebenen für den Client zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-136">When you access cross-namespace instances, you might have to access the security levels for the client.</span></span> <span data-ttu-id="b6d1f-137">Weitere Informationen finden Sie unter Annehmen der Identität [eines Clients](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="b6d1f-137">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

        <span data-ttu-id="b6d1f-138">Der Zuordnungs Anbieter sollte sowohl die [**IWbemServices. kreateingestanceenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) -Methode als auch die [**IWbemServices. GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) -Methode implementieren.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-138">The association provider should implement both the [**IWbemServices.CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) and [**IWbemServices.GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods.</span></span> <span data-ttu-id="b6d1f-139">Die Implementierung der [**IWbemServices.Execqueryasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) -Methode ist optional.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-139">Implementing the [**IWbemServices.ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method is optional.</span></span> <span data-ttu-id="b6d1f-140">Da der Zugriff auf diesen Anbieter sowohl über die Stamm \\ -Interop-als auch die Stamm- \\ <implemented> Namespaces möglich ist, sollte keine explizite Abhängigkeit von einem Namespace innerhalb des Anbieters vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-140">Because this provider can be accessed from both the root\\interop and the root\\<implemented> namespaces, there should not be an explicit dependency on a namespace inside the provider.</span></span>

3.  <span data-ttu-id="b6d1f-141">Registrieren Sie den Zuordnungs Anbieter sowohl im \\ stamminterop als auch in den \\ <implemented> Stammnamespaces.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-141">Register the association provider in both the root\\interop and the root\\<implemented> namespaces.</span></span> <span data-ttu-id="b6d1f-142">Weitere Informationen finden Sie unter [Registrieren eines Instanzanbieters](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b6d1f-142">For more information, see [Registering an Instance Provider](registering-an-instance-provider.md).</span></span>

    <span data-ttu-id="b6d1f-143">Im folgenden Codebeispiel wird die Syntax zum Registrieren des Zuordnungs Anbieters im \\ Namespace "root Interop" beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-143">The following code example describes the syntax to register the association provider in the root\\interop namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\interop")
    instance of __Win32Provider as $P
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $P;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

    <span data-ttu-id="b6d1f-144">Im folgenden Codebeispiel wird die Syntax zum Registrieren des Zuordnungs Anbieters im root \\ CIMV2-Namespace beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-144">The following code example describes the syntax to register the association provider in the root\\cimv2 namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\cimv2")
    instance of __Win32Provider as $R
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $R;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

4.  <span data-ttu-id="b6d1f-145">Platzieren Sie das Schema für die [**CIM- \_ elementumstoprofile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in den implementierten Namespace.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-145">Place the schema for the [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) into the implemented namespace.</span></span> <span data-ttu-id="b6d1f-146">Für Windows-Clients ist dies die Datei "Interop. mof", die sich im Ordner "% SystemRoot% \\ system32 \\ WBEM" befindet.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-146">For Windows clients this is the interop.mof file that is located in the %systemroot%\\system32\\wbem folder.</span></span>
5.  <span data-ttu-id="b6d1f-147">Implementieren Sie die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle für Ihren Anbieter.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-147">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="b6d1f-148">WMI verwendet [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) , um einen Anbieter zu laden und zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-148">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="b6d1f-149">Die [**IWbemProviderInit.Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) -Methode sollte so implementiert werden, dass Sie für zwei verschiedene Namespaces aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6d1f-149">The [**IWbemProviderInit.Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) method should be implemented in a way that allows it to be called for two different namespaces.</span></span> <span data-ttu-id="b6d1f-150">Weitere Informationen finden Sie unter [Initialisieren eines Anbieters](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b6d1f-150">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6d1f-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b6d1f-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6d1f-152">**CIM \_ elementreformstoprofile**</span><span class="sxs-lookup"><span data-stu-id="b6d1f-152">**CIM\_ElementConformsToProfile**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

<span data-ttu-id="b6d1f-153">[**CIM- \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6d1f-153">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b6d1f-154">Schreiben eines Instanzanbieters</span><span class="sxs-lookup"><span data-stu-id="b6d1f-154">Writing an Instance Provider</span></span>](writing-an-instance-provider.md)
</dt> <dt>

[<span data-ttu-id="b6d1f-155">Registrieren eines Instanzanbieters</span><span class="sxs-lookup"><span data-stu-id="b6d1f-155">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> </dl>

 

 
