---
title: Benutzerdefinierte Benutzeroberflächen Elemente
description: Server Entwickler entwerfen barrierefreie Objekte basierend auf der Benutzeroberfläche einer Anwendung.
ms.assetid: d9453fb0-9b4a-4103-81e3-1255091255a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32a086b977a1737a17206261aaaa94faa754d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855648"
---
# <a name="custom-user-interface-elements"></a>Benutzerdefinierte Benutzeroberflächen Elemente

Server Entwickler entwerfen barrierefreie Objekte basierend auf der Benutzeroberfläche einer Anwendung. Da [Active Accessibility die IAccessible-Schnittstelle für vom System bereitgestellte Benutzeroberflächen Elemente](appendix-a--supported-user-interface-elements-reference.md) (z. b. Listenfelder, Menüs und TrackBar-Steuerelemente) implementiert, müssen Sie die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle nur für die folgenden Arten von benutzerdefinierten Benutzeroberflächen Elementen implementieren:

-   Benutzerdefinierte Steuerelemente, die durch das Registrieren einer Anwendungs definierten Fenster Klasse erstellt werden
-   Benutzerdefinierte Steuerelemente, die direkt auf dem Bildschirm gezeichnet werden, denen kein **HWND** zugeordnet ist
-   Benutzerdefinierte Steuerelemente wie Microsoft ActiveX-und Java-Steuerelemente
-   Steuerelemente oder Objekte im Client Fenster der Anwendung, die noch nicht verfügbar sind

Auf Besitzer gezeichnete Steuerelemente und Menüs kann zugegriffen werden, solange Sie die Richtlinien befolgen, die unter Verknüpfungen zum verfügbar machen [benutzerdefinierter Benutzeroberflächen Elemente](shortcuts-for-exposing-custom-user-interface-elements.md)erläutert werden. Wenn Sie diese Richtlinien befolgen, müssen Sie die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle nicht für vom Besitzer gezeichnete Steuerelemente und Menüs implementieren.

In den meisten Fällen sind die über-und untergeordneten Steuerelemente zugänglich, da das System die grundlegenden Funktionen des Steuer Elements behandelt. Wenn jedoch das Verhalten des vom System bereitgestellten Steuer Elements, auf dem es basiert, von einem übergeordneten oder untergeordneten Steuerelement erheblich geändert wird, müssen Sie die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle implementieren. Weitere Informationen finden Sie unter verfügbar machen [von Steuerelementen auf der Grundlage von System Steuerelementen](exposing-controls-based-on-system-controls.md).

Wenn eine Anwendung nur vom System bereitgestellte Benutzeroberflächen Elemente verwendet, muss [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)nicht implementiert werden, außer für das Client Fenster. Beispielsweise stellt eine Anwendung, die einen Text-Editor enthält, der nicht mit einem Bearbeitungs Steuerelement implementiert ist, Textzeilen als barrierefreie Objekte zur Verfügung. Beachten Sie, dass Microsoft Active Accessibility den Text in Edit-und Rich Edit-Steuerelementen automatisch als eine einzelne Text Zeichenfolge in der [**value**](value-property.md) -Eigenschaft des-Steuer Elements verfügbar macht.

 

 




