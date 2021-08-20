---
title: Client- und serverseitige Kommunikation zwischen NAP-Komponenten
description: Client- und serverseitige Kommunikation zwischen NAP-Komponenten
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d3c390aa8bdc8cc80eec8834dd1c250d523737d63963b4b9370877ffa46329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799075"
---
# <a name="nap-client-and-server-side-component-communication"></a>Client- und serverseitige Kommunikation zwischen NAP-Komponenten

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die NAP-Agent-Komponente kann mit der NAP-Verwaltungsserverkomponente über den folgenden Prozess kommunizieren:

1.  Der NAP-Agent übergibt SSoH an den NAP EC.
2.  Der NAP EC übergibt SSoH an den NAP ES.
3.  Der NAP ES übergibt SSoH an den Netzwerkrichtlinienserver-Dienst (NPS).
4.  Der NPS-Dienst übergibt SSoH an den NAP-Verwaltungsserver.

Ein SHA kann mit dem entsprechenden SHV über den folgenden Prozess kommunizieren:

1.  Der SHA übergibt seine SoH-Datei an den NAP-Agent.
2.  Der NAP-Agent übergibt den in SSoH enthaltenen SoH an den NAP EC.
3.  Der NAP EC übergibt den SoH an den NAP ES.
4.  Der NAP ES übergibt die SoH an den NAP-Verwaltungsserver.
5.  Der NAP-Verwaltungsserver übergibt die SoH an die SHV.

Die folgende Abbildung zeigt den Kommunikationsprozess von NAP-Clientkomponenten zu serverseitigen NAP-Komponenten.

![Architektur der Kommunikation zwischen Client und Server auf der Nap-Plattform](images/nap-client-to-server-comm.png)

Der NAP-Verwaltungsserver kann mit dem NAP-Agent über den folgenden Prozess kommunizieren:

1.  Der NAP-Verwaltungsserver übergibt die SoHRs an den NPS-Dienst.
2.  Der NPS-Dienst übergibt SSoHR an den NAP ES.
3.  Der NAP ES übergibt SSoHR an den NAP EC.
4.  Der NAP EC übergibt SSoHR an den NAP-Agent.

Der SHV kann mit dem entsprechenden SHA über den folgenden Prozess kommunizieren:

1.  Der SHV übergibt seine SoHR an den NAP-Verwaltungsserver.
2.  Der NAP-Verwaltungsserver übergibt das SoHR an den NPS-Dienst.
3.  Der NPS-Dienst übergibt den in SSoHR enthaltenen SoHR an den NAP ES.
4.  Der NAP ES übergibt den SoHR an den NAP EC.
5.  Der NAP EC übergibt das SoHR an den NAP-Agent.
6.  Der NAP-Agent übergibt das SoHR an den SHA.

Die folgende Abbildung zeigt den Kommunikationsprozess zwischen serverseitigen NAP-Komponenten und NAP-Clientkomponenten.

![Architektur der Kommunikation zwischen Server und Client auf der Nap-Plattform](images/nap-server-to-client-comm.png)

 

 




