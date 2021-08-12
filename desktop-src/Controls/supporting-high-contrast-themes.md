---
title: Unterstützen hoher Kontrast Designs
description: In diesem Thema wird die Unterstützung für Designs mit hohem Kontrast in Windows 8 mit denen früherer Versionen von Windows verglichen, und es wird erläutert, wie Designs mit hohem Kontrast in einer Windows 8 unterstützt werden.
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f32c89302daeb7190174a0d6b9e822e1c55d3e530ad29baedd00c5ffdefc97b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670626"
---
# <a name="supporting-high-contrast-themes"></a>Unterstützen hoher Kontrast Designs

In diesem Thema wird die Unterstützung für Designs mit hohem Kontrast in Windows 8 mit denen früherer Versionen von Windows verglichen, und es wird erläutert, wie Designs mit hohem Kontrast in einer Windows 8 unterstützt werden.

Sie enthält die folgenden Abschnitte.

-   [Übersicht über die Unterstützung für hoher Kontrast Designs](#overview-of-support-for-high-contrast-themes)
-   [Unterstützen hoher Kontrast Designs in Windows 8 und höher](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [Hinzufügen eines Kompatibilitätsabschnitts zum Anwendungsmanifest](#adding-a-compatibility-section-to-your-application-manifest)
-   [Erkennen hoher Kontrast in früheren Versionen von Windows](#detecting-high-contrast-in-previous-versions-of-windows)
-   [Zugehörige Themen](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a>Übersicht über die Unterstützung für hoher Kontrast Designs

Windows 7 und früher unterstützen zwei Designmodelle, einschließlich des legacy Windows klassischen Modells und der aktuellen visuellen Stile. Das Windows klassische Modell wurde bis Windows 7 beibehalten, um hauptsächlich die verschiedenen Designs mit hohem Kontrast zu unterstützen. Das klassische Windows hat jedoch eine Reihe von Nachteilen:

-   Keine Unterstützung für Designs, die visuelle Stile verwenden, z. B. Windows Denen. Benutzer von Designs mit hohem Kontrast müssen die Windows benutzeroberfläche verwenden.
-   Keine Unterstützung für Benutzeroberflächenfeatures, die für die Ausführung von Desktopfenster-Manager (DWM) verwendet werden, z. B. Miniaturansichten und die in Windows 7 eingeführte Vollbildlupe.
-   Entwickler müssen zwei separate Codepfade verwalten, um die beiden verschiedenen Themingmodelle zu unterstützen.

In Windows 8 und höher werden die vorherigen Nachteile durch die folgenden Änderungen am Themingmodell adressiert:

-   Das Windows klassische Designmodell wird nicht mehr unterstützt, sodass Entwickler nur einen Codepfad für Anwendungen verwalten können, die nur auf Windows 8.
-   Da visuelle Stile und DWM in Windows 8 sind, haben Benutzer mit hohem Kontrast Zugriff auf Features wie Miniaturansichten und die Vollbildlupe.
-   Visuelle Stile unterstützen das Festlegen der Farben verschiedener Benutzeroberflächenelemente, sodass Benutzer mit hohem Kontrast die Benutzeroberfläche an die individuellen Anforderungen und Einstellungen anpassen können.
-   Windows 8 enthält Kompatibilitätsunterstützung für vorhandene Anwendungen, die für die Verwendung von Designs mit hohem Kontrast entwickelt wurden, die auf dem Windows-Designmodell basieren.

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a>Unterstützen hoher Kontrast Designs in Windows 8 und höher

Da Windows 8 visuelle Stile im Modus mit hohem Kontrast aktiviert sind, ist die Unterstützung von Designs mit hohem Kontrast einfach, solange Sie die folgenden Richtlinien befolgen.

-   Schrift- und Steuerelementgrößen. Um sicherzustellen, dass Ihre Benutzeroberfläche für Benutzer mit Behinderungen zugänglich ist, legen Sie die Schriftgrößen gemäß den aktuellen Designeinstellungen fest. Legen Sie die Größe von Steuerelementen auf mindestens die Standardgröße fest.
-   Farben. Vermeiden Sie die Verwendung hart codierten Farben. Verwenden Sie stattdessen die Systemfarben, da sie auf dem aktuellen Design basieren. Die Verwendung benutzerdefinierter Farben kann die Farben in designs mit hohem Kontrast beeinträchtigen und überschreiben.
-   Anwendungsmanifest. Anwendungen, die für die Arbeit mit den neuen Designs mit hohem Kontrast entwickelt wurden, sollten über einen anwendungskompatibilitätsabschnitt verfügen, der in ihrem Manifest definiert ist und Windows 8 Kompatibilitäts-GUIDs enthält. Andernfalls Windows davon ausgegangen, dass die Anwendung für eine ältere Version von Windows entwickelt wurde, und rendert die Benutzeroberfläche der Anwendung, indem das Windows klassisches Designmodell simuliert wird.

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a>Hinzufügen eines Kompatibilitätsabschnitts zum Anwendungsmanifest

Ein Anwendungsmanifest ist eine XML-Datei, die die Anforderungen für eine Anwendung beschreibt. Der Kompatibilitätsabschnitt des Manifests identifiziert die Versionen der Windows von der Anwendung unterstützt werden. Die folgenden GUIDs werden im Kompatibilitätsabschnitt verwendet, um die verschiedenen Versionen von Windows.

| Version       | GUID                                   |
|---------------|----------------------------------------|
| Windows Vista | {e2011457-1546-43c5-a5fe-008deee3d3f0} |
| Windows 7     | {35138b9a-5d96-4fbd-8e2d-a2440225f93a} |
| Windows 8     | {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} |



 

Der Kompatibilitätsabschnitt kann mehrere Versionen von Windows, muss jedoch jeweils in einem eigenen Tag enthalten `<supportedOS/>` sein. Das folgende Beispiel zeigt ein Anwendungsmanifest, das Windows 7 und Windows 8 kompatibilitätsabschnitt angibt:


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!--The ID below indicates application support for Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>

            <!--The ID below indicates application support for Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        </application>
    </compatibility>
</assembly>
```



Wenn eine Anwendung über kein Kompatibilitätsmanifest verfügt, wird davon ausgegangen, dass es sich um eine Windows Vista-Anwendung handelt, und es werden keine Designsteuerelemente im Clientbereich verwendet, wenn ein Design mit hohem Kontrast aktiv ist. Außerdem ist das Verhalten einiger visueller Stilfunktionen betroffen. Beispielsweise geben [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)und [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) FALSE zurück, während [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) und [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) ein NULL-Handle zurückgeben. Dies ist für die Kompatibilitätsunterstützung geeignet, sodass Anwendungen, die vor Windows 8 erstellt wurden, ihre Benutzeroberfläche weiterhin im gleichen Aussehen rendern können wie der Modus mit hohem Kontrast früherer Versionen von Windows wenn visuelle Stile nicht verfügbar sind.

Auf Windows 8 erhält die Anwendung weiterhin die Vorteile der Desktopkomposition. Dies bedeutet beispielsweise, dass Benutzerfreundlichkeitsanwendungen wie die Vollbildlupe nicht vom Status des Manifests einer einzelnen Anwendung abhängen. Die Benutzerfreundlichkeitsanwendung funktioniert weiterhin im Modus mit hohem Kontrast mit einer Anwendung, die sich nicht als Windows 8 im Manifest identifiziert.

Die folgenden Abbildungen zeigen ein einfaches Dialogfeld mit hohem Kontrast Windows 7.

![Dialogfeld "hig-Kontrast"](images/win7-high-contrast.png)

Diese Abbildung zeigt dasselbe Dialogfeld mit hohem Kontrast auf Windows 8, jedoch mit Windows 7-Kompatibilität, die im Anwendungsmanifest angegeben ist:

![Dialogfeld "w8– hoher Kontrast"](images/win7-compat.png)

Diese Abbildung zeigt dasselbe Dialogfeld mit hohem Kontrast auf Windows 8, Windows 8 im Anwendungsmanifest angegeben ist:

![w8-Dialogfeld mit hohem Kontrast mit Manifest](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a>Erkennen hoher Kontrast in früheren Versionen von Windows

Anwendungen, die unter früheren Versionen von Windows haben keinen Zugriff auf die neuen Designs mit hohem Kontrast. Wenn Ihre Anwendung unter früheren Versionen von ausgeführt werden muss, sollten Sie Unterstützung für das Rendern Ihrer Benutzeroberfläche in hohem KontraWindowsst im Windows klassischen Designmodells enthalten. Ihre Anwendung kann bestimmen, ob ein Design mit hohem Kontrast aktiv ist, indem sie die [**SystemParametersInfo-Funktion**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) mit dem **SPI \_ GETHIGHCONTRAST-Flag** aufruft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren von visuellen Stilen](cookbook-overview.md)
</dt> <dt>

[Visuelle Stile](themes-overview.md)
</dt> </dl>

 

 