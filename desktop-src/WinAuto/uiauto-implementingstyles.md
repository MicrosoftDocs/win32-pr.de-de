---
title: Stile-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von istylesprovider, einschließlich Informationen zu Eigenschaften und Methoden. Das Stile-Steuerelement Muster wird verwendet, um ein UI-Element zu beschreiben, das einen bestimmten Stil, eine bestimmte Füllfarbe, ein Füllmuster oder eine Form aufweist.
ms.assetid: 65125E07-70D4-48E5-B18D-E9D66ABC6FC0
keywords:
- UI-Automatisierung, Implementieren von Stile-Steuerelement Mustern
- UI-Automatisierung, Stile-Steuerelement Muster
- UI-Automatisierung, istylesprovider
- IStylesProvider
- Implementieren des Steuerelement Musters der Benutzeroberflächen Automatisierung
- Stile-Steuerelement Muster
- Steuerelement Muster, istylesprovider
- Steuerelement Muster, Implementieren von Benutzeroberflächenautomatisierungs-Stilen
- Steuerelement Muster, Stile
- Schnittstellen, istylesprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 611e2f1979aaa4744ce3ff39965053f63399b2b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729601"
---
# <a name="styles-control-pattern"></a>Stile-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**istylesprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider), einschließlich Informationen zu Eigenschaften und Methoden. Das **Stile** -Steuerelement Muster wird verwendet, um ein UI-Element zu beschreiben, das einen bestimmten Stil, eine bestimmte Füllfarbe, ein Füllmuster oder eine Form aufweist.

Das **Stile** -Steuerelement Muster ist besonders nützlich für das Beschreiben von Elementen in einem Dokument, die häufig über solche Stile verfügen. Stile enthalten in der Regel Informationen, die für Kunden mit Behinderungen nützlich sind. ein Stil kann z. b. eine bestimmte Zeichenfolge als Titel eines Dokuments oder ein bestimmtes Flussdiagramm Objekt als Diamant oder Kreis beschreiben. Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **istylesprovider**](#required-members-for-istylesprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **Stile** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Die UIAutomationClient. h-Header Datei definiert einen Satz benannter konstanter Werte, mit denen verschiedene gängige Stile identifiziert werden. Weitere Informationen finden Sie unter [](uiauto-style-identifiers.md)Format Bezeichner.
-   Wenn Sie [**styleId \_ Custom**](uiauto-style-identifiers.md)verwenden, müssen Sie die [**istylesprovider:: styleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) -Eigenschaft implementieren, damit Clients den Namen des Stils ermitteln können. Sie müssen die **styleName** -Eigenschaft für einen Standardstil nicht implementieren, da die Microsoft-Benutzeroberflächen Automatisierung einen Standardnamen bereitstellt. Sie können Sie jedoch implementieren, wenn Sie den Standardnamen überschreiben müssen.
-   Die anderen Eigenschaften im **Stile** -Muster sind optional. der Anbieter kann [**UIA \_ E \_ NotSupported**](uiauto-error-codes.md) für eine Eigenschaft zurückgeben, die nicht unterstützt wird.
-   Stile in einem Textbereich können durch die folgenden Text Attribute dargestellt werden:
    -   Wenn Sie auf eine Anforderung für das [**styleId**](uiauto-textattribute-ids.md) -Text Attribut reagieren, sollte der Textbereich einen der im [**Stil**](uiauto-style-identifiers.md)Bezeichner beschriebenen Format Bezeichner zurückgeben.
    -   Wenn [**styleId \_ Custom**](uiauto-style-identifiers.md) verwendet wird, sollte der Textbereich einen Zeichen folgen Wert für das Attribut " [**styleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) Text" zurückgeben, damit Clients den Format Namen ermitteln können.
    -   Ein Textbereich, der über mehrere Stile verfügt, z. b. sowohl Überschrift und normaler Text, sollte die besondere Benutzeroberflächenautomatisierungs- [**reservedmixedattributevalue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) -Eigenschaft für die Eigenschaften [**styleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid) und [**styleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) zurückgeben. Ein Client, der diese Antwort empfängt, kann den Textbereich unterteilen, um zu ermitteln, wo die Stile beginnen und enden.
-   Anwendungen können eine Vielzahl von Stilen verwenden, um Objekte zu beschreiben, aber die Benutzeroberflächen Automatisierung stellt nur die gängigsten dar. Um zusätzliche Stil Attribute darzustellen, wie z. b. die Rahmenfarbe, kann ein Anbieter eine Liste zusätzlicher Attribute in der [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) -Eigenschaft zurückgeben. Dabei handelt es sich im Grunde um einen Eigenschaften Behälter mit einer Reihe erweiterter Eigenschaften, z. b. "BorderColor = 0xFF0000; BorderStyle = gepunktete ". Die Werte erweiterter Eigenschaften können anwendungsspezifisch sein.

## <a name="required-members-for-istylesprovider"></a>Erforderliche Member für **istylesprovider**

Die folgenden Eigenschaften sind erforderlich, um die [**istylesprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider) -Schnittstelle zu implementieren.



| Erforderliche Member                                                            | Memberart | Hinweise |
|-----------------------------------------------------------------------------|-------------|-------|
| [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) | Eigenschaft    | Keine  |
| [**FillColor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillcolor)                       | Eigenschaft    | Keine  |
| [**Fillpatterncolor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatterncolor)         | Eigenschaft    | Keine  |
| [**Fillpatternstyle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatternstyle)         | Eigenschaft    | Keine  |
| [**Form**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_shape)                               | Eigenschaft    | Keine  |
| [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid)                           | Eigenschaft    | Keine  |
| [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename)                       | Eigenschaft    | Keine  |



 

Diesem Steuerelementmuster sind keine Methoden oder Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 