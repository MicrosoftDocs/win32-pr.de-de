---
description: Bei der WMI-Hochleistungs-API handelt es sich um eine Reihe von Schnittstellen, die Daten aus Leistungs Leistungsdaten Klassen abrufen.
ms.assetid: ee0a2ead-f53a-4651-a287-04a62eba3f84
ms.tgt_platform: multiple
title: Zugreifen auf Leistungsdaten in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b076e1ab15b934f347ee491711d7d3d1b8fbbe0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352780"
---
# <a name="accessing-performance-data-in-c"></a><span data-ttu-id="00191-103">Zugreifen auf Leistungsdaten in C++</span><span class="sxs-lookup"><span data-stu-id="00191-103">Accessing Performance Data in C++</span></span>

<span data-ttu-id="00191-104">Bei der WMI-Hochleistungs-API handelt es sich um eine Reihe von Schnittstellen, die Daten aus [Leistungs Leistungsdaten Klassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)abrufen.</span><span class="sxs-lookup"><span data-stu-id="00191-104">The WMI high-performance API is a series of interfaces that obtain data from [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="00191-105">Diese Schnittstellen erfordern die Verwendung [*eines Aktualisierungs Objekts,*](gloss-r.md) um die Samplingrate zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="00191-105">These interfaces require use of a [*refresher*](gloss-r.md) object to increase the sampling rate.</span></span> <span data-ttu-id="00191-106">Weitere Informationen zur Verwendung des Aktualisierungs Objekts bei der Skripterstellung finden Sie unter [zugreifen auf Leistungsdaten in Skripts](accessing-performance-data-in-script.md) und [WMI-Tasks: Leistungsüberwachung](wmi-tasks--performance-monitoring.md).</span><span class="sxs-lookup"><span data-stu-id="00191-106">For more information about using the refresher object in scripting, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md) and [WMI Tasks: Performance Monitoring](wmi-tasks--performance-monitoring.md).</span></span>

