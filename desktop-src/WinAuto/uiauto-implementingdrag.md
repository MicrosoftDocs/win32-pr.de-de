---
title: Drag-Steuerelementmuster
description: Stellt Richtlinien und Konventionen für die Implementierung des Drag-Steuerelementmusters mithilfe von IDragProvider bereit, einschließlich Informationen zu Eigenschaften und Methoden. Das Drag-Steuerelementmuster wird verwendet, um ziehbare Steuerelemente oder Steuerelemente mit ziehbaren Elementen zu unterstützen.
ms.assetid: 9853E9CB-D04B-4F67-8E9E-7F1F99BACEA7
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des Drag-Steuerelementmusters
- Benutzeroberflächenautomatisierung,Drag-Steuerelementmuster
- Benutzeroberflächenautomatisierung,IDragProvider
- IDragProvider
- Implementieren Benutzeroberflächenautomatisierung Drag-Steuerelementmustern
- Ziehen von Steuerelementmustern
- Steuerelementmuster,IDragProvider
- Steuerelementmuster,Implementieren von Benutzeroberflächenautomatisierung Drag
- Steuerelementmuster,Ziehen
- interfaces,IDragProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b5e14edbeede46d210e109e63fff40ff0646d1b2ab14b42cf517ddc4e688aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118827204"
---
# <a name="drag-control-pattern"></a>Drag-Steuerelementmuster

Stellt Richtlinien und Konventionen für die Implementierung des Drag-Steuerelementmusters mithilfe von [**IDragProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider)bereit, einschließlich Informationen zu Eigenschaften und Methoden.  Das **Drag-Steuerelementmuster** wird verwendet, um ziehbare Steuerelemente oder Steuerelemente mit ziehbaren Elementen zu unterstützen.

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Verwenden Sie beim Implementieren des Drag-Steuerelementmusters die folgenden Richtlinien und Konventionen: 

-   Die [**IDragProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) unterstützt zwei verschiedene Ziehstile: den Quell-/Zielstil und den Stil nur für die Quelle. Sie müssen den Stil auswählen, der für Ihre Drag & Drop-Szenarien am besten funktioniert:
    -   **Quell-/Zielstil:** Jedes mögliche Abbruchziel wird durch ein Element dargestellt, das die [**IDropTargetProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) implementiert. Während eines Ziehvorganges stammen Microsoft Benutzeroberflächenautomatisierung Ereignisse aus dem element, das gezogen wird, und aus den Drop-Target-Elementen.
    -   **Nur Quellformat:** Abbruchziele werden nicht durch Benutzeroberflächenautomatisierung dargestellt. Während eines Ziehvorganges stammen Ereignisse nur aus dem Element, das gezogen wird.
-   [**IDragProvider ist**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) eine schreibgeschützte Schnittstelle zum Überwachen von Ziehvorgängen. Sie können ihn nicht verwenden, um einen Ziehvorgang zu steuern. Sie können Ziehvorgänge automatisieren, indem Sie Mauseingaben an ein Steuerelement senden.
-   Die [**IDragProvider::IsGrabbed-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) ist erforderlich.
-   Die [**IDragProvider::D ropEffect-**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) und [**IDragProvider::D ropEffects-Eigenschaften**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) sind für eine implementierung im Nur-Quell-Stil erforderlich und für eine Implementierung des Quell-/Zielstils nicht zulässig. In einer Implementierung des Quell-/Zielstils können Drop-Target-Elemente nach ihren Absturzeffekten abgefragt werden.
-   Die [**IDragProvider::GrabbedItems-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) stellt das Ziehen mehrerer Elemente dar. Wenn der Benutzer den Ziehvorgang startet, müssen Sie ein neues Benutzeroberflächenautomatisierung erstellen, das als Ereignisquellenelement dient. Dieses neue Element gibt alle Ereignisse aus, die das Quellelement entweder im Quell-/Zielmodus oder nur im Quellmodus ausgelöst hätte, während keines der Elemente, die tatsächlich gezogen werden, Ereignisse ausgelöst hat. Wenn der Ziehvorgang abgeschlossen ist, zerstören Sie das Ereignisquellenelement.
-   Das -Element muss eigenschaftenveränderungsereignisse für die **Eigenschaften DropEffect** ([**UIA \_ DragDropEffectPropertyId**](uiauto-control-pattern-propids.md)) und **DropEffects** ([**UIA \_ DragDropEffectsPropertyId**](uiauto-control-pattern-propids.md)) bei derEnänderung aus. Eigenschaftenänderungsereignisse für die anderen Eigenschaften sind zulässig, können jedoch von den erforderlichen **DragStart-Ereignissen** ([**UIA \_ \_ DragStartEventId**](uiauto-event-ids.md)), **DragCancel** ([**UIA \_ \_ DragCancelEventId**](uiauto-event-ids.md)) und **DragComplete** ([**UIA \_ \_ DragCompleteEventId**](uiauto-event-ids.md)) abgeleitet werden.
-   

## <a name="required-members-for-idragprovider"></a>Erforderliche Member für **IDragProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IDragProvider-Schnittstelle**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider) erforderlich.



| Erforderliche Member                                                                        | Memberart | Hinweise                                                                         |
|-----------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------|
| [**IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed)                                     | Eigenschaft    | Keine                                                                          |
| [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect)                                   | Eigenschaft    | Erforderlich für eine Implementierung des Nur-Quell-Stils.                      |
| [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects)                                 | Eigenschaft    | Erforderlich, wenn mehr als ein möglicher Absturzeffekt für das greifte Element vorlag. |
| [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems)                         | Methode      | Erforderlich für einen Ziehvorgang mit mehreren Elementen.                                  |
| [**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)       | Ereignis       | Keine                                                                          |
| [**UIA \_ Drag \_ DragCancelEventId**](uiauto-event-ids.md)     | Ereignis       | Keine                                                                          |
| [**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md) | Ereignis       | Keine                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[DropTarget-Steuerelementmuster](/windows/desktop/WinAuto/uiauto-implementingdroptarget)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[UI Automation Support for Drag-and-Drop](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 