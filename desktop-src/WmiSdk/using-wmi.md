---
description: Roadmap für die Verwendung von WMI zum Abrufen von Daten für Client Skripts und Anwendungen oder zum Bereitstellen von Daten für WMI aus einer Anwendung.
ms.assetid: d9a3741c-313f-4b63-8588-696a10d370f5
ms.tgt_platform: multiple
title: Verwenden von WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31878b41de0f44a70c31c2134f0a611a9309a321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131972"
---
# <a name="using-wmi"></a>Verwenden von WMI

Sie können WMI aus Client Anwendungen und Skripts verwenden. Sie stellt eine Infrastruktur bereit, mit der Sie problemlos Verwaltungsaufgaben ermitteln und ausführen können. Außerdem können Sie den Satz möglicher Verwaltungsaufgaben hinzufügen, indem Sie eigene WMI-Anbieter erstellen.

> [!Note]  
> Die WMI-Version der nächsten Generation zum Schreiben von Anwendungen und Skripts ist über die Windows-Verwaltungsinfrastruktur (Windows Management Infrastructure, Mi) verfügbar. Weitere Informationen finden Sie unter [Mi-Anbieter und-Clients](/previous-versions/windows/desktop/wmi_v2/mi-providers-and-clients-node-page).

 

In diesem Abschnitt werden folgende Themen erörtert:

-   [Abrufen von Daten aus WMI](#obtaining-data-from-wmi)
-   [Bereitstellen von Daten für WMI](#providing-data-to-wmi)
-   [Wichtige Aufgaben für WMI](#important-tasks-for-wmi)

## <a name="obtaining-data-from-wmi"></a>Abrufen von Daten aus WMI

Im folgenden Verfahren wird beschrieben, wie Sie Daten aus WMI abrufen, indem Sie ein Skript oder eine Anwendung schreiben.

**So rufen Sie Daten aus WMI durch Schreiben eines Skripts oder einer Anwendung ab**

1.  Entscheiden Sie, welche Sprache verwendet werden soll. Weitere Informationen zur Skripterstellung finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md). Weitere Informationen zu C++ finden Sie unter [Erstellen einer WMI-Anwendung mit C++](creating-a-wmi-application-using-c-.md). Weitere Informationen zu c# oder WMI .net finden Sie unter [Übersicht über WMI .net](/previous-versions/).

    Sie können WMI-Daten in vielen Sprachen anzeigen oder bearbeiten. In der folgenden Tabelle sind die Themen aufgeführt, in denen beschrieben wird, wie die Skript-und Anwendungs Sprachen zum Abrufen von Daten verwendet werden.

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Anwendungssprache</th>
    <th>Thema</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>In Microsoft ActiveX-Skript Hosting geschriebene Skripts, einschließlich Visual Basic Scripting Edition (VBScript) und perl<br/></td>
    <td><a href="scripting-api-for-wmi.md">Skript-API für WMI</a>.<br/> Beginnen Sie mit dem <a href="creating-a-wmi-script.md">Erstellen eines WMI-Skripts</a>.<br/> Skriptcode Beispiele finden Sie unter <a href="wmi-tasks-for-scripts-and-applications.md">WMI-Aufgaben für Skripts und Anwendungen</a> und im TechNet <a href="https://www.microsoft.com/technet/scriptcenter">scriptcenter</a> -Skriptrepository.<br/></td>
    </tr>
    <tr class="even">
    <td>Windows PowerShell<br/></td>
    <td><a href="/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7">Einstieg in Windows PowerShell</a><br/> WMI-PowerShell-Cmdlets, z. b. <a href="/previous-versions//dd315295(v=technet.10)">Get-WMIObject</a>.<br/></td>
    </tr>
    <tr class="odd">
    <td>Visual Basic Anwendungen<br/></td>
    <td><a href="scripting-api-for-wmi.md">Skript-API für WMI</a>.<br/></td>
    </tr>
    <tr class="even">
    <td>Active Server Pages<br/></td>
    <td><a href="scripting-api-for-wmi.md">Skript-API für WMI</a>.<br/> Beginnen Sie mit dem <a href="creating-active-server-pages-for-wmi.md">Erstellen von Active Server Seiten für WMI</a>.<br/></td>
    </tr>
    <tr class="odd">
    <td>C++-Anwendungen<br/></td>
    <td><a href="com-api-for-wmi.md">Com-API für WMI</a>.<br/> Beginnen Sie mit dem <a href="creating-a-wmi-application-using-c-.md">Erstellen einer WMI-Anwendung mithilfe von C++</a> und <a href="wmi-c---application-examples.md">WMI C++ Anwendungsbeispiele</a> (enthält Beispiele).<br/></td>
    </tr>
    <tr class="even">
    <td>.NET Framework in c# geschriebene Anwendungen, Visual Basic .net oder J #<br/></td>
    <td>Klassen im <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft. Management. Infrastructure</strong></a> -Namespace.<br/>
    <blockquote>
    [!Note]<br />
    <strong>System. Management</strong> war der ursprüngliche Namespace, der verwalteten Code für WMI umfasste. Die zugrunde liegende Technologie für <strong>System. Management</strong> ist jedoch in der Regel langsamer als und ist nicht sowohl skalierbar als auch, <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft. Management. Infrastructure</strong></a>. Daher empfiehlt es sich nicht, <strong>System. Management</strong> für neue Projekte zu verwenden. (Weitere Informationen zu <strong>System. Management</strong>finden Sie unter <a href="/previous-versions/bb404655(v=vs.90)">Übersicht über WMI .net</a>.) </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Stellen Sie sicher, dass die Verbindungen mit Remote Computern funktionieren.

    Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).

3.  Das Herstellen einer Verbindung mit WMI auf Remote Computern erfordert die richtigen Sicherheitseinstellungen, wie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md)erläutert. In der folgenden Tabelle sind die Themen aufgeführt, in denen die Konfiguration von Sicherheitseinstellungen mit den Sprachen Skripterstellung und Anwendung beschrieben wird.

    

    | Sprache                                                      | Thema                                                                                                                                                                                                                                                 |
    |---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Skripts in einer beliebigen Sprache, Visual Basic Anwendungen<br/> | [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md)<br/>                                                                                                                 |
    | Active Server Pages<br/>                                | [Konfigurieren von IIS 5 und höher für die WMI-ASP-Skripterstellung](configuring-iis-5-for-wmi-asp-scripting.md)<br/>                                                                                                                                           |
    | C++<br/>                                                | [Festlegen der Standardprozess-Sicherheitsstufe mithilfe von C++](setting-the-default-process-security-level-using-c-.md) und [Festlegen der Sicherheit für IWbemServices und andere](setting-the-security-on-iwbemservices-and-other-proxies.md) Proxys<br/> |

    

     

