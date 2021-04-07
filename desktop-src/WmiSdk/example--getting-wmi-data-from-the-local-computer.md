---
description: Mithilfe der Prozeduren und Codebeispiele in diesem Thema können Sie eine vollständige WMI-Client Anwendung erstellen, die COM-Initialisierung ausführt, eine Verbindung mit WMI auf dem lokalen Computer herstellt, Daten SemiSynchron abruft und dann bereinigt.
ms.assetid: 35dc97aa-dcef-48c1-af8b-ce43e3cf1d3e
ms.tgt_platform: multiple
title: 'Beispiel: erhalten von WMI-Daten vom lokalen Computer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840cd4ada941bdfd8ba7fca9b8ca9393c0b5eb55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864019"
---
# <a name="example-getting-wmi-data-from-the-local-computer"></a><span data-ttu-id="fb0fa-103">Beispiel: erhalten von WMI-Daten vom lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="fb0fa-103">Example: Getting WMI Data from the Local Computer</span></span>

<span data-ttu-id="fb0fa-104">Mithilfe der Prozeduren und Codebeispiele in diesem Thema können Sie eine vollständige WMI-Client Anwendung erstellen, die COM-Initialisierung ausführt, eine Verbindung mit WMI auf dem lokalen Computer herstellt, Daten SemiSynchron abruft und dann bereinigt.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on the local computer, retrieves data semisynchronously, and then cleans up.</span></span> <span data-ttu-id="fb0fa-105">In diesem Beispiel wird der Name des Betriebssystems auf dem lokalen Computer abgerufen und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-105">This example gets the name of the operating system on the local computer and displays it.</span></span> <span data-ttu-id="fb0fa-106">Informationen zum Abrufen von Daten von einem Remote Computer finden Sie unter [Beispiel: Abrufen von WMI-Daten von einem Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="fb0fa-106">To retrieve data from a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span> <span data-ttu-id="fb0fa-107">Informationen zum asynchronen ermitteln der Daten finden Sie unter [Beispiel: Asynchrones erhalten von WMI-Daten vom lokalen Computer](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span><span class="sxs-lookup"><span data-stu-id="fb0fa-107">For getting the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

<span data-ttu-id="fb0fa-108">Das folgende Verfahren wird verwendet, um die WMI-Anwendung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-108">The following procedure is used to execute the WMI application.</span></span> <span data-ttu-id="fb0fa-109">Die Schritte 1 bis 5 enthalten alle erforderlichen Schritte zum Einrichten und Herstellen der Verbindung mit WMI. in den Schritten 6 und 7 werden die Daten abgefragt und empfangen.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-109">Steps 1 through 5 contain all the steps required to set up and connect to WMI, and steps 6 and 7 are where data is queried and received.</span></span>

