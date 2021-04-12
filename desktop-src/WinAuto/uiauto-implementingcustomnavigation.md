---
title: Customnavigation-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren der icustomnavigationprovider-Schnittstelle, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cc6524585f3ddd7ec764a791141fce9daa3c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206706"
---
# <a name="customnavigation-control-pattern"></a>Customnavigation-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren der **icustomnavigationprovider** -Schnittstelle, einschließlich Informationen zu Eigenschaften und Methoden. Das **customnavigation** -Steuerelement Muster wird verwendet, um die benutzerdefinierte Navigation zwischen Steuerelementen in Hierarchie ähnlichen Strukturen zu ermöglichen, z. b. Listenelemente, aufzählige Listen, nummerierte Listen Dies ermöglicht es Anbietern, Strukturen zu beschreiben oder die navigierbaren Beziehungen mit dem Element allein und nicht nur mit dem enthaltenden Steuerelement zu definieren.

Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **icustomnavigationprovider**](#required-members-for-icustomnavigationprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **customnavigation** -Anbieters die folgenden Richtlinien und Konventionen:

-   Eigenschaftswerte für **positioninset**, **sizeofset** und Level sind 1-basierte ganzzahlige Werte. 
-   **Icustomnavigationprovider** bietet keine aktive Bearbeitung des Steuer Elements, z. b. das Verschieben von Positionen, das Hinzufügen und Entfernen von Elementen oder das herauf Stufen und Herabstufen von Ebenen.
-   Steuerelemente, die **icustomnavigationprovider** implementieren, verfügen in der Regel über eine hierarchische Struktur, können jedoch Ebenen mithilfe der **Navigate** -Methode überspringen. Die Eigenschaften **positioninset**, **sizeofset** und **Level** sind für das Muster erforderlich.

## <a name="required-members-for-icustomnavigationprovider"></a>Erforderliche Member für **icustomnavigationprovider**

Die folgenden Eigenschaften sind erforderlich, um die **icustomnavigationprovider** -Schnittstelle zu implementieren.



| Erforderliche Member                                                                  | Memberart | Hinweise                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [**Cachedlevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | Eigenschaft    | In der [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) -Schnittstelle. |
| [**Cachedpositioninset**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | Eigenschaft    | In der [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) -Schnittstelle. |
| [**Cachedsizeofset**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | Eigenschaft    | In der [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) -Schnittstelle. |
| [**Currentlevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | Eigenschaft    | In der [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) -Schnittstelle. |
| [**Currentpositioninset**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | Eigenschaft    | In der [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) -Schnittstelle. |
| [**Currentsizeofset**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | Eigenschaft    | In der [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) -Schnittstelle. |
| [**Navigieren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | Methode      | Keine                                                                                |



 

Diesem Steuerelementmuster sind keine Methoden oder Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[ListItem-Steuerelement](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[HeaderItem-Steuerelement](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[DataItem-Steuerelement](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




