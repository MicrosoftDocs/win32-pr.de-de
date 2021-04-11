---
description: Ein Netzwerkanbieter ist eine DLL, die ein bestimmtes Netzwerkprotokoll unterstützt.
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: Netzwerkanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e3cc231f461d48e7ce71d908cb92f6cd06eabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217318"
---
# <a name="network-providers"></a>Netzwerkanbieter

Ein Netzwerkanbieter ist eine DLL, die ein bestimmtes Netzwerkprotokoll unterstützt. Außerdem wird die [Netzwerkanbieter-API](network-provider-api.md)implementiert. Dies ermöglicht es, mit dem Windows-Betriebssystem zu interagieren, um Standard Netzwerk Anforderungen zu erhalten, z. b. Verbindungs-oder Verbindungsanforderungen. Um diese Anforderungen zu verarbeiten, ruft der Netzwerkanbieter die Netzwerk spezifische API auf, die für das Netzwerkprotokoll geeignet ist, das vom Netzwerkanbieter unterstützt wird. Anders ausgedrückt: der Netzwerkanbieter umschließt die Netzwerk spezifischen Funktionen in einer DLL, die eine Standardschnittstelle für Windows verfügbar macht.

Mithilfe von Netzwerkanbietern kann Windows viele verschiedene Arten von Netzwerkprotokollen unterstützen, ohne die Netzwerk spezifischen Details der einzelnen Netzwerke kennen zu müssen. Dies ist von entscheidender Bedeutung, da immer neue Netzwerkprotokolle entwickelt werden. Mit Netzwerkanbietern ist für die Unterstützung eines neuen Protokolls lediglich das Erstellen und Installieren eines neuen Netzwerk Anbieters erforderlich.

Informationen zu den Funktionen und Strukturen von Netzwerkanbietern finden Sie in den folgenden Themen:

-   [Netzwerkanbieter Funktionen](authentication-functions.md)
-   [Netzwerkanbieter Strukturen](authentication-structures.md)

 

 



