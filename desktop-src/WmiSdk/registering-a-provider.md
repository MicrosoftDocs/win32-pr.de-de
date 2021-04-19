---
description: Vor der Implementierung des Anbieters sollten Sie zunächst Ihren Anbieter bei WMI registrieren. Beim Registrieren des Anbieters werden der Typ des Anbieters und die vom Anbieter unterstützten Klassen definiert. WMI kann nur auf registrierte Anbieter zugreifen.
ms.assetid: b0a1a11c-a8e8-4bc1-b286-fb9243667976
ms.tgt_platform: multiple
title: Registrieren eines Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53592ecb452de1b6071cbb8f59cfaaef42b57f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364054"
---
# <a name="registering-a-provider"></a><span data-ttu-id="11e85-105">Registrieren eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="11e85-105">Registering a Provider</span></span>

<span data-ttu-id="11e85-106">Vor der Implementierung des Anbieters sollten Sie zunächst Ihren Anbieter bei WMI registrieren.</span><span class="sxs-lookup"><span data-stu-id="11e85-106">Before implementing your provider, you should first register your provider with WMI.</span></span> <span data-ttu-id="11e85-107">Beim Registrieren des Anbieters werden der Typ des Anbieters und die vom Anbieter unterstützten Klassen definiert.</span><span class="sxs-lookup"><span data-stu-id="11e85-107">Registering the provider defines the type of the provider and the classes that the provider supports.</span></span> <span data-ttu-id="11e85-108">WMI kann nur auf registrierte Anbieter zugreifen.</span><span class="sxs-lookup"><span data-stu-id="11e85-108">WMI can only access registered providers.</span></span>

> [!Note]  
> <span data-ttu-id="11e85-109">Weitere Informationen zum Registrieren eines Mi-Anbieters finden Sie unter Gewusst [wie: Registrieren eines Mi-Anbieters](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).</span><span class="sxs-lookup"><span data-stu-id="11e85-109">For more information on registering an MI provider, see [How to: Register an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).</span></span>

 

<span data-ttu-id="11e85-110">Sie können den Anbieter Code schreiben, bevor Sie den Anbieter registrieren.</span><span class="sxs-lookup"><span data-stu-id="11e85-110">You can write your provider code before you register the provider.</span></span> <span data-ttu-id="11e85-111">Es ist jedoch sehr schwierig, einen Anbieter zu debuggen, der nicht bei WMI registriert ist.</span><span class="sxs-lookup"><span data-stu-id="11e85-111">However, it is very difficult to debug a provider that is not registered with WMI.</span></span> <span data-ttu-id="11e85-112">Wenn Sie die Schnittstellen für Ihren Anbieter ermitteln, können Sie auch den Zweck und die Struktur eines Anbieters gliedern.</span><span class="sxs-lookup"><span data-stu-id="11e85-112">Determining the interfaces for your provider also helps to outline the purpose and structure of a provider.</span></span> <span data-ttu-id="11e85-113">Daher hilft Ihnen die Registrierung Ihres Anbieters beim Entwerfen Ihres Anbieters.</span><span class="sxs-lookup"><span data-stu-id="11e85-113">Therefore, registering your provider helps you design your provider.</span></span>

<span data-ttu-id="11e85-114">Nur Administratoren können einen Anbieter registrieren oder löschen.</span><span class="sxs-lookup"><span data-stu-id="11e85-114">Only administrators can register or delete a provider.</span></span>

