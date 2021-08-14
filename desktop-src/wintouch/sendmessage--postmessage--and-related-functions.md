---
title: SendMessage-, PostMessage- und verwandte Funktionen
description: In diesem Abschnitt werden Überlegungen zum Weiterleiten von Nachrichten mithilfe von SendMessage, PostMessage und verwandten Funktionen mit Touchnachrichten beschrieben.
ms.assetid: 9fba2013-17a3-499c-80dc-627e89c0edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1274327b53630058779bc3913ce4466394c4c4fa37ba78528d122b8d68e376e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435298"
---
# <a name="sendmessage-postmessage-and-related-functions"></a>SendMessage-, PostMessage- und verwandte Funktionen

In diesem Abschnitt werden Überlegungen zum Weiterleiten von Nachrichten mit [SendMessage,](/windows/desktop/api/winuser/nf-winuser-sendmessage) [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)und verwandten Funktionen mit Touchnachrichten beschrieben.

Wenn eine Touchnachricht mit [SendMessage,](/windows/desktop/api/winuser/nf-winuser-sendmessage) [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)oder einer anderen verwandten Funktion weitergeleitet wird, wird das Toucheingabehand handle geschlossen. Wenn Sie die Informationen abgerufen haben, auf die von einem Toucheingabehand handle durch einen Aufruf von [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)verwiesen wird, bleiben diese Daten gültig, bis Sie den Arbeitsspeicher frei geben.

Eine Anwendung, die Touchnachrichten empfängt, die über einen dieser Mechanismen weitergeleitet werden, besitzt das Toucheingabehandl, das sie in der *Nachrichten-LPARAM* empfängt, und ist für das Schließen verantwortlich. Wenn Sie das Handle nicht mit einem Aufruf von [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle)schließen, die Nachricht an [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)übergeben oder die Nachricht mithilfe von [SendMessage,](/windows/desktop/api/winuser/nf-winuser-sendmessage) [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)oder einer verwandten Funktion weiter senden, kommt es zu einem Speicherverlust.

> [!Note]  
> Touchnachrichten unterliegen normalen REGELN für Benutzeroberfläche Privilege Isolation (UIPI), wenn sie weitergeleitet werden.

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a>Funktionen im Zusammenhang mit SendMessage und PostMessage

Die folgenden Funktionen, die sich auf den Zustand des Toucheingabehandpunkts auswirken können.

-   [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)
-   [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   SendNotifyMessage
-   SendMessageCallback
-   SendMessageTimeout
-   PostThreadMessage

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Funktionen](mtfunctions.md)
</dt> <dt>

[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

 