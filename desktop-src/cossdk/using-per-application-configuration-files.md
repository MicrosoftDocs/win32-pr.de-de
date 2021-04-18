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
# <a name="using-per-application-configuration-files"></a>Verwenden von Per-Application Konfigurationsdateien

Die Verwendung von com+-Konfigurationsdateien pro Anwendung erfordert die folgenden grundlegenden Schritte:

-   Konfigurieren Sie ein Anwendungs Stammverzeichnis für eine COM+-Anwendung.
-   Erstellen Sie die Dateien "Application. Manifest" und "application.config" im com+-Anwendungs Stammverzeichnis.

> [!Note]  
> Anwendungsspezifische Konfigurationsdateien sind nur ab Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.

 

**So verwenden Sie eine anwendungsspezifische Konfigurationsdatei**

1.  Erstellen Sie eine .NET-Klassenbibliothek mit einem Verweis auf die System. EnterpriseServices-Assembly.

2.  Die Klassenbibliothek sollte den folgenden Code enthalten:

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

    

    Beachten Sie, dass "ConfigData1" ein Beispiel Einstellungs Name ist. Sie können dies durch den Einstellungs Namen Ihrer Wahl ersetzen.

3.  Erstellen Sie eine leere com+-Anwendung. Anweisungen hierzu finden Sie unter [Erstellen einer neuen COM+-Anwendung](creating-a-new-com--application.md).
4.  Installieren Sie die Klassenbibliothek, die Sie in der com+-Anwendung erstellt haben. Anweisungen hierzu finden Sie unter [Installieren neuer Komponenten](installing-new-components.md).
5.  Klicken Sie im Verwaltungs Programmkomponenten Dienste mit der rechten Maustaste auf die erstellte COM+-Anwendung, und wählen Sie **Eigenschaften** aus.
6.  Wählen Sie im Dialogfeld **Eigenschaften** die Registerkarte **Aktivierung** aus.
7.  Stellen Sie sicher, dass der **Aktivierungstyp** auf **Server Anwendung** festgelegt ist.
8.  Geben Sie im Textfeld **Anwendungs Stammverzeichnis** den Pfad ein, oder navigieren Sie zu dem Verzeichnis, in dem Sie die Anwendungs Konfigurationsdateien für diese Anwendung speichern möchten.
9.  Klicken Sie auf **OK**.

    Beachten Sie, dass Sie auch das com+-Anwendungs Stammverzeichnis über die ApplicationDirectory-Eigenschaft der [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse angeben können. Weitere Informationen finden Sie unter [**Anwendungen**](applications.md).

10. Erstellen Sie in dem Verzeichnis, das Sie zum Speichern der Anwendungs Konfigurationsdateien ausgewählt haben, eine Datei namens " *Application*. Manifest". Fügen Sie der Datei in einem Text-Editor den folgenden Text hinzu:

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" />
    ```

11. Erstellen Sie im gleichen Verzeichnis eine Datei mit dem Namen " *Application*. config". Fügen Sie der Datei in einem Text-Editor den folgenden Text hinzu:

    ``` syntax
    <?xml version="1.0"?>
    <configuration>
        <appSettings>
            <add key="ConfigData1" value="Configuration Data Number 1"/>
        </appSettings>
    </configuration>
    ```

    Beachten Sie, dass diese Konfigurationsdatei nur ein Beispiel ist. Sie können mehrere Schlüssel mit unterschiedlichen Namen und Werten erstellen. Beachten Sie jedoch, dass "ConfigData1" mit dem Einstellungs Namen übereinstimmt, der in der zuvor erstellten Klassenbibliothek verwendet wurde.

12. Erstellen Sie eine .NET-Konsolenanwendung mit einem Verweis auf die .NET-Klassenbibliothek, die Sie zuvor erstellt haben, und einem Verweis auf die System. EnterpriseServices-Assembly.
13. Die Konsolenanwendung sollte den folgenden Code enthalten:
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

    

Führen Sie die Konsolenanwendung aus. Die Ausgabe sollte wie folgt sein:

``` syntax
Configuration Data Number 1
```

 

 



