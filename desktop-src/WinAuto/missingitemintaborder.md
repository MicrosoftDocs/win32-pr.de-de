---
title: MissingItemInTabOrder
description: MissingItemInTabOrder
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc8e413c12b93ebcb3fcbb9d38e56041bedf4e0b8abb98581d77fae4c275f15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071810"
---
# <a name="missingitemintaborder"></a>MissingItemInTabOrder

## <a name="text"></a>Text

Dieses Element scheint tabellarierbar zu sein, befindet sich jedoch nicht in der Reihenfolge der Registerkarten.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Auf ein fokussierbares Element kann nicht über die standardmäßige Tastaturnavigation (TAB ODER UMSCHALT+TAB) zugegriffen werden. Beispielsweise wurde das Element nicht als Tabstopp markiert oder einem Registerkartenindex zugewiesen. Dieses Problem verursacht Probleme für Personen, die sich auf eine Sprachausgabe und Tastatur für die Navigation verlassen, weil:

-   Das Element kann nicht ermittelt werden.
-   Wenn das Element ein untergeordnetes Element eines benutzerdefinierten Listensteuerelements ist, fehlen möglicherweise Hinweise, die angeben, dass durch das untergeordnete Element mithilfe des Pfeils navigiert werden kann.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Die MSAA-Rolle des Elements oder seines übergeordneten Elements ist nicht ordnungsgemäß festgelegt. Wenn beispielsweise nicht alle Listenelemente in einem Listenansichtssteuerelement über MSAA als ROLE SYSTEM LISTITEM verfügbar gemacht \_ \_ werden, schlägt die Überprüfung fehl, da auf die Listenelemente nicht über die TAB-TASTE zugegriffen werden kann.
-   Das Element oder sein übergeordnetes Element ist ein benutzerdefiniertes Steuerelement, das tabbing nicht ordnungsgemäß implementiert. Beispielsweise ist die MSAA State-Eigenschaft nie auf STATE \_ SYSTEM \_ FOCUSABLE festgelegt.
-   Ein Element, das als Container für andere Elemente fungiert, wurde zur Überprüfung ausgewählt, unterstützt aber die Tastaturnavigation selbst nicht. Beispielsweise kann auf eine Symbolleiste und ihre untergeordneten Elemente nicht über die TAB-TASTE zugegriffen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Richtlinien zur Gestaltung einer tastaturgesteuerten Benutzeroberfläche](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 