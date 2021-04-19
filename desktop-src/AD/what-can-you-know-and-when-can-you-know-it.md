---
title: Was Sie wissen und wann Sie es wissen können
description: Anwendungen, die sich auf von der Latenz verursachende Zustände unterliegen, müssen Problem Zustände erkennen und entsprechende Maßnahmen ergreifen.
ms.assetid: d1d0135e-2d67-47dd-82ac-4869203ce85e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a8a6c6def8475946ad5faa63615d17742fbcb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342240"
---
# <a name="what-can-you-know-and-when-can-you-know-it"></a>Was ist Ihnen bekannt, und wann können Sie Sie wissen?

Anwendungen, die sich auf von der Latenz verursachende Zustände unterliegen, müssen Problem Zustände erkennen und entsprechende Maßnahmen ergreifen. Es gibt zwei Problem Zustände: Versions Schiefe und partielle Aktualisierung. Die Versions Neigung kann nicht erkannt werden, indem der Verzeichnisdienst untersucht wird (Beachten Sie, dass sich das Grundsatz verteilter Computing in der Ursache [Active Directory Domain Services dieses Replikations Modells](why-active-directory-domain-services-uses-this-replication-model.md)befindet). Teil Updates können durch Hinzufügen von Metadaten zu den Objekten erkannt werden, aus denen sich der verknüpfte Satz zusammensetzt. Vorschläge für solche Metadaten werden in den nachfolgenden Abschnitten dieses Dokuments angezeigt. Es gibt Strategien zur Vermeidung von Anwendungen, mit denen die Wahrscheinlichkeit von Versions Schiefe und partiellem Update reduziert werden kann. Diese Strategien werden auch in den nachfolgenden Abschnitten dieses Dokuments erläutert.

 

 




