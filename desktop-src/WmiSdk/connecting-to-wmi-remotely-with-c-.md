---
description: Wie bei anderen Sprachen wie PowerShell, VBScript oder C++ können Sie C# verwenden, um die Hardware und Software auf Remotecomputern remote zu überwachen.
ms.assetid: 9E03A8D0-01AB-4B7E-99B6-FEEF9C1CAE17
ms.tgt_platform: multiple
title: 'Herstellen einer Remoteverbindung mit WMI mit C #'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9ed735a1440d124a065a9f509eac7c58b1fded9be0683e361903b9f02fc1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319438"
---
# <a name="connecting-to-wmi-remotely-with-c"></a>Herstellen einer Remoteverbindung mit WMI mit C #

Wie bei anderen Sprachen wie PowerShell, VBScript oder C++ können Sie C# verwenden, um die Hardware und Software auf Remotecomputern remote zu überwachen. Remoteverbindungen für verwalteten Code werden über den [Namespace Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) durchgeführt. (In früheren Versionen von WMI wurde der [Namespace System.Management](/dotnet/api/system.management) verwendet, der der Vollständigkeit halber hier enthalten ist.)

> [!Note]  
> **System.Management war** der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. Die APIs in diesem Namespace sind jedoch im Allgemeinen langsamer und werden im Vergleich zu ihren moderneren **Microsoft.Management.Infrastructure-Entsprechungen** nicht so gut skaliert.

 

Beim Herstellen einer Remoteverbindung mithilfe von Klassen im [Namespace Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) wird DCOM als zugrunde liegender Remotemechanismus verwendet. WMI-Remoteverbindungen müssen den DCOM-Sicherheitsanforderungen für Identitätswechsel und Authentifizierung entsprechen. Standardmäßig ist ein Bereich an den lokalen Computer und den Systemnamespace "Root \\ CIMv2" gebunden. Sie können jedoch sowohl den Computer, die Domäne als auch den WMI-Namespace ändern, auf den Sie zugreifen. Sie können auch Autorität, Identitätswechsel, Anmeldeinformationen und andere Verbindungsoptionen festlegen.

**So stellen Sie eine Remoteverbindung mit WMI mit C# her (Microsoft.Management.Infrastructure)**

