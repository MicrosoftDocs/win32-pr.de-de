---
title: Verwenden der IAccessible-Schnittstelle
description: Die IAccessible-Schnittstelle ist eine Sammlung von Methoden, die die gängigsten Attribute und Verhaltensweisen einer Vielzahl von Benutzeroberflächenelementen verfügbar machen.
ms.assetid: 82f6e934-58ea-47f2-98a3-2ab1c20f24c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c683e83928db53894c7c2c22976a5cf58c402c241e698dca5248230b1b24177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744895"
---
# <a name="using-the-iaccessible-interface"></a>Verwenden der IAccessible-Schnittstelle

Die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ist eine Sammlung von Methoden, die die gängigsten Attribute und Verhaltensweisen einer Vielzahl von Benutzeroberflächenelementen verfügbar machen. Ein Benutzeroberflächenelement ist ein Steuerelement, z. B. ein Menü oder eine Pushschaltfläche, das Teil der Benutzeroberfläche ist. Ein barrierefreies Objekt ist ein Benutzeroberflächenelement, das über eine aussagekräftige **IAccessible-Schnittstelle** verfügt.

Einige der [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) gelten nicht für jede Art von Benutzeroberflächenelement. Außerdem variiert die Implementierung von **IAccessible** von Anwendung zu Anwendung.

Obwohl die Parameter und Rückgabewerte für die [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und -Methoden vollständig angegeben sind, wird manchmal interpretiert, wie ein Client eine Eigenschaft verwenden soll oder wie ein Server eine Eigenschaft implementieren soll.

Dieser Abschnitt enthält Vorschläge, Richtlinien und Beispiele für die Unterstützung von Clientanwendungen beim Abrufen von Informationen zu Benutzeroberflächenelementen und bei der Bereitstellung geeigneter Informationen durch Serveranwendungen.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Inhalt beschreibender Eigenschaften](content-of-descriptive-properties.md)
-   [Auswahl- und Fokuseigenschaften und -methoden](selection-and-focus-properties-and-methods.md)
-   [Eigenschaften und Methoden der Objektnavigation](object-navigation-properties-and-methods.md)

 

 




