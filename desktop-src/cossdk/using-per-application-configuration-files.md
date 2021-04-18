---
description: Verwenden von Per-Application Konfigurationsdateien
ms.assetid: a600e5a4-b2bb-45a6-8b86-5ea3caf7aa78
title: Verwenden von Per-Application Konfigurationsdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4d59d05f6a7b9b894a2577eb55cceffa49d267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343966"
---
# <a name="using-per-application-configuration-files"></a><span data-ttu-id="824ea-103">Verwenden von Per-Application Konfigurationsdateien</span><span class="sxs-lookup"><span data-stu-id="824ea-103">Using Per-Application Configuration Files</span></span>

<span data-ttu-id="824ea-104">Die Verwendung von com+-Konfigurationsdateien pro Anwendung erfordert die folgenden grundlegenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="824ea-104">Using COM+ per-application configuration files requires the following basic steps:</span></span>

-   <span data-ttu-id="824ea-105">Konfigurieren Sie ein Anwendungs Stammverzeichnis für eine COM+-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="824ea-105">Configure an application root directory for a COM+ application.</span></span>
-   <span data-ttu-id="824ea-106">Erstellen Sie die Dateien "Application. Manifest" und "application.config" im com+-Anwendungs Stammverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="824ea-106">Create application.manifest and application.config files in the COM+ application root directory.</span></span>

> [!Note]  
> <span data-ttu-id="824ea-107">Anwendungsspezifische Konfigurationsdateien sind nur ab Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="824ea-107">Per-application configuration files are only available starting with Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span>

 

<span data-ttu-id="824ea-108">**So verwenden Sie eine anwendungsspezifische Konfigurationsdatei**</span><span class="sxs-lookup"><span data-stu-id="824ea-108">**To use a per-application configuration file**</span></span>

1.  <span data-ttu-id="824ea-109">Erstellen Sie eine .NET-Klassenbibliothek mit einem Verweis auf die System. EnterpriseServices-Assembly.</span><span class="sxs-lookup"><span data-stu-id="824ea-109">Create a .NET class library, with a reference to the System.EnterpriseServices assembly.</span></span>

2.  <span data-ttu-id="824ea-110">Die Klassenbibliothek sollte den folgenden Code enthalten:</span><span class="sxs-lookup"><span data-stu-id="824ea-110">The class library should contain the following code:</span></span>

    ```CSharp
    using System;
    using System.Configuration;
    using System.EnterpriseServices;

    public class Class1 : ServicedComponent
    {
        public string GetConfigData()
        {
            return System.Configuration.ConfigurationSettings.AppSettings
                 ["ConfigData1"];
        }
    }
    ```

    

    <span data-ttu-id="824ea-111">Beachten Sie, dass "ConfigData1" ein Beispiel Einstellungs Name ist.</span><span class="sxs-lookup"><span data-stu-id="824ea-111">Note that "ConfigData1" is a sample setting name.</span></span> <span data-ttu-id="824ea-112">Sie können dies durch den Einstellungs Namen Ihrer Wahl ersetzen.</span><span class="sxs-lookup"><span data-stu-id="824ea-112">You can replace this with the setting name of your choice.</span></span>

