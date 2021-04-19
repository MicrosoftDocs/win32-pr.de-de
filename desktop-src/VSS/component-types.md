---
description: Komponenten geben die Art der Daten an, die Sie durch einen Typ darstellen.
ms.assetid: 19d785d5-09a7-48b9-a0a2-eca3049d67fe
title: Komponenten Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f89355b4b26090b7d43f9753c086b4ccc79df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352359"
---
# <a name="component-types"></a>Komponenten Typen

Komponenten geben die Art der Daten an, die Sie durch einen Typ darstellen.

Derzeit sind Komponenten Typen (siehe [**VSS \_ - \_ Komponententyp**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) auf Folgendes beschränkt:

-   Datenbankkomponenten
-   Dateigruppen

Implementierungs Informationen zum Festlegen von Komponenten Typen finden Sie unter [Definition von Komponenten durch Writer](definition-of-components-by-writers.md).

Writer verfügen über eine Typisierung, die ihre Verwendung angibt (siehe [**VSS- \_ \_ Quelltyp**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)). Dies kann wie folgt lauten:

-   Eine transaktionale Datenbank (z. b. ein SQL Server)
-   Eine nicht transaktionale Datenbank (z. b. ein Tabellen-Client)
-   Datei Gruppe (sonstige)

Wenn Sie einen Komponententyp als Datenbank angeben, kann der Inhalt leichter identifiziert werden, und es wird eine separate Verarbeitung von Protokoll-und Datendateien ermöglicht (Weitere Informationen finden Sie unter [**ivsskreateschreitermetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) und [**ivssexaminewrite Metadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) ). und erzwingt eine größere Sorgfalt in der Dateiauswahl, indem weder eine rekursive Dateiauswahl noch ein [*Alternativer Pfad*](vssgloss-a.md) verwendet wird (siehe [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) und [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)).

Wenn eine Dateigruppen Komponente andererseits nicht weiß, welche Daten Sie enthält, haben Sie mehr Freiheit, wie Dateien eingefügt werden, da Sie rekursive Spezifikationen und alternative Pfade verwenden können.

In Zukunft können zusätzliche Komponenten Typen hinzugefügt werden.

 

 



