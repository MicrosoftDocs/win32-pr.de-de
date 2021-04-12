---
title: Erstellen geeigneter WinEvents
description: Server Entwickler müssen sicherstellen, dass für alle Elemente der Benutzeroberfläche geeignete WinEvents generiert werden, einschließlich Fenster basierter Benutzeroberflächen Elemente, fensterlose Benutzeroberflächen Elemente und Benutzeroberflächen Elemente mit stark angepassten Verhaltensweisen.
ms.assetid: 253e0162-20e6-4e89-b563-aae9cf7e53a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6273411115e908303e863a34908e15ef91b19c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207164"
---
# <a name="generating-appropriate-winevents"></a>Erstellen geeigneter WinEvents

Server Entwickler müssen sicherstellen, dass für alle Elemente der Benutzeroberfläche geeignete WinEvents generiert werden, einschließlich Fenster basierter Benutzeroberflächen Elemente, fensterlose Benutzeroberflächen Elemente und Benutzeroberflächen Elemente mit stark angepassten Verhaltensweisen.

Der Benutzer stellt standardmäßige WinEvent-Unterstützung für Standard-, **HWND**-basierte Benutzeroberflächen Elemente bereit. Da der Benutzer diese Ereignisse automatisch generiert, müssen Server nur Ereignisse für benutzerdefinierte Steuerelemente, fensterlose Elemente oder Steuerelemente generieren, deren Ereignisse nicht bereits vom Benutzer generiert wurden.

Um ein Ereignis zu senden, wird [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) von Servern aufgerufen und die Ereignis Konstante, eine Objekt-ID und das **HWND** für ein Fenster übergeben, das auf Client Anforderungen reagieren kann, um weitere Informationen zu erhalten. Die Ereignisse, die ausgelöst werden müssen, variieren je nach Art des Benutzeroberflächen Elements. Es gibt allgemeine Ereignisse, die für alle Steuerelemente gesendet werden sollen, und bestimmte Ereignisse, die nur für das entsprechende Benutzeroberflächen Element gesendet werden sollen.

## <a name="general-events"></a>Allgemeine Ereignisse

Allgemeine WinEvents können für alle Benutzeroberflächen Elemente gesendet werden. Dazu gehören:

-   [**Ereignis \_ Objekt \_ Erstellen**](event-constants.md) (wenn ein Objekt erstellt wird)
-   [**Ereignis \_ Objekt \_ zerstören**](event-constants.md) (wenn ein Objekt zerstört wird)
-   [**Ereignis \_ Objekt \_ Anzeige**](event-constants.md) (wenn ein Objekt angezeigt wird)
-   [**Ereignis \_ Objekt \_ Ausblenden**](event-constants.md) (wenn ein Objekt ausgeblendet ist)

## <a name="specific-events"></a>Bestimmte Ereignisse

Es gibt auch bestimmte WinEvents, die für einen bestimmten Typ von Benutzeroberflächen Elementen gesendet werden können. Verwenden Sie z. b. die [**Ereignis \_ Objekt \_ Auswahl**](event-constants.md) für Steuerelemente, die es dem Benutzer ermöglichen, eine Auswahl vorzunehmen, z. b. ein Listenfeld.

Weitere Informationen zu den Ereignissen, die für eine bestimmte Art von Benutzeroberflächen Element erwartet werden, finden Sie in den folgenden Ressourcen:

-   [Anhang A: Unterstützte Elemente der Benutzeroberflächen Elemente](appendix-a--supported-user-interface-elements-reference.md). Dieser Anhang enthält Informationen zu vom System generierten UI-Elementen, die von Microsoft Active Accessibility verfügbar gemacht werden. Die Dokumentation für jedes Steuerelement enthält Informationen zu Ereignissen, die vom Benutzeroberflächen Element generiert werden können.
-   [Ereignis Konstanten](event-constants.md). Dieses Thema enthält Informationen zu Ereignissen, die vom Betriebssystem und von Server Anwendungen generiert werden.
-   Barrierefreie Ereignisüberwachung (AccEvent.exe). Dieses Tool zeigt, welche Ereignisse Benutzer für ein bestimmtes UI-Element sendet. Sie können dieses Tool verwenden, um zu erfahren, welche Ereignisse Sie für ein UI-Element erwarten können. Weitere Informationen finden Sie unter [barrierefreie ereigniswatcher](accessible-event-watcher.md).

 

 




