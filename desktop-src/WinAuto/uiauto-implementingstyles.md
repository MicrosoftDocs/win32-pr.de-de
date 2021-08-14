---
title: Stilsteuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von IStylesProvider, einschließlich Informationen zu Eigenschaften und Methoden. Das Steuerelementmuster Stile wird verwendet, um ein Benutzeroberflächenelement zu beschreiben, das über einen bestimmten Stil, eine bestimmte Füllfarbe, ein bestimmtes Füllmuster oder eine bestimmte Form verfügt.
ms.assetid: 65125E07-70D4-48E5-B18D-E9D66ABC6FC0
keywords:
- Benutzeroberflächenautomatisierung,Implementieren von Stilsteuerelementmustern
- Benutzeroberflächenautomatisierung,Stilsteuerelementmuster
- Benutzeroberflächenautomatisierung,IStylesProvider
- IStylesProvider
- Implementieren Benutzeroberflächenautomatisierung Formatvorlagen-Steuerelementmusters
- Stilsteuerelementmuster
- Steuerelementmuster,IStylesProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung Stile
- Steuerelementmuster,Stile
- interfaces,IStylesProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66e52a6829e592cc659d5ce47b51a09b6d8910d4bd2c41a1e03c9b661d027fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324088"
---
# <a name="styles-control-pattern"></a>Stilsteuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung von [**IStylesProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider)einschließlich Informationen zu Eigenschaften und Methoden. Das **Steuerelementmuster Stile** wird verwendet, um ein Benutzeroberflächenelement zu beschreiben, das über einen bestimmten Stil, eine bestimmte Füllfarbe, ein bestimmtes Füllmuster oder eine bestimmte Form verfügt.

Das  Stilsteuerelementmuster ist besonders nützlich, um Elemente in einem Dokument zu beschreiben, die häufig solche Stile aufweisen. Stile enthalten in der Regel Informationen, die für Kunden mit Behinderungen nützlich sind. Beispielsweise kann ein Stil eine bestimmte Zeichenfolge als Titel eines Dokuments oder ein bestimmtes Flussdiagrammobjekt als Raute oder Kreis beschreiben. Beispiele für Steuerelemente, die dieses Steuerelementmuster implementieren, finden Sie unter [Steuerelementtypen und deren unterstützte Steuerelementmuster.](uiauto-controlpatternmapping.md)

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IStylesProvider**](#required-members-for-istylesprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie  beim Implementieren des Stilsteuerelementmusters die folgenden Richtlinien und Konventionen:

-   Die Headerdatei UIAutomationClient.h definiert einen Satz benannter konstanter Werte, mit denen mehrere gängige Stile identifiziert werden. Weitere Informationen finden Sie unter [**Formatbezeichner.**](uiauto-style-identifiers.md)
-   Wenn Sie [**StyleId \_ Custom**](uiauto-style-identifiers.md)verwenden, müssen Sie die [**IStylesProvider::StyleName-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) implementieren, damit Clients den Namen des Stils ermitteln können. Sie müssen die **StyleName-Eigenschaft** nicht für einen Standardstil implementieren, da Microsoft Benutzeroberflächenautomatisierung einen Standardnamen bereitstellt. Sie können sie jedoch implementieren, wenn Sie den Standardnamen überschreiben müssen.
-   Die anderen Eigenschaften im **Stilmuster** sind optional. der Anbieter kann [**UIA \_ E \_ NOTSUPPORTED**](uiauto-error-codes.md) für eine Eigenschaft zurückgeben, die nicht unterstützt wird.
-   Stile in einem Textbereich können durch die folgenden Textattribute dargestellt werden:
    -   Wenn auf eine Anforderung für das Textattribut [**StyleId**](uiauto-textattribute-ids.md) reagiert wird, sollte der Textbereich einen der in [**Formatbezeichner beschriebenen**](uiauto-style-identifiers.md)Formatbezeichner zurückgeben.
    -   Wenn [**StyleId \_ Custom**](uiauto-style-identifiers.md) verwendet wird, sollte der Textbereich einen Zeichenfolgenwert für das Textattribut [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) zurückgeben, damit Clients den Stilnamen ermitteln können.
    -   Ein Textbereich, der mehrere Stile aufweist, z. B. Überschrift und normaler Text, sollte die spezielle Benutzeroberflächenautomatisierung [**ReservedMixedAttributeValue-Eigenschaft**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) sowohl für die [**StyleId-**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid) als auch für die [**StyleName-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) zurückgeben. Ein Client, der diese Antwort empfängt, kann den Textbereich unterteilen, um zu ermitteln, wo die Stile beginnen und enden.
-   Anwendungen können eine Vielzahl von Stilen verwenden, um Objekte zu beschreiben, aber Benutzeroberflächenautomatisierung stellt nur die gängigsten dar. Um zusätzliche Stilattribute darzustellen, z. B. Rahmenfarbe, kann ein Anbieter eine Liste zusätzlicher Attribute in der [**ExtendedProperties-Eigenschaft**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) zurückgeben. Dies ist im Grunde ein Eigenschaftenbehälter mit einer Reihe erweiterter Eigenschaften, z. B. "BorderColor=0xFF0000; BorderStyle=dotted". Die Werte erweiterter Eigenschaften können anwendungsspezifisch sein.

## <a name="required-members-for-istylesprovider"></a>Erforderliche Member für **IStylesProvider**

Die folgenden Eigenschaften sind für die Implementierung der [**IStylesProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider) erforderlich.



| Erforderliche Member                                                            | Memberart | Hinweise |
|-----------------------------------------------------------------------------|-------------|-------|
| [**Extendedproperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) | Eigenschaft    | Keine  |
| [**Fillcolor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillcolor)                       | Eigenschaft    | Keine  |
| [**FillPatternColor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatterncolor)         | Eigenschaft    | Keine  |
| [**FillPatternStyle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatternstyle)         | Eigenschaft    | Keine  |
| [**Formen**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_shape)                               | Eigenschaft    | Keine  |
| [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid)                           | Eigenschaft    | Keine  |
| [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename)                       | Eigenschaft    | Keine  |



 

Diesem Steuerelementmuster sind keine Methoden oder Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und deren unterstützte Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 