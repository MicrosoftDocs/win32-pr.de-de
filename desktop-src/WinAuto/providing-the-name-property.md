---
title: Bereitstellen der Name-Eigenschaft
description: Serverentwickler müssen beim Erstellen vordefinierter und gängiger Steuerelemente darauf achten, dass Microsoft Active Accessibility die Name-Eigenschaft für das Steuerelement verfügbar machen können.
ms.assetid: 2b4ec5ae-bda1-41e6-9387-6ee3cb6c3163
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c93205430f3063b993c49a7145658d7748aac0e697257789c31ac0653d6189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052548"
---
# <a name="providing-the-name-property"></a>Bereitstellen der Name-Eigenschaft

Serverentwickler müssen beim Erstellen vordefinierter und gängiger Steuerelemente darauf achten, dass Microsoft Active Accessibility die [Name-Eigenschaft](name-property.md) für das Steuerelement verfügbar machen können. Abhängig vom Typ des Steuerelements stammt der Text für die Name-Eigenschaft aus einem der folgenden:

-   Der Fenstertext (oder die Beschriftung) des Steuerelements
-   Statischer Text, der das Steuerelement bezeichnet

Um den Fenstertext des Steuerelements zu finden, sendet Microsoft Active Accessibility [**WM \_ GETTEXT-Nachricht**](/windows/desktop/winmsg/wm-gettext) an das Steuerelement. Dieser Text entspricht dem Textparameter in der Ressourcendefinitions-Anweisung des Steuerelements. Bei einigen Steuerelementen, z. B. Schaltflächen, ist dies derselbe Text, der mit dem -Steuerelement angezeigt wird. Bei anderen Steuerelementen, z. B. Symbolleisten, wird dieser Text nicht angezeigt. Daher müssen Serverentwickler aussagekräftigen Text in der Ressourcendefinitions-Anweisung des Steuerelements bereitstellen, damit Benutzer von Client-Hilfsprogrammen das Steuerelement identifizieren können.

Um die Bezeichnung des Steuerelements zu finden, Microsoft Active Accessibility durch Aufrufen von [**GetWindow**](/windows/desktop/api/winuser/nf-winuser-getwindow) mit dem GW HWNDPREV-Flag nach einem statischen \_ Textsteuerfeld suchen. Die Suche wird angehalten, wenn ein statisches Textsteuerfeld gefunden wird oder wenn ein Steuerelement mit den Fensterformaten WS \_ GROUP \| WS \_ TABSTOP gefunden wird. Diese Such reihenfolge entspricht der umgekehrten Registerkarten reihenfolge in einem Dialogfeld. Serverentwickler müssen die Reihenfolge der Registerkarten beim Erstellen von Steuerelementen beachten, damit ein statisches Textsteuerfeld unmittelbar vor dem Steuerelement, das es bezeichnet, vorangegangen ist.

Weitere Informationen zu den Techniken, die Microsoft Active Accessibility, um die [Name-Eigenschaft](name-property.md)verfügbar zu machen, finden Sie unter [Benutzeroberfläche Elementreferenz.](user-interface-element-reference.md)

 

 