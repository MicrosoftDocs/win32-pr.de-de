---
title: MCI-Befehls Zeichenfolgen und-Meldungen
description: MCI-Befehls Zeichenfolgen und-Meldungen
ms.assetid: eb60c96b-e89e-4673-a8e0-98fabe4af7ca
keywords:
- MCI-Befehls Zeichenfolgen, Informationen zu
- MCI-Befehls Meldungen, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a317442280b8fb4c7afe7832205b1c7128513
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858258"
---
# <a name="mci-command-strings-and-messages"></a>MCI-Befehls Zeichenfolgen und-Meldungen

MCI unterstützt [Befehls](command-strings.md) Zeichenfolgen und [Befehls Meldungen](command-messages.md). In ihrer MCI-Anwendung können Sie entweder Zeichen folgen oder Nachrichten oder beides verwenden.

-   Die *befehlsnachrichten Schnittstelle* besteht aus Konstanten und Strukturen. Verwenden Sie die Funktion " [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) ", um Nachrichten an ein MCI-Gerät zu senden.
-   Die *Befehls Zeichenfolgen-Schnittstelle* stellt eine Textversion der Befehls Meldungen bereit. Verwenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion, um Zeichen folgen an ein MCI-Gerät zu senden. Befehls Zeichenfolgen duplizieren die Funktionalität der Befehls Meldungen. Das Betriebssystem konvertiert die Befehls Zeichenfolgen in Befehls Meldungen, bevor diese zur Verarbeitung an den MCI-Treiber gesendet werden.

Die Befehlszeilen, die Informationen abrufen, weisen dies in Form von Strukturen auf, die in einer C-Anwendung leicht interpretiert werden können. Diese Strukturen können Informationen zu vielen verschiedenen Aspekten eines Geräts enthalten. Die Befehls Zeichenfolgen, die Informationen abrufen, führen dies in Form von Zeichen folgen aus und können jeweils nur eine Zeichenfolge abrufen. Die Anwendung muss jede Zeichenfolge analysieren oder testen, um Sie zu interpretieren. In einigen Fällen können Sie feststellen, dass die Befehlszeilen einfacher zu verwenden sind als die Befehls Zeichenfolgen, aber die Befehls Zeichenfolgen sind leicht zu merken und zu implementieren. Einige MCI-Anwendungen verwenden Befehls Zeichenfolgen, wenn der Rückgabewert nicht (außer zum Überprüfen des Erfolgs) und Befehls Meldungen beim Abrufen von Informationen vom Gerät verwendet wird.

Bei der Erörterung von Befehlen wird in dieser Übersicht die Zeichen folgen Form des Befehls verwendet, gefolgt vom Nachrichten Formular in Klammern.

 

 