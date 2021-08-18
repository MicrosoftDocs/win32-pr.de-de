---
title: Windows Spiele-Explorer für Spieleentwickler
description: In diesem Artikel wird der Prozess der Registrierung eines Spiels beim Spiele-Explorer und der Jugendschutzkontrollen in Windows Vista und Windows 7 mithilfe des neuen GDF-Schemas beschrieben.
ms.assetid: 628f14bf-2714-0d68-8267-4f7f48c2774a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6420b4783cfad7afd82483d45448ccb219342b4a7b88aa54e36c2de15ca0f778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070420"
---
# <a name="windows-games-explorer-for-game-developers"></a>Windows Spiele-Explorer für Spieleentwickler

Windows Vista verbessert die Benutzerfreundlichkeit von Spielen auf Windows durch die Einbeziehung von Games Explorer. Der Spiele-Explorer wird im Windows Vista-Startmenü als Ordner Games verfügbar gemacht und bietet einen zentralen Ort für den Zugriff auf Spiele.

Ab dem DirectX SDK-Release vom März 2009 wird ein neues GDF-Schema (Game Definition File) verwendet, um Features in Windows 7, Game Provider und RSS-Feed und IGameExplorer2 zu unterstützen. IGameExplorer2 ist eine neue Schnittstelle auf Windows 7, die die Integration eines Spiels in den Spiele-Explorer vereinfacht.

In diesem Artikel wird der Prozess der Registrierung eines Spiels beim Spiele-Explorer und der Jugendschutzkontrollen in Windows Vista und Windows 7 mithilfe des neuen GDF-Schemas beschrieben.

Inhalte:

