---
title: Windows-Firewall für Spieleentwickler
description: In diesem Artikel wird die Windows Firewall beschrieben, warum sie vorhanden ist, was sie erreicht und wie sie funktioniert. Vor allem wird beschrieben, wie Sie Ihr Spiel so konfigurieren, dass es gut mit der Firewall funktioniert.
ms.assetid: 2ee9f769-03dc-3661-5d5b-6a4ecd151fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e7fc00631ef69f878c54de90c2577221e5bc9a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882675"
---
# <a name="windows-firewall-for-game-developers"></a>Windows-Firewall für Spieleentwickler

In diesem Artikel wird die Windows Firewall beschrieben, warum sie vorhanden ist, was sie erreicht und wie sie funktioniert. Vor allem wird beschrieben, wie Sie Ihr Spiel so konfigurieren, dass es gut mit der Firewall funktioniert.

Inhalte:

-   [Was ist eine Firewall?](#what-is-a-firewall)
-   [Wie kann ich feststellen, ob mein Spiel betroffen ist?](#how-can-i-tell-if-my-game-is-affected)
-   [Die Firewall vor Windows XP SP2](#the-firewall-before-windows-xp-sp2)
-   [Windows XP SP2-Firewall ist besser](#windows-xp-sp2-firewall-is-better)
-   [Arbeiten mit der Windows-Firewall](#working-with-the-windows-firewall)
-   [Integrieren mit InstallShield InstallScript](#integrating-using-installshield-installscript)
-   [Integration in Wise for Windows Installer](#integrating-into-wise-for-windows-installer)
-   [Integrieren in Windows Installer](#integrating-into-windows-installer)
-   [Empfehlungen](#recommendations)

## <a name="what-is-a-firewall"></a>Was ist eine Firewall?

Die Firewall stellt eine Barriere gegen netzwerkbasierte Eindringversuche bereit. Sie blockiert unerwünschten eingehenden Datenverkehr und macht das System im Internet größtenteils unsichtbar, indem ICMP-Anforderungen (Internet Control Message Protocol) abgelehnt werden. Dies bedeutet, dass Ping und tracert nicht funktionieren. Die Firewall sucht auch nach ungültigen Paketen und lehnt sie ab.

Diese Barriere verhindert chancenistische Angriffe. Angriffe werden durch das Auffinden vieler Systeme mit demselben Sicherheitsrisiko verteilt. Die Firewall kann viele Angriffe vereiteln, indem sie ein "Nicht störend"-Zeichen für die derzeit nicht verwendeten Features aufsetzt. Der Angriff wird ignoriert und trifft nicht auf die Startseite zu. Der wesentliche Vorteil der Windows Firewall besteht darin, dass Features und Anwendungen, die nicht verwendet werden, keine Angriffsmöglichkeiten sein können.

Der Benutzer konfiguriert das System, um zu ermitteln, welche Anwendungen und Features benötigt werden, und sollte für das Netzwerk geöffnet sein. Dies geschieht entweder, wenn eine Anwendung installiert ist oder versucht, sich selbst für das Netzwerk zu öffnen.

## <a name="how-can-i-tell-if-my-game-is-affected"></a>Wie kann ich feststellen, ob mein Spiel betroffen ist?

Mit dem Eingang von Windows XP SP2 wurde die Windows Firewall umfassend bereitgestellt. Alle Multiplayer-Windows-Spiele sind bis zu einem gewissen Grad betroffen. Während Clients im Allgemeinen in guter Form sind, benötigen Server, Hosts und Peers in Peer-to-Peers alle die konfigurierte Firewall, um weiterhin funktionieren zu können. Insbesondere wird eingehender nicht angeforderter Datenverkehr gelöscht. Die Firewall fängt Netzwerkdatenverkehr-Filterpakete basierend auf dem Paketinhalt und der aktuellen Netzwerkaktivität ab. Die Firewall verwendet den Inhalt und die Aktivität, um ein Paket weiterzuleiten oder zu löschen. Sobald die Firewall ordnungsgemäß konfiguriert ist, kann ein Spiel wie zuvor eingehenden unerwünschten Datenverkehr akzeptieren.

Wer hat nicht angeforderten eingehenden Datenverkehr?

-   Client/Server: Alle Teilnehmer stellen eine Verbindung mit einem zentralen Server her. Der zentrale Server ist der Server mit eingehendem unerwünschtem Datenverkehr. Die Clients, die eine Verbindung mit dem Server herstellen, fordern den zurückgegebenen Datenverkehr an, der erwartet wird und die Firewall passieren darf, wenn die Regeln für Clients eingehalten werden. Der zentrale Server muss so konfiguriert sein, dass der nicht angeforderte Datenverkehr akzeptiert wird, damit der Clientdatenverkehr die Firewall passieren kann.
-   Massively Multiplayer (MMP): Alle Teilnehmer sind mit einem Rechenzentrum verbunden. Dies entspricht einer komplexen Client-/Serverbeziehung, da das Rechenzentrum über den eingehenden nicht angeforderten Datenverkehr verfügt. Die Teilnehmer sind Clients und müssen im Allgemeinen keinen unerwünschten Datenverkehr akzeptieren.
-   Peer-zu-Peer, wobei alle Teilnehmer direkt miteinander verbunden sind: Alle Teilnehmer müssen bereit sein, unerwünschten Datenverkehr von jedem neuen Spieler zu akzeptieren, der der Gruppe beitritt. In gewissem Sinne müssen alle Teilnehmer als Host fungieren, sodass sie alle so konfiguriert werden müssen, als wären sie Hosts.

Clients sind im Allgemeinen gut in Form. Ihre ausgehenden TCP/IP-Verbindungen (Transmission Control Protocol/Internet Protocol) funktionieren einwandfrei, ebenso wie ausgehende UDP-Nachrichten (User Datagram Protocol) zusammen mit rechtzeitigen Antworten auf diese Nachrichten. Die Firewall hält den Port 90 Sekunden nach jeder ausgehenden Nachricht in Erwartung einer Antwort geöffnet.

## <a name="the-firewall-before-windows-xp-sp2"></a>Firewall vor Windows XP SP2

Die Internet Connection Firewall (ICF) in Windows XP und Windows Server 2003 ist ein zustandsvoller Paketfilter und verarbeitet sowohl Internetprotokoll, Version 4 (IPv4) als auch Internetprotokoll, Version 6 (IPv6). Es ist jedoch nicht standardmäßig aktiviert und unterstützt keine Netzwerkstapel von Drittanbietern, von denen es eine beträchtliche Anzahl auf der Welt gibt, z. B. große Internetanbieter, einschließlich nationalen Telefonunternehmen.

Für Diejenigen, die nicht Windows XP SP2 verwenden, wird dringend empfohlen, ICF zu aktivieren. Lesen Sie die Anweisungen unter "Verwenden einer Internetfirewall" https://www.microsoft.com/security/protect unter als ersten Schritt zum Schützen Ihres PCs. Die Internet Connection Firewall (ICF) stellt port mapping (Portzuordnung) bereit, um den Paketfilter zu überschreiben. Im Wesentlichen geben Sie den port an, der geöffnet werden soll, und bleibt geöffnet, bis Sie ihn schließen. Wenn der Benutzer neu gestartet wird, bevor er geschlossen wird, bleibt er geöffnet, bis er ausdrücklich geschlossen wird. Die Steuerung der Firewall und die Verwaltung der Portzuordnungen erfolgt über [**INetSharingManager**](/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingmanager) (IPv4) und [**INetFwV6Mgr**](/previous-versions/windows/desktop/ics/inetfwv6mgr) (IPv6).

Die Windows Firewall für Windows XP SP2 ist eine umfassendere Lösung, die Netzwerkstapel von Drittanbietern unterstützt und Ports intelligenter verarbeitet: Ports bleiben nur geöffnet, solange die Anwendung, die sie benötigt, noch aktiv ist.

## <a name="windows-xp-sp2-firewall-is-better"></a>Windows XP SP2-Firewall ist besser

Windows XP SP2 stellt die Sicherheitsoptionen und -einstellungen im Vordergrund. Das Ziel besteht darin, standardmäßig zu schützen und es dem Benutzer zu ermöglichen, fundierte Entscheidungen darüber zu treffen, welche Anwendungen auf dem Computer ausgeführt werden dürfen.

Die neue Windows Firewall ist sowohl auf Windows XP SP2 als auch auf Windows Server 2003 Service Pack 1 (SP1) verfügbar. Wie der ICF ist es eine Softwarefirewall, die sowohl IPv4 als auch IPv6 unterstützt, aber im Gegensatz zu ICF unterstützt die Windows Firewall:

-   Bietet Einen Schutz des Systems zur Startzeit, wodurch ein kleines Zeitfenster von Sicherheitsrisiken während des Starts beseitigt wird.
-   Unterstützt Netzwerkstapel von Drittanbietern.
-   Verfügt über den Modus "Ein ohne Ausnahmen", der alle nicht angeforderten eingehenden Pakete blockiert. Dies ist ideal, wenn Sie ein öffentliches Netzwerk verwenden, z. B. in einem Flughafen oder einer Kaffeemaschine.

Im Modus "Ein ohne Ausnahmen" werden alle statischen Löcher geschlossen. API-Aufrufe zum Öffnen einer statischen Lücke sind zulässig, werden jedoch verzögert. Das heißt, sie werden erst angewendet, wenn die Firewall wieder zum normalen Betrieb wechselt. Alle Lauschenanforderungen von Anwendungen werden ebenfalls ignoriert. Ausgehende Verbindungen sind weiterhin erfolgreich.

Fügen Sie ihre Anwendung bei neuen Anwendungen während der Installation der "Ausnahmenliste" hinzu. Sie können die Anwendung mithilfe der [**INetFwAuthorizedApplications-Schnittstelle**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) hinzufügen und dabei den vollständigen Pfad bereitstellen. Die Details im Beispiel werden behandelt.

Als Randnotiz fragen Sie sich vielleicht, ob es ein Sicherheitsrisiko ist, dass Anwendungen Anwendungen hinzufügen und aus der Ausnahmenliste entfernen können, oder sie denken vielleicht, dass das größere Risiko darin besteht, dass Anwendungen die Firewall vollständig deaktivieren können. Um diese Aufgaben ausführen zu können, muss die Anwendung über Administratorrechte verfügen. Wenn auf Ihrem System bösartiger Code im Administratormodus ausgeführt wird, ist das Spiel bereits beendet, und der Hacker hat bereits gewonnen. Die Fähigkeit des Hackers, die Firewall zu deaktivieren, wäre nur eine Fußnote.

Ältere Anwendungen, einschließlich Anwendungen, die vor dem Upgrade des Benutzers auf Windows XP SP2 installiert wurden, werden mit dem Popupfenster Ausnahmenliste behandelt (siehe Abbildung 1). Dieses Dialogfeld zeigt, wenn eine Anwendung versucht, einen Port für eingehenden Datenverkehr zu öffnen– entweder beim Aufrufen von bind() mit einem Port ungleich 0 (null) für UDP oder accept() für das TCP/IP-Protokoll. Sie müssen als Administrator ausgeführt werden, um die Blockierung von Anwendungen aufzuheben, während "Ask Me Later" dieses Mal nicht zu lässt, aber beim nächsten Mal erneut fragt.

Dies ist ein nicht blockierendes modales Systemdialogfeld. Wenn Sie eine Microsoft Direct3D-Vollbildanwendung ausführen, wird das Dialogfeld darunter angezeigt. und der Benutzer kann ihn dann behandeln, wenn die Anwendung den Vollbildmodus verlässt oder alt-tabstopps zurück zum Desktop wechselt. Für den Benutzer ist es jedoch nicht immer offensichtlich, dass dieser Dialog angezeigt wurde, wenn ein Spiel im Vollbildmodus ausgeführt wird. Daher ist es wichtig, zu vermeiden, dass dieser Dialog mithilfe der [**INetFwAuthorizedApplications-Schnittstelle**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) angezeigt wird, wie unten beschrieben.

**Abbildung 1: Popupdialogfeld "Ausnahmenliste"**

![Popupdialogfeld "Ausnahmenliste"](images/firewalls1.jpg)

Sie werden feststellen, dass das Popup den Namen und Herausgeber der Anwendung kennt. Hier gibt es keine Magisches: Es wird aus den Versionsinformationen der ausführbaren Datei abgerufen. Diese Informationen sind ein wichtiges Systemverwaltungstool. sie wird sogar für laufende Anwendungskompatibilitätsarbeiten verwendet. Einige Anwendungen vergessen nicht, diese Versionsinformationen auf dem neuesten Stand zu halten.

Benutzer können ihre Anwendungen auch über die Benutzeroberfläche (UI) hinzufügen (siehe Abbildung 2)

**Abbildung 2. Konfigurieren der Firewall**

![Konfigurieren der Firewall](images/firewalls2.jpg)

**Abbildung 3: Hinzufügen eines Programms zur Firewall-Ausnahmenliste**

![Hinzufügen eines Programms zur Firewall-Ausnahmenliste](images/firewalls3.jpg)

Das beste Szenario besteht darin, Ergänzungen und Entfernungen aus der Ausnahmeliste zu automatisieren. Der beste Zeitpunkt für diese Hinzufügungen und Entfernungen ist während des Installations- und Deinstallationsprozesses. Zum Hinzufügen oder Entfernen aus der Firewallausnahmeliste sind Administratorrechte erforderlich. Berücksichtigen Sie dies daher unbedingt.

## <a name="working-with-the-windows-firewall"></a>Arbeiten mit der Windows-Firewall

Auch hier müssen die meisten Spiele nur dann der Firewallausnahmeliste hinzugefügt werden, wenn sie als Server fungieren können oder ein Peer-zu-Peer-Kommunikationsprotokoll implementieren. Der FirewallInstallHelper.dll ist eine Beispiel-DLL, die von einem Installationsprogramm aufgerufen werden kann. Die Quelle wird bereitgestellt, wenn Sie die Quelle direkt in Ihre eigene Anwendung integrieren möchten. Das Beispiel finden Sie hier:



|             | Datei                                                                             |
|-------------|------------------------------------------------------------------------------|
| **Quelle:**     | (SDK-Stamm) \\ Beispiele \\ für C++-Misc \\ \\ FirewallInstallHelper                        |
| **Ausführbaren:** | (SDK-Stamm) \\ Beispiele \\ für C++ \\ Misc Bin arch \\ \\ &lt; &gt; \\FirewallInstallHelper.dll |



 

Die von dieser DLL exportierten Funktionen sind die folgenden:

<dl> <dt>

<span id="AddApplicationToExceptionListW"></span><span id="addapplicationtoexceptionlistw"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTW"></span>**AddApplicationToExceptionListW**
</dt> <dd>

Diese Funktion fügt der Ausnahmeliste eine Anwendung hinzu. Sie benötigt einen vollständigen Pfad zur ausführbaren Datei und einen Anzeigenamen, der in der Firewallausnahmeliste angezeigt wird. Diese Funktion erfordert Administratorrechte.

</dd> <dt>

<span id="AddApplicationToExceptionListA"></span><span id="addapplicationtoexceptionlista"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTA"></span>**AddApplicationToExceptionListA**
</dt> <dd>

ANSI-Version von **AddApplicationToExceptionListW**

</dd> <dt>

<span id="RemoveApplicationFromExceptionListW"></span><span id="removeapplicationfromexceptionlistw"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTW"></span>**RemoveApplicationFromExceptionListW**
</dt> <dd>

Diese Funktion entfernt die Anwendung aus der Ausnahmeliste. Sie nimmt einen vollständigen Pfad zur ausführbaren Datei an. Diese Funktion erfordert Administratorrechte.

</dd> <dt>

<span id="RemoveApplicationFromExceptionListA"></span><span id="removeapplicationfromexceptionlista"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTA"></span>**RemoveApplicationFromExceptionListA**
</dt> <dd>

ANSI-Version von **RemoveApplicationFromExceptionListW**

</dd> <dt>

<span id="CanLaunchMultiplayerGameW"></span><span id="canlaunchmultiplayergamew"></span><span id="CANLAUNCHMULTIPLAYERGAMEW"></span>**CanLaunchMultiplayerGameW**
</dt> <dd>

Diese Funktion meldet, ob die Anwendung deaktiviert oder aus der Ausnahmenliste entfernt wurde. Sie sollte jedes Mal aufgerufen werden, wenn das Spiel ausgeführt wird. Die Funktion nimmt einen vollständigen Pfad zur ausführbaren Datei an. Für diese Funktion sind keine Administratorrechte erforderlich.

</dd> <dt>

<span id="CanLaunchMultiplayerGameA"></span><span id="canlaunchmultiplayergamea"></span><span id="CANLAUNCHMULTIPLAYERGAMEA"></span>**CanLaunchMultiplayerGameA**
</dt> <dd>

ANSI-Version von **CanLaunchMultiplayerGameW**

</dd> <dt>

<span id="SetMSIFirewallProperties"></span><span id="setmsifirewallproperties"></span><span id="SETMSIFIREWALLPROPERTIES"></span>**SetMSIFirewallProperties**
</dt> <dd>

Rufen Sie dies nur auf, wenn Sie benutzerdefinierte Aktionen in Windows Installer verwenden. Weitere Informationen finden Sie unten.

</dd> <dt>

<span id="AddToExceptionListUsingMSI"></span><span id="addtoexceptionlistusingmsi"></span><span id="ADDTOEXCEPTIONLISTUSINGMSI"></span>**AddToExceptionListUsingMSI**
</dt> <dd>

Rufen Sie dies nur auf, wenn Sie benutzerdefinierte Aktionen in Windows Installer verwenden. Weitere Informationen finden Sie unten.

</dd> <dt>

<span id="RemoveFromExceptionListUsingMSI"></span><span id="removefromexceptionlistusingmsi"></span><span id="REMOVEFROMEXCEPTIONLISTUSINGMSI"></span>**RemoveFromExceptionListUsingMSI**
</dt> <dd>

Rufen Sie dies nur auf, wenn Sie benutzerdefinierte Aktionen in Windows Installer verwenden. Weitere Informationen finden Sie unten.

</dd> </dl>

In den folgenden Abschnitten werden bestimmte Methoden zum Aufrufen der exportierten DLL-Funktionen aus dieser FirewallInstallHelper-Datei in einem InstallShield-, Wise- oder Windows Installer-Paket beschrieben. Alle Methoden rendern die gleichen Ergebnisse, und der Entwickler muss bestimmen, welche Methode implementiert werden soll.

## <a name="integrating-using-installshield-installscript"></a>Integrieren mit InstallShield InstallScript

Eine alternative Methode zur Verwendung der Firewall-APIs ist das Hinzufügen der Funktionsaufrufe zu InstallShield InstallScript. Die schritte, die für die Integration erforderlich sind, sind recht einfach:

1.  Öffnen Sie ein InstallScript-Projekt im InstallShield-Editor.
2.  Fügen Sie dem Projekt die FirewallInstallHelper.dll als Unterstützungsdatei hinzu.

    1.  Öffnen Sie auf Project Registerkarte Assistent die Registerkarte Anwendungsdateien.
    2.  Klicken Sie auf die Schaltfläche Dateien hinzufügen, um dateien zum Anwendungszielordner hinzuzufügen.
    3.  Navigieren Sie zu den FirewallInstallHelper.dll, die Sie erstellt haben, oder verwenden Sie das im DirectX SDK bereitgestellte , und fügen Sie es dem Projekt hinzu.

3.  Fügen Sie InstallScript zum Projekt hinzu.

    1.  Öffnen Sie die Ansicht Installations-Designer, und klicken Sie auf Behavior and Logic InstallScript (Verhalten und Logic \| InstallScript).
    2.  Klicken Sie auf die InstallScript-Datei (normalerweise setup.rul), um sie im Editor zu öffnen.
    3.  Fügen Sie den folgenden Code in die InstallScript-Datei ein:

    ``` syntax
    #include "ifx.h"

    prototype BOOL FirewallInstallHelper.AddApplicationToExceptionListW( WSTRING, WSTRING );
    prototype BOOL FirewallInstallHelper.RemoveApplicationFromExceptionListW( WSTRING );

    function OnMoved()
        WSTRING path[256];
    begin
        // The DLL has been installed into the TARGETDIR
        if !MAINTENANCE then // TRUE when installing
            UseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
            path = TARGETDIR ^ "TODO: change to relative path to executable from install directory";
            FirewallInstallHelper.AddApplicationToExceptionListW( path, "TODO: change to friendly app name" );
            UnUseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
        endif;
    end;
          

    function OnMoving()
        WSTRING path[256];
    begin
        // The DLL is about to be removed from TARGETDIR
        if MAINTENANCE && UNINST != "" then // TRUE when uninstalling
            UseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
            path = TARGETDIR ^ "TODO: change to relative path to executable from install directory";
            FirewallInstallHelper.RemoveApplicationFromExceptionListW( path );
            UnUseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
        endif;
    end;
    ```

    4.  Ändern Sie die TODO-Kommentare mit dem Anwendungsnamen, der in der Firewallausnahmeliste angezeigt wird, und dem Pfad zur ausführbaren Datei des Spiels relativ zum Installationsverzeichnis.

## <a name="integrating-into-wise-for-windows-installer"></a>Integrieren in Wise for Windows Installer

Für die Integration in Wise for Windows Installer müssen die folgenden Schritte ausgeführt werden:

1.  Öffnen Sie ihr Wise for Windows Installer-Projekt.
2.  Wählen Sie unten die Registerkarte "Installationsexperte" aus.
3.  Klicken Sie auf Dateien, und fügen Sie die FirewallInstallHelper.dll aus dem DXSDK dem Installationsverzeichnis des Spiels hinzu.
4.  Wählen Sie unten die Registerkarte "MSI-Skript" aus.
5.  Wählen Sie unten die Registerkarte "Direkt ausführen" aus.
6.  Fügen Sie nach CostFinalize eine Aktion "Eigenschaft festlegen" hinzu, mit der FULLPATH auf \[ "INSTALLDIR relative path to executable from install directory" festgelegt \] wird. Beispiel: \[ "INSTALLDIR \]game.exe" ohne Anführungszeichen
7.  Wählen Sie unten die Registerkarte "Verzögert ausführen" aus.
8.  Fügen Sie nach PublishProduct eine If-Anweisung mit der Bedingung "NICHT installiert" hinzu (Groß-/Kleinschreibung wird beachtet).
9.  Fügen Sie innerhalb des If-Blocks die Aktion "Benutzerdefinierte DLL aus Ziel aufrufen" hinzu.

    1.  Legen Sie das Feld DLL-Datei auf \[ "INSTALLDIR \]FirewallInstallHelper.dll" fest.
    2.  Legen Sie das Feld Funktionsname auf "AddApplicationToExceptionListA" fest.
    3.  Fügen Sie einen Parameter mit dem Typ "Zeichenfolgenzeiger", der Wertquelle "Property" und dem Eigenschaftsnamen "FULLPATH" hinzu.
    4.  Fügen Sie einen zweiten Parameter mit dem Typ "Zeichenfolgenzeiger" und der Wertquelle "Constant" hinzu, und legen Sie den konstanten Wert auf den Anzeigenamen der Anwendung fest, den Sie in der Firewallausnahmeliste anzeigen möchten.
    5.  Schließen Sie den If-Block, indem Sie eine End-Anweisung hinzufügen.

10. Fügen Sie direkt oberhalb der Aktion RemoveFiles am oberen Rand einen weiteren If-Block mit der Bedingung "REMOVE~="ALL"" hinzu (Groß-/Kleinschreibung wird beachtet und keine äußeren Anführungszeichen verwendet).
11. Fügen Sie innerhalb des zweiten If-Blocks die Aktion "Benutzerdefinierte DLL aus Ziel aufrufen" hinzu.

    1.  Legen Sie das Feld DLL-Datei auf \[ "INSTALLDIR \]FirewallInstallHelper.dll" fest.
    2.  Legen Sie das Feld Funktionsname auf "RemoveApplicationFromExceptionListA" fest.
    3.  Fügen Sie einen Parameter mit dem Typ "Zeichenfolgenzeiger", der Wertquelle "Property" und dem Eigenschaftsnamen "FULLPATH" hinzu.
    4.  Schließen Sie den zweiten If-Block, indem Sie eine "End-Anweisung" hinzufügen.

## <a name="integrating-into-windows-installer"></a>Integrieren in Windows Installer

Für die Integration in Windows Installer auf hoher Ebene müssen diese Schritte ausgeführt werden. Sie werden im Folgenden ausführlich erläutert:

-   Fügen Sie wie unten beschrieben die zwei Eigenschaften "FriendlyNameForFirewall" und "RelativePathToExeForFirewall" hinzu.
-   Rufen Sie nach der CostFinalize-Aktion "SetMSIFirewallProperties" in einer unmittelbaren benutzerdefinierten Aktion auf, um die entsprechenden MSI-Eigenschaften für die anderen benutzerdefinierten Aktionen festzulegen.
-   Rufen Sie während der Installation nach der InstallFiles-Aktion eine verzögerte benutzerdefinierte Aktion auf, die die Funktion "AddToExceptionListUsingMSI" von FirewallInstallHelper verwendet.
-   Rufen Sie während der Deinstallation nach der InstallFiles-Aktion eine verzögerte benutzerdefinierte Aktion auf, die die Funktion "RemoveFromExceptionListUsingMSI" von FirewallInstallHelper verwendet.
-   Rufen Sie während des Rollbacks eine verzögerte benutzerdefinierte Aktion auf, die auch die Funktion "RemoveFromExceptionListUsingMSI" von FirewallInstallHelper aufruft.

Die folgenden Schritte sind erforderlich, um dies mithilfe eines MSI-Editors wie Orca im Plattform-SDK zu tun. Beachten Sie, dass einige Editoren über Assistenten verfügen, die einige dieser Schritte vereinfachen:

1.  Öffnen Sie das MSI-Paket in Orca.
2.  Fügen Sie der Binärtabelle Folgendes hinzu:

    

    | Name     | Daten                                                                                                                                                                          |
    |----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | FIREWALL | Zeigen Sie ihn auf den FirewallInstallHelper.dll. Diese Datei wird in das MSI-Paket eingebettet, sodass Sie diesen Schritt jedes Mal durchführen müssen, wenn Sie FirewallInstallHelper.dll neu kompilieren. |

    

     

3.  Fügen Sie der Tabelle CustomAction Folgendes hinzu:

    

    | Aktion                   | type                                                                                                                                                                                                   | `Source`   | Ziel                          |
    |--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------|
    | FirewallSetMSIProperties | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                                                        | FIREWALL | SetMSIFirewallProperties        |
    | FirewallAdd              | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | FIREWALL | AddToExceptionListUsingMSI      |
    | FirewallRemove           | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | FIREWALL | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackAdd      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | FIREWALL | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackRemove   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | FIREWALL | AddToExceptionListUsingMSI      |

    

     

4.  Fügen Sie der Tabelle InstallExecuteSequence Folgendes hinzu:

    

    | Aktion                   | Bedingung     | Sequenz | Hinweise                                                                                                                                                                      |
    |--------------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | FirewallSetMSIProperties |               | 1010     | Dies wird kurz nach CostFinalize erreicht.                                                                                                                                       |
    | FirewallAdd              | NICHT installiert | 4021     | Diese benutzerdefinierte Aktion wird nur während einer neu installierten Installation vorgenommen. Die Sequenznummer platziert die Aktion nach InstallFiles und nach den Rollbacks.                              |
    | FirewallRollBackAdd      | NICHT installiert | 4020     | Diese benutzerdefinierte Aktion wird nur dann vorgenommen, wenn eine neu installierte Installation abgebrochen wird. Die Sequenznummer platziert die Aktion nach InstallFiles und vor der Aktion Benutzerdefinierte Hinzufügen.          |
    | FirewallRemove           | Installiert     | 3461     | Diese benutzerdefinierte Aktion wird nur während der Deinstallation geschehen. Die Sequenznummer platziert die Aktion direkt vor RemoveFiles und nach den Rollbacks.                           |
    | FirewallRollBackRemove   | NICHT installiert | 3460     | Diese benutzerdefinierte Aktion wird nur dann geschehen, wenn eine Deinstallation abgebrochen wird. Die Sequenznummer platziert die Aktion direkt vor RemoveFiles und vor der benutzerdefinierten Aktion Entfernen. |

    

     

5.  Fügen Sie der Tabelle Property Folgendes hinzu:

    

    | Eigenschaft                     | Wert                                                                             |
    |------------------------------|-----------------------------------------------------------------------------------|
    | FriendlyNameForFirewall      | Muss der Name sein, der in der Ausnahmeliste angezeigt wird. Beispiel: "Beispielspiel" |
    | RelativePathToExeForFirewall | Muss die installierte ausführbare Datei des Spiels sein. Beispiel: "ExampleGame.exe"  |

    

     

Weitere Informationen zum Windows-Installer finden Sie unter [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="recommendations"></a>Empfehlungen

Die Firewall ist hier, um zu bleiben. Diese Empfehlungen bieten Ihren Kunden eine gute Firewallerfahrung mit Ihrem Windows:

-   Informieren Sie Benutzer nicht, die Firewall zu deaktivieren, um Ihr Spiel zu spielen. Dadurch wird der gesamte Computer anfällig, auch wenn er ihr Spiel nicht spielt.
-   Sorgen Sie für eine nahtlose Firewallkonfiguration für Ihre Benutzer. Fügen Sie die Anwendung während der Installation der Ausnahmeliste hinzu, und entfernen Sie die Anwendung während der Installation aus der Ausnahmeliste.
-   Geben Sie dem Benutzer Feedback, wenn der Multiplayer-Modus durch den Firewallzustand blockiert wird. Deaktivieren Sie z. B. Netzwerkfeatures, wenn sie nicht funktionieren, weil die Anwendung nicht mehr verfügbar ist oder weil sich das System im Modus "Keine Ausnahmen" befindet.

 

 
