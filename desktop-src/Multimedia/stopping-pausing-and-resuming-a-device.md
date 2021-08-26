---
title: Beenden, Anhalten und Fortsetzen eines Geräts
description: Beenden, Anhalten und Fortsetzen eines Geräts
ms.assetid: df9ca4ab-4711-44dd-a058-909f291a1652
keywords:
- MCI_STOP Befehl
- MCI_PAUSE Befehl
- MCI_RESUME Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5485365a6c846556a1037f55a0b211755ce0f93162bc6720c7241353fc8625b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037100"
---
# <a name="stopping-pausing-and-resuming-a-device"></a>Beenden, Anhalten und Fortsetzen eines Geräts

Mit [**dem Befehl stop**](stop.md) ([**MCI \_ STOP**](mci-stop.md)) wird die Wiedergabe oder Aufzeichnung eines Geräts angehalten. Viele Geräte unterstützen auch den [**Befehl pause**](pause.md) ([**MCI \_ PAUSE**](mci-pause.md)). Der Unterschied zwischen **Anhalten und** **Anhalten hängt** vom Gerät ab. In **der Regel wird der** Betrieb angehalten, aber das Gerät ist bereit, die Wiedergabe oder Aufzeichnung sofort wieder aufzunehmen.

Mit dem Befehl [**play**](play.md) ([**MCI \_ PLAY**](mci-play.md)) oder [**record**](record.md) ([**MCI \_ RECORD**](mci-record.md)) zum Neustarten eines Geräts werden die speicherorte zurückgesetzt, die mit den Flags "to" (MCI TO) und \_ "from" (MCI FROM) angegeben wurden, bevor das Gerät angehalten oder beendet \_ wurde. Ohne das Flag "from" setzen diese Befehle die Startposition auf die aktuelle Position zurück. Ohne das Flag "to" setzen sie die Endposition auf das Ende des Mediums zurück. Um die Wiedergabe oder Aufzeichnung ohne Zurücksetzen einer  zuvor  angegebenen Stoppposition fortzufahren, verwenden Sie das To-Flag des Wiedergabe- oder Aufzeichnungsbefehls, um eine Endposition anzugeben.

Einige Geräte unterstützen den [**Befehl resume**](resume.md) ([**MCI \_ RESUME**](mci-resume.md)), um ein angehaltenes Gerät neu zu starten. Mit diesem Befehl werden die Speicherorte "in" und "von" nicht geändert, die mit dem Befehl **play** oder **record** vor dem Befehl zum Anhalten [**angegeben**](pause.md) wurden.

 

 




