---
title: Überlegungen zum Entwurf von Zustandsservern
description: Je nach Entwurf benötigen Sie möglicherweise einen Server, um die benutzer zu verfolgen, die derzeit im Netzwerk angemeldet sind.
ms.assetid: 2f8d268b-5518-4ad2-aed6-5971c913db6d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39fa2460fbad5ffedd4a517da588cc0c951f734926c1219d750e28f71734c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889480"
---
# <a name="state-server-design-considerations"></a>Überlegungen zum Entwurf von Zustandsservern

> [!Note]  
> Internet Authentication Service (IAS) wurde ab Windows Server 2008 in Network Policy Server (NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Diensts zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

Je nach Entwurf benötigen Sie möglicherweise einen Server, um die benutzer zu verfolgen, die derzeit im Netzwerk angemeldet sind. Die größte Herausforderung beim Zustandsserver besteht darin, die Informationen in der Zustandsserver-Datenbank mit dem tatsächlich angemeldeten Benutzer synchron zu halten. Wenn die Informationen auf dem Zustandsserver nicht synchron sind, können Benutzer mehrere Sitzungen verwenden, wenn sie nicht dazu autorisiert sind. Außerdem können Benutzer, die nicht über mehrere Sitzungen verfügen, versehentlich sanktioniert werden.

Folgendes sollte bei der Implementierung des Zustandsservers berücksichtigt werden:

-   Der Zustandsserver muss die Entscheidung in wenigen Sekunden online treffen. Aus diesem Grund benötigt der Zustandsserver eine skalierbare Infrastruktur, die viele Updates und Abfragen pro Sekunde unterstützen kann. Relationale Datenbanken sind für solche großen Abfragen mit gleichzeitigen Updates nicht geeignet. Relationale Datenbanken sind in erster Linie so aufgebaut, dass Daten konsistent bleiben und allen Kunden eine konsistente Ansicht der Daten zur Verfügung steht. Sie sind nicht für schnelle Updates erstellt.
-   Transaktionskonsistenz bei Updates zwischen mehreren Objekten ist nicht wichtig. Dies liegt daran, dass der Zustandsserver ein kleines Fenster der Verkaufschance tolerieren kann. Die Transaktionskonsistenz eines einzelnen Updates ist jedoch wichtig, um die Wahrscheinlichkeit zu verringern, dass der Zustandsserver in einem inkonsistenten Zustand belässt, wenn einer der RADIUS-Server in der Mitte des Updates heruntergefahren wird.
-   Persistenz (Speichern des Zustands des Netzwerks im permanenten Speicher) ist nicht wichtig, da die persistenten Informationen schnell nicht mehr mit dem tatsächlichen Zustand des Netzwerks synchron sind.
-   Wenn ISDN oder andere Formen von Multilinks im Netzwerk unterstützt werden, sollte der Zustandsserver in der Lage sein, Szenarien zu verarbeiten, in denen diese Features verwendet werden.

Ein möglicher Entwurf ist die Implementierung einer Authentifizierungserweiterungs-DLL und einer Autorisierungserweiterungs-DLL. Jede dieser DLLs kann über das Netzwerk mit einer Datenbank kommunizieren. Die Autorisierungserweiterungs-DLL kann die Datenbank mit Informationen darüber aktualisieren, wer derzeit im Netzwerk angemeldet ist. Die Authentifizierungserweiterungs-DLL kann die Datenbank nach diesen Informationen abfragen, um zu entscheiden, ob die Authentifizierungsanforderung eines bestimmten Benutzers akzeptiert oder abgelehnt werden soll. Wenn der Benutzer bereits angemeldet ist, wird die Anforderung abgelehnt.

Der Vorteil der Aktualisierung der Zustandsserver-Datenbank durch die Autorisierungserweiterungs-DLL ist, dass die Autorisierungserweiterungs-DLL Zugriff auf weitere Informationen über den authentifizierten Benutzer hat. Die Autorisierungserweiterungs-DLL hat Zugriff auf alle Autorisierungsattribute des NPS-Autorisierungsmechanismus. Einige Benutzer verfügen beispielsweise möglicherweise über Autorisierungen, die es ihnen ermöglichen, mehrere Sitzungen zu verwenden. Der Zustandsserver sollte solche Benutzer als Sonderfall behandeln.

 

 




