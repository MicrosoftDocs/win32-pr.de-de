---
title: DropTarget-Steuerelement Muster
description: Stellt Richtlinien und Konventionen für das Implementieren des DropTarget-Steuerelement Musters mithilfe von idroptargetprovider bereit, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: DD5EE4A0-E6C0-4657-A60F-7F59FC569E04
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines DropTarget-Steuerelement Musters
- UI-Automatisierung, DropTarget-Steuerelement Muster
- UI-Automatisierung, idroptargetprovider
- IDropTargetProvider
- Implementieren von DropTarget-Steuerelement Mustern für Benutzeroberflächen Automatisierung
- DropTarget-Steuerelement Muster
- Steuerelement Muster, idroptargetprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs DropTarget
- Steuerelement Muster, DropTarget
- Schnittstellen, idroptargetprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd03d219ce8b26a0ac01806ebab09892a027fbd1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315669"
---
# <a name="droptarget-control-pattern"></a>DropTarget-Steuerelement Muster

Stellt Richtlinien und Konventionen für das Implementieren des **DropTarget** -Steuerelement Musters mithilfe von [**idroptargetprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider)bereit, einschließlich Informationen zu Eigenschaften und Methoden. Das **DropTarget** -Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die als Ziel eines Drag & Drop-Vorgangs verwendet werden können.

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Wenn Sie das **DropTarget** -Steuerelement Muster implementieren, verwenden Sie die folgenden Richtlinien und Konventionen:

-   Das **DropTarget** -Muster muss unterstützt werden, während ein Zieh Vorgang ausgeführt wird. Sie kann auch dann unterstützt werden, wenn kein Zieh Vorgang ausgeführt wird.
-   Die [**idroptargetprovider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) -Eigenschaft ist erforderlich.
-   Die [**idroptargetprovider::D roptargeteffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) -Eigenschaft ist erforderlich, wenn mehrere mögliche Ablage Effekte für das Ziel vorhanden sind.
-   Das-Element muss geänderte Ereignis Eigenschaften für die Eigenschaften **droptargeteffect** ([**UIA \_ droptargetdroptargeteffectpropertyid**](uiauto-control-pattern-propids.md)) und **droptargeteffects** ([**UIA \_ droptargetdroptargeteffectspropertyid**](uiauto-control-pattern-propids.md)) bei Änderungen angeben.

## <a name="required-members-for-idroptargetprovider"></a>Erforderliche Member für **idroptargetprovider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**idroptargetprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                                              | Memberart | Hinweise                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [**Droptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | Eigenschaft    | Keine                                                                     |
| [**Droptargeteffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | Eigenschaft    | Erforderlich, wenn das Ablage Ziel mehr als einen möglichen Ablage Effekt unterstützt. |
| [**UIA \_ DropTarget \_ dragentereventid**](uiauto-event-ids.md) | Ereignis       | Keine                                                                     |
| [**UIA \_ DropTarget \_ dragleaveeventid**](uiauto-event-ids.md) | Ereignis       | Keine                                                                     |
| [**\_Droppedeventid für UIA DropTarget \_**](uiauto-event-ids.md)     | Ereignis       | Keine                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Steuerelement Muster ziehen](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[Benutzeroberflächenautomatisierungs-Unterstützung für Drag & Drop](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 