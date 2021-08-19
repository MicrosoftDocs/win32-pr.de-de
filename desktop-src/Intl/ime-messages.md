---
description: Das Betriebssystem sendet IME-Fenstermeldungen an die Fensterprozedur einer Anwendung, wenn bestimmte Ereignisse auftreten, die sich auf die IME-Fenster auswirken.
ms.assetid: 7eac1ab7-d04b-4e1b-9e2c-fa9a778756cd
title: IME-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa34228f695a18187654707668067ac34562098b48aae185a8d66d777b6f507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949261"
---
# <a name="ime-messages"></a>IME-Nachrichten

Das Betriebssystem sendet IME-Fenstermeldungen an die Fensterprozedur einer Anwendung, wenn bestimmte Ereignisse auftreten, die sich auf die IME-Fenster auswirken. Beispielsweise sendet das Betriebssystem die [**WM \_ IME \_ SETCONTEXT-Meldung**](wm-ime-setcontext.md) an die Anwendung, wenn ein Fenster aktiviert wird. IME-nicht ime-Anwendungen übergeben diese Nachrichten an die [DefWindowProc-Funktion,](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die sie an das entsprechende STANDARD-IME-Fenster sendet. IME-orientierte Anwendungen verarbeiten diese Nachrichten entweder oder senden sie an ihre eigenen IME-Fenster.

Ihre Anwendung kann ein IME-Fenster anleiten, um einen Befehl auszuführen, z. B. die Position eines Kompositionsfensters mithilfe der [**WM \_ IME \_ CONTROL-Meldung zu**](wm-ime-control.md) ändern. Der IME benachrichtigt die Anwendung über Änderungen an der Kompositionszeichenfolge mithilfe der [**WM \_ IME \_ COMPOSITION-Meldung**](wm-ime-composition.md) und über allgemeine Änderungen am Status der IME-Fenster durch Senden der [**WM \_ IME \_ NOTIFY-Meldung.**](wm-ime-notify.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Eingabemethode-Manager](about-input-method-manager.md)
</dt> </dl>

 

 
