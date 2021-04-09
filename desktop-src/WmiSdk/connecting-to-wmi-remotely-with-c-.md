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
# <a name="connecting-to-wmi-remotely-with-c"></a><span data-ttu-id="0b0a0-103">Remote Verbindung mit WMI mit C #</span><span class="sxs-lookup"><span data-stu-id="0b0a0-103">Connecting to WMI Remotely with C#</span></span>

<span data-ttu-id="0b0a0-104">Wie bei anderen Sprachen wie PowerShell, VBScript oder C++ können Sie c# verwenden, um die Hardware und Software auf Remote Computern Remote zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-104">As with other languages such as PowerShell, VBScript, or C++, you can use C# to remotely monitor the hardware and software on remote computers.</span></span> <span data-ttu-id="0b0a0-105">Remote Verbindungen für verwalteten Code werden über den [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) -Namespace erreicht.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-105">Remote connections for managed code are accomplished through the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace.</span></span> <span data-ttu-id="0b0a0-106">(In früheren Versionen von WMI wurde der [System. Management](/dotnet/api/system.management) -Namespace verwendet, der aus Gründen der Vollständigkeit hier enthalten ist.)</span><span class="sxs-lookup"><span data-stu-id="0b0a0-106">(Previous versions of WMI used the [System.Management](/dotnet/api/system.management) namespace, which is included here for completeness.)</span></span>

> [!Note]  
> <span data-ttu-id="0b0a0-107">**System. Management** war der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. die APIs in diesem Namespace sind jedoch in der Regel langsamer und werden relativ zu ihren moderneren **Microsoft. Management. Infrastructure** -Entsprechungen nicht auch skaliert.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-107">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="0b0a0-108">Beim Herstellen einer Remote Verbindung mithilfe von Klassen im [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) -Namespace wird DCOM als zugrunde liegender Remote Mechanismus verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-108">Connecting remotely using classes in the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace uses DCOM as the underlying remote mechanism.</span></span> <span data-ttu-id="0b0a0-109">WMI-Remoteverbindungen müssen den DCOM-Sicherheitsanforderungen für Identitätswechsel und Authentifizierung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-109">WMI remote connections must comply with DCOM security requirements for impersonation and authentication.</span></span> <span data-ttu-id="0b0a0-110">Standardmäßig ist ein Bereich an den lokalen Computer und den \\ System Namespace "root CIMv2" gebunden.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-110">By default, a scope is bound to the local computer and the "Root\\CIMv2" system namespace.</span></span> <span data-ttu-id="0b0a0-111">Sie können jedoch sowohl den Computer, die Domäne als auch den WMI-Namespace ändern, auf den Sie zugreifen.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-111">However, you can change both the computer, domain, and WMI namespace that you access.</span></span> <span data-ttu-id="0b0a0-112">Sie können auch Autorität, Identitätswechsel, Anmelde Informationen und andere Verbindungsoptionen festlegen.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-112">You can also set authority, impersonation, credentials, and other connection options.</span></span>

