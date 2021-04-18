---
description: Wenn Sie den Code für die Lebensdauer der Zelle ändern, wurden mehrere Richtlinien für das Schreiben von hochleistungsfähigen Netzwerkanwendungen entdeckt.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Bewährte Methoden für interaktive Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89764cf19de223f4622edd947c8122bc7fe8b11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354478"
---
# <a name="best-practices-for-interactive-applications"></a>Bewährte Methoden für interaktive Anwendungen

Wenn Sie den Code für die Lebensdauer der Zelle ändern, wurden mehrere Richtlinien für das Schreiben von hochleistungsfähigen Netzwerkanwendungen entdeckt. Beim Schreiben dieser Arten von Anwendungen gelten die folgenden allgemeinen Strategien:

-   Machen Sie den Datenstrom so weit wie möglich, anstatt in Blöcke zu gehen.
-   Verwenden Sie ein paar große Transaktionen, anstatt viele kleine Transaktionen zu verwenden. Große Transaktionen können auch effizient gestreamt werden.
-   Erkennen Sie, dass das Netzwerk eine langsame und unzuverlässige Ressource ist, und entwickeln Sie jede Anwendung, um die Netzwerk Abhängigkeit zu minimieren.
-   Verwenden Sie eine gut konstruierte Darstellung der Daten im Netzwerk. Die Datendarstellung sollte Computerarchitektur agnostisch sein, kein FAT enthalten und möglicherweise komprimiert werden.
-   Lassen Sie den Benutzer während der Initialisierung und des herunter Fahrens nicht warten, bis das Netzwerk gestartet oder heruntergefahren wird. Die netzwerkbezogene Initialisierung kann relativ lange dauern. Trennen Sie den nicht kritischen Netzwerkcode.
-   Behandeln Sie Fehler entsprechend ihren Auswirkungen. Nicht alle Fehler sind von entscheidender Bedeutung. Implementieren von Wiederherstellungs Mechanismen und Bereitstellen von nicht eindringlichem Benutzer Feedback.
-   Verwenden Sie Remote Prozedur Aufrufe (RPC) nur, wenn dies angebracht ist. RPC ist unter Windows Me/98 synchron und führt immer zu einer Chatty, FAT-Protokolle, wenn Sie zum Senden kleiner Datenmengen verwendet werden.
-   Messen Sie den Netzwerk Aufwand mithilfe von netstat. Möglicherweise sind Sie überrascht, was Ihre Messungen zeigen.
-   Testen Sie die Anwendung in einer Vielzahl von Netzwerken, insbesondere bei langsamen oder Ausfall anfälligen Netzwerken. Drahtlose LAN-Netzwerke, Modems und virtuelle private Netzwerke (VPN) über das Internet sind gute Netzwerke für Tests.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hochleistungsfähige Windows Sockets-Anwendungen](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



