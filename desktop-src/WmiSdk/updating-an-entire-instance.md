---
description: Die gängigste Möglichkeit zum Aktualisieren einer WMI-Klasseninstanz ist das gleichzeitige Aktualisieren der gesamten Instanz.
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: Aktualisieren einer gesamten Instanz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41cac29805eeff1f8c659c0bee6832eb65e9e6b5bdee8cd15bd0a052247a70e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995539"
---
# <a name="updating-an-entire-instance"></a>Aktualisieren einer gesamten Instanz

Die gängigste Möglichkeit zum Aktualisieren einer WMI-Klasseninstanz ist das gleichzeitige Aktualisieren der gesamten Instanz. Durch aktualisieren einer gesamten Instanz muss WMI die Instanz nicht in einzelne Eigenschaften analysieren und an Ihre Anwendung senden. Stattdessen kann WMI ihnen einfach die gesamte Instanz senden. Wenn Sie fertig sind, kann WMI dann ihre gesamte geänderte Instanz über die ursprüngliche Instanz kopieren.

Im folgenden Verfahren wird beschrieben, wie Sie eine Instanz mithilfe von PowerShell ändern oder aktualisieren.

**So ändern oder aktualisieren Sie eine Instanz mithilfe von PowerShell**

1.  Rufen Sie eine lokale Kopie des -Objekts mit einem Aufruf von Get-WmiObject ab.

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  Zeigen Sie bei Bedarf die Eigenschaften des -Objekts mit einem Aufruf der Properties-Auflistung an.

    Obwohl dies nicht erforderlich ist, möchten Sie möglicherweise den Wert der Eigenschaft kennen, bevor Sie ihn ändern.

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  Nehmen Sie Änderungen an den eigenschaften des lokalen Objekts vor.

    Dadurch wird nur die lokale Kopie geändert. Um Ihre Änderungen an WMI zu speichern, müssen Sie die gesamte Kopie wieder in das WMI-Repository platzieren.

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  Platzieren Sie das Objekt mithilfe eines Aufrufs der Put-Methode wieder im WMI-Repository.

    ```PowerShell
    $mySettings.Put()
    ```

    

Im folgenden Verfahren wird beschrieben, wie Eine -Instanz mithilfe von C# geändert oder aktualisiert wird.

**So ändern oder aktualisieren Sie eine Instanz mit C# (Microsoft.Management.Infrastructure)**

1.  Rufen Sie eine lokale Kopie des -Objekts mit einem Aufruf von [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85))ab, wie unter [Abrufen einer WMI-Instanz beschrieben.](retrieving-an-instance.md)

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

    

2.  Zeigen Sie bei Bedarf die Eigenschaften des -Objekts mit einem Aufruf der Properties-Auflistung an.

    Obwohl dies nicht erforderlich ist, möchten Sie möglicherweise den Wert der Eigenschaft kennen, bevor Sie ihn ändern.

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  Nehmen Sie Änderungen an den eigenschaften des lokalen Objekts vor.

    Dadurch wird nur die lokale Kopie geändert. Um Ihre Änderungen an WMI zu speichern, müssen Sie die gesamte Kopie wieder in das WMI-Repository platzieren.

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  Platzieren Sie das Objekt mithilfe eines Aufrufs von [CimSession.ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85))wieder im WMI-Repository.

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

Im folgenden Verfahren wird beschrieben, wie Sie eine Instanz mithilfe von PowerShell ändern oder aktualisieren.

> [!Note]  
> **System.Management war** der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. Die APIs in diesem Namespace sind jedoch im Allgemeinen langsamer und werden im Vergleich zu ihren moderneren **Microsoft.Management.Infrastructure-Entsprechungen** nicht so gut skaliert.

 

**So ändern oder aktualisieren Sie eine Instanz mit C# (Microsoft.Management)**

1.  Rufen Sie eine lokale Kopie des -Objekts mit einem Aufruf von [ManagementObject.Get ab.](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get)

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  Zeigen Sie bei Bedarf die Eigenschaften des -Objekts mit einem Aufruf der Properties-Auflistung an.

    Obwohl dies nicht erforderlich ist, möchten Sie möglicherweise den Wert der Eigenschaft kennen, bevor Sie ihn ändern.

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  Nehmen Sie Änderungen an den eigenschaften des lokalen Objekts vor.

    Dadurch wird nur die lokale Kopie geändert. Um Ihre Änderungen an WMI zu speichern, müssen Sie die gesamte Kopie wieder in das WMI-Repository platzieren.

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  Platzieren Sie das Objekt mithilfe eines Aufrufs von [ManagementObject.Put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) oder der -Methode wieder im WMI-Repository.

    ```CSharp
    myDisk.Put();
    ```

    