<span data-ttu-id="0b0a0-113">**So stellen Sie eine Remote Verbindung mit WMI mit c# her (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="0b0a0-113">**To connect to WMI remotely with C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="0b0a0-114">Erstellen Sie eine Sitzung auf dem Remote Computer mit einem [cimsession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85))-Befehl.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-114">Create a session on the remote machine with a call to [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).</span></span>

    <span data-ttu-id="0b0a0-115">Wenn Sie mit den gleichen Anmelde Informationen (Domäne und Benutzername), mit denen Sie angemeldet sind, eine Verbindung mit einem Remote Computer herstellen, können Sie den Namen des Computers im [Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) -Befehl angeben.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-115">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you can specify the name of the computer in the [Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) call.</span></span> <span data-ttu-id="0b0a0-116">Sobald Sie über das zurückgegebene [cimsession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) -Objekt verfügen, können Sie die WMI-Abfrage erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-116">Once you have the returned [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object, you can then make your WMI query.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string OSQuery = "SELECT * FROM Win32_OperatingSystem";
    CimSession mySession = CimSession.Create("Computer_B");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
    ```

    

    <span data-ttu-id="0b0a0-117">Weitere Informationen zum Erstellen von WMI-Abfragen mit der **Microsoft. Management. Infrastructure** -API in c# finden Sie unter [Abrufen von WMI-Klassen-oder Instanzdaten](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="0b0a0-117">For more information on making WMI queries with the **Microsoft.Management.Infrastructure** API in C#, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="0b0a0-118">Wenn Sie unterschiedliche Optionen für die Verbindung festlegen möchten, z. b. unterschiedliche Anmelde Informationen, Gebiets Schema-oder Identitätswechsel Ebenen, müssen Sie in Ihrem [cimsession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85))-Befehl ein [cimsessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) -Objekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-118">If you wish to set different options for your connection, such as different credentials, locale or Impersonation levels, you need to use a [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) object in your call to [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).</span></span>

    <span data-ttu-id="0b0a0-119">[Cimsessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) ist eine Basisklasse für [wsmansessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) und [dcomsessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0b0a0-119">[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) is a base class for [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) and [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)).</span></span> <span data-ttu-id="0b0a0-120">Sie können entweder verwenden, um die Optionen für die WS-Man-bzw. DCOM-Sitzungen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-120">You can use either to set the options on your WS-Man and DCOM sessions, respectively.</span></span> <span data-ttu-id="0b0a0-121">Im folgenden Codebeispiel wird die Verwendung eines [dcomsessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) -Objekts beschrieben, um die Identitätswechsel Ebene auf den Identitätswechsel festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-121">The following code sample describes using a [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) object to set the Impersonation level to Impersonate.</span></span>

    ```CSharp
    string computer = "Computer_B"
    DComSessionOptions DComOptions = new DComSessionOptions();
    DComOptions.Impersonation = ImpersonationType.Impersonate;

    CimSession Session = CimSession.Create(computer, DComOptions);
    ```

    

3.  <span data-ttu-id="0b0a0-122">Wenn Sie die Anmelde Informationen für die Verbindung festlegen möchten, müssen Sie ein [CIM-Anmelde](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) Informationsobjekt erstellen und zu [cimsessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-122">If you wish to set the credentials for your connection, you will need to create and add a [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) object to your [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)).</span></span>

    <span data-ttu-id="0b0a0-123">Im folgenden Codebeispiel wird das Erstellen einer [wsmansessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) -Klasse beschrieben, die mit den richtigen [cimsessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))-Klassen aufgefüllt und in einem [cimsession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) -Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-123">The following code sample describes creating a [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) class, filling it with the proper [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)), and using it in a [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) call.</span></span>

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

    

    <span data-ttu-id="0b0a0-124">Es wird im Allgemeinen empfohlen, ein Kennwort in Ihren Anwendungen nicht hart zu codieren. wie das obige Codebeispiel zeigt, sollten Sie nach Möglichkeit versuchen, den Benutzer nach dem Kennwort abzufragen und es sicher zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-124">It is generally recommended that you do not hardcode a password into your applications; as the above code sample indicates, whenever possible try to query your user for the password, and store it securely.</span></span>

<span data-ttu-id="0b0a0-125">WMI dient der Überwachung von Hardware und Software auf Remotecomputern.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-125">WMI is intended to monitor the hardware and software on remote computers.</span></span> <span data-ttu-id="0b0a0-126">Remote Verbindungen für WMI v1 werden über das [ManagementScope](/dotnet/api/system.management.managementscope) -Objekt erreicht.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-126">Remote connections for WMI v1 is accomplished through the [ManagementScope](/dotnet/api/system.management.managementscope) object.</span></span>

<span data-ttu-id="0b0a0-127">**So stellen Sie eine Remote Verbindung mit WMI mit c# her (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="0b0a0-127">**To connect to WMI remotely with C# (System.Management)**</span></span>

1.  <span data-ttu-id="0b0a0-128">Erstellen Sie ein [ManagementScope](/dotnet/api/system.management.managementscope) -Objekt mit dem Namen des Computers und dem WMI-Pfad, und stellen Sie eine Verbindung mit dem Ziel mit einem-Befehl von ManagementScope. Connect () her.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-128">Create a [ManagementScope](/dotnet/api/system.management.managementscope) object, using the name of the computer and the WMI path, and connect to your target with a call to ManagementScope.Connect().</span></span>

    <span data-ttu-id="0b0a0-129">Wenn Sie mit den gleichen Anmelde Informationen (Domäne und Benutzername), mit denen Sie angemeldet sind, eine Verbindung mit einem Remote Computer herstellen, müssen Sie nur den WMI-Pfad angeben.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-129">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you only have to specify the WMI path.</span></span> <span data-ttu-id="0b0a0-130">Nachdem Sie eine Verbindung hergestellt haben, können Sie die WMI-Abfrage erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-130">Once you have connected, you can make your WMI query.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
    scope.Connect();
    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
    ```

    

    <span data-ttu-id="0b0a0-131">Weitere Informationen zum Erstellen von WMI-Abfragen mit der [System. Management](/dotnet/api/system.management) -API in c# finden Sie unter [Abrufen von WMI-Klassen-oder Instanzdaten](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="0b0a0-131">For more information on making WMI queries with the [System.Management](/dotnet/api/system.management) API in C#, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="0b0a0-132">Wenn Sie eine Verbindung mit einem Remote Computer in einer anderen Domäne herstellen oder einen anderen Benutzernamen und ein anderes Kennwort verwenden, müssen Sie im [ManagementScope](/dotnet/api/system.management.managementscope)-Befehl ein [ConnectionOptions](/dotnet/api/system.management.connectionoptions) -Objekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-132">If you connect to a remote computer in a different domain or using a different user name and password, then you must use a [ConnectionOptions](/dotnet/api/system.management.connectionoptions) object in the call to the [ManagementScope](/dotnet/api/system.management.managementscope).</span></span>

    <span data-ttu-id="0b0a0-133">Die [ConnectionOptions](/dotnet/api/system.management.connectionoptions) -Eigenschaft enthält Eigenschaften zum Beschreiben der Authentifizierung, des Identitäts Wechsels, des Benutzernamens, des Kennworts und anderer Verbindungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-133">The [ConnectionOptions](/dotnet/api/system.management.connectionoptions) contains properties for describing the Authentication, Impersonation, username, password, and other connection options.</span></span> <span data-ttu-id="0b0a0-134">Im folgenden Codebeispiel wird die Verwendung von [ConnectionOptions](/dotnet/api/system.management.connectionoptions) beschrieben, um die Identitätswechsel Ebene auf den Identitätswechsel festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-134">The following code sample describes using a [ConnectionOptions](/dotnet/api/system.management.connectionoptions) to set the Impersonation Level to Impersonate.</span></span>

    ```CSharp
    ConnectionOptions options = new ConnectionOptions();
    options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

    ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
    scope.Connect();

    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);
    ```

    

    <span data-ttu-id="0b0a0-135">Im Allgemeinen wird empfohlen, die Identitätswechsel Ebene so festzulegen, dass Sie einen Identitätswechsel durchgeführt hat, sofern nicht explizit erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-135">Generally speaking, it is recommended that you set your Impersonation level to Impersonate unless explicitly needed otherwise.</span></span> <span data-ttu-id="0b0a0-136">Versuchen Sie noch einmal, den Namen und das Kennwort nicht in c#-Code zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-136">Further, try to avoid writing your name and password into C# code.</span></span> <span data-ttu-id="0b0a0-137">(Wenn möglich, überprüfen Sie, ob Sie den Benutzer Abfragen können, um diese zur Laufzeit dynamisch bereitzustellen.)</span><span class="sxs-lookup"><span data-stu-id="0b0a0-137">(If possible, see if you can query the user to dynamically supply them at runtime.)</span></span>

    <span data-ttu-id="0b0a0-138">Weitere Beispiele für das Festlegen verschiedener Eigenschaften für eine WMI-Remote Verbindung finden Sie im Abschnitt "Beispiele" auf der Referenzseite zu [ConnectionOptions](/dotnet/api/system.management.connectionoptions) .</span><span class="sxs-lookup"><span data-stu-id="0b0a0-138">For more examples of setting different properties on a remote WMI connection, see the Examples section of the [ConnectionOptions](/dotnet/api/system.management.connectionoptions) reference page.</span></span>

## <a name="microsoftmanagementinfrastructure-example"></a><span data-ttu-id="0b0a0-139">Beispiel für Microsoft. Management. Infrastructure</span><span class="sxs-lookup"><span data-stu-id="0b0a0-139">Microsoft.Management.Infrastructure Example</span></span>

<span data-ttu-id="0b0a0-140">Im folgenden c#-Codebeispiel, das auf dem folgenden [Blogbeitrag auf TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage)basiert, wird beschrieben, wie mit [CIM-Anmelde](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) Informationen und [wsmansessionoptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) Anmelde Informationen für eine Remote Verbindung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-140">The following C# code example, based on the following [blog post on TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage), describes how to use [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) and [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) to set credentials on a remote connection.</span></span>


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



## <a name="systemmanagement-example"></a><span data-ttu-id="0b0a0-141">System. Management-Beispiel</span><span class="sxs-lookup"><span data-stu-id="0b0a0-141">System.Management Example</span></span>

<span data-ttu-id="0b0a0-142">Im folgenden c#-Codebeispiel wird eine allgemeine Remote Verbindung mithilfe der System. Management-Objekte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0b0a0-142">The following C# code sample describes a general remote connection, using the System.Management objects.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0b0a0-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b0a0-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b0a0-144">Herstellen einer Verbindung mit WMI auf einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="0b0a0-144">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
