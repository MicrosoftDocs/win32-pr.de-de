---
description: Die Anwendung kann einen von zwei Betriebsmodi anfordern, wenn ein Telefongerät geöffnet wird.
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: Betriebsmodi und Berechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba1cc01ed0552762ac3bc97449b1ae5a923cb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755120"
---
# <a name="operating-modes-and-privileges"></a>Betriebsmodi und Berechtigungen

Die Anwendung kann einen von zwei Betriebsmodi anfordern, wenn ein Telefongerät geöffnet wird. Diese Modi entsprechen den Berechtigungen, die die Anwendung für das Gerät anfordert:

-   Durch das Öffnen eines Telefons für Monitor Berechtigungen kann die Anwendung den Status des Telefon Geräts ermitteln. Nachrichten werden an die Anwendung gesendet, wenn Statusänderungen auf dem Telefongerät erkannt werden.
-   Eine Anwendung, die ein Telefongerät für Besitzer Berechtigungen öffnet, kann Vorgänge verwenden, die den Zustand des Telefon Geräts ändern. Die Berechtigung "Besitzer" enthält automatisch auch vollständige Monitor Berechtigungen. Ein bestimmtes Telefongerät kann jederzeit nur einmal für Besitzer Rechte geöffnet werden, jedoch mehrmals für Überwachungs Berechtigungen. Alle **phonesetvorgänge** erfordern Besitzer Berechtigungen, während für alle **phoneget** -Vorgänge nur Monitor Berechtigungen erforderlich sind.

 

 



