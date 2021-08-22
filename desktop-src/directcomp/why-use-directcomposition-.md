---
title: Gründe für die Verwendung von DirectComposition
description: In diesem Thema werden die Funktionen und Vorteile von Microsoft DirectComposition beschrieben.
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- Gründe für die Verwendung von DirectComposition
- Gründe für die Verwendung von DirectComposition
- DirectComposition-Funktionen und -Vorteile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe9b67b17869c53b393d8a1f1ecb6230a69322d898f691c21370a5b24befda21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562090"
---
# <a name="why-use-directcomposition"></a>Gründe für die Verwendung von DirectComposition

> [!NOTE]
> Für Apps auf Windows 10 empfehlen wir die Verwendung von Windows.UI.Composition-APIs anstelle von DirectComposition. Weitere Informationen finden Sie unter [Modernisieren Ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

In diesem Thema werden die Funktionen und Vorteile von Microsoft DirectComposition beschrieben. Sie enthält die folgenden Abschnitte:

-   [Erstellen einer visuell ansprechenden Benutzeroberfläche](#create-a-visually-engaging-user-interface)
-   [Aktivieren umfangreicher, reibungsloser Animationen für Ihre Anwendung](#enable-rich-smooth-animations-for-your-application)
-   [Kombinieren von Bitmaps aus einer Vielzahl von Quellen](#combine-bitmaps-from-a-variety-of-sources)
-   [Arbeitsspeichereinsparung durch Integration in DWM](#memory-savings-though-integration-with-dwm)
-   [Behalten Sie das, was Sie bereits haben.](#keep-what-you-already-have)
-   [Zugehörige Themen](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a>Erstellen einer visuell ansprechenden Benutzeroberfläche

Mit DirectComposition können Sie [*Visuals*](directcomposition-glossary.md) kombinieren und animieren, um eine visuell ansprechende Benutzeroberfläche für Ihre Windows-basierten Anwendungen zu erstellen. Dies kann dazu beitragen, Ihrer Anwendung ein einzigartiges Aussehen und Gefühl zu verleihen, indem eine Identität festgelegt wird, die sie von anderen Anwendungen unterscheidet.

DirectComposition kann auch die Verwendung Ihrer Anwendungen vereinfachen. Beispielsweise kannst du damit visuelle Hinweise und animierte Bildschirmübergänge erzeugen, die die Beziehungen zwischen Elementen auf dem Bildschirm verdeutlichen.

## <a name="enable-rich-smooth-animations-for-your-application"></a>Aktivieren umfangreicher, reibungsloser Animationen für Ihre Anwendung

DirectComposition ist eine Hochleistungs-Bitmapkompositions-Engine, die hardwarebeschleunigte Grafiken verwendet, um hohe Frameraten zu erzielen, was zu einem reibungslosen und konsistenten Schwenken, Scrollen und Animationen komplexer Inhalte führt. Da er auf einem dedizierten Thread arbeitet, der vom Thread zum Rendern der Anwendungsbenutzeroberfläche getrennt ist, kann DirectComposition den UI-Thread nie "verhungern" oder die Fähigkeit der Anwendung beeinträchtigen, ihre Benutzeroberflächenelemente zu zeichnen.

## <a name="combine-bitmaps-from-a-variety-of-sources"></a>Kombinieren von Bitmaps aus einer Vielzahl von Quellen

Viele Windows-basierten Anwendungen verfügen über eine Benutzeroberfläche, die aus Elementen besteht, die von einer Vielzahl verschiedener Grafikframeworks erstellt wurden. Beispielsweise kann eine Anwendung Windows Forms verwenden, um eine Statusleiste zu erstellen, Windows Graphics Device Interface (GDI) zum Erstellen des Hauptfensterinhalts, Microsoft DirectX für Grafikinhalte usw. DirectComposition ermöglicht es Ihnen, den Inhalt aus einer Vielzahl von Grafikframeworks zu kombinieren und in demselben übergeordneten oder untergeordneten Fenster zu rendern, ohne sich Gedanken darüber machen zu müssen, was geschieht, wenn sich der Inhalt aus verschiedenen Frameworks überschneidet.

## <a name="memory-savings-though-integration-with-dwm"></a>Arbeitsspeichereinsparung durch Integration in DWM

Kompositionen und Animationen, die von DirectComposition erstellt wurden, werden an eine integrierte Komponente von Windows übergeben, die [als Desktopfenster-Manager (DWM)](/windows/desktop/dwm/dwm-overview) zum Rendern auf dem Bildschirm bezeichnet wird. Daher sind keine speziellen Renderingkomponenten oder Benutzeroberflächenframeworks auf dem Computer erforderlich.

## <a name="keep-what-you-already-have"></a>Behalten Sie das, was Sie bereits haben.

Der Benutzeroberflächencode in einer vorhandenen Windows-basierten Anwendung stellt eine erhebliche Investition dar. In den meisten Teilen können Sie mit DirectComposition Ihre vorhandenen Benutzeroberflächeninhalte erstellen und animieren. Dies bedeutet, dass Sie DirectComposition verwenden können, um wichtige Updates und Verbesserungen an ihrer Anwendungsbenutzeroberfläche vorzunehmen, ohne umfangreiche Änderungen an der vorhandenen Codebasis der Benutzeroberfläche vornehmen zu müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectComposition](directcomposition-portal.md)
</dt> </dl>

 

 