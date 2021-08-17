---
title: Richtlinien für Peripheriehardware
description: Wenn ihr Hardwaregerät nicht für die Arbeit über eine Remotesitzung konzipiert ist, müssen Anbieter sicherstellen, dass die Gerätetreibersoftware die Deaktivierung der Umleitung des Geräts mithilfe einer Systemrichtlinie oder Gruppenrichtlinie erzwingt.
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0cbe39010eaa59d4207ad28722521793fe33a04f9d06591f21f8ac381940235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756269"
---
# <a name="peripheral-hardware-guidelines"></a>Richtlinien für Peripheriehardware

Für einen rdc-Client (Remotedesktopverbindung) ist der Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) der lokale Computer. Folglich werden Geräte wie Datenträgerlaufwerke und Drucker, die an den Server angefügt sind, als lokale Geräte für einen Client angezeigt. Im Gegensatz dazu können Laufwerke und Drucker, die an ein Clientterminal angefügt sind, je nach den für die Verbindung ausgewählten Optionen, dem verwendeten Server und der Version der verwendeten Clientsoftware als Remotegeräte erscheinen.

Während die erste Version von Remotedesktopdienste keine Anwendungen unterstützt hat, die ausgaben direkt an serielle, parallele und Soundports senden, die an das Clientterminal angefügt sind, ermöglichen die aktuellen Versionen, dass diese Geräte als lokale Geräte für Anwendungen angezeigt werden, die in der Remotedesktopdienste Sitzung ausgeführt werden.

Wenn ihr Hardwaregerät nicht für die Arbeit über eine Remotesitzung konzipiert ist, müssen Anbieter sicherstellen, dass die Gerätetreibersoftware die Deaktivierung der Umleitung des Geräts mithilfe einer Systemrichtlinie oder Gruppenrichtlinie erzwingt.

 

 




