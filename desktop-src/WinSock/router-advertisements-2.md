---
description: Der Inhalt von IPv6-Routerankündigungen wird automatisch von den veröffentlichten Routen in der Routingtabelle abgeleitet. Nicht veröffentlichte Routen werden für das Routing verwendet, aber beim Erstellen von Routerankündigungen ignoriert.
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: IPv6-Routerankündigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef8a7be2139c03d94e8a84eae410e9f4f2e92da6059def1ef89997138009d351
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612940"
---
# <a name="ipv6-router-advertisements"></a>IPv6-Routerankündigungen

Der Inhalt von IPv6-Routerankündigungen wird automatisch von den veröffentlichten Routen in der Routingtabelle abgeleitet. Nicht veröffentlichte Routen werden für das Routing verwendet, aber beim Erstellen von Routerankündigungen ignoriert.

Routerankündigungen für IPv6 enthalten immer eine Quelllinkebenen-Adressoption und eine MTU-Option. Der Wert für die MTU-Option wird aus der aktuellen Link-MTU der sendenden Schnittstelle übernommen. Dieser Wert kann mit dem Befehl ipv6 ifc mtu geändert werden.

Die Routerankündigung hat nur dann eine Routerlebensdauer ungleich 0 (null), wenn eine veröffentlichte Standardroute vorhanden ist. Eine Standardroute ist eine Route für das Präfix der Länge 0 (null).

Veröffentlichte On-Link-Routen führen zu Präfixinformationsoptionen in Routerankündigungen. Wenn das On-Link-Präfix 64 Bits enthält, ist für die Option "Präfixinformationen" sowohl das L- als auch das A-Bit festgelegt, und hosts, die es empfangen, werden Adressen automatisch konfiguriert.

Eine Schnittstelle, die Routerankündigungen sendet, konfiguriert adressen auch automatisch für sich selbst basierend auf den von ihr gesendeten Präfixinformationsoptionen.

Eine begrenzte Lebensdauer ohne Mittelwerte für alle veröffentlichten Routen (z. B. 30 Minuten) wird empfohlen. Wenn Sie eine Route zurücknehmen möchten, können Sie die Route so ändern, dass sie eine veraltete Lebensdauer hat. Die Route altert im Laufe mehrerer Routerankündigungen und verschwindet dann sowohl vom Router als auch von allen Hosts, die die Routerankündigungen erhalten.

Routen, die Hosts über Routerankündigungen finden, altern und werden nicht veröffentlicht. Adressen, die aus dem Alter der Routerankündigungen automatisch konfiguriert werden.

 

 



