---
description: Die Anwendung kann beim Öffnen eines Telefongeräts einen von zwei Betriebsmodi anfordern.
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: Betriebsmodi und Berechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f7d3c1f6b7049c3986b96734a537906dc62166c48d62e549684cdaa6d35ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012470"
---
# <a name="operating-modes-and-privileges"></a>Betriebsmodi und Berechtigungen

Die Anwendung kann beim Öffnen eines Telefongeräts einen von zwei Betriebsmodi anfordern. Diese Modi spiegeln die Berechtigungen wider, die die Anwendung für das Gerät anfordert:

-   Wenn Sie ein Telefon für Überwachungsberechtigungen öffnen, kann die Anwendung den Status des Telefongeräts bestimmen. Nachrichten werden an die Anwendung gesendet, wenn Statusänderungen auf dem Smartphone erkannt werden.
-   Eine Anwendung, die ein Telefongerät für Besitzerberechtigungen öffnet, kann Vorgänge verwenden, die den Zustand des Telefongeräts ändern. Die Berechtigung "Besitzer" umfasst automatisch auch vollständige Überwachungsberechtigungen. Ein bestimmtes Telefongerät kann jederzeit nur einmal für Besitzerberechtigungen geöffnet werden, aber mehrmals für Überwachungsberechtigungen. Alle **phoneSet-Vorgänge** erfordern Besitzerberechtigungen, während alle **phoneGet-Vorgänge** nur Überwachungsberechtigungen erfordern.

 

 



