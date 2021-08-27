---
title: DropTarget-Steuerelementmuster
description: Stellt Richtlinien und Konventionen für die Implementierung des DropTarget-Steuerelementmusters mithilfe von IDropTargetProvider bereit, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: DD5EE4A0-E6C0-4657-A60F-7F59FC569E04
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des DropTarget-Steuerelementmusters
- Benutzeroberflächenautomatisierung,DropTarget-Steuerelementmuster
- Benutzeroberflächenautomatisierung,IDropTargetProvider
- IDropTargetProvider
- Implementieren von Benutzeroberflächenautomatisierung DropTarget-Steuerelementmustern
- DropTarget-Steuerelementmuster
- Steuerelementmuster,IDropTargetProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung DropTarget
- Steuerelementmuster, DropTarget
- interfaces,IDropTargetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03cc425c9d41a70150eba2431c6fd317f2f8c23f878f7a0615025aec25b85b68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098310"
---
# <a name="droptarget-control-pattern"></a>DropTarget-Steuerelementmuster

Stellt Richtlinien und Konventionen für die Implementierung des **DropTarget-Steuerelementmusters** mithilfe von [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider)bereit, einschließlich Informationen zu Eigenschaften und Methoden. The **DropTarget** control pattern is used to support controls that can be the target of a drag-and-drop operation.

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Verwenden Sie beim Implementieren des **DropTarget-Steuerelementmusters** die folgenden Richtlinien und Konventionen:

-   Das **DropTarget-Muster** muss unterstützt werden, während ein Ziehvorgang ausgeführt wird. Sie kann auch dann unterstützt werden, wenn kein Ziehvorgang ausgeführt wird.
-   Die [**IDropTargetProvider::D ropTargetEffect-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) ist erforderlich.
-   Die [**IDropTargetProvider::D ropTargetEffects-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) ist erforderlich, wenn mehrere mögliche Ablageeffekte für das Ziel vorhanden sind.
-   Das Element muss eigenschaftenänderungsereignisse für die Eigenschaften **DropTargetEffect** ([**UIA \_ DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) und **DropTargetEffects** ([**UIA \_ DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) auslösen, wenn sie geändert werden.

## <a name="required-members-for-idroptargetprovider"></a>Erforderliche Member für **IDropTargetProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IDropTargetProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) erforderlich.



| Erforderliche Member                                                                              | Memberart | Hinweise                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | Eigenschaft    | Keine                                                                     |
| [**DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | Eigenschaft    | Erforderlich, wenn das Ablageziel mehrere mögliche Ablageeffekte unterstützt. |
| [**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md) | Ereignis       | Keine                                                                     |
| [**UIA \_ DropTarget \_ DragLeaveEventId**](uiauto-event-ids.md) | Ereignis       | Keine                                                                     |
| [**UIA \_ DropTarget \_ DroppedEventId**](uiauto-event-ids.md)     | Ereignis       | Keine                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und deren unterstützte Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Drag&](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[UI Automation Support for Drag-and-Drop](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 