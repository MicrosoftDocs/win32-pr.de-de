---
description: Enumeration ist der Vorgang, durch den eine Reihe von Objekten durchlaufen und ggf. jedes Objekt geändert wird.
ms.assetid: fe7e3259-9a7c-4f73-af30-192bbbace1b3
ms.tgt_platform: multiple
title: Auflisten von WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94f4a1fcff06423bad9d2bf5570ec1b9705fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345871"
---
# <a name="enumerating-wmi"></a>Auflisten von WMI

Enumeration ist der Vorgang, durch den eine Reihe von Objekten durchlaufen und ggf. jedes Objekt geändert wird. Beispielsweise können Sie eine Reihe von [**Win32 \_ diskdrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) -Objekten durchlaufen, um nach einer bestimmten Seriennummer zu suchen. Beachten Sie, dass WMI nur Objekte zurückgibt, auf die Sie über Sicherheits Zugriff verfügen, obwohl Sie jedes beliebige Objekt auflisten können.

Enumerationen von großen Datasets können eine große Menge an Ressourcen und eine Leistungssteigerung erfordern. Weitere Informationen finden Sie unter [verbessern der enumerationsleistung](improving-enumeration-performance.md). Sie können auch Daten mit einer spezifischeren Abfrage anfordern. Weitere Informationen finden Sie unter [WMI-Abfrage](querying-wmi.md).

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Auflisten von WMI mithilfe von PowerShell](#enumerating-wmi-using-powershell)
-   [Auflisten von WMI mit c# (Microsoft. Management. Infrastructure)](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)
-   [Auflisten von WMI mit c# (System. Management)](#enumerating-wmi-using-c-systemmanagement)
-   [Auflisten von WMI mithilfe von VBScript](#enumerating-wmi-using-vbscript)
-   [Auflisten von WMI mithilfe von C++](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)

## <a name="enumerating-wmi-using-powershell"></a>Auflisten von WMI mithilfe von PowerShell

Wenn Sie den Objekt Pfad für eine bestimmte Instanz nicht kennen oder alle Instanzen für eine bestimmte Klasse abrufen möchten, verwenden Sie [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx)mit dem Namen der Klasse im *-Class-* Parameter. Wenn Sie eine Abfrage verwenden möchten, können Sie den *-Query-* Parameter verwenden.

Im folgenden Verfahren wird beschrieben, wie die Instanzen einer Klasse mithilfe von PowerShell aufgelistet werden.

**So zählen Sie die Instanzen einer Klasse mithilfe von PowerShell auf**

1.  Zählen Sie die Instanzen mit einem [Get-WMIObject-](https://technet.microsoft.com/library/dd315379.aspx) Cmdlet auf.

    [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) gibt eine Auflistung von einem oder mehreren WMI-Objekten zurück, die Sie auflisten können. Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).

    Wenn Sie eine WMI-Klasseninstanz in einem anderen Namespace oder auf einem anderen Computer abrufen möchten, geben Sie den Computer und den Namespace in den Parametern " *-Computer* " bzw. " *-Namespace* " an. Weitere Informationen finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md). Dies funktioniert nur, wenn Sie über die entsprechenden Zugriffsberechtigungen verfügen. Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md) und [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).

2.  Rufen Sie alle einzelnen Instanzen, die Sie wünschen, mithilfe der Member der Auflistung ab.

Das folgende Codebeispiel ruft eine PowerShell-Sammlung ab und zeigt dann die Size-Eigenschaft für alle Instanzen logischer Laufwerke auf dem lokalen Computer an.


```PowerShell
$objCol = get-wmiobject -class "Win32_LogicalDisk"

# Or, alternately
#$objCol = get-wmiobject -Query "SELECT * FROM Win32_LogicalDisk"

foreach ($Drive in $objCol)
{
    if ($Drive.size -ne $null)
    { "Drive " + $Drive.deviceID + " contains " + $Drive.size + " bytes" }
    else
    { "Drive " + $Drive.deviceID + " is not available." }
}
```



## <a name="enumerating-wmi-using-c-microsoftmanagementinfrastructure"></a>Auflisten von WMI mit c# (Microsoft. Management. Infrastructure)

1.  Fügen Sie einen Verweis auf die Verweisassembly **Microsoft. Management. Infrastructure** hinzu. (Diese Assembly wird als Teil des [Windows Software Development Kit (SDK) für Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx)ausgeliefert.)
2.  Fügen Sie eine **using** -Anweisung für den **Microsoft. Management. Infrastructure** -Namespace hinzu.

```CSharp
    using Microsoft.Management.Infrastructure;
```

    

3.  Instanziieren Sie ein [cimsession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) -Objekt. Im folgenden Code Ausschnitt wird der Standardwert "localhost" für die [**cimsession. Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) -Methode verwendet.

```CSharp
    CimSession cimSession = CimSession.Create("localhost");
```

    

4.  Wenden Sie die Methode [**cimsession. queryinstance**](https://www.bing.com/search?q=**CimSession.QueryInstances**) an, und übergeben Sie den gewünschten CIM-Namespace und die zu verwendende WQL. Der folgende Code Ausschnitt gibt zwei-Instanzen zurück, die zwei standardmäßige Windows-Prozesse darstellen, bei denen die Handle-Eigenschaft (die eine Prozess-ID oder PID darstellt) den Wert 0 oder 4 hat.

```CSharp
    IEnumerable<CimInstance> queryInstances =     
      cimSession.QueryInstances(@"root\cimv2", 
                                "WQL", 
                                @"select name from win32_process where handle = 0 or handle = 4");
```

    

5.  Durchlaufen der zurückgegebenen [**ciminstance**](https://www.bing.com/search?q=**CimInstance**) -Objekte.

```CSharp
    foreach (CimInstance cimInstance in enumeratedInstances)
    { 
      Console.WriteLine("Process name: {0}", cimInstance.CimInstanceProperties["Name"].Value);  
    }
```

    

Im folgenden Codebeispiel werden alle Instanzen der [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse (die aktive Prozesse darstellt) auf dem lokalen Computer aufgelistet, und die Namen der einzelnen Prozesse werden gedruckt.

> [!Note]  
> In einer echten Anwendung würden Sie als Parameter den Computernamen ("localhost") und den CIM-Namespace ("root \\ CIMV2") definieren. Aus Gründen der Einfachheit wurden diese in diesem Beispiel hart codiert.

 


```CSharp
using System;
using System.Collections.Generic;
using Microsoft.Management.Infrastructure;

public partial class MI
{
    static void PrintCimInstance(CimInstance cimInstance)
    {
        Console.ForegroundColor = ConsoleColor.Blue;
        Console.WriteLine("{0} properties", cimInstance.CimSystemProperties.ClassName);
        Console.ResetColor();

        Console.WriteLine(String.Format("{0,-5}{1,-30}{2,-15}{3,-10}", 
                                        "Key?", "Property", "Type", "Value"));

        foreach (var enumeratedProperty in cimInstance.CimInstanceProperties)
        {
            bool isKey = ((enumeratedProperty.Flags & CimFlags.Key) == CimFlags.Key);

            if (enumeratedProperty.Value != null)
            {
                Console.WriteLine(
                    "{0,-5}{1,-30}{2,-15}{3,-10}",
                    isKey == true ? "Y" : string.Empty,
                    enumeratedProperty.Name,
                    enumeratedProperty.CimType,
                    enumeratedProperty.Value);
            }
        }
        Console.WriteLine();
    }

    public static void QueryInstance(string query)
    {
        try
        {
            CimSession cimSession = CimSession.Create("localhost");

            IEnumerable<CimInstance> queryInstances = 
              cimSession.QueryInstances(@"root\cimv2", "WQL", query);
            foreach (CimInstance cimInstance in queryInstances)
            {
                //Use the current instance. This example prints the instance. 
                PrintCimInstance(cimInstance);
            }
        }
         catch (CimException ex) 
        { 
            // Handle the exception as appropriate.
            // This example prints the message.
            Console.WriteLine(ex.Message); 
        }
    }
}
```


```CSharp

using System;

namespace MIClientManaged
{
    class Program
    {
        static void Main(string[] args)
        {
            while (true)
            {
                Console.Write(&quot;Enter WQL (x = Quit): &quot;);
                string query = Console.ReadLine().ToUpper();
                if (query.CompareTo(&quot;X&quot;) == 0) break;
                MI.QueryInstance(query);
            }
        }
    }
}
```





## <a name="enumerating-wmi-using-c-systemmanagement"></a>Auflisten von WMI mit c# (System. Management)

Wenn Sie den Objekt Pfad für eine bestimmte Instanz nicht kennen oder alle Instanzen für eine bestimmte Klasse abrufen möchten, verwenden Sie das [ManagementClass](/dotnet/api/system.management.managementclass) -Objekt, um eine [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) abzurufen, die alle Instanzen einer bestimmten Klasse im WMI-Namespace enthält. Alternativ können Sie WMI über einen [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) Abfragen, um denselben Satz von Objekten zu erhalten.

> [!Note]  
> **System. Management** war der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. die APIs in diesem Namespace sind jedoch in der Regel langsamer und werden relativ zu ihren moderneren **Microsoft. Management. Infrastructure** -Entsprechungen nicht auch skaliert.

 

Im folgenden Verfahren wird beschrieben, wie die Instanzen einer Klasse mit c# aufgelistet werden.

**So zählen Sie die Instanzen einer Klasse mithilfe von C auf #**

1.  Auflisten der-Instanzen mit einem-Befehl von [ManagementClass. getinhaltungen](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).

    Die [getinhaltungen](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) -Methode gibt eine Auflistung von Objekten zurück, die Sie auflisten können, oder legt diese fest. Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md). Die zurückgegebene Auflistung ist tatsächlich ein [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) -Objekt, sodass jede Methode dieses Objekts aufgerufen werden kann.

    Wenn Sie eine WMI-Klasseninstanz in einem anderen Namespace oder auf einem anderen Computer abrufen möchten, geben Sie den Computer und den Namespace im *path* -Parameter an. Weitere Informationen finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md). Dies funktioniert nur, wenn Sie über die entsprechenden Zugriffsberechtigungen verfügen. Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md) und [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).

2.  Rufen Sie alle einzelnen Instanzen, die Sie wünschen, mithilfe der Member der Auflistung ab.

Im folgenden Codebeispiel wird eine c#-Auflistung abgerufen und anschließend die Size-Eigenschaft für alle Instanzen von logischen Laufwerken auf dem lokalen Computer angezeigt.


```PowerShell
using System.Management;
...

ManagementClass mc = new ManagementClass("Win32_LogicalDisk");
ManagementObjectCollection objCol = mc.GetInstances();

//or, alternately
//ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
//ManagementObjectCollection objCol = mgmtObjSearcher.Get();

if (objCol.Count != 0)
{
   foreach (ManagementObject Drive in objCol)
   {
      if (Drive["size"] != null)
      {
         Console.WriteLine("Drive {0} contains {1} bytes.", Drive["deviceID"], Drive["size"]);
      }
      else
      {
         Console.WriteLine("Drive {0} is not available.", Drive["deviceID"]);
      }
   }
}
Console.ReadLine();
```



## <a name="enumerating-wmi-using-vbscript"></a>Auflisten von WMI mithilfe von VBScript

Wenn Sie den Objekt Pfad für eine bestimmte Instanz nicht kennen oder alle Instanzen für eine bestimmte Klasse abrufen möchten, verwenden Sie die Methode " [**errbemservices. InstancesOf**](swbemservices-instancesof.md) ", um eine " [**slibewbjectset**](swbemobjectset.md) "-Enumeration aller Instanzen einer Klasse zurückzugeben. Alternativ können Sie WMI über [**SWbemServices.Execquery**](swbemservices-execquery.md) Abfragen, um denselben Satz von Objekten zu erhalten.

Im folgenden Verfahren wird beschrieben, wie die Instanzen einer Klasse mithilfe von VBScript aufgelistet werden.

**So zählen Sie die Instanzen einer Klasse mithilfe von VBScript auf**

1.  Auflisten der-Instanzen mit einem auflistungsbefehl der Methode " [**Swap Services. InstancesOf**](swbemservices-instancesof.md) ".

    Die [**InstancesOf**](swbemservices-instancesof.md) -Methode gibt eine Auflistung von Objekten zurück, die Sie auflisten können, oder legt diese fest. Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md). Die zurückgegebene Auflistung ist tatsächlich ein [**errbewbjectset**](swbemobjectset.md) -Objekt, sodass jede Methode dieses Objekts aufgerufen werden kann.

    Wenn Sie eine WMI-Klasseninstanz in einem anderen Namespace oder auf einem anderen Computer abrufen möchten, geben Sie den Computer und den Namespace im Moniker an. Weitere Informationen finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md). Dies funktioniert nur, wenn Sie über die entsprechenden Zugriffsberechtigungen verfügen. Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md) und [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).

