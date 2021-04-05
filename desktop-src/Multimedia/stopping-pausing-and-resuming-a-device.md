---
title: Beenden, anhalten und Fortsetzen eines Geräts
description: Beenden, anhalten und Fortsetzen eines Geräts
ms.assetid: df9ca4ab-4711-44dd-a058-909f291a1652
keywords:
- MCI_STOP-Befehl
- MCI_PAUSE-Befehl
- MCI_RESUME-Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddcd9618608226dec108d62754964fe6401d429
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710703"
---
# <a name="stopping-pausing-and-resuming-a-device"></a><span data-ttu-id="bed64-106">Beenden, anhalten und Fortsetzen eines Geräts</span><span class="sxs-lookup"><span data-stu-id="bed64-106">Stopping, Pausing, and Resuming a Device</span></span>

<span data-ttu-id="bed64-107">Der Befehl zum Anhalten ([**MCI \_**](mci-stop.md)-Befehl) [**hält**](stop.md) die Wiedergabe oder Aufzeichnung eines Geräts an.</span><span class="sxs-lookup"><span data-stu-id="bed64-107">The [**stop**](stop.md) ([**MCI\_STOP**](mci-stop.md)) command suspends the playing or recording of a device.</span></span> <span data-ttu-id="bed64-108">Viele Geräte unterstützen auch den [**Pause**](pause.md) -Befehl ([**MCI- \_ Pause**](mci-pause.md)).</span><span class="sxs-lookup"><span data-stu-id="bed64-108">Many devices also support the [**pause**](pause.md) ([**MCI\_PAUSE**](mci-pause.md)) command.</span></span> <span data-ttu-id="bed64-109">Der Unterschied zwischen **Anhalten und anhalten** **hängt vom Gerät** ab.</span><span class="sxs-lookup"><span data-stu-id="bed64-109">The difference between **stop** and **pause** depends on the device.</span></span> <span data-ttu-id="bed64-110">In **der** Regel hält den Vorgang an, während das Gerät sofort wieder aufgenommen oder aufgezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bed64-110">Usually **pause** suspends operation but leaves the device ready to resume playing or recording immediately.</span></span>

<span data-ttu-id="bed64-111">Mithilfe des Befehls [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)) oder [**Datensatz**](record.md) ([**MCI- \_ Datensatz**](mci-record.md)) zum Neustarten eines Geräts werden die mit den Flags "to" (MCI \_ to) und "from" (MCI from) angegebenen Orte zurückgesetzt, \_ bevor das Gerät angehalten oder beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="bed64-111">Using the [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)) or [**record**](record.md) ([**MCI\_RECORD**](mci-record.md)) command to restart a device resets the locations specified with the "to" (MCI\_TO) and "from" (MCI\_FROM) flags before the device was paused or stopped.</span></span> <span data-ttu-id="bed64-112">Ohne das Flag "from" setzen diese Befehle den Start Speicherort auf die aktuelle Position zurück.</span><span class="sxs-lookup"><span data-stu-id="bed64-112">Without the "from" flag, these commands reset the starting location to the current position.</span></span> <span data-ttu-id="bed64-113">Ohne das Flag "to" setzen Sie die Endposition auf das Ende der Medien zurück.</span><span class="sxs-lookup"><span data-stu-id="bed64-113">Without the "to" flag, they reset the ending location to the end of the media.</span></span> <span data-ttu-id="bed64-114">Um die Wiedergabe oder Aufzeichnung fortzusetzen, ohne eine zuvor angegebene Halteposition zurückzusetzen, verwenden Sie das Flag "to" des **Play** -oder **Record** -Befehls, um eine Endposition anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bed64-114">To continue playing or recording without resetting a previously specified stop position, use the **play** or **record** command's "to" flag to specify an ending position.</span></span>

<span data-ttu-id="bed64-115">Einige Geräte unterstützen den Befehl [**Resume**](resume.md) ([**MCI \_ Resume**](mci-resume.md)), um ein angehaltene Gerät neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="bed64-115">Some devices support the [**resume**](resume.md) ([**MCI\_RESUME**](mci-resume.md)) command to restart a paused device.</span></span> <span data-ttu-id="bed64-116">Mit diesem Befehl werden die "to"-und "from"-Speicherorte nicht geändert, die mit dem Befehl " **Play** " oder " **Record** " angegeben wurden, [**der dem Befehl**](pause.md)</span><span class="sxs-lookup"><span data-stu-id="bed64-116">This command does not change the "to" and "from" locations specified with the **play** or **record** command that preceded the [**pause**](pause.md) command.</span></span>

 

 




