---
description: Der Windows Installer installiert Common Language Runtime Assemblys im globalen Assemblycache mithilfe des Microsoft .NET-Frameworks.
ms.assetid: 21d535d5-f05b-411a-8719-2662e6046fbd
title: Installation von Assemblys im globalen Assemblycache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719be313ad74374950092936bbd6124da779a0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214997"
---
# <a name="installation-of-assemblies-to-the-global-assembly-cache"></a>Installation von Assemblys im globalen Assemblycache

Der Windows Installer installiert Common Language Runtime Assemblys im globalen Assemblycache mithilfe des Microsoft .NET-Frameworks. Beim Installieren von Assemblys im globalen Assemblycache kann das Installationsprogramm nicht dieselbe Verzeichnisstruktur und dieselben Datei Versions Regeln verwenden, die bei der Installation regulärer Windows Installer Komponenten verwendet werden. Reguläre Windows Installer Komponenten können von unterschiedlichen Produkten in mehreren Verzeichnis Standorten installiert werden. Assemblys können nur einmal im Assemblycache vorhanden sein. Jede Assembly wird dem Assemblycache als unteilbares Ganzes hinzugefügt und daraus entfernt. aus diesem Grund werden alle Dateien, die eine Assembly enthalten, immer gleich installiert oder entfernt.

Die Datenträger Kosten regulärer Windows Installer Komponenten und Common Language Runtime Assemblys werden unterschiedlich berechnet. Die Gesamtkosten für die Datenträger einer regulären Windows Installer Komponente umfassen lokale Kosten, Quell Kosten und Entfernungs Kosten. Weitere Informationen finden Sie unter [Datei Kosten](file-costing.md). Diese Methode kann nicht verwendet werden, um Common Language Runtime Assemblys zu Kosten, da diese möglicherweise andere Clients als die Windows Installer haben. Die Kosten für Common Language Runtime Assemblys müssen durch Abfragen des Microsoft .NET Framework-Common Language Runtime ermittelt werden.

Der Windows Installer verwendet einen transaktionalen Zweiphasenprozess, um Produkte zu installieren, die Common Language Runtime Assemblys enthalten. Dadurch wird das Rollback der Assemblyinstallation und-Entfernung ermöglicht. Weitere Informationen finden Sie unter [Rollback von](rollback-of-assemblies-in-the-global-assembly-cache.md)Assemblys im globalen Assemblycache.

Beachten Sie, dass Assemblys, die im globalen Assemblycache durch eine Installation im [Installations Kontext](installation-context.md) pro Benutzer installiert werden, nicht durch den Windows-Datei Schutz geschützt werden. Assemblys, die im globalen Assemblycache durch eine Installation im computerspezifischen Installations Kontext installiert werden, werden durch [Windows-Ressourcenschutz](../wfp/windows-resource-protection-portal.md)geschützt.

 

 
