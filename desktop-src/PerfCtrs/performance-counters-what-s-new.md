---
description: In diesem Abschnitt werden die neuen Features beschrieben, die den Leistungsindikatoren für jedes Release hinzugefügt wurden.
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: Neues (Leistungsindikatoren)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c86a6a9ea644f1c650137cc392a2d54b6e8eedb34881d6b759d7b6c51635d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674700"
---
# <a name="whats-new-with-performance-counters"></a>Neues bei Leistungsindikatoren

In diesem Abschnitt werden die neuen Features beschrieben, die den Leistungsindikatoren für jedes Release hinzugefügt wurden.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 und Windows Server 2008 R2

Das [CTRPP-Tool](ctrpp.md) wurde geändert, um die Codegenerierung zu verbessern und zu vereinfachen. Das Tool generiert jetzt nur noch einen Header und eine Ressourcendatei. Wenn Sie altes Codegenerierungsverhalten verwenden möchten (nicht empfohlen), können Sie das neue Argument `-legacy` verwenden.

- Sie müssen nun die neuen Argumente und angeben, die den Namen und Speicherort `-o` `-rc` der Header- bzw. Ressourcendatei angeben.
- Sie können das optionale neue Argument verwenden, um eine Zeichenfolge anzugeben, die am Anfang der globalen Variablen und Funktionen hinzugefügt werden soll, die `-prefix` in der generierten Headerdatei definiert sind.
- Wenn Sie Ihr Leistungsindikatormanifest aktualisieren müssen, entfällt bei Verwendung der neuen Codegenerierung die Notwendigkeit, Ihre vorherige Rückrufimplementierung mit dem neuen generierten Code zusammen zu führen, da die Rückrufe nicht mehr im generierten Code enthalten sind.

Für die `symbol` folgenden Manifestelemente ist ein neues Attribut verfügbar:

- [Anbieter](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [Counterset](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [Zähler](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

Das `symbol` -Attribut ist für provider [und](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) [counterSet erforderlich](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)und für den Indikator [optional.](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element) Mit dem -Attribut können Sie einen symbolischen Namen angeben, mit dem Sie beim Aufrufen der Anbieterfunktionen auf jedes Element verweisen können (Sie können z. B. den symbolischen Indikatorsatznamen verwenden, wenn [Sie PerfCreateInstance aufrufen).](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)

## <a name="windows-vista"></a>Windows Vista

Die Architektur der Leistungsindikatoren für die Bereitstellung von Indikatordaten wurde für dieses Release vollständig geändert.

Zuvor haben Sie eine INI-Datei verwendet, um Ihre Indikatordaten zu definieren, und Sie haben eine Leistungs-DLL implementiert, die im Prozess des Consumers zum Bereitstellen der Daten durchgeführt wurde, als ein Consumer sie angefordert hat. Diese Architektur ist veraltet und wird aufgrund von erheblichen Leistungs- und Zuverlässigkeitsproblemen nicht für neuen Code empfohlen.

Die neue Architektur verwendet ein Manifest, um die Indikatordaten zu definieren, und führt Code im Prozess des Anbieters aus, um die Daten zur Verfügung zu stellen, wenn ein Consumer sie an fordert. Weitere Informationen finden Sie unter [Bereitstellen von Indikatordaten mit Version 2.0.](providing-counter-data-using-version-2-0.md)

Für dieses Release wurden die folgenden Funktionen hinzugefügt:

- [ControlCallback](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [PerfDeleteInstance](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [PerfQueryInstance](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [PerfSetCounterSetInfo](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [PerfSetULongCounterValue](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [PerfSetULongLongCounterValue](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [PerfSetCounterRefValue](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [PerfStartProvider](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [PerfStopProvider](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

Für dieses Release wurden die folgenden Strukturen hinzugefügt:

- [\_ \_ LEISTUNGSINDIKATORIDENTITÄT](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [\_ \_ LEISTUNGSINDIKATORINFORMATIONEN](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [\_LEISTUNGSINDIKATORSATZINFORMATIONEN \_](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [PERF \_ \_ COUNTERSET-INSTANZ](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

Eine Liste der XML-Elemente, die Sie in Ihrem Manifest zum Definieren der Leistungsindikatoren verwenden, finden Sie unter [Schema der Leistungsindikatoren.](performance-counters-schema.md)

Informationen zum CTRPP-Vorprozessortool, das Ihr Manifest analysiert und den Code generiert, den Sie als Ausgangspunkt für Ihren Anbieter verwenden, finden Sie unter [CTRPP](ctrpp.md).
