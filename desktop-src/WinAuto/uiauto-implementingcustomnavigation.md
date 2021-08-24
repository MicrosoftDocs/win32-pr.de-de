---
title: CustomNavigation-Steuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung der ICustomNavigationProvider-Schnittstelle, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4499f5b031b5b5a9391f0c0078cb64c4c2715b61052c324cc2c2b19ccb2f5d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899555"
---
# <a name="customnavigation-control-pattern"></a>CustomNavigation-Steuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung der **ICustomNavigationProvider-Schnittstelle,** einschließlich Informationen zu Eigenschaften und Methoden. Das **CustomNavigation-Steuerelementmuster** wird verwendet, um die benutzerdefinierte Navigation zwischen Steuerelementen in hierarchieähnlichen Strukturen wie Listenelementen, Aufzählungslisten, nummerierten Listen und Überschriften zu ermöglichen. Dadurch können Anbieter Strukturen beschreiben oder die navigierbaren Beziehungen definieren, indem sie das Element allein und nicht nur das enthaltende Steuerelement verwenden.

Beispiele für Steuerelemente, die dieses Steuerelementmuster implementieren, finden Sie unter [Steuerelementtypen und deren unterstützte Steuerelementmuster.](uiauto-controlpatternmapping.md)

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **ICustomNavigationProvider**](#required-members-for-icustomnavigationprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **CustomNavigation-Anbieters** die folgenden Richtlinien und Konventionen:

-   Eigenschaftswerte für **PositionInSet,** **SizeOfSet** und **Level** sind einbasierte ganzzahlige Werte.
-   **ICustomNavigationProvider** ermöglicht keine aktive Bearbeitung des Steuerelements, z. B. das Verschieben von Positionen, das Hinzufügen und Entfernen von Elementen oder das Heraufstufen und Herabstufen von Ebenen.
-   Steuerelemente, die **ICustomNavigationProvider** implementieren, verfügen in der Regel über eine hierarchische Struktur, können ebenen jedoch mithilfe der **Navigate-Methode** überspringen. Die Eigenschaften **PositionInSet,** **SizeOfSet** und **Level** sind für das Muster erforderlich.

## <a name="required-members-for-icustomnavigationprovider"></a>Erforderliche Member für **ICustomNavigationProvider**

Die folgenden Eigenschaften sind für die Implementierung der **ICustomNavigationProvider-Schnittstelle** erforderlich.



| Erforderliche Member                                                                  | Memberart | Hinweise                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [**CachedLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | Eigenschaft    | Befindet sich auf der [**IUIAutomationElement4-Schnittstelle.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**CachedPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | Eigenschaft    | Befindet sich auf der [**IUIAutomationElement4-Schnittstelle.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**CachedSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | Eigenschaft    | Befindet sich auf der [**IUIAutomationElement4-Schnittstelle.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**CurrentLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | Eigenschaft    | Befindet sich auf der [**IUIAutomationElement4-Schnittstelle.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**CurrentPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | Eigenschaft    | Befindet sich auf der [**IUIAutomationElement4-Schnittstelle.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**CurrentSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | Eigenschaft    | Befindet sich auf der [**IUIAutomationElement4-Schnittstelle.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**Navigieren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | Methode      | Keine                                                                                |



 

Diesem Steuerelementmuster sind keine Methoden oder Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und deren unterstützte Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[ListItem-Steuerelement](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[HeaderItem-Steuerelement](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[DataItem-Steuerelement](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