3.  <span data-ttu-id="824ea-113">Erstellen Sie eine leere com+-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="824ea-113">Create an empty COM+ application.</span></span> <span data-ttu-id="824ea-114">Anweisungen hierzu finden Sie unter [Erstellen einer neuen COM+-Anwendung](creating-a-new-com--application.md).</span><span class="sxs-lookup"><span data-stu-id="824ea-114">For instructions on how to do this, see [Creating a New COM+ Application](creating-a-new-com--application.md).</span></span>
4.  <span data-ttu-id="824ea-115">Installieren Sie die Klassenbibliothek, die Sie in der com+-Anwendung erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="824ea-115">Install the class library you created into the COM+ application.</span></span> <span data-ttu-id="824ea-116">Anweisungen hierzu finden Sie unter [Installieren neuer Komponenten](installing-new-components.md).</span><span class="sxs-lookup"><span data-stu-id="824ea-116">For instructions on how to do this, see [Installing New Components](installing-new-components.md).</span></span>
5.  <span data-ttu-id="824ea-117">Klicken Sie im Verwaltungs Programmkomponenten Dienste mit der rechten Maustaste auf die erstellte COM+-Anwendung, und wählen Sie **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="824ea-117">In the Component Services administrative tool, right-click the COM+ application you created and select **Properties**.</span></span>
6.  <span data-ttu-id="824ea-118">Wählen Sie im Dialogfeld **Eigenschaften** die Registerkarte **Aktivierung** aus.</span><span class="sxs-lookup"><span data-stu-id="824ea-118">In the **Properties** dialog box, select the **Activation** tab.</span></span>
7.  <span data-ttu-id="824ea-119">Stellen Sie sicher, dass der **Aktivierungstyp** auf **Server Anwendung** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="824ea-119">Make sure the **Activation type** is set to **Server application**.</span></span>
8.  <span data-ttu-id="824ea-120">Geben Sie im Textfeld **Anwendungs Stammverzeichnis** den Pfad ein, oder navigieren Sie zu dem Verzeichnis, in dem Sie die Anwendungs Konfigurationsdateien für diese Anwendung speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="824ea-120">In the **Application Root Directory** text box, enter the path or browse to the directory where you want to store your application configuration files for this application.</span></span>
9.  <span data-ttu-id="824ea-121">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="824ea-121">Click **OK**.</span></span>

    <span data-ttu-id="824ea-122">Beachten Sie, dass Sie auch das com+-Anwendungs Stammverzeichnis über die ApplicationDirectory-Eigenschaft der [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse angeben können.</span><span class="sxs-lookup"><span data-stu-id="824ea-122">Note that you can also specify the COM+ application root directory through the ApplicationDirectory property of the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span> <span data-ttu-id="824ea-123">Weitere Informationen finden Sie unter [**Anwendungen**](applications.md).</span><span class="sxs-lookup"><span data-stu-id="824ea-123">For more information, see [**Applications**](applications.md).</span></span>

10. <span data-ttu-id="824ea-124">Erstellen Sie in dem Verzeichnis, das Sie zum Speichern der Anwendungs Konfigurationsdateien ausgewählt haben, eine Datei namens " *Application*. Manifest".</span><span class="sxs-lookup"><span data-stu-id="824ea-124">In the directory you chose to store your application configuration files, create a file named *application*.manifest.</span></span> <span data-ttu-id="824ea-125">Fügen Sie der Datei in einem Text-Editor den folgenden Text hinzu:</span><span class="sxs-lookup"><span data-stu-id="824ea-125">With a text editor, add the following text to this file:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" />
    ```

11. <span data-ttu-id="824ea-126">Erstellen Sie im gleichen Verzeichnis eine Datei mit dem Namen " *Application*. config". Fügen Sie der Datei in einem Text-Editor den folgenden Text hinzu:</span><span class="sxs-lookup"><span data-stu-id="824ea-126">In the same directory, create a file named *application*.config. With a text editor, add the following text to this file:</span></span>

    ``` syntax
    <?xml version="1.0"?>
    <configuration>
        <appSettings>
            <add key="ConfigData1" value="Configuration Data Number 1"/>
        </appSettings>
    </configuration>
    ```

    <span data-ttu-id="824ea-127">Beachten Sie, dass diese Konfigurationsdatei nur ein Beispiel ist.</span><span class="sxs-lookup"><span data-stu-id="824ea-127">Note that this configuration file is just an example.</span></span> <span data-ttu-id="824ea-128">Sie können mehrere Schlüssel mit unterschiedlichen Namen und Werten erstellen.</span><span class="sxs-lookup"><span data-stu-id="824ea-128">You can create multiple keys with different names and values.</span></span> <span data-ttu-id="824ea-129">Beachten Sie jedoch, dass "ConfigData1" mit dem Einstellungs Namen übereinstimmt, der in der zuvor erstellten Klassenbibliothek verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="824ea-129">Note, however, that "ConfigData1" matches the setting name used in the class library created earlier.</span></span>

12. <span data-ttu-id="824ea-130">Erstellen Sie eine .NET-Konsolenanwendung mit einem Verweis auf die .NET-Klassenbibliothek, die Sie zuvor erstellt haben, und einem Verweis auf die System. EnterpriseServices-Assembly.</span><span class="sxs-lookup"><span data-stu-id="824ea-130">Create a .NET console application, with a reference to the .NET class library you created earlier, and a reference to the System.EnterpriseServices assembly.</span></span>
13. <span data-ttu-id="824ea-131">Die Konsolenanwendung sollte den folgenden Code enthalten:</span><span class="sxs-lookup"><span data-stu-id="824ea-131">The console application should contain the following code:</span></span>
    ```CSharp
    using System;
    using System.IO;

    class Client
    {
    [STAThread]
        static void Main(string[] args)
        {
            Class1 server = new Class1();
            Console.WriteLine(server.GetConfigData());
            Console.ReadLine();
        }
    }
    ```

    

<span data-ttu-id="824ea-132">Führen Sie die Konsolenanwendung aus.</span><span class="sxs-lookup"><span data-stu-id="824ea-132">Run the console application.</span></span> <span data-ttu-id="824ea-133">Die Ausgabe sollte wie folgt sein:</span><span class="sxs-lookup"><span data-stu-id="824ea-133">The output should be:</span></span>

``` syntax
Configuration Data Number 1
```

 

 



