---
description: Bei einer synchronen Abfrage handelt es sich um eine Abfrage, die die Kontrolle über den Prozess der Anwendung für die Dauer der Abfrage behält.
ms.assetid: 628e9a31-7b0d-4099-bfa5-56330bb4eb6b
ms.tgt_platform: multiple
title: Aufrufen einer synchronen Abfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d4bb2ff61a1c94bf7390a65d51e773ad943a45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362980"
---
# <a name="invoking-a-synchronous-query"></a>Aufrufen einer synchronen Abfrage

Bei einer synchronen Abfrage handelt es sich um eine Abfrage, die die Kontrolle über den Prozess der Anwendung für die Dauer der Abfrage behält. Eine synchrone Abfrage erfordert einen einzelnen Schnittstellen Rückruf und ist daher einfacher als ein asynchroner-Befehl. Eine synchrone Abfrage hat jedoch die Möglichkeit, Ihre Anwendung für große Abfragen oder Abfragen über ein Netzwerk zu sperren.

Im folgenden Verfahren wird beschrieben, wie eine synchrone Datenabfrage mithilfe von PowerShell ausgegeben wird.

**So geben Sie eine synchrone Datenabfrage in PowerShell aus**

-   Beschreiben Sie die WMI-Abfrage mithilfe des WMI-Cmdlets [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) und des *-Query-* Parameters. Das-Cmdlet gibt entweder ein einzelnes-Objekt oder eine Auflistung von-Objekten zurück, abhängig von der Anzahl der Objekte, die der Abfrage entsprechen.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

Im folgenden Verfahren wird beschrieben, wie eine synchrone Datenabfrage mit c# ausgegeben wird.

**So geben Sie eine synchrone Datenabfrage in c# aus (Microsoft. Management. Infrastructure)**

1.  Beschreiben Sie Ihre Abfrage mit "cimsession. queryinstance" in WMI. Diese Methode gibt eine Auflistung von ciminstance-Objekten zurück.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM Win32_LogicalDisk";
    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstances = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

2.  Verwenden Sie standardmäßige c#-sprach Erfassungs Techniken für den Zugriff auf jedes zurückgegebene Objekt

    ```CSharp
    foreach (CimInstance drive in queryInstances)
    {
       Console.WriteLine(drive.CimInstanceProperties["DeviceID"]);
    }
    ```

    

Im folgenden Verfahren wird beschrieben, wie eine synchrone Datenabfrage mit c# ausgegeben wird.

**So geben Sie eine synchrone Datenabfrage in c# aus (System. Management)**

1.  Erstellen Sie die Abfrage mit einem [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) -Objekt, und rufen Sie die Informationen mit einem Aufrufen von [ManagementObjectSearcher. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get)ab.

    Diese Methode gibt ein [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) -Objekt zurück.

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection objCol = mgmtObjSearcher.Get();
    ```

    

2.  Verwenden Sie standardmäßige c#-sprach Erfassungs Techniken für den Zugriff auf jedes zurückgegebene Objekt

    ```CSharp
    foreach (ManagementObject drive in objCol)
    {
       Console.WriteLine(drive["DeviceID"]);
    }
    ```

    

Im folgenden Verfahren wird beschrieben, wie eine synchrone Datenabfrage mithilfe von VBScript ausgegeben wird.

**So geben Sie eine synchrone Datenabfrage in VBScript aus**

1.  Beschreiben Sie die WMI-Abfrage mit [**SWbemServices.Execquery**](swbemservices-execquery.md). Diese Methode gibt ein " [**errbemubjectset**](swbemobjectset.md)" zurück.

    ```VB
    GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
    ```

    

2.  Verwenden Sie Standard Skripts zur [Skript sprach Auflistung](accessing-a-collection.md) , um auf jedes zurückgegebene Objekt zuzugreifen.

    ```VB
    for each Service in _ 
        GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
        WScript.Echo "  "& Service.DisplayName & " [", Service.Name, "]"
    next
    ```

    

Im folgenden Verfahren wird beschrieben, wie eine synchrone Datenabfrage mithilfe von C++ ausgegeben wird.

**So geben Sie eine synchrone Abfrage in C++ aus**

1.  Beschreiben Sie Ihre Abfrage für WMI durch einen Befehl von [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).

    Die [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) -Methode nimmt eine WQL-Such Zeichenfolge als Parameter an, der die Abfrage beschreibt. WMI führt die Abfrage aus und gibt einen [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Schnittstellen Zeiger zurück. Über die **ienumwbemclassobject** -Schnittstelle können Sie auf die Klassen oder Instanzen zugreifen, aus denen das Resultset besteht.

2.  Nachdem Sie die Abfrage erhalten haben, können Sie die Abfrage mit einem [**ienumwbemclassobject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next)-Rückruf auflisten. Weitere Informationen finden Sie unter Auflisten von [WMI](enumerating-wmi.md).

    Für das folgende Codebeispiel sind die folgenden Verweise und \# include-Anweisungen erforderlich, um ordnungsgemäß zu kompilieren.

    ```C++
    #include <wbemidl.h>
    #include <iostream>
    using namespace std;
    ```

    

    Im folgenden Codebeispiel wird beschrieben, wie die-Objekte, die die Benutzer und Gruppen in WMI darstellen, abgefragt werden.

    ```C++
    void ExecQuerySync(IWbemServices *pSvc)
    {
        // Query for all users and groups.

        BSTR Language = SysAllocString(L"WQL");
        BSTR Query = SysAllocString(L"SELECT * FROM __Namespace");

        // Initialize the IEnumWbemClassObject pointer.
        IEnumWbemClassObject *pEnum = 0;

        // Issue the query.
        HRESULT hRes = pSvc->ExecQuery(
            Language,
            Query,
            WBEM_FLAG_FORWARD_ONLY,         // Flags
            0,                              // Context
            &pEnum
            );

        SysFreeString(Query);
        SysFreeString(Language);

        if (hRes != 0)
        {
            printf("Error\n");
            return;
        }
        
        ULONG uTotal = 0;

        // Retrieve the objects in the result set.
        for (;;)
        {
            IWbemClassObject *pObj = 0;
            ULONG uReturned = 0;

            hRes = pEnum->Next(
                0,                  // Time out
                1,                  // One object
                &pObj,
                &uReturned
                );

            uTotal += uReturned;

            if (uReturned == 0)
                break;

            // Use the object.
            
            // ...
            
            // Release it.
            // ===========
            
            pObj->Release();    // Release objects not owned.            
        }

        // All done.
        pEnum->Release();
    }
    ```

    

 

 
