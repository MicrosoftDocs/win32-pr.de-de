---
title: SendMessage, PostMessage und verwandte Funktionen
description: In diesem Abschnitt werden Überlegungen zum Weiterleiten von Nachrichten mit SendMessage, PostMessage und verwandten Funktionen mit Berührungs Nachrichten beschrieben.
ms.assetid: 9fba2013-17a3-499c-80dc-627e89c0edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fc42e31f3c971c704d18f04a961fb6bd40eb91d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390638"
---
# <a name="sendmessage-postmessage-and-related-functions"></a>SendMessage, PostMessage und verwandte Funktionen

In diesem Abschnitt werden Überlegungen zum Weiterleiten von Nachrichten mit [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)und verwandten Funktionen mit Berührungs Nachrichten beschrieben.

Wenn eine Fingereingabe Nachricht mit [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [Post Message](/windows/win32/api/winuser/nf-winuser-postmessagea)oder einer anderen verknüpften Funktion weitergeleitet wird, wird das Fingereingabe Handle geschlossen. Wenn Sie die Informationen, auf die von einem Fingereingabe handle verwiesen wird, über einen aufgerufenen [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)abgerufen haben, bleiben diese Daten gültig, bis Sie den Arbeitsspeicher freigeben.

Eine Anwendung, die über einen dieser Mechanismen weitergeleitete Berührungs Nachrichten empfängt, besitzt das Fingereingabe handle, das in der Nachricht *LPARAM* empfangen wird und für deren Schließung zuständig ist. Wenn Sie das Handle nicht mit einem Rückruf von [**closetouchinputhandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle)schließen, die Nachricht an [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)übergeben oder die Nachricht mit [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)oder einer zugehörigen Funktion weiterleiten, liegt ein Speicherfehler vor.

> [!Note]  
> Berührungs Nachrichten unterliegen den normalen UIPI-Regeln (User Interface Privilege Isolation), wenn Sie weitergeleitet werden.

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a>Funktionen im Zusammenhang mit SendMessage und PostMessage

Die folgenden Funktionen, die den Zustand des Berührungs Eingabe Handles beeinflussen können.

-   [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)
-   [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   Sendnotisymess
-   Sendmessagecallback
-   Von SendMessageTimeout
-   PostThreadMessage

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Funktionen](mtfunctions.md)
</dt> <dt>

[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

 