---
title: Definieren der Schnittstelle
description: Eine Schnittstellen Definition ist eine formale Angabe, wie eine Client Anwendung und eine Serveranwendung miteinander kommunizieren.
ms.assetid: 709ca498-4da3-4e6f-bb12-333a407b74c2
keywords:
- Remote Prozedur Aufruf RPC, Tasks, definieren der Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f447847eeca39258b96ba129c46b3f7bcf054
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036645"
---
# <a name="defining-the-interface"></a>Definieren der Schnittstelle

Eine Schnittstellen Definition ist eine formale Angabe, wie eine Client Anwendung und eine Serveranwendung miteinander kommunizieren. Die-Schnittstelle definiert, wie der Client und der Server einander erkennen, die Remote Prozeduren, die von der Client Anwendung aufgerufen werden können, und die Datentypen für die Parameter und Rückgabewerte dieser Prozeduren. Außerdem wird angegeben, wie die Daten zwischen Client und Server übertragen werden.

Diese Schnittstelle wird in der Microsoft Interface Definition Language (mittlerer l) definiert, die aus C-sprach Definitionen besteht, die mit Schlüsselwörtern (Attribute genannt) erweitert werden, die beschreiben, wie die Daten über das Netzwerk übertragen werden.

Die Schnittstellen Definitionsdatei (IDL) enthält Typdefinitionen, Attribute und Funktionsprototypen, die beschreiben, wie Daten im Netzwerk übertragen werden. Die Anwendungs Konfigurationsdatei (ACF) enthält Attribute, mit denen die Anwendung für eine bestimmte Betriebsumgebung konfiguriert wird, ohne dass sich dies auf die Netzwerk Merkmale auswirkt.

 

 




