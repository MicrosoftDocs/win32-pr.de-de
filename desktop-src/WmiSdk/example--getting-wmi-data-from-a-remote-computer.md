---
description: Mithilfe der Prozeduren und Codebeispiele in diesem Thema können Sie eine vollständige WMI-Client Anwendung erstellen, die COM-Initialisierung ausführt, eine Verbindung mit WMI auf einem Remote Computer herstellt, Daten halb synchron abruft und dann bereinigt.
ms.assetid: 30e65b9e-9372-46d1-843a-bda0d6ec1c69
ms.tgt_platform: multiple
title: 'Beispiel: erhalten von WMI-Daten von einem Remote Computer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3375bd25073defa92358f697ee4165ddb57793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348545"
---
# <a name="example-getting-wmi-data-from-a-remote-computer"></a><span data-ttu-id="04039-103">Beispiel: erhalten von WMI-Daten von einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="04039-103">Example: Getting WMI Data from a Remote Computer</span></span>

<span data-ttu-id="04039-104">Mithilfe der Prozeduren und Codebeispiele in diesem Thema können Sie eine vollständige WMI-Client Anwendung erstellen, die COM-Initialisierung ausführt, eine Verbindung mit WMI auf einem Remote Computer herstellt, Daten halb synchron abruft und dann bereinigt.</span><span class="sxs-lookup"><span data-stu-id="04039-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on a remote computer, gets data semisynchronously, and then cleans up.</span></span> <span data-ttu-id="04039-105">Weitere Informationen zum Ausführen von Daten vom lokalen Computer finden Sie unter [Beispiel: Get WMI Data from the Local Computer](example--getting-wmi-data-from-the-local-computer.md).</span><span class="sxs-lookup"><span data-stu-id="04039-105">For more information about how to get data from the local computer, see [Example: Getting WMI Data from the Local Computer](example--getting-wmi-data-from-the-local-computer.md).</span></span> <span data-ttu-id="04039-106">Weitere Informationen zum asynchronen Ausführen der Daten finden Sie unter [Beispiel: Asynchrones erhalten von WMI-Daten vom lokalen Computer](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span><span class="sxs-lookup"><span data-stu-id="04039-106">For more information about how to get the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

