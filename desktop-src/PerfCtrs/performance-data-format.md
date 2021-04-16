---
description: Das Format der Daten, die von der RegQueryValueEx-Funktion abgerufen werden, beginnt mit einer Header Struktur mit fester Länge, dem Leistungs \_ Daten \_ Block.
ms.assetid: a68fa617-834c-4ad9-b922-fac3a648ad75
title: Leistungsdaten Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88029634594843a50fd6010993eb6517dce831f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567234"
---
# <a name="performance-data-format"></a>Leistungsdaten Format

Das Format der Daten, die von der [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) -Funktion abgerufen werden, beginnt mit einer Header Struktur mit fester Länge, dem Leistungs [**\_ Daten \_ Block**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block). Die **perf- \_ Daten \_ Block** Struktur beschreibt das System und die Leistungsdaten. Auf die **perf- \_ Daten \_ Block** Struktur folgt eine Variable Anzahl von Objektdaten Elementen variabler Länge. Der-Header der einzelnen Objekt Elemente enthält den Offset des nächsten Objekt Elements in der Liste. Das folgende Diagramm zeigt die grundlegende Leistungsdaten Struktur.

![Leistungsdaten Struktur](images/perfdata.png)

Es gibt zwei Formate für die Objektdaten Elemente: eine, die mehrere Instanzen unterstützt, und die andere, die mehrere Instanzen nicht unterstützt.

Jeder Objektdaten Element Block enthält eine [**perf \_ - \_ Objekttyp**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) Struktur, die die Leistungsdaten für das Objekt beschreibt. Auf die **perf- \_ \_ Objekttyp** -Struktur folgt eine Liste von [**perf \_ \_**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) -Leistungs-Leistungs-Leistungs-Leistungs Zuordnungen, eine für jeden für das-Objekt definierten Bei einem Objekt mit nur einer Instanz folgt der Liste der **perf- \_ counter- \_ Definitions** Strukturen eine einzelne [**perf-Objekt \_ \_ Block**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) Struktur, gefolgt von den Leistungsdaten. Jede **perf \_ counter- \_ Definitions** Struktur enthält den Offset vom Beginn der **perf-Leistungs \_ \_ Block** Struktur zu den entsprechenden Leistungsdaten. Das folgende Diagramm zeigt die Struktur eines Leistungsobjekts, das mehrere Instanzen nicht unterstützt.

![Struktur des Leistungsobjekts, das mehrere Instanzen nicht unterstützt](images/perfnoinst.png)

Bei einem Objekttyp, der mehrere Instanzen unterstützt, folgt der Liste der perf-Leistungs Objekt- [**\_ \_ Definitions**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) Strukturen eine Liste von Instanzen Informations Blöcken (eine für jede Instanz). Jeder instanzinformationblock enthält eine [**perf- \_ \_ instanzdefinitionsstruktur**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition) , den Namen der Instanz und eine Leistungs [**Block- \_ \_ Block**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) Struktur. Das folgende Diagramm zeigt die Struktur eines Leistungsobjekts, das zwei-Instanzen unterstützt.

![Struktur eines Leistungsobjekts, das zwei Instanzen unterstützt](images/perfinst.png)

Ein Beispiel, in dem die Offsets verwendet werden, finden Sie unter [Anzeigen von Objekt-, Instanz-und indikatorennamen](displaying-object-instance-and-counter-names.md).

 

 
