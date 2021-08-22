---
description: Netzwerkpaketanbieter (Network Packet Providers, NPPs) stellen COM-Schnittstellen bereit, die von NPP-Anwendungen aufgerufen werden, und Netzwerkmonitor.
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: NPP-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fc38bd5db91354c81f88d9f0fe0a6ad23ce3ccb3ecd4a08c4b6335e25ddd33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676980"
---
# <a name="npp-interfaces"></a>NPP-Schnittstellen

Netzwerkpaketanbieter (Network Packet Providers, NPPs) stellen COM-Schnittstellen bereit, die von NPP-Anwendungen aufgerufen werden, und Netzwerkmonitor. Wenn Sie [CreateNPPInterface aufrufen,](createnppinterface.md)denken Sie daran, dass jedes NPP als einzelnes prozessinternes COM-Objekt dargestellt wird. Anwendungen können eine beliebige Anzahl von NPP-Objekten instanziieren. Jedes instanziierte Objekt muss jedoch nur eine der fünf NPP-Schnittstellen verwenden.

Beachten Sie auch, dass verschiedene NPP-Schnittstellen Netzwerkdaten in verschiedenen Formen bereitstellen. Beispielsweise verwendet Netzwerkmonitor die **IDelaydC-Schnittstelle,** um Netzwerkdatenverkehr zu erfassen und in einer Erfassungsdatei zu speichern. Während Monitore die **IRTC-Schnittstelle** verwenden, um Netzwerkdatenverkehr in Echtzeit zu erfassen. In der folgenden Tabelle werden die Netzwerkmonitor NPP-Schnittstellen beschrieben.



| Schnittstelle                | BESCHREIBUNG                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IDelaydC](idelaydc.md) | Erfasst Netzwerkdatenverkehr, der in einer Erfassungsdatei gespeichert ist. Diese Schnittstelle wird von Netzwerkmonitor und NPP-Anwendungen verwendet.                                          |
| [IESP](iesp.md)         | Erfasst Netzwerkdatenverkehr, der in einer Erfassungsdatei gespeichert ist, und stellt erweiterte Statistiken in einem speziellen ESP-Dateiformat zur Verfügung. Diese Schnittstelle wird von NPP-Anwendungen verwendet. |
| [IRTC](irtc.md)         | Erfasst Netzwerkdatenverkehr in Echtzeit und löst Ereignisse aus, wenn sie auftreten. Diese Schnittstelle wird von [*Monitoren und*](m.md) NPP-Anwendungen verwendet.     |
| [IStats](istats.md)     | Ruft Statistiken als Rohdaten anstelle von Frames ab. Diese Schnittstelle wird von NPP-Anwendungen wie [*Perfmon verwendet.*](p.md)                     |



 

 

 



