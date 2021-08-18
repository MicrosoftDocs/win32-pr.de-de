---
title: Auswählen der zu unterstützenden Eigenschaften
description: Die IAccessible-Eigenschaften bieten Serverentwicklern eine Möglichkeit, eine Vielzahl von Benutzeroberflächenelementen zu beschreiben.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a3c9ef5d56c6d963a05ac84b5e2cacafde488c377ebcc73fa1e2c4be1adab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133963"
---
# <a name="choosing-which-properties-to-support"></a>Auswählen der zu unterstützenden Eigenschaften

Die [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) bieten Serverentwicklern eine Möglichkeit, eine Vielzahl von Benutzeroberflächenelementen zu beschreiben. Aber nicht alle Eigenschaften gelten für jede Art von Benutzeroberflächenelement. Darüber hinaus stellen einige Eigenschaften beschreibende Informationen bereit, die zwar nützlich, aber nicht wichtig sind.

Server müssen die folgenden Eigenschaften und Methoden für jedes Objekt unterstützen:

-   [**Name**](name-property.md)
-   [**Funktion**](role-property.md)
-   [**State**](state-property.md)
-   [**Speicherort**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) und [ **IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) und [ **IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

Die folgenden Eigenschaften und Methoden müssen unterstützt werden, wenn sie auf das -Objekt anwendbar sind:

-   [**KeyboardShortcut**](keyboardshortcut-property.md)
-   [**Wert**](value-property.md)

Die folgenden Eigenschaften und Methoden müssen unterstützt werden, wenn das Objekt über untergeordnete Elemente verfügt:

-   [**Child**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) und [ **ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**Fokus, Auswahl**](selection-and-focus-properties-and-methods.md)und [ **IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

Die folgenden Eigenschaften sind optional, stellen jedoch nützliche beschreibende Informationen zum -Objekt bereit. Die [**Description-Eigenschaft**](description-property.md) wird implementiert, um Bitmaps und andere Bilder zu beschreiben.

-   [**Beschreibung**](description-property.md)
-   [**DefaultAction**](defaultaction-property.md) und [ **IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**Hilfe**](help-property.md)
-   [**Helptopic**](helptopic-property.md)

 

 




