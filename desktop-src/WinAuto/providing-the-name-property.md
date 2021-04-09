---
title: Bereitstellen der Name-Eigenschaft
description: Server Entwickler müssen sorgfältig vorgehen, wenn Sie vordefinierte und allgemeine Steuerelemente erstellen, um sicherzustellen, dass Microsoft Active Accessibility die Name-Eigenschaft für das Steuerelement verfügbar macht.
ms.assetid: 2b4ec5ae-bda1-41e6-9387-6ee3cb6c3163
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d7a4c30c6bc228785a886d9a41717f8cdb8dda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948837"
---
# <a name="providing-the-name-property"></a>Bereitstellen der Name-Eigenschaft

Server Entwickler müssen sorgfältig vorgehen, wenn Sie vordefinierte und allgemeine Steuerelemente erstellen, um sicherzustellen, dass Microsoft Active Accessibility die [Name-Eigenschaft](name-property.md) für das Steuerelement verfügbar macht. Abhängig vom Typ des Steuer Elements stammt der Text für die Name-Eigenschaft von einem der folgenden Elemente:

-   Der Fenster Text des Steuer Elements (oder die Beschriftung).
-   Statischer Text, der das Steuerelement bezeichnet

Um den Fenster Text des Steuer Elements zu ermitteln, sendet Microsoft Active Accessibility die [**WM- \_ gettext**](/windows/desktop/winmsg/wm-gettext) -Nachricht an das Steuerelement. Dieser Text entspricht dem Text-Parameter in der Resource Definition-Anweisung des-Steuer Elements. Bei einigen Steuerelementen, z. b. Schaltflächen, ist dies derselbe Text, der mit dem Steuerelement angezeigt wird. Bei anderen Steuerelementen, z. b. Symbolleisten, wird dieser Text nicht angezeigt. Daher müssen Server Entwickler sinnvollen Text in der Ressourcen Definitions Anweisung des-Steuer Elements bereitstellen, damit Benutzer von Client Dienstprogrammen das Steuerelement identifizieren können.

Um die Bezeichnung des Steuer Elements zu finden, sucht Microsoft Active Accessibility nach einem statischen Text Steuerelement, indem [**GetWindow**](/windows/desktop/api/winuser/nf-winuser-getwindow) mit dem GW- \_ Flag "hwndprev" aufgerufen wird. Die Suche wird angehalten, wenn ein statisches Text Steuerelement gefunden wird, oder wenn ein Steuerelement gefunden wird, das die Fenster Stile WS- \_ Gruppe \| WS \_ Tabstopps hat. Diese Such Reihenfolge entspricht der Reihenfolge der umgekehrten Registerkarten in einem Dialogfeld. Server Entwickler müssen beim Erstellen von Steuerelementen die Aktivier Reihenfolge beobachten, damit ein statisches Text Steuerelement unmittelbar vor dem Steuerelement liegt, das es bezeichnet.

Weitere Informationen zu den Methoden, die Microsoft Active Accessibility verwendet, um die [Name-Eigenschaft](name-property.md)verfügbar zu machen, finden Sie unter [User Interface Element Reference](user-interface-element-reference.md).

 

 