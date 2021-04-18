---
title: Windows Games Explorer für Spieleentwickler
description: In diesem Artikel wird beschrieben, wie Sie mit dem neuen GDF-Schema ein Spiel in Games Explorer und in Windows Vista und Windows 7 registrieren.
ms.assetid: 628f14bf-2714-0d68-8267-4f7f48c2774a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f59b90a23f407be3990a6a4e24b92d39e66852
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340924"
---
# <a name="windows-games-explorer-for-game-developers"></a>Windows Games Explorer für Spieleentwickler

Windows Vista verbessert die Benutzer Funktionen von spielen unter Windows, indem er den Spiele-Explorer einschließt. Games Explorer wird im Startmenü von Windows Vista als Ordner "Games" verfügbar gemacht und bietet einen zentralen Ort für den Zugriff auf Spiele.

Ab der Version von März 2009 des DirectX SDK wird ein neues GDF-Schema (Game Definition File) zur Unterstützung von Features in Windows 7, Spielanbieter und RSS-Feed und IGameExplorer2 verwendet. IGameExplorer2 ist eine neue Schnittstelle unter Windows 7, die den Prozess der Integration eines Spiels in den Spiele-Explorer vereinfacht.

In diesem Artikel wird beschrieben, wie Sie mit dem neuen GDF-Schema ein Spiel in Games Explorer und in Windows Vista und Windows 7 registrieren.

Inhalte:

-   [Voraussetzungen](#prerequisites)
-   [Integrieren in ein Installationsprogramm](#integrating-with-an-installer)
-   [Integrationsprozess](#integration-process)
-   [Spiele-Explorer-Tasks](#games-explorer-tasks)
-   [Integrieren in InstallScript](#integrating-into-installscript)
-   [Integrieren in ein MSI-Paket](#integrating-into-an-msi-package)
-   [Debugtipps](#debugging-tips)
    -   [Testen mit Beispielcode](#test-with-sample-code)
    -   [Stellen Sie sicher, dass Ihr Spiel ordnungsgemäß entfernt wurde.](#make-sure-that-your-game-was-removed-properly)
    -   [Signieren Sie sich mit Authenticode.](#be-sure-to-sign-using-authenticode)
    -   [Stellen Sie sicher, dass elterliche Kontrollen verfügbar sind](#be-sure-that-parental-controls-are-available)
    -   [Überprüfen Sie, ob Tasks den richtigen Typ haben.](#verify-that-tasks-are-of-the-correct-type)
    -   [Überprüfen der Daten in der GDF-Binärdatei](#verify-the-data-in-gdf-binary)
-   [Zusammenfassung](#summary)

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie ein Spiel in den Spiele-Explorer integrieren können, müssen Sie eine Spiel Definitionsdatei (GDF) erstellen. Eine GDF ist eine XML-Datei, die Metadaten enthält, die das Spiel beschreiben. In der Version vom März 2009 des DirectX SDK wurde ein Abschnitt für den Spielanbieter, den RSS-Feed und die Game-Aufgabe zum GDF-Schema hinzugefügt. Um die Anweisungen in diesem Artikel verwenden zu können, müssen Sie dieses neue GDF-Format verwenden, um die GDF-Datei zu erstellen.

Microsoft stellt ein Tool zum Erstellen von dsfs im DirectX SDK, dem Spiel Definitionsdatei-Editor, bereit, um diesen Erstellungs Prozess zu vereinfachen. Dieses Tool hilft Ihnen auch beim Erstellen lokalisierter Versionen einer GDF.

Nachdem eine GDF erstellt und lokalisiert wurde, muss Sie in einem Ressourcenabschnitt einer Binärdatei (entweder eine ausführbare Datei oder eine DLL) zusammen mit der Miniaturansicht und dem Symbol des Spiels gekapselt werden. Die GDF enthält alle Metadaten, die dem Spiel zugeordnet sind, einschließlich der Bewertung des Spiels. Die Jugend Teuerung von Windows verwendet die Bewertung des Spiels, damit übergeordnete Elemente den Zugriff auf das Spiel steuern können. Die Binärdatei, die das GDF enthält, muss mit einem gültigen Authenticode-Zertifikat digital signiert werden. Andernfalls ignoriert Games Explorer und das Eltern Steuerungssystem die Bewertung des Spiels, da die Bewertungsinformationen ohne Zertifizierung nicht vertrauenswürdig sind. Weitere Informationen zum Signieren von Code mit Authenticode finden Sie unter [Authenticode-Signierung für Spieleentwickler](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

## <a name="integrating-with-an-installer"></a>Integrieren in ein Installationsprogramm

Um die Integration von Games Explorer zu vereinfachen, bietet das gameuxinstallhelper-Beispiel eine gemeinsame API, die unter Windows XP, Windows Vista und Windows 7 aufgerufen werden kann. Es ist für die Arbeit mit Skripts für InstallShield und ein weises Installations System sowie für benutzerdefinierte MSI-Aktionen und benutzerdefinierte Installations Tools konzipiert. Die Erkennung des Betriebssystems wird in dieser Beispiel-dll behandelt, sodass sich der Aufrufer nicht darum kümmern muss, ob auf dem Client Windows XP, Windows Vista oder Windows 7 ausgeführt wird.

Die von dieser DLL exportierten Funktionen lauten wie folgt:

<dl> <dt>

<span id="GameExplorerInstallW"></span><span id="gameexplorerinstallw"></span><span id="GAMEEXPLORERINSTALLW"></span>**Gameexplorerinstallw**
</dt> <dd>

Registriert ein Spiel bei Games Explorer, wenn ein Pfad zur GDF-Binärdatei, ein vollständiger Pfad zu dem Ordner, in dem das Spiel installiert ist, und der Installationsbereich angezeigt wird.

</dd> <dt>

<span id="GameExplorerInstallA"></span><span id="gameexplorerinstalla"></span><span id="GAMEEXPLORERINSTALLA"></span>**Gameexplorerinstalla**
</dt> <dd>

Registriert ein Spiel bei Games Explorer. ANSI-Version von **gameexplorerinstallw**.

</dd> <dt>

<span id="GameExplorerUninstallW"></span><span id="gameexploreruninstallw"></span><span id="GAMEEXPLORERUNINSTALLW"></span>**Gameexploreruninstallw**
</dt> <dd>

Entfernt ein Spiel aus der Registrierung mit dem Games Explorer, wenn ein Pfad zur GDF-Binärdatei angezeigt wird.

</dd> <dt>

<span id="GameExplorerUninstallA"></span><span id="gameexploreruninstalla"></span><span id="GAMEEXPLORERUNINSTALLA"></span>**Gameexploreruninstalla**
</dt> <dd>

Entfernt ein Spiel aus der Registrierung mit dem Spiele-Explorer. ANSI-Version von **gameexploreruninstallw**.

</dd> <dt>

<span id="GameExplorerSetMSIProperties"></span><span id="gameexplorersetmsiproperties"></span><span id="GAMEEXPLORERSETMSIPROPERTIES"></span>**Gameexplorer* tmsiproperties**
</dt> <dd>

Konfiguriert die customaktiondata-Eigenschaften für die Aktionen einer verzögerten MSI-Installation. Die Verwendung dieser Funktion wird weiter unten in diesem Artikel ausführlich beschrieben.

</dd> <dt>

<span id="GameExplorerInstallUsingMSI"></span><span id="gameexplorerinstallusingmsi"></span><span id="GAMEEXPLORERINSTALLUSINGMSI"></span>**Gameexplorerinstallusingmsi**
</dt> <dd>

Fügt Spiele-Explorer ein Spiel hinzu. zur Verwendung während der Installation einer benutzerdefinierten MSI-Aktion.

</dd> <dt>

<span id="GameExplorerUninstallUsingMSI"></span><span id="gameexploreruninstallusingmsi"></span><span id="GAMEEXPLORERUNINSTALLUSINGMSI"></span>**Gameexploreruninstallusingmsi**
</dt> <dd>

Entfernt ein Spiel aus dem Spiele-Explorer. zur Verwendung während der Installation einer benutzerdefinierten MSI-Aktion.

</dd> </dl>

Diese Funktionen werden im gameuxinstallhelper. h-Header ausführlicher erläutert.

## <a name="integration-process"></a>Integrationsprozess

Nachdem die GDF und verknüpfte Dateien einer binären Ressource hinzugefügt wurden, ist es möglich, das Spiel in Games Explorer zu integrieren. Durch die Verwendung von **gameuxinstallhelper** wird der Integrationsprozess vereinfacht. Um das Spiel bei Games Explorer zu registrieren, nennen Sie **gameexplorerinstall** mit einem Pfad zur GDF-Binärdatei, einem vollständigen Pfad zu dem Ordner, in dem das Spiel installiert ist, und dem Installationsbereich. Um die Registrierung des Spiels zu entfernen, nennen Sie **gameexploreruninstall** mit einem Pfad zur GDF-Binärdatei.

Beachten Sie, dass beim Entfernungs Vorgang nur eine eindeutige Installation entfernt wird. Wenn ein Spiel mehrmals installiert wurde, muss dieser Vorgang für jede eindeutige Installation wiederholt werden.

## <a name="games-explorer-tasks"></a>Spiele-Explorer-Tasks

Spiele-Explorer-Tasks werden im Kontextmenü eines Elements in Games Explorer angezeigt. Tasks werden in Wiedergabe Aufgaben und Unterstützungsaufgaben aufgeteilt. Wiedergabe Aufgaben starten ein Spiel in einem bestimmten Modus, während Support Aufgaben einen anderen Zweck erfüllen, einschließlich der Verknüpfung mit Websites.

In Windows Vista sind Aufgaben einfach Verknüpfungen, die sich in bestimmten Ordnern befinden. Wiedergabe Aufgaben und Unterstützungsaufgaben werden in Ordnern mit den entsprechenden Namen "playtasks" und "supporttasks" gespeichert. Gameuxinstallhelper kann die Aufgabeninformationen des Spiels aus der GDF-Binärdatei lesen und alle Verknüpfungen automatisch erstellen.

In Windows 7 werden die Verknüpfungen zu den Aufgaben nicht benötigt, da Games Explorer alle Aufgabeninformationen direkt aus der GDF-Binärdatei abruft.

## <a name="integrating-into-installscript"></a>Integrieren in InstallScript

Das Aufrufen von Spiele-Explorer-APIs aus InstallShield InstallScript wird mithilfe des gameuxinstallhelper-Beispiels leicht gemacht. Die erforderlichen Schritte für die Integration von InstallShield lauten wie folgt:

1.  Öffnen Sie ein InstallScript-Projekt im InstallShield-Editor.
2.  Fügen Sie dem Projekt, das im Zielverzeichnis installiert werden soll, GameUXInstallHelper.dll hinzu.

    **So fügen Sie GameUXInstallHelper.dll einem InstallScript-Projekt hinzu:**

    1.  Klicken Sie auf der Registerkarte **Installations-Designer** im Navigationsbereich auf der linken Seite auf **Anwendungsdaten** .
    2.  Klicken Sie auf **Dateien und Ordner** , und suchen Sie in **den Quellcomputer Ordnern** nach GameUXInstallerHelper.dll in **den Dateien des Quell Computers**.

        Der Standard Speicherort für GameUXInstallerHelper.dll ist DirectX SDK Root \\ Samples \\ C++ \\ misc \\ bin \\ x86.

    3.  Klicken Sie unter **Ordner des Ziel Computers** auf **Anwendungs Zielordner**.
    4.  Ziehen Sie GameUXInstallerHelper.dll aus **den Dateien des Quell Computers** auf **die Dateien des Ziel Computers**.

3.  Klicken Sie im InstallScript-Explorer auf die Datei InstallScript (normalerweise Setup. rul), die die DLL-Funktion aufruft.
4.  Fügen Sie das folgende InstallScript in die Datei ein:

    ``` syntax
    typedef GUID
    begin
    LONG  Data1;
    SHORT Data2;
    SHORT Data3;
    CHAR  Data4(8);
    end;

    prototype LONG GameUXInstallHelper.GameExplorerInstallW(WSTRING, WSTRING, NUMBER);
    prototype LONG GameUXInstallHelper.GameExplorerUninstallW(WSTRING);

    function OnMoved()

    WSTRING gdfbin[256];
    WSTRING path[256];
    NUMBER scope;

    begin

    if !MAINTENANCE then

    UseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UseDLL( WINSYSDIR ^ "OLE32.dll" );

    path = TARGETDIR;
    gdfbin = TARGETDIR ^ "bin\\ExampleGame.exe";  // TODO: Change this to point to binary containing the GDF

    if ALLUSERS == 1 then
    scope = 3;
    else
    scope = 2;
    endif;

    GameUXInstallHelper.GameExplorerInstallW( gdfbin, path, scope);

    UnUseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UnUseDLL( WINSYSDIR ^ "OLE32.dll" );

    endif;

    end;

    function OnMoving()

    WSTRING gdfbin[256];

    begin

    if MAINTENANCE && UNINST != "" then

    UseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UseDLL( WINSYSDIR ^ "OLE32.dll" );

    gdfbin = path ^ "bin\\ExampleGame.exe";  // TODO: Change this to point to binary containing the GDF

    GameUXInstallHelper.GameExplorerUninstallW(gdfbin);
    UnUseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UnUseDLL( WINSYSDIR ^ "OLE32.dll" );

    endif;

    end;
    ```

## <a name="integrating-into-an-msi-package"></a>Integrieren in ein MSI-Paket

Im folgenden finden Sie eine allgemeine Beschreibung der Schritte, die erforderlich sind, um die Spiele-Explorer-APIs mithilfe von benutzerdefinierten MSI-Aktionen aufzurufen:

1.  Fügen Sie der MSI-Eigenschaften Tabelle eine Eigenschaft mit dem Namen "relativepathumgdf" hinzu, die den relativen Pfad zur GDF-Binärdatei enthält.
2.  Nach der Aktion "costfinalize" wird die gameuxinstallhelper-DLL-Funktion " **setmsigameexplorerproperties** " in einer unmittelbaren benutzerdefinierten Aktion aufgerufen, um die entsprechenden MSI-Eigenschaften für die anderen benutzerdefinierten Aktionen festzulegen.
3.  Löst bei der Installation eine verzögerte benutzerdefinierte Aktion nach der InstallFiles-Aktion aus, die die gameuxinstallhelper-DLL-Funktion **adddegameexplorerusingmsi** aufruft. Wenn die Installation für alle Benutzer gilt, muss die benutzerdefinierte Aktion das Flag "msidbcustomaction typoidentitäts Ate" festlegen. Andernfalls darf dieses Flag nicht festgelegt werden. Daher sind zwei fast identische benutzerdefinierte Aktionen definiert: gameuxaddasadmin und gameuxaddascurruser.
4.  Löst nach dem Entfernen der Installation eine verzögerte benutzerdefinierte Aktion vor der RemoveFiles-Aktion aus, die die gameuxinstallhelper-DLL-Funktion **removefromgameexplorerusingmsi** aufruft. Wenn die Installation für alle Benutzer erfolgte, muss die benutzerdefinierte Aktion das Flag "msidbcustomaction typoidentitäts Ate" festlegen. Andernfalls darf dieses Flag nicht festgelegt werden. Daher sind zwei fast identische benutzerdefinierte Aktionen definiert: gameuxremoveasadmin und gameuxremoveascurruser.
5.  Definieren Sie benutzerdefinierte Rollbacks-Aktionen, um den Fall zu behandeln, in dem der Benutzer das Installieren oder entfernen abbricht, nachdem eine dieser benutzerdefinierten Aktionen bereits erfolgt ist. Dies führt zu zusätzlichen vier benutzerdefinierten Aktionen: gameuxrollbackaddasadmin, gameuxrollbackaddascurruser, gameuxrollbackremoveasadmin und gameuxrollbackremoveascurruser.

Dieses Verfahren wird in den folgenden Anweisungen ausführlich beschrieben, die einen Prozess beschreiben, der mit einem MSI-Editor ausgeführt werden kann, wie z. b. dem Orca-Editor im Platform SDK. Einige MSI-Editoren verfügen über Assistenten, die einige dieser Konfigurationsschritte vereinfachen.

**So konfigurieren Sie ein MSI-Paket für die Integration in Games Explorer**

1.  Öffnen Sie das MSI-Paket in Orca.
2.  Fügen Sie die in der folgenden Tabelle gezeigte Zeile der **Binär** Tabelle im MSI-Paket hinzu. 

    | Name   | Daten                                          |
    |--------|-----------------------------------------------|
    | Gameux | Dateipfad zur DLL- \\GameUXInstallHelper.dll |

    

     

    > [!Note]  
    > Diese Datei wird in das MSI-Paket eingebettet, sodass Sie diesen Schritt bei jeder erneuten Kompilierung GameUXInstallHelper.dll ausführen müssen.

     

3.  Fügen Sie die in der folgenden Tabelle gezeigten Zeilen der Tabelle **CustomAction** des MSI-Pakets hinzu.

    | Aktion                        | type                                                                                                                                                                                                   | `Source` | Ziel                         |
    |-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|--------------------------------|
    | Gameuxentmsiproperties        | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue = 65                                                                                                        | Gameux | Eigenschaften von "" "" ".   |
    | Gameuxaddasadmin              | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue + msidbcustomaktiontypeingescript + msidbcustomaktiontybinoidentitäts Ate = 3137                                 | Gameux | AddTo gameexplorerusingmsi      |
    | Gameuxaddascurruser            | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue + msidbcustomaktiontypeingabe = 1089                                                                      | Gameux | AddTo gameexplorerusingmsi      |
    | Gameuxrollbackaddasadmin      | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue + msidbcustomaktiontyperollback + msidbcustomaktiontypeingescript + msidbcustomaktiontypoperfate = 3393 | Gameux | Removefromgameexplorerusingmsi |
    | Gameuxrollbackaddascurruser    | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue + msidbcustomaktiontyperollback + msidbcustomaktiontypeingangs Skript = 1345                                      | Gameux | Removefromgameexplorerusingmsi |
    | Gameuxremoveasadmin           | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue + msidbcustomaktiontypeingescript + msidbcustomaktiontybinoidentitäts Ate = 3137                                 | Gameux | Removefromgameexplorerusingmsi |
    | Gameuxremoveascurruser         | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue + msidbcustomaktiontypeingabe = 1089                                                                      | Gameux | Removefromgameexplorerusingmsi |
    | Gameuxrollbackremoveasadmin   | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue + msidbcustomaktiontyperollback + msidbcustomaktiontypeingescript + msidbcustomaktiontypoperfate = 3393 | Gameux | AddTo gameexplorerusingmsi      |
    | Gameuxrollbackremoveascurruser | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue + msidbcustomaktiontyperollback + msidbcustomaktiontypeingangs Skript = 1345                                      | Gameux | AddTo gameexplorerusingmsi      |

    

     

4.  Fügen Sie die Werte, die für Aktion, Bedingung und Sequenz in der folgenden Tabelle angezeigt werden, der **InstallExecuteSequence** -Tabelle im MSI-Paket hinzu.

    | Aktion                        | Bedingung                      | Sequenz | Notizen                                                                                                                                                                                            |
    |-------------------------------|--------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Gameuxentmsiproperties        |                                | 1015     | Durch die Sequenznummer wird die Aktion bald nach "costfinalize" platziert.                                                                                                                                   |
    | Gameuxaddasadmin              | Nicht installiert und ALLUSERS     | 4003     | Diese benutzerdefinierte Aktion erfolgt nur bei einer Neuinstallation für alle Benutzer. Die Sequenznummer platziert die Aktion nach "InstallFiles" und nach den Rollbacks.                                 |
    | Gameuxaddascurruser            | Nicht installiert und keine ALLUSERS | 4004     | Diese benutzerdefinierte Aktion erfolgt nur bei einer Neuinstallation nur für den aktuellen Benutzer. Die Sequenznummer platziert die Aktion nach "InstallFiles" und nach den Rollbacks.                     |
    | Gameuxrollbackaddasadmin      | Nicht installiert und ALLUSERS     | 4001     | Diese benutzerdefinierte Aktion wird nur ausgeführt, wenn eine neue Installation für alle Benutzer abgebrochen wird. Die Sequenznummer platziert die Aktion nach InstallFiles und vor der Aktion benutzerdefiniertes hinzufügen.             |
    | Gameuxrollbackaddascurruser    | Nicht installiert und keine ALLUSERS | 4002     | Diese benutzerdefinierte Aktion wird nur ausgeführt, wenn eine neue Installation nur für den aktuellen Benutzer abgebrochen wird. Die Sequenznummer platziert die Aktion nach InstallFiles und vor der Aktion benutzerdefiniertes hinzufügen. |
    | Gameuxremoveasadmin           | Remove ~ = "All" und ALLUSERS     | 3452     | Diese benutzerdefinierte Aktion wird nur während der Entfernung für alle Benutzer durchgeführt. Die Sequenznummer platziert die Aktion direkt vor RemoveFiles und nach den Rollbacks.                                     |
    | Gameuxremoveascurruser         | Remove ~ = "All" und nicht ALLUSERS | 3453     | Diese benutzerdefinierte Aktion wird nur beim Entfernen des aktuellen Benutzers ausgeführt. Die Sequenznummer platziert die Aktion direkt vor RemoveFiles und nach den Rollbacks.                              |
    | Gameuxrollbackremoveasadmin   | Remove ~ = "All" und ALLUSERS     | 3450     | Diese benutzerdefinierte Aktion wird nur ausgeführt, wenn das Entfernen für alle Benutzer abgebrochen wird. Die Sequenznummer platziert die Aktion direkt vor RemoveFiles und vor der benutzerdefinierten Aktion Entfernen.              |
    | Gameuxrollbackremoveascurruser | Remove ~ = "All" und nicht ALLUSERS | 3451     | Diese benutzerdefinierte Aktion wird nur ausgeführt, wenn das Entfernen für den aktuellen Benutzer abgebrochen wird. Die Sequenznummer platziert die Aktion direkt vor RemoveFiles und vor der benutzerdefinierten Aktion Entfernen.       |

    

     

5.  Fügen Sie die in der folgenden Tabelle gezeigte Zeile der Eigenschaften Tabelle im MSI-Paket hinzu.

    | Eigenschaft          | Wert                                                         |
    |-------------------|---------------------------------------------------------------|
    | Relativepathumgdf | relativer \\ Dateipfadname der Binärdatei, die die GDF enthält. |

    

     

    > [!Note]  
    > Der durch den Pfad angegebene Speicherort ist relativ zum Speicherort, der durch den Installationspfad angegeben wird. Beispielsweise bin \\GDF.dll.

     

6.  Speichern Sie das MSI-Paket.

Ausführlichere Informationen zu MSI-Paketen und Windows Installer finden Sie unter [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="debugging-tips"></a>Debugtipps

Im folgenden finden Sie einige Tipps zum Debuggen von Problemen beim Aufrufen von Spiele-Explorer-APIs:

### <a name="test-with-sample-code"></a>Testen mit Beispielcode

Beim Erstellen der gameuxinstallhelper-Beispiellösung werden eine GameUXInstallHelper.dll und eine GDFInstall.exe erstellt. Der GDFInstall.exe ist eine Beispielanwendung, die GameUXInstallHelper.dll verwendet. Wenn Sie GDFInstall.exe ausführen, werden Sie aufgefordert, eine GDF-Binärdatei aus dem Spiel-Explorer zu installieren oder zu entfernen Sie können die GDF-Binärdatei testen, indem Sie Sie als erste Befehlszeile mit arg an GDFInstall.exe übergeben.

Wenn Sie nicht über eine GDF-Binärdatei verfügen oder wenn Sie nicht installieren können, versuchen Sie, das Beispiel-GDF im DirectX SDK zu verwenden. Das gdfexamplebinary-Beispiel befindet sich im DirectX SDK und ist nur eine DLL, die nur eine GDF-Datei enthält. In der Quelle ist auch das zugehörige gdfmaker-Projekt enthalten. Sie können Sie erstellen und mit GDFInstall.exe testen. Sie können auch den zugehörigen XML-Code mit Ihnen vergleichen, um genau zu ermitteln, wo das Problem liegt.

### <a name="make-sure-that-your-game-was-removed-properly"></a>Stellen Sie sicher, dass Ihr Spiel ordnungsgemäß entfernt wurde.

Wenn das Spiel bereits im Spiele-Explorer installiert ist, geben nachfolgende Aufrufe von **igameexplorer:: AddGame** den Wert E \_ Fail zurück. Stellen Sie daher sicher, dass Ihr Spiel vor dem Testen nicht installiert ist. Dies gilt auch, wenn Sie die GDF nur für den aktuellen Benutzer installieren und anschließend versuchen, die GDF für alle Benutzer zu installieren. Sie müssen das Spiel zunächst aus den aktuellen Benutzern entfernen, bevor **igameexplorer:: AddGame** erfolgreich ausgeführt werden kann.

Wenn Sie **GDFInstall.exe** Enumeration ausführen, wechselt die Beispielanwendung in einen anderen Modus, in dem alle installierten Spiele-Explorer-Spiele aufgelistet werden, und Sie werden aufgefordert, Sie zu entfernen. Sie können auch die Registrierung in HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion gameux durchsuchen und Durchsuchen \\ , um sicherzustellen, dass Ihr Spiel nicht für einen anderen Benutzer auf dem System installiert ist. Ändern Sie diese Registrierungs Einstellungen jedoch nicht für andere Zwecke, da Sie in zukünftigen Versionen des Betriebssystems nicht garantiert kompatibel bleiben.

### <a name="be-sure-to-sign-using-authenticode"></a>Signieren Sie sich mit Authenticode.

Wenn Sie eine Bewertung bereitgestellt haben, diese aber nicht in Games Explorer sehen, stellen Sie sicher, dass Sie Authenticode verwendet haben, um die ausführbare Datei oder DLL-Datei zu signieren, die die Bewertung enthält. Der Spiele-Explorer ignoriert Bewertungsinformationen in nicht signierten Dateien. Weitere Informationen zu Authenticode finden Sie [unter Authenticode-Signierung für Spieleentwickler](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

### <a name="be-sure-that-parental-controls-are-available"></a>Stellen Sie sicher, dass elterliche Kontrollen verfügbar sind

Stellen Sie sicher, dass Sie die Jugendschutz Maßnahmen für eine Edition von Windows Vista testen, die Eltern Kontrollen bereitstellt: Home Basic, Home Premium oder Ultimate. Windows Vista Business und Windows Vista Enterprise bieten keine Jugendschutz Maßnahmen. Wenn Sie jedoch unter Windows Vista Ultimate testen und der Testcomputer einer Domäne angehört, müssen Sie eine Gruppenrichtlinien Einstellung ändern, um die Steuerelemente für Eltern sichtbar zu machen. Informationen hierzu finden Sie unter [Getting Started with Games Explorer](/previous-versions/windows/desktop/legacy/ee417682(v=vs.85)).

### <a name="verify-that-tasks-are-of-the-correct-type"></a>Überprüfen Sie, ob Tasks den richtigen Typ haben.

Wenn Sie Unterstützungsaufgaben angegeben haben, die nicht im Spiele-Explorer angezeigt werden, vergewissern Sie sich, dass es sich um alle Weblinks handelt. Alle anderen Verknüpfungs Aufgaben müssen als Wiedergabe Aufgaben erstellt werden. Aufgaben werden weiter oben in diesem Artikel in den [Aufgaben des Games Explorers](#games-explorer-tasks)behandelt.

### <a name="verify-the-data-in-gdf-binary"></a>Überprüfen der Daten in der GDF-Binärdatei

GDFTrace.exe ist ein Tool, das im DirectX SDK enthalten ist. Sie können GDFTrace.exe für die GDF-Binärdatei ausführen und alle GDF-Metadaten, die in der Binärdatei für jede unterstützte Sprache enthalten sind, für die schnelle Überprüfung ausgeben. Außerdem werden Warnungen zu fehlenden oder veralteten Informationen angezeigt.

## <a name="summary"></a>Zusammenfassung

Games Explorer in Windows Vista bietet eine einfache, anpassbare Möglichkeit, Ihr Spiel Benutzern von Windows Vista vorzustellen, aber es erfordert auch, dass Sie das Spiel während des Installationsvorgangs beim System registrieren. Das gameuxinstallhelper-Beispiel vereinfacht diesen Prozess für Entwickler erheblich.

 

 