1.  <span data-ttu-id="fb0fa-110">Initialisieren von com-Parametern mit einem [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-110">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="fb0fa-111">Weitere Informationen finden Sie unter [Initialisieren von com für eine WMI-Anwendung](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="fb0fa-111">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="fb0fa-112">Initialisieren Sie die com-Prozesssicherheit durch Aufrufen von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="fb0fa-112">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="fb0fa-113">Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="fb0fa-113">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="fb0fa-114">Rufen Sie den anfänglichen Serverlocatorpunkt in WMI durch Aufrufen von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)ab.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-114">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="fb0fa-115">Weitere Informationen finden Sie unter [Erstellen einer Verbindung mit einem WMI-Namespace](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="fb0fa-115">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="fb0fa-116">Rufen Sie mithilfe [](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \\ von [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)einen Zeiger auf IWbemServices für den Stamm-CIMV2-Namespace auf dem lokalen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-116">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the root\\cimv2 namespace on the local computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="fb0fa-117">Informationen zum Herstellen einer Verbindung mit einem Remote Computer finden Sie unter [Beispiel: erhalten von WMI-Daten von einem Remote Computer aus](example--getting-wmi-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="fb0fa-117">To connect to a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span>

    <span data-ttu-id="fb0fa-118">Weitere Informationen finden Sie unter [Erstellen einer Verbindung mit einem WMI-Namespace](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="fb0fa-118">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

5.  <span data-ttu-id="fb0fa-119">Legen Sie die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Proxy Sicherheit fest, damit der WMI-Dienst die Identität des Clients durch Aufrufen von [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-119">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so the WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="fb0fa-120">Weitere Informationen finden Sie unter [Festlegen der Sicherheitsstufen für eine WMI-Verbindung](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fb0fa-120">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

6.  <span data-ttu-id="fb0fa-121">Verwenden Sie den [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Zeiger, um WMI-Anforderungen zu stellen.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-121">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests of WMI.</span></span> <span data-ttu-id="fb0fa-122">In diesem Beispiel wird eine Abfrage für den Namen des Betriebssystems durch Aufrufen von [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-122">This example executes a query for the name of the operating system by calling [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span></span>

    <span data-ttu-id="fb0fa-123">Die folgende WQL-Abfrage ist eines der Methodenargumente.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-123">The following WQL query is one of the method arguments.</span></span>

    `SELECT * FROM Win32_OperatingSystem`

    <span data-ttu-id="fb0fa-124">Das Ergebnis dieser Abfrage wird in einem [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Zeiger gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-124">The result of this query is stored in an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer.</span></span> <span data-ttu-id="fb0fa-125">Auf diese Weise können die Datenobjekte aus der Abfrage SemiSynchron mit der **ienumwbemclassobject** -Schnittstelle abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-125">This allows the data objects from the query to be retrieved semisynchronously with the **IEnumWbemClassObject** interface.</span></span> <span data-ttu-id="fb0fa-126">Weitere Informationen finden Sie unter Auflisten von [WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="fb0fa-126">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span> <span data-ttu-id="fb0fa-127">Informationen zum asynchronen ermitteln der Daten finden Sie unter [Beispiel: Asynchrones erhalten von WMI-Daten vom lokalen Computer](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span><span class="sxs-lookup"><span data-stu-id="fb0fa-127">For getting the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

    <span data-ttu-id="fb0fa-128">Weitere Informationen zum Erstellen von WMI-Anforderungen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md), [Abfragen von WMI](querying-wmi.md)und [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="fb0fa-128">For more information about making requests to WMI, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Querying WMI](querying-wmi.md), and [Calling a Method](calling-a-method.md).</span></span>

7.  <span data-ttu-id="fb0fa-129">Hiermit werden die Daten aus der WQL-Abfrage angezeigt und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-129">Get and display the data from the WQL query.</span></span> <span data-ttu-id="fb0fa-130">Der [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Zeiger ist mit den Datenobjekten verknüpft, die von der Abfrage zurückgegeben wurden, und die Datenobjekte können mit der [**ienumwbemclassobject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-130">The [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer is linked to the data objects that the query returned, and the data objects can be retrieved with the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) method.</span></span> <span data-ttu-id="fb0fa-131">Diese Methode verknüpft die Datenobjekte mit einem [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Zeiger, der an die-Methode übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-131">This method links the data objects to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that is passed into the method.</span></span> <span data-ttu-id="fb0fa-132">Verwenden Sie die [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) -Methode, um die gewünschten Informationen aus den Datenobjekten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-132">Use the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method to get the desired information from the data objects.</span></span>

    <span data-ttu-id="fb0fa-133">Das folgende Codebeispiel wird verwendet, um die Name-Eigenschaft aus dem Datenobjekt zu erhalten, das den Namen des Betriebssystems bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-133">The following code example is used to get the Name property from the data object, which provides the name of the operating system.</span></span>

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    ```

    

    <span data-ttu-id="fb0fa-134">Nachdem der Wert der Name-Eigenschaft in der [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Variablen vtprop gespeichert wurde, kann er dem Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-134">After the value of the Name property is stored in the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) variable vtProp, it can then be displayed to the user.</span></span>

    <span data-ttu-id="fb0fa-135">Weitere Informationen finden Sie unter Auflisten von [WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="fb0fa-135">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

<span data-ttu-id="fb0fa-136">Im folgenden Codebeispiel werden WMI-Daten von einem lokalen Computer aus SemiSynchron abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fb0fa-136">The following code example retrieves WMI data semisynchronously from a local computer.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int argc, char **argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
            << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM authentication
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;                    // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the root\cimv2 namespace with
    // the current user and obtain pointer pSvc
    // to make IWbemServices calls.
    hres = pLoc->ConnectServer(
         _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
         NULL,                    // User name. NULL = current user
         NULL,                    // User password. NULL = current
         0,                       // Locale. NULL indicates current
         NULL,                    // Security flags.
         0,                       // Authority (for example, Kerberos)
         0,                       // Context object 
         &pSvc                    // pointer to IWbemServices proxy
         );
    
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(
       pSvc,                        // Indicates the proxy to set
       RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx
       NULL,                        // Server principal name 
       RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
       NULL,                        // client identity
       EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("SELECT * FROM Win32_OperatingSystem"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: -------------------------------------------------
    // Get the data from the query in step 6 -------------------
 
    IWbemClassObject *pclsObj = NULL;
    ULONG uReturn = 0;
   
    while (pEnumerator)
    {
        HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
            &pclsObj, &uReturn);

        if(0 == uReturn)
        {
            break;
        }

        VARIANT vtProp;

        // Get the value of the Name property
        hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
        wcout << " OS Name : " << vtProp.bstrVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
    }

    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



 

 
