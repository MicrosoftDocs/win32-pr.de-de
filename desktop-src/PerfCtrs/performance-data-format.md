---
description: Das Format der von der RegQueryValueEx-Funktion abgerufenen Daten beginnt mit der Headerstruktur PERF \_ DATA BLOCK mit fester \_ Länge.
ms.assetid: a68fa617-834c-4ad9-b922-fac3a648ad75
title: Format der Leistungsdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea20d0cc0be6174fdd945c4bf956d7df60a067cd9f20b3d08d9762d75b8b97a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143916"
---
# <a name="performance-data-format"></a>Format der Leistungsdaten

Das Format der von der [**RegQueryValueEx-Funktion**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) abgerufenen Daten beginnt mit der Headerstruktur [**PERF \_ DATA BLOCK mit \_ fester Länge.**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block) Die **PERF \_ DATA \_ BLOCK-Struktur** beschreibt das System und die Leistungsdaten. Auf **die PERF \_ DATA \_ BLOCK-Struktur** folgt eine variable Anzahl von Objektdatenelementen variabler Länge. Der Header jedes Objektelements enthält den Offset des nächsten Objektelements in der Liste. Das folgende Diagramm zeigt die grundlegende Struktur der Leistungsdaten.

![Leistungsdatenstruktur](images/perfdata.png)

Es gibt zwei Formate für die Objektdatenelemente: eins, das mehrere Instanzen unterstützt, und das andere, das nicht mehrere Instanzen unterstützt.

Jeder Objektdatenelementblock enthält eine [**PERF \_ OBJECT \_ TYPE-Struktur,**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) die die Leistungsdaten für das Objekt beschreibt. Auf **die PERF \_ OBJECT \_ TYPE-Struktur** folgt eine Liste von [**PERF COUNTER \_ \_ DEFINITION-Strukturen,**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) eine für jeden für das Objekt definierten Leistungsindikator. Für ein Objekt mit nur einer Instanz folgt auf die Liste der **PERF \_ COUNTER \_ DEFINITION-Strukturen** eine einzelne [**PERF \_ COUNTER \_ BLOCK-Struktur,**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) gefolgt von den Indikatordaten. Jede **PERF \_ COUNTER \_ DEFINITION-Struktur** enthält den Offset vom Anfang der **PERF COUNTER \_ \_ BLOCK-Struktur** zu den entsprechenden Indikatordaten. Das folgende Diagramm zeigt die Struktur eines Leistungsobjekts, das mehrere Instanzen nicht unterstützt.

![Struktur des Leistungsobjekts, das nicht mehrere Instanzen unterstützt](images/perfnoinst.png)

Bei einem Objekttyp, der mehrere Instanzen unterstützt, folgt auf die Liste der [**PERF \_ COUNTER \_ DEFINITION-Strukturen**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) eine Liste von Instanzinformationsblöcken (eins für jede Instanz). Jeder Instanzinformationsblock enthält eine [**PERF \_ INSTANCE \_ DEFINITION-Struktur,**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition) den Namen der Instanz und eine [**PERF \_ COUNTER \_ BLOCK-Struktur.**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) Das folgende Diagramm zeigt die Struktur eines Leistungsobjekts, das zwei -Instanzen unterstützt.

![Struktur eines Leistungsobjekts, das zwei Instanzen unterstützt](images/perfinst.png)

Ein Beispiel, in dem die Offsets verwendet werden, finden Sie unter [Anzeigen von Objekt-, Instanz- und Indikatornamen.](displaying-object-instance-and-counter-names.md)

 

 
