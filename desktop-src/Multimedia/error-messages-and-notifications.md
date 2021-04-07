---
title: Fehlermeldungen und Benachrichtigungen
description: Fehlermeldungen und Benachrichtigungen
ms.assetid: 7f804364-d8be-4e52-ab0e-fba05bcf76ce
keywords:
- Mciwndgeterror-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e40e78c72dc378baa37b56dbb2d5718ae2d85b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038886"
---
# <a name="error-messages-and-notifications"></a>Fehlermeldungen und Benachrichtigungen

Mciwnd verwendet MCI zum Steuern der Geräte, die Multimedia-Daten wiedergeben und aufzeichnen. Im Allgemeinen zeigt mciwnd MCI-Fehler in einem Fehler Dialogfeld an. Ein MCI-Fehler wird generiert, wenn ein MCI-Befehl fehlschlägt. Wenn die Anwendung z. b. versucht, die angehaltene Wiedergabe mit dem [**mciwndresume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) -Makro fortzusetzen, und das aktuelle Gerät die Wiederaufnahme nicht unterstützt, wird dem Benutzer ein Fehler gemeldet.

Mciwnd ermöglicht Ihnen zwei Optionen für die Behandlung von Fehlermeldungen:

-   Sie können verhindern, dass Fehlermeldungen den Benutzer erreichen. Wenn Sie die Anzeige von MCI-Fehlermeldungen verhindern möchten, geben Sie das Fenster Format mciwndf \_ noerrordlg an, wenn Sie eine Instanz eines mciwnd-Fensters mithilfe der Funktion " [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) " oder " [deatewindowex](/windows/win32/api/winuser/nf-winuser-createwindowexa) " erstellen.
-   Sie können Sie zur Anzeige an Ihre Anwendung umleiten. Wenn Sie MCI-Fehlermeldungen an Ihre Anwendung umleiten möchten, geben Sie das Fenster Format mciwndf \_ notifyerror an, wenn Sie eine Instanz eines mciwnd-Fensters mithilfe von " **mciwndcreate** " oder " **kreatewindowex**" erstellen.

Wenn die Fehler Benachrichtigung aktiviert ist, sendet mciwnd jede Benachrichtigungs Meldung ([**mciwndm \_ notifyerror**](mciwndm-notifyerror.md)) an den Hauptnachrichten Handler des übergeordneten Elements des mciwnd-Fensters. Die Anwendung muss über einen Nachrichten Handler verfügen, um die empfangenen Benachrichtigungs Meldungen zu verarbeiten.

Eine Textbeschreibung der neuesten MCI-Fehlermeldung erhalten Sie, indem Sie das [**mciwndgeterror**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) -Makro verwenden. Dieses Makro gibt den Text in einem Anwendungs definierten Puffer zurück. Wenn die Fehler Zeichenfolge länger als der Puffer ist, wird die Zeichenfolge von mciwnd abgeschnitten.

Sie können alle Benachrichtigungen mithilfe des [**mciwndseetowner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) -Makros an ein anderes Fenster weiterleiten.

 

 