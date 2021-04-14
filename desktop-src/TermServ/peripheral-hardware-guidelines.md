---
title: Richtlinien für Peripheriegeräte
description: Wenn Ihr Hardware Gerät nicht für eine Remote Sitzung konzipiert ist, müssen die Anbieter sicherstellen, dass die Gerätetreibersoftware die Deaktivierung der Umleitung des Geräts mithilfe einer System Richtlinie oder Gruppenrichtlinie erzwingt.
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8e8e6a81a75abdef76851fedcb979526e1653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388549"
---
# <a name="peripheral-hardware-guidelines"></a>Richtlinien für Peripheriegeräte

Bei einem Remotedesktopverbindung-Client (RDC) ist der Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server der lokale Computer. Folglich werden Geräte, z. b. Laufwerke und Drucker, die an den Server angefügt sind, als lokale Geräte für einen Client angezeigt. Im Gegensatz dazu können Laufwerke und Drucker, die an ein Client Terminal angeschlossen sind, als Remote Geräte angezeigt werden. Dies hängt von den Optionen ab, die für die Verbindung ausgewählt wurden, dem verwendeten Server und der Version der verwendeten Client Software.

In der ersten Version von Remotedesktopdienste wurden keine Anwendungen unterstützt, die die Ausgabe direkt an serielle, parallele und Audioports senden, die an das Client Terminal angeschlossen sind. in den aktuellen Versionen können diese Geräte beispielsweise als lokale Geräte für Anwendungen angezeigt werden, die in der Remotedesktopdienste Sitzung ausgeführt werden.

Wenn Ihr Hardware Gerät nicht für eine Remote Sitzung konzipiert ist, müssen die Anbieter sicherstellen, dass die Gerätetreibersoftware die Deaktivierung der Umleitung des Geräts mithilfe einer System Richtlinie oder Gruppenrichtlinie erzwingt.

 

 




