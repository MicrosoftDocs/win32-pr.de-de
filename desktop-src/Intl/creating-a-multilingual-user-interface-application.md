---
description: In diesem Tutorial wird veranschaulicht, wie Sie eine monolingual-Anwendung erstellen und Sie als weltweit bereitstellen. Diese Anwendung ist in Form einer umfassenden Lösung, die in Microsoft Visual Studio erstellt wird.
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: Hinzufügen von Unterstützung für mehrsprachige Benutzeroberflächen zu Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192d9053513a7fe915990c80deb32ffdb9114910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867944"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a>Hinzufügen von Unterstützung für mehrsprachige Benutzeroberflächen zu Anwendungen

In diesem Tutorial wird veranschaulicht, wie Sie eine monolingual-Anwendung erstellen und Sie als weltweit bereitstellen. Diese Anwendung ist in Form einer umfassenden Lösung, die in Microsoft Visual Studio erstellt wird.

-   [Übersicht](#splitting-the-various-language-resource-modules-an-overview)
    -   [Die Idee hinter Hello MUI](#the-idea-behind-hello-mui)
-   [Einrichten der Hello MUI-Lösung](#setting-up-the-hello-mui-solution)
    -   [Platt Form Anforderungen](#platform-requirements)
    -   [Voraussetzungen](#prerequisites)
-   [Schritt 0: Erstellen der hart codierten Hello MUI](#step-0-creating-the-hard-coded-hello-mui)
-   [Schritt 1: Implementieren des grundlegenden Ressourcen Moduls](#step-1-implementing-the-basic-resource-module)
-   [Schritt 2: aufbauen des grundlegenden Ressourcen Moduls](#step-2-building-the-basic-resource-module)
    -   [Aufteilen der verschiedenen Sprachressourcen Module: eine Übersicht](#splitting-the-various-language-resource-modules-an-overview)
    -   [Aufteilen der verschiedenen Sprachressourcen Module: Erstellen der Dateien](#splitting-the-various-language-resource-modules-creating-the-files)
-   [Schritt 3: Erstellen eines Resource-Savvy "Hello MUI"](#step-3-creating-a-resource-savvy-hello-mui)
-   [Schritt 4: Globalisieren von "Hello MUI"](#step-4-globalizing-hello-mui)
-   [Schritt 5: Anpassen von "Hello MUI"](#step-5-customizing-hello-mui)
-   [Weitere Überlegungen zu MUI](#additional-considerations-for-mui)
    -   [Unterstützung für Konsolen Anwendungen](#support-for-console-applications)
    -   [Bestimmung der zur Laufzeit zu unterstützten Sprachen](#determination-of-languages-to-support-at-run-time)
    -   [Unterstützung komplexer Skripts in Versionen vor Windows Vista](#complex-script-support-in-versions-prior-to-windows-vista)
-   [Zusammenfassung](#summary)

## <a name="overview"></a>Übersicht

Ab Windows Vista wurde das Windows-Betriebssystem von Grund auf als mehrsprachige Plattform entwickelt, mit zusätzlicher Unterstützung, die es Ihnen ermöglicht, mehrsprachige Anwendungen zu erstellen, die das Windows MUI-Ressourcenmodell verwenden.

Dieses Tutorial veranschaulicht diese neue Unterstützung für mehrsprachige Anwendungen, indem die folgenden Aspekte abgedeckt werden:

-   Verwendet die verbesserte MUI-Platt Form Unterstützung, um mehrsprachige Anwendungen problemlos zu aktivieren.
-   Erweitert mehrsprachige Anwendungen für die Ausführung unter Windows-Versionen vor Windows Vista.
-   Berührt die zusätzlichen Überlegungen bei der Entwicklung von spezialisierten mehrsprachigen Anwendungen, wie z. b. Konsolen Anwendungen.

Diese Links helfen Ihnen, eine schnelle Auffrischung der Konzepte bei Internationalisierung und MUI zu ermöglichen:

-   [Kurze Übersicht](understanding-internationalization.md)über die Internationalisierung.
-   [MUI-Konzepte](understanding-mui.md).
-   [Verwenden von MUI zum Entwickeln von Win32-Anwendungen](using-multilingual-user-interface.md).

### <a name="the-idea-behind-hello-mui"></a>Die Idee hinter Hello MUI

Sie sind wahrscheinlich mit der klassischen Hallo Welt Anwendung vertraut, die grundlegende Programmier Konzepte veranschaulicht. Dieses Tutorial veranschaulicht, wie Sie mit dem MUI-Ressourcenmodell eine monolingual-Anwendung aktualisieren, um eine mehrsprachige Version mit dem Namen "Hello MUI" zu erstellen.

> [!Note]  
> Die Aufgaben in diesem Tutorial werden anhand der Genauigkeit, mit der diese Aktivitäten ausgeführt werden müssen, in ausführlichen Schritten beschrieben. Außerdem müssen Sie die Details für Entwickler, die nur wenig mit diesen Aufgaben vertraut sind, erläutern.

 

## <a name="setting-up-the-hello-mui-solution"></a>Einrichten der Hello MUI-Lösung

Diese Schritte beschreiben, wie Sie die Erstellung der Hello MUI-Lösung vorbereiten.

### <a name="platform-requirements"></a>Plattformanforderungen

Die Codebeispiele in diesem Tutorial müssen mithilfe des Windows Software Development Kit (SDK) für Windows 7 und Visual Studio 2008 kompiliert werden. Das Windows 7 SDK wird unter Windows XP, Windows Vista und Windows 7 installiert, und die Beispiellösung kann auf jeder dieser Betriebssystemversionen erstellt werden.

Alle Codebeispiele in diesem Tutorial sind für die Ausführung auf x86-und x64-Versionen von Windows XP, Windows Vista und Windows 7 konzipiert. Bestimmte Teile, die unter Windows XP nicht funktionieren, werden bei Bedarf genannt.

### <a name="prerequisites"></a>Voraussetzungen

1.  Installieren Sie Visual Studio 2008.

    Weitere Informationen finden Sie im [Visual Studio Developer Center](https://msdn.microsoft.com/vstudio/default.aspx).

2.  Installieren Sie die Windows SDK für Windows 7.

    Sie können Sie über die Seite Windows SDK des [Windows Developer Centers](https://msdn.microsoft.com/windowsserver/bb980924.aspx)installieren. Das SDK umfasst Hilfsprogramme zum Entwickeln von Anwendungen für Betriebssystemversionen ab Windows XP bis zu den neuesten Versionen.

    > [!Note]  
    > Wenn Sie das Paket nicht am Standard Speicherort installieren, oder wenn Sie nicht auf dem Systemlaufwerk installieren, bei dem es sich normalerweise um das Laufwerk C handelt, notieren Sie sich den Installationspfad.

     

3.  Konfigurieren Sie die Visual Studio-Befehlszeilenparameter.

    1.  Öffnen Sie ein Visual Studio-Befehlsfenster.
    2.  Der **Pfad für die Typmenge**.
    3.  Vergewissern Sie sich, dass die PATH-Variable den Pfad des Ordners bin des Windows 7 SDK enthält:... Microsoft sdert \\ Windows \\ v 7.0 \\ bin

4.  Installieren Sie das Add-on-Paket Microsoft nls-kompatible-APIs.
    > [!Note]  
    > Im Rahmen dieses Tutorials ist dieses Paket nur erforderlich, wenn Sie die Anwendung so anpassen, dass Sie unter Windows-Versionen vor Windows Vista ausgeführt werden kann. Weitere Informationen finden Sie unter [Schritt 5: Anpassen von Hello MUI](#step-5-customizing-hello-mui).

     

    1.  Laden Sie das Paket von seiner [Download Website](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en)herunter, und installieren Sie es.
    2.  Wenn Sie das Paket nicht am Standard Speicherort installieren, oder wenn Sie nicht auf dem Systemlaufwerk installieren (normalerweise Laufwerk C), notieren Sie sich den Installationspfad, wenn Sie das Paket nicht am Standard Speicherort installieren. Windows SDK
    3.  Wenn Ihre Entwicklungsplattform Windows XP oder Windows Server 2003 ist, vergewissern Sie sich, dass Nlsdl.dll ordnungsgemäß installiert und registriert ist.

        1.  Navigieren Sie zum Ordner "Redist" unter dem Speicherort des Installations Pfads.
        2.  Führen Sie die entsprechende verteilbare nlsdl aus \* . exe, z. b. nlsdl.x86.exe. In diesem Schritt werden Nlsdl.dll installiert und registriert.

    > [!Note]  
    > Wenn Sie eine Anwendung entwickeln, die MUI verwendet und unter Windows-Versionen vor Windows Vista ausgeführt werden muss, müssen Nlsdl.dll auf der Windows-Zielplattform vorhanden sein. In den meisten Fällen bedeutet dies, dass die Anwendung das verteilbare nlsdl-Installationsprogramm ausführen und installieren muss (und nicht nur Nlsdl.dll selbst kopieren).

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a>Schritt 0: Erstellen der hart codierten Hello MUI

Dieses Tutorial beginnt mit der Version der Version "Hello MUI" in der Version. Die Anwendung geht von der Verwendung der C++-Programmiersprache, breit Zeichenfolgen und der [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) -Funktion für die Ausgabe aus.

Erstellen Sie zunächst die anfängliche Anwendung "guistep \_ 0" und die Lösung "hellomui", die alle Anwendungen in diesem Tutorial enthält.

1.  Erstellen Sie in Visual Studio 2008 ein neues Projekt. Verwenden Sie die folgenden Einstellungen und Werte:

    1.  Projekttyp: Wählen Sie unter Visual C++ Win32 aus, und wählen Sie dann unter von Visual Studio installierte Vorlagen Win32-Projekt aus.
    2.  Name: guistep \_ 0.
    3.  Speicherort: *projectrootdirectory* (spätere Schritte verweisen auf dieses Verzeichnis).
    4.  Projektmappenname: hellomui.
    5.  Aktivieren Sie Projektmappenverzeichnis erstellen.
    6.  Wählen Sie im Win32-Anwendungs-Assistenten den Standard Anwendungstyp: Windows-Anwendung aus.

2.  Konfigurieren Sie das Projekt Threading Modell:

    1.  Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf das Projekt guistep \_ 0, und wählen Sie dann Eigenschaften aus.
    2.  Im Dialogfeld Eigenschaften Seiten für Projekt:

        1.  Legen Sie in der Dropdown-Dropdown-Dropdown-Datei die Konfiguration auf alle Konfigurationen fest
        2.  Erweitern Sie unter Konfigurations Eigenschaften die Option C/C++, wählen Sie Code Generierung aus, und legen Sie Lauf Zeit Bibliothek: Multithread Debuggen (/MTD) fest.

3.  Ersetzen Sie den Inhalt von "guistep \_ 0. cpp" durch den folgenden Code:
    ```C++
    // GuiStep_0.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_0.h"

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        MessageBoxW(NULL,L"Hello MUI",L"HelloMUI!",MB_OK | MB_ICONINFORMATION);
        return 0;
    }
    ```

    

4.  Erstellen Sie die Anwendung, und führen Sie sie aus.

Der unkomplizierte Quellcode ist die vereinfachte Entwurfs Auswahl von Hard-Coding oder Einbettungen, die gesamte Ausgabe, die dem Benutzer angezeigt wird – in diesem Fall der Text "Hello MUI". Diese Auswahl schränkt das Hilfsprogramm der Anwendung für Benutzer ein, die das englische Wort "Hello" nicht kennen. Da MUI ein Technologie basiertes englisches Akronym ist, wird für dieses Tutorial angenommen, dass die Zeichenfolge für alle Sprachen "MUI" bleibt.

## <a name="step-1-implementing-the-basic-resource-module"></a>Schritt 1: Implementieren des grundlegenden Ressourcen Moduls

Microsoft Win32 bietet den Anwendungsentwicklern seit langem die Möglichkeit, ihre UI-Ressourcen Daten aus dem Quellcode der Anwendung zu trennen. Diese Trennung erfolgt in Form des Win32-Ressourcen Modells, in dem Zeichen folgen, Bitmaps, Symbole, Meldungen und andere Elemente, die normalerweise für einen Benutzer angezeigt werden, in einen unterschiedlichen Abschnitt der ausführbaren Datei gepackt werden, der vom ausführbaren Code getrennt ist.

Um diese Trennung zwischen ausführbarem Code und Ressourcen Daten Verpackung zu veranschaulichen, wird in diesem Schritt die zuvor hart codierte "Hello"-Zeichenfolge (die "en-US"-Ressource) in diesem Schritt in den Ressourcenabschnitt eines dll-Moduls im Projekt "hellomodule \_ en US" eingefügt \_ .

Diese Win32-DLL kann auch eine ausführbare Bibliothekstypen Funktion enthalten (wie jede andere dll möglicherweise). Um sich auf die im Zusammenhang mit Win32-ressourcenbezogenen Aspekte zu konzentrieren, lassen wir den Code der Lauf Zeit-dll in "DllMain. cpp" aus. In den nachfolgenden Abschnitten dieses Tutorials werden die hier erstellten Ressourcen Daten von hellomodule verwendet, und es werden auch der entsprechende Lauf Zeit Code dargestellt.

Um ein Win32-Ressourcen Modul zu erstellen, erstellen Sie zunächst eine DLL mit einem stubout-DllMain:

1.  Fügen Sie der Projekt Mappe "hellomui" ein neues Projekt hinzu:

    1.  Wählen Sie im Menü Datei die Option hinzufügen und dann neues Projekt aus.
    2.  Projekttyp: Win32-Projekt.
    3.  Name: hellomodule \_ en \_ US.
    4.  Speicherort: *projectrootdirectory* \\ hellomui.
    5.  Wählen Sie im Win32-Anwendungs-Assistenten Anwendungstyp: dll aus.

2.  Das Threading Modell dieses Projekts konfigurieren:

    1.  Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf das Projekt hellomodule \_ en \_ US, und wählen Sie Eigenschaften aus.
    2.  Im Dialogfeld Eigenschaften Seiten des Projekts:

        1.  Legen Sie in der Dropdown-Dropdown-Dropdown-Datei die Konfiguration auf alle Konfigurationen fest
        2.  Erweitern Sie unter Konfigurations Eigenschaften die Option C/C++, wählen Sie Code Generierung aus, und legen Sie Lauf Zeit Bibliothek: Multithread Debuggen (/MTD) fest.

3.  Untersuchen Sie DllMain. cpp. (Es kann sein, dass Sie den Verweis \_ hinzufügen möchten. Parameter Makros für den generierten Code, wie hier beschrieben, damit es auf Warnstufe 4 kompiliert werden kann.)
    ```C++
    // dllmain.cpp : Defines the entry point for the DLL application.
    #include "stdafx.h"

    BOOL APIENTRY DllMain( HMODULE hModule,
                           DWORD  ul_reason_for_call,
                           LPVOID lpReserved
                         )
    {
        UNREFERENCED_PARAMETER(hModule);
        UNREFERENCED_PARAMETER(lpReserved);

        switch (ul_reason_for_call)
        {
        case DLL_PROCESS_ATTACH:
        case DLL_THREAD_ATTACH:
        case DLL_THREAD_DETACH:
        case DLL_PROCESS_DETACH:
            break;
        }
        return TRUE;
    }
    ```

    

4.  Fügen Sie dem Projekt eine Ressourcen Definitionsdatei "hellomodule. RC" hinzu:

    1.  Klicken Sie im Projekt hellomodule en mit der \_ \_ rechten Maustaste auf den Ordner Ressourcen Dateien, und wählen Sie hinzufügen und dann neues Element aus.
    2.  Wählen Sie im Dialogfeld Neues Element hinzufügen Folgendes aus:

        1.  Kategorien: Wählen Sie unter Visual C++ Ressource auswählen aus, und wählen Sie dann unter "installierte Vorlagen von Visual Studio" die Ressourcen Datei (. RC) aus.
        2.  Name: hellomodule.
        3.  Speicherort: übernehmen Sie die Standardeinstellung.
        4.  Klicken Sie auf Hinzufügen.

    3.  Geben Sie an, dass die neue Datei "hellomodule. RC" als Unicode gespeichert werden soll:

        1.  Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf hellomodule. RC, und wählen Sie Code anzeigen aus.
        2.  Wenn eine Meldung angezeigt wird, in der Sie darüber informiert werden, dass die Datei bereits geöffnet ist, und Sie gefragt werden, ob Sie Sie schließen möchten, klicken Sie auf Ja.
        3.  Wenn die Datei als Text angezeigt wird, erstellen Sie die Menü Auswahl Datei und dann erweiterte Speicheroptionen.
        4.  Geben Sie unter Codierung die Angabe Unicode-Codepage 1200 an.
        5.  Klicken Sie auf OK.
        6.  Speichern und schließen Sie hellomodule. rc.

    4.  Fügen Sie eine Zeichen folgen Tabelle mit der Zeichenfolge "Hello" hinzu:

        1.  Klicken Sie im Ressourcenansicht mit der rechten Maustaste auf hellomodule. RC, und wählen Sie Ressource hinzufügen aus.
        2.  Wählen Sie Zeichen folgen Tabelle aus.
        3.  Klicken Sie auf Neu.
        4.  Fügen Sie der Zeichen folgen Tabelle eine Zeichenfolge hinzu:

            1.  ID: Hello \_ MUI \_ Str \_ 0.
            2.  Wert: 0.
            3.  Beschriftung: Hello.

        Wenn Sie "hellomodule. RC" jetzt als Text anzeigen, werden verschiedene Teile des Ressourcen spezifischen Quellcodes angezeigt. Das größte Interesse ist der Abschnitt, der die Zeichenfolge "Hello" beschreibt:

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "Hello"
        END
        ```

        

        Diese "Hello"-Zeichenfolge ist die Ressource, die lokalisiert (übersetzt, übersetzt) werden muss, in jede Sprache, die von der Anwendung unterstützt wird. Beispielsweise enthält die hellomodule- \_ TA \_ in Project (die im nächsten Schritt erstellt wird) eine eigene lokalisierte Version von hellomodule. RC für "TA-in":

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "வணக்கம்"
        END
        ```

        

    5.  Erstellen Sie das Projekt "hellomodule \_ en \_ US", um sicherzustellen, dass keine Fehler vorliegen.

5.  Erstellen Sie sechs weitere Projekte in der hellomui-Lösung (oder beliebig viele), um sechs weitere Ressourcen-DLLs für zusätzliche Sprachen zu erstellen. Verwenden Sie die Werte in dieser Tabelle:

    | Projektname        | Name der RC-Datei | Zeichenfolgen-ID          | Zeichenfolgenwert | Zeichen folgen Beschriftung |
    |---------------------|------------------|--------------------|--------------|----------------|
    | Hellomodule \_ de \_ de | Hellomodule      | Hello \_ MUI \_ Str \_ 0 | 0            | Hallo          |
    | Hellomodule \_ es \_ es | Hellomodule      | Hello \_ MUI \_ Str \_ 0 | 0            | Nachdrücklich           |
    | Hellomodule \_ fr \_ fr | Hellomodule      | Hello \_ MUI \_ Str \_ 0 | 0            | Bonjour        |
    | Hellomodule \_ Hi \_ in | Hellomodule      | Hello \_ MUI \_ Str \_ 0 | 0            | नमस्           |
    | Hellomodule \_ ru \_ ru | Hellomodule      | Hello \_ MUI \_ Str \_ 0 | 0            | "", "".   |
    | Hellomodule- \_ TA \_ in | Hellomodule      | Hello \_ MUI \_ Str \_ 0 | 0            | வணக்கம்        |

    

     

Weitere Informationen zur. rc-Dateistruktur und-Syntax finden Sie unter [Informationen zu Ressourcen Dateien](../menurc/about-resource-files.md).

## <a name="step-2-building-the-basic-resource-module"></a>Schritt 2: aufbauen des grundlegenden Ressourcen Moduls

Die Verwendung früherer Ressourcen Modelle führt zum Aufbau eines der sieben hellomodule-Projekte zu sieben separaten DLLs. Jede DLL enthält einen Ressourcenabschnitt mit einer einzelnen Zeichenfolge, die in der entsprechenden Sprache lokalisiert ist. Obwohl es für das historische Win32-Ressourcenmodell geeignet ist, nutzt dieser Entwurf nicht MUI.

Im Windows Vista SDK und höher bietet MUI die Möglichkeit, ausführbare Dateien in Quellcode und lokalisierbare Inhalts Module aufzuteilen. Mit der zusätzlichen Anpassung, die später in Schritt 5 behandelt wird, können Anwendungen für die mehrsprachige Unterstützung für Versionen vor Windows Vista aktiviert werden.

Die primären Mechanismen zum Aufteilen von Ressourcen aus ausführbarem Code, beginnend mit Windows Vista, sind folgende:

-   Verwenden von rc.exe (dem RC-Compiler) mit bestimmten Switches oder
-   Verwenden eines Tools zum Aufteilen von postbuilds namens muirct.exe.

Weitere Informationen finden Sie unter [Ressourcen Hilfsprogramme](resource-utilities.md) .

Der Einfachheit halber wird in diesem Tutorial muirct.exe verwendet, um die ausführbare Datei "Hello MUI" aufzuteilen.

### <a name="splitting-the-various-language-resource-modules-an-overview"></a>Aufteilen der verschiedenen Sprachressourcen Module: eine Übersicht

Ein mehrstufiges Verfahren ist daran beteiligt, die DLLs in eine ausführbare HelloModule.dll und eine HelloModule.dll. MUI für jede der sieben unterstützten Sprachen in diesem Tutorial aufzuteilen. In dieser Übersicht werden die erforderlichen Schritte beschrieben. der nächste Abschnitt enthält eine Befehlsdatei, die diese Schritte ausführt.

Teilen Sie zunächst das englische HelloModule.dll Modul mit dem folgenden Befehl:


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



In der obigen Befehlszeile wird die Konfigurationsdatei "dorevercmuiloc. rcconfig" verwendet. Diese Art von Konfigurationsdatei wird in der Regel von muirct.exe verwendet, um Ressourcen zwischen der sprach neutralen dll (LN) und den sprach abhängigen MUI-Dateien aufzuteilen. In diesem Fall gibt die XML-Datei "dorevertarmuiloc. rcconfig" (aufgelistet im nächsten Abschnitt) viele Ressourcentypen an, Sie sind jedoch in der Kategorie "localizedresources" oder der MUI-Datei enthalten, und es sind keine Ressourcen in der sprach neutralen Kategorie vorhanden. Weitere Informationen zum Vorbereiten einer Ressourcen Konfigurationsdatei finden Sie unter [Vorbereiten einer Ressourcen Konfigurationsdatei](preparing-a-resource-configuration-file.md).

Zusätzlich zum Erstellen einer HelloModule.dll. MUI-Datei, die die englische Zeichenfolge "Hello" enthält, bettet muirct.exe auch während der Aufteilung eine MUI-Ressource in das HelloModule.dll-Modul ein. Um zur Laufzeit die entsprechenden Ressourcen aus den sprachspezifischen HelloModule.dll. MUI-Modulen ordnungsgemäß zu laden, muss für jede MUI-Datei die Prüfsummen korrigiert werden, damit Sie mit den Prüfsummen im sprach neutralen LN-Modul der Baseline identisch sind. Dies wird durch einen Befehl wie z. b.:


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



Auf ähnliche Weise wird muirct.exe aufgerufen, um eine HelloModule.dll MUI-Datei für jede andere Sprache zu erstellen. In diesen Fällen wird die sprachneutrale dll jedoch verworfen, da nur der erste erstellt werden muss. Die Befehle, die die Spanisch-und Französisch-Ressourcen verarbeiten, sehen wie folgt aus:


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



Eine der wichtigsten Punkte, die in den obigen muirct.exe Befehlszeilen zu beachten ist, besteht darin, dass das-x-Flag verwendet wird, um eine Zielsprachen-ID anzugeben. Der für muirct.exe angegebene Wert ist für jedes sprachspezifische HelloModule.dll Modul anders. Dieser sprach Wert ist zentral und wird von muirct.exe verwendet, um die MUI-Datei beim Aufteilen entsprechend zu kennzeichnen. Ein falscher Wert erzeugt Fehler beim Laden von Ressourcen für diese bestimmte MUI-Datei zur Laufzeit. Weitere Informationen zum Zuordnen von Sprachen Namen zu LCID finden Sie unter [sprach Bezeichner-Konstanten und-](language-identifier-constants-and-strings.md) Zeichen folgen.

Jede "Split. MUI"-Datei wird am Ende in ein Verzeichnis eingefügt, das dem Sprachnamen entspricht, und zwar direkt unterhalb des Verzeichnisses, in dem sich die sprachneutrale HelloModule.dll befinden wird. Weitere Informationen zum Platzieren von MUI-Dateien finden Sie unter [Anwendungs Bereitstellung](application-deployment.md).

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a>Aufteilen der verschiedenen Sprachressourcen Module: Erstellen der Dateien

In diesem Tutorial erstellen Sie eine Befehlsdatei, die die Befehle zum Aufteilen der verschiedenen DLLs enthält, und Sie rufen Sie manuell auf. Beachten Sie, dass Sie bei der eigentlichen Entwicklung das Potenzial von Buildfehlern reduzieren können, indem Sie diese Befehle als Präbuildereignisse oder Postbuildereignisse in der hellomui-Lösung einschließen, aber dies würde den Rahmen dieses Tutorials sprengen.

Erstellen Sie die Dateien für den Debugbuild:

1.  Erstellen Sie die Befehlsdatei "dorevercmuiloc. cmd", die die folgenden Befehle enthält:
    ```C++
    mkdir .\en-US
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui

    mkdir .\de-DE
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0407 -g 0x0407 .\HelloModule_de_de.dll .\HelloModule_discard.dll .\de-DE\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e de-DE\HelloModule.dll.mui

    mkdir .\es-ES
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

    mkdir .\fr-FR
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui

    mkdir .\hi-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0439 -g 0x0407 .\HelloModule_hi_in.dll .\HelloModule_discard.dll .\hi-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e hi-IN\HelloModule.dll.mui

    mkdir .\ru-RU
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0419 -g 0x0407 .\HelloModule_ru_ru.dll .\HelloModule_discard.dll .\ru-RU\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ru-RU\HelloModule.dll.mui

    mkdir .\ta-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0449 -g 0x0407 .\HelloModule_ta_in.dll .\HelloModule_discard.dll .\ta-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ta-IN\HelloModule.dll.mui
    pause
    ```

    

2.  Erstellen Sie die XML-Datei "dorevercmuiloc. rcconfig", die die folgenden Zeilen enthält:
    ```C++
    <?xml version="1.0" encoding="utf-8"?>
        <localization>
            <resources>
                <win32Resources fileType="Application">
                    <neutralResources>
                    </neutralResources>
                    <localizedResources>
                        <resourceType typeNameId="#1"/>
                        <resourceType typeNameId="#10"/>
                        <resourceType typeNameId="#1024"/>
                        <resourceType typeNameId="#11"/>
                        <resourceType typeNameId="#12"/>
                        <resourceType typeNameId="#13"/>
                        <resourceType typeNameId="#14"/>
                        <resourceType typeNameId="#15"/>
                        <resourceType typeNameId="#16"/>
                        <resourceType typeNameId="#17"/>
                        <resourceType typeNameId="#18"/>
                        <resourceType typeNameId="#19"/>
                        <resourceType typeNameId="#2"/>
                        <resourceType typeNameId="#20"/>
                        <resourceType typeNameId="#2110"/>
                        <resourceType typeNameId="#23"/>
                        <resourceType typeNameId="#240"/>
                        <resourceType typeNameId="#3"/>
                        <resourceType typeNameId="#4"/>
                        <resourceType typeNameId="#5"/>
                        <resourceType typeNameId="#6"/>
                        <resourceType typeNameId="#7"/>
                        <resourceType typeNameId="#8"/>
                        <resourceType typeNameId="#9"/>
                        <resourceType typeNameId="HTML"/>
                        <resourceType typeNameId="MOFDATA"/>
                    </localizedResources>
                </win32Resources>
            </resources>
        </localization>
    ```

    

3.  Kopieren Sie doreversemuiloc. cmd und doreversemuiloc. rcconfig in *projectrootdirectory* \\ hellomui \\ Debug.
4.  Öffnen Sie die Visual Studio 2008-Eingabeaufforderung, und navigieren Sie zum Debugverzeichnis.
5.  Führen Sie doreverdormuiloc. cmd aus.

Wenn Sie einen Releasebuild erstellen, kopieren Sie die gleichen Dateien "doreversemuiloc. cmd" und "doreversemuiloc. rcconfig" in das releaseverzeichnis, und führen Sie dort die Befehlsdatei aus.

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a>Schritt 3: Erstellen eines Resource-Savvy "Hello MUI"

Aufbauend auf dem ersten hart codierten guistep \_0.exe Beispiel oben können Sie die Reichweite der Anwendung auf mehrere sprach Benutzer ausweiten, indem Sie das Win32-Ressourcenmodell integrieren. Der in diesem Schritt vorgestellte neue Lauf Zeit Code umfasst das Laden von Modulen ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) und das Abrufen von Zeichen folgen ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)).

1.  Fügen Sie der Projekt Mappe hellomui (mithilfe der Menü Auswahl Datei, hinzufügen und neues Projekt) ein neues Projekt mit den folgenden Einstellungen und Werten hinzu:

    1.  Projekttyp: Win32-Projekt.
    2.  Name: guistep \_ 1.
    3.  Speicherort: übernehmen Sie die Standardeinstellung.
    4.  Wählen Sie im Win32-Anwendungs-Assistenten den Standard Anwendungstyp: Windows-Anwendung aus.

2.  Legen Sie fest, dass dieses Projekt in Visual Studio ausgeführt wird, und konfigurieren Sie das Thread Modell:

    1.  Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf das Projekt guistep \_ 1, und wählen Sie als Startprojekt festlegen aus.
    2.  Klicken Sie erneut mit der rechten Maustaste, und wählen Sie Eigenschaften aus.
    3.  Im Dialogfeld Eigenschaften Seiten des Projekts:

        1.  Legen Sie in der Dropdown-Dropdown-Dropdown-Datei die Konfiguration auf alle Konfigurationen fest
        2.  Erweitern Sie unter Konfigurations Eigenschaften die Option C/C++, wählen Sie Code Generierung aus, und legen Sie Lauf Zeit Bibliothek: Multithread Debuggen (/MTD) fest.

3.  Ersetzen Sie den Inhalt von guistep \_ 1. cpp durch den folgenden Code:
    ```C++
    // GuiStep_1.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_1.h"
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Basic application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 2. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 3. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 4. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }
    ```

    

4.  Erstellen Sie die Anwendung, und führen Sie sie aus. Die Ausgabe wird in der Sprache angezeigt, die zurzeit als Anzeige Sprache des Computers festgelegt ist (vorausgesetzt, es handelt sich dabei um eine der sieben Sprachen, die wir erstellt haben).

## <a name="step-4-globalizing-hello-mui"></a>Schritt 4: Globalisieren von "Hello MUI"

Obwohl im vorherigen Beispiel die Ausgabe in verschiedenen Sprachen angezeigt werden kann, ist Sie in einigen Bereichen kurz. Vielleicht das auffälligste ist, dass die Anwendung nur in einer kleinen Teilmenge von Sprachen verfügbar ist, im Vergleich zum Windows-Betriebssystem selbst. Wenn z. b. die Anwendung "guistep \_ 1" aus dem vorherigen Schritt auf einem japanischen Build von Windows installiert wurde, wäre es wahrscheinlich, dass Ressourcen Speicherort Fehler auftreten.

Um diese Situation zu beheben, haben Sie zwei primäre Optionen:

-   Stellen Sie sicher, dass Ressourcen in einer vordefinierten, ultimativen Fall Back Sprache eingeschlossen werden.
-   Bieten Sie dem Endbenutzer die Möglichkeit, Ihre Spracheinstellungen aus der Teilmenge von Sprachen zu konfigurieren, die speziell von der Anwendung unterstützt werden.

Diese Optionen sind dringend empfehlenswert und werden in diesem Tutorial implementiert, indem das Flag "-g" an muirct.exe übergeben wird, wie oben gezeigt. Dieses Flag weist muirct.exe an, eine bestimmte Sprache (de-de/0x0407) zu der Ultimate-Fall Back Sprache zu machen, die dem sprach neutralen dll-Modul (HelloModule.dll) zugeordnet ist. Zur Laufzeit wird dieser Parameter als letztes Mittel zum Generieren von Text verwendet, der dem Benutzer angezeigt wird. Wenn eine ultimative Fall Back Sprache nicht gefunden wird und in der sprach neutralen Binärdatei keine geeignete Ressource verfügbar ist, tritt beim Laden der Ressource ein Fehler auf. Daher sollten Sie sorgfältig die Szenarien ermitteln, die Ihre Anwendung möglicherweise trifft, und die endgültige Fall Back Sprache entsprechend planen.

Die andere Möglichkeit, konfigurierbare Spracheinstellungen zuzulassen und Ressourcen basierend auf dieser benutzerdefinierten Hierarchie zu laden, kann die Kundenzufriedenheit erheblich steigern. Leider ist es auch komplizierter, wenn die Funktionalität innerhalb der Anwendung erforderlich ist.

In diesem Schritt des Tutorials wird ein vereinfachter Textdatei-Mechanismus verwendet, um die benutzerdefinierte Benutzer Sprachkonfiguration zu aktivieren. Die Textdatei wird zur Laufzeit von der Anwendung analysiert, und die analysierte und validierte Sprachliste wird beim Einrichten einer benutzerdefinierten Fall Back Liste verwendet. Nachdem die benutzerdefinierte Fall Back Liste festgelegt wurde, werden die Ressourcen von den Windows-APIs entsprechend der in dieser Liste aufgeführten sprach Rangfolge geladen. Der Rest des Codes ähnelt dem, der im vorherigen Schritt gefunden wurde.

1.  Fügen Sie der Projekt Mappe hellomui (mithilfe der Menü Auswahl Datei, hinzufügen und neues Projekt) ein neues Projekt mit den folgenden Einstellungen und Werten hinzu:

    1.  Projekttyp: Win32-Projekt.
    2.  Name: guistep \_ 2.
    3.  Speicherort: übernehmen Sie die Standardeinstellung.
    4.  Wählen Sie im Win32-Anwendungs-Assistenten den Standard Anwendungstyp: Windows-Anwendung aus.

2.  Legen Sie fest, dass dieses Projekt in Visual Studio ausgeführt wird, und konfigurieren Sie das Thread Modell:

    1.  Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf das Projekt guistep \_ 2, und wählen Sie als Startprojekt festlegen aus.
    2.  Klicken Sie erneut mit der rechten Maustaste, und wählen Sie Eigenschaften aus.
    3.  Im Dialogfeld Eigenschaften Seiten des Projekts:

        1.  Legen Sie in der Dropdown-Dropdown-Dropdown-Datei die Konfiguration auf alle Konfigurationen fest
        2.  Erweitern Sie unter Konfigurations Eigenschaften die Option C/C++, wählen Sie Code Generierung aus, und legen Sie Lauf Zeit Bibliothek: Multithread Debuggen (/MTD) fest.

3.  Ersetzen Sie den Inhalt von guistep \_ 2. cpp durch den folgenden Code:
    ```C++
    // GuiStep_2.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_2.h"
    #include <strsafe.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now sets the appropriate fallback list
        DWORD langCount = 0;
        // next commented out line of code could be used on Windows 7 and later
        // using SetProcessPreferredUILanguages is recomended for new applications (esp. multi-threaded applications)
    //    if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        // the following line of code is supported on Windows Vista and later
        if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to set the user defined languages, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // NOTES on step #1:
        // an application developer that makes the assumption the fallback list provided by the
        // system / OS is entirely sufficient may or may not be making a good assumption based 
        // mostly on:
        // A. your choice of languages installed with your application
        // B. the languages on the OS at application install time
        // C. the OS users propensity to install/uninstall language packs
        // D. the OS users propensity to change laguage settings

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) && 
                    IsValidLocaleName(next))
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  Erstellen Sie eine Unicode-Textdatei langs.txt mit der folgenden Zeile:

    ``` syntax
    hi-IN ta-IN ru-RU fr-FR es-ES en-US
    ```

    > [!Note]  
    > Stellen Sie sicher, dass Sie die Datei als Unicode speichern.

     

    Kopieren Sie langs.txt in das Verzeichnis, in dem das Programm ausgeführt wird:

    -   Wenn Sie in Visual Studio ausführen, kopieren Sie Sie in *projectrootdirectory* \\ hellomui \\ guistep \_ 2.
    -   Wenn Sie den Windows-Explorer ausführen, kopieren Sie ihn in dasselbe Verzeichnis wie die guistep- \_2.exe.

5.  Erstellen Sie das Projekt, und führen Sie es aus. Bearbeiten Sie langs.txt, damit unterschiedliche Sprachen am Anfang der Liste angezeigt werden.

## <a name="step-5-customizing-hello-mui"></a>Schritt 5: Anpassen von "Hello MUI"

Eine Reihe von Lauf Zeit Features, die bisher in diesem Tutorial erwähnt wurden, sind nur unter Windows Vista und höher verfügbar. Möglicherweise möchten Sie den Aufwand für die Lokalisierung und Aufteilung von Ressourcen wieder verwenden, indem Sie die Anwendung auf Windows-Betriebssystemversionen unter Windows XP (Windows XP) anwenden. Dieser Prozess beinhaltet das Anpassen des vorherigen Beispiels in zwei wichtigen Bereichen:

-   Die Funktionen zum Laden von Ressourcen vor Windows Vista (z. b. [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)usw.) sind nicht MUI-fähig. Anwendungen, die mit Split-Ressourcen ausgeliefert werden (LN-und MUI-Dateien), müssen Ressourcen Module mithilfe einer dieser beiden Funktionen laden:

    -   Wenn die Anwendung nur unter Windows Vista und höher ausgeführt werden soll, sollte Sie Ressourcen Module mit [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)laden.
    -   Wenn die Anwendung auf Versionen vor Windows Vista und Windows Vista oder höher ausgeführt werden soll, muss Sie [**loadmuilibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)verwenden. dabei handelt es sich um eine bestimmte kompatible-Funktion, die im Windows 7 SDK bereitgestellt wird.

-   Die Unterstützung der sprach Verwaltung und der sprach Fall Back Reihenfolge, die in Versionen vor Windows Vista des Windows-Betriebssystems angeboten wird, unterscheidet sich deutlich von der in Windows Vista und höher. Aus diesem Grund müssen Anwendungen, die den Benutzer konfigurierten sprach Fall Back zulassen, die sprach Verwaltungsverfahren anpassen:

    -   Wenn die Anwendung nur unter Windows Vista und höher ausgeführt werden soll, ist das Festlegen der Sprachliste mithilfe von [**setthreadpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) ausreichend.
    -   Wenn die Anwendung unter allen Windows-Versionen ausgeführt werden soll, muss Code erstellt werden, der auf downlevelplattformen ausgeführt wird, um die Liste der Benutzer konfigurierten Sprachen zu durchlaufen und nach dem gewünschten Ressourcen Modul zu suchen. Dies ist in den Abschnitten 1C und 2 des Codes zu sehen, der später in diesem Schritt bereitgestellt wird.

Erstellen Sie ein Projekt, das die lokalisierten Ressourcen Module für jede Windows-Version verwenden kann:

1.  Fügen Sie der Projekt Mappe hellomui (mithilfe der Menü Auswahl Datei, hinzufügen und neues Projekt) ein neues Projekt mit den folgenden Einstellungen und Werten hinzu:

    1.  Projekttyp: Win32-Projekt.
    2.  Name: guistep \_ 3.
    3.  Speicherort: übernehmen Sie die Standardeinstellung.
    4.  Wählen Sie im Win32-Anwendungs-Assistenten den Standard Anwendungstyp: Windows-Anwendung aus.

2.  Legen Sie fest, dass dieses Projekt in Visual Studio ausgeführt wird, und konfigurieren Sie das Threading Modell. Konfigurieren Sie Sie außerdem so, dass die erforderlichen Header und Bibliotheken hinzugefügt werden.

    > [!Note]  
    > Bei den in diesem Tutorial verwendeten Pfaden wird davon ausgegangen, dass das Windows 7 SDK und das Microsoft nls-kompatible-APIs-Paket in ihren Standardverzeichnissen installiert wurden. Wenn dies nicht der Fall ist, ändern Sie die Pfade entsprechend.

     

    1.  Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf das Projekt, \_ und wählen Sie als Startprojekt festlegen aus.
    2.  Klicken Sie erneut mit der rechten Maustaste, und wählen Sie Eigenschaften aus.
    3.  Im Dialogfeld Eigenschaften Seiten des Projekts:

        1.  Legen Sie in der Dropdown-Dropdown-Dropdown-Datei die Konfiguration auf alle Konfigurationen fest
        2.  Erweitern Sie unter Konfigurations Eigenschaften die Option C/C++, wählen Sie Code Generierung aus, und legen Sie Lauf Zeit Bibliothek: Multithread Debuggen (/MTD) fest.
        3.  Wählen Sie Allgemein aus, und fügen Sie weitere Includeverzeichnisse hinzu:

            -   "C: \\ Microsoft nls-Downlevel-APIs \\ enthalten".

        4.  Wählen Sie Sprache aus, und legen Sie WCHAR \_ t als integrierten Typ: Nein (/Zc: WCHAR \_ t-) fest.
        5.  Wählen Sie erweitert aus, und legen Sie die Aufruf Konvention fest: \_ StdCall (/gz).
        6.  Erweitern Sie unter Konfigurations Eigenschaften die Option Linker, wählen Sie Eingabe aus, und fügen Sie zusätzliche Abhängigkeiten hinzu:

            -   "C: \\ Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ lib \\ muiload. lib".
            -   "C: \\ Microsoft nls-Downlevel-APIs \\ lib \\ x86 \\ nlsdl. lib".

3.  Ersetzen Sie den Inhalt von guistep \_ 3. cpp durch den folgenden Code:
    ```C++
    // GuiStep_3.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_3.h"
    #include <strsafe.h>
    #include <Nlsdl.h>
    #include <MUILoad.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now attempts to set the fallback list - this is much different for a down-level 
        // shipping application when compared to a Windows Vista or Windows 7 only shipping application    
        BOOL setSuccess = FALSE;
        DWORD setLangCount = 0;
        HMODULE hDLL = GetModuleHandleW(L"kernel32.dll");
        if( hDLL )
        {
            typedef BOOL (* SET_PREFERRED_UI_LANGUAGES_PROTOTYPE ) ( DWORD, PCWSTR, PULONG );
            SET_PREFERRED_UI_LANGUAGES_PROTOTYPE fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE)NULL;
            fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetProcessPreferredUILanguages");
            if( fp_SetPreferredUILanguages )
            {
                // call SetProcessPreferredUILanguages if it is available in Kernel32.dll's export table - Windows 7 and later
                setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
            else
            {
                fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetThreadPreferredUILanguages");
                // call SetThreadPreferredUILanguages if it is available in Kernel32.dll's export table - Windows Vista and later
                if(fp_SetPreferredUILanguages)
                    setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
        }

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module
        // LoadMUILibrary is the preferred alternative for loading of resource modules
        // when the application is potentially run on OS versions prior to Windows Vista
        // LoadMUILibrary is available via Windows SDK releases in Windows Vista and later
        // When available, it is advised to get the most up-to-date Windows SDK (e.g., Windows 7)
        HMODULE resContainer = NULL;
        if(setSuccess) // Windows Vista and later OS scenario
        {
            resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        else // this block should only be hit on Windows XP and earlier OS platforms as setSuccess will be TRUE on Windows Vista and later
        {
            // need to provide your own fallback mechanism such as the implementation below
            // in essence the application will iterate through the user configured language list
            WCHAR * next = userLanguagesMultiString;
            while(!resContainer && *next != L'\0')
            {
                // convert the language name to an appropriate LCID
                // DownlevelLocaleNameToLCID is available via standalone download package 
                // and is contained in Nlsdl.h / Nlsdl.lib
                LCID nextLcid = DownlevelLocaleNameToLCID(next,DOWNLEVEL_LOCALE_NAME);
                // then have LoadMUILibrary attempt to probe for the right .mui module
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,(LANGID)nextLcid);
                // increment to the next language name in our list
                size_t nextStrLen = 0;
                if(SUCCEEDED(StringCchLengthW(next,LOCALE_NAME_MAX_LENGTH,&nextStrLen)))
                    next += (nextStrLen + 1);
                else
                    break; // string is invalid - need to exit
            }
            // if the user configured list did not locate a module then try the languages associated with the system
            if(!resContainer)
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeMUILibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) 
                    && DownlevelLocaleNameToLCID(next,0) != 0)
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string 
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  Erstellen oder kopieren Sie langs.txt in das entsprechende Verzeichnis, wie zuvor in [Schritt 4: Globalisieren von "Hello MUI"](#step-4-globalizing-hello-mui)beschrieben.
5.  Erstellen Sie das Projekt, und führen Sie es aus.

> [!Note]  
> Wenn die Anwendung unter Windows-Versionen vor Windows Vista ausgeführt werden soll, lesen Sie unbedingt die Dokumente, die im Paket mit den [Microsoft nls-kompatible-APIs](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) für die Neuverteilung Nlsdl.dll.

 

## <a name="additional-considerations-for-mui"></a>Weitere Überlegungen zu MUI

### <a name="support-for-console-applications"></a>Unterstützung für Konsolen Anwendungen

Die in diesem Tutorial behandelten Verfahren können auch in Konsolen Anwendungen verwendet werden. Im Gegensatz zu den meisten standardmäßigen GUI-Steuerelementen können im Windows-Befehlsfenster jedoch keine Zeichen für alle Sprachen angezeigt werden. Aus diesem Grund erfordern mehrsprachige Konsolen Anwendungen besondere Aufmerksamkeit.

Das Aufrufen der APIs [**setthreaduilanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) oder [**setthreadpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) mit bestimmten Filterflags bewirkt, dass die Funktionen zum Laden von Ressourcen Sprachressourcen Tests für bestimmte Sprachen entfernen, die normalerweise nicht innerhalb eines Befehls Fensters angezeigt werden. Wenn diese Flags festgelegt sind, gestatten die sprach Einstellungs Algorithmen, dass nur die Sprachen, die im Befehlsfenster ordnungsgemäß angezeigt werden, in der Fall Back Liste angezeigt werden.

Weitere Informationen zum Erstellen einer mehrsprachigen Konsolenanwendung mithilfe dieser APIs finden Sie in den Hinweisen zu den Abschnitten [**setthreaduilanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) und [**setthreadpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).

### <a name="determination-of-languages-to-support-at-run-time"></a>Bestimmung der zu unterstützten Sprachen in Run-Time

Sie können einen der folgenden Entwurfsvorschläge anwenden, um zu bestimmen, welche Sprachen von Ihrer Anwendung zur Laufzeit unterstützt werden sollen:

-   **Aktivieren Sie den Endbenutzer während der Installation, um die bevorzugte Sprache aus einer Liste unterstützter Sprachen auszuwählen.**

-   **Lesen einer Sprachliste aus einer Konfigurationsdatei**

    Einige der Projekte in diesem Tutorial enthalten eine Funktion, die zum Analysieren einer langs.txt Konfigurationsdatei verwendet wird, die eine Sprachliste enthält.

    Da diese Funktion externe Eingaben annimmt, überprüfen Sie die Sprachen, die als Eingabe bereitgestellt werden. Weitere Informationen zum Durchführen dieser Überprüfung finden Sie in den Funktionen [**isvalidlocalename**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) oder [**downlevellocalenametolcid**](downlevellocalenametolcid.md) .

-   **Abfragen des Betriebssystems, um zu bestimmen, welche Sprachen installiert sind**

    Dieser Ansatz hilft der Anwendung, die gleiche Sprache wie das Betriebssystem zu verwenden. Obwohl dies keine Benutzer Aufforderung erfordert, müssen Sie, wenn Sie diese Option auswählen, beachten, dass Betriebssystemsprachen jederzeit hinzugefügt oder entfernt werden können und sich ändern können, nachdem der Benutzer die Anwendung installiert hat. Beachten Sie auch, dass in einigen Fällen das Betriebssystem mit eingeschränkter Sprachunterstützung installiert wird und die Anwendung mehr nutzen kann, wenn Sie Sprachen unterstützt, die vom Betriebssystem nicht unterstützt werden.

    Weitere Informationen zum Bestimmen der derzeit installierten Sprachen im Betriebssystem finden Sie unter der Funktion " [**enumuilanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) ".

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a>Unterstützung komplexer Skripts in Versionen vor Windows Vista

Wenn eine Anwendung, die bestimmte komplexe Skripts unterstützt, auf einer Windows-Version vor Windows Vista ausgeführt wird, wird der Text in diesem Skript in GUI-Komponenten möglicherweise nicht ordnungsgemäß angezeigt. Beispielsweise werden in diesem Lernprogramm im kompatible-Projekt möglicherweise in der MessageBox-und Ta-Skripts aufgrund von Problemen mit der Verarbeitung komplexer Skripts und dem Fehlen verwandter Schriftarten nicht in der MessageBox angezeigt. Normalerweise stellen Probleme dieser Art als quadratische Felder in der GUI-Komponente dar.

Weitere Informationen zum Aktivieren der komplexen Skript Verarbeitung finden Sie unter [Skript-und Schriftart Unterstützung in Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).

## <a name="summary"></a>Zusammenfassung

In diesem Tutorial wurde eine monolingual-Anwendung globalisiert, und es wurden die folgenden bewährten Methoden demonstriert.

-   Entwerfen Sie die Anwendung, um das Win32-Ressourcenmodell zu nutzen.
-   Verwenden Sie die MUI-Aufteilung von Ressourcen in Satelliten Binärdateien (MUI-Dateien).
-   Stellen Sie sicher, dass der Lokalisierungsprozess die Ressourcen in den MUI-Dateien so aktualisiert, dass Sie für die Zielsprache geeignet sind.
-   Stellen Sie sicher, dass die Paket Erstellung und die Bereitstellung der Anwendung, zugeordneten MUI-Dateien und Konfigurations Inhalte ordnungsgemäß durchgeführt werden, damit die Ressourcen, die APIs laden, den lokalisierten Inhalt finden.
-   Stellen Sie dem Endbenutzer einen Mechanismus bereit, um die Sprachkonfiguration der Anwendung anzupassen.
-   Passen Sie den Lauf Zeit Code so an, dass die Sprachkonfiguration genutzt wird, damit die Anwendung schneller auf die Anforderungen der Endbenutzer reagiert.

 

 
