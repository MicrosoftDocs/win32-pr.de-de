---
title: Was sind WinEvents?
description: Serveranwendungen und das Betriebssystem verwenden WinEvents, um Clients zu benachrichtigen, wenn eine Änderung im System oder auf der Benutzeroberfläche auftritt.
ms.assetid: 43723706-a173-4ddc-b135-824a7a8e8b40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c177183fa776a6becf52d62b86fe0ae6785c5be19dd287324ba3345b586af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563511"
---
# <a name="what-are-winevents"></a>Was sind WinEvents?

Serveranwendungen und das Betriebssystem verwenden WinEvents, um Clients zu benachrichtigen, wenn eine Änderung im System oder auf der Benutzeroberfläche auftritt.

Die WinEvent-Unterstützung ist ein Feature des Windows Betriebssystems, das Folgendes bietet:

-   Eine einfache Möglichkeit für Clients, sich für Ereignisbenachrichtigungen zu registrieren.
-   Ein Mechanismus zum Einfügen von Clientcode in Server.
-   Routing von Ereignissen von Servern zu interessierten Clients.
-   Automatische Ereignisgenerierung für die meisten **HWND-basierten** Steuerelemente.

Die Ereignisgenerierung für **HWND-basierte** Steuerelemente ist für Serverentwickler besonders wichtig. Die Microsoft Active Accessibility Laufzeit stellt [**IAccessible-Proxys**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für alle Standardelemente der Benutzeroberfläche bereit. Auf ähnliche Weise generiert das System automatisch die entsprechenden WinEvents, wenn es ein **HWND-basiertes** Steuerelement erstellt, zerstört, verschiebt, seine Größe annimmt oder eine andere Aktion ausführt.

Einige WinEvents, einschließlich allgemeiner **HWND-Ereignisse,** werden automatisch vom System unterstützt. Andere WinEvents-Typen, z. B. Zustandsänderungen oder Auswahlereignisse, die für ein bestimmtes Steuerelement spezifisch sind, werden von Microsoft Active Accessibility-Servern unterstützt.

Wenn ein Ereignis auftritt, das sich auf die Benutzeroberfläche auswirkt, können Server eine Ereignisbenachrichtigung an alle interessierten Clients senden, indem sie die [**NotifyWinEvent-Funktion**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) aufrufen. Der Funktionsaufruf enthält Informationen, die den Typ des aufgetretenen Ereignisses und das Ui-Element identifizieren, für das das Ereignis gilt. Clients können diese Informationen verwenden, um ein [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für das Benutzeroberflächenelement abzurufen und weitere Informationen zu sammeln.

Um Clients beispielsweise zu benachrichtigen, dass sich der Name eines Steuerelements geändert hat, ruft ein Server [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) auf und übergibt [**EVENT OBJECT \_ \_ NAMECHANGE**](event-constants.md) im Ereignisparameter. Das System antwortet, indem ermittelt wird, welche Clients sich für den Empfang dieses bestimmten Ereignisses registriert haben, und ruft die registrierte Rückruffunktion auf. Wenn sich keine Clients für das Ereignis registriert haben, ist der Aufruf des Servers für **NotifyWinEvent** mit einem "No-Vorgang" vergleichbar, und die Auswirkungen auf die Leistung sind vernachlässigbar.

Server rufen [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) auf, um das Ereignis an das System anzukündigen, nachdem das Ereignis aufgetreten ist. Sie dürfen das System nie über ein Ereignis benachrichtigen, bevor das Ereignis eintritt.

Clients registrieren Rückrufhookfunktionen mithilfe von [**SetWinEventHook,**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)um über Ereignisse benachrichtigt zu werden. Clients legen eine einzelne Hookfunktion für alle möglichen Ereignisse oder mehrere Hookfunktionen für diskrete Bereiche von Ereignissen fest. Weitere Informationen finden Sie unter [Registrieren einer Hookfunktion.](registering-a-hook-function.md)

Wenn Microsoft Active Accessibility über ein Ereignis benachrichtigt wird, ruft es alle Hookfunktionen auf, die für dieses Ereignis registriert wurden, und übergibt die Parameter von [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent).

 

 




