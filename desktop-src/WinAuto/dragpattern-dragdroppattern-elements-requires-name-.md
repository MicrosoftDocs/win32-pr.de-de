---
title: Dragpattern/dragdroppattern-Elemente benötigen einen Namen
description: Dragpattern/dragdroppattern-Elemente benötigen einen Namen
ms.assetid: DEF58FB2-5830-4162-87D0-40DEC1237529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc60eeca59f4754f9c160696cdfa2556c36a5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337135"
---
# <a name="dragpatterndragdroppattern-elements-requires-name"></a>Dragpattern/dragdroppattern-Elemente benötigen einen Namen

## <a name="text"></a>Text

Für Elemente, die Drag & Drop unterstützen, muss ein gültiger Name festgelegt sein.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Das Element unterstützt entweder [**iuiautomationdragpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) oder [**iuiautomationdroptargetpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), aber es ist kein gültiger Name festgelegt.

Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm verlassen, Probleme haben. Der Benutzer kann nicht erkennen, was dieses Objekt ist, da der Bildschirm Lesevorgang keinen gültigen Namen ausliest, um zu unterscheiden, was dieses Element beim ziehen ist.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Das Element oder das übergeordnete Element weist einen falsch zugewiesenen Namen oder eine Bezeichnung auf.
-   Ein Entwickler weiß nicht, dass Bildschirm Sprachausgaben Namen und Steuerelement Typen lesen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name-Eigenschaft](name-property.md)
</dt> <dt>

[**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)
</dt> <dt>

[**Iuiautomationelement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