2.  Rufen Sie mithilfe der Auflistungs Methoden alle einzelnen gewünschten Instanzen ab.

Im folgenden Codebeispiel wird ein-Objekt vom Typ " [**Swap Services**](swbemservices.md) " abgerufen und anschließend die [**InstancesOf**](swbemservices-instancesof.md) -Methode ausgeführt, um die Size-Eigenschaft für alle Instanzen von logischen Laufwerken auf dem lokalen Computer anzuzeigen.


```VB
Set objCol = GetObject("WinMgmts:").InstancesOf("Win32_LogicalDisk")
For Each Drive In objCol
    If Not IsNull(Drive.Size) Then    
       WScript.Echo ("Drive " & Drive.deviceid & " contains " & Drive.Size & " bytes")
    Else
       WScript.Echo ("Drive " & Drive.deviceid & " is not available.")
    End If
Next
```



## <a name="enumerating-wmi-using-c"></a>Auflisten von WMI mithilfe von C++

Zusätzlich zur Durchführung der einfachen Enumeration können Sie mehrere Flags und Eigenschaften festlegen, um die Leistung der Enumeration zu erhöhen. Weitere Informationen finden Sie unter [verbessern der enumerationsleistung](improving-enumeration-performance.md).

**So zählen Sie einen Objekt Satz in WMI auf**

