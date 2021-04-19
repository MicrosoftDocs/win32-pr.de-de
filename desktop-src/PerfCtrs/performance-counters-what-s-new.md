---
description: In diesem Abschnitt werden die neuen Features beschrieben, die Leistungsindikatoren für die einzelnen Releases hinzugefügt wurden.
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: Neuerungen (Leistungsindikatoren)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0c1189a185351eabae438a01c6f111952f164e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348012"
---
# <a name="whats-new-with-performance-counters"></a>Neuerungen bei Leistungsindikatoren

In diesem Abschnitt werden die neuen Features beschrieben, die Leistungsindikatoren für die einzelnen Releases hinzugefügt wurden.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 und Windows Server 2008 R2

Das [ctrpp](ctrpp.md) -Tool wurde geändert, um die Codegenerierung zu verbessern und zu vereinfachen. Das Tool generiert nun nur eine Kopfzeile und eine Ressourcen Datei. Wenn Sie das alte Code Generierungs Verhalten (nicht empfohlen) verwenden möchten, können Sie das neue `-legacy` Argument verwenden.

- Sie müssen jetzt das neue `-o` -Argument und das- `-rc` Argument angeben, die den Namen und den Speicherort des Headers bzw. der Ressourcen Datei angeben.
- Sie können das optionale New- `-prefix` Argument verwenden, um eine Zeichenfolge anzugeben, die dem Anfang globaler Variablen und Funktionen hinzugefügt werden soll, die in der generierten Header Datei definiert sind.
- Wenn Sie das Zähler Manifest aktualisieren müssen, entfällt die Verwendung der neuen Codegenerierung darauf, dass Sie die vorherige Rückruf Implementierung mit dem neuen generierten Code zusammenführen müssen, da die Rückrufe nicht mehr im generierten Code enthalten sind.

Ein neues `symbol` Attribut ist für die folgenden Manifest-Elemente verfügbar:

- [ab](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [Indikator](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

Das- `symbol` Attribut ist für den [Anbieter](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) und [CounterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)erforderlich, und ist für [Counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)optional. Mithilfe des-Attributs können Sie einen symbolischen Namen bereitstellen, mit dem Sie auf jedes Element verweisen können, wenn Sie die Anbieter Funktionen aufrufen (Sie können z. b. den symbolischen Namen des Leistungs Zählers beim Aufrufen von [perfcreateinstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)verwenden).

## <a name="windows-vista"></a>Windows Vista

Die Leistungsindikator Architektur für die Bereitstellung von Indikator Daten wurde für diese Version vollständig geändert.

Zuvor haben Sie eine INI-Datei verwendet, um die Leistungsdaten zu definieren, und Sie haben eine Leistungs-dll implementiert, die im Prozess des Consumers ausgeführt wurde, um die Daten anzugeben, wenn ein Consumer Sie angefordert hat. Diese Architektur ist veraltet und wird aufgrund erheblicher Leistungs-und Zuverlässigkeitsprobleme nicht für neuen Code empfohlen.

In der neuen Architektur wird ein Manifest verwendet, um die zählungdaten zu definieren und Code im Prozess des Anbieters ausführen, um die Daten bereitzustellen, wenn ein Consumer Sie anfordert. Weitere Informationen finden Sie unter [Bereitstellen von Counter-Daten mit Version 2,0](providing-counter-data-using-version-2-0.md).

Die folgenden Funktionen wurden für diese Version hinzugefügt:

- [Controlcallback](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [Perfkreateingestance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [Perfdelta eteinstance](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [Perfqueryinstance](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [Perfsetcountersetinfo](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [Perfsetulongcountervalue](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [Perfsetulonglongcountervalue](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [Perfsetcounterref-Wert](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [Perfstartprovider](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [Perfstopprovider](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

Die folgenden Strukturen wurden für diese Version hinzugefügt:

- [Identität des Leistungs \_ Zählers \_](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [Leistungsdaten \_ gegen \_ Info](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [Leistungsindikator \_ \_ Informationen](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [Perf- \_ CounterSet- \_ Instanz](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

Eine Liste der XML-Elemente, die Sie im Manifest zum Definieren der [Leistungsindikatoren](performance-counters-schema.md)verwenden, finden Sie unter Leistungsindikator Schema.

Informationen zum ctrpp-Präprozessortool, das das Manifest analysiert und den Code generiert, den Sie als Ausgangspunkt für Ihren Anbieter verwenden, finden Sie unter [ctrpp](ctrpp.md).
