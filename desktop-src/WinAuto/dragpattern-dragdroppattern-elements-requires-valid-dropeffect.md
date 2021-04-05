---
title: Dragpattern/dragdroppattern-Elemente erfordern gültiges dropffect
description: Dragpattern/dragdroppattern-Elemente erfordern gültiges dropffect
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33acda19732e2ebd96182023fce9641012b50d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707164"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a>Dragpattern/dragdroppattern-Elemente erfordern gültiges dropffect

## <a name="text"></a>Text

Für Elemente, die Drag & Drop unterstützen, sollte ein gültiger "dropeer"-Satz festgelegt sein.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Das-Element unterstützt entweder [**iuiautomationdragpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) oder [**iuiautomationdroptargetpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), aber es ist keine gültige [**dropeer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) -Eigenschaft festgelegt.

Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm verlassen, Probleme haben. Der Benutzer kann nicht erkennen, welche Auswirkung dieses Objekt beim ziehen hat.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Das-Element oder das übergeordnete Element hat den [**dropffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) -oder den [**dropeer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) -Typ nicht zu einem fälschlicherweise zugewiesenen Namen oder einer Bezeichnung erstellt.
-   Ein Entwickler weiß nicht, dass die Bildschirm Sprachausgaben dropeer ffect (s) lesen.

 

 




