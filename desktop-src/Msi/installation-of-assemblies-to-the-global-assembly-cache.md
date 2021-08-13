---
description: Der Windows Installer installiert Common Language Runtime-Assemblys mithilfe der Microsoft-.NET Framework im globalen Assemblycache.
ms.assetid: 21d535d5-f05b-411a-8719-2662e6046fbd
title: Installation von Assemblys im globalen Assemblycache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dec84b507491da5b3ec4b2352044dc899230b41f41d2c81a943fba83b3ba0b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634208"
---
# <a name="installation-of-assemblies-to-the-global-assembly-cache"></a>Installation von Assemblys im globalen Assemblycache

Der Windows Installer installiert Common Language Runtime-Assemblys mithilfe der Microsoft-.NET Framework im globalen Assemblycache. Beim Installieren von Assemblys im globalen Assemblycache kann das Installationsprogramm nicht die gleichen Verzeichnisstruktur- und Dateiversionsregeln verwenden, die beim Installieren regulärer Windows Installer-Komponenten verwendet werden. Reguläre Windows Installer-Komponenten können von verschiedenen Produkten an mehreren Verzeichnisspeicherorten installiert werden. Assemblys können nur einmal im Assemblycache vorhanden sein. Jede Assembly wird als unteilbares Ganzes hinzugefügt und aus dem Assemblycache entfernt. daher werden alle Dateien, aus denen eine Assembly besteht, immer zusammen installiert oder entfernt.

Die Datenträgerkosten für reguläre Windows Installer-Komponenten und Common Language Runtime-Assemblys werden unterschiedlich berechnet. Die Gesamtdatenträgerkosten einer regulären Windows Installer-Komponente umfassen lokale Kosten, Quellkosten und Entfernungskosten. Weitere Informationen finden Sie unter [Dateikosten.](file-costing.md) Diese Methode kann nicht verwendet werden, um Common Language Runtime-Assemblys zu kosten, da diese möglicherweise andere Clients als den Windows Installer haben. Die Kosten für Common Language Runtime-Assemblys müssen durch Abfragen der Microsoft .NET Framework Common Language Runtime bestimmt werden.

Der Windows Installer verwendet einen zweistufigen Transaktionsprozess, um Produkte zu installieren, die Common Language Runtime-Assemblys enthalten. Dies ermöglicht das Rollback der Assemblyinstallation und -entfernung. Weitere Informationen finden Sie unter [Rollback von Assemblys im globalen Assemblycache.](rollback-of-assemblies-in-the-global-assembly-cache.md)

Beachten Sie, dass Assemblys, die von einer Installation im [Benutzerinstallationskontext](installation-context.md) im globalen Assemblycache installiert wurden, nicht durch Windows Dateischutz geschützt werden. Assemblys, die durch eine Installation im Installationskontext pro Computer im globalen Assemblycache installiert werden, werden durch [Windows Resource Protection](../wfp/windows-resource-protection-portal.md)geschützt.

 

 
