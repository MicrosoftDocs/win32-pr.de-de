---
description: Der erste Objekttyp, den Sie abrufen können, ist eine WMI-Klasse.
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: Abrufen einer WMI-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e2695a934436e6e53fe84ee11c6008615b3d6f5d1807039d76b72fa704a2cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739879"
---
# <a name="retrieving-a-wmi-class"></a>Abrufen einer WMI-Klasse

Der erste Objekttyp, den Sie abrufen können, ist eine WMI-Klasse. Beim Abrufen einer WMI-Klasse rufen Sie tatsächlich eine Klassendefinition ab, bei der es sich um eine Auflistung der Eigenschaften, Qualifizierer und Methoden handelt, die die Klasse vollständig beschreiben. Eine Klassendefinition ist jedoch im Grunde die Klasse selbst.

PowerShell verwendet eine Standardabfrage, um Klassendefinitionen mithilfe der **\_ Metaklassenklasse** abzurufen.

**So rufen Sie eine Klassendefinition in PowerShell ab**

-   Verwenden Sie [get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) mit einer Abfrage an die **\_ Metaklasse,** wobei die WHERE-Klausel den Namen der Klasse enthält, die Sie abrufen möchten.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) ist das Standard-Cmdlet, das PowerShell zum Abrufen von Klassen- und Instanzinformationen aus WMI verwendet. Die **\_ Metaklassenklasse** definiert die Abfrage als Schemaabfrage. Ohne die **\_ Metaklassenklasse** würde diese Abfrage alle Instanzen von Win32 \_ LogicalDisk zurückgeben. Weitere Informationen zum Abfragen von WMI finden Sie unter [SELECT-Anweisung für Schemaabfragen.](select-statement-for-schema-queries.md)

Der aktuelle Prozess zum Abrufen einer WMI-Definition in C# ist die Verwendung der **CIMInstance-Klasse.**

**So rufen Sie eine Klassendefinition in C# ab (Microsoft.Management.Infrastructure)**

1.  Erstellen Sie **mit dem Microsoft.Management.Infrastructure-Namespace** eine **CIMInstance-Klasse** mit dem angegebenen Namespace und Klassennamen.

    Die erstellte Klasse enthält alle Klasseninformationen, aber keine Instanzdaten.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  Alternativ können Sie wie bei PowerShell auch eine Abfrage ausführen, indem Sie das **\_ Metaklassentag** als Teil der Abfrage verwenden.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

Wie bei PowerShell verwendet C# eine **\_ Metaklassenabfrage,** um Klassendefinitionen abzurufen. Alternativ können Sie ein **ManagementClass-Objekt** erstellen, um direkt auf die Klassendefinition zu zugreifen.

> [!Note]  
> **System.Management war** der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. Die APIs in diesem Namespace sind jedoch im Allgemeinen langsamer und werden im Vergleich zu ihren moderneren **Microsoft.Management.Infrastructure-Entsprechungen** nicht so gut skaliert.

 

**So rufen Sie eine Klassendefinition in C# ab (System.Management)**

1.  Sie können [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) mit einer Abfrage an die **Metaklasse \_** verwenden, wobei die WHERE-Klausel den Namen der Klasse enthält, die Sie abrufen möchten.

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    [ManagementObjectSerarcher ist](/dotnet/api/system.management.managementobjectsearcher) die Standardklasse, die .NET zum Abrufen von Klassen- und Instanzinformationen aus WMI verwendet. [ManagementObjectSerarcher.Get gibt](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) eine [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) zurück, die die Schemadefinitionsklasse enthält. Die **\_ Metaklassenklasse** definiert die Abfrage als Schemaabfrage. Ohne die **\_ Metaklassenklasse** würde diese Abfrage alle Instanzen von [**Win32 \_ LogicalDisk zurückgeben.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) Weitere Informationen zum Abfragen von WMI finden Sie unter [SELECT-Anweisung für Schemaabfragen.](select-statement-for-schema-queries.md)

2.  Alternativ können Sie ein neues [ManagementClass-Objekt](/dotnet/api/system.management.managementclass) mit dem Namen als Pfad erstellen, um die Klasse abzurufen.

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

Sie können eine Klassendefinition in VBScript auf ähnliche Weise abrufen wie beim Abrufen einer bestimmten Instanz.

**So rufen Sie eine Klassendefinition in VBScript ab**

1.  Rufen [**Sie SWbemServices.Get auf,**](swbemservices-get.md) identifizieren Sie jedoch keine bestimmte Instanz im Objektpfad für die -Klasse.
2.  Im folgenden Codebeispiel wird die Klassendefinition für die -Klasse abgerufen, die logische Laufwerke auf Ihrem Computer beschreibt.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    Windows Der Skripthost (WSH) unterstützt auch Folgendes.

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    Verwenden Active Server Pages (ASP) [**getObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) oder [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) im serverseitigen Skript. Weitere Informationen finden Sie unter [Erstellen Active Server Pages für WMI.](creating-active-server-pages-for-wmi.md)

3.  Es kann auch eine Klasse oder Instanz angegeben werden. In diesem Fall ist das zurückgegebene Objekt ein WMI-Objekt, z. B. eine Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)und kein Dienstobjekt. Beachten Sie, dass Sie die VBScript [**GetObject-Funktionen**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) nicht verwenden können, um eine Instanz des generischen [**Objekts SWbemObject zu erstellen.**](swbemobject.md)
4.  In HTML-Seiten, die in Microsoft Internet Explorer (IE) ausgeführt werden, können [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) und [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) fehlschlagen, da WMI-Skriptobjekte wie ActiveX-Steuerelemente nicht als sicher für Skripts markiert sind. Die einzige Ausnahme ist das [**SWbemDateTime-Objekt.**](swbemdatetime.md) Diese Aufrufe können nur erfolgreich sein, wenn Sie die IE-Sicherheitseinstellungen senken. Dies wird nicht empfohlen.

Rufen Sie beim Abrufen einer Klasse in C++ die [**IWbemServices-Version**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) von [**GetObject auf.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)

**So rufen Sie eine Klassendefinition in C++ ab**

1.  Rufen Sie [**die Methoden IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) auf, um die Definition einer Klasse abzurufen.
2.  Eine Klasse kann über mehrere Klassendefinitionen verfügen. Dies geschieht in der Regel, wenn sie mehrere Klassenanbieter in einen Namespace geladen haben. Wenn eine Klasse über mehrere Klassendefinitionen verfügt, gibt WMI die erste gefundene Definition und den **WBEM \_ S \_ DUPLICATE \_ OBJECTS-Statuscode** zurück.

Da [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) eine Klassendefinition zurückgibt, wird sie häufig als erster Schritt beim Erstellen einer Instanz verwendet. Weitere Informationen zur Verwendung von **GetObject** finden Sie unter [Erstellen und Deklarieren einer Instanz mithilfe von C++.](creating-and-declaring-an-instance-using-c-.md)

 

 
