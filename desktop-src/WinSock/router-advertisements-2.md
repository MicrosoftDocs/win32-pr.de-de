---
description: Der Inhalt von IPv6-Routerankündigungen wird automatisch von den veröffentlichten Routen in der Routing Tabelle abgeleitet. Nicht veröffentlichte Routen werden für das Routing verwendet, werden jedoch beim Erstellen von Routerankündigungen ignoriert.
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: IPv6-Routerankündigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a75b31a988595cba85d23dbafc1bd93ffff4ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349143"
---
# <a name="ipv6-router-advertisements"></a>IPv6-Routerankündigungen

Der Inhalt von IPv6-Routerankündigungen wird automatisch von den veröffentlichten Routen in der Routing Tabelle abgeleitet. Nicht veröffentlichte Routen werden für das Routing verwendet, werden jedoch beim Erstellen von Routerankündigungen ignoriert.

Routerankündigungen für IPv6 enthalten immer eine Quell Verbindungsschicht-Adress Option und eine MTU-Option. Der Wert für die MTU-Option wird von der aktuellen Link-MTU der Sende Schnittstelle entnommen. Dieser Wert kann mit dem IPv6-Befehl "IPMTU" geändert werden.

Die Routerankündigung hat nur eine routerlebensdauer, wenn eine veröffentlichte Standardroute vorhanden ist. Eine Standardroute ist eine Route für das Präfix mit der Länge 0 (null).

Veröffentlichte on-Link-Routen führen zu Präfix Informations Optionen in Routerankündigungen. Wenn das on-Link-Präfix 64 Bits hat, wird für die Option für die Präfix Informationen sowohl L als auch Bits festgelegt, und Hosts, die Sie empfangen, werden Adressen automatisch konfigurieren.

Eine Schnittstelle, die Routerankündigungen sendet, konfiguriert auch Adressen für sich selbst auf der Grundlage der von ihr gesendeten Optionen für Präfix Informationen automatisch.

Es wird empfohlen, eine begrenzte Dauer Lebensdauer für alle veröffentlichten Routen (z. b. 30 Minuten) zu erhalten. Wenn Sie eine Route zurückziehen möchten, können Sie die Route so ändern, dass Sie eine Alterungs Lebensdauer hat. Die Route wird im Verlauf mehrerer Routerankündigungen verwendet und verschwindet dann vom Router und allen Hosts, die die Routerankündigungen empfangen.

Routen, die Hosts über das Alter von Routerankündigungen suchen und nicht veröffentlicht werden. Adressen, die von Routerankündigungen ebenfalls automatisch konfiguriert werden.

 

 



