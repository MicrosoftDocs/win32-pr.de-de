---
description: Wie bei anderen Sprachen wie PowerShell, VBScript oder C++ können Sie c# verwenden, um die Hardware und Software auf Remote Computern Remote zu überwachen.
ms.assetid: 9E03A8D0-01AB-4B7E-99B6-FEEF9C1CAE17
ms.tgt_platform: multiple
title: 'Remote Verbindung mit WMI mit C #'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ad9fe2008b52276a8f68149b33ae3729daaf7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042683"
---
# <a name="connecting-to-wmi-remotely-with-c"></a>Remote Verbindung mit WMI mit C #

Wie bei anderen Sprachen wie PowerShell, VBScript oder C++ können Sie c# verwenden, um die Hardware und Software auf Remote Computern Remote zu überwachen. Remote Verbindungen für verwalteten Code werden über den [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) -Namespace erreicht. (In früheren Versionen von WMI wurde der [System. Management](/dotnet/api/system.management) -Namespace verwendet, der aus Gründen der Vollständigkeit hier enthalten ist.)

> [!Note]  
> **System. Management** war der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. die APIs in diesem Namespace sind jedoch in der Regel langsamer und werden relativ zu ihren moderneren **Microsoft. Management. Infrastructure** -Entsprechungen nicht auch skaliert.

 

Beim Herstellen einer Remote Verbindung mithilfe von Klassen im [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) -Namespace wird DCOM als zugrunde liegender Remote Mechanismus verwendet. WMI-Remoteverbindungen müssen den DCOM-Sicherheitsanforderungen für Identitätswechsel und Authentifizierung entsprechen. Standardmäßig ist ein Bereich an den lokalen Computer und den \\ System Namespace "root CIMv2" gebunden. Sie können jedoch sowohl den Computer, die Domäne als auch den WMI-Namespace ändern, auf den Sie zugreifen. Sie können auch Autorität, Identitätswechsel, Anmelde Informationen und andere Verbindungsoptionen festlegen.

**So stellen Sie eine Remote Verbindung mit WMI mit c# her (Microsoft. Management. Infrastructure)**

