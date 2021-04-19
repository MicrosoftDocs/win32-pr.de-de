---
description: Netzwerk Paketanbieter (NPPs) stellen COM-Schnittstellen bereit, die von NPP-Anwendungen aufgerufen werden, und Netzwerkmonitor.
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: NPP-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3146d34798c57aea0bbd0f4bfec0037ed2ac879c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355518"
---
# <a name="npp-interfaces"></a>NPP-Schnittstellen

Netzwerk Paketanbieter (NPPs) stellen COM-Schnittstellen bereit, die von NPP-Anwendungen aufgerufen werden, und Netzwerkmonitor. Beachten Sie beim Aufrufen von " [comatenppinterface](createnppinterface.md)", dass jede NPP als einzelnes in-Process-COM-Objekt dargestellt wird. Anwendungen können eine beliebige Anzahl von NPP-Objekten instanziieren. Allerdings muss jedes instanziierte Objekt nur eine – und nur eine – der fünf NPP-Schnittstellen verwenden.

Beachten Sie auch, dass unterschiedliche NPP-Schnittstellen Netzwerkdaten in verschiedenen Formularen bereitstellen. Netzwerkmonitor z. b. die **idelta-DC** -Schnittstelle verwendet, um Netzwerk Datenverkehr zu erfassen und in einer Erfassungs Datei zu speichern. während Monitore den Netzwerk Datenverkehr in Echtzeit mithilfe der " **untc** "-Schnittstelle erfassen. In der folgenden Tabelle werden Netzwerkmonitor NPP-Schnittstellen beschrieben.



| Schnittstelle                | BESCHREIBUNG                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Idelta-DC](idelaydc.md) | Erfasst Netzwerk Datenverkehr, der in einer Erfassungs Datei gespeichert ist. Diese Schnittstelle wird von Netzwerkmonitor-und NPP-Anwendungen verwendet.                                          |
| [IESP](iesp.md)         | Erfasst Netzwerk Datenverkehr, der in einer Erfassungs Datei gespeichert ist, und stellt erweiterte Statistiken in einem speziellen ESP-Dateiformat bereit. Diese Schnittstelle wird von NPP-Anwendungen verwendet. |
| ["Iran"](irtc.md)         | Erfasst Netzwerk Datenverkehr in Echtzeit und löst Ereignisse aus, wenn diese auftreten. Diese Schnittstelle wird von [*Monitoren*](m.md) und NPP-Anwendungen verwendet.     |
| [IStats](istats.md)     | Ruft Statistiken als Rohdaten und nicht als Frames ab. Diese Schnittstelle wird von NPP-Anwendungen wie [*Perfmon*](p.md)verwendet.                     |



 

 

 



