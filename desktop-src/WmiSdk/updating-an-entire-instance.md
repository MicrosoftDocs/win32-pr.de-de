---
description: Die gängigste Methode, eine WMI-Klasseninstanz zu aktualisieren, besteht darin, die gesamte Instanz gleichzeitig zu aktualisieren.
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: Aktualisieren einer gesamten Instanz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b334d1d89a7e936e2c9d80aebfbeecb430bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217115"
---
# <a name="updating-an-entire-instance"></a>Aktualisieren einer gesamten Instanz

Die gängigste Methode, eine WMI-Klasseninstanz zu aktualisieren, besteht darin, die gesamte Instanz gleichzeitig zu aktualisieren. Wenn Sie eine gesamte Instanz aktualisieren, muss die Instanz von WMI nicht in einzelne Eigenschaften analysiert und an Ihre Anwendung gesendet werden. Stattdessen kann WMI Ihnen einfach die gesamte-Instanz senden. Wenn Sie fertig sind, kann die gesamte geänderte Instanz von WMI über die ursprüngliche Instanz kopiert werden.

Im folgenden Verfahren wird beschrieben, wie Sie eine Instanz mithilfe von PowerShell ändern oder aktualisieren.

**So ändern oder aktualisieren Sie eine Instanz mithilfe von PowerShell**

1.  Rufen Sie eine lokale Kopie des Objekts mit einem Get-WMIObject-Befehl ab.

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  Zeigen Sie ggf. die Eigenschaften des-Objekts an, indem Sie die Properties-Auflistung aufzurufen.

    Obwohl es nicht erforderlich ist, sollten Sie den Wert der-Eigenschaft kennen, bevor Sie ihn ändern.

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  Nehmen Sie Änderungen an den Eigenschaften des lokalen Objekts vor.

    Dadurch wird nur die lokale Kopie geändert. Zum Speichern der Änderungen an WMI müssen Sie die gesamte Kopie wieder im WMI-Repository platzieren.

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  Versetzen Sie das Objekt mithilfe eines Aufrufens der Put-Methode wieder in das WMI-Repository.

    ```PowerShell
    $mySettings.Put()
    ```

    

Im folgenden Verfahren wird beschrieben, wie Sie eine Instanz mit c# ändern oder aktualisieren.

**So ändern oder aktualisieren Sie eine Instanz mit c# (Microsoft. Management. Infrastructure)**

