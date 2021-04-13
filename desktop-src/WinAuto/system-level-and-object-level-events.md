---
title: Ereignisse System-Level und Object-Level
description: In Microsoft Active Accessibility werden drei Klassen der WinEvents-Systemebene, der Objektebene und der-Konsole verwendet.
ms.assetid: 3333fe6c-38cd-4e7e-be4b-94c9f824e7e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d14a0469527a7654dd3e323adb47d650866ca9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309740"
---
# <a name="system-level-and-object-level-events"></a>Ereignisse System-Level und Object-Level

In Microsoft Active Accessibility werden drei Klassen von WinEvents verwendet: *Systemebene*, *Objektebene* und *Konsole*. Jede verfügt über einen der folgenden entsprechenden [Ereignis Konstanten](event-constants.md) Werte:

-   Ereignis Konstanten, die mit dem Ereignis System beginnen, \_ identifizieren Ereignisse auf System Ebene. Diese Ereignisse beschreiben Situationen, die sich auf alle Anwendungen im System auswirken.
-   Ereignis Konstanten, die mit dem Ereignis Objekt beginnen, \_ identifizieren Ereignisse auf Objektebene. Diese Ereignisse beziehen sich auf spezifische Situationen von Objekten in einer Anwendung.
-   Ereignis Konstanten, die mit der Ereignis Konsole beginnen, \_ identifizieren Ereignisse auf Konsolen Ebene. Diese Ereignisse weisen auf Änderungen in den Konsolen Fenstern hin.

Die Klassen der System-und Objektebene werden von den Betriebssystem-und Server Anwendungen generiert. Das Betriebssystem generiert Ereignisse auf Systemebene und auf Objektebene für die folgenden Szenarien:

-   System weite Benachrichtigungen zu Fokus Änderungen
-   Aktivierungs Änderungen
-   Ereignisse für vom System bereitgestellte Objekte, z. b. allgemeine Steuerelemente

Server Anwendungen generieren Ereignisse auf Systemebene für benutzerdefinierte Objekte, die Systemobjekte replizieren, z. b. benutzerdefinierte Menüs und Bild Lauf leisten.

Server Anwendungen generieren in der Regel Ereignisse auf Objektebene für Änderungen an den zugänglichen Objekten, die Sie enthalten, z. b. Objekt Erstellung, Zerstörung und Auswahl.

Obwohl das Systemereignisse auf Objektebene für [**Fenster**](window.md) Objekte generiert, müssen Server auch Ereignisse auf Objektebene für jedes in einem Fenster enthaltene barrierefreie Objekt senden. Wenn z. b. eine Serveranwendung eine Anwendungs definierte Fenster Klasse zum Erstellen eines benutzerdefinierten Steuer Elements registriert, generiert das Systemereignisse auf Objektebene für das Fenster, das das benutzerdefinierte Steuerelement enthält. der Server generiert Ereignisse auf Objektebene für das barrierefreie Objekt, das Informationen über das Steuerelement bereitstellt.

Server generieren nur Ereignisse auf Objektebene für die benutzerdefinierten Steuerelemente, für die Sie die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle implementieren. Weitere Informationen finden Sie unter Benutzer [definierte Benutzeroberflächen Elemente](custom-user-interface-elements.md).

 

 




