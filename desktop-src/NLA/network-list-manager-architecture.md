---
title: Netzwerk Listen-Manager-Architektur
description: Netzwerk Listen-Manager-Architektur
ms.assetid: d3d03891-7c61-4f7e-a2e2-ef13353e8688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567b103cfd5d9944aa33a799c2cc1bc4b983759
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948073"
---
# <a name="network-list-manager-architecture"></a>Netzwerk Listen-Manager-Architektur

Der Netzwerk Listen-Manager wird im Zusammenhang mit Svchost.exe als Dienst ausgeführt und während der Computer Start Prozedur gestartet. Der Netzwerk Listen-Manager-Dienst verwaltet eine Tabelle mit verfügbaren Netzwerken und Netzwerk Attributen, die von Anwendungen über die Netzwerk Listen-Manager-API abgerufen werden. Der Netzwerk Listen-Manager stellt grundlegende Funktionen zum Filtern und Abfragen des Netzwerk Listen-Manager-Dienstanbieter für bestimmte Netzwerke und zum Abrufen der Attribute dieser Netzwerke bereit. Das folgende Diagramm zeigt die Architektur des Netzwerk Listen-Managers und die Interaktion zwischen dem Netzwerk Listen-Manager-Dienst und der Client Anwendung.

![Diagramm zur Netzwerk Bewusstsein-Architektur](images/architecture.png)

 

 




