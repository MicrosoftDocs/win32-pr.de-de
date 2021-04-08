---
title: Textchild-Steuerelement Muster
description: Führt Richtlinien und Konventionen zum Implementieren von itextchildprovider ein, einschließlich Informationen zu Eigenschaften und Methoden. Das textchild-Steuerelement Muster wird verwendet, um auf den nächsten Vorgänger eines Elements zuzugreifen, der das Text-Steuerelement Muster unterstützt.
ms.assetid: B33BCBEF-9AD2-4A5A-871E-E97E69BE8195
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines textchild-Steuerelement Musters
- UI-Automatisierung, textchild-Steuerelement Muster
- UI-Automatisierung, itextchildprovider
- ITextChildProvider
- Implementieren von textchild-Steuerelement Mustern für Benutzeroberflächen Automatisierung
- Textchild-Steuerelement Muster
- Steuerelement Muster, itextchildprovider
- Steuerelement Muster, Implementieren von Benutzeroberflächen Automatisierung-textchild
- Steuerelement Muster, textchild
- Schnittstellen, itextchildprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21102abfef7cee0553850ac01c4f759f81988e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729953"
---
# <a name="textchild-control-pattern"></a>Textchild-Steuerelement Muster

Führt Richtlinien und Konventionen zum Implementieren von [**itextchildprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider)ein, einschließlich Informationen zu Eigenschaften und Methoden. Das **textchild** -Steuerelement Muster wird verwendet, um auf den nächsten Vorgänger eines Elements zuzugreifen, der das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster unterstützt.

Angenommen, Text in einem Dokument enthält ein eingebettetes Bild und einen Hyperlink, wie in der folgenden Abbildung dargestellt.

![Screenshot mit Text, der ein eingebettetes Bild und einen Hyperlink enthält](images/textchild-pattern.png)

Wenn Sie Microsoft UI Automation-Tools verwenden, um die Benutzeroberflächenautomatisierungs-Struktur für diesen Dokumentinhalt zu überprüfen, wird möglicherweise ein Dokument Element mit einem untergeordneten Element angezeigt, das das Bild darstellt, und ein weiteres untergeordnetes Element, das den Hyperlink darstellt Beispiel:

![Screenshot, der zeigt, wie Sie eine Beispiel-UI-Automatisierungs Elementstruktur melden](images/textchild-pattern-tree.png)

In der Regel unterstützt das Document-Element im vorangehenden Beispiel das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster, die beiden untergeordneten Elemente des Document-Elements jedoch nicht. Wenn eine Benutzeroberflächenautomatisierungs-Client Anwendung über einen Verweis auf das Bildelement-oder Hyperlink-Element verfügt, kann der Client das **textchild** -Steuerelement Muster als bequeme Methode zum Zugreifen auf das TextControl-Muster verwenden, das vom enthaltenden Dokument Element verfügbar gemacht wird.

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren der [**itextchildprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) -Schnittstelle die folgenden Richtlinien und Konventionen:

-   Die [**itextchildprovider:: Text Container**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) -Eigenschaft sollte das nächste Vorgänger Element angeben, das die [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) -Schnittstelle unterstützt, unabhängig davon, ob auch Elemente in der Vorgänger Kette **ITextProvider** unterstützen.
-   Ein Element sollte nicht sowohl die [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) -als auch die [itextchildprovider * *](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) -Schnittstelle unterstützen.
- Ein Element, das [**itextchildprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) implementiert, muss ein untergeordnetes Element oder ein Nachfolger Element eines Elements sein, das [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider)implementiert. Es ist nicht erforderlich, dass dieses Element auch das [Text-Steuerelement Muster](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange)implementiert.
-   Die [**itextchildprovider:: TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) -Eigenschaft sollte denselben Textbereich angeben, den das enthaltende Text Anbieter Element zurückgibt, wenn die zugehörige [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) -Funktion mit dem untergeordneten Text-Element als eingeschlossenes untergeordnetes Element aufgerufen wird.

## <a name="required-members-for-itextchildprovider"></a>Erforderliche Member für **itextchildprovider**

Diese Eigenschaften und Methoden sind für die Implementierung der [**itextchildprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                     | Memberart | Hinweise |
|----------------------------------------------------------------------|-------------|-------|
| [**Text Container**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | Eigenschaft    | Keine  |
| [**TextRange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | Eigenschaft    | Keine  |



 

Diesem Steuerelementmuster sind keine Methoden oder Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

**Licher**

- [Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
- [Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
- [Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)