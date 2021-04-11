---
title: Verwenden der IAccessible-Schnittstelle
description: Die IAccessible-Schnittstelle ist eine Auflistung von Methoden, die die gängigsten Attribute und Verhaltensweisen einer Breite Palette von Benutzeroberflächen Elementen verfügbar machen.
ms.assetid: 82f6e934-58ea-47f2-98a3-2ab1c20f24c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218d009793dc1bebac2a7e5caeba8fa140ac0d96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310255"
---
# <a name="using-the-iaccessible-interface"></a>Verwenden der IAccessible-Schnittstelle

Die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle ist eine Auflistung von Methoden, die die gängigsten Attribute und Verhaltensweisen einer Breite Palette von Benutzeroberflächen Elementen verfügbar machen. Ein Benutzeroberflächen Element ist ein Steuerelement, z. b. ein Menü oder eine Schaltfläche, das Teil der Benutzeroberfläche ist. Ein Barrierefreies Objekt ist ein UI-Element, das über eine sinnvolle **IAccessible** -Schnittstelle verfügt.

Einige der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften können nicht auf jede Art von Benutzeroberflächen Element angewendet werden. Außerdem variiert die Implementierung von **IAccessible** von der Anwendung bis zur Anwendung.

Obwohl die Parameter und Rückgabewerte für die Eigenschaften und Methoden von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) vollständig angegeben sind, wird die Art und Weise, wie ein Client eine Eigenschaft verwenden sollte oder wie ein Server eine Eigenschaft implementieren soll, manchmal interpretiert.

Dieser Abschnitt enthält Vorschläge, Richtlinien und Beispiele für die Unterstützung von Client Anwendungen beim Abrufen von Informationen zu Benutzeroberflächen Elementen und zur Unterstützung von Server Anwendungen bei der Bereitstellung geeigneter

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Inhalt von beschreibenden Eigenschaften](content-of-descriptive-properties.md)
-   [Auswahl-und Fokus Eigenschaften und-Methoden](selection-and-focus-properties-and-methods.md)
-   [Objekt Navigations Eigenschaften und-Methoden](object-navigation-properties-and-methods.md)

 

 




