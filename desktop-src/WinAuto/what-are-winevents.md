---
title: Was sind WinEvents?
description: Server Anwendungen und das Betriebssystem verwenden WinEvents, um Clients zu benachrichtigen, wenn eine Änderung im System oder in der Benutzeroberfläche auftritt.
ms.assetid: 43723706-a173-4ddc-b135-824a7a8e8b40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97864f2b1464718680d781ad843345f1e46fce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340235"
---
# <a name="what-are-winevents"></a>Was sind WinEvents?

Server Anwendungen und das Betriebssystem verwenden WinEvents, um Clients zu benachrichtigen, wenn eine Änderung im System oder in der Benutzeroberfläche auftritt.

Die Unterstützung von WinEvent ist eine Funktion des Windows-Betriebssystems, die Folgendes bereitstellt:

-   Eine einfache Möglichkeit für Clients, sich für Ereignis Benachrichtigungen zu registrieren.
-   Ein Mechanismus zum Einfügen von Client Code in Server.
-   Routing von Ereignissen von Servern an interessierte Clients.
-   Automatische Ereignis Generierung für die meisten **HWND**-basierten Steuerelemente.

Die Ereignis Generierung für **HWND**-basierte Steuerelemente ist besonders wichtig für Server Entwickler. Die Microsoft Active Accessibility-Laufzeit stellt [**ibarrierefreie**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Proxys für alle Standardbenutzer Oberflächen Elemente bereit. Auf ähnliche Weise generiert das System automatisch die entsprechenden WinEvents, wenn es eine beliebige andere Aktion für ein **HWND**-basiertes Steuerelement erstellt, zerstört, verschoben, verkleinert oder ausführt.

Einige WinEvents, einschließlich allgemeiner **HWND** -Ereignisse, werden automatisch vom System unterstützt. Andere Typen von WinEvents, z. b. Zustandsänderungen oder Auswahl Ereignisse, die für ein bestimmtes Steuerelement spezifisch sind, werden von Microsoft Active Accessibility-Servern unterstützt.

Wenn ein Ereignis auftritt, das die Benutzeroberfläche beeinflusst, können Server eine Ereignis Benachrichtigung an alle interessierten Clients senden, indem Sie die [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) -Funktion aufrufen. Der Funktions aufruer enthält Informationen, die den Typ des aufgetretenen Ereignisses und das Benutzeroberflächen Element, auf das das Ereignis angewendet wird, identifiziert. Clients können diese Informationen verwenden, um ein [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt für das UI-Element abzurufen und weitere Informationen zu sammeln.

Um z. b. Clients zu benachrichtigen, dass sich der Name eines Steuer Elements geändert hat, Ruft ein Server [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) auf und übergibt [**Ereignis \_ Objekt \_ NameChange**](event-constants.md) im Ereignis Parameter. Das System reagiert, indem er festlegt, welche Clients registriert wurden, um das jeweilige Ereignis zu empfangen, und ruft die registrierte Rückruffunktion auf. Wenn keine Clients für das Ereignis registriert sind, ist der-Rückruf des **Servers mit dem** Hinweis "kein Vorgang" vergleichbar, und die Auswirkungen auf die Leistung sind unerheblich.

Server wenden [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) an, um das Ereignis für das System anzukündigen, nachdem das Ereignis aufgetreten ist. Sie müssen das System eines Ereignisses niemals Benachrichtigen, bevor das Ereignis auftritt.

Um über Ereignisse benachrichtigt zu werden, registrieren Clients Rückruf-Hook-Funktionen mithilfe von [**setwineventhook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook). Clients legen eine einzelne Hook-Funktion für alle möglichen Ereignisse oder mehrere Hook-Funktionen für diskrete Bereiche von Ereignissen fest. Weitere Informationen finden Sie unter [Registrieren einer Hookfunktion](registering-a-hook-function.md).

Wenn Microsoft Active Accessibility über ein Ereignis benachrichtigt wird, ruft es alle Hookfunktionen auf, die für dieses Ereignis registriert wurden, und übergibt die Parameter von [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent).

 

 




