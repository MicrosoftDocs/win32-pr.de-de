---
title: Wiedergabe und Positionierung
description: Wiedergabe und Positionierung
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9993c2ed4402184d2b15d5c3e54bb0137d1e7a3fe34f8cca36559ca329ada9d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892970"
---
# <a name="playback-and-positioning"></a>Wiedergabe und Positionierung

Eine Reihe von MCI-Befehlen, z. B. Wiedergabe [**(**](play.md) [**MCI \_ PLAY**](mci-play.md)), [**Beenden**](stop.md) ([**MCI \_ STOP**](mci-stop.md)), [**Anhalten**](pause.md) ([**MCI \_ PAUSE**](mci-pause.md)), [**Fortsetzen**](resume.md) ([**MCI \_ RESUME**](mci-resume.md)) und [**Seek**](seek.md) ([**MCI \_ SEEK**](mci-seek.md)), wirken sich auf die Wiedergabe oder Positionierung einer Multimediadatei aus. Wenn ein MCI-Gerät einen Wiedergabebefehl empfängt, während ein anderer Wiedergabebefehl ausgeführt wird, akzeptiert es den Befehl und beendet oder ersetzt den vorherigen Befehl.

Viele MCI-Befehle, z. B. [**set**](set.md) ([**MCI \_ SET**](mci-set.md)), wirken sich nicht auf die Wiedergabe aus. Eine Benachrichtigung von einem dieser Befehle beeinträchtigt keine ausstehenden Wiedergabe- oder Positionsbefehle, solange die Benachrichtigungen nicht von derselben Instanz des Treibers ausgeführt werden. Beispielsweise können Sie einen  Set- oder Status-Befehl [**(**](status.md) [**MCI \_ STATUS**](mci-status.md)) ausführen, während ein Gerät einen Suchbefehl ohne Beenden oder Absetzen des  **Seek-Befehls** ausführen muss.

Es kann jedoch nur eine ausstehende Benachrichtigung geben. Wenn eine Anwendung z. B.  eine Wiedergabebenachrichtigung anfing und dieser Anforderung  mit dem Status **"Startposition** benachrichtigen" folgt, gibt die Wiedergabebenachrichtigung "ersetzt" zurück, und die Benachrichtigung für den Statusbefehl wird nach Abschluss der Wiedergabe wieder angezeigt. In diesem Fall ist der **Befehl play** jedoch weiterhin erfolgreich, obwohl die Anwendung die Benachrichtigung nicht erhalten hat.

 

 




