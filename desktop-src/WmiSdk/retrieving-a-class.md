---
description: Der erste Objekttyp, den Sie abrufen können, ist eine WMI-Klasse.
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: Abrufen einer WMI-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9378854eb483c6cdac7ddee47d581d8876270e97
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "106354918"
---
# <a name="retrieving-a-wmi-class"></a>Abrufen einer WMI-Klasse

Der erste Objekttyp, den Sie abrufen können, ist eine WMI-Klasse. Wenn Sie eine WMI-Klasse abrufen, rufen Sie tatsächlich eine Klassendefinition ab, die eine Auflistung der Eigenschaften, Qualifizierer und Methoden ist, die die Klasse vollständig beschreiben. Eine Klassendefinition ist jedoch im Grunde die Klasse selbst.

PowerShell verwendet eine Standard Abfrage zum Abrufen von Klassendefinitionen mithilfe der **Meta \_ Class** -Klasse.

**So rufen Sie eine Klassendefinition in PowerShell ab**

-   Verwenden Sie das [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) mit einer Abfrage an eine **Meta- \_ Klasse** mit der WHERE-Klausel, die den Namen der Klasse enthält, die Sie abrufen möchten.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) ist das Standard-Cmdlet, das PowerShell verwendet, um Klassen-und Instanzinformationen aus WMI abzurufen. Die **Meta \_ Class** -Klasse definiert die Abfrage als Schema Abfrage. Ohne die **Meta \_ Class** -Klasse würde diese Abfrage alle Instanzen von Win32 \_ LogicalDisk zurückgeben. Weitere Informationen zum Abfragen von WMI finden Sie unter [SELECT-Anweisung für Schema Abfragen](select-statement-for-schema-queries.md).

Der aktuelle Prozess zum Abrufen einer WMI-Definition in c# ist die Verwendung der **ciminstance** -Klasse.

**So rufen Sie eine Klassendefinition in c# ab (Microsoft. Management. Infrastructure)**

1.  Erstellen Sie mithilfe des **Microsoft. Management. Infrastructure** -Namespace eine **ciminstance** -Klasse mit dem angegebenen Namespace und dem Klassennamen.

    Die erstellte Klasse enthält alle Klassen Informationen, aber keine Instanzdaten.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  Alternativ können Sie wie bei PowerShell auch eine Abfrage durchführen, indem Sie das **Meta- \_ klassentag** als Teil der Abfrage verwenden.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

Wie bei PowerShell verwendet c# eine **Meta- \_ Klassen** Abfrage zum Abrufen von Klassendefinitionen. Alternativ können Sie ein **ManagementClass** -Objekt erstellen, um direkt auf die Klassendefinition zuzugreifen.

> [!Note]  
> **System. Management** war der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. die APIs in diesem Namespace sind jedoch in der Regel langsamer und werden relativ zu ihren moderneren **Microsoft. Management. Infrastructure** -Entsprechungen nicht auch skaliert.

 

**So rufen Sie eine Klassendefinition in c# ab (System. Management)**

1.  Sie können [managementobjectserarcher](/dotnet/api/system.management.managementobjectsearcher) mit einer Abfrage an eine **Meta- \_ Klasse** mit der WHERE-Klausel verwenden, die den Namen der Klasse enthält, die Sie abrufen möchten.

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    [Managementobjectserarcher](/dotnet/api/system.management.managementobjectsearcher) ist die Standardklasse, die .NET verwendet, um Klassen-und Instanzinformationen aus WMI abzurufen. [Managementobjectserarcher. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) gibt eine [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) zurück, die die Schema Definitions Klasse enthält. Die **Meta \_ Class** -Klasse definiert die Abfrage als Schema Abfrage. Ohne die **Meta \_ Class** -Klasse würde diese Abfrage alle Instanzen von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)zurückgeben. Weitere Informationen zum Abfragen von WMI finden Sie unter [SELECT-Anweisung für Schema Abfragen](select-statement-for-schema-queries.md).

2.  Erstellen Sie alternativ ein neues [ManagementClass](/dotnet/api/system.management.managementclass) -Objekt mit dem Namen als Pfad, um die Klasse abzurufen.

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

Sie können eine Klassendefinition in VBScript auf ähnliche Weise abrufen, um eine bestimmte Instanz abzurufen.

**So rufen Sie eine Klassendefinition in VBScript ab**

1.  Ruft die Methode " [**Austausch Services. Get**](swbemservices-get.md) " auf, identifiziert aber keine bestimmte Instanz im Objekt Pfad für die Klasse.
2.  Das folgende Codebeispiel ruft die Klassendefinition für die-Klasse ab, die logische Laufwerke auf Ihrem Computer beschreibt.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    Windows Script Host (WSH) unterstützt auch Folgendes:

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    Verwenden Sie auf Active Server Seiten (ASP) [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) oder [kreateobject](/previous-versions//xzysf6hc(v=vs.85)) im Server seitigen Skript. Weitere Informationen finden Sie unter [Erstellen von Active Server Seiten für WMI](creating-active-server-pages-for-wmi.md).

3.  Es kann auch eine Klasse oder eine Instanz angegeben werden. in diesem Fall handelt es sich bei dem zurückgegebenen Objekt um ein WMI-Objekt, z. b. eine Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), anstatt um ein Dienst Objekt. Beachten Sie, dass Sie die [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) -Funktionen von VBScript nicht verwenden können, um eine Instanz des generischen Objekts " [**errbewbject**](swbemobject.md)" zu erstellen.
4.  In HTML-Seiten, die in Microsoft Internet Explorer (IE) ausgeführt werden, können [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) und [kreateobject](/previous-versions//xzysf6hc(v=vs.85)) fehlschlagen, da WMI-Skript Objekte, wie z. b. ActiveX-Steuerelemente, nicht als sichere Skripts gekennzeichnet sind Die einzige Ausnahme ist das Objekt " [**taubemdatetime**](swbemdatetime.md) ". Diese Aufrufe können nur dann erfolgreich ausgeführt werden, wenn Sie die Internet Explorer-Sicherheitseinstellungen verringern, was nicht empfohlen wird.

Wenn Sie eine Klasse in C++ abrufen, rufen Sie die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Version von [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)auf.

**So rufen Sie eine Klassendefinition in C++ ab**

1.  Rufen Sie die [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Methode oder die [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) -Methode auf, um die Definition einer Klasse abzurufen.
2.  Eine Klasse kann über mehrere Klassendefinitionen verfügen. Dies geschieht in der Regel, wenn Sie mehr als einen Klassen Anbieter in einen Namespace geladen haben. Wenn eine Klasse über mehrere Klassendefinitionen verfügt, gibt WMI die erkannte erste Definition und den Statuscode der **WBEM \_ S- \_ \_ Objekte dupliziert** zurück.

Da [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) eine Klassendefinition zurückgibt, wird diese häufig als erster Schritt beim Erstellen einer Instanz verwendet. Weitere Informationen zur Verwendung von **GetObject** finden [Sie unter Erstellen und Deklarieren einer Instanz mithilfe von C++](creating-and-declaring-an-instance-using-c-.md).

 

 
