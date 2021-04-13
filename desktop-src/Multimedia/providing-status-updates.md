---
title: Bereitstellen von Status Aktualisierungen
description: Bereitstellen von Status Aktualisierungen
ms.assetid: 0f22c5d5-c85b-411e-a4dd-b7ad768be975
keywords:
- Mciwndabtactivetimer-Makro
- Mciwndabtinactivetimer-Makro
- Mciwndgetactivetimer-Makro
- Mciwndgetinactivetimer-Makro
- Mciwndsettimers-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd53c9580f3ae9be09817979178d10e60765ea3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388230"
---
# <a name="providing-status-updates"></a>Bereitstellen von Status Aktualisierungen

Mciwnd verwendet Timer, um in regelmäßigen Abständen Informationen in der Fenstertitelleiste und der Scrollleiste zu aktualisieren und Benachrichtigungs Meldungen an das übergeordnete Fenster zu senden. Ein Timer steuert den Aktualisierungs Zeitraum des aktiven mciwnd-Fensters, und ein zweiter Timer steuert den Update Zeitraum für inaktive mciwnd-Fenster. Die Anwendung kann die mciwnd-Timer-Makros verwenden, um die aktuellen Zeit Geber Einstellungen abzurufen und die Aktualisierungs Zeiträume anzupassen.

Sie können den Update Zeitraum festlegen, der vom aktiven Zeit Geber verwendet wird, indem Sie das Makro [**mciwndsetactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) verwenden. Dieses Makro legt den Zeitraum fest, der von mciwnd zum Aktualisieren der Trackleiste verwendet wird, um die in der Fenstertitelleiste gemeldete Wiedergabe Position zu aktualisieren und um das übergeordnete Fenster zu benachrichtigen, dass sich das Medium geändert hat. Sie können den aktuellen Aktualisierungs Zeitraum, der vom aktiven Fenster Timer verwendet wird, mit dem [**mciwndgetactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) -Makro abrufen. Der Standard Update Zeitraum für den aktiven Zeit Geber beträgt 500 Millisekunden.

Sie können den Update Zeitraum festlegen, der vom inaktiven Fenster Timer verwendet wird, indem Sie das [**mciwndsetinactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) -Makro verwenden. Dieses Makro legt den Zeitraum fest, der von mciwnd zum Aktualisieren der Trackleiste verwendet wird, um die in der Fenster Beschriftung gemeldete Wiedergabe Position zu aktualisieren, und um das übergeordnete Fenster darüber zu benachrichtigen, dass sich das Medium geändert hat. Sie können den aktuellen Aktualisierungs Zeitraum, der vom inaktiven Fenster Timer verwendet wird, mithilfe des [**mciwndgetinactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) -Makros abrufen. Der Standard Update Zeitraum für den Timer des inaktiven Fensters beträgt 2000 Millisekunden.

Die Anwendung kann den Update Zeitraum für beide Timer gleichzeitig mit dem [**mciwndsettimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) -Makro festlegen. Der Speicher für den Wert des Aktualisierungs Zeitraums ist auf 16 Bits beschränkt. Wenn eine größere Menge für einen der beiden Aktualisierungs Zeitraum erforderlich ist, legen Sie die Timer einzeln fest.

 

 