Im folgenden Verfahren wird beschrieben, wie Eine -Instanz mit VBScript geändert oder aktualisiert wird.

**So ändern oder aktualisieren Sie eine Instanz mit VBScript**

1.  Rufen Sie eine lokale Kopie des -Objekts mit einem Aufruf von **GetObject ab.**
2.  Zeigen Sie bei Bedarf die Eigenschaften des -Objekts mit einem Aufruf der [**Properties-Methode \_**](swbemobject-properties-.md) an.

    Obwohl dies nicht erforderlich ist, möchten Sie möglicherweise den Wert der Eigenschaft kennen, bevor Sie ihn ändern.

3.  Nehmen Sie änderungen an den Objekteigenschaften mit einem Aufruf der [**SWbemProperty.Value-Methode**](swbemproperty-value.md) vor.

    Die **Value-Methode** ändert nur die lokale Kopie. Um Ihre Änderungen an WMI zu speichern, müssen Sie die gesamte Kopie wieder in das WMI-Repository platzieren.

4.  Platzieren Sie das Objekt mit einem Aufruf der [**Methoden SWbemObject.Put \_**](swbemobject-put-.md) oder [**SWbemObject.PutAsync \_**](swbemobject-putasync-.md) wieder im WMI-Repository.

Wie die Namen implizieren, [**werden \_ Updates**](swbemobject-put-.md) synchron und [**PutAsync \_**](swbemobject-putasync-.md) asynchron aktualisiert. Beide Methoden kopieren die ursprüngliche Instanz mit Ihrer geänderten Instanz. Um jedoch die asynchrone Verarbeitung nutzen zu können, müssen Sie ein [**SWbemSink-Objekt**](swbemsink.md) erstellen. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Im folgenden Verfahren wird beschrieben, wie Eine -Instanz mit C++ geändert oder aktualisiert wird.

**So ändern oder aktualisieren Sie eine Instanz mit C++**

1.  Rufen Sie eine lokale Kopie der -Instanz mit einem Aufruf von [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**IWbemServices::GetObjectAsync ab.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
2.  Zeigen Sie bei Bedarf die Eigenschaften des -Objekts mit einem Aufruf von [**IWbemClassObject::Get an.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)

    Obwohl dies nicht erforderlich ist, möchten Sie möglicherweise den Wert der Eigenschaft kennen, bevor Sie ihn ändern.

3.  Nehmen Sie alle erforderlichen Änderungen an der Kopie mit einem Aufruf von [**IWbemClassObject::P ut vor.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)

    Die **Put-Methode** ändert nur die lokale Kopie. Um Ihre Änderungen an WMI zu speichern, müssen Sie die gesamte Kopie wieder in das WMI-Repository platzieren.

4.  Platzieren Sie Ihre Kopie wieder im WMI-Repository, und rufen Sie die Methoden [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) oder [**IWbemServices::P utInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) auf.

    Wie die Namen implizieren, **wird PutInstance** synchron aktualisiert, während [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) asynchron aktualisiert wird. Beide Methoden kopieren die ursprüngliche Instanz mit Ihrer geänderten Instanz. Um jedoch die asynchrone Verarbeitung nutzen zu können, müssen Sie die [**IWbemObjectSink-Schnittstelle**](iwbemobjectsink.md) implementieren.

    Beachten Sie, dass ein Aktualisierungsvorgang für eine Instanz, die zu einer Klassenhierarchie gehört, aufgrund eines Fehlers im Zusammenhang mit einer anderen Klasse in der Hierarchie möglicherweise nicht erfolgreich ist. WMI ruft die [**PutInstanceAsync-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) jedes Anbieters auf, der für die Klassen verantwortlich ist, von denen die Klasse, die die ursprüngliche Instanz besitzt, leitet. Wenn einer dieser Anbieter fehlschlägt, schlägt die ursprüngliche Updateanforderung fehl. Weitere Informationen finden Sie im Abschnitt "Hinweise" von [**PutInstanceAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

Weitere Informationen finden Sie unter [Aufrufen einer Anbietermethode.](calling-a-provider-method.md)

> [!Note]  
> Da der Rückruf an die Senke möglicherweise nicht auf derselben Authentifizierungsebene zurückgegeben wird, wie der Client erfordert, wird empfohlen, anstelle der asynchronen Kommunikation semisynchrone zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

 

 

 
