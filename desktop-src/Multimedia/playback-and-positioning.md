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
# <a name="playback-and-positioning"></a><span data-ttu-id="eff8b-103">Wiedergabe und Positionierung</span><span class="sxs-lookup"><span data-stu-id="eff8b-103">Playback and Positioning</span></span>

<span data-ttu-id="eff8b-104">Eine Reihe von MCI-Befehlen, wie z. b. [**Play**](play.md) ([**MCI \_ Play**](mci-play.md) [**),**](resume.md) Anhaltevorgang ([**MCI \_**](mci-stop.md)-Pause), [**Anhalten**](stop.md) ([**MCI- \_ Pause**](mci-pause.md)), fort [**setzen (**](pause.md) MCI-Fortsetzung) und [**Suchen**](seek.md) ([**MCI- \_ Suche**](mci-seek.md)), wirken sich auf die Wiedergabe oder Positionierung einer Multimedia-Datei aus [**\_**](mci-resume.md)</span><span class="sxs-lookup"><span data-stu-id="eff8b-104">A number of MCI commands, such as [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)), [**stop**](stop.md) ([**MCI\_STOP**](mci-stop.md)), [**pause**](pause.md) ([**MCI\_PAUSE**](mci-pause.md)), [**resume**](resume.md) ([**MCI\_RESUME**](mci-resume.md)), and [**seek**](seek.md) ([**MCI\_SEEK**](mci-seek.md)), affect the playback or positioning of a multimedia file.</span></span> <span data-ttu-id="eff8b-105">Wenn ein MCI-Gerät einen Wiedergabe Befehl empfängt, während ein anderer Wiedergabe Befehl ausgeführt wird, akzeptiert er den Befehl und beendet oder ersetzt den vorherigen Befehl.</span><span class="sxs-lookup"><span data-stu-id="eff8b-105">If an MCI device receives a playback command while another playback command is in progress, it accepts the command and either stops or supersedes the previous command.</span></span>

<span data-ttu-id="eff8b-106">Viele MCI-Befehle, z. b. [**Set**](set.md) ([**MCI \_ set**](mci-set.md)), wirken sich nicht auf die Wiedergabe aus.</span><span class="sxs-lookup"><span data-stu-id="eff8b-106">Many MCI commands, such as [**set**](set.md) ([**MCI\_SET**](mci-set.md)), do not affect playback.</span></span> <span data-ttu-id="eff8b-107">Eine Benachrichtigung von einem dieser Befehle beeinträchtigt nicht den ausstehenden Wiedergabe-oder Positions Befehl, solange die Benachrichtigungen nicht von derselben Instanz des Treibers ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="eff8b-107">A notification from one of these commands does not interfere with pending playback or position commands as long as the notifications are not performed from the same instance of the driver.</span></span> <span data-ttu-id="eff8b-108">Beispielsweise können Sie einen **Set** -oder [**Status**](status.md) -Befehl ([**MCI- \_ Status**](mci-status.md)) ausgeben, während ein Gerät einen **Seek** -Befehl ausführt, ohne den **Seek** -Befehl zu beenden oder zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="eff8b-108">For example, you can issue a **set** or [**status**](status.md) ([**MCI\_STATUS**](mci-status.md)) command while a device is performing a **seek** command without stopping or superseding the **seek** command.</span></span>

<span data-ttu-id="eff8b-109">Es darf jedoch nur eine ausstehende Benachrichtigung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="eff8b-109">However, there can be only one pending notification.</span></span> <span data-ttu-id="eff8b-110">Wenn eine Anwendung z. b. eine Benachrichtigung für die wieder **Gabe** anfordert und dieser Anforderung mit dem **Status** "Benachrichtigung starten" folgt, gibt die **Wiedergabe** Benachrichtigung "abgelöst" zurück, und die Benachrichtigung für den Status Befehl wird nach Abschluss des Vorgangs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eff8b-110">For example, if an application requests a notification for **play** and follows that request with **status** "start position notify," the **play** notification will return "superseded" and the notification for the status command will return when it is finished.</span></span> <span data-ttu-id="eff8b-111">In diesem Fall ist der **Wiedergabe** Befehl jedoch weiterhin erfolgreich, obwohl die Anwendung die Benachrichtigung nicht erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="eff8b-111">In this case, however, the **play** command will still succeed, even though the application did not receive the notification.</span></span>

 

 




