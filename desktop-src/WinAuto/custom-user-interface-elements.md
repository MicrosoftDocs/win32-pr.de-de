---
title: Benutzerdefinierte Benutzeroberfläche-Elemente
description: Serverentwickler entwerfen barrierefreie Objekte basierend auf der Benutzeroberfläche einer Anwendung.
ms.assetid: d9453fb0-9b4a-4103-81e3-1255091255a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 183a7024f546aa3e982b632430dad88c89ae79082ac3d91da97e56c821fde62c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133873"
---
# <a name="custom-user-interface-elements"></a>Benutzerdefinierte Benutzeroberfläche-Elemente

Serverentwickler entwerfen barrierefreie Objekte basierend auf der Benutzeroberfläche einer Anwendung. Da Active Accessibility [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) im Namen von vom System bereitgestellten Benutzeroberflächenelementen wie Listenfeldern, Menüs und Trackbar-Steuerelementen implementiert, müssen Sie die [IAccessible-Schnittstelle](appendix-a--supported-user-interface-elements-reference.md) nur für die folgenden Arten von benutzerdefinierten Benutzeroberflächenelementen implementieren:

-   Benutzerdefinierte Steuerelemente, die durch Registrieren einer anwendungsdefinierten Fensterklasse erstellt werden
-   Benutzerdefinierte Steuerelemente, die direkt auf dem Bildschirm gezeichnet werden und über kein zugeordnetes **HWND verfügen**
-   Benutzerdefinierte Steuerelemente wie Microsoft ActiveX und Java-Steuerelemente
-   Steuerelemente oder Objekte im Clientfenster der Anwendung, die noch nicht verfügbar gemacht wurden

Auf vom Besitzer gezeichnete Steuerelemente und Menüs kann zugegriffen werden, solange Sie die Richtlinien befolgen, die unter Verknüpfungen zum Verfügbar machen von benutzerdefinierten Benutzeroberfläche [werden.](shortcuts-for-exposing-custom-user-interface-elements.md) Wenn Sie diese Richtlinien befolgen, müssen Sie die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für Steuerelemente und Menüs, die vom Besitzer gezeichnet werden, nicht implementieren.

In den meisten Fällen kann auf Steuerelemente mit Übergeordneten und Unterklassen zugegriffen werden, da das System die grundlegende Funktionalität des Steuerelements verarbeitet. Wenn ein über- oder unterklassiertes Steuerelement jedoch das Verhalten des vom System bereitgestellten Steuerelements, auf dem es basiert, erheblich ändert, müssen Sie die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementieren. Weitere Informationen finden Sie unter [Verfügbar machen von Steuerelementen, die auf Systemsteuerelementen basieren.](exposing-controls-based-on-system-controls.md)

Wenn eine Anwendung nur vom System bereitgestellte Benutzeroberflächenelemente verwendet, muss sie mit Ausnahme des Clientfensters nicht [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementieren. Beispielsweise macht eine Anwendung, die einen Text-Editor enthält, der nicht mit einem Bearbeitungssteuerfeld implementiert wird, Textzeilen als barrierefreie Objekte verfügbar. Beachten Sie Microsoft Active Accessibility dass der Text in Bearbeitungs- und Rich Edit-Steuerelementen automatisch als einzelne Textzeichenfolge in der [**Value-Eigenschaft**](value-property.md) des Steuerelements verfügbar ist.

 

 




