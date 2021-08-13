---
description: Eine synchrone Abfrage ist eine Abfrage, die die Kontrolle über den Prozess Ihrer Anwendung für die Dauer der Abfrage behält.
ms.assetid: 628e9a31-7b0d-4099-bfa5-56330bb4eb6b
ms.tgt_platform: multiple
title: Aufrufen einer synchronen Abfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f089ac5a2d315aa55fe7af7e648d3b001bae032b92ed5b7d67a1b6b120b96561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556118"
---
# <a name="invoking-a-synchronous-query"></a>Aufrufen einer synchronen Abfrage

Eine synchrone Abfrage ist eine Abfrage, die die Kontrolle über den Prozess Ihrer Anwendung für die Dauer der Abfrage behält. Eine synchrone Abfrage erfordert einen einzelnen Schnittstellenaufruf und ist daher einfacher als ein asynchroner Aufruf. Eine synchrone Abfrage hat jedoch das Potenzial, Ihre Anwendung für große Abfragen oder Abfragen über ein Netzwerk zu sperren.

Im folgenden Verfahren wird beschrieben, wie Sie eine synchrone Datenabfrage mithilfe von PowerShell ausführen.

**So stellen Sie eine synchrone Datenabfrage in PowerShell aus**

-   Beschreiben Sie Ihre WMI-Abfrage mithilfe des [WMI-Cmdlets Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) und des *Parameters -query.* Das Cmdlet gibt entweder ein einzelnes Objekt oder eine Auflistung von -Objekten zurück, je nachdem, wie viele Objekte zur Abfrage passen.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

Im folgenden Verfahren wird beschrieben, wie Eine synchrone Datenabfrage mit C# ausgegeben wird.

**So führen Sie eine synchrone Datenabfrage in C# aus (Microsoft.Management.Infrastructure)**

1.  Beschreiben Sie Ihre WMI-Abfrage mithilfe von CimSession.QueryInstances. Diese Methode gibt eine Auflistung von CimInstance-Objekten zurück.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM Win32_LogicalDisk";
    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstances = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

2.  Verwenden Sie standardmäßige C#-Sprachsammlungsverfahren, um auf jedes zurückgegebene Objekt zuzugreifen.

    ```CSharp
    foreach (CimInstance drive in queryInstances)
    {
       Console.WriteLine(drive.CimInstanceProperties["DeviceID"]);
    }
    ```

    

Im folgenden Verfahren wird beschrieben, wie Eine synchrone Datenabfrage mit C# ausgegeben wird.

**So führen Sie eine synchrone Datenabfrage in C# aus (System.Management)**

1.  Erstellen Sie die Abfrage mit einem [ManagementObjectSearcher-Objekt,](/dotnet/api/system.management.managementobjectsearcher) und rufen Sie die Informationen mit einem Aufruf von [ManagementObjectSearcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get)ab.

    Diese Methode gibt ein [ManagementObjectCollection-Objekt](/dotnet/api/system.management.managementobjectcollection) zurück.

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection objCol = mgmtObjSearcher.Get();
    ```

    

2.  Verwenden Sie standardmäßige C#-Sprachsammlungsverfahren, um auf jedes zurückgegebene Objekt zuzugreifen.

    ```CSharp
    foreach (ManagementObject drive in objCol)
    {
       Console.WriteLine(drive["DeviceID"]);
    }
    ```

    

Im folgenden Verfahren wird beschrieben, wie Sie eine synchrone Datenabfrage mitHILFE von VBScript ausführen.

**So stellen Sie eine synchrone Datenabfrage in VBScript aus**

1.  Beschreiben Sie Ihre WMI-Abfrage mit [**SWbemServices.ExecQuery**](swbemservices-execquery.md). Diese Methode gibt ein [**SWbemObjectSet**](swbemobjectset.md)zurück.

    ```VB
    GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
    ```

    

2.  Verwenden Sie Standardmäßige Techniken zur [Skriptsprachsammlung,](accessing-a-collection.md) um auf jedes zurückgegebene Objekt zuzugreifen.

    ```VB
    for each Service in _ 
        GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
        WScript.Echo "  "& Service.DisplayName & " [", Service.Name, "]"
    next
    ```

    

Im folgenden Verfahren wird beschrieben, wie Eine synchrone Datenabfrage mit C++ ausgegeben wird.

**So stellen Sie eine synchrone Abfrage in C++ aus**

1.  Beschreiben Sie Ihre WMI-Abfrage durch einen Aufruf von [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).

    Die [**ExecQuery-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) verwendet eine WQL-Suchzeichenfolge als Parameter, der Ihre Abfrage beschreibt. WMI führt die Abfrage aus und gibt einen [**IEnumWbemClassObject-Schnittstellenzeiger**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) zurück. Über die **IEnumWbemClassObject-Schnittstelle** können Sie auf die Klassen oder Instanzen zugreifen, die das Resultset bilden.

2.  Nachdem Sie die Abfrage erhalten haben, können Sie Die Abfrage mit einem Aufruf von [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next)auflisten. Weitere Informationen finden Sie unter [Aufzählen von WMI.](enumerating-wmi.md)

    Das folgende Codebeispiel erfordert die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.

    ```C++
    #include <wbemidl.h>
    #include <iostream>
    using namespace std;
    ```

    

    Im folgenden Codebeispiel wird beschrieben, wie Die Objekte abgefragt werden, die die Benutzer und Gruppen in WMI darstellen.

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

    

 

 
