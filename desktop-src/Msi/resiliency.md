---
description: Resilienz ist die Fähigkeit einer Anwendung, sich ordnungsgemäß aus Situationen wiederherzustellen, in denen eine wichtige Komponente fehlt oder durch eine inkompatible Version ersetzt wurde.
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: Resilienz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73565a129c25b19e0fb362e5363626f1acfee0387b2d4e4826f79222e7425b96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810780"
---
# <a name="resiliency"></a>Resilienz

Resilienz ist die Fähigkeit einer Anwendung, sich ordnungsgemäß aus Situationen wiederherzustellen, in denen eine wichtige Komponente fehlt oder durch eine inkompatible Version ersetzt wurde. Durch das Erstellen eines Installationspakets und die Verwendung der [Installerfunktionen](installer-functions.md)können Entwickler den Windows Installer verwenden, um resiliente Anwendungen zu erstellen, die in solchen Situationen wiederhergestellt werden können.

-   Verwenden Sie die Quellliste des Installationsprogramms, um die Resilienz von Anwendungen zu erhöhen, die auf Netzwerkressourcen angewiesen sind. Weitere Informationen finden Sie unter [Quellresilienz.](source-resiliency.md)
-   Verwenden Sie die -API des Installationsprogramms, um zu überprüfen, ob eine wichtige Funktion, Komponente, Datei oder Dateiversion installiert ist.
-   Verwenden Sie die -API des Installationsprogramms, um den Pfad zu einer Komponente zur Laufzeit zu überprüfen. Dadurch wird die Abhängigkeit Ihrer Anwendung von statischen Dateipfaden reduziert, die sich häufig von Computer zu Computer unterscheiden.
-   Verwenden Sie das Installationsprogramm, um beschädigte Verknüpfungen, Registrierungseinträge und andere Komponenten neu zu installieren, ohne das Setup erneut ausführen zu müssen.
-   Erhöhen Sie die Resilienz der Installation Ihres Produkts, indem Sie die Rollbackfunktion des Installationsprogramms aktiviert lassen. Weitere Informationen finden Sie unter [Rollbackinstallation.](rollback-installation.md)

 

 