> [!Note]  
> <span data-ttu-id="04039-107">Wenn Sie versuchen, eine Verbindung mit einem Remote Computer herzustellen, lesen Sie die Informationen unter Herstellen einer Remote[Verbindung mit WMI](connecting-to-wmi-remotely-starting-with-vista.md).</span><span class="sxs-lookup"><span data-stu-id="04039-107">If you are trying to connect to a remote computer refer to the information in[Connecting to WMI Remotely](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

 

<span data-ttu-id="04039-108">Das folgende Verfahren zeigt, wie Sie die WMI-Anwendung ausführen.</span><span class="sxs-lookup"><span data-stu-id="04039-108">The following procedure shows how to execute the WMI application.</span></span> <span data-ttu-id="04039-109">Die Schritte 1 bis 5 enthalten alle Schritte, die für die Einrichtung und Verbindung mit WMI erforderlich sind, und in den Schritten 6 und 7 werden die Daten abgefragt und empfangen.</span><span class="sxs-lookup"><span data-stu-id="04039-109">Steps 1 through 5 contain all of the steps required to set up and connect to WMI, and steps 6 and 7 are where data is queried and received.</span></span>

<span data-ttu-id="04039-110">**So erhalten Sie WMI-Daten von einem Remote Computer**</span><span class="sxs-lookup"><span data-stu-id="04039-110">**To get WMI data from a remote computer**</span></span>

1.  <span data-ttu-id="04039-111">Initialisieren von com-Parametern mit einem [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="04039-111">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="04039-112">Weitere Informationen finden Sie unter [Initialisieren von com für eine WMI-Anwendung](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="04039-112">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="04039-113">Initialisieren Sie die com-Prozesssicherheit durch Aufrufen von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="04039-113">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="04039-114">Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="04039-114">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="04039-115">Rufen Sie den anfänglichen Serverlocatorpunkt in WMI durch Aufrufen von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)ab.</span><span class="sxs-lookup"><span data-stu-id="04039-115">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="04039-116">Weitere Informationen finden Sie unter [Erstellen einer Verbindung mit einem WMI-Namespace](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="04039-116">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="04039-117">Rufen Sie mithilfe [](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \\ \\ \\ von [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)einen Zeiger auf IWbemServices für den Stamm-CIMV2-Namespace auf einem Remote Computer ab.</span><span class="sxs-lookup"><span data-stu-id="04039-117">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the \\\\root\\cimv2 namespace on a remote computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="04039-118">Beim Herstellen einer Verbindung mit einem Remote Computer müssen Sie den Computernamen, die Domäne, den Benutzernamen und das Kennwort des Remote Computers kennen, mit dem Sie eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="04039-118">When connecting to a remote computer, you need to know the computer name, domain, user name, and password of the remote computer you are connecting to.</span></span> <span data-ttu-id="04039-119">Diese Attribute werden alle an die **IWBEMLocator:: ConnectServer** -Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="04039-119">These attributes are all passed into the **IWbemLocator::ConnectServer** method.</span></span> <span data-ttu-id="04039-120">Stellen Sie außerdem sicher, dass der Benutzername auf dem Computer, der versucht, eine Verbindung mit dem Remote Computer herzustellen, über die richtigen Zugriffsberechtigungen auf dem Remote Computer verfügt.</span><span class="sxs-lookup"><span data-stu-id="04039-120">Also, ensure the user name on the computer that is trying to connect to the remote computer has the correct access privileges on the remote computer.</span></span> <span data-ttu-id="04039-121">Weitere Informationen finden Sie unter [Herstellen einer Verbindung über die Windows-Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span><span class="sxs-lookup"><span data-stu-id="04039-121">For more information, see [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span> <span data-ttu-id="04039-122">Informationen zum Herstellen einer Verbindung mit dem lokalen Computer finden Sie unter [Beispiel: Informationen zum Herstellen von WMI-Daten vom lokalen Computer](example--getting-wmi-data-from-the-local-computer.md) und zum [Erstellen einer Verbindung mit einem WMI-Namespace](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="04039-122">To connect to the local computer, see [Example: Getting WMI Data from the Local Computer](example--getting-wmi-data-from-the-local-computer.md) and [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

    <span data-ttu-id="04039-123">Bei der Handhabung von Benutzernamen und Kenn Wörtern empfiehlt es sich, dass der Benutzer zur Eingabe der Informationen aufgefordert wird, die Informationen verwendet und die Informationen dann gelöscht werden, damit die Daten weniger wahrscheinlich von einem nicht autorisierten Benutzer abgefangen werden.</span><span class="sxs-lookup"><span data-stu-id="04039-123">When handling user names and passwords, it is recommended that the user be prompted for the information, use the information, and then delete the information, so that there is less of a chance of the information being intercepted by an unauthorized user.</span></span> <span data-ttu-id="04039-124">In Schritt 4 im folgenden Beispielcode wird " [**roduipromptforanmelde**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) " verwendet, um den Benutzernamen und das Kennwort zu erhalten, und anschließend wird " [**securezeromemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) " verwendet, um die Informationen zu entfernen, nachdem Sie in " [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)" verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="04039-124">Step 4 in the example code below uses [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to get the user name and password, and then uses [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) to get rid of the information after it is used in [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="04039-125">Weitere Informationen finden Sie unter [behandeln](/windows/desktop/SecBP/handling-passwords) von Kenn Wörtern und [anfordern von Anmelde Informationen für den Benutzer](/windows/desktop/SecBP/asking-the-user-for-credentials) auf MSDN.</span><span class="sxs-lookup"><span data-stu-id="04039-125">For more information, see [Handling Passwords](/windows/desktop/SecBP/handling-passwords) and [Asking the User for Credentials](/windows/desktop/SecBP/asking-the-user-for-credentials) on MSDN.</span></span>

5.  <span data-ttu-id="04039-126">Erstellen Sie eine [COAUTHIDENTITY](/windows/win32/api/wtypesbase/ns-wtypesbase-coauthidentity) -Struktur, um Anmelde Informationen zum Festlegen der Proxy Sicherheit bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="04039-126">Create a [COAUTHIDENTITY](/windows/win32/api/wtypesbase/ns-wtypesbase-coauthidentity) structure to provide credentials for setting the proxy security.</span></span>
6.  <span data-ttu-id="04039-127">Legen Sie die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Proxy Sicherheit fest, damit der WMI-Dienst die Identität des Clients durch Aufrufen von [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="04039-127">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="04039-128">Weitere Informationen finden Sie unter [Festlegen der Sicherheitsstufen für eine WMI-Verbindung](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="04039-128">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

7.  <span data-ttu-id="04039-129">Verwenden Sie den [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Zeiger, um WMI-Anforderungen zu stellen.</span><span class="sxs-lookup"><span data-stu-id="04039-129">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests of WMI.</span></span> <span data-ttu-id="04039-130">Eine Abfrage wird ausgeführt, um den Namen des Betriebssystems und den Umfang des freien physischen Speichers durch Aufrufen von [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)abzurufen.</span><span class="sxs-lookup"><span data-stu-id="04039-130">A query is executed to obtain the name of the operating system and the amount of free physical memory by calling [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span></span>

    <span data-ttu-id="04039-131">Die folgende WQL-Abfrage ist eines der Methodenargumente.</span><span class="sxs-lookup"><span data-stu-id="04039-131">The following WQL query is one of the method arguments.</span></span>

    `SELECT * FROM Win32_OperatingSystem`

    <span data-ttu-id="04039-132">Das Ergebnis dieser Abfrage wird in einem [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Zeiger gespeichert.</span><span class="sxs-lookup"><span data-stu-id="04039-132">The result of this query is stored in an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer.</span></span> <span data-ttu-id="04039-133">Auf diese Weise können die Datenobjekte aus der Abfrage SemiSynchron mit der **ienumwbemclassobject** -Schnittstelle abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="04039-133">This allows the data objects from the query to be retrieved semisynchronously with the **IEnumWbemClassObject** interface.</span></span> <span data-ttu-id="04039-134">Weitere Informationen finden Sie unter Auflisten von [WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="04039-134">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span> <span data-ttu-id="04039-135">Informationen zum asynchronen ermitteln der Daten finden Sie unter [Beispiel: Asynchrones erhalten von WMI-Daten vom lokalen Computer](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span><span class="sxs-lookup"><span data-stu-id="04039-135">For getting the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

    <span data-ttu-id="04039-136">Weitere Informationen zum Erstellen von WMI-Anforderungen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md), [Abfragen von WMI](querying-wmi.md)und [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="04039-136">For more information about making requests of WMI, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Querying WMI](querying-wmi.md), and [Calling a Method](calling-a-method.md).</span></span>

8.  <span data-ttu-id="04039-137">Legen Sie [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -enumeratorproxysicherheit fest.</span><span class="sxs-lookup"><span data-stu-id="04039-137">Set [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) enumerator proxy security.</span></span> <span data-ttu-id="04039-138">Stellen Sie sicher, dass Sie die Anmelde Informationen aus dem Arbeitsspeicher löschen, nachdem Sie Sie verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="04039-138">Make sure to erase the credentials from memory after you have finished using them.</span></span>

    <span data-ttu-id="04039-139">Weitere Informationen finden Sie unter [Festlegen der Sicherheit für IWbemServices und andere](setting-the-security-on-iwbemservices-and-other-proxies.md)Proxys.</span><span class="sxs-lookup"><span data-stu-id="04039-139">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

9.  <span data-ttu-id="04039-140">Hiermit werden die Daten aus der WQL-Abfrage angezeigt und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="04039-140">Get and display the data from the WQL query.</span></span> <span data-ttu-id="04039-141">Der [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Zeiger ist mit den Datenobjekten verknüpft, die von der Abfrage zurückgegeben wurden, und die Datenobjekte können mit der [**ienumwbemclassobject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="04039-141">The [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer is linked to the data objects that the query returned, and the data objects can be retrieved with the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) method.</span></span> <span data-ttu-id="04039-142">Diese Methode verknüpft die Datenobjekte mit einem [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Zeiger, der an die-Methode übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="04039-142">This method links the data objects to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that is passed into the method.</span></span> <span data-ttu-id="04039-143">Verwenden Sie die [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) -Methode, um die gewünschten Informationen aus den Datenobjekten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="04039-143">Use the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method to get the desired information from the data objects.</span></span>

    <span data-ttu-id="04039-144">Das folgende Codebeispiel wird verwendet, um die- `Name` Eigenschaft aus dem-Datenobjekt zu erhalten, das den Namen des Betriebssystems bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="04039-144">The following code example is used to get the `Name` property from the data object, which provides the name of the operating system.</span></span>

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    wcout << " OS Name : " << vtProp.bstrVal << endl;
    ```

    

    <span data-ttu-id="04039-145">Nachdem der Wert der `Name` Eigenschaft in der [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Variablen gespeichert `vtProp` wurde, kann er dem Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="04039-145">Once the value of the `Name` property is stored in the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) variable `vtProp`, it can then be displayed to the user.</span></span>

    <span data-ttu-id="04039-146">Im folgenden Codebeispiel wird gezeigt, wie die [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Variable wieder verwendet werden kann, um den Wert des freien physischen Speichers zu speichern und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="04039-146">The following code example shows how the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) variable can be used again to store and display the value of the amount of free physical memory.</span></span>

    ```C++
    hr = pclsObj->Get(L"FreePhysicalMemory",
        0, &vtProp, 0, 0);
    wcout << " Free physical memory (in kilobytes): "
        << vtProp.uintVal << endl;
    ```

    

    <span data-ttu-id="04039-147">Weitere Informationen finden Sie unter Auflisten von [WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="04039-147">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

<span data-ttu-id="04039-148">Im folgenden Codebeispiel wird veranschaulicht, wie WMI-Daten von einem Remote Computer aus SemiSynchron abgeraten werden.</span><span class="sxs-lookup"><span data-stu-id="04039-148">The following code example shows how to get WMI data semisynchronously from a remote computer.</span></span>


```C++
#define _WIN32_DCOM
#define UNICODE
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
#pragma comment(lib, "credui.lib")
#pragma comment(lib, "comsuppw.lib")
#include <wincred.h>
#include <strsafe.h>

int __cdecl main(int argc, char **argv)
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
        RPC_C_IMP_LEVEL_IDENTIFY,    // Default Impersonation  
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

    // Get the user name and password for the remote computer
    CREDUI_INFO cui;
    bool useToken = false;
    bool useNTLM = true;
    wchar_t pszName[CREDUI_MAX_USERNAME_LENGTH+1] = {0};
    wchar_t pszPwd[CREDUI_MAX_PASSWORD_LENGTH+1] = {0};
    wchar_t pszDomain[CREDUI_MAX_USERNAME_LENGTH+1];
    wchar_t pszUserName[CREDUI_MAX_USERNAME_LENGTH+1];
    wchar_t pszAuthority[CREDUI_MAX_USERNAME_LENGTH+1];
    BOOL fSave;
    DWORD dwErr;

    memset(&cui,0,sizeof(CREDUI_INFO));
    cui.cbSize = sizeof(CREDUI_INFO);
    cui.hwndParent = NULL;
    // Ensure that MessageText and CaptionText identify
    // what credentials to use and which application requires them.
    cui.pszMessageText = TEXT("Press cancel to use process token");
    cui.pszCaptionText = TEXT("Enter Account Information");
    cui.hbmBanner = NULL;
    fSave = FALSE;

    dwErr = CredUIPromptForCredentials( 
        &cui,                             // CREDUI_INFO structure
        TEXT(""),                         // Target for credentials
        NULL,                             // Reserved
        0,                                // Reason
        pszName,                          // User name
        CREDUI_MAX_USERNAME_LENGTH+1,     // Max number for user name
        pszPwd,                           // Password
        CREDUI_MAX_PASSWORD_LENGTH+1,     // Max number for password
        &fSave,                           // State of save check box
        CREDUI_FLAGS_GENERIC_CREDENTIALS |// flags
        CREDUI_FLAGS_ALWAYS_SHOW_UI |
        CREDUI_FLAGS_DO_NOT_PERSIST);  

    if(dwErr == ERROR_CANCELLED)
    {
        useToken = true;
    }
    else if (dwErr)
    {
        cout << "Did not get credentials " << dwErr << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;      
    }

    // change the computerName strings below to the full computer name
    // of the remote computer
    if(!useNTLM)
    {
        StringCchPrintf(pszAuthority, CREDUI_MAX_USERNAME_LENGTH+1, L"kERBEROS:%s", L"COMPUTERNAME");
    }

    // Connect to the remote root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    //---------------------------------------------------------
   
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTERNAME\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
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


    // step 5: --------------------------------------------------
    // Create COAUTHIDENTITY that can be used for setting security on proxy

    COAUTHIDENTITY *userAcct =  NULL ;
    COAUTHIDENTITY authIdent;

    if( !useToken )
    {
        memset(&authIdent, 0, sizeof(COAUTHIDENTITY));
        authIdent.PasswordLength = wcslen (pszPwd);
        authIdent.Password = (USHORT*)pszPwd;

        LPWSTR slash = wcschr (pszName, L'\\');
        if( slash == NULL )
        {
            cout << "Could not create Auth identity. No domain specified\n" ;
            pSvc->Release();
            pLoc->Release();     
            CoUninitialize();
            return 1;               // Program has failed.
        }

        StringCchCopy(pszUserName, CREDUI_MAX_USERNAME_LENGTH+1, slash+1);
        authIdent.User = (USHORT*)pszUserName;
        authIdent.UserLength = wcslen(pszUserName);

        StringCchCopyN(pszDomain, CREDUI_MAX_USERNAME_LENGTH+1, pszName, slash - pszName);
        authIdent.Domain = (USHORT*)pszDomain;
        authIdent.DomainLength = slash - pszName;
        authIdent.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

        userAcct = &authIdent;

    }

    // Step 6: --------------------------------------------------
    // Set security levels on a WMI connection ------------------

    hres = CoSetProxyBlanket(
       pSvc,                           // Indicates the proxy to set
       RPC_C_AUTHN_DEFAULT,            // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_DEFAULT,            // RPC_C_AUTHZ_xxx
       COLE_DEFAULT_PRINCIPAL,         // Server principal name 
       RPC_C_AUTHN_LEVEL_PKT_PRIVACY,  // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE,    // RPC_C_IMP_LEVEL_xxx
       userAcct,                       // client identity
       EOAC_NONE                       // proxy capabilities 
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

    // Step 7: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("Select * from Win32_OperatingSystem"),
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

    // Step 8: -------------------------------------------------
    // Secure the enumerator proxy
    hres = CoSetProxyBlanket(
        pEnumerator,                    // Indicates the proxy to set
        RPC_C_AUTHN_DEFAULT,            // RPC_C_AUTHN_xxx
        RPC_C_AUTHZ_DEFAULT,            // RPC_C_AUTHZ_xxx
        COLE_DEFAULT_PRINCIPAL,         // Server principal name 
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,  // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE,    // RPC_C_IMP_LEVEL_xxx
        userAcct,                       // client identity
        EOAC_NONE                       // proxy capabilities 
        );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket on enumerator. Error code = 0x" 
             << hex << hres << endl;
        pEnumerator->Release();
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // When you have finished using the credentials,
    // erase them from memory.
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
    SecureZeroMemory(pszUserName, sizeof(pszUserName));
    SecureZeroMemory(pszDomain, sizeof(pszDomain));


    // Step 9: -------------------------------------------------
    // Get the data from the query in step 7 -------------------
 
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

        // Get the value of the FreePhysicalMemory property
        hr = pclsObj->Get(L"FreePhysicalMemory",
            0, &vtProp, 0, 0);
        wcout << " Free physical memory (in kilobytes): "
            << vtProp.uintVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
        pclsObj = NULL;
    }

    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();
    if( pclsObj )
    {
        pclsObj->Release();
    }
    
    CoUninitialize();

    return 0;   // Program successfully completed.
    
}
```



 

 
