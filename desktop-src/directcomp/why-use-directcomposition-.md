---
title: Gründe für die Verwendung von directcomposition
description: In diesem Thema werden die Funktionen und Vorteile von Microsoft directcomposition beschrieben.
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- Gründe für die Verwendung von directcomposition
- Gründe für die Verwendung von directcomposition
- Directcomposition-Funktionen und-Vorteile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ad68f779abc023b7645ed9e66f8af3bf63a140
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340520"
---
# <a name="why-use-directcomposition"></a>Gründe für die Verwendung von directcomposition

> [!NOTE]
> Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen. Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

In diesem Thema werden die Funktionen und Vorteile von Microsoft directcomposition beschrieben. Sie enthält die folgenden Abschnitte:

-   [Erstellen einer visuell ansprechenden Benutzeroberfläche](#create-a-visually-engaging-user-interface)
-   [Umfassende, reibungslose Animationen für Ihre Anwendung aktivieren](#enable-rich-smooth-animations-for-your-application)
-   [Kombinieren von Bitmaps aus einer Vielzahl von Quellen](#combine-bitmaps-from-a-variety-of-sources)
-   [Speicher Einsparungen bei der Integration in DWM](#memory-savings-though-integration-with-dwm)
-   [Behalten Sie, was Sie bereits haben](#keep-what-you-already-have)
-   [Zugehörige Themen](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a>Erstellen einer visuell ansprechenden Benutzeroberfläche

Mithilfe von directcomposition können Sie [*visuelle*](directcomposition-glossary.md) Elemente kombinieren und animieren, um eine visuell ansprechende Benutzeroberfläche für Ihre Windows-basierten Anwendungen zu erstellen. Es kann Ihnen helfen, Ihre Anwendung zu einem eindeutigen Aussehen und Gefühl zu machen, indem Sie eine Identität einrichten, die Sie von anderen Anwendungen unterscheidet.

Directcomposition kann auch helfen, die Verwendung Ihrer Anwendungen zu vereinfachen. Beispielsweise kannst du damit visuelle Hinweise und animierte Bildschirmübergänge erzeugen, die die Beziehungen zwischen Elementen auf dem Bildschirm verdeutlichen.

## <a name="enable-rich-smooth-animations-for-your-application"></a>Umfassende, reibungslose Animationen für Ihre Anwendung aktivieren

Directcomposition ist eine hochleistungsfähige Bitmap-Kompositions-Engine, die hardwarebeschleunigte Grafiken verwendet, um hohe Frameraten zu erzielen. Dies führt zu Smooth-und konsistenten schwenken, scrollen und Animationen komplexer Inhalte. Da es auf einem dedizierten Thread funktioniert, der von dem Thread getrennt ist, der zum Renderns der Anwendungs Benutzeroberfläche verwendet wird, kann directcomposition den UI-Thread niemals "verhungern" oder die Fähigkeit der Anwendung beeinträchtigen, seine Benutzeroberflächen Elemente zu zeichnen.

## <a name="combine-bitmaps-from-a-variety-of-sources"></a>Kombinieren von Bitmaps aus einer Vielzahl von Quellen

Viele Windows-basierte Anwendungen verfügen über eine Benutzeroberfläche, die aus Elementen besteht, die von verschiedenen Grafik Frameworks erstellt werden. Eine Anwendung kann z. b. Windows Forms zum Erstellen einer Statusleiste, Windows Graphics Device Interface (GDI) zum Erstellen der Hauptfenster Inhalte, Microsoft DirectX für Grafik Inhalte usw. verwenden. Directcomposition ermöglicht es Ihnen, den Inhalt aus einer Vielzahl von Grafik Frameworks zu kombinieren und ihn im gleichen oberen oder untergeordneten Fenster zu rendernieren, ohne sich Gedanken darüber machen zu müssen, was geschieht, wenn sich der Inhalt von verschiedenen Frameworks überschneidet.

## <a name="memory-savings-though-integration-with-dwm"></a>Speicher Einsparungen bei der Integration in DWM

Die von directcomposition erstellten Kompositionen und Animationen werden an eine integrierte Komponente von Windows mit dem Namen [Desktopfenster-Manager (DWM)](/windows/desktop/dwm/dwm-overview) für das Rendering auf dem Bildschirm übermittelt. Daher sind keine besonderen renderingkomponenten oder Benutzeroberflächen-Frameworks auf dem Computer erforderlich.

## <a name="keep-what-you-already-have"></a>Behalten Sie, was Sie bereits haben

Der UI-Code in einer vorhandenen Windows-basierten Anwendung stellt eine bedeutende Investition dar. Zum größten Teil können Sie mit directcomposition vorhandene Inhalte der Benutzeroberfläche verfassen und animieren. Dies bedeutet, dass Sie directcomposition verwenden können, um wichtige Aktualisierungen und Verbesserungen an der Benutzeroberfläche Ihrer Anwendung vorzunehmen, ohne umfassende Änderungen an der vorhandenen UI-Codebasis vornehmen zu müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectComposition](directcomposition-portal.md)
</dt> </dl>

 

 