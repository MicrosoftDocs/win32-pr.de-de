---
description: Das Abrufen einer Instanz ist eines der gängigsten Abruf Prozeduren, die Sie in WMI wahrscheinlich ausführen.
ms.assetid: c3258783-ffcd-4c40-aaf2-7c65617cf9f8
ms.tgt_platform: multiple
title: Abrufen einer WMI-Instanz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdacf5fe5c86618eb84d70a5505897a94a7ace2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050514"
---
# <a name="retrieving-a-wmi-instance"></a>Abrufen einer WMI-Instanz

Das Abrufen einer Instanz ist eines der gängigsten Abruf Prozeduren, die Sie in WMI wahrscheinlich ausführen. Sie können eine vorhandene Instanz von abrufen oder eine neue unbenannte Instanz erstellen. Der WMI-Pfad zur vorhandenen Instanz ist ein erforderlicher Parameter. Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).

> [!Note]  
> Wenn eine-Instanz bereitgestellt wird, kann ein Anbieter möglicherweise keinen Wert für bestimmte Eigenschaften bereitstellen. Sofern in der Eigenschafts Beschreibung nicht anders angegeben, können Sie keine Bedeutung von einem leeren Wert ableiten. Dies muss nicht mit einer Zeichenfolge verwechselt werden, die einen **null** -Wert aufweist. In diesem Fall wird der Wert aufgefüllt. Er ist leer, hat aber einen Wert: **null**.

 

Rufen Sie eine lokale Kopie der-Instanz mit einem Aufrufen des PowerShell-Cmdlets [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) ab.

**So rufen Sie eine Instanz einer WMI-Klasse mithilfe von PowerShell ab**

-   Sie können mithilfe der Parameter *-Class* und *-Filter* bestimmte Instanzen abrufen.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

Sie können eine WMI-Instanz mithilfe von c# abrufen, indem Sie ein Such Objekt mithilfe von [ciminstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))erstellen und dann mit den relevanten Schlüsselwerten auffüllen und dann mit einem [cimsession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) -Befehl nach diesem Objekt suchen.

**So rufen Sie mithilfe von c# eine Instanz einer WMI-Klasse ab (Microsoft. Management. Infrastructure)**

1.  Erstellen Sie mit dem [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) -Namespace ein neues [ciminstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) -Objekt mit dem entsprechenden Klassennamen und Namespace.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance myDrive = new CimInstance(className, Namespace);
    ```

    

2.  Erstellen Sie eine [cimproperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) , die den Namen und den Wert der Schlüsseleigenschaft der Instanz enthält, nach der Sie suchen möchten, und fügen Sie diese Eigenschaft dem Klassenobjekt hinzu.

    ```CSharp
    myDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    ```

    

3.  Rufen Sie das-Objekt mit einem [cimsession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) -Befehl aus WMI ab.

    ```CSharp
    CimSession mySession = CimSession.Create("localhost");
    CimInstance searchInstance = mySession.GetInstance(Namespace, myDrive);
    ```

    

Sie können entweder eine bestimmte WMI-Klasseninstanz oder eine Auflistung von WMI-Klassen Instanzen abrufen, indem Sie Klassen im [System. Management](/dotnet/api/system.management) -Namespace verwenden.

> [!Note]  
> **System. Management** war der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. die APIs in diesem Namespace sind jedoch in der Regel langsamer und werden relativ zu ihren moderneren **Microsoft. Management. Infrastructure** -Entsprechungen nicht auch skaliert.

 

**So rufen Sie mithilfe von c# eine Instanz einer WMI-Klasse ab (System. Management)**

1.  Rufen Sie eine lokale Kopie einer bestimmten Instanz ab, indem Sie ein neues [Management Object](/dotnet/api/system.management.managementobject)erstellen, wobei der Name und der angegebene Instanzwert auch über den *ManagementPath* -Parameter übergeben werden. Sie können dann die Instanzdaten abrufen, indem Sie " [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get)" explizit aufrufen.

    ```CSharp
    using System.Management;
    ...
    ManagementObject objInst = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    objInst.Get();
    ```

    

2.  Alternativ können Sie alle Instanzen einer WMI-Klasse abrufen, indem Sie mit einem [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher)suchen und dann die zurückgegebene [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection)auflisten.

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

    foreach (ManagementObject objDisk in colDisks)
    {
       Console.WriteLine("Device ID : {0}", objDisk["DeviceID"]);
    }

    Console.ReadLine();
    ```

    

    Sie können die **Get** -Methode implizit aufrufen, indem Sie auf die-Instanz zugreifen. Weitere Informationen finden Sie unter [Abrufen eines Teils einer WMI-Instanz](retrieving-part-of-an-instance.md).

Rufen Sie eine lokale Kopie der-Instanz mit einem aufzurufenden Befehl der [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) -Methode von VBScript ab.

**So rufen Sie eine Instanz einer WMI-Klasse mithilfe von VBScript ab**

-   Aufrufen von [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) mit dem Objekt Pfad der-Instanz, wie im folgenden Beispiel gezeigt.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk='C:'")
    ```

    

    Zum Abrufen einer bestimmten Instanz muss ein Name als Teil des Objekt Pfads vergeben werden.

Nennen Sie in C++ [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

**So rufen Sie eine Instanz einer WMI-Klasse mithilfe von C++ ab**

-   Rufen Sie eine lokale Kopie der-Instanz mit einem Befehl zum Aufrufen von [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)ab. Der WMI-Pfad zum-Objekt muss eingeschlossen werden.

    Wie der Name schon sagt, ruft [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) die Instanz asynchron ab, während [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) die Instanz synchron abruft. Wenn Sie den asynchronen Abruf verwenden möchten, müssen Sie die [**iwbebobjectsink**](iwbemobjectsink.md) -Schnittstelle implementieren.

## <a name="examples"></a>Beispiele

Ein VBScript-Beispiel, das als Vorlage zum Abrufen von Klassen-und Instanzinformationen verwendet wird, finden Sie im [WMI-Vorlagen Skript](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) Beispiel in der TechNet Gallery. In diesem speziellen Beispiel wird GetObject verwendet, um den WMI-Dienst abzurufen.

 

 
