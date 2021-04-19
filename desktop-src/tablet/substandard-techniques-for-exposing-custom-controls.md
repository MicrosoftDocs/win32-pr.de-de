---
description: Beschreibung der unter Standardtechniken zum verfügbar machen von benutzerdefinierten Steuerelementen.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Unter Standardtechniken zum verfügbar machen von benutzerdefinierten Steuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194614474596b55e0b1cf0530a07f9b3c411f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359193"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a>Unter Standardtechniken zum verfügbar machen von benutzerdefinierten Steuerelementen

Wenn eine Anwendung Microsoft Active Accessibility nicht unterstützt, ist Sie möglicherweise nicht vollständig zugänglich. Die folgenden Techniken zum Rendering von Steuerelementen sind teilweise kompatibel:

-   Gibt eine beschreibende Zeichenfolge zurück, wenn das Steuerelement mithilfe der WM-gettext-Nachricht abgefragt wird \_ . Gestatten Sie z. b. einem benutzerdefinierten Äquivalent eines Schaltflächen-Steuer Elements mit der Bezeichnung "Print", die Zeichenfolge "Print Button" zurückzugeben. Dadurch werden sowohl der Steuerelement Typ als auch die Bezeichnung identifiziert Die gleiche Zeichenfolge eignet sich für eine Schaltfläche mit einer Bezeichnung, die etwas anderes als Text ist, z. b. eine Grafik eines Druckers. Gleichermaßen können Sie zulassen, dass ein benutzerdefiniertes Steuerelement, das sich wie ein Kontrollkästchen verhält, die Beschriftungs Zeichenfolge "Druck aktiviert" zurückgibt.
-   Unterstützung der WM- \_ getdlgcode-Meldung, die die unterstützte Tastatureingabe identifiziert. Gestatten Sie z. b. einem benutzerdefinierten Äquivalent eines Bearbeitungs Steuer Elements, WM \_ getdlgcode zu behandeln, indem Sie dlgc \_ hassetsel zurückgeben, wenn Nachrichten zum Festlegen der Auswahl verarbeitet werden, dlgc \_ wantpfeile bei Verwendung von Pfeiltasten und dlgc- \_ wantchars, um anzugeben, dass es Zeichen Eingaben verwendet.
    > [!Note]  
    > Nur Steuerelemente, die über eigene Fenster Handles verfügen, können auf die \_ Nachrichten WM gettext und WM \_ getdlgcode Antworten.

     

Um Kompatibilitätsprobleme mit Hilfen bei der Barrierefreiheit zu vermeiden, sollten Sie beim Entwerfen von benutzerdefinierten Steuerelementen genau Active Accessibility Richtlinien befolgen. Weitere Informationen zum Vermeiden von Kompatibilitätsproblemen mit hilfshilfen finden Sie im Abschnitt zur [Barrierefreiheit](../accessibility/accessibility.md) .

 

 