1.  Rufen Sie eine lokale Kopie des-Objekts mit einem [cimsession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85))-Befehl ab, wie unter [Abrufen einer WMI-Instanz](retrieving-an-instance.md)beschrieben.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "win32_logicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));

    CimSession session = CimSession.Create("localhost");
    CimInstance myDisk = session.GetInstance(Namespace, diskDrive);
    ```

    

2.  Zeigen Sie ggf. die Eigenschaften des-Objekts an, indem Sie die Properties-Auflistung aufzurufen.

    Obwohl es nicht erforderlich ist, sollten Sie den Wert der-Eigenschaft kennen, bevor Sie ihn ändern.

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  Nehmen Sie Änderungen an den Eigenschaften des lokalen Objekts vor.

    Dadurch wird nur die lokale Kopie geändert. Zum Speichern der Änderungen an WMI müssen Sie die gesamte Kopie wieder im WMI-Repository platzieren.

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  Versetzen Sie das Objekt mithilfe eines Aufrufens von [cimsession. modifyinstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85))wieder in das WMI-Repository.

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

Im folgenden Verfahren wird beschrieben, wie Sie eine Instanz mithilfe von PowerShell ändern oder aktualisieren.

> [!Note]  
> **System. Management** war der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. die APIs in diesem Namespace sind jedoch in der Regel langsamer und werden relativ zu ihren moderneren **Microsoft. Management. Infrastructure** -Entsprechungen nicht auch skaliert.

 

**So ändern oder aktualisieren Sie eine Instanz mit c# (Microsoft. Management)**

1.  Rufen Sie eine lokale Kopie des Objekts mit einem-Befehl von [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get)ab.

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  Zeigen Sie ggf. die Eigenschaften des-Objekts an, indem Sie die Properties-Auflistung aufzurufen.

    Obwohl es nicht erforderlich ist, sollten Sie den Wert der-Eigenschaft kennen, bevor Sie ihn ändern.

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  Nehmen Sie Änderungen an den Eigenschaften des lokalen Objekts vor.

    Dadurch wird nur die lokale Kopie geändert. Zum Speichern der Änderungen an WMI müssen Sie die gesamte Kopie wieder im WMI-Repository platzieren.

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  Versetzen Sie das Objekt mithilfe eines Aufrufens der [ManagementObject. Put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) -oder-Methode wieder in das WMI-Repository.

    ```CSharp
    myDisk.Put();
    ```

    

Im folgenden Verfahren wird beschrieben, wie Sie eine Instanz mit VBScript ändern oder aktualisieren.

**So ändern oder aktualisieren Sie eine Instanz mit VBScript**

1.  Rufen Sie eine lokale Kopie des Objekts mit einem Aufrufen von **GetObject** ab.
2.  Zeigen Sie ggf. die Eigenschaften des-Objekts an, indem Sie [**die \_ Properties**](swbemobject-properties-.md) -Methode aufzurufen.

    Obwohl es nicht erforderlich ist, sollten Sie den Wert der-Eigenschaft kennen, bevor Sie ihn ändern.

3.  Nehmen Sie Änderungen an den Objekteigenschaften vor, indem Sie die Methode " [**Swap-Eigenschaft. Value**](swbemproperty-value.md) " aufzurufen.

    Die **value** -Methode ändert nur die lokale Kopie. Zum Speichern der Änderungen an WMI müssen Sie die gesamte Kopie wieder im WMI-Repository platzieren.

4.  Versetzen Sie das Objekt wieder in das WMI-Repository, indem Sie die Methoden " [**errbewbject. Put \_**](swbemobject-put-.md) " oder " [**errbewbject. putasync \_**](swbemobject-putasync-.md) " aufrufen.

Wie die Namen impliziert, werden Updates synchron [**eingefügt \_**](swbemobject-put-.md) , während [**putasync \_**](swbemobject-putasync-.md) asynchron aktualisiert wird. Beide Methoden kopieren die ursprüngliche Instanz mit der geänderten Instanz. Um die Nutzung der asynchronen Verarbeitung zu nutzen, müssen Sie jedoch ein " [**taubemsink**](swbemsink.md) "-Objekt erstellen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Im folgenden Verfahren wird beschrieben, wie eine Instanz mit C++ geändert oder aktualisiert wird.

**So ändern oder aktualisieren Sie eine Instanz mithilfe von C++**

1.  Rufen Sie eine lokale Kopie der-Instanz mit einem Befehl zum Aufrufen von [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)ab.
2.  Zeigen Sie ggf. die Eigenschaften des Objekts mit einem Befehl an, um [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)aufzurufen.

    Obwohl es nicht erforderlich ist, sollten Sie den Wert der-Eigenschaft kennen, bevor Sie ihn ändern.

3.  Nehmen Sie alle notwendigen Änderungen an der Kopie mit einem Befehl [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)vor.

    Mit der **Put** -Methode wird nur die lokale Kopie geändert. Zum Speichern der Änderungen an WMI müssen Sie die gesamte Kopie wieder im WMI-Repository platzieren.

4.  Fügen Sie die Kopie zurück in das WMI-Repository ein, indem Sie die Methoden [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) oder [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) aufrufen.

    Wie die Namen impliziert, aktualisiert **PutInstance** synchron, während [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) asynchron aktualisiert wird. Beide Methoden kopieren die ursprüngliche Instanz mit der geänderten Instanz. Um die asynchrone Verarbeitung zu nutzen, müssen Sie jedoch die [**iwbebobjectsink**](iwbemobjectsink.md) -Schnittstelle implementieren.

    Beachten Sie, dass ein Aktualisierungs Vorgang für eine Instanz, die zu einer Klassenhierarchie gehört, aufgrund eines Fehlers, der eine andere Klasse in der Hierarchie einschließt, möglicherweise nicht erfolgreich ist. WMI Ruft die [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) -Methode für jeden Anbieter auf, der für die Klassen verantwortlich ist, von denen die Klasse, die die ursprüngliche Instanz besitzt, abgeleitet ist. Wenn einer dieser Anbieter ausfällt, tritt bei der ursprünglichen Update Anforderung ein Fehler auf. Weitere Informationen finden Sie im Abschnitt "Hinweise" von [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).

Weitere Informationen finden Sie unter [Aufrufen einer Anbieter Methode](calling-a-provider-method.md).

> [!Note]  
> Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

 

 
