---
title: Generieren geeigneter WinEvents
description: Serverentwickler müssen sicherstellen, dass geeignete WinEvents für alle Benutzeroberflächenelemente generiert werden, einschließlich fensterbasierter Ui-Elemente, fensterloser UI-Elemente und Benutzeroberflächenelemente mit hochgradig angepasstem Verhalten.
ms.assetid: 253e0162-20e6-4e89-b563-aae9cf7e53a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e148578f55f59d2827fd13a637baf5139c3f934ddf24059e437185c15349b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860390"
---
# <a name="generating-appropriate-winevents"></a>Generieren geeigneter WinEvents

Serverentwickler müssen sicherstellen, dass geeignete WinEvents für alle Benutzeroberflächenelemente generiert werden, einschließlich fensterbasierter Ui-Elemente, fensterloser UI-Elemente und Benutzeroberflächenelemente mit hochgradig angepasstem Verhalten.

USER bietet Standardmäßige WinEvent-Unterstützung für **HWND-basierte Standardelemente** der Benutzeroberfläche. Da USER diese Ereignisse automatisch generiert, müssen Server Ereignisse nur für benutzerdefinierte Steuerelemente, fensterlose Elemente oder Steuerelemente generieren, deren Ereignisse nicht bereits von USER generiert wurden.

Um ein Ereignis zu senden, rufen Die Server [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) auf und übergeben die Ereigniskonstante, eine Objekt-ID und den **HWND** für ein Fenster, das auf Clientanforderungen reagieren kann, um weitere Informationen zu erhalten. Die Ereignisse, die ausgelöst werden müssen, variieren je nach Typ des Benutzeroberflächenelements. Es gibt allgemeine Ereignisse, die für alle Steuerelemente gesendet werden sollen, und bestimmte Ereignisse, die nur für das entsprechende Benutzeroberflächenelement gesendet werden sollen.

## <a name="general-events"></a>Allgemeine Ereignisse

Allgemeine WinEvents können für alle Benutzeroberflächenelemente gesendet werden. Dazu zählen unter anderem folgende Einstellungen:

-   [**EVENT \_ OBJECT \_ CREATE**](event-constants.md) (wenn ein Objekt erstellt wird)
-   [**EVENT \_ OBJECT \_ DESTROY**](event-constants.md) (wenn ein Objekt zerstört wird)
-   [**EVENT \_ OBJECT \_ SHOW**](event-constants.md) (wenn ein Objekt angezeigt wird)
-   [**EVENT \_ OBJECT \_ HIDE**](event-constants.md) (wenn ein Objekt ausgeblendet ist)

## <a name="specific-events"></a>Bestimmte Ereignisse

Es gibt auch bestimmte WinEvents, die für einen bestimmten Benutzeroberflächenelementtyp gesendet werden können. Verwenden Sie beispielsweise [**EVENT \_ OBJECT \_ SELECTION**](event-constants.md) für Steuerelemente, die es dem Benutzer ermöglichen, eine Auswahl zu treffen, z. B. ein Listenfeld.

Weitere Informationen dazu, welche Ereignisse für einen bestimmten Benutzeroberflächenelementtyp erwartet werden, finden Sie in den folgenden Ressourcen:

-   [Anhang A: Unterstützte Benutzeroberfläche-Elemente verweisen auf](appendix-a--supported-user-interface-elements-reference.md). Dieser Anhang enthält Informationen zu vom System generierten UI-Elementen, die von Microsoft Active Accessibility verfügbar gemacht werden. Die Dokumentation für jedes Steuerelement enthält Informationen zu Ereignissen, die vom Benutzeroberflächenelement generiert werden können.
-   [Ereigniskonstanten](event-constants.md). Dieses Thema enthält Informationen zu Ereignissen, die von den Betriebssystem- und Serveranwendungen generiert werden.
-   Barrierefreier Event Watcher (AccEvent.exe). Dieses Tool zeigt, welche Ereignisse DER BENUTZER für ein bestimmtes Benutzeroberflächenelement sendet. Sie können dieses Tool verwenden, um zu erfahren, welche Ereignisse Sie für ein Benutzeroberflächenelement erwarten können. Weitere Informationen finden Sie unter [Accessible Event Watcher](accessible-event-watcher.md).

 

 