<span data-ttu-id="11e85-115">Ein Anbieter muss für alle unterschiedlichen Typen von Anbieter Funktionen registriert werden, die er ausführt.</span><span class="sxs-lookup"><span data-stu-id="11e85-115">A provider must be registered for all the different types of provider functions that it performs.</span></span> <span data-ttu-id="11e85-116">Fast alle Anbieter stellen Instanzen von Klassen bereit, die Sie definieren, aber Sie können auch Eigenschafts Daten, Methoden, Ereignisse oder Klassen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="11e85-116">Nearly all providers supply instances of classes they define, but they may also provide property data, methods, events, or classes.</span></span> <span data-ttu-id="11e85-117">Der Anbieter kann auch als Ereignisconsumeranbieter oder Leistungsindikatorenanbieter registriert werden.</span><span class="sxs-lookup"><span data-stu-id="11e85-117">The provider may also be registered as an event consumer provider or a performance counter provider.</span></span> <span data-ttu-id="11e85-118">Es wird empfohlen, dass Sie alle Anbieter Funktionen in einem Anbieter kombinieren, anstatt für jeden Typ viele separate Anbieter zu haben.</span><span class="sxs-lookup"><span data-stu-id="11e85-118">It is recommended that you combine all provider functionality in one provider rather than having many separate providers for each type.</span></span> <span data-ttu-id="11e85-119">Ein Beispiel hierfür ist der [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider), der Methoden und Instanzen bereitstellt, sowie der Anbieter für Daten [Träger Kontingente](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), der Instanzen, Methoden und Ereignisse bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="11e85-119">An example is the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which provides methods and instances, and the [Disk Quota provider](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), which supplies instances, methods, and events.</span></span>

<span data-ttu-id="11e85-120">Ein Anbieter muss für alle unterschiedlichen Typen von Anbieter Funktionen registriert werden, die er ausführt.</span><span class="sxs-lookup"><span data-stu-id="11e85-120">A provider must be registered for all the different types of provider functions that it performs.</span></span> <span data-ttu-id="11e85-121">Fast alle Anbieter stellen Instanzen von Klassen bereit, die Sie definieren, aber Sie können auch Eigenschafts Daten, Methoden, Ereignisse oder Klassen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="11e85-121">Nearly all providers supply instances of classes they define, but they may also provide property data, methods, events, or classes.</span></span> <span data-ttu-id="11e85-122">Der Anbieter kann auch als Ereignisconsumeranbieter oder Leistungsindikatorenanbieter registriert werden.</span><span class="sxs-lookup"><span data-stu-id="11e85-122">The provider may also be registered as an event consumer provider or a performance counter provider.</span></span>

<span data-ttu-id="11e85-123">Dieselbe Instanz von [**\_ \_ Win32Provider**](--win32provider.md) wird für jeden Registrierungstyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="11e85-123">The same instance of [**\_\_Win32Provider**](--win32provider.md) is used for each type of registration:</span></span>

