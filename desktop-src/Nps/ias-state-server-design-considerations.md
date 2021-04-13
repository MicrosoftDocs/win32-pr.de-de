---
title: Überlegungen zum Status Server Entwurf
description: Abhängig von Ihrem Entwurf benötigen Sie möglicherweise einen Server, um die Benutzer zu verfolgen, die zurzeit am Netzwerk angemeldet sind.
ms.assetid: 2f8d268b-5518-4ad2-aed6-5971c913db6d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0ef654f3641138075acc667d733b20c94c4840
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388547"
---
# <a name="state-server-design-considerations"></a>Überlegungen zum Status Server Entwurf

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

Abhängig von Ihrem Entwurf benötigen Sie möglicherweise einen Server, um die Benutzer zu verfolgen, die zurzeit am Netzwerk angemeldet sind. Die Hauptaufgabe beim Zustands Server besteht darin, die Informationen in der Zustands Server Datenbank synchron mit der Person zu halten, die gerade angemeldet ist. Wenn die Informationen auf dem Zustands Server nicht synchron sind, können Benutzer möglicherweise über mehrere Sitzungen verfügen, wenn Sie dazu nicht berechtigt sind. Benutzer, die nicht über mehrere Sitzungen verfügen, könnten auch versehentlich benachteiligt werden.

Beim Implementieren des Zustands Servers sollte Folgendes berücksichtigt werden:

-   Der Zustands Server muss die Entscheidung innerhalb weniger Sekunden online stellen. Aus diesem Grund benötigt der Zustands Server eine skalierbare Infrastruktur, die viele Updates und Abfragen pro Sekunde unterstützen kann. Relationale Datenbanken eignen sich nicht für solche großen Abfragen mit gleichzeitigen Updates. Relationale Datenbanken werden primär erstellt, um die Daten konsistent zu halten und eine konsistente Sicht der Daten für alle Consumer bereitzustellen. Sie sind nicht für schnelle Updates konzipiert.
-   Die Transaktions Konsistenz bei Updates zwischen mehreren Objekten ist nicht von Bedeutung. Dies liegt daran, dass der Zustands Server ein kleines Fenster der Gelegenheit tolerieren kann. Allerdings ist die Transaktions Konsistenz eines einzelnen Updates wichtig, um die Wahrscheinlichkeit zu verringern, dass der Zustands Server in einem inkonsistenten Zustand belassen wird, wenn einer der RADIUS-Server in der Mitte des Updates heruntergefahren wird.
-   Persistenz (das Speichern des Zustands des Netzwerks in einem persistenten Speicher) ist nicht wichtig, da die persistenten Informationen schnell mit dem tatsächlichen Status des Netzwerks synchronisiert werden.
-   Wenn ISDN oder andere Formen von mehrfach im Netzwerk unterstützt werden, sollte der Zustands Server Szenarios verarbeiten können, die diese Features verwenden.

Ein möglicher Entwurf besteht darin, sowohl eine Authentifizierungs Erweiterungs-DLL als auch eine Autorisierungs Erweiterungs-DLL zu implementieren. Jede dieser DLLs kann über das Netzwerk mit einer Datenbank kommunizieren. Die Autorisierungs Erweiterungs-DLL kann die Datenbank mit Informationen darüber aktualisieren, wer zurzeit im Netzwerk angemeldet ist. Die authentifizierungserweiterungs-dll kann die Datenbank nach diesen Informationen Abfragen, um zu entscheiden, ob die Authentifizierungsanforderung eines bestimmten Benutzers angenommen oder abgelehnt werden soll. Wenn der Benutzer bereits angemeldet ist, wird die Anforderung abgelehnt.

Der Vorteil, dass die Autorisierungs Erweiterungs-DLL die State-Server-Datenbank aktualisiert, besteht darin, dass die Autorisierungs Erweiterungs-DLL Zugriff auf Weitere Informationen über den authentifizierten Benutzer hat. Die dll der Autorisierungs Erweiterung hat Zugriff auf Alle Autorisierungs Attribute aus dem NPS-Autorisierungs Mechanismus. Beispielsweise können einige Benutzer über Autorisierungen verfügen, mit denen Sie mehrere Sitzungen haben können. Der Zustands Server sollte solche Benutzer als Sonderfall behandeln.

 

 




