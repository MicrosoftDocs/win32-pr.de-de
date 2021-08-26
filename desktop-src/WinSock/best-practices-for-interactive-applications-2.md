---
description: Beim Umgestalten des Life Cell Update-Codes wurden mehrere Richtlinien zum Schreiben von Hochleistungsnetzwerkanwendungen entdeckt.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Bewährte Methoden für interaktive Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497fc56419f8859b7490671590b4589092c4c5b37047a01b0bf80cee9bf8c213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996900"
---
# <a name="best-practices-for-interactive-applications"></a>Bewährte Methoden für interaktive Anwendungen

Beim Umgestalten des Life Cell Update-Codes wurden mehrere Richtlinien zum Schreiben von Hochleistungsnetzwerkanwendungen entdeckt. Einige allgemeine Strategien, die beim Schreiben dieser Anwendungstypen angewendet werden sollten, sind:

-   Machen Sie den Datenstrom so weit wie möglich, anstatt in Blöcke zu gehen.
-   Verwenden Sie einige große Transaktionen anstelle vieler kleiner Transaktionen. Große Transaktionen können auch effizient gestreamt werden.
-   Erkennen Sie, dass das Netzwerk eine langsame, unzuverlässige Ressource ist, und entwickeln Sie jede Anwendung, um ihre Abhängigkeit vom Netzwerk zu minimieren.
-   Verwenden Sie eine gut durchdachte Darstellung der Daten im Netzwerk. Die Datendarstellung sollte computerarchitekturunabhängig sein, kein Fett enthalten und möglicherweise komprimiert werden.
-   Während des Initialisierens und Herunterfahrens darf der Benutzer nicht warten, bis das Netzwerk gestartet oder heruntergefahren wurde. Die netzwerkbezogene Initialisierung kann relativ lange dauern. Trennen Sie den nicht kritischen Netzwerkcode.
-   Behandeln Sie Fehler entsprechend ihren Auswirkungen. Nicht alle Fehler sind kritisch. Implementieren Sie Wiederherstellungsmechanismen, und geben Sie unintrusives Benutzerfeedback.
-   Verwenden Sie Remoteprozeduraufrufe (RPC) nur bei Bedarf. RPC ist auf Windows Me/98 synchron und führt immer zu fetten Protokollen, wenn kleine Datenmengen gesendet werden.
-   Messen Des Netzwerkaufwands mithilfe von Netstat Sie sind möglicherweise von ihren Messungen überrascht.
-   Testen Sie die Anwendung in einer Vielzahl von Netzwerken, insbesondere in langsamen oder verlustanfälligen Netzwerken. WLAN-Netzwerke, Modems und virtuelle private Netzwerke (VPN) über das Internet sind gute Netzwerke für Tests.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hochleistungsanwendungen für Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



