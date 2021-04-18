---
description: Das WMI-Repository enthält vorinstallierte Leistungsklassen für alle Leistungs Bibliotheksobjekte.
ms.assetid: 2158385f-d0dc-4102-84db-ce02d2b0ee53
ms.tgt_platform: multiple
title: Zugreifen auf vorinstallierte WMI-Leistungsklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265f9b4008913a463545ed03cd6f1025b58ef5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347623"
---
# <a name="accessing-wmi-preinstalled-performance-classes"></a><span data-ttu-id="ee4f7-103">Zugreifen auf vorinstallierte WMI-Leistungsklassen</span><span class="sxs-lookup"><span data-stu-id="ee4f7-103">Accessing WMI Preinstalled Performance Classes</span></span>

<span data-ttu-id="ee4f7-104">Das WMI-Repository enthält vorinstallierte Leistungsklassen für alle Leistungs Bibliotheksobjekte.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-104">The WMI repository contains preinstalled performance classes for all the performance library objects.</span></span> <span data-ttu-id="ee4f7-105">Beispielsweise stellen Instanzen der RAW-Daten Leistungsklasse [**Win32 \_ perfrawdata \_ perfproc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) Prozesse dar.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-105">For example, instances of the raw data performance class [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) represent processes.</span></span> <span data-ttu-id="ee4f7-106">Dieses Leistungs Objekt ist im System Monitor als Prozess Objekt sichtbar.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-106">This performance object is visible in System Monitor as the Process object.</span></span>

