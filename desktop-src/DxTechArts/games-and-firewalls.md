---
title: Windows-Firewall für Spieleentwickler
description: In diesem Artikel wird die Windows-Firewall beschrieben. Warum Sie vorhanden ist, was Sie erreicht und wie dies funktioniert. Vor allem wird beschrieben, wie Sie Ihr Spiel so konfigurieren, dass es mit der Firewall gut funktioniert.
ms.assetid: 2ee9f769-03dc-3661-5d5b-6a4ecd151fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88656fb3f622a847c15544646c333b807f3a0fb2
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104530566"
---
# <a name="windows-firewall-for-game-developers"></a>Windows-Firewall für Spieleentwickler

In diesem Artikel wird die Windows-Firewall beschrieben. Warum Sie vorhanden ist, was Sie erreicht und wie dies funktioniert. Vor allem wird beschrieben, wie Sie Ihr Spiel so konfigurieren, dass es mit der Firewall gut funktioniert.

Inhalte:

-   [Was ist eine Firewall?](#what-is-a-firewall)
-   [Wie kann ich erkennen, ob mein Spiel betroffen ist?](#how-can-i-tell-if-my-game-is-affected)
-   [Die Firewall vor Windows XP SP2](#the-firewall-before-windows-xp-sp2)
-   [Windows XP SP2-Firewall ist besser](#windows-xp-sp2-firewall-is-better)
-   [Arbeiten mit der Windows-Firewall](#working-with-the-windows-firewall)
-   [Integrieren mithilfe von InstallShield InstallScript](#integrating-using-installshield-installscript)
-   [Integration in eine Weise für Windows Installer](#integrating-into-wise-for-windows-installer)
-   [Integration in Windows Installer](#integrating-into-windows-installer)
-   [Empfehlungen](#recommendations)

## <a name="what-is-a-firewall"></a>Was ist eine Firewall?

Die Firewall stellt eine Barriere gegen netzwerkbasierte Eindring Versuche dar. Er blockiert nicht angeforderten eingehenden Datenverkehr und macht das System vor allem im Internet unsichtbar, indem ICMP-Anforderungen (Internet Control Message Protocol) abgelehnt werden. Dies bedeutet, dass Ping und tracert nicht funktionieren. Die Firewall sucht auch nach ungültigen Paketen und lehnt sie ab.

Diese Barriere verhindert opportunistische Angriffe. Angriffe werden durch das Auffinden vieler Systeme mit dem gleichen Sicherheitsrisiko verteilt. Die Firewall kann viele Angriffe behindern, indem Sie für die Features, die derzeit nicht verwendet werden, ein "nicht stören"-Vorzeichen ansetzt. der Angriff wird ignoriert und schlägt nicht zu Hause. Der wesentliche Vorteil der Windows-Firewall besteht darin, dass Features und Anwendungen, die nicht verwendet werden, keine Angriffsmöglichkeiten sind.

Der Benutzer konfiguriert das System, um zu ermitteln, welche Anwendungen und Features benötigt werden und für das Netzwerk geöffnet sein sollten. Dies geschieht entweder, wenn eine Anwendung installiert wird oder wenn versucht wird, sich im Netzwerk zu öffnen.

## <a name="how-can-i-tell-if-my-game-is-affected"></a>Wie kann ich erkennen, ob mein Spiel betroffen ist?

Bei der Ankunft von Windows XP SP2 wurde die Windows-Firewall umfassend bereitgestellt. Alle multiplayerwindowsspielen sind von einem gewissen Grad betroffen. Während sich Clients in der Regel in einer guten Form befinden, muss die Firewall für die Fortsetzung der Firewall konfiguriert werden, und zwar für Server, Hosts und Peers in Peer-to-Peer. Insbesondere wird eingehender nicht angeforderter Datenverkehr gelöscht. Die Firewall fängt Netzwerkverkehrs Filter Pakete ab, die auf dem Paket Inhalt und der aktuellen Netzwerkaktivität basieren. Die Firewall verwendet den Inhalt und die Aktivität, um ein Paket weiterzuleiten oder zu löschen. Sobald die Firewall ordnungsgemäß konfiguriert ist, kann ein Spiel eingehenden nicht angeforderten Datenverkehr wie zuvor akzeptieren.

Wer hat nicht angeforderten Datenverkehr?

-   Client/Server: alle Teilnehmer stellen eine Verbindung mit einem zentralen Server her. Der zentrale Server ist der Server mit einem eingehenden nicht angeforderten Datenverkehr. Die Clients, die eine Verbindung mit dem Server herstellen, geben den zurückgegebenen Datenverkehr an. Dies ist zu erwarten, und die Firewall kann durchlaufen werden, wenn die Regeln für Clients befolgt werden. Der zentrale Server muss so konfiguriert werden, dass er den nicht angeforderten Datenverkehr akzeptiert, damit der Client Datenverkehr die Firewall durchlaufen kann.
-   Massively Multiplayer (MMP): alle Teilnehmer sind mit einem Rechenzentrum verbunden. Dies ergibt eine komplexe Client/Server-Beziehung, da das Rechenzentrum über den eingehenden nicht angeforderten Datenverkehr verfügt. Die Teilnehmer sind Clients und müssen im Allgemeinen nicht angeforderten Datenverkehr akzeptieren.
-   Peer-to-Peer, bei dem alle Teilnehmer direkt miteinander verbunden sind: alle Teilnehmer müssen bereit sein, nicht angeforderten Datenverkehr von jedem neuen Spieler zu akzeptieren, der der Gruppe Beitritt. In gewisser Hinsicht muss jeder Teilnehmer als Host fungieren, sodass er alle so konfiguriert werden muss, als ob es sich um Hosts handelt.

Clients sind im Allgemeinen eine gute Form. Ihre ausgehenden TCP/IP-Verbindungen (Transmission Control Protocol/Internet Protocol) funktionieren ordnungsgemäß, da ausgehende UDP-Nachrichten (User Datagram Protocol) zusammen mit rechtzeitigen Antworten auf diese Nachrichten verwendet werden. die Firewall hält den Port für 90 Sekunden nach jeder ausgehenden Nachricht in Erwartung einer Antwort offen.

## <a name="the-firewall-before-windows-xp-sp2"></a>Die Firewall vor Windows XP SP2

Die Internetverbindungs Firewall (ICF) in Windows XP und Windows Server 2003 ist ein Zustands behafteter Paketfilter, der sowohl Internet Protocol, Version 4 (IPv4) als auch Internet Protocol, Version 6 (IPv6), verarbeitet. Es ist jedoch nicht standardmäßig aktiviert und unterstützt keine Netzwerk Stapel von Drittanbietern, von denen es eine beträchtliche Zahl weltweit gibt, wie z. b. große Internetanbieter, einschließlich Länder Telefonunternehmen.

Für diejenigen, die nicht unter Windows XP SP2 angezeigt werden, wird dringend empfohlen, das ICF zu aktivieren. Weitere Informationen finden Sie in den Anweisungen zum Verwenden einer Internet Firewall https://www.microsoft.com/security/protect als ersten Schritt zum Sichern Ihres PCs. Die Internetverbindungs Firewall (ICF) bietet Port Zuordnung, um den Paketfilter zu überschreiben. Im wesentlichen geben Sie den zu öffnenden Port an und bleiben geöffnet, bis Sie ihn schließen. Wenn der Benutzer neu gestartet wird, bevor er geschlossen wird, bleibt er geöffnet, bis er explizit geschlossen wird. Die Kontrolle über die Firewall und die Verwaltung der Port Zuordnungen erfolgt über [**inetsharingmanager**](/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingmanager) (IPv4) und [**INetFwV6Mgr**](/previous-versions/windows/desktop/ics/inetfwv6mgr) (IPv6).

Die Windows-Firewall für Windows XP SP2 ist eine umfassendere Lösung, die Netzwerk Stapel von Drittanbietern unterstützt und Ports intelligenter verarbeitet: Ports werden nur geöffnet, solange die Anwendung, die Sie benötigt, immer noch aktiv ist.

## <a name="windows-xp-sp2-firewall-is-better"></a>Windows XP SP2-Firewall ist besser

Windows XP SP2 stellt die Sicherheitsoptionen und-Einstellungen vor. Ziel ist es, standardmäßig zu schützen und den Benutzern zu ermöglichen, fundierte Entscheidungen zu treffen, welche Anwendungen auf Ihrem Computer ausgeführt werden dürfen.

Die neue Windows-Firewall ist sowohl unter Windows XP SP2 als auch unter Windows Server 2003 Service Pack 1 (SP1) verfügbar. Wie bei ICF auch, ist es eine Software Firewall, die sowohl IPv4 als auch IPv6 unterstützt, aber im Gegensatz zu ICF die Windows-Firewall:

-   Verfügt über einen systemeigenen systemeigenen Schutz, um beim Start ein kleines Sicherheitsrisiko zu vermeiden.
-   Unterstützt Netzwerk Stapel von Drittanbietern.
-   Verfügt über einen Modus ohne Ausnahmen, der alle nicht angeforderten eingehenden Pakete blockiert. Dies ist hervorragend, wenn Sie ein öffentliches Netzwerk verwenden, z. b. in einem Flughafen oder Coffee-Shop.

Im Modus "bei ohne Ausnahmen" werden alle statischen Löcher geschlossen. API-Aufrufe zum Öffnen einer statischen Lücke sind zulässig, aber verzögert; Das heißt, Sie werden erst angewendet, wenn die Firewall wieder zum normalen Betrieb wechselt. Alle lauschen-Anforderungen von Anwendungen werden ebenfalls ignoriert. Ausgehende Verbindungen sind weiterhin erfolgreich.

Fügen Sie bei neuen Anwendungen die Anwendung während der Installation der Ausnahmeliste hinzu. Sie können die Anwendung mithilfe der [**inetswautorizedapplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) -Schnittstelle hinzufügen, die den vollständigen Pfad bereitstellt. Wir behandeln die Details im Beispiel.

Sie Fragen sich vielleicht, ob es sich um ein Sicherheitsrisiko handelt, mit dem Anwendungen Anwendungen aus der Ausnahmeliste jedes Benutzers hinzufügen und daraus entfernen können. das größere Risiko ist, dass Anwendungen die Firewall vollständig deaktivieren können. Die Anwendung muss über Administratorrechte verfügen, um diese Berechtigungen ausführen zu können. Wenn auf Ihrem System bösartiger Code im Administrator Modus ausgeführt wird, ist das Spiel bereits aktiv, und der Hacker hat bereits gewonnen. Die Fähigkeit des Hacker, die Firewall zu deaktivieren, würde nur wenig mehr als eine Fußnote verdienen.

Ältere Anwendungen, einschließlich Anwendungen, die vor dem Upgrade des Benutzers auf Windows XP SP2 installiert wurden, werden mit dem Dropdown Listen-Popup behandelt (siehe Abbildung 1). In diesem Dialogfeld wird angezeigt, wenn eine Anwendung versucht, einen Port für eingehenden Datenverkehr zu öffnen, entweder beim Aufrufen von BIND () mit einem Port ungleich NULL für UDP oder Accept () für das TCP/IP-Protokoll. Sie müssen als Administrator ausgeführt werden, um die Blockierung von Anwendungen zu verhindern, während "später Fragen", diese Zeit nicht mehr zulässt, sondern das nächste Mal erneut fragt.

Dies ist ein nicht blockierendes Systemmodales Dialogfeld. Beim Ausführen einer Vollbild-Microsoft Direct3D-Anwendung, wird das Dialogfeld unterhalb von angezeigt. der Benutzer kann ihn dann verarbeiten, wenn die Anwendung den Vollbildmodus oder die alt-Registerkarten zurück zum Desktop verlässt. Es ist jedoch nicht immer offensichtlich, dass dieses Dialogfeld angezeigt wird, wenn ein Spiel voll Bildschirm ausgeführt wird. Daher ist es wichtig zu vermeiden, dass dieses Dialogfeld angezeigt wird, indem Sie die [**inetfwautorizedapplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) -Schnittstelle verwenden, wie unten erläutert.

**Abbildung 1. Popup Dialogfeld für Ausnahmen Liste**

![Popup Dialogfeld für Ausnahmen Liste](images/firewalls1.jpg)

Sie werden feststellen, dass das Popup den Namen und den Herausgeber der Anwendung kennt. Hier gibt es keine Magie, sondern Sie werden aus den Versionsinformationen der ausführbaren Datei abgerufen. Diese Informationen sind ein wichtiges System Verwaltungs Tool. Sie wird sogar für fortlaufende Anwendungs Kompatibilitäts Arbeiten verwendet. Einige Anwendungen vernachlässigen diese Versionsinformationen nicht auf dem neuesten Stand.

Benutzer können Ihre Anwendungen auch über die Benutzeroberfläche (UI) hinzufügen (siehe Abbildung 2).

**Abbildung 2. Konfigurieren der Firewall**

![Konfigurieren der Firewall](images/firewalls2.jpg)

**Abbildung 3. Hinzufügen eines Programms zur Liste der Firewallausnahmen**

![Hinzufügen eines Programms zur Liste der Firewallausnahmen](images/firewalls3.jpg)

Das beste Szenario ist, dass Ergänzungen und Entfernungen aus der Ausnahmeliste automatisiert werden. Der beste Zeitpunkt, diese Ergänzungen und Entfernungen auszuführen, ist während der Installation und Deinstallation. Zum Hinzufügen oder Entfernen von aus der Liste der Firewallausnahmen sind Administratorrechte erforderlich. Achten Sie daher darauf, dies zu berücksichtigen.

## <a name="working-with-the-windows-firewall"></a>Arbeiten mit der Windows-Firewall

Auch hier müssen die meisten Spiele nur der Liste der Firewallausnahmen hinzugefügt werden, wenn Sie als Server fungieren können oder ein Peer-zu-Peer-Kommunikationsprotokoll implementiert. Der FirewallInstallHelper.dll ist eine Beispiel-dll, die von einem Installer aufgerufen werden kann. Die Quelle wird bereitgestellt, wenn Sie die Quelle direkt in Ihre eigene Anwendung integrieren möchten. Das Beispiel finden Sie hier:



|             |                                                                              |
|-------------|------------------------------------------------------------------------------|
| Quelle:     | (SDK-Stamm) \\ Beispiele \\ C++ \\ misc \\ firewallinstallhelper                        |
| Ausführbare Datei: | (SDK-Stamm) \\ Beispiele \\ C++ \\ misc \\ bin \\ <arch> \\FirewallInstallHelper.dll |



 

Die von dieser DLL exportierten Funktionen lauten wie folgt:

<dl> <dt>

<span id="AddApplicationToExceptionListW"></span><span id="addapplicationtoexceptionlistw"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTW"></span>**Addapplicationreexceptionlistw**
</dt> <dd>

Mit dieser Funktion wird eine Anwendung zur Ausnahmeliste hinzugefügt. Es wird ein kompletter Pfad zur ausführbaren Datei und ein Anzeige Name verwendet, der in der Ausnahmeliste der Firewall angezeigt wird. Diese Funktion erfordert Administratorrechte.

</dd> <dt>

<span id="AddApplicationToExceptionListA"></span><span id="addapplicationtoexceptionlista"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTA"></span>**Addapplicationreexceptionlista**
</dt> <dd>

ANSI-Version von **addapplicationdeexceptionlistw**

</dd> <dt>

<span id="RemoveApplicationFromExceptionListW"></span><span id="removeapplicationfromexceptionlistw"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTW"></span>**Removeapplicationfromexceptionlistw**
</dt> <dd>

Diese Funktion entfernt die Anwendung aus der Ausnahmeliste. Es wird ein kompletter Pfad zur ausführbaren Datei benötigt. Diese Funktion erfordert Administratorrechte.

</dd> <dt>

<span id="RemoveApplicationFromExceptionListA"></span><span id="removeapplicationfromexceptionlista"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTA"></span>**Removeapplicationfromexceptionlista**
</dt> <dd>

ANSI-Version von **removeapplicationfromexceptionlistw**

</dd> <dt>

<span id="CanLaunchMultiplayerGameW"></span><span id="canlaunchmultiplayergamew"></span><span id="CANLAUNCHMULTIPLAYERGAMEW"></span>**Canlaunchmultiplayergamew**
</dt> <dd>

Diese Funktion meldet, ob die Anwendung deaktiviert oder aus der Ausnahmeliste entfernt wurde. Er sollte bei jedem Ausführen des Spiels aufgerufen werden. Die-Funktion nimmt einen kompletten Pfad zur ausführbaren Datei an. Diese Funktion erfordert keine Administratorrechte.

</dd> <dt>

<span id="CanLaunchMultiplayerGameA"></span><span id="canlaunchmultiplayergamea"></span><span id="CANLAUNCHMULTIPLAYERGAMEA"></span>**Canlaunchmultiplayergamea**
</dt> <dd>

ANSI-Version von **canlaunchmultiplayergamew**

</dd> <dt>

<span id="SetMSIFirewallProperties"></span><span id="setmsifirewallproperties"></span><span id="SETMSIFIREWALLPROPERTIES"></span>**"*"**
</dt> <dd>

Dies wird nur aufgerufen, wenn Sie benutzerdefinierte Aktionen in Windows Installer verwenden. Weitere Informationen finden Sie unten.

</dd> <dt>

<span id="AddToExceptionListUsingMSI"></span><span id="addtoexceptionlistusingmsi"></span><span id="ADDTOEXCEPTIONLISTUSINGMSI"></span>**Add-exceptionlistusingmsi**
</dt> <dd>

Dies wird nur aufgerufen, wenn Sie benutzerdefinierte Aktionen in Windows Installer verwenden. Weitere Informationen finden Sie unten.

</dd> <dt>

<span id="RemoveFromExceptionListUsingMSI"></span><span id="removefromexceptionlistusingmsi"></span><span id="REMOVEFROMEXCEPTIONLISTUSINGMSI"></span>**Removefromexceptionlistusingmsi**
</dt> <dd>

Dies wird nur aufgerufen, wenn Sie benutzerdefinierte Aktionen in Windows Installer verwenden. Weitere Informationen finden Sie unten.

</dd> </dl>

In den folgenden Abschnitten werden bestimmte Methoden zum Aufrufen der exportierten DLL-Funktionen aus diesem firewallinstallhelper aus einem InstallShield-, Wise-oder Windows Installer-Paket beschrieben. Alle Methoden führen die gleichen Ergebnisse aus, und der Entwickler muss die Methode ermitteln, die implementiert werden soll.

## <a name="integrating-using-installshield-installscript"></a>Integrieren mithilfe von InstallShield InstallScript

Eine alternative Methode zur Verwendung der Firewall-APIs besteht darin, die Funktionsaufrufe einem InstallShield InstallScript hinzuzufügen. Die Schritte, die für die Integration erforderlich sind, sind recht einfach:

1.  Öffnen Sie ein InstallScript-Projekt im InstallShield-Editor.
2.  Fügen Sie dem Projekt die FirewallInstallHelper.dll als Unterstützungs Datei hinzu.

    1.  Öffnen Sie die Registerkarte Anwendungs Dateien auf der Registerkarte Projekt-Assistent.
    2.  Klicken Sie auf die Schaltfläche Dateien hinzufügen, um dem Anwendungs Zielordner Dateien hinzuzufügen.
    3.  Navigieren Sie zu der FirewallInstallHelper.dll, die Sie erstellt haben, oder verwenden Sie die im DirectX SDK bereitgestellte, und fügen Sie Sie dem Projekt hinzu.

3.  Fügen Sie dem Projekt InstallScript hinzu.

    1.  Öffnen Sie die Ansicht des Installations-Designers, und klicken Sie auf das Verhalten und die logische \| InstallScript.
    2.  Klicken Sie auf die InstallScript-Datei (normalerweise Setup. rul), um Sie im Editor zu öffnen.
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

    4.  Ändern Sie die TODO-Kommentare mit dem Anwendungsnamen, der in der Ausnahmeliste der Firewall angezeigt wird, und dem Pfad zur ausführbaren Datei des Spiels relativ zum Installationsverzeichnis.

## <a name="integrating-into-wise-for-windows-installer"></a>Integration in eine Weise für Windows Installer

Diese Schritte müssen ausgeführt werden, um die Windows Installer in eine Weise zu integrieren:

1.  Öffnen Sie Ihre Weise für Windows Installer Projekt.
2.  Wählen Sie unten die Registerkarte "Installationsexperte" aus.
3.  Klicken Sie auf Dateien, und fügen Sie die FirewallInstallHelper.dll aus dem dxsdk dem Installationsverzeichnis des Spiels hinzu.
4.  Wählen Sie unten die Registerkarte "MSI-Skript" aus.
5.  Klicken Sie im unteren Bereich auf die Registerkarte direkt ausführen.
6.  Fügen Sie nach der costfinalize-Aktion eine Aktion zum Festlegen der Eigenschaft hinzu, die FullPath auf " \[ INSTALLDIR \] relativer Pfad zur ausführbaren Datei aus dem Installationsverzeichnis" festlegt. Beispiel: " \[ INSTALLDIR \]game.exe" ohne Anführungszeichen
7.  Wählen Sie im unteren Bereich die Registerkarte "verzögert ausführen" aus.
8.  Fügen Sie nach publishproduct eine "if-Anweisung" mit der Bedingung "nicht installiert" (Groß-/Kleinschreibung wird beachtet) hinzu.
9.  Fügen Sie im If-Block eine Aktion zum Abrufen der benutzerdefinierten DLL aus dem Ziel hinzu.

    1.  Legen Sie das Feld dll-Datei auf " \[ INSTALLDIR \]FirewallInstallHelper.dll" fest.
    2.  Legen Sie das Feld Funktions Name auf "addapplicationdeexceptionlista" fest.
    3.  Fügen Sie einen Parameter mit dem Typ "Zeichen folgen Zeiger", der Wert Quelle "Property" und dem Eigenschaftsnamen "FullPath" hinzu.
    4.  Fügen Sie einen zweiten Parameter vom Typ "Zeichen folgen Zeiger", Wert Quelle "Konstante" hinzu, und legen Sie den konstanten Wert auf den gewünschten Anwendungsnamen fest, der in der Liste der Firewallausnahmen angezeigt werden soll.
    5.  Schließen Sie den If-Block durch Hinzufügen einer "End"-Anweisung.

10. Fügen Sie direkt oberhalb der RemoveFiles-Aktion am oberen Rand einen weiteren If-Block mit der Bedingung "Remove ~ =" All "" (Groß-/Kleinschreibung und ohne äußere Anführungszeichen) hinzu.
11. Fügen Sie im zweiten If-Block eine Aktion zum Abrufen der benutzerdefinierten DLL aus dem Ziel hinzu.

    1.  Legen Sie das Feld dll-Datei auf " \[ INSTALLDIR \]FirewallInstallHelper.dll" fest.
    2.  Legen Sie für das Feld Funktions Name den Wert removeapplicationfromexceptionlista fest.
    3.  Fügen Sie einen Parameter mit dem Typ "Zeichen folgen Zeiger", der Wert Quelle "Property" und dem Eigenschaftsnamen "FullPath" hinzu.
    4.  Schließen Sie den zweiten If-Block durch Hinzufügen einer "End"-Anweisung.

## <a name="integrating-into-windows-installer"></a>Integration in Windows Installer

Diese Schritte müssen ausgeführt werden, damit Sie in Windows Installer auf hoher Ebene integriert werden können. Sie werden im folgenden ausführlich erläutert:

-   Fügen Sie 2 Eigenschaften "friendlynameforfirewall" und "relativepathtoexeforfirewall" hinzu, wie unten beschrieben.
-   Nach der Aktion "costfinalize" wird in einer unmittelbaren benutzerdefinierten Aktion "setmsifirewallproperties" aufgerufen, um die entsprechenden MSI-Eigenschaften für die anderen benutzerdefinierten Aktionen festzulegen.
-   Bei der Installation nach der InstallFiles-Aktion wird eine verzögerte benutzerdefinierte Aktion aufgerufen, die die Funktion "adddeexceptionlistusingmsi" von firewallinstallhelper verwendet.
-   Bei der Deinstallation nach der InstallFiles-Aktion wird eine verzögerte benutzerdefinierte Aktion aufgerufen, die die Funktion "removefromexceptionlistusingmsi" von firewallinstallhelper verwendet.
-   Rufen Sie während des Rollbacks eine verzögerte benutzerdefinierte Aktion auf, die auch die Funktion "removefromexceptionlistusingmsi" von firewallinstallhelper aufruft.

Im folgenden finden Sie die Schritte, die dazu erforderlich sind, mithilfe eines MSI-Editors, wie z. b. Orca im Platform SDK. Beachten Sie, dass einige Editoren über Assistenten verfügen, die einige dieser Schritte vereinfachen:

1.  Öffnen Sie das MSI-Paket in Orca.
2.  Fügen Sie der binären Tabelle Folgendes hinzu:

    

    | Name     | Daten                                                                                                                                                                          |
    |----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Brand | Zeigen Sie auf den FirewallInstallHelper.dll. Diese Datei wird in das MSI-Paket eingebettet, sodass Sie diesen Schritt bei jeder erneuten Kompilierung FirewallInstallHelper.dll ausführen müssen. |

    

     

3.  Fügen Sie der Tabelle CustomAction Folgendes hinzu:

    

    | Aktion                   | type                                                                                                                                                                                                   | `Source`   | Ziel                          |
    |--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------|
    | Firewallabtmsiproperties | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue = 65                                                                                                        | Brand | "*"        |
    | Firewalladd              | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue + msidbcustomaktiontypeingescript + msidbcustomaktiontybinoidentitäts Ate = 3137                                 | Brand | Add-exceptionlistusingmsi      |
    | Firewallremove           | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue + msidbcustomaktiontypeingescript + msidbcustomaktiontybinoidentitäts Ate = 3137                                 | Brand | Removefromexceptionlistusingmsi |
    | Firewallrollbackadd      | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue + msidbcustomaktiontyperollback + msidbcustomaktiontypeingescript + msidbcustomaktiontypoperfate = 3393 | Brand | Removefromexceptionlistusingmsi |
    | Firewallrollbackremove   | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue + msidbcustomaktiontyperollback + msidbcustomaktiontypeingescript + msidbcustomaktiontypoperfate = 3393 | Brand | Add-exceptionlistusingmsi      |

    

     

4.  Fügen Sie der Tabelle InstallExecuteSequence Folgendes hinzu:

    

    | Aktion                   | Bedingung     | Sequenz | Notizen                                                                                                                                                                      |
    |--------------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Firewallabtmsiproperties |               | 1010     | Dieser Platz wird bald nach der costfinalize-                                                                                                                                       |
    | Firewalladd              | Nicht installiert | 4021     | Diese benutzerdefinierte Aktion erfolgt nur bei einer Neuinstallation. Die Sequenznummer platziert die Aktion nach "InstallFiles" und nach den Rollbacks.                              |
    | Firewallrollbackadd      | Nicht installiert | 4020     | Diese benutzerdefinierte Aktion wird nur ausgeführt, wenn eine neue Installation abgebrochen wird. Die Sequenznummer platziert die Aktion nach InstallFiles und vor der Aktion benutzerdefiniertes hinzufügen.          |
    | Firewallremove           | Installiert     | 3461     | Diese benutzerdefinierte Aktion wird nur während der Deinstallation ausgeführt. Die Sequenznummer platziert die Aktion direkt vor RemoveFiles und nach den Rollbacks.                           |
    | Firewallrollbackremove   | Nicht installiert | 3460     | Diese benutzerdefinierte Aktion wird nur ausgeführt, wenn eine Deinstallation abgebrochen wird. Die Sequenznummer platziert die Aktion direkt vor RemoveFiles und vor der benutzerdefinierten Aktion Entfernen. |

    

     

5.  Fügen Sie der Eigenschaften Tabelle Folgendes hinzu:

    

    | Eigenschaft                     | Wert                                                                             |
    |------------------------------|-----------------------------------------------------------------------------------|
    | Friendlynameforfirewall      | Muss der Name sein, der in der Ausnahmeliste angezeigt wird. Beispiel: "Beispiel Spiel" |
    | Relativepathtoexeforfirewall | Muss die installierte ausführbare Datei des Spiels sein. Beispiel: "ExampleGame.exe"  |

    

     

Weitere Informationen zu Windows Installer finden Sie unter [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="recommendations"></a>Empfehlungen

Die Firewall bleibt erhalten. Diese Empfehlungen bieten ihren Kunden eine gute Firewall-Darstellung mit Ihrem Windows-Spiel:

-   Teilen Sie den Benutzern nicht mit, dass die Firewall zum spielen Ihres Spiels deaktiviert werden muss. Dadurch ist der gesamte Computer anfällig, auch wenn er nicht in Ihrem Spiel spielt.
-   Machen Sie die Firewallkonfiguration für Ihre Benutzer nahtlos. Fügen Sie die Anwendung während der Installation zur Ausnahmeliste hinzu, und entfernen Sie die Anwendung während der Installation aus der Ausnahmeliste.
-   Geben Sie dem Benutzer Feedback, wenn multiplayerzustand durch den Firewallstatus blockiert wird. Deaktivieren Sie z. b. Netzwerk Features, wenn Sie nicht funktionieren, weil die Anwendung nicht zulässig ist oder weil sich das System im Modus "keine Ausnahmen" befindet.

 

 