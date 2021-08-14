---
description: Ein Netzwerkanbieter ist eine DLL, die ein bestimmtes Netzwerkprotokoll unterstützt.
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: Netzwerkanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5443ec7366b0f7ad74037f868e1ca4a93dbd913d0c13fda46c7b9fdabd0e0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786598"
---
# <a name="network-providers"></a>Netzwerkanbieter

Ein Netzwerkanbieter ist eine DLL, die ein bestimmtes Netzwerkprotokoll unterstützt. Außerdem wird die [Netzwerkanbieter-API implementiert.](network-provider-api.md) Dies ermöglicht es, mit dem Windows zu interagieren, um Standardnetzwerkanforderungen wie Verbindungs- oder Trennungsanforderungen zu empfangen. Um diese Anforderungen zu verarbeiten, ruft der Netzwerkanbieter dann die netzwerkspezifische API auf, die für das netzwerkspezifische Protokoll geeignet ist, das der Netzwerkanbieter unterstützt. Anders ausgedrückt: Der Netzwerkanbieter umschließt die netzwerkspezifische Funktionalität in einer DLL, die eine Standardschnittstelle für die Windows.

Mithilfe von Netzwerkanbietern Windows Netzwerkprotokolle viele verschiedene Arten von Netzwerkprotokollen unterstützen, ohne die netzwerkspezifischen Details der einzelnen Netzwerke kennen zu müssen. Dies ist wichtig, da immer neue Netzwerkprotokolle entwickelt werden. Bei Netzwerkanbietern erfordert die Unterstützung eines neuen Protokolls lediglich das Erstellen und Installieren eines neuen Netzwerkanbieters.

Informationen zu Netzwerkanbieterfunktionen und -strukturen finden Sie in den folgenden Themen:

-   [Netzwerkanbieterfunktionen](authentication-functions.md)
-   [Netzwerkanbieterstrukturen](authentication-structures.md)

 

 



