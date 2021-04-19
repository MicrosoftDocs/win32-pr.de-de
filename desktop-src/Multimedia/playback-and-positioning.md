---
title: Wiedergabe und Positionierung
description: Wiedergabe und Positionierung
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efbd6256fbd0d258f5d5c9d3da9b01c72a203dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339410"
---
# <a name="playback-and-positioning"></a>Wiedergabe und Positionierung

Eine Reihe von MCI-Befehlen, wie z. b. [**Play**](play.md) ([**MCI \_ Play**](mci-play.md) [**),**](resume.md) Anhaltevorgang ([**MCI \_**](mci-stop.md)-Pause), [**Anhalten**](stop.md) ([**MCI- \_ Pause**](mci-pause.md)), fort [**setzen (**](pause.md) MCI-Fortsetzung) und [**Suchen**](seek.md) ([**MCI- \_ Suche**](mci-seek.md)), wirken sich auf die Wiedergabe oder Positionierung einer Multimedia-Datei aus [**\_**](mci-resume.md) Wenn ein MCI-Gerät einen Wiedergabe Befehl empfängt, während ein anderer Wiedergabe Befehl ausgeführt wird, akzeptiert er den Befehl und beendet oder ersetzt den vorherigen Befehl.

Viele MCI-Befehle, z. b. [**Set**](set.md) ([**MCI \_ set**](mci-set.md)), wirken sich nicht auf die Wiedergabe aus. Eine Benachrichtigung von einem dieser Befehle beeinträchtigt nicht den ausstehenden Wiedergabe-oder Positions Befehl, solange die Benachrichtigungen nicht von derselben Instanz des Treibers ausgeführt werden. Beispielsweise können Sie einen **Set** -oder [**Status**](status.md) -Befehl ([**MCI- \_ Status**](mci-status.md)) ausgeben, während ein Gerät einen **Seek** -Befehl ausführt, ohne den **Seek** -Befehl zu beenden oder zu ersetzen.

Es darf jedoch nur eine ausstehende Benachrichtigung vorhanden sein. Wenn eine Anwendung z. b. eine Benachrichtigung für die wieder **Gabe** anfordert und dieser Anforderung mit dem **Status** "Benachrichtigung starten" folgt, gibt die **Wiedergabe** Benachrichtigung "abgelöst" zurück, und die Benachrichtigung für den Status Befehl wird nach Abschluss des Vorgangs zurückgegeben. In diesem Fall ist der **Wiedergabe** Befehl jedoch weiterhin erfolgreich, obwohl die Anwendung die Benachrichtigung nicht erhalten hat.

 

 




