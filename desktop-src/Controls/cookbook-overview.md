---
title: Aktivieren von visuellen Stilen
description: In diesem Thema wird erläutert, wie Sie Ihre Anwendung konfigurieren, um sicherzustellen, dass allgemeine Steuerelemente im bevorzugten visuellen Stil des Benutzers angezeigt werden.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39339c0535767011a59730534486604389f62468
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949180"
---
# <a name="enabling-visual-styles"></a>Aktivieren von visuellen Stilen

In diesem Thema wird erläutert, wie Sie Ihre Anwendung konfigurieren, um sicherzustellen, dass allgemeine Steuerelemente im bevorzugten visuellen Stil des Benutzers angezeigt werden.

Das Thema enthält folgende Abschnitte:

-   [Verwenden von Manifesten oder Direktiven, um sicherzustellen, dass visuelle Stile auf Anwendungen angewendet werden können](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [Verwenden von ComCtl32.dll Version 6 in einer Anwendung, die nur Standard Erweiterungen verwendet](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [Verwenden von ComCtl32 Version 6 in der Systemsteuerung oder einer DLL, die von RunDll32.exeausgeführt wird ](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [Hinzufügen von Unterstützung für visuelle Stile zu einer Erweiterung, einem Plug-in, einem MMC-Snap-in oder einer DLL, die in einen Prozess integriert wird](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [Ausschalten visueller Stile](#turning-off-visual-styles)
-   [Verwenden von visuellen Stilen mit HTML-Inhalten](#using-visual-styles-with-html-content)
-   [Wenn visuelle Stile nicht angewendet werden](#when-visual-styles-are-not-applied)
-   [Kompatibilität Ihrer Anwendung mit früheren Versionen von Windows](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [Zugehörige Themen](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a>Verwenden von Manifesten oder Direktiven, um sicherzustellen, dass visuelle Stile auf Anwendungen angewendet werden können

Um der Anwendung die Verwendung visueller Stile zu ermöglichen, müssen Sie ComCtl32.dll Version 6 oder höher verwenden. Da Version 6 nicht weitervertreibbar ist, ist Sie nur verfügbar, wenn Ihre Anwendung unter einer Windows-Version ausgeführt wird, in der Sie enthalten ist. Windows ist sowohl mit Version 5 als auch mit Version 6 ausgeliefert. ComCtl32.dll Version 6 enthält sowohl die Benutzer Steuerelemente als auch die allgemeinen Steuerelemente. Standardmäßig verwenden Anwendungen die in User32.dll definierten Benutzer Steuerelemente und die allgemeinen Steuerelemente, die in ComCtl32.dll Version 5 definiert sind. Eine Liste der DLL-Versionen und deren Verteilungs Plattformen finden Sie unter [allgemeine Steuerelement Versionen](common-control-versions.md).

Wenn Sie möchten, dass Ihre Anwendung visuelle Stile verwendet, müssen Sie ein Anwendungs Manifest oder eine Compilerdirektive hinzufügen, die angibt, dass ComCtl32.dll Version 6 verwendet werden soll, wenn Sie verfügbar ist.

Ein Anwendungs Manifest ermöglicht einer Anwendung, anzugeben, welche Versionen einer Assembly benötigt werden. In Microsoft Win32 ist eine Assembly ein Satz von DLLs und eine Liste mit Versions fähigen Objekten, die in diesen DLLs enthalten sind.

Manifeste werden in XML geschrieben. Der Name der Anwendungs Manifest-Datei ist der Name der ausführbaren Datei, gefolgt von der Dateinamenerweiterung. Manifest; beispielsweise MyApp.exe. manifest. Das folgende Beispiel Manifest zeigt, dass im ersten Abschnitt das Manifest selbst beschrieben wird. In der folgenden Tabelle sind die Attribute aufgeführt, die vom Element **assemblyIdentity** im Abschnitt Beschreibung des Manifests festgelegt wurden.



| Attribut             | BESCHREIBUNG                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| version               | Version des Manifests. Die Version muss im Format major. Minor. Revision. Build vorliegen (d. h. n. n, wobei n <= 65535). |
| processorArchitecture | Der Prozessor, für den die Anwendung entwickelt wird.                                                                          |
| name                  | Schließt den Firmennamen, den Produktnamen und den Anwendungsnamen ein.                                                                   |
| type                  | Der Typ der Anwendung, z. b. Win32.                                                                                    |



 

Das Beispiel Manifest enthält außerdem eine Beschreibung Ihrer Anwendung und gibt Anwendungsabhängigkeiten an. In der folgenden Tabelle sind die Attribute aufgeführt, die vom **assemblyIdentity** -Element im Abhängigkeits Abschnitt festgelegt werden.



| Attribut             | BESCHREIBUNG                                      |
|-----------------------|--------------------------------------------------|
| type                  | Der Typ der Abhängigkeits Komponente, z. b. Win32. |
| name                  | Der Name der Komponente.                           |
| version               | Version der Komponente.                        |
| processorArchitecture | Prozessor, für den die Komponente entworfen wurde.    |
| PublicKeyToken        | Schlüssel Token, das mit dieser Komponente verwendet wird.              |
| language              | Die Sprache der Komponente.                       |



 

Im folgenden finden Sie ein Beispiel für eine Manifest-Datei.

> [!IMPORTANT]
> Legen Sie den Eintrag **ProcessorArchitecture** auf **"x86"** fest, wenn Ihre Anwendung auf die 32-Bit-Windows-Plattform ausgerichtet ist, oder auf **"amd64"** , wenn die Anwendung auf die Windows-Plattform mit dem 64 Bit Sie können auch **" \* "** angeben. Dadurch wird sichergestellt, dass alle Plattformen als Ziel festgelegt werden, wie in den folgenden Beispielen gezeigt.

 


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



Wenn Sie Microsoft Visual C++ 2005 oder höher verwenden, können Sie die folgende Compilerdirektive in Ihren Quellcode einfügen, anstatt ein Manifest manuell zu erstellen. Zur besseren Lesbarkeit wird die-Direktive hier in mehrere Zeilen aufgeteilt.


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



In den folgenden Themen werden die Schritte zum Anwenden visueller Stile auf verschiedene Anwendungs Typen beschrieben. Beachten Sie, dass das Manifest-Format in jedem Fall identisch ist.

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a>Verwenden von ComCtl32.dll Version 6 in einer Anwendung, die nur Standard Erweiterungen verwendet

Im folgenden finden Sie Beispiele für Anwendungen, die keine Erweiterungen von Drittanbietern verwenden.

-   Rechner
-   Freecell
-   Minesweeper
-   Editor
-   Solitär

**, Um ein Manifest zu erstellen und die Anwendung für die Verwendung visueller Stile zu aktivieren.**

1.  Verknüpfung mit Comctl32. lib und [**callinitcommoncontrols**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).
2.  Fügen Sie der Quell Struktur, die das XML-Manifest-Format aufweist, eine Datei mit dem Namen YourApp.exe. Manifest hinzu.
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

    

3.  Fügen Sie das Manifest wie folgt der Ressourcen Datei Ihrer Anwendung hinzu:
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > Wenn Sie den vorherigen Eintrag der Ressource hinzufügen, müssen Sie ihn in einer Zeile formatieren. Alternativ können Sie die XML-Manifest-Datei im gleichen Verzeichnis wie die ausführbare Datei der Anwendung platzieren. Das Betriebssystem lädt das Manifest zuerst aus dem Dateisystem und überprüft dann den Ressourcenabschnitt der ausführbaren Datei. Die Dateisystem Version hat Vorrang.

     

Wenn Sie die Anwendung erstellen, wird das Manifest als binäre Ressource hinzugefügt.

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a>Verwenden von ComCtl32 Version 6 in der Systemsteuerung oder einer DLL, die von RunDll32.exe ausgeführt wird

**, Um ein Manifest zu erstellen und die Anwendung für die Verwendung visueller Stile zu aktivieren.**

1.  Verknüpfung mit Comctl32. lib und [**callinitcommoncontrols**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).
2.  Fügen Sie der Quell Struktur, die das XML-Manifest-Format aufweist, eine Datei mit dem Namen YourApp.cpl. Manifest hinzu.
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

    

3.  Fügen Sie das Manifest der Ressourcen Datei Ihrer Anwendung als Ressourcen-ID 123 hinzu.

> [!Note]  
> Wenn Sie eine System Steuerungsanwendung erstellen, platzieren Sie Sie in der entsprechenden Kategorie. Die Systemsteuerung unterstützt jetzt die Kategorisierung von System Steuerungsanwendungen. Dies bedeutet, dass System Steuerungsanwendungen IDs zugewiesen und in Aufgabenbereiche wie z. b. hinzufügen oder Entfernen von Programmen, Darstellung und Designs oder Datums-, Uhrzeit-, sprach-und Regions Optionen aufgeteilt werden können.

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a>Hinzufügen von Unterstützung für visuelle Stile zu einer Erweiterung, einem Plug-in, einem MMC-Snap-in oder einer DLL, die in einen Prozess integriert wird

Die Unterstützung für visuelle Stile kann zu einer Erweiterung, einem Plug-in, einem MMC-Snap-in oder einer DLL hinzugefügt werden, die in einen Prozess eingebunden wird. Verwenden Sie beispielsweise die folgenden Schritte, um Unterstützung für visuelle Stile für ein Microsoft Management Console (MMC)-Snap-in hinzuzufügen.

1.  Kompilieren Sie das Snap-in mit dem Flag "-disolations- \_ \_ fähig", oder fügen Sie die folgende Anweisung vor der \# include-Anweisung "Windows. h" ein.

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    Weitere Informationen zur \_ \_ aktivierten Isolation finden Sie unter [Isolieren von Komponenten](/windows/desktop/SbsCs/isolating-components).

2.  Schließen Sie die allgemeine Steuerungs Header Datei in die Snap-in-Quelle ein.
    ```C++
    #include <commctrl.h>
    ```

    

3.  Fügen Sie der Quell Struktur, die das XML-Manifest-Format verwendet, eine Datei namens yourapp. Manifest hinzu.
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

    

4.  Fügen Sie das Manifest der Ressourcen Datei Ihres Snap-Ins hinzu. Weitere Informationen zum Hinzufügen eines Manifests zu einer Ressourcen Datei finden [Sie unter Verwenden von ComCtl32 Version 6 in einer Anwendung, die Erweiterungen, Plug-ins oder eine DLL verwendet, die in einen Prozess eingefügt wird](/previous-versions//ms649781(v=vs.85)) .

## <a name="turning-off-visual-styles"></a>Ausschalten visueller Stile

Sie können visuelle Stile für ein-Steuerelement oder für alle Steuerelemente in einem Fenster deaktivieren, indem Sie die [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) -Funktion wie folgt aufrufen:


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



Im vorherigen Beispiel ist *HWND* das Handle des Fensters, in dem visuelle Stile deaktiviert werden. Nach dem-Befehl wird das-Steuerelement ohne visuelle Stile gerendert.

## <a name="using-visual-styles-with-html-content"></a>Verwenden von visuellen Stilen mit HTML-Inhalten

Auf HTML-Seiten, die die Eigenschaften des Cascading Stylesheets (CSS) ändern (z. b. Hintergrund oder Rahmen), werden keine visuellen Stile auf Sie angewendet. Sie zeigen das angegebene CSS-Attribut an. Wenn die meisten CSS-Eigenschaften als Teil des Inhalts angegeben werden, gelten die meisten CSS-Eigenschaften für Elemente, auf die visuelle Stile angewendet werden.

Standardmäßig werden visuelle Stile auf die systeminternen HTML-Steuerelemente auf Seiten angewendet, die in Microsoft Internet Explorer 6 und höheren Versionen angezeigt werden. Um visuelle Stile für eine HTML-Seite zu deaktivieren, fügen Sie ein Meta-Tag zum <head> -Abschnitt. Dieses Verfahren gilt auch für Inhalte, die als HTML-Anwendungen (HTAs) verpackt sind. Um visuelle Stile zu deaktivieren, muss das Meta-Tag wie folgt lauten:


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> Wenn die Browsereinstellung und die tageinstellung nicht übereinstimmen, werden auf der Seite keine visuellen Stile angewendet. Wenn das Meta-Tag beispielsweise auf "No" festgelegt ist und der Browser so festgelegt ist, dass visuelle Stile aktiviert werden, werden visuelle Stile nicht auf die Seite angewendet. Wenn jedoch entweder der Browser oder das Meta-Tag auf "yes" festgelegt ist und das andere Element nicht angegeben ist, werden visuelle Stile angewendet.

 

Visuelle Stile können das Layout Ihrer Inhalte ändern. Wenn Sie bestimmte Attribute auf systeminternen HTML-Steuerelementen festlegen, wie z. b. die Breite einer Schaltfläche, können Sie feststellen, dass die Bezeichnung auf der Schaltfläche unter bestimmte visuelle Stile nicht lesbar ist.

Sie müssen Ihre Inhalte mit visuellen Stilen gründlich testen, um zu bestimmen, ob das Anwenden visueller Stile eine negative Auswirkung auf ihren Inhalt und Ihr Layout hat.

## <a name="when-visual-styles-are-not-applied"></a>Wenn visuelle Stile nicht angewendet werden

Um zu vermeiden, dass visuelle Stile auf ein Fenster der obersten Ebene angewendet werden, weisen Sie dem Fenster einen nicht-NULL-Bereich (**setwindowrgn**) zu. Das System geht davon aus, dass ein Fenster mit einer nicht-NULL-Region ein spezielles Fenster ist, in dem keine visuellen Stile verwendet werden. Ein untergeordnetes Fenster, das einem Fenster auf oberster Ebene der nicht visuellen Stile zugeordnet ist, kann dennoch visuelle Stile anwenden, auch wenn das übergeordnete Fenster dies nicht tut.

Wenn Sie die Verwendung visueller Stile für alle Fenster in der Anwendung deaktivieren möchten, rufen Sie [**settemeappproperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) auf, und übergeben Sie das Flag "STAP \_ Allow \_ nonclient" nicht. Wenn eine Anwendung **settemeappproperties** nicht aufruft, werden die angenommenen Flagwerte STAP \_ Allow \_ nonclient STAP Allow Control STAP Allow \| \_ \_ \| \_ \_ Webcontent. Die angenommenen Werte bewirken, dass der nicht-Client Bereich, die Steuerelemente und Webinhalte auf einen visuellen Stil angewendet werden.

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a>Kompatibilität Ihrer Anwendung mit früheren Versionen von Windows

Ein Großteil der Architektur des visuellen Stils ist so konzipiert, dass es einfach ist, Ihr Produkt in früheren Versionen von Windows bereitzustellen, die das Ändern der Darstellung von Steuerelementen nicht unterstützen. Beachten Sie Folgendes, wenn Sie eine Anwendung für mehr als ein Betriebssystem versenden:

-   In Windows-Versionen vor Windows 8 sind visuelle Stile deaktiviert, wenn ein hoher Kontrast auf on steht. Um einen hohen Kontrast zu unterstützen, muss eine ältere Anwendung, die visuelle Stile unterstützt, einen separaten Codepfad bereitstellen, um Benutzeroberflächen Elemente im hohen Kontrast korrekt zu zeichnen. In Windows 8 ist der hohe Kontrast ein Teil von visuellen Stilen. eine Windows 8-Anwendung (eine mit der Windows 8-GUID im Kompatibilitäts Abschnitt des Anwendungs Manifests) muss jedoch immer noch einen separaten Codepfad bereitstellen, um im hohen Kontrast zu Windows 7 einem früheren Zeitpunkt ordnungsgemäß zu Rendering.
-   Wenn Sie die Funktionen in ComCtl32.dll Version 6 verwenden (z. b. die Kachel Ansicht oder das Link Steuerelement), müssen Sie den Fall behandeln, in dem diese Steuerelemente auf dem Computer des Benutzers nicht verfügbar sind. ComCtl32.dll Version 6 ist nicht Verteil Bar.
-   Testen Sie Ihre Anwendung, um sicherzustellen, dass Sie sich nicht auf Features von ComCtl32.dll Version 6 verlassen, ohne zuerst die aktuelle Version zu überprüfen.
-   Nicht mit "uxtheme. lib" verknüpfen.
-   Schreiben Sie Fehler Behandlungs Code für-Instanzen, wenn visuelle Stile nicht erwartungsgemäß funktionieren.
-   Wenn Sie das Manifest der Anwendung in früheren Versionen installieren, wirkt sich dies nicht auf das Rendering von Steuerelementen aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Visuelle Stile](themes-overview.md)
</dt> </dl>

 

 