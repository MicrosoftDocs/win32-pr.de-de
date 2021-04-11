---
title: Direct3D 11-Bereitstellung für Spieleentwickler
description: In diesem Artikel wird beschrieben, wie Sie die Direct3D 11-Komponenten ggf. auf einem System bereitstellen.
ms.assetid: 1fd43638-0d67-4a94-3be6-8789095f491e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd935aedee23ba731bc74e52c0773e6f02e5b5fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209317"
---
# <a name="direct3d-11-deployment-for-game-developers"></a>Direct3D 11-Bereitstellung für Spieleentwickler

In diesem Artikel wird beschrieben, wie Sie die Direct3D 11-Komponenten ggf. auf einem System bereitstellen.

-   [Übersicht](#overview)
-   [Direct3D 11,3](#direct3d-113)
-   [Direct3D 11,2](#direct3d-112)
-   [Direct3D 11,1](#direct3d-111)
-   [D3D11InstallHelper.dll](#d3d11installhelperdll)
-   [D3D11Install.exe](#d3d11installexe)
-   [Integrieren in Installationsprogramme](#integrating-into-installation-programs)
    -   [Integration in InstallShield](#integrating-into-installshield)
    -   [Integrieren in ein MSI-Paket](#integrating-into-an-msi-package)
-   [Debugtipps](#debugging-tips)
-   [Firmeneinstellungen](#corporate-settings)
-   [Verwandte Artikel](#related-articles)

## <a name="overview"></a>Übersicht

Die API Direct3D 11 erweitert die vorhandene Direct3D 10,1-API durch Unterstützung für Multithread-Rendering und Ressourcen Erstellung, COMPUTE-Shader, Hardware Mosaik, BC6H/bzw bc7-Textur Komprimierung und HLSL-Shader-Modell 5,0 durch dynamische shaderverknüpfung. Zusätzlich zur Direct3D 11-Komponente sind in der DirectX 11-Laufzeit eine Reihe zusätzlicher Grafik Komponenten enthalten: Direct3D 11, DXGI 1,1, 10level9, WARP10 Software Rendering Device, Direct2D, DirectWrite und ein aktualisiertes Direct3D 10,1 mit Unterstützung für 10level9 und WARP10. Weitere Informationen zu diesen und anderen Windows-Grafik Komponenten finden Sie unter [Grafik-APIs in Windows](graphics-apis-in-windows-vista.md).

Alle diese neuen Grafik Komponenten sind in die Betriebssysteme Windows 7 und Windows Server 2008 R2 integriert. Die Direct3D 11-API und zugehörige Komponenten können auch unter Windows Vista mithilfe eines Systemupdates aus Windows Update installiert werden. Weitere Informationen finden Sie im Knowledge Base-Artikel [KB 971644](https://support.microsoft.com/kb/971644). Dieses Update erfordert Windows Vista und Service Pack 2. Für Endbenutzer mit aktiviertem automatischem Update werden die Direct3D 11-Komponenten wahrscheinlich bereits installiert, ebenso wie alle Windows 7-Benutzer.

Das D3D11InstallHelper-Beispiel wurde entwickelt, um die Erkennung der Direct3D 11-API zu vereinfachen, das System Update automatisch zu installieren, falls es auf den Computer eines Endbenutzers anwendbar ist, und den Endbenutzern entsprechende Meldungen zur manuellen Prozedur bereitzustellen, wenn ein neueres Service Pack erforderlich ist.

> [!Note]  
> Der HLSL-Compiler (D3DCompile \* . dll) und die D3DX Utility Library für Direct3D 11 (Bibliothek d3dx11 \* . dll) sind nicht in eine Version des Windows-Betriebssystems integriert, können aber mithilfe der vorhandenen DirectSetup-Technologie als Teil des Installationsprogramms einer Anwendung bereitgestellt werden. Weitere Informationen zur Verwendung von DirectSetup finden Sie unter [DirectX-Installation für Spieleentwickler](/windows/desktop/DxTechArts/directx-setup-for-game-developers). "Effekte 11" ist als freigegebene Quell Unterstützungs Bibliothek mit [Effekten für das Update von Direct3D 11](https://github.com/Microsoft/FX11)verfügbar, und Sie können Sie direkt in eine APP einschließen (ähnlich wie die dxut Utility Library). Folglich gibt es keine zusätzlichen Anforderungen an die Lauf Zeit Weitergabe.

## <a name="direct3d-113"></a>Direct3D 11,3

Windows 10 ist mit der integrierten Direct3D 11,3-API ausgeliefert. Eine Liste der neuen Features in der Direct3D 11,3-API finden Sie unter [Direct3D 11,3 Features](/windows/desktop/direct3d11/direct3d-11-3-features) .

## <a name="direct3d-112"></a>Direct3D 11,2

Windows 8.1 und Windows Server 2012 R2 werden mit der integrierten Direct3D 11,2-API ausgeliefert. Eine Liste der neuen Features in der Direct3D 11,2-API finden Sie unter [Direct3D 11,2 Features](/windows/desktop/direct3d11/direct3d-11-2-features) .

## <a name="direct3d-111"></a>Direct3D 11,1

Windows 8 und Windows Server 2012 werden mit der integrierten [Direct3D 11,1-API](/windows/desktop/direct3d11/direct3d-11-1-features) ausgeliefert. Teil Unterstützung für die Direct3D 11,1-API ist unter Windows 7 oder Windows Server 2008 R2 mit installiertem [Platt Form Update für Windows 7](https://support.microsoft.com/kb/2670838) verfügbar. Weitere Informationen zum Platt Form Update für Windows 7 finden Sie unter [Platt Form Update für Windows 7](platform-update-for-windows-7.md).

## <a name="d3d11installhelperdll"></a>D3D11InstallHelper.dll

D3D11InstallHelper.dll hostet die Kernfunktionen zum Erkennen von Direct3D 11-Komponenten und führt ggf. das System Update über den Windows Update Dienst durch. Die DLL zeigt keine Nachrichten oder Dialogfelder direkt an.

Die dll besteht aus den folgenden Einstiegspunkten:

<dl> <dt>

<span id="CheckDirect3D11Status"></span><span id="checkdirect3d11status"></span><span id="CHECKDIRECT3D11STATUS"></span>CheckDirect3D11Status
</dt> <dd>

Diese Funktion führt die erforderlichen Überprüfungen durch und gibt den Status von Direct3D 11 auf diesem Computer zurück. Diese Funktion erfordert keine Administratorrechte.

-   Der Status installiert D3D11IH \_ gibt \_ an, dass Direct3D 11 bereits auf dem Computer installiert ist und einsatzbereit ist.
-   D3D11IH \_ Status \_ nicht \_ unterstützt gibt an, dass diese Version von Windows Direct3D 11 oder verwandte Technologien nicht unterstützt.
-   Der Status "D3D11IH \_ " \_ muss den Status "neueste SP" aufweisen \_ \_ , dass das neueste Windows Vista Service Pack vom Benutzer installiert werden muss.
-   Zum Schluss erfordert der Status D3D11IH \_ Status \_ \_ Update, dass auf dem System Direct3D 11 nicht installiert ist, aber dass das System Update auf diese Windows-Version angewendet wird.

</dd> <dt>

<span id="DoUpdateForDirect3D11"></span><span id="doupdatefordirect3d11"></span><span id="DOUPDATEFORDIRECT3D11"></span>DoUpdateForDirect3D11
</dt> <dd>

Diese Funktion verwendet die Windows Update-API, um das System Update für die Installation von Direct3D 11 auf diesem System auszuführen, falls zutreffend. Beachten Sie, dass für diese Funktion eine Netzwerk Konnektivität erforderlich ist, um Windows Update, um erfolgreich zu sein, sowie Administratorrechte. Sie nimmt eine optionale Fortschritts Rückruffunktion und einen Benutzer Kontext Zeiger an und gibt nach Abschluss einen abschließenden Ergebniscode zurück.

-   Das Ergebnis \_ \_ Erfolgs Ergebnis von D3D11IH gibt an, dass das System Update angewendet wurde und einsatzbereit ist, während der Neustart des D3D11IH- \_ Ergebnisses \_ \_ darauf hinweist, dass der Computer neu gestartet werden muss, bevor er abgeschlossen ist. Beachten Sie, dass diese Funktion keinen Systemneustart plant.
-   D3D11IH \_ Result \_ Not \_ Supported gibt an, dass das System Update nicht für diese Version von Windows gilt. Dieses Ergebnis sollte nicht auftreten, wenn diese Funktion erst aufgerufen wird, nachdem ein D3D11IH- \_ Status den \_ \_ Update Status von CheckDirect3D11Status erfordert.
-   Das Ergebnis der D3D11IH \_ - \_ Ergebnis \_ Aktualisierung \_ wurde nicht gefunden und zeigt an, dass das System Update Paket auf den Windows Update Servern nicht gefunden wurde.
-   Wenn das Windows Update herunterladen oder die Installation fehlschlägt, wird das Ergebnis des D3D11IH- \_ Ergebnis \_ Updates \_ \_ oder die D3D11IH- \_ Ergebnis \_ Update Installation \_ \_ als Ergebnis zurückgegeben.
-   Wenn ein Netzwerkkonnektivitätsproblem von der Windows Update-API zurückgegeben wird, wird das Ergebnis des D3D11IH- \_ \_ Wu- \_ Dienst \_ Fehlers zurückgegeben, das angibt, dass das Problem möglicherweise zeitweilig oder mit der Netzwerkkonfiguration oder den Firewalleinstellungen Die erneute Ausführung der Update-Funktion ist möglicherweise erfolgreich.

</dd> </dl>

Weitere Informationen zur Windows Update-API finden Sie unter [Windows Update Agent-API](/windows/desktop/Wua_Sdk/portal-client).

## <a name="d3d11installexe"></a>D3D11Install.exe

> [!Note]  
> D3D11Install.exe müssen D3D11InstallHelper.dll ausgeführt werden.

D3D11Install.exe ist ein Tool für die Verwendung D3D11InstallHelper.dll als eigenständiges Installationsprogramm mit Benutzeroberflächen-und Endbenutzer Nachrichten sowie als Beispiel für die ordnungsgemäße Verwendung der dll. Der Prozess wird mit 0 beendet, wenn Direct3D 11 bereits installiert ist, wenn das System Update erfolgreich ausgeführt wird, ohne dass ein Systemneustart erforderlich ist, wenn eine Service Pack-Installation erforderlich ist oder wenn Direct3D 11 von diesem Computer nicht unterstützt wird. 1 wird zurückgegeben, wenn das System Update erfolgreich angewendet wurde und ein Systemneustart erforderlich ist. Für andere Fehlerbedingungen wird 2 zurückgegeben. Beachten Sie, dass für diese ausführbare Datei Administratorrechte erforderlich sind und dass Sie über ein Manifest verfügt, das bei Ausführung unter Windows Vista oder Windows 7 mit aktivierter UAC eine Erhöhung der Rechte anfordert. D3D11Install.exe können als eigenständiges Tool zum Bereitstellen des Direct3D 11-Updates verwendet werden, oder es kann direkt von Installationsprogrammen verwendet werden.

Sie unterstützt die folgenden Befehls Zeilenschalter:

<dl> <dt>

<span id="_quiet__"></span><span id="_QUIET__"></span>/Quiet 
</dt> <dd>

Zeigt keine Meldungen, Eingabe Aufforderungen, Status Dialogfelder oder Fehlermeldungen an.

</dd> <dt>

<span id="_passive__"></span><span id="_PASSIVE__"></span>/passive 
</dt> <dd>

Zeigt keine Meldungen, Eingabe Aufforderungen oder Fehlermeldungen an, zeigt jedoch das Status Dialogfeld an.

</dd> <dt>

<span id="_minimal__"></span><span id="_MINIMAL__"></span>/minimal 
</dt> <dd>

Zeigt nur minimale Eingabe Aufforderungen an.

</dd> <dt>

<span id="_y__"></span><span id="_Y__"></span>/y 
</dt> <dd>

Unterdrückt die Aufforderung zur Bestätigung der Installation des Updates bei Bedarf und anwendbar für eine standardmäßige und minimale Installation.

</dd> <dt>

<span id="_langid_decimal__"></span><span id="_LANGID_DECIMAL__"></span>/langid Dezimal 
</dt> <dd>

Erzwingt den zu verwendenden sprachbezeichnercode, wenn Endbenutzer Meldungen und Dialogfeld Ressourcen angezeigt werden. Der Standardwert ist 1024, bei dem die Standard Spracheinstellung des Systems verwendet wird.

</dd> <dt>

<span id="_wu__"></span><span id="_WU__"></span>/wu 
</dt> <dd>

Erzwingt die Verwendung von Windows Update anstelle des System Standards, der auf einem verwalteten Server oder einer anderen nicht standardmäßigen Konfiguration Windows Server Update Services (WSUS) ausgeführt werden kann.

</dd> </dl>

## <a name="integrating-into-installation-programs"></a>Integrieren in Installationsprogramme

Um die Unterstützung der einfachen Installation, die [technische Anforderung 3,1 für Spiele für Windows](/windows/desktop/DxTechArts/games-for-windows-technical-requirements-1-1-0006)einzuhalten, muss sorgfältig vorgegangen werden, damit alle Eingabe Aufforderungen für Endbenutzer frühzeitig im Installationsvorgang angezeigt werden und sichergestellt werden, dass nicht mehrere UAC-bezogene Eingabe Aufforderungen für erhöhte Rechte vorhanden sind. Es gibt drei grundlegende Möglichkeiten, dieses Ziel zu erreichen:

1.  Die grundlegendste Methode besteht darin, die D3D11Install.exe mit dem Befehls Zeilenschalter **/Minimal** auszuführen. Dies sollte früh im Installationsprogramm Q&A erfolgen, und bei der Installation sollte der Rückgabewert 1 verwendet werden, um anzugeben, dass am Ende der Installation ein Neustart geplant werden soll. Zum Ausführen des Programms sind Administratorrechte erforderlich.
2.  Verwenden Sie D3D11InstallHelper.dll direkt, um die Notwendigkeit für das Update zu erkennen, und stellen Sie alle Endbenutzer-Nachrichten bereit, die für den Status erforderlich \_ sind D3D11IH Status \_ muss \_ Latest \_ SP sein, damit die Lösung manuelle Benutzer Vorgänge erfordert. Das Status Ergebnis des Status "D3D11IH" wird \_ \_ nicht \_ unterstützt, um die Installation von Direct3D 11 – zugehörigen Assets zu steuern, oder als Fehlerbedingung für Direct3D 11 – nur Anwendungen, aber ansonsten nicht notwendigerweise eine nützliche Endbenutzer Nachricht. Für den Status D3D11IH \_ \_ erfordert \_ Update, kann das Installationsprogramm direkt den DLL-Einstiegspunkt DoUpdateForDirect3D11 verwenden, um das Update auszuführen und die verschiedenen resultierenden Endbenutzer Meldungen zu verarbeiten. Beispiele für Standard Nachrichten finden Sie im Dialogfeld D3D11Install.exe und in den Zeichen folgen Tabellen Ressourcen. Der Update Einstiegspunkt erfordert Administratorrechte.
3.  Ein hybrider Ansatz besteht darin, den Status mit D3D11InstallHelper.dll zu überprüfen, und im Fall des Statuscodes D3D11IH \_ Status \_ muss den Status " \_ Latest \_ SP" oder "D3D11IH" erfordert " \_ Update" \_ \_ , D3D11Install.exe mit den Switches **/Minimal** und **/y** ausgeführt werden können, um das Dialogfeld anzuzeigen, oder um das Update nach Bedarf auszuführen. Diese Schritte sollten früh im Installationsprozess ausgeführt werden, in der Regel unmittelbar nach dem Q&A, und das Ausführen der ausführbaren Datei erfordert Administratorrechte.

### <a name="integrating-into-installshield"></a>Integration in InstallShield

Das Verarbeiten der Direct3D 11-Bereitstellung aus InstallShield InstallScript erfolgt problemlos mithilfe des D3D11InstallHelper-Beispiels. Die Schritte, die für die Integration von InstallShield mithilfe von InstallScript erforderlich sind, lauten wie folgt (mit der im vorherigen Abschnitt beschriebenen Methode 3):

1.  Öffnen Sie ein InstallScript-Projekt im InstallShield-Editor.
2.  Fügen Sie dem Projekt in **Unterstützungs Dateien** D3D11InstallHelper.dll und D3D11Install.exe hinzu.

    **So fügen Sie die Dateien dem InstallShield-Projekt hinzu**

    1.  Klicken Sie auf der Registerkarte **Installations-Designer** im Navigationsbereich auf der linken Seite unter **Verhalten und Logik** auf **Unterstützungs Dateien/-Datenträger** .
    2.  Klicken Sie auf **sprachunabhängig**, klicken Sie mit der rechten Maustaste in das Fenster **Dateien** , und wählen Sie **Dateien einfügen** aus. Navigieren Sie zum Hinzufügen von D3D11InstallHelper.dll und D3D11Install.exe. Der Standard Speicherort für diese Dateien ist: SDK Root \\ Samples \\ C++ \\ misc \\ bin \\ x86

3.  Klicken Sie im InstallScript-Explorer auf die Datei InstallScript (normalerweise Setup. rul), die die dll oder ausführbare Datei aufruft, die sich im Navigationsbereich auf der linken Seite unter **Verhalten und Logik** befindet.
4.  Fügen Sie das folgende InstallScript in die Datei im oberen Bereich ein:

    ``` syntax
#define D3D11IH_STATUS_INSTALLED       0
#define D3D11IH_STATUS_NOT_SUPPORTED   1
#define D3D11IH_STATUS_REQUIRES_UPDATE 2
#define D3D11IH_STATUS_NEED_LATEST_SP  3
#define D3D11IH_STATUS_ERROR           -1
    prototype NUMBER D3D11InstallHelper.CheckDirect3D11StatusIS();

#define D3D11IH_RESULT_SUCCESS                0
#define D3D11IH_RESULT_SUCCESS_REBOOT         1
#define D3D11IH_RESULT_NOT_SUPPORTED          2
#define D3D11IH_RESULT_UPDATE_NOT_FOUND       3
#define D3D11IH_RESULT_UPDATE_DOWNLOAD_FAILED 4
#define D3D11IH_RESULT_UPDATE_INSTALL_FAILED  5
#define D3D11IH_RESULT_WU_SERVICE_ERROR       6
#define D3D11IH_RESULT_ERROR                  -1
    prototype NUMBER D3D11InstallHelper.DoUpdateForDirect3D11IS(BOOL);
    ```

5.  Fügen Sie das folgende InstallScript direkt vor der Rückgabe 0 in die Datei in der **onfirstuibefore** -Funktion ein:

    ``` syntax
    Dlg_D3D11:
        UseDLL( SUPPORTDIR ^ "D3D11InstallHelper.DLL" );
        nResult = D3D11InstallHelper.CheckDirect3D11StatusIS();   
        UnUseDLL( SUPPORTDIR ^ "D3D11InstallHelper.DLL" );
        
        if ( nResult = D3D11IH_STATUS_REQUIRES_UPDATE
             || nResult = D3D11IH_STATUS_NEED_LATEST_SP) then
            nResult = LaunchAppAndWait(
    SUPPORTDIR^"D3D11Install.exe",
    "/minimal /y", WAIT);
            if ( nResult < 0 ) then
                MessageBox("Unable to launch D3D11Install.exe",
     SEVERE);
            elseif ( nResult == 1 ) then
                BATCH_INSTALL = 1;
            endif;          
        endif;
    ```

### <a name="integrating-into-an-msi-package"></a>Integrieren in ein MSI-Paket

Im folgenden finden Sie eine allgemeine Beschreibung der Schritte, die erforderlich sind, um die Bereitstellung von Direct3D 11 mithilfe von benutzerdefinierten MSI-Aktionen (mit der weiter oben in diesem Thema beschriebenen Methode 3) zu integrieren:

1.  Fügen Sie der MSI-Eigenschaften Tabelle RelativePathToD3D11IH eine Eigenschaft mit dem Namen  hinzu, die während der Installation den relativen Pfad zu D3D11Install.exe und D3D11InstallHelper.dll enthält (in der Regel im Medien Image). Dadurch wird auch eine MSI-Eigenschaft D3D11IH \_ Status auf den von CheckDirect3D11Status zurückgegebenen Status festgelegt (eine Zeichen folgen Eigenschaft gleich dem enumerationssymbol oder "Error").
2.  Nachdem Sie die Aktion "costfinalize" ausgeführt haben, können Sie die D3D11InstallHelper.dll-Funktion **SetD3D11InstallMSIProperties** als sofortige benutzerdefinierte Aktion zum Festlegen der entsprechenden MSI-Eigenschaften für die anderen benutzerdefinierten Aktionen aufzurufen
3.  Löst bei der Installation eine verzögerte benutzerdefinierte Aktion nach der InstallFiles-Aktion aus, die die D3D11InstallHelper.dll-Funktion **DoD3D11InstallUsingMSI** aufruft. Die benutzerdefinierte Aktion muss das Flag "msidbcustomaction typoidentitäts Ate" festlegen, um in einem erweiterten Kontext ausgeführt zu werden.
4.  Nach der InstallFinalize-Aktion wird die D3D11InstallHelper.dll-Funktion **FinishD3D11InstallUsingMSI** als sofortige benutzerdefinierte Aktion aufgerufen, um den erfolgreichen Ergebniscode der Neustart Anforderung bei Bedarf zu verarbeiten.

Dieses Verfahren wird in den folgenden Anweisungen ausführlich beschrieben, die einen Prozess beschreiben, der mit einem MSI-Editor, z. b. dem [Orca-Editor](/windows/desktop/Msi/orca-exe), ausgeführt werden kann. Einige MSI-Editoren verfügen über Assistenten, die einige dieser Konfigurationsschritte vereinfachen.

**So konfigurieren Sie ein MSI-Paket für die Integration mit D3D11InstallHelper.dll**

1.  Öffnen Sie das MSI-Paket in Orca.
2.  Fügen Sie die in der folgenden Tabelle gezeigte Zeile der Binär Tabelle im MSI-Paket hinzu.

    | Name    | Daten                                         |
    |---------|----------------------------------------------|
    | D3D11IH | Dateipfad zur DLL- \\D3D11InstallHelper.dll |

    

     

    > [!Note]  
    > Diese Datei wird in das MSI-Paket eingebettet, sodass Sie diesen Schritt bei jeder erneuten Kompilierung D3D11InstallHelper.dll ausführen müssen.

     

3.  Fügen Sie die in der folgenden Tabelle gezeigten Zeilen der Tabelle CustomAction des MSI-Pakets hinzu. 

    | Aktion              | type                                                                                                                                                                   | `Source`  | Ziel                       |
    |---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|------------------------------|
    | Direct3D11SetProps  | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue = 65                                                                        | D3D11IH | SetD3D11InstallMSIProperties |
    | Direct3D11DoInstall | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue + msidbcustomaktiontypeingescript + msidbcustomaktiontybinoidentitäts Ate = 3137 | D3D11IH | DoD3D11InstallUsingMSI       |
    | Direct3D11Finish    | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypecontinue = 65                                                                        | D3D11IH | FinishD3D11InstallUsingMSI   |

    

     

4.  Fügen Sie die Werte, die für Aktion, Bedingung und Sequenz in der folgenden Tabelle angezeigt werden, der InstallExecuteSequence-Tabelle im MSI-Paket hinzu. 

    | Aktion              | Bedingung     | Sequenz | Notizen                                                                                                                                                          |
    |---------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Direct3D11SetProps  |               | 1016     | Durch die Sequenznummer wird die Aktion bald nach "costfinalize" platziert.                                                                                                 |
    | Direct3D11DoInstall | Nicht installiert | 4004     | Diese benutzerdefinierte Aktion tritt nur während einer neuen Installation für alle Benutzer auf. Die Sequenznummer platziert die Aktion nach "InstallFiles" und nach den Rollbacks. |
    | Direct3D11Finish    |               | 6615     | Die Sequenznummer platziert die Aktion bald nach InstallFinalize.                                                                                              |

    

     

5.  Fügen Sie die in der folgenden Tabelle gezeigte Zeile der **Eigenschaften** Tabelle im MSI-Paket hinzu. 

    | Eigenschaft              | Wert                                                                        |
    |-----------------------|------------------------------------------------------------------------------|
    | RelativePathToD3D11IH | relativer Dateipfad, der D3D11Install.exe und D3D11InstallHelper.dll enthält. |

    

     

    > [!Note]  
    > Der durch den Pfad angegebene Speicherort ist relativ zum Speicherort, der durch den Installationspfad angegeben wird, z. –. "Redist \\ ".

     

6.  Speichern Sie das MSI-Paket. Ausführlichere Informationen zu MSI-Paketen und Windows Installer finden Sie unter [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="debugging-tips"></a>Tipps zum Debuggen

Sowohl D3D11InstallHelper.dll als auch D3D11Install.exe können mit der Debugkonfiguration in Visual Studio erstellt werden, und diese Versionen Drucken Meldungen an den standardmäßigen Windows-Debug-Ausgabe Mechanismus.

## <a name="corporate-settings"></a>Firmeneinstellungen

Das D3D11InstallHelper-Beispiel ist für die Standard Bereitstellung über Windows Update konzipiert. Dies ist das häufigste Szenario für die Installation eines Spiels durch Consumer. Viele Spieleentwickler, die für Verleger und in Entwicklungsstudio arbeiten, machen dies jedoch in Unternehmens Einstellungen mit einem lokal verwalteten Server, der Software Updates mithilfe von Windows Server Update Services (WSUS)-Technologie bereitstellt. In dieser Art von Umgebung verfügt der lokale IT-Administrator über die Genehmigung, welche Updates den Computern innerhalb des Unternehmensnetzwerks zur Verfügung gestellt werden, und die Standard Consumer-Version von Update KB 971644 ist nicht verfügbar.

Es gibt drei grundlegende Lösungen für die Bereitstellung von DirectX 11 in Unternehmens-/Unternehmenseinstellungen:

-   In einigen Konfigurationen ist es möglich, Windows Update direkt zu überprüfen, anstatt den lokal verwalteten WSUS-Server zu verwenden. Aus diesem Grund unterstützt D3D11InstallHelper den **/Wu** -Befehls Zeilenschalter. Allerdings lassen nicht alle Unternehmensnetzwerke Verbindungen mit den öffentlichen Microsoft-Servern zu.
-   Der lokale IT-Administrator kann KB 971512 genehmigen, ein vom Unternehmen unterstütztes Update, das von WSUS bereitgestellt wird und die Direct3D 11-API umfasst. Dies ist die einzige Möglichkeit für einen Standard Benutzer, das Update Direct3D 11 in einer Umgebung zu erhalten, die vollständig gesperrt ist.
-   Alternativ dazu können Sie auch [KB 971512](https://support.microsoft.com/kb/971512/) manuell installieren.

Es ist sehr selten, dass der Computer eines Spielers nur Updates von einem lokal verwalteten WSUS-Server erhalten kann. es handelt sich hierbei nur um Entwickler in großen Organisationen, die sich wahrscheinlich in solchen Umgebungen befinden.

## <a name="related-articles"></a>Verwandte Artikel

[Windows-Firewall für Spieleentwickler](/windows/desktop/DxTechArts/games-and-firewalls)

[Windows Games Explorer für Spieleentwickler](/windows/desktop/DxTechArts/windows-game-explorer-integration)