1.  Erstellen Sie eine Sitzung auf dem Remotecomputer mit einem Aufruf von [CimSession.Create.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85))

    Wenn Sie eine Verbindung mit einem Remotecomputer mit den gleichen Anmeldeinformationen (Domäne und Benutzername) herstellen, mit dem Sie angemeldet sind, können Sie den Namen des Computers im [Create-Aufruf](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) angeben. Sobald Sie über das [zurückgegebene CimSession-Objekt](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) verfügen, können Sie Ihre WMI-Abfrage erstellen.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string OSQuery = "SELECT * FROM Win32_OperatingSystem";
    CimSession mySession = CimSession.Create("Computer_B");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
    ```

    

    Weitere Informationen zum Erstellen von WMI-Abfragen mit der **Microsoft.Management.Infrastructure-API** in C# finden Sie unter [Abrufen von WMI-Klassen- oder Instanzdaten.](retrieving-class-or-instance-data.md)

2.  Wenn Sie verschiedene Optionen für Ihre Verbindung festlegen möchten, z. B. unterschiedliche Anmeldeinformationen, Ein- oder Identitätswechselebenen, müssen Sie ein [CimSessionOptions-Objekt](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) in Ihrem Aufruf von [CimSession.Create verwenden.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85))

    [CimSessionOptions ist](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) eine Basisklasse für [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) und [DComSessionOptions.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) Sie können entweder verwenden, um die Optionen für Ihre WS-Man bzw. DCOM-Sitzungen festlegen. Im folgenden Codebeispiel wird die Verwendung eines [DComSessionOptions-Objekts](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) beschrieben, um die Identitätswechselebene auf Impersonate (Identitätswechsel) zu setzen.

    ```CSharp
    string computer = "Computer_B"
    DComSessionOptions DComOptions = new DComSessionOptions();
    DComOptions.Impersonation = ImpersonationType.Impersonate;

    CimSession Session = CimSession.Create(computer, DComOptions);
    ```

    

3.  Wenn Sie die Anmeldeinformationen für Ihre Verbindung festlegen möchten, müssen Sie ein [CimCredentials-Objekt](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) erstellen und Ihrem [CimSessionOptions-Objekt hinzufügen.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))

    Im folgenden Codebeispiel wird das Erstellen einer [WSManSessionOptions-Klasse](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) beschrieben, die mit der richtigen [CimSessionOptions-Klasse](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))gefüllt und in einem [CimSession.Create-Aufruf verwendet](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) wird.

    ```CSharp
    string computer = “Computer_B”;
    string domain = “Domain1″;
    string username = “User1″;

    string plaintextpassword; 

    //Retrieve password from the user. 
    //For the complete code, see the sample at the bottom of this topic.

    CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, domain, username, securepassword); 

    WSManSessionOptions SessionOptions = new WSManSessionOptions();
    SessionOptions.AddDestinationCredentials(Credentials); 

    CimSession Session = CimSession.Create(computer, SessionOptions);
    ```

    

    Es wird im Allgemeinen empfohlen, ein Kennwort nicht hartcodieren. wie das obige Codebeispiel zeigt, versuchen Sie nach Möglichkeit, ihren Benutzer nach dem Kennwort zu fragen und es sicher zu speichern.

WMI dient der Überwachung von Hardware und Software auf Remotecomputern. Remoteverbindungen für WMI v1 werden über das [ManagementScope-Objekt](/dotnet/api/system.management.managementscope) durchgeführt.

**So stellen Sie eine Remoteverbindung mit WMI mit C# her (System.Management)**

1.  Erstellen Sie unter Verwendung des Namens des Computers und des WMI-Pfads ein [ManagementScope-Objekt,](/dotnet/api/system.management.managementscope) und stellen Sie mithilfe eines Aufrufs von ManagementScope eine Verbindung mit Ihrem Ziel her. Verbinden().

    Wenn Sie eine Verbindung mit einem Remotecomputer mit den gleichen Anmeldeinformationen (Domäne und Benutzername) herstellen, mit dem Sie angemeldet sind, müssen Sie nur den WMI-Pfad angeben. Nachdem Sie eine Verbindung erstellt haben, können Sie Ihre WMI-Abfrage erstellen.

    ```CSharp
    using System.Management;
    ...
    ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
    scope.Connect();
    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
    ```

    

    Weitere Informationen zum Erstellen von WMI-Abfragen mit der [System.Management-API](/dotnet/api/system.management) in C# finden Sie unter [Abrufen von WMI-Klassen- oder Instanzdaten.](retrieving-class-or-instance-data.md)

2.  Wenn Sie eine Verbindung mit einem Remotecomputer in einer anderen Domäne herstellen oder einen anderen Benutzernamen und ein anderes Kennwort verwenden, müssen Sie ein [ConnectionOptions-Objekt](/dotnet/api/system.management.connectionoptions) im Aufruf von [ManagementScope verwenden.](/dotnet/api/system.management.managementscope)

    [ConnectionOptions enthält Eigenschaften](/dotnet/api/system.management.connectionoptions) zum Beschreiben der Optionen Authentifizierung, Identitätswechsel, Benutzername, Kennwort und andere Verbindungsoptionen. Im folgenden Codebeispiel wird die Verwendung von [ConnectionOptions](/dotnet/api/system.management.connectionoptions) zum Festlegen der Identitätswechselebene auf Identitätswechsel beschrieben.

    ```CSharp
    ConnectionOptions options = new ConnectionOptions();
    options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

    ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
    scope.Connect();

    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);
    ```

    

    Im Allgemeinen empfiehlt es sich, die Identitätswechselebene auf Impersonate (Identitätswechsel) zu setzen, sofern nicht explizit anders angegeben. Vermeiden Sie außerdem, Ihren Namen und Ihr Kennwort in C#-Code zu schreiben. (Wenn möglich, sehen Sie, ob Sie den Benutzer abfragen können, um ihn zur Laufzeit dynamisch zur Bereitstellung zu verwenden.)

    Weitere Beispiele zum Festlegen verschiedener Eigenschaften für eine WMI-Remoteverbindung finden Sie im Abschnitt Beispiele der [Referenzseite ConnectionOptions.](/dotnet/api/system.management.connectionoptions)

## <a name="microsoftmanagementinfrastructure-example"></a>Beispiel für Microsoft.Management.Infrastructure

Im folgenden C#-Codebeispiel wird basierend auf dem folgenden Blogbeitrag auf [TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage)beschrieben, wie [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) und [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) zum Festlegen von Anmeldeinformationen für eine Remoteverbindung verwendet werden.


```CSharp
using System;
using System.Text;
using System.Threading;
using Microsoft.Management.Infrastructure;
using Microsoft.Management.Infrastructure.Options;
using System.Security; 

