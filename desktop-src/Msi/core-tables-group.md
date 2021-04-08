---
description: Weitere Informationen zum folgenden Diagramm finden Sie unter Entity Relationship Diagram-Legende.
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: Kern Tabellen Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a5cc87e80c60505025825353272699db574bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960644"
---
# <a name="core-tables-group"></a>Kern Tabellen Gruppe

Weitere Informationen zum folgenden Diagramm finden Sie unter [Entity Relationship Diagram-Legende](entity-relationship-diagram-legend.md).

![Kern Tabellen Gruppe](images/core.png)

Die Kerngruppe besteht aus Tabellen, in denen die grundlegenden Features und Komponenten der Anwendung und des Installationspakets beschrieben werden. Entwickler von Installationspaketen sollten daher berücksichtigen, wie diese Tabellen zuerst aufgefüllt werden, da die Organisation eines Großteil der Datenbank aus dem Inhalt dieser Gruppe ersichtlich wird.

-   In der [Featuretabelle](feature-table.md) werden alle Funktionen aufgelistet, die zur Anwendung gehören.
-   Die Bedingungs [Tabelle](condition-table.md) enthält die bedingten Ausdrücke, die bestimmen, ob ein bestimmtes Feature installiert wird.
-   In der [FeatureComponents-Tabelle](featurecomponents-table.md) wird beschrieben, welche Komponenten zu den einzelnen Features gehören.
-   In der [Komponenten Tabelle](component-table.md) werden alle Komponenten aufgelistet, die zur Installation gehören.
-   In der [Verzeichnis Tabelle](directory-table.md) sind die Verzeichnisse aufgelistet, die während der Installation benötigt werden. Da jede Komponente nur einem Verzeichnis zugeordnet werden muss, ist die Komponenten Tabelle eng mit dieser Tabelle verknüpft und weist einen externen Schlüssel für die Verzeichnis Tabelle auf.
-   In der [Tabelle PublishComponent](publishcomponent-table.md) werden die Features und Komponenten aufgelistet, die für die Verwendung durch andere Anwendungen veröffentlicht werden. [Komponenten und Funktionen](components-and-features.md) sind die zwei Arten von featureankündigungen.
-   Die [MsiAssembly-Tabelle](msiassembly-table.md) gibt Windows Installer Einstellungen für .NET Framework Common Language Runtime Assemblys und Win32-Assemblys an.
-   Die [MsiAssemblyName-Tabelle](msiassemblyname-table.md) gibt das Schema für die Elemente eines starken Assemblycache-namens für eine Common Language Runtime-oder Win32-Assembly an.
-   Die [complus-Tabelle](complus-table.md) enthält Informationen, die zum Installieren von com+-Anwendungen erforderlich sind.
-   Die [isolatedcomponent-Tabelle](isolatedcomponent-table.md) ordnet die in der Spalte Komponenten \_ Anwendung angegebene Komponente (i. a. exe) der Komponente zu, die in der freigegebenen Spalte der Komponente angegeben ist \_ (häufig eine freigegebene DLL).
-   Die [upgradetabelle](upgrade-table.md) enthält Informationen, die bei [größeren Upgrades](major-upgrades.md)erforderlich sind.

 

 



