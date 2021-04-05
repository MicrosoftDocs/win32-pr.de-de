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
# <a name="stopping-pausing-and-resuming-a-device"></a>Beenden, anhalten und Fortsetzen eines Geräts

Der Befehl zum Anhalten ([**MCI \_**](mci-stop.md)-Befehl) [**hält**](stop.md) die Wiedergabe oder Aufzeichnung eines Geräts an. Viele Geräte unterstützen auch den [**Pause**](pause.md) -Befehl ([**MCI- \_ Pause**](mci-pause.md)). Der Unterschied zwischen **Anhalten und anhalten** **hängt vom Gerät** ab. In **der** Regel hält den Vorgang an, während das Gerät sofort wieder aufgenommen oder aufgezeichnet werden kann.

Mithilfe des Befehls [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)) oder [**Datensatz**](record.md) ([**MCI- \_ Datensatz**](mci-record.md)) zum Neustarten eines Geräts werden die mit den Flags "to" (MCI \_ to) und "from" (MCI from) angegebenen Orte zurückgesetzt, \_ bevor das Gerät angehalten oder beendet wurde. Ohne das Flag "from" setzen diese Befehle den Start Speicherort auf die aktuelle Position zurück. Ohne das Flag "to" setzen Sie die Endposition auf das Ende der Medien zurück. Um die Wiedergabe oder Aufzeichnung fortzusetzen, ohne eine zuvor angegebene Halteposition zurückzusetzen, verwenden Sie das Flag "to" des **Play** -oder **Record** -Befehls, um eine Endposition anzugeben.

Einige Geräte unterstützen den Befehl [**Resume**](resume.md) ([**MCI \_ Resume**](mci-resume.md)), um ein angehaltene Gerät neu zu starten. Mit diesem Befehl werden die "to"-und "from"-Speicherorte nicht geändert, die mit dem Befehl " **Play** " oder " **Record** " angegeben wurden, [**der dem Befehl**](pause.md)

 

 




