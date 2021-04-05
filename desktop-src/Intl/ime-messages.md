---
description: Das Betriebssystem sendet IME-Fenster Meldungen an die Fenster Prozedur einer Anwendung, wenn bestimmte Ereignisse auftreten, die sich auf die IME-Fenster auswirken.
ms.assetid: 7eac1ab7-d04b-4e1b-9e2c-fa9a778756cd
title: IME-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f30baa01081e0aca1423f3384926938e6fdc07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041802"
---
# <a name="ime-messages"></a>IME-Nachrichten

Das Betriebssystem sendet IME-Fenster Meldungen an die Fenster Prozedur einer Anwendung, wenn bestimmte Ereignisse auftreten, die sich auf die IME-Fenster auswirken. Beispielsweise sendet das Betriebssystem die " [**WM \_ IME \_ SetContext**](wm-ime-setcontext.md) "-Meldung an die Anwendung, wenn ein Fenster aktiviert wird. IME-unbekannte Anwendungen übergeben diese Nachrichten an die [defwindowproc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion, die Sie an das entsprechende Standard-IME-Fenster sendet. IME-fähige Anwendungen verarbeiten diese Nachrichten oder leiten Sie an Ihre eigenen IME-Fenster weiter.

Die Anwendung kann ein IME-Fenster anweisen, einen Befehl auszuführen, z. b. die Position eines Kompositions Fensters mithilfe der WM- [**\_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung zu ändern. Der IME benachrichtigt die Anwendung über Änderungen an der Kompositions Zeichenfolge unter Verwendung der [**WM \_ IME- \_ Kompositions**](wm-ime-composition.md) Nachricht und über allgemeine Änderungen am Status der IME-Fenster durch Senden der [**WM-IME- \_ \_ Benachrichtigungs**](wm-ime-notify.md) Meldung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über den Eingabemethoden-Manager](about-input-method-manager.md)
</dt> </dl>

 

 
