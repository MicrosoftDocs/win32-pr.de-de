---
title: Auswählen der zu unterstützten Eigenschaften
description: Die IAccessible-Eigenschaften bieten Server Entwicklern die Möglichkeit, eine Vielzahl von Benutzeroberflächen Elementen zu beschreiben.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c88a808889403f88d414f7ad950b3e431c00e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310500"
---
# <a name="choosing-which-properties-to-support"></a>Auswählen der zu unterstützten Eigenschaften

Die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften bieten Server Entwicklern die Möglichkeit, eine Vielzahl von Benutzeroberflächen Elementen zu beschreiben. Allerdings sind nicht alle Eigenschaften für jede Art von Benutzeroberflächen Element anwendbar. Außerdem bieten einige Eigenschaften beschreibende Informationen, die hilfreich, aber nicht unbedingt erforderlich sind.

Server müssen für jedes Objekt die folgenden Eigenschaften und Methoden unterstützen:

-   [**Name**](name-property.md)
-   [**Funktion**](role-property.md)
-   [**State**](state-property.md)
-   [**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) und [ **IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) und [ **IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

Die folgenden Eigenschaften und Methoden müssen unterstützt werden, wenn Sie auf das Objekt anwendbar sind:

-   [**KeyboardShortcut**](keyboardshortcut-property.md)
-   [**Wert**](value-property.md)

Die folgenden Eigenschaften und Methoden müssen unterstützt werden, wenn das-Objekt über untergeordnete Elemente verfügt:

-   [**Child**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) und [ **childCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**Fokus, Auswahl**](selection-and-focus-properties-and-methods.md)und [ **IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

Die folgenden Eigenschaften sind optional, bieten jedoch nützliche beschreibende Informationen über das Objekt. Die [**Description**](description-property.md) -Eigenschaft wird implementiert, um Bitmaps und andere Bilder zu beschreiben.

-   [**Beschreibung**](description-property.md)
-   [**DEFAULTACTION**](defaultaction-property.md) und [ **IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**Hilfe**](help-property.md)
-   [**HelpTopic**](helptopic-property.md)

 

 




