---
title: Kommunikation zwischen NAP-Client und Server seitiger Komponente
description: Kommunikation zwischen NAP-Client und Server seitiger Komponente
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07597ac80a1e02c4f8528b3c99050aefb5963988
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388657"
---
# <a name="nap-client-and-server-side-component-communication"></a>Kommunikation zwischen NAP-Client und Server seitiger Komponente

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die NAP-Agent-Komponente kann über den folgenden Prozess mit der NAP-Verwaltungs Server Komponente kommunizieren:

1.  Der NAP-Agent übergibt die SSOH an die NAP ec.
2.  Der NAP EC übergibt die SSOH an die NAP es.
3.  Der NAP es übergibt die SSOH an den Netzwerk Richtlinien Server (NPS)-Dienst.
4.  Der NPS-Dienst übergibt die SSOH an den NAP-Verwaltungs Server.

Ein SHA kann über den folgenden Prozess mit dem entsprechenden SHV kommunizieren:

1.  Der SHA übergibt seine SoH an den NAP-Agent.
2.  Der NAP-Agent übergibt das SoH, das in SSOH enthalten ist, an die NAP ec.
3.  Der NAP EC übergibt das SoH an die NAP es.
4.  Der NAP es übergibt das SoH an den NAP-Verwaltungs Server.
5.  Der NAP-Verwaltungs Server übergibt das SoH an den SHV.

Die folgende Abbildung zeigt den Kommunikationsprozess von NAP-Client Komponenten mit NAP-serverseitigen Komponenten.

![Architektur der Kommunikation zwischen Client und Server auf der NAP-Plattform](images/nap-client-to-server-comm.png)

Der NAP-Verwaltungs Server kann über den folgenden Prozess mit dem NAP-Agent kommunizieren:

1.  Der NAP-Verwaltungs Server übergibt die sostd an den NPS-Dienst.
2.  Der NPS-Dienst übergibt die SSoHR an den NAP es.
3.  Der NAP es übergibt die SSoHR an die NAP ec.
4.  Der NAP EC übergibt die SSoHR an den NAP-Agent.

Der SHV kann mit dem entsprechenden SHA über den folgenden Prozess kommunizieren:

1.  Der SHV übergibt seine Sohr an den NAP-Verwaltungs Server.
2.  Der NAP-Verwaltungs Server übergibt die Sohr an den NPS-Dienst.
3.  Der NPS-Dienst übergibt die im SSoHR enthaltene Sohr an die NAP es.
4.  Der NAP es übergibt die Sohr an die NAP ec.
5.  Der NAP EC übergibt die Sohr an den NAP-Agent.
6.  Der NAP-Agent übergibt die Sohr an den SHA.

Die folgende Abbildung zeigt den Kommunikationsprozess von NAP-serverseitigen Komponenten mit NAP-Client Komponenten.

![Architektur der Server-zu-Client-Kommunikation auf der NAP-Plattform](images/nap-server-to-client-comm.png)

 

 