1.  Erstellen Sie eine [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Schnittstelle, die den Satz von Objekten beschreibt, die Sie auflisten möchten.

    Ein [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Objekt enthält eine Liste, in der ein Satz von WMI-Objekten beschrieben wird. Sie können die **ienumwbemclassobject** -Methoden verwenden, um vorwärts aufzuzählen, Objekte zu überspringen, am Anfang zu beginnen und den Enumerator zu kopieren. In der folgenden Tabelle werden die Methoden aufgelistet, die zum Erstellen von Enumeratoren für verschiedene Typen von WMI-Objekten verwendet werden.

    

    <table>
    <thead>
    <tr class="header">
    <th>Object</th>
    <th>Methode</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Klasse</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices:: kreateclassenum</strong></a><br />
[<strong>IWbemServices:: feateclassenumschlag</strong>Sequenz] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Instanz</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices:: kreateinstanceaufumum</strong></a><br />
[<strong>IWbemServices:: "kreateingestanceenumasync</strong>"] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)<br />
    </dl></td>
    </tr>
    <tr class="odd">
    <td>Abfrageergebnis</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices:: ExecQuery</strong></a><br />
[<strong>IWbemServices:: ExecQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Ereignisbenachrichtigung</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices:: ExecNotificationQuery</strong></a><br />
[<strong>IWbemServices:: ExecNotificationQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)<br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Durchlaufen der zurückgegebenen Enumeration mithilfe mehrerer Aufrufe von [**ienumwbemclassobject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) oder [**ienumwbemclassobject:: nextasync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).

Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).

 

 
