---
title: TextChild-Steuerelementmuster
description: Führt Richtlinien und Konventionen für die Implementierung von ITextChildProvider ein, einschließlich Informationen zu Eigenschaften und Methoden. Das TextChild-Steuerelementmuster wird verwendet, um auf den nächsten Vorgänger eines Elements zu zugreifen, der das Text-Steuerelementmuster unterstützt.
ms.assetid: B33BCBEF-9AD2-4A5A-871E-E97E69BE8195
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des TextChild-Steuerelementmusters
- Benutzeroberflächenautomatisierung,TextChild-Steuerelementmuster
- Benutzeroberflächenautomatisierung,ITextChildProvider
- ITextChildProvider
- Implementieren Benutzeroberflächenautomatisierung TextChild-Steuerelementmustern
- TextChild-Steuerelementmuster
- Steuerelementmuster,ITextChildProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung TextChild
- Steuerelementmuster,TextChild
- interfaces,ITextChildProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5c7bfb1852a02efc7baa789e137a4c05e2c2e85a65606109b26a622dfafcf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929041"
---
# <a name="textchild-control-pattern"></a>TextChild-Steuerelementmuster

Führt Richtlinien und Konventionen für die Implementierung [**von ITextChildProvider ein,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider)einschließlich Informationen zu Eigenschaften und Methoden. Das **TextChild-Steuerelementmuster** wird verwendet, um auf den nächsten Vorgänger eines Elements zu zugreifen, der das [Text-Steuerelementmuster](uiauto-implementingtextandtextrange.md) unterstützt.

Angenommen, text in einem Dokument enthält ein eingebettetes Bild und einen Link, wie in der folgenden Abbildung dargestellt.

![Screenshot mit Text, der ein eingebettetes Bild und einen Link enthält](images/textchild-pattern.png)

Wenn Sie microsoft Benutzeroberflächenautomatisierung-Tools verwenden, um die Benutzeroberflächenautomatisierung-Struktur für diesen Dokumentinhalt zu untersuchen, wird möglicherweise ein Dokumentelement mit einem untergeordneten Element angezeigt, das das Bild darstellt, und einem anderen untergeordneten Element, das den Link darstellt. Beispiel:

![Screenshot: Überprüfen der Berichterstellung einer Beispielelementstruktur für die Benutzeroberflächenautomatisierung](images/textchild-pattern-tree.png)

In der Regel unterstützt das Dokumentelement [](uiauto-implementingtextandtextrange.md) im vorherigen Beispiel das Text-Steuerelementmuster, die beiden unteren Elemente des Dokumentelements jedoch nicht. Wenn eine Benutzeroberflächenautomatisierung-Clientanwendung über einen Verweis auf das Bildelement oder Linkelement verfügt, kann der Client das **TextChild-Steuerelementmuster** als bequeme Möglichkeit für den Zugriff auf das Textcontrol-Muster verwenden, das vom enthaltenden Dokumentelement verfügbar gemacht wird.

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim [**Implementieren der ITextChildProvider-Schnittstelle**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) die folgenden Richtlinien und Konventionen:

-   Die [**ITextChildProvider::TextContainer-Eigenschaft**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) sollte das nächste Vorgängerelement angeben, das die [**ITextProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) unterstützt, unabhängig davon, ob Elemente, die sich weiter in der Vorgängerkette befinden, **auch ITextProvider unterstützen.**
-   Ein Element sollte nicht sowohl den [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) als auch die [ITextChildProvider**-Schnittstelle](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) unterstützen.
- Ein Element, das [**ITextChildProvider implementiert,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) muss ein untergeordnetes Element oder ein untergeordnetes Element eines Elements sein, das [**ITextProvider implementiert.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider) Es ist nicht erforderlich, dass dieses Element auch das [Text-Steuerelementmuster implementiert.](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange)
-   Die [**ITextChildProvider::TextRange-Eigenschaft**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) sollte den gleichen Textbereich angeben, den das enthaltende Textanbieterelement zurückgibt, wenn seine [**ITextProvider::RangeFromChild-Funktion**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) mit dem untergeordneten Textelement als eingeschlossenes untergeordnetes Element aufgerufen wird.

## <a name="required-members-for-itextchildprovider"></a>Erforderliche Member für **ITextChildProvider**

Diese Eigenschaften und Methoden sind für die Implementierung der [**ITextChildProvider-Schnittstelle**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) erforderlich.



| Erforderliche Member                                                     | Memberart | Hinweise |
|----------------------------------------------------------------------|-------------|-------|
| [**TextContainer**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | Eigenschaft    | Keine  |
| [**Textrange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | Eigenschaft    | Keine  |



 

Diesem Steuerelementmuster sind keine Methoden oder Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

**Konzeptionellen**

- [Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md)
- [Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
- [Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)