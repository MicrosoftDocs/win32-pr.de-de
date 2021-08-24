---
description: In diesem Tutorial wird veranschaulicht, wie Sie eine einsprachige Anwendung nutzen und für die Welt bereit machen. Diese Anwendung hat die Form einer vollständigen Lösung, die in Microsoft Visual Studio erstellt wird.
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: Hinzufügen von mehrsprachige Benutzeroberfläche-Unterstützung zu einer Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5ca1ddba2574610cde1f375f7fab2b07461008665f2092c9c8e88ae9b51f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147693"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a>Hinzufügen von mehrsprachige Benutzeroberfläche-Unterstützung zu einer Anwendung

In diesem Tutorial wird veranschaulicht, wie Sie eine einsprachige Anwendung nutzen und für die Welt bereit machen. Diese Anwendung hat die Form einer vollständigen Lösung, die in Microsoft Visual Studio erstellt wird.

-   [Übersicht](#splitting-the-various-language-resource-modules-an-overview)
    -   [The Idea Behind Hello HELLO (Die Idee hinter Hello HELLO)](#the-idea-behind-hello-mui)
-   [Einrichten der Hello-PROJEKTMAPPE "HELLO"](#setting-up-the-hello-mui-solution)
    -   [Plattformanforderungen](#platform-requirements)
    -   [Voraussetzungen](#prerequisites)
-   [Schritt 0: Erstellen des hart codierten Hello-CODES](#step-0-creating-the-hard-coded-hello-mui)
-   [Schritt 1: Implementieren des Grundlegenden Ressourcenmoduls](#step-1-implementing-the-basic-resource-module)
-   [Schritt 2: Erstellen des Grundlegenden Ressourcenmoduls](#step-2-building-the-basic-resource-module)
    -   [Aufteilen der verschiedenen Sprachressourcenmodule: Eine Übersicht](#splitting-the-various-language-resource-modules-an-overview)
    -   [Aufteilen der verschiedenen Sprachressourcenmodule: Erstellen der Dateien](#splitting-the-various-language-resource-modules-creating-the-files)
-   [Schritt 3: Erstellen eines Resource-Savvy "Hello HELLO"](#step-3-creating-a-resource-savvy-hello-mui)
-   [Schritt 4: Globalisieren von "Hello HELLO"](#step-4-globalizing-hello-mui)
-   [Schritt 5: Anpassen von "Hello HELLO"](#step-5-customizing-hello-mui)
-   [Weitere Überlegungen zu DEN ÜBERLEGUNGEN](#additional-considerations-for-mui)
    -   [Unterstützung für Konsolenanwendungen](#support-for-console-applications)
    -   [Bestimmung der zur Laufzeit zu unterstützenden Sprachen](#determination-of-languages-to-support-at-run-time)
    -   [Unterstützung komplexer Skripts in Versionen vor Windows Vista](#complex-script-support-in-versions-prior-to-windows-vista)
-   [Zusammenfassung](#summary)

## <a name="overview"></a>Übersicht

Ab Windows Vista wurde das Windows Betriebssystem selbst von Grund auf als mehrsprachige Plattform entwickelt, mit zusätzlicher Unterstützung, mit der Sie mehrsprachige Anwendungen erstellen können, die das Windows RESOURCE Model VERWENDEN.

In diesem Tutorial wird diese neue Unterstützung für mehrsprachige Anwendungen anhand der folgenden Aspekte veranschaulicht:

-   Verwendet die verbesserte UNTERSTÜTZUNG für DIE PLATFORM, um mehrsprachige Anwendungen einfach zu aktivieren.
-   Erweitert mehrsprachige Anwendungen für die Ausführung auf Versionen von Windows vor Windows Vista.
-   Geht auf die zusätzlichen Aspekte ein, die bei der Entwicklung spezialisierter mehrsprachiger Anwendungen wie Konsolenanwendungen zu berücksichtigen sind.

Über diese Links erhalten Sie eine schnelle Aktualisierung der Konzepte zur Internationalisierung und zu DEN FOLGENDEN Themen:

-   [Kurze Übersicht über die Internationalisierung.](understanding-internationalization.md)
-   [CONCEPTS Concepts](understanding-mui.md).
-   [Verwenden von CSV zum Entwickeln von Win32-Anwendungen.](using-multilingual-user-interface.md)

### <a name="the-idea-behind-hello-mui"></a>The Idea Behind Hello HELLO (Die Idee hinter Hello HELLO)

Sie sind wahrscheinlich mit der klassischen Hallo Welt-Anwendung vertraut, die grundlegende Programmierkonzepte veranschaulicht. In diesem Tutorial wird ein ähnlicher Ansatz verwendet, um zu veranschaulichen, wie Sie mithilfe des RESSOURCENmodells VOM TYP AUS eine einsprachige Anwendung aktualisieren, um eine mehrsprachige Version namens Hello CSV zu erstellen.

> [!Note]  
> Die Aufgaben in diesem Tutorial werden aufgrund der Genauigkeit, mit der diese Aktivitäten ausgeführt werden müssen, in ausführlichen Schritten beschrieben und müssen Entwicklern, die wenig Erfahrung mit diesen Aufgaben haben, die Details erläutern.

 

## <a name="setting-up-the-hello-mui-solution"></a>Einrichten der Hello-PROJEKTMAPPE "HELLO"

In diesen Schritten wird beschrieben, wie Sie die Erstellung der Hello CSV-Lösung vorbereiten.

### <a name="platform-requirements"></a>Plattformanforderungen

Sie müssen die Codebeispiele in diesem Tutorial mit dem Windows Software Development Kit (SDK) für Windows 7 und Visual Studio 2008 kompilieren. Das Windows 7 SDK wird unter Windows XP, Windows Vista und Windows 7 installiert, und die Beispiellösung kann auf einer dieser Betriebssystemversionen erstellt werden.

Alle Codebeispiele in diesem Tutorial sind für die Ausführung auf x86- und x64-Versionen von Windows XP, Windows Vista und Windows 7 konzipiert. Bestimmte Teile, die auf Windows XP nicht funktionieren, werden nach Bedarf aufgerufen.

### <a name="prerequisites"></a>Voraussetzungen

1.  Installieren Sie Visual Studio 2008.

    Weitere Informationen finden Sie im [Visual Studio Developer Center.](https://msdn.microsoft.com/vstudio/default.aspx)

2.  Installieren Sie das Windows SDK für Windows 7.

    Sie können es auf der Seite Windows SDK des [Windows Developer Center](https://msdn.microsoft.com/windowsserver/bb980924.aspx)installieren. Das SDK enthält Hilfsprogramme zum Entwickeln von Anwendungen für Betriebssystemversionen, beginnend mit Windows XP bis zur neuesten Version.

    > [!Note]  
    > Notieren Sie sich den Installationspfad, wenn Sie das Paket nicht am Standardspeicherort installieren oder wenn Sie es nicht auf dem Systemlaufwerk installieren, bei dem es sich in der Regel um das Laufwerk C handelt.

     

3.  Konfigurieren Sie die Visual Studio Befehlszeilenparameter.

    1.  Öffnen Sie ein Visual Studio Befehlsfenster.
    2.  Geben Sie **den Pfad ein.**
    3.  Vergewissern Sie sich, dass die Path-Variable den Pfad des Ordners bin des Windows 7 SDK enthält: ... Microsoft SDKs \\ Windows \\ v7.0 \\ bin

4.  Installieren Sie das Downlevel-APIs-Add-On-Paket von Microsoft NLS.
    > [!Note]  
    > Im Rahmen dieses Tutorials ist dieses Paket nur erforderlich, wenn Sie die Anwendung so anpassen, dass sie auf Windows Versionen vor Windows Vista ausgeführt wird. Weitere Informationen finden Sie unter [Schritt 5: Anpassen von Hello HELLO.](#step-5-customizing-hello-mui)

     

    1.  Laden Sie das Paket von der Downloadwebsite herunter, und installieren [Sie es.](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en)
    2.  Notieren Sie sich wie beim Windows SDK den Installationspfad, wenn Sie das Paket nicht am Standardspeicherort installieren oder wenn Sie es nicht auf dem Systemlaufwerk installieren, bei dem es sich in der Regel um das Laufwerk C handelt.
    3.  Wenn Ihre Entwicklungsplattform Windows XP oder Windows Server 2003 ist, vergewissern Sie sich, dass Nlsdl.dll ordnungsgemäß installiert und registriert ist.

        1.  Navigieren Sie unter dem Installationspfad zum Ordner "redist".
        2.  Führen Sie die entsprechende verteilbare Nlsdl aus. \*.exe, z. B. nlsdl.x86.exe. In diesem Schritt werden Nlsdl.dll installiert und registriert.

    > [!Note]  
    > Wenn Sie eine Anwendung entwickeln, die DIE -Anwendung verwendet und auf Windows Versionen vor Windows Vista ausgeführt werden muss, müssen Nlsdl.dll auf der Zielplattform Windows vorhanden sein. In den meisten Fällen bedeutet dies, dass die Anwendung das verteilbare Nlsdl-Installationsprogramm tragen und installieren muss (und nicht nur Nlsdl.dll selbst kopieren).

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a>Schritt 0: Erstellen des hart codierten Hello-CODES

Dieses Tutorial beginnt mit der einsprachigen Version der Hello-ANWENDUNG "HELLO". Die Anwendung geht davon aus, dass die Programmiersprache C++, Breitzeichenfolgen und die [**MessageBoxW-Funktion**](/windows/win32/api/winuser/nf-winuser-messagebox) für die Ausgabe verwendet werden.

Erstellen Sie zunächst die anfängliche GuiStep \_ 0-Anwendung sowie die HelloMUI-Lösung, die alle Anwendungen in diesem Tutorial enthält.

1.  Erstellen Sie in Visual Studio 2008 ein neues Projekt. Verwenden Sie die folgenden Einstellungen und Werte:

    1.  Project Typ: Wählen Sie unter Visual C++ Win32 und dann unter Visual Studio installierte Vorlagen win32 Project aus.
    2.  Name: GuiStep \_ 0.
    3.  Speicherort: *ProjectRootDirectory* (Spätere Schritte verweisen auf dieses Verzeichnis).
    4.  Projektmappenname: HelloMUI.
    5.  Aktivieren Sie Projektmappenverzeichnis erstellen.
    6.  Wählen Sie im Win32-Anwendungs-Assistenten den Standardanwendungstyp aus: Windows Anwendung.

2.  Konfigurieren Sie das Projektthreadingmodell:

    1.  Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf das Projekt GuiStep \_ 0, und wählen Sie eigenschaften aus.
    2.  Im Dialogfeld Eigenschaftenseiten des Projekts:

        1.  Legen Sie in der dropdown linken oberen Dropdown-Seite Konfiguration auf Alle Konfigurationen fest.
        2.  Erweitern Sie unter Konfigurationseigenschaften die Option C/C++, wählen Sie Codegenerierung aus, und legen Sie Laufzeitbibliothek: Multithreaddebuggen (/MTd) fest.

3.  Ersetzen Sie den Inhalt von GuiStep \_ 0.cpp durch den folgenden Code:
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

Durch den einfachen Quellcode oben wird die einfache Entwurfsauswahl für die hartcodierende oder einbettende Ausgabe getroffen, die dem Benutzer angezeigt wird– in diesem Fall der Text "Hello USERNAME". Diese Auswahl schränkt das Hilfsprogramm der Anwendung für Benutzer ein, die das englische Wort "Hello" nicht erkennen. Da es sich bei DEM UME um ein technologiebasiertes englisches Akronym handelt, wird für dieses Tutorial davon ausgegangen, dass die Zeichenfolge für alle Sprachen "CSV" bleibt.

## <a name="step-1-implementing-the-basic-resource-module"></a>Schritt 1: Implementieren des Grundlegenden Ressourcenmoduls

Microsoft Win32 bietet Anwendungsentwicklern seit langem die Möglichkeit, ihre Benutzeroberflächenressourcendaten vom Anwendungsquellcode zu trennen. Diese Trennung erfolgt in Form des Win32-Ressourcenmodells, in dem Zeichenfolgen, Bitmaps, Symbole, Nachrichten und andere Elemente, die normalerweise einem Benutzer angezeigt werden, in einen separaten Abschnitt der ausführbaren Datei gepackt werden, getrennt von ausführbarem Code.

Um diese Trennung zwischen ausführbarem Code und der Paketierung von Ressourcendaten zu veranschaulichen, platziert das Tutorial in diesem Schritt die zuvor hart codierte "Hello"-Zeichenfolge (die Ressource "en-US") in den Ressourcenabschnitt eines DLL-Moduls im Projekt HelloModule \_ en \_ us.

Diese Win32-DLL kann auch ausführbare Funktionen des Bibliothekstyps enthalten (wie jede andere DLL). Um sich jedoch auf die win32-ressourcenbezogenen Aspekte zu konzentrieren, lassen wir den Laufzeit-DLL-Code in dllmain.cpp stubbed. In den nachfolgenden Abschnitten dieses Tutorials werden die helloModule-Ressourcendaten verwendet, die hier erstellt werden, und es wird auch entsprechender Laufzeitcode angezeigt.

Um ein Win32-Ressourcenmodul zu erstellen, erstellen Sie zunächst eine DLL mit einem ausgestupften DLL-Code:

1.  Fügen Sie der HelloMUI-Projektmappe ein neues Projekt hinzu:

    1.  Wählen Sie im Menü Datei die Option Hinzufügen und dann Neu Project aus.
    2.  Project Typ: Win32 Project.
    3.  Name: HelloModule \_ en \_ us.
    4.  Speicherort: *ProjectRootDirectory* \\ HelloMUI.
    5.  Wählen Sie im Win32-Anwendungs-Assistenten anwendungstyp: DLL aus.

2.  Konfigurieren Sie das Threadingmodell dieses Projekts:

    1.  Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf das Projekt HelloModule \_ \_ en us, und wählen Sie Eigenschaften aus.
    2.  Im Dialogfeld Eigenschaftenseiten des Projekts:

        1.  Legen Sie in der dropdown linken oberen Dropdown-Seite Konfiguration auf Alle Konfigurationen fest.
        2.  Erweitern Sie unter Konfigurationseigenschaften die Option C/C++, wählen Sie Codegenerierung aus, und legen Sie Laufzeitbibliothek: Multithreaddebuggen (/MTd) fest.

3.  Untersuchen Sie dllmain.cpp. (Möglicherweise möchten Sie UNREFERENCED \_ hinzufügen. PARAMETER-Makros für den generierten Code, wie hier, um die Kompilierung auf Warnstufe 4 zu ermöglichen.)
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

    

4.  Fügen Sie dem Projekt die Ressourcendefinitionsdatei HelloModule.rc hinzu:

    1.  Klicken Sie unter dem Projekt HelloModule en us mit \_ der rechten Maustaste auf den Ordner \_ Ressourcendateien, und wählen Sie Hinzufügen und dann Neues Element aus.
    2.  Wählen Sie im Dialogfeld Neues Element hinzufügen Folgendes aus:

        1.  Kategorien: Wählen Sie unter Visual C++ Ressource und dann unter "Visual Studio installierte Vorlagen" die Option Ressourcendatei (RC) aus.
        2.  Name: HelloModule.
        3.  Speicherort: Übernehmen Sie die Standardeinstellung.
        4.  Klicken Sie auf Hinzufügen.

    3.  Geben Sie an, dass die neue Datei HelloModule.rc als Unicode gespeichert werden soll:

        1.  Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf HelloModule.rc, und wählen Sie Code anzeigen aus.
        2.  Wenn eine Meldung mit dem Hinweis angezeigt wird, dass die Datei bereits geöffnet ist, und Sie gefragt werden, ob Sie sie schließen möchten, klicken Sie auf Ja.
        3.  Wenn die Datei als Text angezeigt wird, wählen Sie im Menü Datei und dann Erweiterte Speicheroptionen aus.
        4.  Geben Sie unter Codierung unicode – Codepage 1200 an.
        5.  Klicken Sie auf OK.
        6.  Speichern und schließen Sie HelloModule.rc.

    4.  Fügen Sie eine Zeichenfolgentabelle mit der Zeichenfolge "Hello" hinzu:

        1.  Klicken Sie im Ressourcenansicht mit der rechten Maustaste auf HelloModule.rc, und wählen Sie Ressource hinzufügen aus.
        2.  Wählen Sie Zeichenfolgentabelle aus.
        3.  Klicken Sie auf Neu.
        4.  Fügen Sie der Zeichenfolgentabelle eine Zeichenfolge hinzu:

            1.  ID: HELLO \_ HELLO HELLO \_ STR \_ 0.
            2.  Wert: 0.
            3.  Beschriftung: Hello.

        Wenn Sie HelloModule.rc jetzt als Text anzeigen, werden verschiedene Teile des ressourcenspezifischen Quellcodes angezeigt. Am wichtigsten ist der Abschnitt, in dem die Zeichenfolge "Hello" beschrieben wird:

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

        

        Diese "Hello"-Zeichenfolge ist die Ressource, die in jede Sprache lokalisiert (d. h. übersetzt) werden muss, die die Anwendung unterstützen möchte. Der HelloModule \_ ta \_ in-Projekt (den Sie im nächsten Schritt erstellen) enthält beispielsweise eine eigene lokalisierte Version von HelloModule.rc für "ta-IN":

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

        

    5.  Erstellen Sie das Projekt HelloModule \_ en \_ us, um sicherzustellen, dass keine Fehler auftreten.

5.  Erstellen Sie sechs weitere Projekte in der HelloMUI-Projektmappe (oder so viele davon, wie Sie möchten), um sechs weitere Ressourcen-DLLs für zusätzliche Sprachen zu erstellen. Verwenden Sie die Werte in dieser Tabelle:

    | Projektname        | Name der RC-Datei | Zeichenfolgen-ID          | Zeichenfolgenwert | Zeichenfolgenbeschriftung |
    |---------------------|------------------|--------------------|--------------|----------------|
    | HelloModule \_ \_ de de | HelloModule      | HELLO \_ HELLO HELLO STR \_ \_ 0 | 0            | Hallo          |
    | HelloModule \_ \_ es es | HelloModule      | HELLO \_ HELLO HELLO STR \_ \_ 0 | 0            | Hola           |
    | HelloModule \_ fr \_ fr | HelloModule      | HELLO \_ HELLO HELLO STR \_ \_ 0 | 0            | Bonjour        |
    | HelloModule \_ hi \_ in | HelloModule      | HELLO \_ HELLO HELLO STR \_ \_ 0 | 0            | नमस्           |
    | HelloModule \_ ru \_ ru | HelloModule      | HELLO \_ HELLO HELLO STR \_ \_ 0 | 0            | Здравствуйте   |
    | HelloModule \_ ta \_ in | HelloModule      | HELLO \_ HELLO HELLO STR \_ \_ 0 | 0            | வணக்கம்        |

    

     

Weitere Informationen zur RC-Dateistruktur und -Syntax finden Sie unter [Informationen zu Ressourcendateien.](../menurc/about-resource-files.md)

## <a name="step-2-building-the-basic-resource-module"></a>Schritt 2: Erstellen des Grundlegenden Ressourcenmoduls

Bei Verwendung vorheriger Ressourcenmodelle würde die Erstellung eines der sieben HelloModule-Projekte zu sieben separaten DLLs führen. Jede DLL würde einen Ressourcenabschnitt mit einer einzelnen Zeichenfolge enthalten, die in der entsprechenden Sprache lokalisiert ist. Obwohl es für das historische Win32-Ressourcenmodell geeignet ist, nutzt dieser Entwurf nicht DIE Vorteile von CSV.

Im Windows Vista SDK und höher bietet DIE MÖGLICHKEIT, ausführbare Dateien in Quellcode und lokalisierbare Inhaltsmodule aufzuteilen. Mit der zusätzlichen Anpassung, die weiter unten in Schritt 5 behandelt wird, können Anwendungen für mehrsprachige Unterstützung aktiviert werden, um auf Versionen vor Windows Vista ausgeführt zu werden.

Die wichtigsten Verfügbaren Mechanismen zum Aufteilen von Ressourcen aus ausführbarem Code, beginnend mit Windows Vista, sind:

-   Verwenden von rc.exe (RC-Compiler) mit bestimmten Schaltern oder
-   Verwenden eines Tools für die Stilaufteilung nach dem Build mit dem Namen muirct.exe.

Weitere Informationen finden Sie unter [Ressourcenprogramme.](resource-utilities.md)

Der Einfachheit halber wird in diesem Tutorial muirct.exe verwendet, um die ausführbare Datei "Hello CSV" aufzuteilen.

### <a name="splitting-the-various-language-resource-modules-an-overview"></a>Aufteilen der verschiedenen Sprachressourcenmodule: Eine Übersicht

Ein mehrteiliges Verfahren ist an der Aufteilung der DLLs in eine ausführbare HelloModule.dll sowie an einer HelloModule.dll.msi für jede der sieben unterstützten Sprachen in diesem Tutorial beteiligt. In dieser Übersicht werden die erforderlichen Schritte beschrieben. Der nächste Abschnitt enthält eine Befehlsdatei, die diese Schritte ausführt.

Teilen Sie zunächst das modul "English-only HelloModule.dll" mit dem Befehl auf:


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



In der obigen Befehlszeile wird die Konfigurationsdatei DoReverseMuiLoc.rcconfig verwendet. Diese Art von Konfigurationsdatei wird in der Regel von muirct.exe verwendet, um Ressourcen zwischen der sprachneutralen DLL (LN) und den sprachabhängigen DATEIEN ZU teilen. In diesem Fall gibt die XML-Datei DoReverseMuiLoc.rcconfig (im nächsten Abschnitt aufgeführt) viele Ressourcentypen an, aber sie fallen alle in die Dateikategorie "localizedResources" oder .js, und es gibt keine Ressourcen in der sprachneutralen Kategorie. Weitere Informationen zum Vorbereiten einer Ressourcenkonfigurationsdatei finden Sie unter [Vorbereiten einer Ressourcenkonfigurationsdatei.](preparing-a-resource-configuration-file.md)

Zusätzlich zum Erstellen einer datei "HelloModule.dll.strings", die die englische Zeichenfolge "Hello" enthält, bettet muirct.exe während der Aufteilung auch eine RESSOURCE vom Typ "TAGGED" in das HelloModule.dll-Modul ein. Damit die entsprechenden Ressourcen aus den sprachspezifischen modulen HelloModule.dll.modules zur Laufzeit ordnungsgemäß geladen werden können, muss für jede DATEI der ERWEITERUNGsdatei eine feste Prüfsumme festgelegt sein, damit sie mit den Prüfsummen im sprachneutralen LN-Modul der Baseline übereinstimmt. Dies erfolgt mit einem Befehl wie dem folgenden:


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



Ebenso wird muirct.exe aufgerufen, um eine HelloModule.dll.msi-Datei für jede der anderen Sprachen zu erstellen. In diesen Fällen wird die sprachneutrale DLL jedoch verworfen, da nur die erste erstellte DLL benötigt wird. Die Befehle, die die spanischen und französischen Ressourcen verarbeiten, sehen wie folgt aus:


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



Eines der wichtigsten Zu beachtenden In den obigen muirct.exe befehlszeilen ist, dass das Flag -x verwendet wird, um eine Zielsprach-ID anzugeben. Der wert, der für muirct.exe bereitgestellt wird, ist für jedes sprachspezifische Modul HelloModule.dll unterschiedlich. Dieser Sprachwert ist von zentraler Bedeutung und wird von muirct.exe verwendet, um die DATEI BEIM Teilen entsprechend zu markieren. Ein falscher Wert führt zur Laufzeit zu Fehlern beim Laden von Ressourcen für diese bestimmte DATEI VOMO. Weitere [Informationen zum Zuordnen des Sprachnamens](language-identifier-constants-and-strings.md) zur LCID finden Sie unter Sprachbezeichnerkonstatoren und Zeichenfolgen.

Jede geteilte DATEI wird schließlich in einem Verzeichnis platziert, das ihrem Sprachnamen entspricht, direkt unter dem Verzeichnis, in dem sich die sprachneutrale Datei HelloModule.dll befindet. Weitere Informationen zur Platzierung der DATEI ".dateityp" finden Sie unter [Anwendungsbereitstellung.](application-deployment.md)

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a>Aufteilen der verschiedenen Sprachressourcenmodule: Erstellen der Dateien

In diesem Tutorial erstellen Sie eine Befehlsdatei, die die Befehle zum Aufteilen der verschiedenen DLLs enthält, und rufen sie manuell auf. Beachten Sie, dass Sie bei der eigentlichen Entwicklung das Potenzial für Buildfehler verringern können, indem Sie diese Befehle als Prä- oder Post-Buildereignisse in die HelloMUI-Projektmappe einreihen. Dies geht jedoch über den Rahmen dieses Tutorials hinaus.

Erstellen Sie die Dateien für den Debugbuild:

1.  Erstellen Sie eine Befehlsdatei DoReverseMuiLoc.cmd, die die folgenden Befehle enthält:
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

    

2.  Erstellen Sie eine XML-Datei DoReverseMuiLoc.rcconfig, die die folgenden Zeilen enthält:
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

    

3.  Kopieren Sie DoReverseMuiLoc.cmd und DoReverseMuiLoc.rcconfig in *ProjectRootDirectory* \\ HelloMUI \\ Debug.
4.  Öffnen Sie die Visual Studio 2008-Eingabeaufforderung, und navigieren Sie zum Verzeichnis Debuggen.
5.  Führen Sie DoReverseMuiLoc.cmd aus.

Wenn Sie einen Release-Build erstellen, kopieren Sie die gleichen Dateien DoReverseMuiLoc.cmd und DoReverseMuiLoc.rcconfig in das Verzeichnis Release und führen dort die Befehlsdatei aus.

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a>Schritt 3: Erstellen eines Resource-Savvy "Hello HELLO"

Auf der Grundlage des oben genannten hart codierten GuiStep0.exe beispiels, können Sie die Reichweite der Anwendung auf mehrere Sprachbenutzer erweitern, indem Sie das \_ Win32-Ressourcenmodell integrieren. Der in diesem Schritt vorgestellte neue Laufzeitcode enthält die Logik zum Laden des Moduls ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) und zum Abrufen von Zeichenfolgen ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)).

1.  Fügen Sie der HelloMUI-Projektmappe (mithilfe der Menüauswahl Datei, Hinzufügen und Neuer Project) ein neues Projekt mit den folgenden Einstellungen und Werten hinzu:

    1.  Project: Win32-Project.
    2.  Name: GuiStep \_ 1.
    3.  Speicherort: Übernehmen Sie die Standardeinstellung.
    4.  Wählen Sie im Win32-Anwendungs-Assistenten den Standardanwendungstyp aus: Windows Anwendung.

2.  Legen Sie dieses Projekt so fest, dass es in Visual Studio ausgeführt wird, und konfigurieren Sie das Threadingmodell:

    1.  Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf das Projekt GuiStep 1, und wählen \_ Sie Als Start festlegen Project.
    2.  Klicken Sie erneut mit der rechten Maustaste darauf, und wählen Sie Eigenschaften aus.
    3.  Führen Sie im Dialogfeld Eigenschaftenseiten des Projekts Die folgenden Optionen aus:

        1.  Legen Sie in der Dropdownliste oben links Die Konfiguration auf Alle Konfigurationen fest.
        2.  Erweitern Sie unter Konfigurationseigenschaften die Option C/C++, wählen Sie Codegenerierung aus, und legen Sie Laufzeitbibliothek: Multithreaddebuggen (/MTd) fest.

3.  Ersetzen Sie den Inhalt von GuiStep \_ 1.cpp durch den folgenden Code:
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

    

4.  Erstellen Sie die Anwendung, und führen Sie sie aus. Die Ausgabe wird in der Sprache angezeigt, die derzeit als Anzeigesprache des Computers festgelegt ist (vorausgesetzt, es handelt sich um eine der sieben Sprachen, die wir erstellt haben).

## <a name="step-4-globalizing-hello-mui"></a>Schritt 4: Globalisieren von "Hello HELLO"

Obwohl im vorherigen Beispiel die Ausgabe in verschiedenen Sprachen angezeigt werden kann, ist sie in einer Reihe von Bereichen nicht verfügbar. Am deutlichsten ist vielleicht, dass die Anwendung nur in einer kleinen Teilmenge von Sprachen verfügbar ist, wenn sie mit dem Windows Betriebssystem selbst verglichen wird. Wenn z. B. die GuiStep 1-Anwendung aus dem vorherigen Schritt auf einem japanischen Build von Windows installiert wurde, sind Fehler beim \_ Ressourcenspeicherort wahrscheinlich.

Um dieser Situation zu helfen, haben Sie zwei primäre Optionen:

-   Stellen Sie sicher, dass Ressourcen in einer vordefinierten endgültigen Fallbacksprache enthalten sind.
-   Bieten Sie dem Endbenutzer eine Möglichkeit, seine Spracheinstellungen aus einer Teilmenge von Sprachen zu konfigurieren, die speziell von der Anwendung unterstützt werden.

Von diesen Optionen ist die Option, die eine endgültige Fallbacksprache bietet, dringend zu empfehlen und wird in diesem Tutorial implementiert, indem das Flag -g an muirct.exe übergeben wird, wie oben gezeigt. Dieses Flag weist muirct.exe an, eine bestimmte Sprache (de-DE/0x0407) zur endgültigen Fallbacksprache zu machen, die dem sprachneutralen DLL-Modul (HelloModule.dll) zugeordnet ist. Zur Laufzeit wird dieser Parameter als letztes Mittel verwendet, um Text zu generieren, der dem Benutzer angezeigt wird. Wenn keine endgültige Fallbacksprache gefunden wird und keine entsprechende Ressource in der sprachneutralen Binärdatei verfügbar ist, schlägt das Laden der Ressource fehl. Daher sollten Sie sorgfältig die Szenarien ermitteln, auf die Ihre Anwendung stoßen kann, und die endgültige Fallbacksprache entsprechend planen.

Die andere Möglichkeit, konfigurierbare Spracheinstellungen zu ermöglichen und Ressourcen basierend auf dieser benutzerdefinierten Hierarchie zu laden, kann die Kundenzufriedenheit deutlich steigern. Leider erschwert dies auch die funktionalität, die in der Anwendung erforderlich ist.

In diesem Schritt des Tutorials wird ein vereinfachter Mechanismus für Textdateien verwendet, um die Konfiguration der benutzerdefinierten Benutzersprache zu aktivieren. Die Textdatei wird zur Laufzeit von der Anwendung analysiert, und die analysierte und überprüfte Sprachliste wird verwendet, um eine benutzerdefinierte Fallbackliste zu erstellen. Nachdem die benutzerdefinierte Fallbackliste eingerichtet wurde, laden die Windows-APIs Ressourcen entsprechend der in dieser Liste festgelegten Sprach rangfolge. Der Rest des Codes ähnelt dem im vorherigen Schritt gefundenen Code.

1.  Fügen Sie der HelloMUI-Projektmappe (mithilfe der Menüauswahl Datei, Hinzufügen und Neuer Project) ein neues Projekt mit den folgenden Einstellungen und Werten hinzu:

    1.  Project: Win32-Project.
    2.  Name: GuiStep \_ 2.
    3.  Speicherort: Übernehmen Sie die Standardeinstellung.
    4.  Wählen Sie im Win32-Anwendungs-Assistenten den Standardanwendungstyp aus: Windows Anwendung.

2.  Legen Sie dieses Projekt so fest, dass es in Visual Studio ausgeführt wird, und konfigurieren Sie das Threadingmodell:

    1.  Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf das Projekt GuiStep 2, und wählen \_ Sie Als Start festlegen Project.
    2.  Klicken Sie erneut mit der rechten Maustaste darauf, und wählen Sie Eigenschaften aus.
    3.  Führen Sie im Dialogfeld Eigenschaftenseiten des Projekts Die folgenden Optionen aus:

        1.  Legen Sie in der Dropdownliste oben links Die Konfiguration auf Alle Konfigurationen fest.
        2.  Erweitern Sie unter Konfigurationseigenschaften die Option C/C++, wählen Sie Codegenerierung aus, und legen Sie Laufzeitbibliothek: Multithreaddebuggen (/MTd) fest.

3.  Ersetzen Sie den Inhalt von GuiStep \_ 2.cpp durch den folgenden Code:
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

    

4.  Erstellen Sie eine Unicode-Textdateilangs.txt die die folgende Zeile enthält:

    ``` syntax
    hi-IN ta-IN ru-RU fr-FR es-ES en-US
    ```

    > [!Note]  
    > Achten Sie darauf, dass Sie die Datei als Unicode speichern.

     

    Kopieren langs.txt in das Verzeichnis, aus dem das Programm ausgeführt wird:

    -   Wenn die Ausführung innerhalb Visual Studio, kopieren Sie sie in *ProjectRootDirectory* \\ HelloMUI \\ GuiStep \_ 2.
    -   Wenn sie über Windows Explorer ausgeführt wird, kopieren Sie sie in dasselbe Verzeichnis wie GuiStep \_2.exe.

5.  Erstellen Sie das Projekt, und führen Sie es aus. Versuchen Sie, langs.txt so zu bearbeiten, dass am Anfang der Liste verschiedene Sprachen angezeigt werden.

## <a name="step-5-customizing-hello-mui"></a>Schritt 5: Anpassen von "Hello HELLO"

Einige der bisher in diesem Tutorial erwähnten Laufzeitfeatures sind nur auf Windows Vista und höher verfügbar. Möglicherweise möchten Sie den Aufwand, der in die Lokalisierung und Aufteilung von Ressourcen investiert wurde, wiederverarbeiten, indem Sie die Anwendung auf downlevelbasierten Windows Betriebssystemversionen wie Windows XP verwenden. Dieser Prozess umfasst die Anpassung des vorherigen Beispiels in zwei Hauptbereichen:

-   Die Vor-Windows Vista-Funktionen zum Laden von Ressourcen (z. B. [**LoadString,**](/windows/win32/api/winuser/nf-winuser-loadstringa) [**LoadIcon,**](/windows/win32/api/winuser/nf-winuser-loadicona) [**LoadBitmap,**](/windows/win32/api/winuser/nf-winuser-loadbitmapa) [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)und andere) sind nicht ÜBER EINE-Funktion kompatibel. Anwendungen, die mit geteilten Ressourcen (LN- und SOLLEN-Dateien) ausgestattet sind, müssen Ressourcenmodule mithilfe einer dieser beiden Funktionen laden:

    -   Wenn die Anwendung nur unter Windows Vista und höher ausgeführt werden soll, sollten Ressourcenmodule mit [**LoadLibraryEx geladen werden.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)
    -   Wenn die Anwendung in Versionen vor Windows Vista sowie Windows Vista oder höher ausgeführt werden soll, muss [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)verwendet werden. Dabei handelt es sich um eine bestimmte downlevel-Funktion, die im Windows 7 SDK bereitgestellt wird.

-   Die Unterstützung der Sprachverwaltung und der Fallback-Reihenfolge, die in Versionen vor Windows Vista des Windows-Betriebssystems angeboten wird, unterscheidet sich erheblich von der Unterstützung in Windows Vista und höher. Aus diesem Grund müssen Anwendungen, die vom Benutzer konfigurierte Sprachfallbacks zulassen, ihre Sprachverwaltungsmethoden anpassen:

    -   Wenn die Anwendung nur unter Windows Vista und höher ausgeführt werden soll, ist das Festlegen der Sprachliste mit [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) ausreichend.
    -   Wenn die Anwendung auf allen Windows-Versionen ausgeführt werden soll, muss Code erstellt werden, der auf downlevel-Plattformen ausgeführt wird, um die vom Benutzer konfigurierte Sprachliste zu iterieren und das gewünschte Ressourcenmodul zu prüfen. Dies ist in den Abschnitten 1c und 2 des Codes zu sehen, der später in diesem Schritt bereitgestellt wird.

Erstellen Sie ein Projekt, das die lokalisierten Ressourcenmodule in einer beliebigen Version von Windows:

1.  Fügen Sie der HelloMUI-Projektmappe (mithilfe der Menüauswahl Datei, Hinzufügen und Neuer Project) ein neues Projekt mit den folgenden Einstellungen und Werten hinzu:

    1.  Project: Win32-Project.
    2.  Name: GuiStep \_ 3.
    3.  Speicherort: Übernehmen Sie die Standardeinstellung.
    4.  Wählen Sie im Win32-Anwendungs-Assistenten den Standardanwendungstyp aus: Windows Anwendung.

2.  Legen Sie dieses Projekt so fest, dass es innerhalb Visual Studio ausgeführt wird, und konfigurieren Sie das Threadingmodell. Konfigurieren Sie sie außerdem so, dass die erforderlichen Header und Bibliotheken hinzugefügt werden.

    > [!Note]  
    > Bei den in diesem Tutorial verwendeten Pfaden wird davon ausgegangen, dass das Windows 7 SDK und das Downlevel-APIs-Paket von Microsoft NLS in ihren Standardverzeichnissen installiert wurden. Wenn dies nicht der Fall ist, ändern Sie die Pfade entsprechend.

     

    1.  Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf das Projekt GuiStep 3, und wählen \_ Sie Als Start festlegen Project.
    2.  Klicken Sie erneut mit der rechten Maustaste darauf, und wählen Sie Eigenschaften aus.
    3.  Führen Sie im Dialogfeld Eigenschaftenseiten des Projekts Die folgenden Optionen aus:

        1.  Legen Sie in der Dropdownliste oben links Die Konfiguration auf Alle Konfigurationen fest.
        2.  Erweitern Sie unter Konfigurationseigenschaften die Option C/C++, wählen Sie Codegenerierung aus, und legen Sie Laufzeitbibliothek: Multithreaddebuggen (/MTd) fest.
        3.  Wählen Sie Allgemein aus, und fügen Sie zusätzliche Includeverzeichnisse hinzu:

            -   "C: \\ Microsoft NLS Downlevel APIs \\ Include".

        4.  Wählen Sie Sprache aus, und legen Sie WCHAR \_ T als integrierten Typ behandeln fest: Nein (/Zc:wchar \_ t-).
        5.  Wählen Sie Erweitert aus, und legen Sie Aufrufkonvention: \_ stdcall (/Gz) fest.
        6.  Erweitern Sie unter Konfigurationseigenschaften den Linker, wählen Sie Eingabe aus, und fügen Sie zu Zusätzliche Abhängigkeiten hinzu:

            -   "C: \\ Programme \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Lib \\ CSVLoad.lib".
            -   "C: \\ Microsoft NLS Downlevel APIs \\ Lib \\ x86 \\ Nlsdl.lib".

3.  Ersetzen Sie den Inhalt von GuiStep \_ 3.cpp durch den folgenden Code:
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

    

4.  Erstellen oder kopieren Sie langs.txt in das entsprechende Verzeichnis, wie zuvor in [Schritt 4: Globalisieren von "Hello HELLO"](#step-4-globalizing-hello-mui)beschrieben.
5.  Erstellen Sie das Projekt, und führen Sie es aus.

> [!Note]  
> Wenn die Anwendung auf Windows Versionen vor Windows Vista ausgeführt werden soll, lesen Sie unbedingt die Dokumente, die im [Downlevel-APIs-Paket](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) von Microsoft NLS enthalten sind, um Nlsdl.dll neu zu verteilen.

 

## <a name="additional-considerations-for-mui"></a>Weitere Überlegungen zu DEN ÜBERLEGUNGEN

### <a name="support-for-console-applications"></a>Unterstützung für Konsolenanwendungen

Die in diesem Tutorial behandelten Techniken können auch in Konsolenanwendungen verwendet werden. Im Gegensatz zu den meisten Standard-GUI-Steuerelementen kann das Windows Befehlsfenster jedoch keine Zeichen für alle Sprachen anzeigen. Aus diesem Grund erfordern mehrsprachige Konsolenanwendungen besondere Aufmerksamkeit.

Das Aufrufen der APIs [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) oder [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) mit bestimmten Filterflags bewirkt, dass die Funktionen zum Laden von Ressourcen Sprachressourcentest für bestimmte Sprachen entfernen, die normalerweise nicht in einem Befehlsfenster angezeigt werden. Wenn diese Flags festgelegt sind, lassen die Spracheinstellungsalgorithmen nur die Sprachen zu, die im Befehlsfenster ordnungsgemäß in der Fallbackliste angezeigt werden.

Weitere Informationen zur Verwendung dieser APIs zum Erstellen einer mehrsprachigen Konsolenanwendung finden Sie in den Abschnitten zu den Hinweisen von [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) und [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).

### <a name="determination-of-languages-to-support-at-run-time"></a>Bestimmung der zu unterstützenden Sprachen auf Run-Time

Sie können einen der folgenden Entwurfsvorschläge übernehmen, um zu bestimmen, welche Sprachen Ihre Anwendung zur Laufzeit unterstützen soll:

-   **Ermöglichen Sie es dem Endbenutzer während der Installation, die bevorzugte Sprache aus einer Liste der unterstützten Sprachen auszuwählen.**

-   **Lesen einer Sprachliste aus einer Konfigurationsdatei**

    Einige der Projekte in diesem Tutorial enthalten eine Funktion, die verwendet wird, um eine langs.txt Konfigurationsdatei zu analysieren, die eine Sprachliste enthält.

    Da diese Funktion externe Eingaben annimmt, überprüfen Sie die Sprachen, die als Eingabe bereitgestellt werden. Weitere Informationen zur Durchführung dieser Überprüfung finden Sie in den Funktionen [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) oder [**DownLevelLocaleNameToLCID.**](downlevellocalenametolcid.md)

-   **Abfragen des Betriebssystems, um zu bestimmen, welche Sprachen installiert sind**

    Dieser Ansatz hilft der Anwendung, die gleiche Sprache wie das Betriebssystem zu verwenden. Obwohl dies keine Benutzeraufforderung erfordert, sollten Sie bei Auswahl dieser Option beachten, dass Betriebssystemsprachen jederzeit hinzugefügt oder entfernt werden können und sich ändern können, nachdem der Benutzer die Anwendung installiert hat. Beachten Sie außerdem, dass das Betriebssystem in einigen Fällen mit eingeschränkter Sprachunterstützung installiert ist und die Anwendung einen größeren Nutzen bietet, wenn sie Sprachen unterstützt, die vom Betriebssystem nicht unterstützt werden.

    Weitere Informationen zum Ermitteln der derzeit im Betriebssystem installierten Sprachen finden Sie in der [**EnumUILanguages-Funktion.**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa)

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a>Unterstützung komplexer Skripts in Versionen vor Windows Vista

Wenn eine Anwendung, die bestimmte komplexe Skripts unterstützt, auf einer Version von Windows vor Windows Vista ausgeführt wird, wird text in diesem Skript möglicherweise nicht ordnungsgemäß in GUI-Komponenten angezeigt. Im kompatiblen Projekt in diesem Tutorial werden hi-IN- und ta-IN-Skripts aufgrund von Problemen bei der Verarbeitung komplexer Skripts und fehlender zugehöriger Schriftarten möglicherweise nicht im Meldungsfeld angezeigt. Normalerweise stellen sich Probleme dieser Art als quadratische Felder in der GUI-Komponente dar.

Weitere Informationen zum Aktivieren der komplexen Skriptverarbeitung finden Sie unter [Skript- und Schriftartunterstützung in Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).

## <a name="summary"></a>Zusammenfassung

In diesem Tutorial wurde eine einsprachige Anwendung globalisiert und die folgenden bewährten Methoden veranschaulicht.

-   Entwerfen Sie die Anwendung so, dass sie das Win32-Ressourcenmodell nutzt.
-   Verwenden Sie DIE SPLIT-Aufteilung von Ressourcen in Satellitenbinärdateien (.files).
-   Stellen Sie sicher, dass der Lokalisierungsprozess die Ressourcen in den DATEIEN DER DATEIEN AKTUALISIERT, sodass sie für die Zielsprache geeignet sind.
-   Stellen Sie sicher, dass die Paketierung und Bereitstellung der Anwendung, der zugeordneten DATEIEN und des Konfigurationsinhalts ordnungsgemäß durchgeführt wird, damit die RESSOURCENlade-APIs den lokalisierten Inhalt finden können.
-   Stellen Sie dem Endbenutzer einen Mechanismus bereit, um die Sprachkonfiguration der Anwendung anzupassen.
-   Passen Sie den Laufzeitcode an, um die Sprachkonfiguration zu nutzen, damit die Anwendung reaktionsfähiger auf die Anforderungen der Endbenutzer reagiert.

 

 
