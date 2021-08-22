---
title: Definieren der Schnittstelle
description: Eine Schnittstellendefinition ist eine formale Spezifikation dafür, wie eine Clientanwendung und eine Serveranwendung miteinander kommunizieren.
ms.assetid: 709ca498-4da3-4e6f-bb12-333a407b74c2
keywords:
- Remoteprozeduraufruf-RPC , Aufgaben, Definieren der Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654c6690e6980e659df8a68652aec59b296b7d88543eca02605f489a2c3a909c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930805"
---
# <a name="defining-the-interface"></a>Definieren der Schnittstelle

Eine Schnittstellendefinition ist eine formale Spezifikation dafür, wie eine Clientanwendung und eine Serveranwendung miteinander kommunizieren. Die -Schnittstelle definiert, wie sich Client und Server erkennen, welche Remoteverfahren die Clientanwendung aufrufen kann, und wie die Datentypen für die Parameter und Rückgabewerte dieser Prozeduren sind. Außerdem wird angegeben, wie die Daten zwischen Client und Server übertragen werden.

Sie definieren diese Schnittstelle in der Microsoft Interface Definition Language (MIDL), die aus C-Sprachdefinitionen besteht, die um Schlüsselwörter erweitert werden, die als Attribute bezeichnet werden und beschreiben, wie die Daten über das Netzwerk übertragen werden.

Die IDL-Datei (Interface Definition) enthält Typdefinitionen, Attribute und Funktionsprototypen, die beschreiben, wie Daten im Netzwerk übertragen werden. Die Anwendungskonfigurationsdatei (Application Configuration, ACF) enthält Attribute, die Ihre Anwendung für eine bestimmte Betriebsumgebung konfigurieren, ohne die Netzwerkmerkmale zu beeinträchtigen.

 

 




