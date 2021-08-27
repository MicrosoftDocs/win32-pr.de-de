---
description: Roadmap für die Verwendung von WMI zum Abrufen von Daten für Clientskripts und Anwendungen oder zum Bereitstellen von Daten für WMI aus einer Anwendung.
ms.assetid: d9a3741c-313f-4b63-8588-696a10d370f5
ms.tgt_platform: multiple
title: Verwenden von WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d1556d321441c7e6a3191bf95e85db356e7ba9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475316"
---
# <a name="using-wmi"></a>Verwenden von WMI

Sie können WMI aus Clientanwendungen und Skripts verwenden. Sie stellt eine Infrastruktur zur Verfügung, mit der Sie Verwaltungsaufgaben leicht finden und ausführen können. Darüber hinaus können Sie dem Satz möglicher Verwaltungsaufgaben hinzufügen, indem Sie Eigene WMI-Anbieter erstellen.

> [!Note]  
> Die WMI-Version der nächsten Generation zum Schreiben von Anwendungen und Skripts ist über die Windows Management Infrastructure (MI) verfügbar. Weitere Informationen finden Sie unter [MI Providers and Clients](/previous-versions/windows/desktop/wmi_v2/mi-providers-and-clients-node-page).

 

In diesem Abschnitt werden folgende Themen erörtert:

