---
description: Der System Registrierungs Anbieter wird als Teil des WMI-Installationsvorgangs unter Windows registriert.
ms.assetid: ce5d0785-6e1b-411c-91df-f25767310530
ms.tgt_platform: multiple
title: Der System Registrierungs Anbieter wird registriert.
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d600872c4efab5560f4fd794cac63beb4365841c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359989"
---
# <a name="registering-the-system-registry-provider"></a><span data-ttu-id="6046d-103">Der System Registrierungs Anbieter wird registriert.</span><span class="sxs-lookup"><span data-stu-id="6046d-103">Registering the System Registry Provider</span></span>

<span data-ttu-id="6046d-104">Der System Registrierungs Anbieter wird als Teil des WMI-Installationsvorgangs unter Windows registriert.</span><span class="sxs-lookup"><span data-stu-id="6046d-104">The System Registry provider is registered as part of the WMI installation process on Windows.</span></span> <span data-ttu-id="6046d-105">Wenn Sie eine andere Plattform verwenden und den System Registrierungs Anbieter verwenden möchten, müssen Sie zuerst den Anbieter registrieren, indem Sie die nachstehend beschriebenen Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="6046d-105">If you are using another platform and want to use the System Registry provider, you must first register the provider yourself following the steps described below.</span></span>

<span data-ttu-id="6046d-106">Im folgenden Verfahren wird beschrieben, wie der System Registrierungs Anbieter registriert wird.</span><span class="sxs-lookup"><span data-stu-id="6046d-106">The following procedure describes how to register the System Registry provider.</span></span>

<span data-ttu-id="6046d-107">**So registrieren Sie den System Registrierungs Anbieter**</span><span class="sxs-lookup"><span data-stu-id="6046d-107">**To register the System Registry provider**</span></span>