4.  Nach dem Herstellen einer Verbindung mit WMI können Sie Daten über Abfragen und Enumerationen abrufen.

    Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md) und [Abfragen mit WQL](querying-with-wql.md).

5.  Registrierungsdaten sind über WMI verfügbar, und Sie können neue Schlüssel und Werte erstellen oder vorhandene ändern.

    Weitere Informationen finden Sie unter [Ändern der System Registrierung](modifying-the-system-registry.md).

6.  Sie können Ereignis Benachrichtigungen über WMI abonnieren, entweder vorübergehend zwischen Systemneustarts oder dauerhaft.

    Weitere Informationen finden Sie unter über [Wachen von Ereignissen](monitoring-events.md) und [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).

7.  Leistungsdaten für ein System sind über WMI verfügbar.

    Die Leistungsindikatoren für die System Leistungs Bibliothek werden in WMI-Klassen konvertiert. Weitere Informationen finden Sie unter über [Wachen von Leistungsdaten](monitoring-performance-data.md).

8.  [WMI-Tasks für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md) beschreibt, wie viele administrative Aufgaben mit WMI ausgeführt werden.

## <a name="providing-data-to-wmi"></a>Bereitstellen von Daten für WMI

Im folgenden Verfahren wird beschrieben, wie Sie Daten für WMI bereitstellen, indem Sie einen-Anbieter schreiben.

**So stellen Sie Daten für WMI durch Schreiben eines Anbieters bereit**

