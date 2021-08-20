---
title: DragPattern/DragDropPattern-Elemente erfordern gültige DropEffect-Elemente.
description: DragPattern/DragDropPattern-Elemente erfordern gültige DropEffect-Elemente.
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd95e1da2d3d05c7499f72c86d454da2832947cafd0150e8f62b2f3e8d56af2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115678"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a>DragPattern/DragDropPattern-Elemente erfordern gültige DropEffect-Elemente.

## <a name="text"></a>Text

Elemente, die Drag/Drop unterstützen, sollten über einen gültigen Satz von "DropEffect" verfügen.

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Das -Element unterstützt entweder [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) oder [**IUIAutomationDropTargetPattern,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern)verfügt jedoch nicht über einen gültigen [**DropEffect-Eigenschaftensatz.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect)

Dieses Problem verursacht Probleme für Personen, die sich auf eine Sprachausgabe verlassen. Der Benutzer kann beim Ziehen nicht erkennen, welche Auswirkungen dieses Objekt hat.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Das Element oder sein übergeordnetes Element hat den [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) oder [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) nicht mit einem falsch zugewiesenen Namen oder einer falsch zugewiesenen Bezeichnung erstellt.
-   Ein Entwickler weiß nicht, dass Sprachausgaben DropEffect(s) lesen.

 

 