namespace SMAPIQuery
{
    class Program
    {
        static void Main(string[] args)
        { 

            string computer = "Computer_B";
            string domain = "DOMAIN";
            string username = "AdminUserName";


            string plaintextpassword; 

            Console.WriteLine("Enter password:");
            plaintextpassword = Console.ReadLine(); 

            SecureString securepassword = new SecureString();
            foreach (char c in plaintextpassword)
            {
                securepassword.AppendChar(c);
            } 

            // create Credentials
            CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, 
                                                          domain, 
                                                          username, 
                                                          securepassword); 

            // create SessionOptions using Credentials
            WSManSessionOptions SessionOptions = new WSManSessionOptions();
            SessionOptions.AddDestinationCredentials(Credentials); 

            // create Session using computer, SessionOptions
            CimSession Session = CimSession.Create(computer, SessionOptions); 

            var allVolumes = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Volume");
            var allPDisks = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_DiskDrive"); 

            // Loop through all volumes
            foreach (CimInstance oneVolume in allVolumes)
            {
                // Show volume information

                if (oneVolume.CimInstanceProperties["DriveLetter"].ToString()[0] > ' '  )
                {
                    Console.WriteLine("Volume ‘{0}’ has {1} bytes total, {2} bytes available", 
                                      oneVolume.CimInstanceProperties["DriveLetter"], 
                                      oneVolume.CimInstanceProperties["Size"], 
                                      oneVolume.CimInstanceProperties["SizeRemaining"]);
                }

            } 

            // Loop through all physical disks
            foreach (CimInstance onePDisk in allPDisks)
            {
                // Show physical disk information
                Console.WriteLine("Disk {0} is model {1}, serial number {2}", 
                                  onePDisk.CimInstanceProperties["DeviceId"], 
                                  onePDisk.CimInstanceProperties["Model"].ToString().TrimEnd(), 
                                  onePDisk.CimInstanceProperties["SerialNumber"]);
            } 

            Console.ReadLine();
         }
     }
 }
```



## <a name="systemmanagement-example"></a>System.Management-Beispiel

Im folgenden C#-Codebeispiel wird eine allgemeine Remoteverbindung mithilfe der System.Management-Objekte beschrieben.


```CSharp
using System;
using System.Management;
public class RemoteConnect 
{
    public static void Main() 
    {
        ConnectionOptions options = new ConnectionOptions();
        options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

        
        ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
        scope.Connect();

        //Query system for Operating System information
        ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
        ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);

        ManagementObjectCollection queryCollection = searcher.Get();
        foreach ( ManagementObject m in queryCollection)
        {
            // Display the remote computer information
            Console.WriteLine("Computer Name     : {0}", m["csname"]);
            Console.WriteLine("Windows Directory : {0}", m["WindowsDirectory"]);
            Console.WriteLine("Operating System  : {0}", m["Caption"]);
            Console.WriteLine("Version           : {0}", m["Version"]);
            Console.WriteLine("Manufacturer      : {0}", m["Manufacturer"]);
        }
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herstellen einer Verbindung mit WMI auf einem Remotecomputer](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
