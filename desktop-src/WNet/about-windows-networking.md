---
title: Informationen über Windows-Netzwerke
description: Anwendungen können die WNET-Funktionen zum Hinzufügen und Abbrechen von Netzwerkverbindungen und zum Abrufen von Informationen über die aktuelle Netzwerkkonfiguration verwenden.
ms.assetid: 37ce0762-b0b2-4d68-9942-b7034f1b76b7
keywords:
- WNET für Windows-Netzwerke, beschrieben
- WNET WNET, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91f7c8f58d4e44439bac18a2b7d7b850b21f955
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037568"
---
# <a name="about-windows-networking"></a>Informationen über Windows-Netzwerke

Anwendungen können die WNET-Funktionen zum Hinzufügen und Abbrechen von Netzwerkverbindungen und zum Abrufen von Informationen über die aktuelle Netzwerkkonfiguration verwenden.

Die folgende Abbildung zeigt die Struktur eines typischen Netzwerks.

![Typische Netzwerkstruktur](images/csnet-01.png)

In der obigen Abbildung wird die Hierarchie für Windows NT Server/Windows 2000-Server Ressourcen ausführlich als Netzwerkanbieter \# 1 angegeben. Netzwerkressourcen von anderen Anbietern verfügen über unterschiedliche hierarchische Systeme. Eine Anwendung benötigt keine Informationen über die Hierarchie, bevor Sie mit einem Netzwerk funktioniert. Der Vorgang kann vom Netzwerk Stamm (d. h. der obersten Container Ressource) fortgesetzt werden, und es werden Informationen zu den Ressourcen des Netzwerks abgerufen, wenn die Informationen benötigt werden.

Netzwerkressourcen, die andere Ressourcen enthalten, werden als *Container* bezeichnet. Container Ressourcen befinden sich in den Feldern in der obigen Abbildung.

Ressourcen, die keine anderen Ressourcen enthalten, werden als *Objekte* bezeichnet. In der obigen Abbildung sind SharePoint \# 1 und SharePoint \# 2 Objekte. Ein *SharePoint* ist ein Objekt, auf das über das Netzwerk zugegriffen werden kann. Beispiele für Share Points sind Drucker und freigegebene Verzeichnisse.

 

 




