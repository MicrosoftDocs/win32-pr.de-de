---
title: ExpandCollapse-Steuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von IExpandCollapseProvider, einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen.
ms.assetid: 0ffc26c3-8696-44f9-b463-902a69e06d21
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des ExpandCollapse-Steuerelementmusters
- Benutzeroberflächenautomatisierung,ExpandCollapse-Steuerelementmuster
- Benutzeroberflächenautomatisierung,IExpandCollapseProvider
- IExpandCollapseProvider
- Implementieren von Benutzeroberflächenautomatisierung ExpandCollapse-Steuerelementmustern
- ExpandCollapse-Steuerelementmuster
- Steuerelementmuster,IExpandCollapseProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung ExpandCollapse
- Steuerelementmuster,ExpandCollapse
- interfaces,IExpandCollapseProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7fa1461110a7fcdee83b8b3c20c15653e7bd5740187b89337620f5410b2bf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998040"
---
# <a name="expandcollapse-control-pattern"></a>ExpandCollapse-Steuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung von [**IExpandCollapseProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen. Das **ExpandCollapse-Steuerelementmuster** wird verwendet, um Steuerelemente zu unterstützen, die visuell erweitert werden, um mehr Inhalt anzuzeigen, und reduzieren, um Inhalt auszublenden.

Beispiele für Steuerelemente, die dieses Steuerelementmuster implementieren, finden Sie unter [Steuerelementtypen und deren unterstützte Steuerelementmuster.](uiauto-controlpatternmapping.md)

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IExpandCollapseProvider**](#required-members-for-iexpandcollapseprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **ExpandCollapse-Steuerelementmusters** die folgenden Richtlinien und Konventionen:

-   Aggregatsteuerelemente, die mit untergeordneten Objekten erstellt wurden, die der Benutzeroberfläche Funktionen zum Erweitern/Reduzieren bieten, müssen das **ExpandCollapse-Steuerelementmuster** unterstützen, während die untergeordneten Elemente dies nicht tun. Beispielsweise wird ein Kombinationsfeld-Steuerelement mit einer Kombination aus Listenfeld-, Schaltflächen- und Bearbeitungssteuerelementen erstellt, aber es ist nur das übergeordnete Kombinationsfeld, das das **ExpandCollapse-Steuerelementmuster** unterstützen muss.
    > [!Note]  
    > Eine Ausnahme ist das Menüsteuerelement, das ein Aggregat einzelner Menüelementobjekte ist. Die Menüelementobjekte können das **ExpandCollapse-Steuerelementmuster** unterstützen, das übergeordnete Menüsteuerelement jedoch nicht. Eine ähnliche Ausnahme gilt für die Struktur- und Strukturelementsteuerelemente.

     

-   Wenn [**IExpandCollapseProvider::ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) eines Steuerelements auf **ExpandCollapseState \_ LeafNode** festgelegt ist, sind alle **ExpandCollapse-Funktionen** für das Steuerelement derzeit inaktiv, und die einzigen Informationen, die mit diesem Steuerelementmuster abgerufen werden können, sind **ExpandCollapseState**. Wenn anschließend untergeordnete Objekte hinzugefügt werden, ändert **sich expandCollapseState,** und die **ExpandCollapse-Funktionalität** wird aktiviert.
-   [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) bezieht sich nur auf die Sichtbarkeit von unmittelbar untergeordneten Objekten. sie verweist nicht auf die Sichtbarkeit aller Nachfolgerobjekte.
-   [**Die IExpandCollapseProvider::Expand-**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) und [**Collapse-Funktionalität**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) ist steuerelementspezifisch. Im Folgenden finden Sie Beispiele dieses Verhaltens.
    -   Das Office Persönliches Menü kann ein Menüelement mit drei Zuständen ("Erweitert", "Reduziert" und "Teilweise erweitert") sein, wobei das Steuerelement den Zustand angibt, der beim Aufrufen von [**Erweitern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) oder [**Reduzieren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) angenommen werden soll.
    -   Beim Aufrufen von [**Erweitern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) für ein Strukturelement werden möglicherweise alle Nachfolger oder nur unmittelbar untergeordnete Elemente angezeigt.
    -   Wenn der Aufruf von [**Erweitern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) oder [**Reduzieren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) für ein Steuerelement den Zustand seiner Nachfolger beibehält, sollte ein Sichtbarkeitsänderungsereignis gesendet werden, kein Zustandsänderungsereignis. Wenn das übergeordnete Steuerelement beim Reduzieren nicht den Zustand seiner Nachfolger beibehält, kann das Steuerelement alle nachfolgerlichen Elemente zerstören, die nicht mehr sichtbar sind, und ein zerstörtes Ereignis auslösen. oder sie kann den [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) für jedes Nachfolger-Element ändern und ein Sichtbarkeitsänderungsereignis auslösen.
-   Um die Navigation zu gewährleisten, ist es wünschenswert, dass sich ein Objekt in der Microsoft Benutzeroberflächenautomatisierung-Struktur (mit entsprechendem Sichtbarkeitszustand) befindet, unabhängig von seinen Eltern [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate). Wenn Nachfolger bei Bedarf generiert werden, werden sie möglicherweise nur in der Benutzeroberflächenautomatisierung-Struktur angezeigt, nachdem sie zum ersten Mal angezeigt wurden, oder nur, wenn sie sichtbar sind.

## <a name="required-members-for-iexpandcollapseprovider"></a>Erforderliche Member für **IExpandCollapseProvider**

Die folgenden Eigenschaften, Methoden und Ereignisse sind für die Implementierung der [**IExpandCollapseProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) erforderlich.



| Erforderliche Member                                                                                    | Memberart | Hinweise                                                                  |
|-----------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------|
| [**Expandcollapsestate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)                   | Eigenschaft    | Keine                                                                   |
| [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)                                             | Methode      | Keine                                                                   |
| [**Reduzieren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)                                         | Methode      | Keine                                                                   |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Ereignis       | Diesem Steuerelement sind keine Ereignisse zugeordnet. verwenden Sie diesen generischen Ereignishandler. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und deren unterstützte Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