<span data-ttu-id="00191-107">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="00191-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="00191-108">Aktualisieren von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="00191-108">Refreshing Performance Data</span></span>](#refreshing-performance-data)
-   [<span data-ttu-id="00191-109">Hinzufügen von Enumeratoren zum WMI-Aktualisierungs Programm</span><span class="sxs-lookup"><span data-stu-id="00191-109">Adding Enumerators to the WMI Refresher</span></span>](#adding-enumerators-to-the-wmi-refresher)
-   [<span data-ttu-id="00191-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="00191-110">Example</span></span>](#example)
-   [<span data-ttu-id="00191-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00191-111">Related topics</span></span>](#related-topics)

## <a name="refreshing-performance-data"></a><span data-ttu-id="00191-112">Aktualisieren von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="00191-112">Refreshing Performance Data</span></span>

<span data-ttu-id="00191-113">Ein Aktualisierungs Objekt erhöht die Datenanbieter-und Client Leistung, indem Daten abgerufen werden, ohne dass Prozess Grenzen überschritten werden.</span><span class="sxs-lookup"><span data-stu-id="00191-113">A refresher object increases data provider and client performance by retrieving data without crossing process boundaries.</span></span> <span data-ttu-id="00191-114">Wenn sich sowohl der Client als auch der Server auf demselben Computer befinden, lädt ein Aktualisierungs Programm den Hochleistungs Anbieter Prozess seitig in den Client und kopiert Daten direkt von Anbieter Objekten in Client Objekte.</span><span class="sxs-lookup"><span data-stu-id="00191-114">If both the client and the server are located on the same computer, a refresher loads the high-performance provider in-process to the client, and copies data directly from provider objects into client objects.</span></span> <span data-ttu-id="00191-115">Wenn sich der Client und der Server auf unterschiedlichen Computern befinden, steigert das Aktualisierungs Programm die Leistung, indem Objekte auf dem Remote Computer zwischengespeichert werden und minimale Datasets an den Client übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="00191-115">If the client and the server are located on different computers, the refresher increases performance by caching objects on the remote computer, and transmitting minimal data sets to the client.</span></span>

<span data-ttu-id="00191-116">Ein Aktualisierungs Programm ist ebenfalls:</span><span class="sxs-lookup"><span data-stu-id="00191-116">A refresher also:</span></span>

-   <span data-ttu-id="00191-117">Verbindet einen Client automatisch erneut mit einem WMI-Remote Dienst, wenn ein Netzwerkfehler auftritt oder der Remote Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="00191-117">Automatically reconnects a client to a remote WMI service when a network error occurs, or the remote computer is restarted.</span></span>

    <span data-ttu-id="00191-118">Standardmäßig versucht ein Aktualisierungs Programm, eine Verbindung zwischen der Anwendung und dem relevanten Hochleistungs Anbieter herzustellen, wenn eine Remote Verbindung zwischen den beiden Computern fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="00191-118">By default, a refresher attempts to reconnect your application to the relevant high-performance provider when a remote connection between the two computers fails.</span></span> <span data-ttu-id="00191-119">Um die erneute Verbindung zu verhindern, übergeben Sie im [**Aktualisierungs**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) Methoden aufrufsbefehl das **WBEM- \_ Flag \_ aktualisieren \_ No \_ Auto \_ Reconnect** .</span><span class="sxs-lookup"><span data-stu-id="00191-119">To prevent the reconnection, pass the **WBEM\_FLAG\_REFRESH\_NO\_AUTO\_RECONNECT** flag in the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method call.</span></span> <span data-ttu-id="00191-120">Skript Clients müssen die Eigenschaft " [**Swap. autoreconnetct**](swbemrefresher-autoreconnect.md) " auf " **false**" festlegen.</span><span class="sxs-lookup"><span data-stu-id="00191-120">Scripting clients must set the [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) property to **FALSE**.</span></span>

-   <span data-ttu-id="00191-121">Lädt mehrere-Objekte und Enumeratoren, die von demselben oder unterschiedlichen Anbietern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="00191-121">Loads multiple objects and enumerators that are provided by the same or different providers.</span></span>

    <span data-ttu-id="00191-122">Ermöglicht es Ihnen, mehrere Objekte, Enumeratoren oder beides einem Aktualisierungs Programm hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="00191-122">Allows you to add multiple objects, enumerators, or both to a refresher.</span></span>

-   <span data-ttu-id="00191-123">Listet-Objekte auf.</span><span class="sxs-lookup"><span data-stu-id="00191-123">Enumerates objects.</span></span>

    <span data-ttu-id="00191-124">Wie bei anderen Anbietern kann ein Hochleistungs Anbieter Objekte aufzählen.</span><span class="sxs-lookup"><span data-stu-id="00191-124">Like other providers, a high-performance provider can enumerate objects.</span></span>

<span data-ttu-id="00191-125">Nachdem Sie den Hochleistungs Client geschrieben haben, möchten Sie möglicherweise die Reaktionszeit verbessern.</span><span class="sxs-lookup"><span data-stu-id="00191-125">After you finish writing your high-performance client, you may want to improve your response time.</span></span> <span data-ttu-id="00191-126">Da die [**iwbefibjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) -Schnittstelle für die Geschwindigkeit optimiert ist, ist die Schnittstelle nicht intrinsisch Thread sicher.</span><span class="sxs-lookup"><span data-stu-id="00191-126">Because the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface is optimized for speed, the interface is not intrinsically threadsafe.</span></span> <span data-ttu-id="00191-127">Daher können Sie während eines Aktualisierungs Vorgangs nicht auf das aktualisierbare Objekt oder die Aufzählung zugreifen.</span><span class="sxs-lookup"><span data-stu-id="00191-127">Therefore, during a refresh operation, do not access the refreshable object or enumeration.</span></span> <span data-ttu-id="00191-128">Verwenden Sie zum Schutz von Objekten während der **iwbemubjectaccess** -Methodenaufrufe die Methoden [**iwbemubjectaccess:: Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) und [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) .</span><span class="sxs-lookup"><span data-stu-id="00191-128">To protect objects across threads during **IWbemObjectAccess** method calls, use the [**IWbemObjectAccess::Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) and [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) methods.</span></span> <span data-ttu-id="00191-129">Synchronisieren Sie Ihre Threads, um die Leistung zu verbessern, sodass Sie keine einzelnen Threads Sperren müssen.</span><span class="sxs-lookup"><span data-stu-id="00191-129">For improved performance, synchronize your threads so that you do not need to lock individual threads.</span></span> <span data-ttu-id="00191-130">Das Reduzieren von Threads und das Synchronisieren von Gruppen von Objekten für Aktualisierungs Vorgänge bietet die beste Gesamtleistung.</span><span class="sxs-lookup"><span data-stu-id="00191-130">Reducing threads and synchronizing groups of objects for refresh operations provides the best overall performance.</span></span>

## <a name="adding-enumerators-to-the-wmi-refresher"></a><span data-ttu-id="00191-131">Hinzufügen von Enumeratoren zum WMI-Aktualisierungs Programm</span><span class="sxs-lookup"><span data-stu-id="00191-131">Adding Enumerators to the WMI Refresher</span></span>

<span data-ttu-id="00191-132">Die Anzahl der Instanzen und Daten in jeder Instanz werden aktualisiert, indem dem Aktualisierungs Programm ein Enumerator hinzugefügt wird, sodass jeder [**callbemrefresh Sher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) -Befehl eine komplette Enumeration ergibt.</span><span class="sxs-lookup"><span data-stu-id="00191-132">Both the number of instances and data in each instance are refreshed by adding an enumerator to the refresher so that each call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) results in a complete enumeration.</span></span>

<span data-ttu-id="00191-133">Im folgenden C++-Codebeispiel werden die folgenden Verweise und \# include-Anweisungen für die ordnungsgemäße Kompilierung benötigt.</span><span class="sxs-lookup"><span data-stu-id="00191-133">The following C++ code example requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="00191-134">Im folgenden Verfahren wird gezeigt, wie ein Enumerator zu einem Aktualisierungs Programm hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="00191-134">The following procedure shows how to add an enumerator to a refresher.</span></span>

<span data-ttu-id="00191-135">**So fügen Sie einem Aktualisierungs Programm einen Enumerator hinzu**</span><span class="sxs-lookup"><span data-stu-id="00191-135">**To add an enumerator to a refresher**</span></span>

1.  <span data-ttu-id="00191-136">Rufen Sie die [**iwbemconfigurerefresher:: AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) -Methode auf, indem Sie den Pfad zum aktualisierbaren Objekt und die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="00191-136">Call the [**IWbemConfigureRefresher::AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) method using the path to the refreshable object and the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

    <span data-ttu-id="00191-137">Das Aktualisierungs Programm gibt einen Zeiger auf eine [**iwbemhiperfenum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="00191-137">The refresher returns a pointer to an [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) interface.</span></span> <span data-ttu-id="00191-138">Sie können die **iwbemhiperferum** -Schnittstelle verwenden, um auf die Objekte in der-Enumeration zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="00191-138">You can use the **IWbemHiPerfEnum** interface to access the objects in the enumeration.</span></span>

    ```C++
    IWbemHiPerfEnum* pEnum = NULL;
    long lID;
    IWbemConfigureRefresher* pConfig;
    IWbemServices* pNameSpace;

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL,
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;
    ```

    

2.  <span data-ttu-id="00191-139">Erstellen Sie eine-Schleife, die die folgenden Aktionen ausführt:</span><span class="sxs-lookup"><span data-stu-id="00191-139">Create a loop that performs the following actions:</span></span>

    -   <span data-ttu-id="00191-140">Aktualisiert das-Objekt mithilfe eines Aufrufes von [**iwbemrefresh Sher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).</span><span class="sxs-lookup"><span data-stu-id="00191-140">Refreshes the object by using a call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).</span></span>
    -   <span data-ttu-id="00191-141">Stellt ein Array von [**iwbearbjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) -Schnittstellen Zeigern für die [**iwbemhiperferum:: GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) -Methode bereit.</span><span class="sxs-lookup"><span data-stu-id="00191-141">Provides an array of [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface pointers to the [**IWbemHiPerfEnum::GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) method.</span></span>
    -   <span data-ttu-id="00191-142">Greift auf die Eigenschaften des Enumerators zu, indem die [**iwbemubjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) -Methoden verwendet werden, die an [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects)übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="00191-142">Accesses the properties of the enumerator by using the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) methods passed into [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span></span>

        <span data-ttu-id="00191-143">Ein Eigenschaften Handle kann an jede [**iwbemubjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) -Instanz übermittelt werden, um den aktualisierten Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="00191-143">A property handle can be passed to each [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) instance to retrieve the refreshed value.</span></span> <span data-ttu-id="00191-144">Der Client muss [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) aufrufen, um die von [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects)zurückgegebenen **iwbemubjectaccess** -Zeiger freizugeben.</span><span class="sxs-lookup"><span data-stu-id="00191-144">The client must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the **IWbemObjectAccess** pointers returned by [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span></span>

## <a name="example"></a><span data-ttu-id="00191-145">Beispiel</span><span class="sxs-lookup"><span data-stu-id="00191-145">Example</span></span>

<span data-ttu-id="00191-146">Im folgenden C++-Codebeispiel wird eine Hochleistungs Klasse aufgelistet, bei der der Client ein Eigenschaften Handle aus dem ersten-Objekt abruft und das Handle für den Rest des Aktualisierungs Vorgangs erneut verwendet.</span><span class="sxs-lookup"><span data-stu-id="00191-146">The following C++ code example enumerates a high-performance class, where the client retrieves a property handle from the first object, and reuses the handle for the remainder of the refresh operation.</span></span> <span data-ttu-id="00191-147">Jeder Aufrufe der [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) -Methode aktualisiert die Anzahl von Instanzen und die Instanzdaten.</span><span class="sxs-lookup"><span data-stu-id="00191-147">Each call to the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method updates the number of instances and the instance data.</span></span>


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int __cdecl wmain(int argc, wchar_t* argv[])
{
    // To add error checking,
    // check returned HRESULT below where collected.
    HRESULT                 hr = S_OK;
    IWbemRefresher          *pRefresher = NULL;
    IWbemConfigureRefresher *pConfig = NULL;
    IWbemHiPerfEnum         *pEnum = NULL;
    IWbemServices           *pNameSpace = NULL;
    IWbemLocator            *pWbemLocator = NULL;
    IWbemObjectAccess       **apEnumAccess = NULL;
    BSTR                    bstrNameSpace = NULL;
    long                    lID = 0;
    long                    lVirtualBytesHandle = 0;
    long                    lIDProcessHandle = 0;
    DWORD                   dwVirtualBytes = 0;
    DWORD                   dwProcessId = 0;
    DWORD                   dwNumObjects = 0;
    DWORD                   dwNumReturned = 0;
    DWORD                   dwIDProcess = 0;
    DWORD                   i=0;
    int                     x=0;

    if (FAILED (hr = CoInitializeEx(NULL,COINIT_MULTITHREADED)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_NONE,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, EOAC_NONE, 0)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemLocator, 
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemLocator,
        (void**) &pWbemLocator)))
    {
        goto CLEANUP;
    }

    // Connect to the desired namespace.
    bstrNameSpace = SysAllocString(L"\\\\.\\root\\cimv2");
    if (NULL == bstrNameSpace)
    {
        hr = E_OUTOFMEMORY;
        goto CLEANUP;
    }
    if (FAILED (hr = pWbemLocator->ConnectServer(
        bstrNameSpace,
        NULL, // User name
        NULL, // Password
        NULL, // Locale
        0L,   // Security flags
        NULL, // Authority
        NULL, // Wbem context
        &pNameSpace)))
    {
        goto CLEANUP;
    }
    pWbemLocator->Release();
    pWbemLocator=NULL;
    SysFreeString(bstrNameSpace);
    bstrNameSpace = NULL;

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher, 
        (void**) &pRefresher)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = pRefresher->QueryInterface(
        IID_IWbemConfigureRefresher,
        (void **)&pConfig)))
    {
        goto CLEANUP;
    }

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL, 
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;

    // Get a property handle for the VirtualBytes property.

    // Refresh the object ten times and retrieve the value.
    for(x = 0; x < 10; x++)
    {
        dwNumReturned = 0;
        dwIDProcess = 0;
        dwNumObjects = 0;

        if (FAILED (hr =pRefresher->Refresh(0L)))
        {
            goto CLEANUP;
        }

        hr = pEnum->GetObjects(0L, 
            dwNumObjects, 
            apEnumAccess, 
            &dwNumReturned);
        // If the buffer was not big enough,
        // allocate a bigger buffer and retry.
        if (hr == WBEM_E_BUFFER_TOO_SMALL 
            && dwNumReturned > dwNumObjects)
        {
            apEnumAccess = new IWbemObjectAccess*[dwNumReturned];
            if (NULL == apEnumAccess)
            {
                hr = E_OUTOFMEMORY;
                goto CLEANUP;
            }
            SecureZeroMemory(apEnumAccess,
                dwNumReturned*sizeof(IWbemObjectAccess*));
            dwNumObjects = dwNumReturned;

            if (FAILED (hr = pEnum->GetObjects(0L, 
                dwNumObjects, 
                apEnumAccess, 
                &dwNumReturned)))
            {
                goto CLEANUP;
            }
        }
        else
        {
            if (hr == WBEM_S_NO_ERROR)
            {
                hr = WBEM_E_NOT_FOUND;
                goto CLEANUP;
            }
        }

        // First time through, get the handles.
        if (0 == x)
        {
            CIMTYPE VirtualBytesType;
            CIMTYPE ProcessHandleType;
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"VirtualBytes",
                &VirtualBytesType,
                &lVirtualBytesHandle)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"IDProcess",
                &ProcessHandleType,
                &lIDProcessHandle)))
            {
                goto CLEANUP;
            }
        }
           
        for (i = 0; i < dwNumReturned; i++)
        {
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lVirtualBytesHandle,
                &dwVirtualBytes)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lIDProcessHandle,
                &dwIDProcess)))
            {
                goto CLEANUP;
            }

            wprintf(L"Process ID %lu is using %lu bytes\n",
                dwIDProcess, dwVirtualBytes);

            // Done with the object
            apEnumAccess[i]->Release();
            apEnumAccess[i] = NULL;
        }

        if (NULL != apEnumAccess)
        {
            delete [] apEnumAccess;
            apEnumAccess = NULL;
        }

       // Sleep for a second.
       Sleep(1000);
    }
    // exit loop here
    CLEANUP:

    if (NULL != bstrNameSpace)
    {
        SysFreeString(bstrNameSpace);
    }

    if (NULL != apEnumAccess)
    {
        for (i = 0; i < dwNumReturned; i++)
        {
            if (apEnumAccess[i] != NULL)
            {
                apEnumAccess[i]->Release();
                apEnumAccess[i] = NULL;
            }
        }
        delete [] apEnumAccess;
    }
    if (NULL != pWbemLocator)
    {
        pWbemLocator->Release();
    }
    if (NULL != pNameSpace)
    {
        pNameSpace->Release();
    }
    if (NULL != pEnum)
    {
        pEnum->Release();
    }
    if (NULL != pConfig)
    {
        pConfig->Release();
    }
    if (NULL != pRefresher)
    {
        pRefresher->Release();
    }

    CoUninitialize();

    if (FAILED (hr))
    {
        wprintf (L"Error status=%08x\n",hr);
    }

    return 1;
}
```



## <a name="related-topics"></a><span data-ttu-id="00191-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00191-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00191-149">Leistungs Leistungsdaten-Klassen</span><span class="sxs-lookup"><span data-stu-id="00191-149">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="00191-150">Zugreifen auf Leistungsdaten im Skript</span><span class="sxs-lookup"><span data-stu-id="00191-150">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="00191-151">Aktualisieren von WMI-Daten in Skripts</span><span class="sxs-lookup"><span data-stu-id="00191-151">Refreshing WMI Data in Scripts</span></span>](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[<span data-ttu-id="00191-152">WMI-Tasks: Leistungsüberwachung</span><span class="sxs-lookup"><span data-stu-id="00191-152">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="00191-153">Überwachen von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="00191-153">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="00191-154">Eigenschafts Qualifizierer für formatierte Leistungs Objektklassen</span><span class="sxs-lookup"><span data-stu-id="00191-154">Property Qualifiers for Formatted Performance Counter Classes</span></span>](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="00191-155">WMI-Leistungsdaten Typen</span><span class="sxs-lookup"><span data-stu-id="00191-155">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> <dt>

[<span data-ttu-id="00191-156">**Wmiadap.exe**</span><span class="sxs-lookup"><span data-stu-id="00191-156">**Wmiadap.exe**</span></span>](wmiadap.md)
</dt> <dt>

[<span data-ttu-id="00191-157">**QueryPerformanceCounter**</span><span class="sxs-lookup"><span data-stu-id="00191-157">**QueryPerformanceCounter**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> </dl>

 

 
