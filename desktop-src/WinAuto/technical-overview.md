---
title: Technischer Überblick
description: Microsoft Active Accessibility verbessert die Art und Weise, wie Barrierefreiheits Hilfen (spezialisierte Programme, die Menschen mit Behinderungen helfen, die Computer effektiver verwenden) mit Anwendungen arbeiten, die unter Microsoft Windows ausgeführt werden.
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f3931c6a69e9b8caed849942424039178a7884
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712947"
---
# <a name="technical-overview"></a>Technischer Überblick

Microsoft Active Accessibility verbessert die Art und Weise, wie Barrierefreiheits Hilfen (spezialisierte Programme, die Menschen mit Behinderungen helfen, die Computer effektiver verwenden) mit Anwendungen arbeiten, die unter Microsoft Windows ausgeführt werden.

Microsoft Active Accessibility basiert auf der von Microsoft entwickelten Component Object Model (com) und ist ein Industriestandard, der eine gängige Methode für die Kommunikation von Anwendungen und Betriebssystemen definiert. Microsoft Active Accessibility besteht aus den folgenden Komponenten:

-   Die COM-Schnittstelle [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), die Informationen über Benutzeroberflächen Elemente verfügbar macht. **IAccessible** verfügt auch über Eigenschaften und Methoden zum Abrufen von Informationen über und zum Bearbeiten dieses Benutzeroberflächen Elements.
-   WinEvents, ein Ereignis System, mit dem Server Clients benachrichtigen können, wenn ein Barrierefreies Objekt geändert wird.
-   Oleacc.dll, eine Support-oder Lauf Zeit-dll.

Die Microsoft Active Accessibility-dll, Oleacc.dll, besteht aus den folgenden Komponenten:

-   Funktionen, die es Clients ermöglichen, einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger anzufordern (z. b. [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).
-   Funktionen, mit denen Server einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger an einen Client (z. [**b. lresultfromuject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)) zurückgeben können.
-   Funktionen zum erhalten von lokalisiertem Text für die Rollen-und Statuscodes (z. b. [**getroletext**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) und [**getstatetext**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).
-   Einige Hilfsfunktionen ([**accessiblechildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).
-   Code, der die Standard Implementierung von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für Standardbenutzer-und COMCTL-Steuerelemente bereitstellt. Da diese im Namen der System Steuerelemente **IAccessible** implementieren, werden *Sie als* Proxys bezeichnet.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Funktionsweise von Active Accessibility](how-active-accessibility-works.md)
-   [Grundlagen zu Active Accessibility](active-accessibility-basics.md)
-   [Server Richtlinien](server-guidelines.md)
-   [Client Richtlinien](client-guidelines.md)
-   [COM-und Unicode-Richtlinien](com-and-unicode-guidelines.md)

 

 




