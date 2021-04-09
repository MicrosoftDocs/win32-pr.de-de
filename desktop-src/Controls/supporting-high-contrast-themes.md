---
title: Unterstützen von hoher Kontrast Designs
description: In diesem Thema wird die Unterstützung für Designs mit hohem Kontrast in Windows 8 mit denen früherer Windows-Versionen verglichen, und es wird erläutert, wie Designs mit hohem Kontrast in einer Windows 8-Anwendung unterstützt werden.
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2068d64b585f302f578296c9e156895c23b9bce9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858489"
---
# <a name="supporting-high-contrast-themes"></a>Unterstützen von hoher Kontrast Designs

In diesem Thema wird die Unterstützung für Designs mit hohem Kontrast in Windows 8 mit denen früherer Windows-Versionen verglichen, und es wird erläutert, wie Designs mit hohem Kontrast in einer Windows 8-Anwendung unterstützt werden.

Dies umfasst die folgenden Abschnitte.

-   [Übersicht über die Unterstützung von hoher Kontrast Designs](#overview-of-support-for-high-contrast-themes)
-   [Unterstützen von hoher Kontrast Designs in Windows 8 und höher](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [Hinzufügen eines Kompatibilitäts Abschnitts zum Anwendungs Manifest](#adding-a-compatibility-section-to-your-application-manifest)
-   [Erkennen von hoher Kontrast in früheren Versionen von Windows](#detecting-high-contrast-in-previous-versions-of-windows)
-   [Zugehörige Themen](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a>Übersicht über die Unterstützung von hoher Kontrast Designs

Windows 7 und frühere Versionen unterstützen zwei Designmodelle, einschließlich des klassischen Windows Classic-Modells und der aktuellen visuellen Stile. Das klassische Windows-Modell wurde über Windows 7 vor allem zur Unterstützung der verschiedenen Designs mit hohem Kontrast beibehalten. Das klassische Windows-Modell weist jedoch eine Reihe von Nachteilen auf:

-   Keine Unterstützung für Designs, die visuelle Stile verwenden, wie z. b. Windows Aero. Benutzer mit Designs mit hohem Kontrast müssen die klassische Windows-Benutzeroberfläche verwenden.
-   Keine Unterstützung für Benutzeroberflächen Features, die zum Ausführen von Desktopfenster-Manager (DWM) benötigt werden, wie z. b. Miniaturansichten und die voll Bild Bildschirmlupe, die in Windows 7 eingeführt wurde.
-   Entwickler müssen zwei separate Codepfade verwalten, um die beiden unterschiedlichen Designmodelle zu unterstützen.

In Windows 8 und höher werden die vorherigen Nachteile durch die folgenden Änderungen am Designmodell behandelt:

-   Das klassische Windows-Designmodell wird nicht mehr unterstützt, sodass Entwickler nur einen Codepfad für Anwendungen verwalten können, die nur auf Windows 8 abzielen.
-   Da visuelle Stile und DWM in Windows 8 vorhanden sind, haben Benutzer mit hohem Kontrast Zugriff auf Features wie Miniaturansichten und die Bildschirmlupe.
-   Visuelle Stile unterstützen das Festlegen der Farben verschiedener Benutzeroberflächen Elemente, sodass Benutzer mit hohem Kontrast die Benutzeroberfläche anpassen können, um die individuellen Anforderungen und Vorlieben zu erfüllen.
-   Windows 8 umfasst Kompatibilitäts Unterstützung für vorhandene Anwendungen, die für die Verwendung von Designs mit hohem Kontrast basierend auf dem klassischen Windows-Designmodell entwickelt wurden.

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a>Unterstützen von hoher Kontrast Designs in Windows 8 und höher

Da visuelle Stile in Windows 8 im Modus mit hohem Kontrast angezeigt werden, ist die Unterstützung von Designs mit hohem Kontrast unkompliziert, solange Sie die folgenden Richtlinien beachten.

-   Schrift-und Steuerelement Größen. Um sicherzustellen, dass die Benutzeroberfläche für Benutzer mit Behinderungen zugänglich ist, legen Sie Schriftart Größen entsprechend den aktuellen Design Einstellungen fest. Legen Sie die Größe der Steuerelemente auf mindestens die Standardgröße fest.
-   Ellen. Vermeiden Sie es, hart codierte Farben zu verwenden. Verwenden Sie stattdessen die Systemfarben, da Sie auf dem aktuellen Design basieren. Durch die Verwendung benutzerdefinierter Farben können die Farben in den Designs mit hohem Kontrast beeinträchtigt und überschrieben werden.
-   Anwendungs Manifest. Für Anwendungen, die für die Arbeit mit den neuen Designs mit hohem Kontrast entwickelt wurden, sollte ein Anwendungs Kompatibilitäts Abschnitt definiert sein, der die Windows 8-Kompatibilitäts-GUIDs enthält. Andernfalls geht Windows davon aus, dass die Anwendung auf eine ältere Version von Windows ausgelegt ist, und rendert die Benutzeroberfläche der Anwendung, indem das klassische Windows-Designmodell simuliert wird.

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a>Hinzufügen eines Kompatibilitäts Abschnitts zum Anwendungs Manifest

Ein Anwendungs Manifest ist eine XML-Datei, in der die Anforderungen für eine Anwendung beschrieben werden. Der Kompatibilitäts Abschnitt des Manifests identifiziert die Versionen von Windows, die von der Anwendung unterstützt werden. Die folgenden GUIDs werden im Kompatibilitäts Abschnitt verwendet, um die verschiedenen Versionen von Windows zu identifizieren.

| Version       | GUID                                   |
|---------------|----------------------------------------|
| Windows Vista | {e2011457-1546-43c5-a5fe-008deee3d3f0} |
| Windows 7     | {35138b9a-5d96-4f BD-8e2d-a2440225b93a} |
| Windows 8     | {4a2b28e3-53b9-4441-ba9c-d69d4a4a6e38} |



 

Im Kompatibilitäts Abschnitt können mehrere Versionen von Windows angegeben werden, die jeweils in einem eigenen Tag enthalten sein müssen `<supportedOS/>` . Das folgende Beispiel zeigt ein Anwendungs Manifest, das Windows 7 und Windows 8 im Kompatibilitäts Abschnitt angibt:


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



Wenn für eine Anwendung kein Kompatibilitäts Manifest vorhanden ist, wird davon ausgegangen, dass es sich um eine Windows Vista-Anwendung handelt, und es werden keine Design Steuerelemente im Client Bereich verwendet, wenn ein Design mit hohem Kontrast aktiv ist. Außerdem ist das Verhalten einiger visueller Stile-Funktionen betroffen. Beispielsweise wird von [**isthmeactive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**iscompositionactive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)und [**isapptheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) false zurückgegeben, während [**openthmedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) und [**openrowmedataex**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) ein NULL-Handle zurückgeben. Dies dient der Kompatibilitäts Unterstützung, sodass Anwendungen, die vor Windows 8 erstellt wurden, Ihre Benutzeroberfläche immer noch in demselben aussehen wie der Modus für hohe Kontraste in früheren Versionen von Windows renderingelemente darstellen können, in dem visuelle Stile nicht verfügbar sind.

Unter Windows 8 erhält die Anwendung weiterhin die Vorteile der Desktop Komposition. Dies bedeutet beispielsweise, dass die Verwendbarkeit von Anwendungen wie z. b. der Vollbild-Bildschirmlupe nicht vom Status des Manifests einer einzelnen Anwendung abhängt. Die Verwendbarkeits Anwendung funktioniert im Modus mit hohem Kontrast weiterhin mit einer Anwendung, die sich nicht im Manifest als Windows 8-kompatibel identifiziert.

In den folgenden Abbildungen wird ein einfaches Dialogfeld in hohem Kontrast zu Windows 7 angezeigt.

![Dialogfeld "Benutzer-Kontrast"](images/win7-high-contrast.png)

Dieses Bild zeigt das gleiche Dialogfeld in hohem Kontrast zu Windows 8, aber mit der Windows 7-Kompatibilität, die im Anwendungs Manifest angegeben ist:

![Dialogfeld für den hohen Kontrast von W8](images/win7-compat.png)

Dieses Bild zeigt das gleiche Dialogfeld in hohem Kontrast zu Windows 8, wobei Windows 8 im Anwendungs Manifest angegeben ist:

![W8-Dialogfeld mit hohem Kontrast und Manifest](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a>Erkennen von hoher Kontrast in früheren Versionen von Windows

Anwendungen, die in früheren Versionen von Windows ausgeführt werden, haben keinen Zugriff auf die neuen Designs mit hohem Kontrast. Wenn Ihre Anwendung auf früheren Versionen von ausgeführt werden muss, sollten Sie die Unterstützung für das Rendern Ihrer Benutzeroberfläche im klassischen Windows-Designmodell in High kontra windowsst einschließen. Die Anwendung kann ermitteln, ob ein Design mit hohem Kontrast aktiv ist, indem die [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion mit dem **SPI \_ gethighcontrast** -Flag aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren von visuellen Stilen](cookbook-overview.md)
</dt> <dt>

[Visuelle Stile](themes-overview.md)
</dt> </dl>

 

 