---
title: Aktivieren von visuellen Stilen
description: In diesem Thema wird erläutert, wie Sie Ihre Anwendung konfigurieren, um sicherzustellen, dass allgemeine Steuerelemente im bevorzugten visuellen Stil des Benutzers angezeigt werden.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f259be6165bd3a4f9f5a655aaecf0fe6837de3dce057848ba92ac737e608fbc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413366"
---
# <a name="enabling-visual-styles"></a>Aktivieren von visuellen Stilen

In diesem Thema wird erläutert, wie Sie Ihre Anwendung konfigurieren, um sicherzustellen, dass allgemeine Steuerelemente im bevorzugten visuellen Stil des Benutzers angezeigt werden.

Das Thema enthält folgende Abschnitte:

-   [Verwenden von Manifesten oder Direktiven, um sicherzustellen, dass visuelle Stile auf Anwendungen angewendet werden können](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [Verwenden ComCtl32.dll Version 6 in einer Anwendung, die nur Standarderweiterungen verwendet](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [Verwenden von ComCtl32 Version 6 in Systemsteuerung oder einer DLL, die von RunDll32.exe](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [Hinzufügen der Unterstützung visueller Stile zu einer Erweiterung, einem Plug-In, einem MMC-Snap-In oder einer DLL, die in einen Prozess eingebunden wird](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [Deaktivieren von visuellen Stilen](#turning-off-visual-styles)
-   [Verwenden von visuellen Stilen mit HTML-Inhalt](#using-visual-styles-with-html-content)
-   [Wenn visuelle Stile nicht angewendet werden](#when-visual-styles-are-not-applied)
-   [Herstellen der Kompatibilität Ihrer Anwendung mit früheren Versionen von Windows](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [Zugehörige Themen](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a>Verwenden von Manifesten oder Direktiven, um sicherzustellen, dass visuelle Stile auf Anwendungen angewendet werden können

Damit Ihre Anwendung visuelle Stile verwenden kann, müssen Sie ComCtl32.dll Version 6 oder höher verwenden. Da Version 6 nicht verteilbar ist, ist sie nur verfügbar, wenn Ihre Anwendung unter einer Version von Windows ausgeführt wird, die sie enthält. Windows wird sowohl mit Version 5 als auch mit Version 6 ausgeliefert. ComCtl32.dll Version 6 enthält sowohl die Benutzersteuerelemente als auch die allgemeinen Steuerelemente. Standardmäßig verwenden Anwendungen die in User32.dll definierten Benutzersteuerelemente und die allgemeinen Steuerelemente, die in ComCtl32.dll Version 5 definiert sind. Eine Liste der DLL-Versionen und deren Verteilungsplattformen finden Sie unter [Allgemeine Steuerungsversionen.](common-control-versions.md)

Wenn Ihre Anwendung visuelle Stile verwenden soll, müssen Sie ein Anwendungsmanifest oder eine Compilerdirektive hinzufügen, die angibt, dass ComCtl32.dll Version 6 verwendet werden soll, wenn sie verfügbar ist.

Mit einem Anwendungsmanifest kann eine Anwendung angeben, welche Versionen einer Assembly erforderlich sind. In Microsoft Win32 besteht eine Assembly aus einer Reihe von DLLs und einer Liste von objekten, die versionierbar sind, die in diesen DLLs enthalten sind.

Manifeste werden in XML geschrieben. Der Name der Anwendungsmanifestdatei ist der Name Ihrer ausführbaren Datei, gefolgt von der Dateinamenerweiterung .manifest. beispiel: MyApp.exe.manifest. Das folgende Beispielmanifest zeigt, dass im ersten Abschnitt das Manifest selbst beschrieben wird. Die folgende Tabelle zeigt die Attribute, die vom **assemblyIdentity-Element** im Abschnitt manifest description festgelegt wurden.



| attribute             | BESCHREIBUNG                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| version               | Version des Manifests. Die Version muss das Format major.minor.revision.build haben (d.h. n.n.n.n, wobei n <=65535). |
| processorArchitecture | Prozessor, für den Ihre Anwendung entwickelt wird.                                                                          |
| name                  | Enthält den Firmennamen, den Produktnamen und den Anwendungsnamen.                                                                   |
| Type                  | Typ Ihrer Anwendung, z. B. Win32.                                                                                    |



 

Das Beispielmanifest enthält auch eine Beschreibung Ihrer Anwendung und gibt Anwendungsabhängigkeiten an. Die folgende Tabelle zeigt die Attribute, die vom **assemblyIdentity-Element** im Abschnitt "dependency" festgelegt werden.



| attribute             | BESCHREIBUNG                                      |
|-----------------------|--------------------------------------------------|
| type                  | Typ der Abhängigkeitskomponente, z. B. Win32. |
| name                  | Der Name der Komponente.                           |
| version               | Version der Komponente.                        |
| processorArchitecture | Prozessor, für den die Komponente entworfen wurde.    |
| Publickeytoken        | Schlüsseltoken, das mit dieser Komponente verwendet wird.              |
| language              | Sprache der Komponente.                       |



 

Es folgt ein Beispiel für eine Manifestdatei.

> [!IMPORTANT]
> Legen Sie den Eintrag **processorArchitecture** auf **"X86"** fest, wenn Ihre Anwendung auf die 32-Bit-Windows-Plattform abzielt, oder auf **"amd64",** wenn Ihre Anwendung auf die 64-Bit-Windows-Plattform abzielt. Sie können auch **" \* " "** angeben, um sicherzustellen, dass alle Plattformen als Ziel verwendet werden, wie in den folgenden Beispielen gezeigt.

 


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity
    version="1.0.0.0"
    processorArchitecture="*"
    name="CompanyName.ProductName.YourApplication"
    type="win32"
/>
<description>Your application description here.</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="*"
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
</assembly>
```



Wenn Sie Microsoft Visual C++ 2005 oder höher verwenden, können Sie dem Quellcode die folgende Compilerdirektive hinzufügen, anstatt manuell ein Manifest zu erstellen. Aus Gründen der Lesbarkeit ist die -Direktive hier in mehrere Zeilen unterteilt.


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



In den folgenden Themen werden die Schritte zum Anwenden visueller Stile auf verschiedene Anwendungstypen beschrieben. Beachten Sie, dass das Manifestformat in jedem Fall identisch ist.

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a>Verwenden ComCtl32.dll Version 6 in einer Anwendung, die nur Standarderweiterungen verwendet

Im Folgenden sind Beispiele für Anwendungen aufgeführt, die keine Erweiterungen von Drittanbietern verwenden.

-   Calculator
-   FreeCell (in Windows Vista und Windows 7)
-   Zungeweeper (in Windows Vista und Windows 7)
-   Editor
-   Solitair (in Windows Vista und Windows 7)

**So erstellen Sie ein Manifest und ermöglichen Ihrer Anwendung die Verwendung visueller Stile.**

1.  Link zu ComCtl32.lib, und rufen [**Sie InitCommonControls auf.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)
2.  Fügen Sie ihrer Quellstruktur eine Datei namens YourApp.exe.manifest mit dem XML-Manifestformat hinzu.
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  Fügen Sie das Manifest wie folgt der Ressourcendatei Ihrer Anwendung hinzu:
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > Wenn Sie der Ressource den vorherigen Eintrag hinzufügen, müssen Sie ihn in einer Zeile formatieren. Alternativ können Sie die XML-Manifestdatei im selben Verzeichnis wie die ausführbare Datei Ihrer Anwendung platzieren. Das Betriebssystem lädt zuerst das Manifest aus dem Dateisystem und überprüft dann den Ressourcenabschnitt der ausführbaren Datei. Die Dateisystemversion hat Vorrang.

     

Wenn Sie Ihre Anwendung erstellen, wird das Manifest als binäre Ressource hinzugefügt.

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a>Verwenden von ComCtl32 Version 6 in Systemsteuerung oder einer DLL, die von RunDll32.exe

**So erstellen Sie ein Manifest und ermöglichen Ihrer Anwendung die Verwendung visueller Stile.**

1.  Link zu ComCtl32.lib, und rufen [**Sie InitCommonControls auf.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)
2.  Fügen Sie ihrer Quellstruktur eine Datei namens YourApp.cpl.manifest mit dem XML-Manifestformat hinzu.
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  Fügen Sie das Manifest der Ressourcendatei Ihrer Anwendung als Ressourcen-ID 123 hinzu.

> [!Note]  
> Wenn Sie eine Systemsteuerung Anwendung erstellen, platzieren Sie sie in der entsprechenden Kategorie. Systemsteuerung unterstützt jetzt die Kategorisierung von Systemsteuerung Anwendungen. Dies bedeutet, dass Systemsteuerung Anwendungen Bezeichner zugewiesen und in Aufgabenbereiche wie Programme hinzufügen oder entfernen, Darstellung und Designs oder Datum, Uhrzeit, Sprache und regionale Optionen unterteilt werden können.

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a>Hinzufügen der Unterstützung visueller Stile zu einer Erweiterung, einem Plug-In, einem MMC-Snap-In oder einer DLL, die in einen Prozess eingebunden wird

Unterstützung für visuelle Stile kann einer Erweiterung, einem Plug-In, einem MMC-Snap-In oder einer DLL hinzugefügt werden, die in einen Prozess eingefügt wird. Verwenden Sie beispielsweise die folgenden Schritte, um visuelle Stile für ein mmc-Snap-In (Microsoft Management Console) hinzuzufügen.

1.  Kompilieren Sie das Snap-In mit dem Flag -DISOLATION \_ AWARE \_ ENABLED, oder fügen Sie die folgende Anweisung vor der \# include "windows.h"-Anweisung ein.

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    Weitere Informationen zu ISOLATION \_ AWARE ENABLED finden Sie unter Isolieren von \_ [Komponenten.](/windows/desktop/SbsCs/isolating-components)

2.  Schließen Sie die allgemeine Steuerheaderdatei in ihre Snap-In-Quelle ein.
    ```C++
    #include <commctrl.h>
    ```

    

3.  Fügen Sie Ihrer Quellstruktur eine Datei namens YourApp.manifest hinzu, die das XML-Manifestformat verwendet.
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

4.  Fügen Sie das Manifest der Ressourcendatei Ihres Snap-Ins hinzu. Ausführliche Informationen zum Hinzufügen eines Manifests zu einer Ressourcendatei finden Sie unter [Verwenden von ComCtl32 Version 6 in einer Anwendung, die Erweiterungen, Plug-Ins oder eine DLL verwendet, die in einen Prozess eingebunden wird.](/previous-versions//ms649781(v=vs.85))

## <a name="turning-off-visual-styles"></a>Deaktivieren von visuellen Stilen

Sie können visuelle Stile für ein Steuerelement oder für alle Steuerelemente in einem Fenster deaktivieren, indem Sie die [**SetWindowTheme-Funktion**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) wie folgt aufrufen:


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



Im vorherigen Beispiel ist *hwnd* das Handle des Fensters, in dem visuelle Stile deaktiviert werden. Nach dem Aufruf wird das Steuerelement ohne visuelle Stile gerendert.

## <a name="using-visual-styles-with-html-content"></a>Verwenden von visuellen Stilen mit HTML-Inhalt

AUF HTML-Seiten, die die CSS-Eigenschaften (Cascading Stylesheets) ändern, z. B. Hintergrund oder Rahmen, werden keine visuellen Stile angewendet. Sie zeigen das angegebene CSS-Attribut an. Wenn sie als Teil des Inhalts angegeben werden, gelten die meisten CSS-Eigenschaften für Elemente, auf die visuelle Stile angewendet wurden.

Standardmäßig werden visuelle Stile auf systeminterne HTML-Steuerelemente auf Seiten angewendet, die in Microsoft Internet Explorer 6 und höher angezeigt werden. Um visuelle Stile für eine HTML-Seite zu deaktivieren, fügen Sie der ein META-Tag hinzu. <head> -Abschnitt. Diese Technik gilt auch für Inhalte, die als HTML-Anwendungen (HTAs) gepackt sind. Um visuelle Stile zu deaktivieren, muss das META-Tag wie folgt lauten:


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> Wenn die Browsereinstellung und die Tageinstellung nicht übereinstimmen, wendet die Seite keine visuellen Stile an. Wenn das META-Tag beispielsweise auf "Nein" festgelegt ist und der Browser visuelle Stile aktiviert, werden visuelle Stile nicht auf die Seite angewendet. Wenn das Browser- oder META-Tag jedoch auf "Ja" festgelegt ist und das andere Element nicht angegeben ist, werden visuelle Stile angewendet.

 

Visuelle Stile können das Layout Ihres Inhalts ändern. Wenn Sie bestimmte Attribute für systeminterne HTML-Steuerelemente festlegen, z. B. die Breite einer Schaltfläche, stellen Sie möglicherweise fest, dass die Bezeichnung auf der Schaltfläche unter bestimmten visuellen Stilen nicht lesbar ist.

Sie müssen Ihre Inhalte gründlich mithilfe visueller Stile testen, um zu ermitteln, ob das Anwenden visueller Stile negative Auswirkungen auf Ihren Inhalt und Ihr Layout hat.

## <a name="when-visual-styles-are-not-applied"></a>Wenn visuelle Stile nicht angewendet werden

Um zu vermeiden, dass visuelle Stile auf ein Fenster der obersten Ebene angewendet werden, geben Sie dem Fenster einen Bereich ungleich NULL (**SetWindowRgn**). Das System geht davon aus, dass ein Fenster mit einem Nicht-NULL-Bereich ein spezialisiertes Fenster ist, das keine visuellen Stile verwendet. Ein untergeordnetes Fenster, das einem Fenster der obersten Ebene zugeordnet ist, das keine visuellen Stile enthält, kann visuelle Stile anwenden, auch wenn das übergeordnete Fenster dies nicht tut.

Wenn Sie die Verwendung visueller Stile für alle Fenster in Ihrer Anwendung deaktivieren möchten, rufen [**Sie SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) auf, und übergeben Sie nicht das Flag STAP \_ ALLOW \_ NONCLIENT. Wenn eine Anwendung **SetThemeAppProperties** nicht aufruft, sind die angenommenen Flagwerte STAP \_ ALLOW \_ NONCLIENT \| STAP \_ ALLOW CONTROLS \_ \| STAP ALLOW \_ \_ WEBCONTENT. Die angenommenen Werte bewirken, dass für den Nichtclientbereich, die Steuerelemente und den Webinhalt ein visueller Stil angewendet wird.

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a>Herstellen der Kompatibilität Ihrer Anwendung mit früheren Versionen von Windows

Ein Großteil der visuellen Stilarchitektur ist so konzipiert, dass es einfach ist, Ihr Produkt weiterhin in früheren Versionen von Windows zu liefern, die das Ändern der Darstellung von Steuerelementen nicht unterstützen. Beachten Sie beim Versand einer Anwendung für mehrere Betriebssysteme Folgendes:

-   In Versionen von Windows vor Windows 8 sind visuelle Stile deaktiviert, wenn hoher Kontrast eingeschaltet ist. Um hohen Kontrast zu unterstützen, muss eine ältere Anwendung, die visuelle Stile unterstützt, einen separaten Codepfad bereitstellen, um Benutzeroberflächenelemente mit hohem Kontrast ordnungsgemäß zu zeichnen. In Windows 8 ist hoher Kontrast Teil visueller Stile. eine Windows 8 Anwendung (die die Windows 8 GUID im Kompatibilitätsabschnitt ihres Anwendungsmanifests enthält) muss jedoch weiterhin einen separaten Codepfad bereitstellen, um auf Windows 7 einen korrekten Kontrast zu rendern.
-   Wenn Sie die Features in ComCtl32.dll Version 6 verwenden, z. B. die Kachelansicht oder das Linksteuerelement, müssen Sie den Fall behandeln, in dem diese Steuerelemente auf dem Computer Ihres Benutzers nicht verfügbar sind. ComCtl32.dll Version 6 ist nicht verteilbar.
-   Testen Sie Ihre Anwendung, um sicherzustellen, dass Sie sich nicht auf Features von ComCtl32.dll Version 6 verlassen, ohne zuerst nach der aktuellen Version zu suchen.
-   Verknüpfen Sie nicht mit UxTheme.lib.
-   Schreiben Sie Fehlerbehandlungscode für Instanzen, wenn visuelle Stile nicht wie erwartet funktionieren.
-   Die Installation des Anwendungsmanifests in früheren Versionen wirkt sich nicht auf das Rendering von Steuerelementen aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Visuelle Stile](themes-overview.md)
</dt> </dl>

 

 
