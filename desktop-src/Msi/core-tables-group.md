---
description: Weitere Informationen zum folgenden Diagramm finden Sie in der Legende des Entitätsbeziehungsdiagramms.
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: Kerntabellengruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a8704a13e71f019e3d0686384057d3f209de06530c97bda6f0a63ff352d4db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948539"
---
# <a name="core-tables-group"></a>Kerntabellengruppe

Weitere Informationen zum folgenden Diagramm finden Sie in der Legende [des Entitätsbeziehungsdiagramms.](entity-relationship-diagram-legend.md)

![Kerntabellengruppe](images/core.png)

Die Kerngruppe besteht aus Tabellen, die die grundlegenden Features und Komponenten der Anwendung und des Installationspakets beschreiben. Entwickler von Installationspaketen sollten daher überlegen, wie diese Tabellen zuerst aufgefüllt werden, da die Organisation eines großen Teil der Datenbank durch den Inhalt dieser Gruppe ersichtlich wird.

-   In [der Tabelle Feature](feature-table.md) werden alle Funktionen aufgeführt, die zur Anwendung gehören.
-   Die [Tabelle Bedingung enthält](condition-table.md) die bedingten Ausdrücke, die bestimmen, ob ein bestimmtes Feature installiert wird.
-   In [der Tabelle FeatureComponents wird](featurecomponents-table.md) beschrieben, welche Komponenten zu den einzelnen Features gehören.
-   In [der Tabelle Komponente](component-table.md) werden alle Komponenten aufgeführt, die zur Installation gehören.
-   In [der Tabelle Verzeichnis](directory-table.md) werden die Verzeichnisse aufgeführt, die während der Installation benötigt werden. Da jede Komponente nur einem Verzeichnis zugeordnet werden muss, ist die Component-Tabelle eng mit dieser Tabelle verknüpft und verfügt über einen externen Schlüssel für die Directory-Tabelle.
-   In [der Tabelle PublishComponent sind](publishcomponent-table.md) die Features und Komponenten aufgeführt, die für die Verwendung durch andere Anwendungen veröffentlicht werden. [Komponenten und Features](components-and-features.md) sind die beiden Arten von Featureanzeigen.
-   Die [Tabelle MsiAssembly gibt](msiassembly-table.md) Windows Installer-Einstellungen für .NET Framework Common Language Runtime-Assemblys und Win32-Assemblys an.
-   Die [Tabelle MsiAssemblyName](msiassemblyname-table.md) gibt das Schema für die Elemente eines starken Assemblycachenamens für eine Common Language Runtime- oder Win32-Assembly an.
-   Die [Tabelle Complus enthält](complus-table.md) Informationen, die zum Installieren von COM+-Anwendungen erforderlich sind.
-   Die [IsolatedComponent-Tabelle](isolatedcomponent-table.md) ordnet die in der Spalte Komponentenanwendung angegebene Komponente (im Allgemeinen eine .exe) der Komponente zu, die in der Spalte Freigegebene Komponenten (häufig eine freigegebene DLL) angegeben \_ \_ ist.
-   Die [Tabelle Upgrade enthält](upgrade-table.md) Informationen, die bei größeren Upgrades erforderlich [sind.](major-upgrades.md)

 

 