-   Entscheiden Sie sich für den Typ des zu schreibenden Anbieters.

    Ein WMI-Anbieter kann nicht in VBScript geschrieben werden. Sie können jedoch auch mehrere andere Ansätze zum Schreiben eines WMI-com-Anbieters nutzen:

    -   Verwenden des WMI-ATL-Assistenten in Visual Studio.

        Bei diesem Ansatz wird ein nicht verwalteter com-Anbieter erstellt. Weitere Informationen finden Sie unter [Hinzufügen eines WMI-Instanzanbieters](./writing-an-instance-provider.md) und [Hinzufügen eines WMI-Ereignis Anbieters](./writing-an-event-provider.md).

    -   Direkte Verwendung von com in jeder integrierten Entwicklungsumgebung.

        Bei diesem Ansatz wird ein nicht verwalteter com-Anbieter erstellt.

    -   Verwenden von WMI in der .NET Framework, um einen Anbieter für verwalteten Code zu erstellen.

        Bei diesem Ansatz wird ein Anbieter für verwalteten Code erstellt. Anbieter verwalteter Code können in jeder beliebigen .NET Framework Sprache geschrieben werden, sind einfacher zu schreiben als WMI-com-Anbieter und können Daten aus den WMI- [*CIM*](gloss-c.md)-basierten Klassen, z. b. [Win32-Klassen](/windows/desktop/CIMWin32Prov/win32-provider), abrufen. Der .NET Framework WMI-Anbieter weist jedoch einige Einschränkungen auf. Weitere Informationen finden Sie unter [Verwalten von Anwendungen mit WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

    -   Es wird nicht empfohlen, die [Anbieter Framework-Klassen](wmi-c-classes.md) zu verwenden.

        Das Anbieter Framework wurde durch die WMI-ATL-Assistenten ersetzt, indem com direkt oder .NET Framework Anbieter verwendet wurde. Das Erstellen eines WMI-com-Anbieters mit den Anbieter Framework-Klassen wird nicht mehr empfohlen. In der folgenden Tabelle sind die Themen aufgeführt, in denen die Verwendung von com-oder .NET Framework Anbietern beschrieben wird.

    

    | Anbieter                                                      | Thema                                                                                                   |
    |---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
    | COM-Anbieter im gleichen Prozess wie WMI<br/>            | [Bereitstellen von Daten für WMI](providing-data-to-wmi.md)<br/>                                           |
    | Von com entkoppelter Anbieter<br/>                             | [Einbinden eines Anbieters in eine Anwendung](incorporating-a-provider-in-an-application.md)<br/> |
    | .NET Framework Anbieter in c# oder Visual Basic.net<br/> | [Verwalten von Anwendungen mithilfe von WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))<br/>            |

    

     

## <a name="important-tasks-for-wmi"></a>Wichtige Aufgaben für WMI

In den folgenden Themen finden Sie Informationen zur Verwendung von WMI zum Überwachen und Steuern von Enterprise-Komponenten.



| Thema                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WMI-Tasks für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md)<br/>                                                 | Hier wird beschrieben, wie Sie die richtige WMI-Klasse und die richtigen Prozeduren für Skripts und Anwendungen finden, die allgemeine Computer-und Netzwerk Verwaltungsaufgaben ausführen, z. b. das Hinzufügen einer neuen Druckerverbindung für einen Remote Computer oder das Auffinden aller installierten Hotfixes auf einem Computer.<br/>                                                                            |
| [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md)<br/>                                                     | Jede Skriptsprache, z. b. VBScript oder perl, die mit ActiveX-Objekten funktioniert, kann auf WMI-Daten zugreifen. Anwendungen können auf WMI in C++ mithilfe der [com-API für WMI](com-api-for-wmi.md) oder in Visual Basic zugreifen, mithilfe der wbemdisp. tlb-[Typbibliothek](using-the-wmi-scripting-type-library.md) und der [Skript-API für WMI](scripting-api-for-wmi.md).<br/> |
| [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md)<br/>                                                 | Beschreibt, wie-Skripts,-Anwendungen und-Anbieter Verbindungen mit WMI auf Remote Computern herstellen können, um Daten abzurufen oder Hardware und Software zu steuern.<br/>                                                                                                                                                                                                   |
| [Herstellen einer Verbindung mit WMI auf einem Remote Computer mithilfe von Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)<br/> | Beschreibt die Verwendung von Windows PowerShell zum Herstellen von Verbindungen mit WMI auf Remote Computern zum Abrufen von Daten oder zum Steuern von Hardware und Software.<br/>                                                                                                                                                                                                            |
| [Überwachen von Ereignissen](monitoring-events.md)<br/>                                                                                           | Hier wird beschrieben, wie Sie Ereignis Benachrichtigungen durch Erstellen temporärer oder dauerhafter WMI-Ereignisconsumer erhalten.<br/>                                                                                                                                                                                                                                                           |
| [Bereitstellen von Daten für WMI](providing-data-to-wmi.md)<br/>                                                                                   | WMI stellt dynamische Verwaltungsdaten für Client Skripts und Anwendungen bereit, indem Sie Sie von Anbietern erhalten.<br/>                                                                                                                                                                                                                                                    |
| [Erhalten und Bereitstellen von Daten auf einem 64-Bit-Computer](getting-and-providing-data-on-a-64-bit-computer.md)<br/>                               | Beschreibt den Zugriff auf nicht standardmäßige Anbieter und Überlegungen für Anbieterwriter auf 64-Bit-Systemen.<br/>                                                                                                                                                                                                                                                    |