1.  <span data-ttu-id="6046d-108">Registrieren Sie den Anbieter als com-Server.</span><span class="sxs-lookup"><span data-stu-id="6046d-108">Register the provider as a COM server.</span></span>

    <span data-ttu-id="6046d-109">Falls erforderlich, müssen Sie möglicherweise Registrierungseinträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="6046d-109">If necessary, you may need to create registry entries.</span></span> <span data-ttu-id="6046d-110">Dieser Vorgang gilt für alle com-Server und steht nicht im Zusammenhang mit WMI.</span><span class="sxs-lookup"><span data-stu-id="6046d-110">This process applies to all COM servers and is unrelated to WMI.</span></span> <span data-ttu-id="6046d-111">Weitere Informationen finden Sie in der [com](https://msdn.microsoft.com/library/aa139695.aspx) -Dokumentation im Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="6046d-111">For more information, see the [COM](https://msdn.microsoft.com/library/aa139695.aspx) documentation in the Microsoft Windows Software Development Kit (SDK).</span></span>

2.  <span data-ttu-id="6046d-112">Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, um die Implementierung des System Registrierungs Anbieters zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6046d-112">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class to describe the implementation of the System Registry provider.</span></span>

    <span data-ttu-id="6046d-113">Die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz beschreibt den Namen des Anbieters und dessen Klassen Bezeichner (**CLSID**).</span><span class="sxs-lookup"><span data-stu-id="6046d-113">The [**\_\_Win32Provider**](--win32provider.md) instance describes the name of the provider and its class identifier (**CLSID**).</span></span>

    <span data-ttu-id="6046d-114">Im folgenden Beispiel wird beschrieben, wie [**\_ \_ Win32Provider**](--win32provider.md) als Instanzeigenschaft, Ereignis oder Methoden Anbieter registriert wird.</span><span class="sxs-lookup"><span data-stu-id="6046d-114">The following example describes how to register [**\_\_Win32Provider**](--win32provider.md) as an instance property, event, or method provider.</span></span>

    ``` syntax
    // Instance provider
    instance of __Win32Provider as $InstProv
    {
        Name    = "RegProv" ;
        ClsId   = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}" ;
    };    
    // Property provider 
    instance of __Win32Provider as $PropProv 
    {
        Name = "RegPropProv"; 
        Clsid = "{72967901-68EC-11d0-B729-00AA0062CBB7}"; 
    }; 
    // Event provider
    instance of __Win32Provider as $RegEvent
    {
        Name = "RegistryEventProvider";
        Clsid = "{fa77a74e-e109-11d0-ad6e-00c04fd8fdff}";
    };
    instance of __Win32Provider as $RegMethod
    {
        Name = "RegistryMethodProvider";
        Clsid = "{44DE513E-60C2-11d3-AF33-00C04F79FEB1}";
    };
    ```

3.  <span data-ttu-id="6046d-115">Erstellen Sie eine oder mehrere Instanzen von Klassen, die von der [**\_ \_ providerregistration**](--providerregistration.md) -Klasse abgeleitet werden, um die logische Implementierung des System Registrierungs Anbieters zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6046d-115">Create one or more instances of classes derived from the [**\_\_ProviderRegistration**](--providerregistration.md) class to describe the logical implementation of the System Registry provider.</span></span>

    <span data-ttu-id="6046d-116">Abhängig von dem Zweck, für den Sie den System Registrierungs Anbieter registrieren, können Sie eine oder mehrere der folgenden Klassen erstellen.</span><span class="sxs-lookup"><span data-stu-id="6046d-116">Depending on the purpose for which you are registering the System Registry provider, you can create one or more of the following classes.</span></span>

    [<span data-ttu-id="6046d-117">**\_\_Instanceproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="6046d-117">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)

    [<span data-ttu-id="6046d-118">**\_\_Propertyproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="6046d-118">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)

    [<span data-ttu-id="6046d-119">**\_\_Eventproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="6046d-119">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)

    [<span data-ttu-id="6046d-120">**\_\_Methodproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="6046d-120">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)

    <span data-ttu-id="6046d-121">Im folgenden MOF-Codebeispiel wird beschrieben, wie Sie den System Registrierungs Anbieter als Instanz, Eigenschaft, Ereignis oder Methoden Anbieter registrieren können.</span><span class="sxs-lookup"><span data-stu-id="6046d-121">The following MOF code example describes how you can register the System Registry provider as an instance, property, event, or method provider.</span></span>

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $InstProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
        SupportsDelete = FALSE;
        SupportsEnumeration = TRUE;
    };
    instance of __PropertyProviderRegistration
    {
        Provider = $PropProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
    }; 
    instance of __EventProviderRegistration
    {
        Provider = $RegEvent;
        EventQueryList = {
                "select * from RegistryKeyChangeEvent",
                "select * from RegistryValueChangeEvent",
                "select * from RegistryTreeChangeEvent"};
    };
    // Method provider
    instance of __MethodProviderRegistration
    {
        Provider = $RegMethod;
    };
    ```

4.  <span data-ttu-id="6046d-122">Kompilieren Sie die MOF-Datei mit dem MOF-Compiler oder der [**imuf Compiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6046d-122">Compile the MOF file using the MOF compiler or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

<span data-ttu-id="6046d-123">Die regevent. MOF-Datei, die im WMI-Abschnitt des Windows SDK bereitgestellt wird, enthält die [**\_ \_ Win32Provider**](--win32provider.md) -und [**\_ \_ eventproviderregistration**](--eventproviderregistration.md) -Instanzen, die zum Registrieren des System Registrierungs Anbieters als Ereignis Anbieter erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6046d-123">The RegEvent.mof file provided in the WMI section of the Windows SDK contains the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventproviderregistration.md) instances necessary to register the System Registry provider as an event provider.</span></span> <span data-ttu-id="6046d-124">Weitere Informationen zum Registrieren eines Anbieters finden Sie unter [Registrieren eines Anbieters](registering-a-provider.md) und [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="6046d-124">For more information about registering a provider, see [Registering a Provider](registering-a-provider.md) and [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

 

 



