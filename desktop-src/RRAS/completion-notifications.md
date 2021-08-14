---
title: Vervollständigungsbenachrichtigungen
description: Der Remotezugriffsserver Verbindungs-Manager Statusbenachrichtigungen fortgesetzt, bis der Verbindungsvorgang abgeschlossen ist.
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6dcfad1ae0dfd4eefb3df00dceefce0df77d93239a6e7c2c4fa6517cac25e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791604"
---
# <a name="completion-notifications"></a>Vervollständigungsbenachrichtigungen

Der Remotezugriffsserver Verbindungs-Manager Statusbenachrichtigungen fortgesetzt, bis der Verbindungsvorgang abgeschlossen ist. Dies tritt in den folgenden Situationen auf:

-   Der Handler empfängt eine RASCS \_ Connected- oder RASCS \_ Disconnected-Benachrichtigung. Die RAS-Clientanwendung kann beendet werden, ohne eine verbindung herzustellen.
-   Ein Fehler tritt auf. Der Handler empfängt eine Benachrichtigung, die den Fehler und den Verbindungsstatus angibt, als der Fehler aufgetreten ist. Die RAS-Clientanwendung kann beendet werden.

Die RAS-Clientanwendung sollte nicht davon ausgehen, dass der Verbindungsvorgang nach dem Aufruf von [**RasHangUp abgeschlossen ist.**](/windows/desktop/api/Ras/nf-ras-rashangupa) Sie sollte auf eine der oben genannten Bedingungen warten, bevor sie beendet wird.

 

 




