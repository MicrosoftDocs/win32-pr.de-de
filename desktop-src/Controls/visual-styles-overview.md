---
title: Übersicht über visuelle Stile
description: In diesem Thema werden visuelle Stile beschrieben und die Windows, die diese unterstützen. Außerdem werden die Schritte erläutert, die Sie ausführen müssen, um visuelle Stile in Ihren Anwendungen zu verwenden.
ms.assetid: 5B5D7BB6-684F-478D-BF5F-B8D18BBCFF2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 237ac858e1a60e615a6af177728102fb7e6ea1737a3a2d94d93091264b02121a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077724"
---
# <a name="visual-styles-overview"></a>Übersicht über visuelle Stile

In diesem Thema werden visuelle Stile beschrieben und die Windows, die diese unterstützen. Außerdem werden die Schritte erläutert, die Sie ausführen müssen, um visuelle Stile in Ihren Anwendungen zu verwenden. Dieses Thema enthält die folgenden Abschnitte:

-   [Themes and Visual Styles](#themes-and-visual-styles)
-   [Komponenten visueller Stile](#visual-styles-components)
-   [Anwendungsanforderungen für die Unterstützung visueller Stile](#application-requirements-for-supporting-visual-styles)
-   [Zugehörige Themen](#related-topics)

## <a name="themes-and-visual-styles"></a>Themes and Visual Styles

Windows enthält mehrere Features, mit denen Benutzer die Benutzeroberfläche an ihre individuellen Anforderungen und Einstellungen anpassen können. Zu diesen Features gehören Designs, die in Microsoft Plus eingeführt wurden. für Windows 95. Ein Design ist eine vom Benutzer auswählbare Sammlung von Einstellungen, die Hintergrundbilder, Cursor, Schriftarten, Sounds und Symbole umfasst. Im Folgenden finden Sie einige Merkmale von Designs.

-   Designeinstellungen werden in DESIGN-Dateien angegeben, die ein ähnliches Format wie win.ini haben.
-   Ein unabhängiger Softwarehersteller (INDEPENDENT Software Vendor, ISV) kann eine DESIGN-Datei mit einem Produkt erstellen und verteilen.
-   In Versionen vor Windows Vista werden Designdateien auf der Registerkarte Design der Systemsteuerung Anzeigen angezeigt. In Windows Vista und höher werden Designs in der Systemsteuerung für die Personalisierung angezeigt.

Weitere Informationen zu DESIGN-Dateien finden Sie unter [Designdateiformat](themesfileformat-overview.md).

Ein visueller Stil ist eine Spezifikation, die die Darstellung der allgemeinen steuerelemente Windows definiert. Visuelle Stile sind Designs zugeordnet. Das heißt, eine DESIGN-Datei enthält einen Abschnitt, der den visuellen Stil angibt, der angewendet werden soll, wenn das bestimmte Design aktiv ist. Im Folgenden finden Sie einige Merkmale visueller Stile.

-   Benutzer können den visuellen Stil jederzeit ändern, indem sie ein anderes Design auswählen.
-   Sie müssen die API für visuelle Stile verwenden, um den derzeit aktiven visuellen Stil auf die benutzerdefinierten oder vom Besitzer gezeichneten Steuerelemente Ihrer Anwendung anzuwenden(sofern verfügbar).
-   Die Informationen, die einen visuellen Stil definieren, werden in einer MSSTYLES-Datei gespeichert. Microsoft unterstützt die Erstellung von MSSTYLES-Dateien nicht.


Die folgende Abbildung zeigt ein einfaches Dialogfeld mit einer Taskleiste auf einem Windows 7-Desktop, der das Design Windows Ohne Transparenz verwendet. Da die Anwendung nicht für die Verwendung visueller Stile konfiguriert ist, werden die Schaltflächen unabhängig von den Designeinstellungen gleich angezeigt.

![Screenshot eines Dialogfelds mit Schaltflächen, die keine Transparenz verwenden](images/tb-wostyles.png)

Im Gegensatz dazu zeigt die folgende Abbildung das gleiche Dialogfeld auf demselben Desktop, aber dieses Mal wurde die Anwendung für die Arbeit mit visuellen Stilen konfiguriert. Beachten Sie die unterschiedliche Darstellung der Schaltflächen im Clientbereich. Die Schaltflächen sehen anders aus, da das System die visuellen Stile angewendet hat, die im Design "Stil" definiert sind.

![Screenshot eines Dialogfelds mit Schaltflächen, die Transparenz verwenden](images/tb-withstyles.png)

Das folgende Beispiel zeigt ein ähnliches Dialogfeld auf einem Windows 8 Desktop. In Windows 8 sind visuelle Stile immer ein on, sodass Windows 8-Apps "kostenlos" erhalten.

![Screenshot eines einfachen Dialogfelds auf dem Windows 8-Desktop](images/tb-win8.png)

## <a name="visual-styles-components"></a>Komponenten visueller Stile

Visuelle Stile werden von den folgenden Komponenten unterstützt:

-   Version 6 oder höher der common control library (ComCtl32.dll)
-   Die api für visuelle Stile, die in UxTheme.dll
-   Designs-Dienst
-   Eine oder mehrere Visuelle Stildefinitionsdateien (MSSTYLES)

Die API für visuelle Stile ist von einem Systemdienst namens Designs abhängig. Die allgemeine Steuerelementbibliothek fragt den Themes-Dienst ab, um stilbezogene Informationen zu erhalten, und verwendet den Dienst bis Windows 7, um Steuerelemente im aktuellen visuellen Stil zu rendern.

In Windows 8 und höher funktioniert die API für visuelle Stile weiterhin, wenn der Dienst Designs deaktiviert ist. Dies bedeutet, dass die allgemeinen Steuerelemente und der Nicht-Clientbereich von Fenstern weiterhin visuelle Stile haben, wenn der Dienst Designs deaktiviert ist. Die Windows 8 Features, die weiterhin den Themes-Dienst erfordern, umfassen Folgendes:

-   Ändern des visuellen Stils, in der Regel über die **Personalisierungsseite** von **PC Einstellungen**.
-   Leistungsoptimierungen beim Wechseln von Benutzern, Abmelden, Herunterfahren und Freigeben über Benutzersitzungen hinweg.

Die API für visuelle Stile ruft Stilinformationen aus der MSSTYLES-Datei ab, die dem aktuell ausgewählten Design zugeordnet ist. Die MSSTYLES-Datei enthält eine Reihe von Metriken, Schriftarten, Farben und Bitmaps, die einen visuellen Stil definieren.

## <a name="application-requirements-for-supporting-visual-styles"></a>Anwendungsanforderungen für die Unterstützung visueller Stile

Um visuelle Stile verwenden zu können, muss Ihre Anwendung unter einem Betriebssystem ausgeführt werden, das ComCtl32.dll Version 6 oder höher enthält. Wenn Sie möchten, dass Ihre Anwendung ComCtl32.dll Version 6 verwendet, müssen Sie ein Anwendungsmanifest oder eine Compilerrichtlinie hinzufügen, um anzugeben, dass Version 6 verwendet werden soll, wenn sie verfügbar ist. Informationen zum Erstellen eines Anwendungsmanifests, mit dem Ihre Anwendung visuelle Stile verwenden kann, finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

Für allgemeine Steuerelemente ist keine weitere Aktion erforderlich, um sicherzustellen, dass die Steuerelemente im bevorzugten visuellen Stil des Benutzers angezeigt werden.

Wenn Ihre Anwendung benutzerdefinierte oder vom Besitzer gezeichnete Steuerelemente enthält, müssen Sie die API für visuelle Stile verwenden, um Informationen zum derzeit aktiven visuellen Stil abzurufen und die Steuerelemente in diesem Stil zu zeichnen.

Für Windows-Versionen vor Windows 8 müssen Anwendungen in der Regel zwei separate Codepfade zum Zeichnen von benutzerdefinierten und vom Besitzer gezeichneten Steuerelementen bereitstellen. Ein Codepfad zeichnet die Steuerelemente, wenn ein Design aktiv ist, das visuelle Stile verwendet, und ein anderer Codepfad zeichnet die Steuerelemente, wenn das Windows Classic-Design oder ein Design mit hohem Kontrast aktiv ist. In Windows 8 sind visuelle Stile jedoch immer ein on, sodass separate Codepfade zum Thema nicht erforderlich sind. Anwendungen, die sich für die Windows 8, erhalten "kostenlos" einen hohen Kontrast. Weitere Informationen finden Sie unter Supporting hoher Kontrast Themes (Unterstützen [hoher Kontrast Designs).](supporting-high-contrast-themes.md)

Weitere Informationen zu finden Sie unter Using Visual Styles with Custom and Owner-Drawn Controls and Visual Styles Reference (Verwenden von visuellen Stilen mit benutzerdefinierten und [Owner-Drawn-Steuerelementen](using-visual-styles.md) und Referenz [zu visuellen Stilen).](uxctl-ref.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Visuelle Stile](themes-overview.md)
</dt> </dl>

 

 




