---
title: ExpandCollapse-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von iexpandreduseprovider, einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen.
ms.assetid: 0ffc26c3-8696-44f9-b463-902a69e06d21
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines ExpandCollapse-Steuerelement Musters
- UI-Automatisierung, ExpandCollapse-Steuerelement Muster
- UI-Automatisierung, iexpandreduseprovider
- IExpandCollapseProvider
- Implementieren von ExpandCollapse-Steuerelement Mustern für Benutzeroberflächen Automatisierung
- ExpandCollapse-Steuerelement Muster
- Steuerelement Muster, iexpandreduseprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächen Automatisierung ExpandCollapse
- Steuerelement Muster, ExpandCollapse
- Schnittstellen, iexpandreduseprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bd28ddcc201dcff0a4811a1eb8e04670f93091
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036726"
---
# <a name="expandcollapse-control-pattern"></a>ExpandCollapse-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**iexpandreduseprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider), einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen. Das **ExpandCollapse** -Steuerelement Muster wird verwendet, um Steuerelemente zu unterstützen, die visuell erweitert werden, um mehr Inhalt anzuzeigen und den Inhalt auszublenden.

Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **iexpandreduseprovider**](#required-members-for-iexpandcollapseprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **ExpandCollapse** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Aggregat Steuerelemente, die mit untergeordneten Objekten erstellt wurden, die die Benutzeroberfläche mit Erweiterungs-/reduzierungsfunktionalität bereitstellen, müssen das **ExpandCollapse** -Steuerelement Muster unterstützen, während deren unter Beispielsweise wird ein Kombinations Feld-Steuerelement mit einer Kombination aus Listenfeld-, Schaltflächen-und Bearbeitungs Steuerelementen erstellt, aber es ist nur das übergeordnete Kombinations Feld, das das **ExpandCollapse** -Steuerelement Muster unterstützen muss.
    > [!Note]  
    > Eine Ausnahme stellt das Menü Steuerelement dar, bei dem es sich um ein Aggregat einzelner Menü Element Objekte handelt. Die Menü Element Objekte können das **ExpandCollapse** -Steuerelement Muster unterstützen, aber das übergeordnete Menü Steuerelement ist nicht möglich. Eine ähnliche Ausnahme gilt für die Struktur-und Strukturelement-Steuerelemente.

     

-   Wenn [**iexpandreduseprovider:: expandredusestate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) eines Steuer Elements auf **expandredusestate \_ leafnode** festgelegt ist, sind alle **ExpandCollapse** -Funktionen für das Steuerelement derzeit inaktiv, und die einzigen Informationen, die mithilfe dieses Steuerelement Musters abgerufen werden können, sind **expandredusestate**. Wenn nachfolgend untergeordnete Objekte hinzugefügt werden, werden die Funktionen " **expandredusestate** " und " **ExpandCollapse** " aktiviert.
-   [**Expandredusestate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) verweist nur auf die Sichtbarkeit unmittelbarer untergeordneter Objekte. Sie verweist nicht auf die Sichtbarkeit aller untergeordneten Objekte.
-   [**Iexpandreduseprovider:: Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) -und [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) -Funktionalität ist Steuerelement spezifisch. Im Folgenden finden Sie Beispiele dieses Verhaltens.
    -   Das persönliche Office-Menü kann ein drei-Status-Menü Element ("Erweitert", "reduziert" und "partiallyexpanded") sein, wobei das Steuerelement den zu verwendenden Zustand angibt, wenn " [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) " oder " [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) " aufgerufen wird.
    -   Wenn Sie " [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) " für ein Strukturelement aufrufen, werden möglicherweise alle Nachfolger oder nur direkt untergeordnete Elemente
    -   Wenn das Aufrufen von [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) oder [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) für ein Steuerelement den Zustand seiner Nachfolger Elemente beibehält, sollte ein Sichtbarkeits Änderungs Ereignis gesendet werden, kein Status Änderungs Ereignis. Wenn das übergeordnete Steuerelement den Zustand seiner Nachfolger nicht beibehält, wenn es reduziert ist, kann das Steuerelement alle Nachfolger zerstören, die nicht mehr sichtbar sind, und ein zerstörtes Ereignis darstellen. oder Sie kann den [**expandredu-State**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) für jeden Nachfolger ändern und ein Sichtbarkeits Änderungs Ereignis auswerfen.
-   Um die Navigation zu gewährleisten, ist es wünschenswert, dass sich ein Objekt unabhängig von seinen übergeordneten Elementen [**expandredusestate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)in der Microsoft UI Automation-Struktur (mit dem entsprechenden Sichtbarkeits Zustand) befindet. Wenn Nachfolger Bedarfs gesteuert generiert werden, werden Sie möglicherweise nur in der Benutzeroberflächenautomatisierungs-Struktur angezeigt, nachdem Sie zum ersten Mal oder nur angezeigt werden, wenn Sie sichtbar sind.

## <a name="required-members-for-iexpandcollapseprovider"></a>Erforderliche Member für **iexpandreduseprovider**

Die folgenden Eigenschaften, Methoden und Ereignisse sind für die Implementierung der [**iexpandreduseprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                                                    | Memberart | Hinweise                                                                  |
|-----------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------|
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)                   | Eigenschaft    | Keine                                                                   |
| [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)                                             | Methode      | Keine                                                                   |
| [**Reduzieren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)                                         | Methode      | Keine                                                                   |
| [**Iuiautomationpropertychangeabventhandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Ereignis       | Diesem Steuerelement sind keine Ereignisse zugeordnet. Verwenden Sie diesen generischen Ereignishandler. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