-   [Abrufen von Daten aus WMI](#obtaining-data-from-wmi)
-   [Bereitstellen von Daten für WMI](#providing-data-to-wmi)
-   [Wichtige Aufgaben für WMI](#important-tasks-for-wmi)

## <a name="obtaining-data-from-wmi"></a>Abrufen von Daten aus WMI

Im folgenden Verfahren wird beschrieben, wie Sie Daten aus WMI abrufen, indem Sie ein Skript oder eine Anwendung schreiben.

**So erhalten Sie Daten aus WMI durch Schreiben eines Skripts oder einer Anwendung**

1.  Entscheiden Sie, welche Sprache sie verwenden soll. Weitere Informationen zur Skripterstellung finden Sie unter [Erstellen eines WMI-Skripts.](creating-a-wmi-script.md) Weitere Informationen zu C++ finden Sie unter [Erstellen einer WMI-Anwendung mithilfe von C++.](creating-a-wmi-application-using-c-.md) Weitere Informationen zu C# oder WMI .NET finden Sie unter [Übersicht über WMI .NET.](/previous-versions/)

    Sie können WMI-Daten in vielen Sprachen anzeigen oder bearbeiten. In der folgenden Tabelle sind die Themen aufgeführt, in denen beschrieben wird, wie die Skript- und Anwendungssprachen zum Abrufen von Daten verwendet werden.

    

    
| Anwendungssprache | Thema | 
|----------------------|-------|
| Skripts, die in Microsoft ActiveX-Skripthosting geschrieben wurden, einschließlich Visual Basic Scripting Edition (VBScript) und Perl<br /> | <a href="scripting-api-for-wmi.md">Skripterstellungs-API für WMI</a>.<br /> Beginnen Sie mit <a href="creating-a-wmi-script.md">Erstellen eines WMI-Skripts.</a><br /> Skriptcodebeispiele finden Sie unter <a href="wmi-tasks-for-scripts-and-applications.md">WMI-Aufgaben für Skripts und Anwendungen</a> und im TechNet <a href="https://www.microsoft.com/technet/scriptcenter">ScriptCenter</a> Script Repository.<br /> | 
| Windows PowerShell<br /> | <a href="/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7">Erste Schritte mit Windows PowerShell</a><br /> WMI-PowerShell-Cmdlets, z. <a href="/previous-versions//dd315295(v=technet.10)">B. Get-WmiObject</a>.<br /> | 
| Visual Basic von Anwendungen<br /> | <a href="scripting-api-for-wmi.md">Skripterstellungs-API für WMI</a>.<br /> | 
| Active Server Pages<br /> | <a href="scripting-api-for-wmi.md">Skripterstellungs-API für WMI</a>.<br /> Beginnen Sie <a href="creating-active-server-pages-for-wmi.md">mit Erstellen Active Server Pages für WMI.</a><br /> | 
| C++-Anwendungen<br /> | <a href="com-api-for-wmi.md">COM-API für WMI</a>.<br /> Beginnen Sie <a href="creating-a-wmi-application-using-c-.md">mit Erstellen einer WMI-Anwendung mit C++-</a> und <a href="wmi-c---application-examples.md">WMI-C++-Anwendungsbeispielen</a> (enthält Beispiele).<br /> | 
| .NET Framework in C#, Visual Basic .NET oder J geschriebene Anwendungen #<br /> | Klassen im <a href="/previous-versions//hh872326(v=vs.85)"><strong>Namespace Microsoft.Management.Infrastructure.</strong></a><br /><blockquote>    [!Note]<br /><strong>System.Management war</strong> der ursprüngliche Namespace, der verwalteten Code für WMI behandelte. Die zugrunde liegende Technologie für <strong>System.Management</strong> ist jedoch im Allgemeinen langsamer als und wird nicht so gut skaliert wie <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft.Management.Infrastructure</strong></a>. Daher wird davon abraten, <strong>System.Management für</strong> neue Projekte zu verwenden. (Weitere Informationen zu <strong>System.Management finden Sie</strong>unter <a href="/previous-versions/bb404655(v=vs.90)">WMI .NET Overview</a>.)    </blockquote><br /> | 


    

     

2.  Stellen Sie sicher, dass Ihre Verbindungen mit Remotecomputern funktionieren.

    Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md)

3.  Für das Herstellen einer Verbindung mit WMI auf Remotecomputern sind die richtigen Sicherheitseinstellungen erforderlich, wie unter Verwalten der [WMI-Sicherheit erläutert.](maintaining-wmi-security.md) In der folgenden Tabelle sind die Themen aufgeführt, in denen beschrieben wird, wie Sicherheitseinstellungen mit den Skript- und Anwendungssprachen konfiguriert werden.

    

    | Sprache                                                      | Thema                                                                                                                                                                                                                                                 |
    |---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Skripts in einer beliebigen Sprache, Visual Basic Anwendungen<br/> | [Festlegen der Standardprozesssicherheitsebene mit VBScript](setting-the-default-process-security-level-using-vbscript.md)<br/>                                                                                                                 |
    | Active Server Pages<br/>                                | [Konfigurieren von IIS 5 und höher für die WMI-ASP-Skripterstellung](configuring-iis-5-for-wmi-asp-scripting.md)<br/>                                                                                                                                           |
    | C++<br/>                                                | [Festlegen der Standardprozesssicherheitsstufe mit C++](setting-the-default-process-security-level-using-c-.md) und [Festlegen der Sicherheit für IWbemServices und andere Proxys](setting-the-security-on-iwbemservices-and-other-proxies.md)<br/> |

    

     

4.  Nach dem Herstellen einer Verbindung mit WMI können Sie Daten über Abfragen und Enumerationen abrufen.

    Weitere Informationen finden Sie unter [Manipulating Class and Instance Information (Bearbeiten von Klassen- und Instanzinformationen)](manipulating-class-and-instance-information.md) [und Querying with WQL (Abfragen mit WQL).](querying-with-wql.md)

5.  Registrierungsdaten sind über WMI verfügbar, und Sie können neue Schlüssel und Werte erstellen oder vorhandene ändern.

    Weitere Informationen finden Sie unter [Ändern der Systemregistrierung.](modifying-the-system-registry.md)

6.  Sie können Ereignisbenachrichtigungen über WMI abonnieren, entweder vorübergehend zwischen Systemneustarts oder dauerhaft.

    Weitere Informationen finden Sie unter [Überwachen von Ereignissen und](monitoring-events.md) Empfangen eines [WMI-Ereignisses.](receiving-a-wmi-event.md)

7.  Leistungsindikatordaten für ein System sind über WMI verfügbar.

    Die Leistungsindikatoren der Systemleistungsbibliothek werden in WMI-Klassen konvertiert. Weitere Informationen finden Sie unter [Überwachen von Leistungsdaten.](monitoring-performance-data.md)

8.  [WMI Tasks for Scripts and Applications (WMI-Tasks](wmi-tasks-for-scripts-and-applications.md) für Skripts und Anwendungen) beschreibt, wie viele administrative Aufgaben mit WMI ausgeführt werden.

## <a name="providing-data-to-wmi"></a>Bereitstellen von Daten für WMI

Im folgenden Verfahren wird beschrieben, wie Daten durch Schreiben eines Anbieters an WMI übermittelt werden.

**So liefern Sie Daten an WMI durch Schreiben eines Anbieters**

-   Entscheiden Sie sich für den Typ des zu schreibenden Anbieters.

    Sie können keinen WMI-Anbieter in VBScript schreiben. Sie können jedoch mehrere andere Ansätze zum Schreiben eines WMI-COM-Anbieters verwenden:

    -   Verwenden des WMI-ATL-Assistenten in Visual Studio.

        Bei diesem Ansatz wird ein nicht verwalteter COM-Anbieter erstellt. Weitere Informationen finden Sie unter [Hinzufügen eines WMI-Instanzanbieters](./writing-an-instance-provider.md) und [Hinzufügen eines WMI-Ereignisanbieters.](./writing-an-event-provider.md)

    -   Direktes Verwenden von COM in jeder integrierten Entwicklungsumgebung.

        Bei diesem Ansatz wird ein nicht verwalteter COM-Anbieter erstellt.

    -   Verwenden von WMI in der .NET Framework, um einen Anbieter für verwalteten Code zu erstellen.

        Bei diesem Ansatz wird ein Anbieter für verwalteten Code erstellt. Anbieter von verwaltetem Code können in einer beliebigen .NET Framework-Sprache geschrieben werden, sind einfacher zu [](gloss-c.md)schreiben als WMI-COM-Anbieter und können Daten aus den WMI CIM-basierten Klassen wie [Win32-Klassen abrufen.](/windows/desktop/CIMWin32Prov/win32-provider) Für den .NET Framework WMI-Anbieter gelten jedoch einige Einschränkungen. Weitere Informationen finden Sie unter [Verwalten von Anwendungen mit WMI.](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))

    -   Die Verwendung [der Anbieterframeworkklassen](wmi-c-classes.md) wird nicht empfohlen.

        Das Anbieterframework wurde durch die WMI ATL-Assistenten ersetzt, indem COM direkt verwendet oder .NET Framework werden. Das Erstellen eines WMI-COM-Anbieters mit den Anbieterframeworkklassen wird nicht mehr empfohlen. In der folgenden Tabelle sind die Themen aufgeführt, in denen die Verwendung von COM- oder .NET Framework beschrieben wird.

    

    | Anbieter                                                      | Thema                                                                                                   |
    |---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
    | COM-Anbieter im gleichen Prozess wie WMI<br/>            | [Bereitstellen von Daten für WMI](providing-data-to-wmi.md)<br/>                                           |
    | Entkoppelter COM-Anbieter<br/>                             | [Integrieren eines Anbieters in eine Anwendung](incorporating-a-provider-in-an-application.md)<br/> |
    | .NET Framework in C# oder Visual Basic.NET<br/> | [Verwalten von Anwendungen mit WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))<br/>            |

    

     

## <a name="important-tasks-for-wmi"></a>Wichtige Aufgaben für WMI

Die folgenden Themen enthalten Informationen zur Verwendung von WMI zum Überwachen und Steuern von Unternehmenskomponenten.



| Thema                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WMI-Aufgaben für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md)<br/>                                                 | Beschreibt, wie sie die richtige WMI-Klasse und -Prozeduren finden, die in Skripts und Anwendungen verwendet werden, die allgemeine Computer- und Netzwerkverwaltungsaufgaben ausführen, z. B. das Hinzufügen einer neuen Druckerverbindung für einen Remotecomputer oder das Suchen aller installierten Hotfixes auf einem Computer.<br/>                                                                            |
| [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md)<br/>                                                     | Jede Skriptsprache, z. B. VBScript oder Perl, die mit ActiveX funktioniert, kann auf WMI-Daten zugreifen. Anwendungen können mithilfe der [COM-API](com-api-for-wmi.md) für WMI oder in Visual Basic mithilfe der Typbibliothek Wbemdisp.tlb[](using-the-wmi-scripting-type-library.md) und der [Skripterstellungs-API](scripting-api-for-wmi.md)für WMI auf WMI in C++ zugreifen.<br/> |
| [Herstellen einer Verbindung mit WMI auf einem Remotecomputer](connecting-to-wmi-on-a-remote-computer.md)<br/>                                                 | Beschreibt, wie Skripts, Anwendungen und Anbieter Verbindungen mit WMI auf Remotecomputern herstellen können, um Daten zu erhalten oder Hardware und Software zu steuern.<br/>                                                                                                                                                                                                   |
| [Herstellen einer Verbindung mit WMI auf einem Remotecomputer mit Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)<br/> | Beschreibt, wie Sie mithilfe Windows PowerShell Verbindungen mit WMI auf Remotecomputern herstellen, um Daten zu erhalten oder Hardware und Software zu steuern.<br/>                                                                                                                                                                                                            |
| [Überwachen von Ereignissen](monitoring-events.md)<br/>                                                                                           | Beschreibt, wie Sie Ereignisbenachrichtigungen durch Erstellen temporärer oder permanenter WMI-Ereignisverbraucher erhalten.<br/>                                                                                                                                                                                                                                                           |
| [Bereitstellen von Daten für WMI](providing-data-to-wmi.md)<br/>                                                                                   | WMI stellt dynamische Verwaltungsdaten für Clientskripts und Anwendungen zur Verfügung, indem diese von Anbietern erhalten werden.<br/>                                                                                                                                                                                                                                                    |
| [Abrufen und Bereitstellen von Daten auf einem 64-Bit-Computer](getting-and-providing-data-on-a-64-bit-computer.md)<br/>                               | Beschreibt den Zugriff auf Nichtstandardanbieter und Überlegungen für Anbieterautoren auf 64-Bit-Systemen.<br/>                                                                                                                                                                                                                                                    |