<span data-ttu-id="ee4f7-107">Die **pagefehlerspersec** -Eigenschaft des [**Win32 \_ perfrawdata \_ perfproc- \_ Prozesses**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) stellt den Leistungs Leistungs Monitor "Seiten Fehler pro Sekunde" für den Prozess dar.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-107">The **PageFaultsPerSec** property of [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) represents the Page Faults per second performance counter for the process.</span></span> <span data-ttu-id="ee4f7-108">Die [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) -Klassen enthalten die berechneten Datenwerte, die im System Monitor (Perfmon.exe) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-108">The [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes contain the calculated data values displayed in System Monitor (Perfmon.exe).</span></span> <span data-ttu-id="ee4f7-109">Der Wert der **pagefehlerspersec** -Eigenschaft des [**Win32 \_ perfformatteddata \_ perfproc- \_ Prozesses**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) entspricht dem, wenn er im System Monitor angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-109">The value of the **PageFaultsPerSec** property of [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) is the same as when it appears in System Monitor.</span></span>

<span data-ttu-id="ee4f7-110">Verwenden Sie entweder die [com-API für WMI](com-api-for-wmi.md) oder die [Skript-API für WMI](scripting-api-for-wmi.md) , um über die [Leistungs Leistungsdaten Klassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)auf Leistungsdaten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-110">Use either the [COM API for WMI](com-api-for-wmi.md) or the [Scripting API for WMI](scripting-api-for-wmi.md) to access performance data through the [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="ee4f7-111">In beiden Fällen ist [*ein*](gloss-r.md) Aktualisierungs Objekt zum Abrufen der einzelnen Daten Stichproben erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-111">In both cases a [*refresher*](gloss-r.md) object is required to obtain each data sample.</span></span> <span data-ttu-id="ee4f7-112">Weitere Informationen und Skriptcode Beispiele für die Verwendung von aktualisierungsproblegern und den Zugriff auf Leistungsklassen finden Sie unter [WMI-Tasks: Leistungsüberwachung](wmi-tasks--performance-monitoring.md).</span><span class="sxs-lookup"><span data-stu-id="ee4f7-112">For more information and script code examples for using refreshers and accessing performance classes, see [WMI Tasks: Performance Monitoring](wmi-tasks--performance-monitoring.md).</span></span> <span data-ttu-id="ee4f7-113">Weitere Informationen finden Sie unter [zugreifen auf Leistungsdaten im Skript](accessing-performance-data-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="ee4f7-113">For more information, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md).</span></span>

## <a name="accessing-performance-data-from-c"></a><span data-ttu-id="ee4f7-114">Zugreifen auf Leistungsdaten von C++</span><span class="sxs-lookup"><span data-stu-id="ee4f7-114">Accessing Performance Data from C++</span></span>

<span data-ttu-id="ee4f7-115">Im folgenden C++-Codebeispiel wird der Leistungsindikatorenanbieter verwendet, um auf vordefinierte hochleistungsklassen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-115">The following C++ code example uses the Performance Counter provider to access predefined high-performance classes.</span></span> <span data-ttu-id="ee4f7-116">Er erstellt ein Aktualisierungs Objekt und fügt dem Aktualisierungs Programm ein Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-116">It creates a refresher object and adds an object to the refresher.</span></span> <span data-ttu-id="ee4f7-117">Das-Objekt ist eine [**Win32 \_ perfrawdata \_ perfproc- \_ Prozess**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) Instanz, die die Leistung eines bestimmten Prozesses überwacht.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-117">The object is a [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) instance that monitors the performance of a specific process.</span></span> <span data-ttu-id="ee4f7-118">Der Code liest nur eine Counter-Eigenschaft im Process-Objekt, der **virtualbytes** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-118">The code only reads one counter property in the process object, the **VirtualBytes** property.</span></span> <span data-ttu-id="ee4f7-119">Der Code erfordert, dass die folgenden Verweise und **\# include** -Anweisungen ordnungsgemäß kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-119">The code requires the following references and **\#include** statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="ee4f7-120">Im folgenden Verfahren wird gezeigt, wie Sie in C++ auf Daten von einem Hochleistungs Anbieter zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-120">The following procedure shows how to access data from a high-performance provider in C++.</span></span>

<span data-ttu-id="ee4f7-121">**So greifen Sie auf Daten eines Hochleistungs Anbieters in C++ zu**</span><span class="sxs-lookup"><span data-stu-id="ee4f7-121">**To access data from a high-performance provider in C++**</span></span>

1.  <span data-ttu-id="ee4f7-122">Stellen Sie eine Verbindung mit dem WMI-Namespace her, und legen Sie die WMI-Sicherheit mithilfe eines Aufrufes von [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) und [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)fest.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-122">Establish a connection to the WMI namespace, and set WMI security by using a call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) and [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="ee4f7-123">Dieser Schritt ist ein Standard Schritt zum Erstellen einer beliebigen WMI-Client Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-123">This step is a standard step for creating any WMI client application.</span></span> <span data-ttu-id="ee4f7-124">Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung mithilfe von C++](creating-a-wmi-application-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="ee4f7-124">For more information, see [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md).</span></span>

2.  <span data-ttu-id="ee4f7-125">Erstellen Sie ein Aktualisierungs Objekt, indem Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit CLSID \_ wbemaktualisierungs Programm verwenden.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-125">Create a refresher object by using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with CLSID\_WbemRefresher.</span></span> <span data-ttu-id="ee4f7-126">Fordern Sie mithilfe der [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode eine [**iwbemconfigurerefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) -Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-126">Request an [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) interface through the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method.</span></span> <span data-ttu-id="ee4f7-127">Fordern Sie mithilfe der **QueryInterface** -Methode eine [**iwbemaktualisierungs**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) -Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-127">Request an [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interface through the **QueryInterface** method.</span></span>

    <span data-ttu-id="ee4f7-128">Die [**iwbemfreshsher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) -Schnittstelle ist die Hauptschnittstelle für das [**WMI-**](swbemrefreshableitem-refresher.md) Aktualisierungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-128">The [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interface is the main interface for the WMI [**Refresher**](swbemrefreshableitem-refresher.md) object.</span></span>

    <span data-ttu-id="ee4f7-129">Im folgenden C++-Codebeispiel wird gezeigt, wie [**iwbemconfigurerefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-129">The following C++ code example shows how to retrieve [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).</span></span>

    ```C++
    IWbemRefresher* pRefresher = NULL;

    HRESULT hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher,
        (void**) &pRefresher);

    IWbemConfigureRefresher* pConfig = NULL;

    pRefresher->QueryInterface( 
        IID_IWbemConfigureRefresher,
        (void**) &pConfig
      );
    ```

    

3.  <span data-ttu-id="ee4f7-130">Fügen Sie dem Aktualisierungs Programm ein Objekt hinzu, indem Sie die [**iwbemconfigurerefresher:: addobjectbypath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-130">Add an object to the refresher through a call to the [**IWbemConfigureRefresher::AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) method.</span></span>

    <span data-ttu-id="ee4f7-131">Wenn Sie dem Aktualisierungs Programm ein Objekt hinzufügen, aktualisiert WMI das Objekt, wenn Sie die [**iwbemrefresh Sher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-131">When you add an object to the refresher, WMI refreshes the object whenever you call the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method.</span></span> <span data-ttu-id="ee4f7-132">Das Objekt, das Sie hinzufügen, bestimmt den Anbieter in seinen Klassen Qualifizierern.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-132">The object you add designates the provider in its class qualifiers.</span></span>

    <span data-ttu-id="ee4f7-133">Im folgenden C++-Codebeispiel wird gezeigt, wie [**addobjectbypath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-133">The following C++ code example shows how to call [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).</span></span>

    ```C++
    IWbemClassObject* pObj = NULL;
    IWbemServices* pNameSpace = NULL;

    // Add the instance to be refreshed.
    hr = pConfig->AddObjectByPath(
         pNameSpace,
         L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
         0L,
         NULL,
         &pObj,
         NULL
    );
    if (FAILED(hr))
    {
       cout << "Could not add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }
    ```

    

4.  <span data-ttu-id="ee4f7-134">Um einen schnelleren Zugriff auf das Objekt einzurichten, stellen Sie über [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf der [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Schnittstelle eine Verbindung mit der [**iwbewbjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) -Schnittstelle her.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-134">To set up faster access to the object, connect to the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface through [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface.</span></span>

    <span data-ttu-id="ee4f7-135">Im folgenden C++-Codebeispiel wird gezeigt, wie ein Zeiger auf das-Objekt mithilfe von [**iwbemubjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) anstelle von [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-135">The following C++ code example shows how to retrieve a pointer to the object using [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) instead of [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).</span></span>

    ```C++
        // For quick property retrieval, use IWbemObjectAccess.
        IWbemObjectAccess* pAcc = NULL;
        pObj->QueryInterface( IID_IWbemObjectAccess, (void**) &pAcc );
        // This is not required.
        pObj->Release();
    ```

    

    <span data-ttu-id="ee4f7-136">Die [**iwbemubjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) -Schnittstelle steigert die Leistung, da Sie Handles für bestimmte Leistungstest Eigenschaften abrufen können. Außerdem müssen Sie das Objekt im Code Sperren und entsperren. dabei handelt es sich um einen Vorgang, den [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) für jeden Eigenschaften Zugriff ausführt.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-136">The [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface increases performance because you can get handles to specific counter properties, and it requires that you lock and unlock the object in your code, which is an operation that [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) performs for each property access.</span></span>

5.  <span data-ttu-id="ee4f7-137">Rufen Sie die Handles der zu überprüfenden Eigenschaften mithilfe von Aufrufen der [**iwbewbjectaccess:: getpropertyhandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) -Methode ab.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-137">Obtain the handles of the properties to examine by using calls to the [**IWbemObjectAccess::GetPropertyHandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) method.</span></span>

    <span data-ttu-id="ee4f7-138">Eigenschaften Handles sind für alle Instanzen einer Klasse identisch. Dies bedeutet, dass Sie das Eigenschaften Handle verwenden, das Sie von einer bestimmten Instanz für alle Instanzen einer bestimmten Klasse abrufen.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-138">Property handles are the same for all instances of a class, which means that use the property handle you retrieve from a specific instance for all instances of a specific class.</span></span> <span data-ttu-id="ee4f7-139">Sie können auch ein Handle von einem Klassenobjekt abrufen, um Eigenschaftswerte aus einem Instanzobjekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-139">You can also obtain a handle from a class object to retrieve property values from an instance object.</span></span>

    <span data-ttu-id="ee4f7-140">Im folgenden C++-Codebeispiel wird gezeigt, wie ein Eigenschaften Handle abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-140">The following C++ code example shows how to retrieve a property handle.</span></span>

    ```C++
        // Get a property handle for the VirtualBytes property
        long lVirtualBytesHandle = 0;
        DWORD dwVirtualBytes = 0;
        CIMTYPE variant;

        hr = pAcc->GetPropertyHandle(L"VirtualBytes",
             &variant,
             &lVirtualBytesHandle 
        );
        if (FAILED(hr))
        {
           cout << "Could not get property handle. Error code: 0x"
                << hex << hr << endl;
           return hr;
        }
    ```

    

6.  <span data-ttu-id="ee4f7-141">Erstellen Sie eine Programmier Schleife, die die folgenden Aktionen ausführt:</span><span class="sxs-lookup"><span data-stu-id="ee4f7-141">Create a programming loop that performs the following actions:</span></span>

    -   <span data-ttu-id="ee4f7-142">Aktualisieren Sie das Objekt mit einem [**callbemrefresh Sher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) -Befehl, indem Sie den Zeiger verwenden, der im vorherigen Aufrufen von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-142">Refresh the object with a call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) by using the pointer created in the previous call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

        <span data-ttu-id="ee4f7-143">In diesem-Befehl aktualisiert das WMI-Aktualisierungs Programm das-Client Objekt mithilfe von Daten, die der Anbieter bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-143">In this call, the WMI Refresher refreshes the client object by using data that the provider supplies.</span></span>

    -   <span data-ttu-id="ee4f7-144">Führen Sie für das Objekt gegebenenfalls eine beliebige Aktion aus, z. b. das Abrufen eines Eigenschafts namens, eines Datentyps oder eines Werts.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-144">Perform any action as necessary on the object, such as retrieving a property name, data type, or value.</span></span>

        <span data-ttu-id="ee4f7-145">Sie können über das zuvor erhaltene Eigenschaften Handle auf die-Eigenschaft zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-145">You can access the property through the property handle obtained earlier.</span></span> <span data-ttu-id="ee4f7-146">Aufgrund des [**Aktualisierungs**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) Aufrufes aktualisiert WMI die-Eigenschaft jedes Mal durch die-Schleife.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-146">Due to the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) call, WMI refreshes the property each time through the loop.</span></span>

<span data-ttu-id="ee4f7-147">Im folgenden Beispiel wird gezeigt, wie die Hochleistungs-API von WMI verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-147">The following C++ example shows how to use the WMI high-performance API.</span></span>


```C++
// Get the local locator object
IWbemServices* pNameSpace = NULL;
IWbemLocator* pWbemLocator = NULL;
CIMTYPE variant;
VARIANT VT;

CoCreateInstance( CLSID_WbemLocator, NULL,
    CLSCTX_INPROC_SERVER, IID_IWbemLocator, (void**) &pWbemLocator
);

// Connect to the desired namespace
BSTR bstrNameSpace = SysAllocString( L"\\\\.\\root\\cimv2" );

HRESULT hr = WBEM_S_NO_ERROR;

hr = pWbemLocator->ConnectServer(
     bstrNameSpace,      // Namespace name
     NULL,               // User name
     NULL,               // Password
     NULL,               // Locale
     0L,                 // Security flags
     NULL,               // Authority
     NULL,               // Wbem context
     &pNameSpace         // Namespace
);

if ( SUCCEEDED( hr ) )
{
    // Set namespace security.
    IUnknown* pUnk = NULL;
    pNameSpace->QueryInterface( IID_IUnknown, (void**) &pUnk );

    hr = CoSetProxyBlanket(
         pNameSpace, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }

    hr = CoSetProxyBlanket(pUnk, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pUnk->Release();
       return hr;
    }

    // Clean up the IUnknown.
    pUnk->Release();

    IWbemRefresher* pRefresher = NULL;
    IWbemConfigureRefresher* pConfig = NULL;

    // Create a WMI Refresher and get a pointer to the
    // IWbemConfigureRefresher interface.
    CoCreateInstance(CLSID_WbemRefresher, 
                     NULL,
                     CLSCTX_INPROC_SERVER, 
                     IID_IWbemRefresher, 
                     (void**) &pRefresher 
    );
    
    pRefresher->QueryInterface(IID_IWbemConfigureRefresher,
                               (void**) &pConfig );

    IWbemClassObject* pObj = NULL;

    // Add the instance to be refreshed.
    pConfig->AddObjectByPath(
       pNameSpace,
       L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
       0L,
       NULL,
       &pObj,
       NULL 
    );
    if (FAILED(hr))
    {
       cout << "Cannot add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       
       return hr;
    }

    // For quick property retrieval, use IWbemObjectAccess.
    IWbemObjectAccess* pAcc = NULL;
    pObj->QueryInterface(IID_IWbemObjectAccess, 
                         (void**) &pAcc );

    // This is not required.
    pObj->Release();

    // Get a property handle for the VirtualBytes property.
    long lVirtualBytesHandle = 0;
    DWORD dwVirtualBytes = 0;

    pAcc->GetPropertyHandle(L"VirtualBytes", 
                            &variant, 
                            &lVirtualBytesHandle );

    // Refresh the object ten times and retrieve the value.
    for( int x = 0; x < 10; x++ )
    {
        pRefresher->Refresh( 0L );
        pAcc->ReadDWORD( lVirtualBytesHandle, &dwVirtualBytes );
        printf( "Process is using %lu bytes\n", dwVirtualBytes );
        // Sleep for a second.
        Sleep( 1000 );
    }
    // Clean up all the objects.
    pAcc->Release();
    // Done with these too.
    pConfig->Release();
    pRefresher->Release();
    pNameSpace->Release();
}
SysFreeString( bstrNameSpace );
pWbemLocator->Release();
```



## <a name="related-topics"></a><span data-ttu-id="ee4f7-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee4f7-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee4f7-149">Leistungs Leistungsdaten-Klassen</span><span class="sxs-lookup"><span data-stu-id="ee4f7-149">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="ee4f7-150">WMI-Tasks: Leistungsüberwachung</span><span class="sxs-lookup"><span data-stu-id="ee4f7-150">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
