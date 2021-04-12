---
title: Übersicht über visuelle Stile
description: Dieses Thema beschreibt visuelle Stile und identifiziert die Windows-Komponenten, die diese unterstützen. Außerdem werden die Schritte erläutert, die Sie ausführen müssen, um visuelle Stile in Ihren Anwendungen zu verwenden.
ms.assetid: 5B5D7BB6-684F-478D-BF5F-B8D18BBCFF2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5663730c752fbf16c4f229a031eafa0c65bb9dbb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474668"
---
# <a name="visual-styles-overview"></a>Übersicht über visuelle Stile

Dieses Thema beschreibt visuelle Stile und identifiziert die Windows-Komponenten, die diese unterstützen. Außerdem werden die Schritte erläutert, die Sie ausführen müssen, um visuelle Stile in Ihren Anwendungen zu verwenden. Dieses Thema enthält die folgenden Abschnitte:

-   [Themes and Visual Styles](#themes-and-visual-styles)
-   [Komponenten von visuellen Stilen](#visual-styles-components)
-   [Anwendungsanforderungen für die Unterstützung visueller Stile](#application-requirements-for-supporting-visual-styles)
-   [Zugehörige Themen](#related-topics)

## <a name="themes-and-visual-styles"></a>Themes and Visual Styles

Windows umfasst mehrere Features, mit denen Benutzer die Benutzeroberfläche anpassen können, um Ihren individuellen Anforderungen und Vorlieben gerecht zu werden. Zu diesen Features gehören Designs, die in Microsoft pluseingeführt wurden. für Windows 95. Ein Design ist eine vom Benutzer auswählbare Auflistung von Einstellungen, die Hintergrundbild, Cursor, Schriftarten, Sounds und Symbole enthält. Im folgenden finden Sie einige Merkmale von Designs.

-   Design-Einstellungen werden in. Design-Dateien angegeben, die über ein ähnliches Format wie win.ini-Dateien verfügen.
-   Ein unabhängiger Softwarehersteller (Independent Software Vendor, ISV) kann eine. Theme-Datei mit einem Produkt erstellen und verteilen.
-   In früheren Versionen als Windows Vista werden Designdateien auf der Registerkarte Design der Systemsteuerung angezeigt. In Windows Vista und höher werden Designs in der Personalisierungs-Systemsteuerung angezeigt.

Weitere Informationen zu. Theme-Dateien finden Sie unter Design [File Format](themesfileformat-overview.md).

Ein visueller Stil ist eine Spezifikation, die die Darstellung der allgemeinen Windows-Steuerelemente definiert. Visuelle Stile sind Designs zugeordnet. Das heißt, eine. Theme-Datei enthält einen Abschnitt, der den visuellen Stil angibt, der angewendet werden soll, wenn das jeweilige Design aktiv ist. Im folgenden finden Sie einige Merkmale von visuellen Stilen.

-   Benutzer können den visuellen Stil jederzeit ändern, indem Sie ein anderes Design auswählen.
-   Sie müssen die Visualisierungs Stile-API verwenden, um den derzeit aktiven visuellen Stil auf die benutzerdefinierten oder vom Besitzer gezeichneten Steuerelemente der Anwendung anzuwenden.
-   Die Informationen, die einen visuellen Stil definieren, werden in einer msstyles-Datei gespeichert. Die Erstellung von msstyles-Dateien wird von Microsoft nicht unterstützt.


Die folgende Abbildung zeigt ein einfaches Dialogfeld mit einer Taskleiste auf einem Windows 7-Desktop, der das Windows Aero-Design ohne Transparenz verwendet. Da die Anwendung nicht für die Verwendung visueller Stile konfiguriert ist, werden die Schaltflächen unabhängig von den Design Einstellungen unverändert angezeigt.

![Screenshot eines Dialog Felds mit Schaltflächen, die keine Transparenz verwenden](images/tb-wostyles.png)

Im Gegensatz dazu wird in der folgenden Abbildung das gleiche Dialogfeld auf demselben Desktop angezeigt, aber dieses Mal wurde die Anwendung für die Arbeit mit visuellen Stilen konfiguriert. Beachten Sie die unterschiedliche Darstellung der Schaltflächen im Client Bereich. Die Schaltflächen sehen anders aus, da das System die visuellen Stile angewendet hat, die im Aero-Design definiert sind.

![Screenshot eines Dialog Felds mit Schaltflächen, die Transparenz verwenden](images/tb-withstyles.png)

Das folgende Beispiel zeigt ein ähnliches Dialogfeld auf einem Windows 8-Desktop. In Windows 8 sind visuelle Stile immer eingeschaltet, sodass Windows 8-Apps "kostenlos" werden.

![Screenshot eines einfachen Dialog Felds auf dem Windows 8-Desktop](images/tb-win8.png)

## <a name="visual-styles-components"></a>Komponenten von visuellen Stilen

Visuelle Stile werden von den folgenden Komponenten unterstützt:

-   Version 6 oder höher der allgemeinen Steuerelement Bibliothek (ComCtl32.dll)
-   Die in UxTheme.dll implementierte Visual Styles-API
-   Design Dienst
-   Mindestens eine visuelle Stil Definitionsdatei (. msstyles)

Die API für visuelle Stile hängt von einem Systemdienst mit dem Namen "Designs" ab. Die allgemeine Steuerelement Bibliothek fragt den Designs-Dienst ab, um Stil bezogene Informationen zu erhalten, und verwendet den Dienst, um die Steuerelemente im aktuellen visuellen Stil mithilfe von Windows 7 zu Rendering.

In Windows 8 und höher funktioniert die API für visuelle Stile weiterhin, wenn der Designs-Dienst deaktiviert ist. Dies bedeutet, dass die allgemeinen Steuerelemente und der nicht-Client Bereich von Fenstern weiterhin visuelle Stile aufweisen, wenn der Designs-Dienst deaktiviert ist. Die Windows 8-Features, für die weiterhin der Designs-Dienst erforderlich ist, sind:

-   Ändern des visuellen Stils, in der Regel über die **Personalisierungs** Seite der **PC-Einstellungen**.
-   Leistungsoptimierungen bei der Umstellung von Benutzern, abmelden, Herunterfahren und Freigeben von Benutzersitzungen.

Die API für visuelle Stile ruft Stil Informationen aus der msstyles-Datei ab, die dem aktuell ausgewählten Design zugeordnet ist. Die msstyles-Datei enthält einen Satz von Metriken, Schriftarten, Farben und Bitmaps, die einen visuellen Stil definieren.

## <a name="application-requirements-for-supporting-visual-styles"></a>Anwendungsanforderungen für die Unterstützung visueller Stile

Um visuelle Stile zu verwenden, muss die Anwendung unter einem Betriebssystem ausgeführt werden, das ComCtl32.dll Version 6 oder höher enthält. Wenn Sie möchten, dass Ihre Anwendung ComCtl32.dll Version 6 verwendet, müssen Sie ein Anwendungs Manifest oder eine Compilerdirektive hinzufügen, um anzugeben, dass Version 6 verwendet werden soll, wenn Sie verfügbar ist. Informationen zum Erstellen eines Anwendungs Manifests, mit dem Ihre Anwendung visuelle Stile verwenden kann, finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

Für allgemeine Steuerelemente ist keine weitere Aktion erforderlich, um sicherzustellen, dass die Steuerelemente im bevorzugten visuellen Stil des Benutzers angezeigt werden.

Wenn Ihre Anwendung benutzerdefinierte oder vom Besitzer gezeichnete Steuerelemente enthält, müssen Sie die Visualisierungs Stile-API verwenden, um Informationen über den momentan aktiven visuellen Stil abzurufen und die Steuerelemente in diesem Stil zu zeichnen.

Bei Windows-Versionen vor Windows 8 müssen Anwendungen in der Regel zwei separate Codepfade zum Zeichnen von benutzerdefinierten und vom Besitzer gezeichneten Steuerelementen bereitstellen. Ein Codepfad zeichnet die Steuerelemente, wenn ein Design, das visuelle Stile verwendet, aktiv ist, und ein anderer Codepfad die Steuerelemente zeichnet, wenn das klassische Windows-Design oder ein Design mit hohem Kontrast aktiv ist. In Windows 8 sind visuelle Stile jedoch immer eingeschaltet, sodass getrennte Code Pfade nicht benötigt werden. Anwendungen, die sich für Windows 8 manifestieren, erhalten eine hohe Kontrast "kostenlos". Weitere Informationen finden Sie [unter unterstützen von hoher Kontrast](supporting-high-contrast-themes.md)Designs.

Weitere Informationen zu finden Sie unter [Verwenden von visuellen Stilen mit benutzerdefinierten Steuerelementen und Owner-Drawn Steuerelementen](using-visual-styles.md) und [visueller Stile-Referenz](uxctl-ref.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Visuelle Stile](themes-overview.md)
</dt> </dl>

 

 




