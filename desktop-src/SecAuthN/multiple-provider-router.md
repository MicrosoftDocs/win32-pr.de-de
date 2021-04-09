---
description: Der multianbieterrouter (MPR) übernimmt die Kommunikation zwischen dem Windows-Betriebssystem und den installierten Netzwerkanbietern. Dadurch kann Windows dem Benutzer ein integriertes Netzwerk vorstellen.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Mehrere Anbieter Router
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa7c4e76901c31e3b5dc7f329a23838aba4f7be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867247"
---
# <a name="multiple-provider-router"></a>Mehrere Anbieter Router

Der [*multianbieterrouter*](../secgloss/m-gly.md) (MPR) übernimmt die Kommunikation zwischen dem Windows-Betriebssystem und den installierten Netzwerkanbietern. Dadurch kann Windows dem Benutzer ein integriertes Netzwerk vorstellen.

Beim Start der MPR wird die Registrierung überprüft, um zu bestimmen, welche Netzwerkanbieter auf dem System installiert sind und in welcher Reihenfolge Sie durchlaufen werden sollen. Alle registrierten Netzwerkanbieter-DLLs werden geladen und verwendet, um nachfolgende WNET-Aufrufe von der Benutzeroberfläche oder anderen Anwendungen zu verarbeiten.

Weitere Informationen zu WNET-Funktionen finden Sie unter [Windows-Netzwerke](../wnet/windows-networking-wnet-.md).

 

 
