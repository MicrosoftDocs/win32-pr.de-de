---
title: Steuerelement Muster ziehen
description: Stellt Richtlinien und Konventionen für das Implementieren des Drag-Steuerelement Musters mithilfe von idragprovider bereit, einschließlich Informationen zu Eigenschaften und Methoden. Das Drag-Steuerelement Muster wird zur Unterstützung von dragfähigen Steuerelementen oder Steuerelementen mit dragfähigen Elementen verwendet.
ms.assetid: 9853E9CB-D04B-4F67-8E9E-7F1F99BACEA7
keywords:
- Benutzeroberflächenautomatisierung, Implementieren eines Drag-Steuerelement Musters
- UI-Automatisierung, Drag-Steuerelement Muster
- UI-Automatisierung, idragprovider
- IDragProvider
- Implementieren von Drag-Steuerungs Mustern für Benutzeroberflächen Automatisierung
- Ziehen von Steuerelement Mustern
- Steuerelement Muster, idragprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-Drag
- Steuerelement Muster, ziehen
- Schnittstellen, idragprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f0212eca37e1890596143f27e9af70e1fb19a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039211"
---
# <a name="drag-control-pattern"></a>Steuerelement Muster ziehen

Stellt Richtlinien und Konventionen für das Implementieren des **Drag** -Steuerelement Musters mithilfe von [**idragprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider)bereit, einschließlich Informationen zu Eigenschaften und Methoden. Das **Drag** -Steuerelement Muster wird zur Unterstützung von dragfähigen Steuerelementen oder Steuerelementen mit dragfähigen Elementen verwendet.

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Verwenden Sie die folgenden Richtlinien und Konventionen, wenn Sie das **Drag** -Steuerelement Muster implementieren:

-   Die [**idragprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) -Schnittstelle unterstützt zwei unterschiedliche Zieh Stile: den Quell-/Zielstil und den reinen Quell Stil. Sie müssen den Stil auswählen, der für Ihre Drag & Drop-Szenarien am besten geeignet ist:
    -   **Quell-/Zielstil:** Jedes mögliche Ablage Ziel wird durch ein Element dargestellt, das die [**idroptargetprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) -Schnittstelle implementiert. Während eines Zieh Vorgangs stammen Microsoft UI Automation-Ereignisse aus dem gezogenen Element und aus den Drop-Target-Elementen.
    -   **Nur Quelle:** Drop-Ziele werden nicht durch Benutzeroberflächenautomatisierungs-Elemente dargestellt. Während eines Zieh Vorgangs stammen Ereignisse nur aus dem Element, das gezogen wird.
-   [**Idragprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) ist eine schreibgeschützte Schnittstelle, die zum Überwachen von Drag-Vorgängen vorgesehen ist. Sie können Sie nicht verwenden, um einen Zieh Vorgang zu steuern. Sie können Zieh Vorgänge automatisieren, indem Sie Maus Eingaben an ein-Steuerelement senden.
-   Die [**idragprovider:: isgrab**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) -Eigenschaft ist erforderlich.
-   Die [**idragprovider::D ropeer ffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) -und [**idragprovider::D ropeer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) -Eigenschaften sind für eine reine Quell Implementierung erforderlich und sind für eine Implementierung des Quell-/Zielstils unzulässig. In einer Implementierung des Quell-/Zielstils können Drop-Target-Elemente für Ihre Ablage Effekte abgefragt werden.
-   Die [**idragprovider:: grabbeditems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) -Eigenschaft stellt das Ziehen mehrerer Elemente dar. Wenn der Benutzer den Zieh Vorgang startet, müssen Sie ein neues Benutzeroberflächenautomatisierungs-Element erstellen, das als Ereignis Quell Element fungiert. Dieses neue Element löst alle Ereignisse aus, die das Quell Element im Quell-oder Ziel Modus ausgelöst hätte, während keines der Elemente, die tatsächlich gezogen werden, Ereignisse auslöst. Wenn der Zieh Vorgang beendet ist, zerstören Sie das Ereignis Quell Element.
-   Das-Element muss bei der Änderung Eigenschaften geänderte Ereignisse für die Eigenschaften **dropffect** ([**UIA \_ dragdropeer ffectpropertyid**](uiauto-control-pattern-propids.md)) und **dropeer** . ([**UIA \_ dragdropeer ffectspropertyid**](uiauto-control-pattern-propids.md)) auslösen. Eigenschaften geänderte Ereignisse für die anderen Eigenschaften sind zulässig, können jedoch von der erforderlichen **DragStart** ([**UIA \_ Drag \_ dragstarteventid**](uiauto-event-ids.md)), **dragcancel** ([**UIA \_ Drag \_ dragcanceleventid**](uiauto-event-ids.md)) und **dragcomplete** ([**UIA \_ Drag \_ dragcompleteeventid**](uiauto-event-ids.md)) abgeleitet werden.
-   

## <a name="required-members-for-idragprovider"></a>Erforderliche Member für **idragprovider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**idragprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                                        | Memberart | Hinweise                                                                         |
|-----------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------|
| [**Isgrab**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed)                                     | Eigenschaft    | Keine                                                                          |
| [**Dropffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect)                                   | Eigenschaft    | Erforderlich für eine Implementierung des reinen Quell Stils.                      |
| [**Drof ffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects)                                 | Eigenschaft    | Erforderlich, wenn mehrere mögliche Ablage Effekte für das eingepackte Element vorhanden sind. |
| [**Getgrabbeditems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems)                         | Methode      | Erforderlich für einen Drag-Vorgang mit mehreren Elementen.                                  |
| [**UIA \_ Drag \_ dragstarteventid**](uiauto-event-ids.md)       | Ereignis       | Keine                                                                          |
| [**UIA \_ Drag \_ dragcanceleventid**](uiauto-event-ids.md)     | Ereignis       | Keine                                                                          |
| [**UIA \_ Drag \_ dragcompleteeventid**](uiauto-event-ids.md) | Ereignis       | Keine                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[DropTarget-Steuerelement Muster](/windows/desktop/WinAuto/uiauto-implementingdroptarget)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[Benutzeroberflächenautomatisierungs-Unterstützung für Drag & Drop](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 