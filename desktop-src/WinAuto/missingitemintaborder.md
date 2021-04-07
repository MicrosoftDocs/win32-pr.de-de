---
title: Missingitemintaborder
description: Missingitemintaborder
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9841ab71e9f5d40cf25454e737b9790ce27a04de
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727520"
---
# <a name="missingitemintaborder"></a>Missingitemintaborder

## <a name="text"></a>Text

Dieses Element ist anscheinend Tabellen fähig, aber nicht in der Aktivier Reihenfolge.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Auf ein Fokussier bares Element kann nicht über die Standardtastatur Navigation (Tab oder UMSCHALT + TAB) zugegriffen werden. Beispielsweise wurde das-Element nicht als Tabstopp gekennzeichnet, oder es wurde ein Registerkarten Index zugewiesen. Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, folgende Probleme verursachen:

-   Das Element kann nicht gefunden werden.
-   Wenn das Element ein untergeordnetes Element eines benutzerdefinierten Listen Steuer Elements ist, können die Hinweise, die angeben, dass das untergeordnete Element mithilfe des Pfeils oder der Seiten Tasten navigiert werden kann, fehlen

## <a name="possible-causes"></a>Mögliche Ursachen

-   Die MSAA-Rolle des Elements oder des übergeordneten Elements ist nicht ordnungsgemäß festgelegt. Wenn z. b. alle Listenelemente in einem Listenansicht-Steuerelement nicht über MSAA als \_ ListItem-Rollen System verfügbar gemacht werden, tritt bei \_ der Überprüfung ein Fehler auf, da die Listenelemente nicht mithilfe der Tab-Taste aufgerufen werden können.
-   Das Element oder das übergeordnete Element ist ein benutzerdefiniertes Steuerelement, das die Tabstopps nicht korrekt implementiert. Beispielsweise ist die Eigenschaft MSAA State nie auf State \_ System \_ focverwendbar festgelegt.
-   Ein Element, das als Container für andere Elemente fungiert, wurde zur Überprüfung ausgewählt, unterstützt jedoch keine Tastaturnavigation. Beispielsweise können Sie mit der Tab-Taste auf eine Symbolleiste und deren untergeordnete Elemente nicht zugreifen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Richtlinien zur Gestaltung einer tastaturgesteuerten Benutzeroberfläche](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 