-   [Voraussetzungen](#prerequisites)
-   [Integrieren in einen Installer](#integrating-with-an-installer)
-   [Integrationsprozess](#integration-process)
-   [Aufgaben im Spiele-Explorer](#games-explorer-tasks)
-   [Integration in InstallScript](#integrating-into-installscript)
-   [Integrieren in ein MSI-Paket](#integrating-into-an-msi-package)
-   [Debuggen Tipps](#debugging-tips)
    -   [Testen mit Beispielcode](#test-with-sample-code)
    -   [Stellen Sie sicher, dass Ihr Spiel ordnungsgemäß entfernt wurde.](#make-sure-that-your-game-was-removed-properly)
    -   [Stellen Sie sicher, dass Sie sich mit Authenticode anmelden.](#be-sure-to-sign-using-authenticode)
    -   [Stellen Sie sicher, dass Die Jugendschutzkontrollen verfügbar sind.](#be-sure-that-parental-controls-are-available)
    -   [Stellen Sie sicher, dass Tasks den richtigen Typ haben.](#verify-that-tasks-are-of-the-correct-type)
    -   [Überprüfen der Daten in der GDF-Binärdatei](#verify-the-data-in-gdf-binary)
-   [Zusammenfassung](#summary)

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie ein Spiel in den Spiele-Explorer integrieren können, müssen Sie eine Spieldefinitionsdatei (GDF) erstellen. Eine GDF ist eine XML-Datei, die Metadaten enthält, die das Spiel beschreiben. Im Release von März 2009 des DirectX SDK wurde dem GDF-Schema ein Abschnitt für Spielanbieter, RSS-Feed und Spielaufgabe hinzugefügt. Um die Anweisungen in diesem Artikel zu verwenden, müssen Sie dieses neue GDF-Format verwenden, um Ihre GDF-Datei zu erstellen.

Microsoft stellt ein Tool zum Erstellen von GDFs im DirectX SDK( Game Definition File Editor) bereit, um diesen Erstellungsprozess zu vereinfachen. Mit diesem Tool können Sie auch lokalisierte Versionen einer GDF erstellen.

Nachdem eine GDF erstellt und lokalisiert wurde, muss sie in einem Ressourcenabschnitt einer Binärdatei (entweder eine ausführbare Datei oder DLL) zusammen mit der Miniaturansicht und dem Symbol des Spiels gekapselt werden. Die GDF enthält alle metadaten, die dem Spiel zugeordnet sind, einschließlich der Bewertung des Spiels. Windows Die Jugendschutzkontrollen verwenden die Bewertung des Spiels, damit Eltern den Zugriff auf das Spiel steuern können. Die Binärdatei, die die GDF enthält, muss digital mit einem gültigen Authenticode-Zertifikat signiert werden. Andernfalls ignorieren der Spiele-Explorer und das Jugendkontrollsystem die Bewertung des Spiels, da die Bewertungsinformationen ohne Zertifizierung nicht als vertrauenswürdig eingestuft werden können. Weitere Informationen zum Signieren von Code mit Authenticode finden Sie unter [Authenticode Signing for Game Developers](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

## <a name="integrating-with-an-installer"></a>Integrieren in einen Installer

Zur Vereinfachung der Integration von Games Explorer bietet das GameUXInstallHelper-Beispiel eine allgemeine API, die unter Windows XP, Windows Vista und Windows 7 aufgerufen werden kann. Es ist für die Arbeit mit Skripts für InstallShield und Wise Installation System sowie mit benutzerdefinierten MSI-Aktionen und benutzerdefinierten Installationstools konzipiert. Die Erkennung des Betriebssystems erfolgt in dieser Beispiel-DLL, sodass sich der Aufrufer keine Gedanken darüber machen muss, ob der Client Windows XP, Windows Vista oder Windows 7 ausgeführt wird.

Die von dieser DLL exportierten Funktionen sind die folgenden:

<dl> <dt>

<span id="GameExplorerInstallW"></span><span id="gameexplorerinstallw"></span><span id="GAMEEXPLORERINSTALLW"></span>**GameExplorerInstallW**
</dt> <dd>

Registriert ein Spiel beim Spiele-Explorer, wobei ein Pfad zur GDF-Binärdatei, ein vollständiger Pfad zum Ordner, in dem das Spiel installiert ist, und der Installationsumfang angegeben sind.

</dd> <dt>

<span id="GameExplorerInstallA"></span><span id="gameexplorerinstalla"></span><span id="GAMEEXPLORERINSTALLA"></span>**GameExplorerInstallA**
</dt> <dd>

Registriert ein Spiel im Spiele-Explorer. ANSI-Version von **GameExplorerInstallW**.

</dd> <dt>

<span id="GameExplorerUninstallW"></span><span id="gameexploreruninstallw"></span><span id="GAMEEXPLORERUNINSTALLW"></span>**GameExplorerUninstallW**
</dt> <dd>

Entfernt ein Spiel aus der Registrierung beim Spiele-Explorer, wenn ein Pfad zur GDF-Binärdatei angegeben wird.

</dd> <dt>

<span id="GameExplorerUninstallA"></span><span id="gameexploreruninstalla"></span><span id="GAMEEXPLORERUNINSTALLA"></span>**GameExplorerUninstallA**
</dt> <dd>

Entfernt ein Spiel aus der Registrierung beim Spiele-Explorer. ANSI-Version von **GameExplorerUninstallW**.

</dd> <dt>

<span id="GameExplorerSetMSIProperties"></span><span id="gameexplorersetmsiproperties"></span><span id="GAMEEXPLORERSETMSIPROPERTIES"></span>**GameExplorerSetMSIProperties**
</dt> <dd>

Konfiguriert die CustomActionData-Eigenschaften für die Aktionen einer verzögerten benutzerdefinierten MSI-Installation. Die Verwendung dieser Funktion wird weiter unten in diesem Artikel ausführlich beschrieben.

</dd> <dt>

<span id="GameExplorerInstallUsingMSI"></span><span id="gameexplorerinstallusingmsi"></span><span id="GAMEEXPLORERINSTALLUSINGMSI"></span>**GameExplorerInstallUsingMSI**
</dt> <dd>

Fügt dem Spiele-Explorer ein Spiel hinzu. zur Verwendung während der Installation einer benutzerdefinierten MSI-Aktion.

</dd> <dt>

<span id="GameExplorerUninstallUsingMSI"></span><span id="gameexploreruninstallusingmsi"></span><span id="GAMEEXPLORERUNINSTALLUSINGMSI"></span>**GameExplorerUninstallUsingMSI**
</dt> <dd>

Entfernen eines Spiels aus dem Spiele-Explorer; zur Verwendung während der Installation einer benutzerdefinierten MSI-Aktion.

</dd> </dl>

Diese Funktionen werden im Header GameUXInstallHelper.h weiter erläutert.

## <a name="integration-process"></a>Integrationsprozess

Nachdem die GDF und die zugehörigen Dateien einer binären Ressource hinzugefügt wurden, ist es dann möglich, das Spiel in den Spiele-Explorer zu integrieren. Die **Verwendung von GameUXInstallHelper** vereinfacht den Integrationsprozess. Um das Spiel im Spiele-Explorer zu registrieren, rufen Sie **GameExplorerInstall** mit einem Pfad zur GDF-Binärdatei, einem vollständigen Pfad zum Ordner, in dem das Spiel installiert ist, und dem Installationsumfang auf. Um die Registrierung des Spiels zu entfernen, rufen **Sie GameExplorerUninstall mit** einem Pfad zur GDF-Binärdatei auf.

Beachten Sie, dass beim Entfernen nur eine eindeutige Installation entfernt wird. Wenn ein Spiel mehrmals installiert wurde, muss dieser Prozess für jede eindeutige Installation wiederholt werden.

## <a name="games-explorer-tasks"></a>Aufgaben im Spiele-Explorer

Aufgaben im Spiele-Explorer werden im Kontextmenü eines Elements im Spiele-Explorer angezeigt. Aufgaben sind in Wiedergabe- und Supportaufgaben unterteilt. Play-Aufgaben starten ein Spiel in einem bestimmten Modus, während Supportaufgaben anderen Zwecken dienen, einschließlich der Verknüpfung mit Websites.

In Windows Vista sind Aufgaben einfach Verknüpfungen, die sich in bestimmten Ordnern befinden. Wiedergabe- und Supportaufgaben werden in Ordnern mit den entsprechenden Namen PlayTasks und SupportTasks gespeichert. GameUXInstallHelper kann die Aufgabeninformationen des Spiels aus der GDF-Binärdatei lesen und alle Tastenkombinationen automatisch erstellen.

In Windows 7 sind die Verknüpfungen zu den Aufgaben nicht erforderlich, da der Spiele-Explorer alle Aufgabeninformationen direkt aus der GDF-Binärdatei erhält.

## <a name="integrating-into-installscript"></a>Integration in InstallScript

Das Aufrufen von Games Explorer-APIs aus InstallShield InstallScript wird mithilfe des GameUXInstallHelper-Beispiels einfach gemacht. Für die Integration in InstallShield sind die folgenden Schritte erforderlich:

1.  Öffnen Sie ein InstallScript-Projekt im InstallShield-Editor.
2.  Fügen GameUXInstallHelper.dll dem Projekt hinzu, das im Zielverzeichnis installiert werden soll.

    **So fügen sie GameUXInstallHelper.dll InstallScript-Projekt hinzu:**

    1.  Klicken Sie auf der  **Registerkarte Installations-Designer** im Navigationsbereich auf der linken Seite auf Anwendungsdaten.
    2.  Klicken **Sie auf Dateien und Ordner,** und suchen Sie in den Ordnern des Quellcomputers nach GameUXInstallerHelper.dll Dateien des **Quellcomputers.** 

        Der Standardspeicherort für GameUXInstallerHelper.dll ist DirectX \\ SDK-Stammbeispiele \\ C++ \\ Misc \\ Bin \\ x86.

    3.  Klicken **Sie unter Ordner des Zielcomputers** auf **Anwendungszielordner**.
    4.  Ziehen GameUXInstallerHelper.dll aus **den Dateien des Quellcomputers** in die Dateien **des Zielcomputers.**

3.  Klicken Sie im InstallScript-Explorer auf die InstallScript-Datei (normalerweise setup.rul), die die DLL-Funktion aufruft.
4.  Fügen Sie den folgenden InstallScript-Code in die Datei ein:

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

Im Folgenden finden Sie eine allgemeine Beschreibung der Schritte, die zum Aufrufen der Games Explorer-APIs mithilfe benutzerdefinierter MSI-Aktionen erforderlich sind:

1.  Fügen Sie der MSI-Eigenschaftentabelle eine Eigenschaft namens "RelativePathToGDF" hinzu, die den relativen Pfad zur GDF-Binärdatei enthält.
2.  Rufen Sie nach der CostFinalize-Aktion die GameUXInstallHelper-DLL-Funktion **SetMSIGameExplorerProperties** in einer sofortigen benutzerdefinierten Aktion auf, um die entsprechenden MSI-Eigenschaften für die anderen benutzerdefinierten Aktionen festlegen.
3.  Lösen Sie bei der Installation eine zurückgestellte benutzerdefinierte Aktion nach der InstallFiles-Aktion aus, die die GameUXInstallHelper-DLL-Funktion **AddToGameExplorerUsingMSI aufruft.** Wenn die Installation für alle Benutzer durchgeführt wird, muss die benutzerdefinierte Aktion das Flag msidbCustomActionTypeNoImpersonate festlegen. Andernfalls darf dieses Flag nicht festgelegt werden. Daher werden zwei nahezu identische benutzerdefinierte Aktionen definiert: GameUXAddAsAdmin und GameUXAddAsCurUser.
4.  Lösen Sie nach dem Entfernen der Installation eine verzögerte benutzerdefinierte Aktion vor der RemoveFiles-Aktion aus, die die GameUXInstallHelper-DLL-Funktion **RemoveFromGameExplorerUsingMSI aufruft.** Wenn die Installation für alle Benutzer durchgeführt wurde, muss die benutzerdefinierte Aktion das Flag msidbCustomActionTypeNoImpersonate festlegen. Andernfalls darf dieses Flag nicht festgelegt werden. Daher werden zwei nahezu identische benutzerdefinierte Aktionen definiert: GameUXRemoveAsAdmin und GameUXRemoveAsCurUser.
5.  Definieren Sie benutzerdefinierte Rollbackaktionen, um den Fall zu behandeln, dass der Benutzer die Installation oder Entfernung abbricht, nachdem eine dieser benutzerdefinierten Aktionen bereits erfolgt ist. Dies führt zu weiteren vier benutzerdefinierten Aktionen: GameUXRollBackAddAsAdmin, GameUXRollBackAddAsCurUser, GameUXRollBackRemoveAsAdmin und GameUXRollBackRemoveAsCurUser.

Dieses Verfahren wird in den folgenden Anweisungen ausführlich beschrieben, in denen ein Prozess beschrieben wird, der mithilfe eines MSI-Editors ausgeführt werden kann, z. B. dem Orca-Editor im Plattform-SDK. Einige MSI-Editoren verfügen über Assistenten, die einige dieser Konfigurationsschritte vereinfachen.

**So konfigurieren Sie ein MSI-Paket für die Integration in Den Spiele-Explorer**

1.  Öffnen Sie das MSI-Paket in Orca.
2.  Fügen Sie die in der folgenden Tabelle angezeigte Zeile der **Binärtabelle** im MSI-Paket hinzu. 

    | Name   | Daten                                          |
    |--------|-----------------------------------------------|
    | GAMEUX | Dateipfad zum \\ DLL-GameUXInstallHelper.dll |

    

     

    > [!Note]  
    > Diese Datei wird in das MSI-Paket eingebettet. Daher müssen Sie diesen Schritt jedes Mal durchführen, wenn Sie GameUXInstallHelper.dll neu kompilieren.

     

3.  Fügen Sie die in der folgenden Tabelle angezeigten Zeilen der **Tabelle CustomAction** im MSI-Paket hinzu.

    | Aktion                        | type                                                                                                                                                                                                   | `Source` | Ziel                         |
    |-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|--------------------------------|
    | GameUXSetMSIProperties        | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                                                        | GAMEUX | SetMSIGameExplorerProperties   |
    | GameUXAddAsAdmin              | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXAddAsCurUser            | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089                                                                      | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXRollBackAddAsAdmin      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRollBackAddAsCurUser    | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345                                      | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRemoveAsAdmin           | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRemoveAsCurUser         | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089                                                                      | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRollBackRemoveAsAdmin   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXRollBackRemoveAsCurUser | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345                                      | GAMEUX | AddToGameExplorerUsingMSI      |

    

     

4.  Fügen Sie die Werte für Aktion, Bedingung und Sequenz in der folgenden Tabelle der **Tabelle InstallExecuteSequence** im MSI-Paket hinzu.

    | Aktion                        | Bedingung                      | Sequenz | Hinweise                                                                                                                                                                                            |
    |-------------------------------|--------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | GameUXSetMSIProperties        |                                | 1015     | Die Sequenznummer platziert die Aktion kurz nach CostFinalize.                                                                                                                                   |
    | GameUXAddAsAdmin              | NICHT INSTALLIERT UND ALLUSERS     | 4003     | Diese benutzerdefinierte Aktion wird nur während einer Neuinstallation für alle Benutzer erfolgen. Die Sequenznummer platziert die Aktion nach InstallFiles und nach den Rollbacks.                                 |
    | GameUXAddAsCurUser            | NICHT INSTALLIERT UND NICHT ALLUSERS | 4004     | Diese benutzerdefinierte Aktion wird nur während einer Neuinstallation für den aktuellen Benutzer erfolgen. Die Sequenznummer platziert die Aktion nach InstallFiles und nach den Rollbacks.                     |
    | GameUXRollBackAddAsAdmin      | NICHT INSTALLIERT UND ALLUSERS     | 4001     | Diese benutzerdefinierte Aktion tritt nur auf, wenn eine Neuinstallation für alle Benutzer abgebrochen wird. Die Sequenznummer platziert die Aktion nach InstallFiles und vor der Aktion Benutzerdefinierte Aktion hinzufügen.             |
    | GameUXRollBackAddAsCurUser    | NICHT INSTALLIERT UND NICHT ALLUSERS | 4002     | Diese benutzerdefinierte Aktion tritt nur auf, wenn eine Neuinstallation für den aktuellen Benutzer abgebrochen wird. Die Sequenznummer platziert die Aktion nach InstallFiles und vor der Aktion Benutzerdefinierte Aktion hinzufügen. |
    | GameUXRemoveAsAdmin           | REMOVE~="ALL" UND ALLUSERS     | 3452     | Diese benutzerdefinierte Aktion wird nur während des Entfernens für alle Benutzer erfolgen. Die Sequenznummer platziert die Aktion direkt vor RemoveFiles und nach den Rollbacks.                                     |
    | GameUXRemoveAsCurUser         | REMOVE~="ALL" AND NOT ALLUSERS | 3453     | Diese benutzerdefinierte Aktion wird nur während des Entfernens für den aktuellen Benutzer erfolgen. Die Sequenznummer platziert die Aktion direkt vor RemoveFiles und nach den Rollbacks.                              |
    | GameUXRollBackRemoveAsAdmin   | REMOVE~="ALL" UND ALLUSERS     | 3450     | Diese benutzerdefinierte Aktion erfolgt nur, wenn das Entfernen für alle Benutzer abgebrochen wird. Die Sequenznummer platziert die Aktion direkt vor RemoveFiles und vor der benutzerdefinierten Aktion Entfernen.              |
    | GameUXRollBackRemoveAsCurUser | REMOVE~="ALL" AND NOT ALLUSERS | 3451     | Diese benutzerdefinierte Aktion erfolgt nur, wenn das Entfernen für den aktuellen Benutzer abgebrochen wird. Die Sequenznummer platziert die Aktion direkt vor RemoveFiles und vor der benutzerdefinierten Aktion Entfernen.       |

    

     

5.  Fügen Sie die in der folgenden Tabelle angezeigte Zeile der Tabelle Property im MSI-Paket hinzu.

    | Eigenschaft          | Wert                                                         |
    |-------------------|---------------------------------------------------------------|
    | RelativePathToGDF | Relativer \\ Dateipfadname der Binärdatei, die die GDF enthält |

    

     

    > [!Note]  
    > Der vom Pfad angegebene Speicherort ist relativ zum Speicherort, der vom Installationspfad angegeben wird. Beispiel: bin \\GDF.dll.

     

6.  Speichern Sie das MSI-Paket.

Ausführlichere Informationen zu MSI-Paketen und Windows Installer finden Sie unter [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="debugging-tips"></a>Debuggen Tipps

Im Folgenden werden einige Tipps zum Debuggen von Problemen beim Aufrufen von Games Explorer-APIs aufgeführt:

### <a name="test-with-sample-code"></a>Testen mit Beispielcode

Beim Erstellen der GameUXInstallHelper-Beispiellösung werden ein GameUXInstallHelper.dll und ein GDFInstall.exe erstellt. Der GDFInstall.exe ist eine Beispielanwendung, die GameUXInstallHelper.dll verwendet. Wenn Sie GDFInstall.exe ausführen, werden Sie aufgefordert, eine GDF-Binärdatei im Spiel-Explorer zu installieren oder zu entfernen. Sie können Ihre GDF-Binärdatei testen, indem Sie sie als erstes Befehlszeilen-Argument an GDFInstall.exe übergeben.

Wenn Sie keine GDF-Binärdatei haben oder Ihre nicht installiert werden kann, verwenden Sie das GDF-Beispiel im DirectX SDK. Das GDFExampleBinary-Beispiel befindet sich im DirectX SDK und ist nur eine DLL, die nur eine GDF-Datei enthält. In der Quelle ist auch das GDFMaker-Projekt enthalten. Sie können sie erstellen und mit GDFInstall.exe testen. Sie können auch den XML-Code mit Ihrem vergleichen, um genau zu ermitteln, wo sich das Problem befindet.

### <a name="make-sure-that-your-game-was-removed-properly"></a>Stellen Sie sicher, dass Ihr Spiel ordnungsgemäß entfernt wurde.

Wenn das Spiel bereits im Games-Explorer installiert ist, geben nachfolgende Aufrufe von **IGameExplorer::AddGame** E FAIL zurück. Stellen Sie \_ daher sicher, dass Ihr Spiel vor dem Testen nicht installiert ist. Dies gilt auch, wenn Sie gdf nur für den aktuellen Benutzer installieren und dann versuchen, gdf für alle Benutzer zu installieren. Sie müssen zuerst das Spiel aus den aktuellen Benutzern entfernen, bevor **IGameExplorer::AddGame** erfolgreich ausgeführt wird.

Wenn Sie **GDFInstall.exe** Enumeration ausführen, wechselt die Beispielanwendung in einen anderen Modus, der alle installierten Games Explorer-Spiele aufzählt und Sie auffordert, sie zu entfernen. Sie können die Registrierung auch in HKEY LOCAL MACHINE Software Microsoft Windows CurrentVersion GameUX durchsuchen und \_ \_ \\ \\ \\ \\ \\ durchsuchen, um sicherzustellen, dass Ihr Spiel nicht für einen anderen Benutzer auf dem System installiert ist. Ändern Sie diese Registrierungseinstellungen jedoch nicht für andere Zwecke, da sie in zukünftigen Versionen des Betriebssystems nicht garantiert kompatibel bleiben.

### <a name="be-sure-to-sign-using-authenticode"></a>Achten Sie darauf, dass Sie sich mit Authenticode anmelden.

Wenn Sie eine Bewertung angegeben haben, diese aber im Spiele-Explorer nicht angezeigt wird, stellen Sie sicher, dass Sie Authenticode zum Signieren der ausführbaren Datei oder DLL-Datei verwendet haben, die die Bewertung enthält. Spiele-Explorer ignoriert Bewertungsinformationen in nicht signierten Dateien. Weitere Informationen zu Authenticode finden Sie unter [Authenticode Signing for Game Developers](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

### <a name="be-sure-that-parental-controls-are-available"></a>Stellen Sie sicher, dass die Jugendschutzmaßnahmen verfügbar sind.

Stellen Sie sicher, dass Sie die Jugendschutzmaßnahmen für eine Edition von Windows Vista testen, die die Jugendschutzmaßnahmen bereitstellt: Home Basic, Home Premium oder Ultimate. Windows Vista Business und Windows Vista Enterprise keine Jugendschutzmaßnahmen bereitstellen. Wenn Sie jedoch auf Windows Vista Ultimate testen und der Testcomputer in eine Domäne eingebunden ist, müssen Sie eine Gruppenrichtlinieneinstellung ändern, um die Jugendschutzfunktionen sichtbar zu machen. Informationen hierzu finden Sie unter [Erste Schritte mit Games Explorer.](/previous-versions/windows/desktop/legacy/ee417682(v=vs.85))

### <a name="verify-that-tasks-are-of-the-correct-type"></a>Stellen Sie sicher, dass Tasks den richtigen Typ aufweisen.

Wenn Sie Unterstützungsaufgaben angegeben haben, die nicht im Spiele-Explorer angezeigt werden, überprüfen Sie, ob es sich um alle Weblinks handelt. Alle anderen Verknüpfungsaufgaben müssen als Wiedergabeaufgaben erstellt werden. Aufgaben werden weiter oben in diesem Artikel in [Games Explorer Tasks](#games-explorer-tasks)behandelt.

### <a name="verify-the-data-in-gdf-binary"></a>Überprüfen der Daten in der GDF-Binärdatei

GDFTrace.exe ist ein Tool im DirectX SDK. Sie können GDFTrace.exe für Ihre GDF-Binärdatei ausführen und alle GDF-Metadaten, die in der Binärdatei enthalten sind, für jede unterstützte Sprache ausgeben, um eine schnelle Überprüfung zu ermöglichen. Außerdem werden Warnungen zu fehlenden oder veralteten Informationen angezeigt.

## <a name="summary"></a>Zusammenfassung

Games Explorer in Windows Vista bietet eine einfache, anpassbare Möglichkeit, Ihr Spiel Benutzern von Windows Vista zu präsentieren, erfordert jedoch auch, dass Sie das Spiel während der Installation beim System registrieren. Das GameUXInstallHelper-Beispiel vereinfacht diesen Prozess für Entwickler erheblich.

 

 