1.  Erstellen Sie eine Sitzung auf dem Remote Computer mit einem [cimsession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85))-Befehl.

    Wenn Sie mit den gleichen Anmelde Informationen (Domäne und Benutzername), mit denen Sie angemeldet sind, eine Verbindung mit einem Remote Computer herstellen, können Sie den Namen des Computers im [Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) -Befehl angeben. Sobald Sie über das zurückgegebene [cimsession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) -Objekt verfügen, können Sie die WMI-Abfrage erstellen.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string OSQuery = "SELECT * FROM Win32_OperatingSystem";
    CimSession mySession = CimSession.Create("Computer_B");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
    ```

    

    Weitere Informationen zum Erstellen von WMI-Abfragen mit der **Microsoft. Management. Infrastructure** -API in c# finden Sie unter [Abrufen von WMI-Klassen-oder Instanzdaten](retrieving-class-or-instance-data.md).

2.  Wenn Sie unterschiedliche Optionen für die Verbindung festlegen möchten, z. b. unterschiedliche Anmelde Informationen, Gebiets Schema-oder Identitätswechsel Ebenen, müssen Sie in Ihrem [cimsession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85))-Befehl ein [cimsessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) -Objekt verwenden.

    [Cimsessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) ist eine Basisklasse für [wsmansessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) und [dcomsessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)). Sie können entweder verwenden, um die Optionen für die WS-Man-bzw. DCOM-Sitzungen festzulegen. Im folgenden Codebeispiel wird die Verwendung eines [dcomsessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) -Objekts beschrieben, um die Identitätswechsel Ebene auf den Identitätswechsel festzulegen.

    ```CSharp
    string computer = "Computer_B"
    DComSessionOptions DComOptions = new DComSessionOptions();
    DComOptions.Impersonation = ImpersonationType.Impersonate;

    CimSession Session = CimSession.Create(computer, DComOptions);
    ```

    

3.  Wenn Sie die Anmelde Informationen für die Verbindung festlegen möchten, müssen Sie ein [CIM-Anmelde](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) Informationsobjekt erstellen und zu [cimsessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))hinzufügen.

    Im folgenden Codebeispiel wird das Erstellen einer [wsmansessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) -Klasse beschrieben, die mit den richtigen [cimsessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))-Klassen aufgefüllt und in einem [cimsession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) -Befehl verwendet wird.

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

    

    Es wird im Allgemeinen empfohlen, ein Kennwort in Ihren Anwendungen nicht hart zu codieren. wie das obige Codebeispiel zeigt, sollten Sie nach Möglichkeit versuchen, den Benutzer nach dem Kennwort abzufragen und es sicher zu speichern.

WMI dient der Überwachung von Hardware und Software auf Remotecomputern. Remote Verbindungen für WMI v1 werden über das [ManagementScope](/dotnet/api/system.management.managementscope) -Objekt erreicht.

**So stellen Sie eine Remote Verbindung mit WMI mit c# her (System. Management)**

1.  Erstellen Sie ein [ManagementScope](/dotnet/api/system.management.managementscope) -Objekt mit dem Namen des Computers und dem WMI-Pfad, und stellen Sie eine Verbindung mit dem Ziel mit einem-Befehl von ManagementScope. Connect () her.

    Wenn Sie mit den gleichen Anmelde Informationen (Domäne und Benutzername), mit denen Sie angemeldet sind, eine Verbindung mit einem Remote Computer herstellen, müssen Sie nur den WMI-Pfad angeben. Nachdem Sie eine Verbindung hergestellt haben, können Sie die WMI-Abfrage erstellen.

    ```CSharp
    using System.Management;
    ...
    ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
    scope.Connect();
    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
    ```

    

    Weitere Informationen zum Erstellen von WMI-Abfragen mit der [System. Management](/dotnet/api/system.management) -API in c# finden Sie unter [Abrufen von WMI-Klassen-oder Instanzdaten](retrieving-class-or-instance-data.md).

2.  Wenn Sie eine Verbindung mit einem Remote Computer in einer anderen Domäne herstellen oder einen anderen Benutzernamen und ein anderes Kennwort verwenden, müssen Sie im [ManagementScope](/dotnet/api/system.management.managementscope)-Befehl ein [ConnectionOptions](/dotnet/api/system.management.connectionoptions) -Objekt verwenden.

    Die [ConnectionOptions](/dotnet/api/system.management.connectionoptions) -Eigenschaft enthält Eigenschaften zum Beschreiben der Authentifizierung, des Identitäts Wechsels, des Benutzernamens, des Kennworts und anderer Verbindungsoptionen. Im folgenden Codebeispiel wird die Verwendung von [ConnectionOptions](/dotnet/api/system.management.connectionoptions) beschrieben, um die Identitätswechsel Ebene auf den Identitätswechsel festzulegen.

    ```CSharp
    ConnectionOptions options = new ConnectionOptions();
    options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

    ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
    scope.Connect();

    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);
    ```

    

    Im Allgemeinen wird empfohlen, die Identitätswechsel Ebene so festzulegen, dass Sie einen Identitätswechsel durchgeführt hat, sofern nicht explizit erforderlich. Versuchen Sie noch einmal, den Namen und das Kennwort nicht in c#-Code zu schreiben. (Wenn möglich, überprüfen Sie, ob Sie den Benutzer Abfragen können, um diese zur Laufzeit dynamisch bereitzustellen.)

    Weitere Beispiele für das Festlegen verschiedener Eigenschaften für eine WMI-Remote Verbindung finden Sie im Abschnitt "Beispiele" auf der Referenzseite zu [ConnectionOptions](/dotnet/api/system.management.connectionoptions) .

## <a name="microsoftmanagementinfrastructure-example"></a>Beispiel für Microsoft. Management. Infrastructure

Im folgenden c#-Codebeispiel, das auf dem folgenden [Blogbeitrag auf TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage)basiert, wird beschrieben, wie mit [CIM-Anmelde](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) Informationen und [wsmansessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) Anmelde Informationen für eine Remote Verbindung festgelegt werden.


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



## <a name="systemmanagement-example"></a>System. Management-Beispiel

Im folgenden c#-Codebeispiel wird eine allgemeine Remote Verbindung mithilfe der System. Management-Objekte beschrieben.


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

[Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