-   [<span data-ttu-id="11e85-124">Registrieren eines Instanzanbieters</span><span class="sxs-lookup"><span data-stu-id="11e85-124">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
-   [<span data-ttu-id="11e85-125">Registrieren eines Klassen Anbieters</span><span class="sxs-lookup"><span data-stu-id="11e85-125">Registering a Class Provider</span></span>](registering-a-class-provider.md)
-   [<span data-ttu-id="11e85-126">Registrieren eines Methoden Anbieters</span><span class="sxs-lookup"><span data-stu-id="11e85-126">Registering a Method Provider</span></span>](registering-a-method-provider.md)
-   [<span data-ttu-id="11e85-127">Registrieren eines Ereignis Anbieters</span><span class="sxs-lookup"><span data-stu-id="11e85-127">Registering an Event Provider</span></span>](registering-an-event-provider.md)
-   [<span data-ttu-id="11e85-128">Registrieren eines Ereignisconsumeranbieters</span><span class="sxs-lookup"><span data-stu-id="11e85-128">Registering an Event Consumer Provider</span></span>](registering-an-event-consumer-provider.md)
-   [<span data-ttu-id="11e85-129">Erstellen eines Instanzanbieters in einen High-Performance-Anbieter</span><span class="sxs-lookup"><span data-stu-id="11e85-129">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a><span data-ttu-id="11e85-130">Beispiel: Erstellen und Registrieren einer Instanz eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="11e85-130">Example: Creating and Registering an Instance of a Provider</span></span>

<span data-ttu-id="11e85-131">Das folgende Beispiel zeigt eine MOF-Datei, die eine Instanz des [System Registrierungs Anbieters](/previous-versions/windows/desktop/regprov/system-registry-provider) im root cimv2-Namespace erstellt und registriert \\ .</span><span class="sxs-lookup"><span data-stu-id="11e85-131">The following example shows a MOF file that creates and registers an instance of the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider) in the root\\cimv2 namespace.</span></span> <span data-ttu-id="11e85-132">Er weist den Alias $reg dem Anbieter zu, um den für die Instanz-und Methoden Registrierungen erforderlichen langen Pfadnamen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="11e85-132">It assigns the alias $Reg to the provider to avoid the long pathname required in the instance and method registrations.</span></span> <span data-ttu-id="11e85-133">Weitere Informationen finden Sie unter [Erstellen eines Alias](creating-an-alias.md).</span><span class="sxs-lookup"><span data-stu-id="11e85-133">For more information, see [Creating an Alias](creating-an-alias.md).</span></span>

``` syntax
// Place the Registry provider in the root\cimv2 namespace
#pragma namespace("\\\\.\\ROOT\\cimv2")

// Create an instance of __Win32Provider
instance of __Win32Provider as $Reg
{
Name = "RegProv";        
CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
HostingModel = "NetworkServiceHost:LocalServiceHost";
};

// Register as an instance provider by
// creating an instance
// of __InstanceProviderRegistration
instance of __InstanceProviderRegistration
{
 provider = $Reg;
 SupportsDelete = FALSE;
 SupportsEnumeration = TRUE;
 SupportsGet = TRUE;
 SupportsPut = TRUE;
};

// Register as a method provider by
// creating an instance
// of __MethodProviderRegistration
instance of __MethodProviderRegistration
{
 provider = $Reg;
};

// Define the StdRegProv class
[dynamic: ToInstance, provider("RegProv")]
class StdRegProv
{
[implemented, static] uint32 CreateKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 DeleteKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 EnumKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[]);
[implemented, static] uint32 EnumValues(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[], 
 [OUT] sint32 Types[]);
[implemented, static] uint32 DeleteValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName);
 [implemented, static] uint32 SetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] uint32 uValue = 3);
[implemented, static] uint32 GetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint32 uValue);
[implemented, static] uint32 SetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "hello");
[implemented, static] uint32 GetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue[] = {"hello", "there"});
[implemented, static] uint32 GetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue[]);
[implemented, static] uint32 SetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "%path%");
[implemented, static] uint32 GetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetBinaryValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [in] uint8 uValue[] = {1, 2});
[implemented, static] uint32 GetBinaryValue(
 {IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint8 uValue[]);
[implemented, static] uint32 CheckAccess(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] uint32 uRequired = 3, 
 [OUT] boolean bGranted);
};
```

## <a name="example-registering-a-provider"></a><span data-ttu-id="11e85-134">Beispiel: Registrieren eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="11e85-134">Example: Registering a Provider</span></span>

<span data-ttu-id="11e85-135">Im folgenden Verfahren wird beschrieben, wie Sie einen-Anbieter registrieren.</span><span class="sxs-lookup"><span data-stu-id="11e85-135">The following procedure describes how to register a provider.</span></span>

<span data-ttu-id="11e85-136">**So registrieren Sie einen Anbieter**</span><span class="sxs-lookup"><span data-stu-id="11e85-136">**To register a provider**</span></span>

1.  <span data-ttu-id="11e85-137">Registrieren Sie den Anbieter als com-Server.</span><span class="sxs-lookup"><span data-stu-id="11e85-137">Register the provider as a COM server.</span></span>

    <span data-ttu-id="11e85-138">Falls erforderlich, müssen Sie möglicherweise Registrierungseinträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="11e85-138">If necessary, you may need to create registry entries.</span></span> <span data-ttu-id="11e85-139">Dieser Vorgang gilt für alle com-Server und steht nicht im Zusammenhang mit WMI.</span><span class="sxs-lookup"><span data-stu-id="11e85-139">This process applies to all COM servers and is unrelated to WMI.</span></span> <span data-ttu-id="11e85-140">Weitere Informationen finden Sie im Abschnitt zu com in der Dokumentation zum Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="11e85-140">For more information, see the COM section in the Microsoft Windows Software Development Kit (SDK) documentation.</span></span>

2.  <span data-ttu-id="11e85-141">Erstellen Sie eine MOF-Datei, die Instanzen von [**\_ \_ Win32Provider**](--win32provider.md) und eine Instanz einer Klasse enthält, die entweder direkt oder indirekt von [**\_ \_ providerregistration**](--providerregistration.md)(z. b. [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md)) abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="11e85-141">Create a MOF file that contains instances of [**\_\_Win32Provider**](--win32provider.md) and an instance of a class derived either directly or indirectly from [**\_\_ProviderRegistration**](--providerregistration.md), such as [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md).</span></span> <span data-ttu-id="11e85-142">Nur Administratoren können einen Anbieter registrieren oder löschen, indem Sie Instanzen von Klassen erstellen, die von **\_ \_ Win32Provider** oder [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="11e85-142">Only administrators can register or delete a provider by creating instances of classes derived from **\_\_Win32Provider** or [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>
3.  <span data-ttu-id="11e85-143">Legen Sie das [**hostingmodel**](--win32provider.md) in der Instanz von **\_ \_ Win32Provider** entsprechend den Werten in den [Hostingmodellen](provider-hosting-and-security.md)fest.</span><span class="sxs-lookup"><span data-stu-id="11e85-143">Set the [**HostingModel**](--win32provider.md) in the instance of **\_\_Win32Provider** according to the values in [Hosting models](provider-hosting-and-security.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="11e85-144">Wenn der Anbieter die hohen Berechtigungen des Kontos LocalSystem erfordert, sollte die Eigenschaft [**\_ \_ Win32Provider. hostingmodel**](--win32provider.md) auf networkservicehost festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="11e85-144">Unless the provider requires the high privileges of the LocalSystem account, the [**\_\_Win32Provider.HostingModel**](--win32provider.md) property should be set to "NetworkServiceHost".</span></span> <span data-ttu-id="11e85-145">Weitere Informationen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="11e85-145">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

     

    <span data-ttu-id="11e85-146">Das folgende MOF-Beispiel aus dem vollständigen Beispiel zeigt den Code, der eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="11e85-146">The following MOF example from the full example shows the code that creates an instance of [**\_\_Win32Provider**](--win32provider.md).</span></span>

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  <span data-ttu-id="11e85-147">Eine Instanz einer Klasse, die entweder direkt oder indirekt von [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet wird, um die logische Implementierung des Anbieters zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="11e85-147">An instance of a class derived either directly or indirectly from [**\_\_ProviderRegistration**](--providerregistration.md), to describe the logical implementation of the provider.</span></span> <span data-ttu-id="11e85-148">Ein Anbieter kann für verschiedene Arten von Funktionen registriert werden.</span><span class="sxs-lookup"><span data-stu-id="11e85-148">A provider can be registered for several different types of functionality.</span></span> <span data-ttu-id="11e85-149">Im obigen Beispiel wird RegProv als Instanz-und Methoden Anbieter registriert.</span><span class="sxs-lookup"><span data-stu-id="11e85-149">The example above registers RegProv as an instance and method provider.</span></span> <span data-ttu-id="11e85-150">Wenn RegProv die Funktionalität jedoch unterstützt, kann Sie auch als Eigenschaft oder Ereignis Anbieter registriert werden.</span><span class="sxs-lookup"><span data-stu-id="11e85-150">But if RegProv supports the functionality, it could also be registered as a property or event provider.</span></span> <span data-ttu-id="11e85-151">In der folgenden Tabelle werden die-Klassen aufgelistet, die Anbieter Funktionen registrieren.</span><span class="sxs-lookup"><span data-stu-id="11e85-151">The following table lists the classes that register provider functionality.</span></span>

    

    | <span data-ttu-id="11e85-152">Anbieter Registrierungs Klassen</span><span class="sxs-lookup"><span data-stu-id="11e85-152">Provider registration classes</span></span>                                                        | <span data-ttu-id="11e85-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11e85-153">Description</span></span>                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [<span data-ttu-id="11e85-154">**\_\_Instanceproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="11e85-154">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)           | <span data-ttu-id="11e85-155">Registriert einen [Instanzanbieter](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="11e85-155">Registers an [instance provider](registering-an-instance-provider.md).</span></span>             |
    | [<span data-ttu-id="11e85-156">**\_\_Eventproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="11e85-156">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)                 | <span data-ttu-id="11e85-157">Registriert einen [Ereignis Anbieter](registering-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="11e85-157">Registers an [event provider](registering-an-event-provider.md).</span></span>                   |
    | [<span data-ttu-id="11e85-158">**\_\_Eventconsumerproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="11e85-158">**\_\_EventConsumerProviderRegistration**</span></span>](--eventconsumerproviderregistration.md) | <span data-ttu-id="11e85-159">Registriert einen [Ereignisconsumeranbieter](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="11e85-159">Registers an [event consumer provider](registering-an-event-consumer-provider.md).</span></span> |
    | [<span data-ttu-id="11e85-160">**\_\_Methodproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="11e85-160">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)               | <span data-ttu-id="11e85-161">Registriert einen [Methoden Anbieter](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="11e85-161">Registers a [method provider](registering-an-event-consumer-provider.md).</span></span>          |
    | [<span data-ttu-id="11e85-162">**\_\_Propertyproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="11e85-162">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)           | <span data-ttu-id="11e85-163">Registriert einen [Eigenschaften Anbieter](registering-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="11e85-163">Registers a [property provider](registering-a-property-provider.md).</span></span>               |

    

     

5.  <span data-ttu-id="11e85-164">Platzieren Sie die MOF-Datei in einem permanenten Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="11e85-164">Place the MOF file into a permanent directory.</span></span>

    <span data-ttu-id="11e85-165">In der Regel sollten Sie die Datei im Installationsverzeichnis des Anbieters platzieren.</span><span class="sxs-lookup"><span data-stu-id="11e85-165">Typically, you should place the file in the installation directory of the provider.</span></span>

6.  <span data-ttu-id="11e85-166">Kompilieren [Sie die](mofcomp.md) MOF-Datei mit der [**-Schnittstelle**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) von "MOF".</span><span class="sxs-lookup"><span data-stu-id="11e85-166">Compile the MOF file using [mofcomp](mofcomp.md) or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="11e85-167">Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="11e85-167">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

    <span data-ttu-id="11e85-168">**Windows 8 und Windows Server 2012:** Beim Installieren von Anbietern werden [](mofcomp.md) [**die**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) \[ Schlüssel \] -und \[ statischen \] Qualifizierer unabhängig von ihren tatsächlichen Werten als true behandelt, wenn Sie vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="11e85-168">**Windows 8 and Windows Server 2012:** When installing providers, both [**mofcomp**](mofcomp.md) and the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface treat the \[Key\] and \[Static\] qualifiers as true if they are present, regardless of their actual values.</span></span> <span data-ttu-id="11e85-169">Andere Qualifizierer werden als false behandelt, wenn Sie vorhanden sind, aber nicht explizit auf true festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="11e85-169">Other qualifiers are treated as false if they are present but not explicitly set to true.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11e85-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11e85-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11e85-171">Entwickeln eines WMI-Anbieters</span><span class="sxs-lookup"><span data-stu-id="11e85-171">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="11e85-172">Festlegen von namepace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="11e85-172">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="11e85-173">Sichern Ihres Anbieters</span><span class="sxs-lookup"><span data-stu-id="11e85-173">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
