---
title: Technischer Überblick
description: Microsoft Active Accessibility verbessert die Art und Weise, wie Barrierefreiheitshilfen (spezielle Programme, die Personen mit Behinderungen helfen, Computer effektiver zu nutzen) mit Anwendungen arbeiten, die auf Microsoft Windows ausgeführt werden.
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e2bfd984dce863a2bdcdbd41d7b3d72b521861177bc4086a93eb578eb71c5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325151"
---
# <a name="technical-overview"></a>Technischer Überblick

Microsoft Active Accessibility verbessert die Art und Weise, wie Barrierefreiheitshilfen (spezielle Programme, die Personen mit Behinderungen helfen, Computer effektiver zu nutzen) mit Anwendungen arbeiten, die auf Microsoft Windows ausgeführt werden.

Microsoft Active Accessibility basiert auf dem Component Object Model (COM), das von Microsoft entwickelt wurde und ein Branchenstandard ist, der eine gemeinsame Methode für die Kommunikation von Anwendungen und Betriebssystemen definiert. Microsoft Active Accessibility besteht aus den folgenden Komponenten:

-   Die COM-Schnittstelle [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), die Informationen zu Benutzeroberflächenelementen verfügbar macht. **IAccessible** verfügt auch über Eigenschaften und Methoden zum Abrufen von Informationen zu und Bearbeiten dieses Benutzeroberflächenelements.
-   WinEvents, ein Ereignissystem, mit dem Server Clients benachrichtigen können, wenn sich ein barrierefreies Objekt ändert.
-   Oleacc.dll, eine Support- oder Laufzeit-DLL.

Die Microsoft Active Accessibility DLL Oleacc.dll besteht aus den folgenden Komponenten:

-   Funktionen, mit denen Clients einen [**IAccessible-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) anfordern können (z. B. [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).
-   Funktionen, mit denen Server einen [**IAccessible-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) an einen Client zurückgeben können (z. B. [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)).
-   Funktionen zum Abrufen von lokalisierten Text für die Rollen- und Statuscodes (z. B. [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) und [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).
-   Einige Hilfsfunktionen ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).
-   Code, der die Standardimplementierung von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für USER- und COMCTL-Standardsteuerelemente bereitstellt. Da diese **IAccessible** im Namen der Systemsteuerelemente implementieren, werden sie als *Proxys* bezeichnet.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Funktionsweise von Active Accessibility](how-active-accessibility-works.md)
-   [Active Accessibility Grundlagen](active-accessibility-basics.md)
-   [Serverrichtlinien](server-guidelines.md)
-   [Clientrichtlinien](client-guidelines.md)
-   [COM- und Unicode-Richtlinien](com-and-unicode-guidelines.md)

 

 




