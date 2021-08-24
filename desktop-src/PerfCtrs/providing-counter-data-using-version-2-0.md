---
description: Mit Version 2.0 haben Leistungsindikatoren die Architektur geändert, um den Prozess für die Bereitstellung von Indikatordaten für Consumer zu vereinfachen.
ms.assetid: 37f75b15-3f52-4259-a6d9-5a1a14f88379
title: Bereitstellen von Indikatordaten mit Version 2.0
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8e839fb72f8cbd8272f9afd89aa3456e1e0b08fc7197dd992b1069fec7ce108d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143793"
---
# <a name="providing-counter-data-using-version-20"></a>Bereitstellen von Indikatordaten mit Version 2.0

Moderne Leistungsdatenanbieter verwenden ein Manifest, um die Indikatordaten zu definieren, und verwenden Leistungsindikatoranbieter-APIs, um Daten im Kontext des Anbieters zu verwalten. Anbieter, die mithilfe von Manifest- und Leistungsindikatoranbieter-APIs implementiert werden, werden häufig als **V2-Anbieter** bezeichnet. Windows unterstützt V2-Anbieter im Benutzermodus auf Windows Vista oder höher und Kernelmodus-V2-Anbieter auf Windows 7 oder höher.

Auf dieser Seite werden V2-Anbieter im Benutzermodus beschrieben. Informationen zu Kernelmodus-V2-Anbietern finden Sie unter [Kernelmodus-Leistungsüberwachung.](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring)

Zur Laufzeit funktionieren V2-Anbieter wie folgt:

- Der Anbieterprozess registriert sich selbst beim Windows Leistungsindikatorsystem, indem PerfStartProvider und PerfSetCounterSetInfo aufgerufen werden. Der Anbieter stellt optional eine Rückruffunktion bereit, die über Consumeranforderungen benachrichtigt wird.
- Der Anbieterprozess fügt instanzen mit perfCreateInstance und PerfDeleteInstance nach Bedarf hinzu oder entfernt sie. Der Anbieter aktualisiert Leistungsindikatorwerte, wenn sie sich mithilfe von PerfSet-APIs ändern.
- Ein Consumer stellt eine Anforderung für Daten aus einem Counterset. Das System überprüft, ob der Aufrufer über Berechtigungen zum Sammeln der Daten verfügt. Das System verwendet dann einen Arbeitsthread, der im Anbieterprozess ausgeführt wird, um die Anforderung zu verarbeiten, und ruft ggf. die Rückruffunktion des Anbieters auf. Der Arbeitsthread kopiert die gesammelten Daten in einen vom System verwalteten Puffer, und das System gibt die Daten dann an den Consumer zurück.

## <a name="steps-to-creating-a-provider"></a>Schritte zum Erstellen eines Anbieters

1. Schreiben Sie ein Manifest, das die Indikatordaten definiert, die ihr Anbieter bereitstellt. Ausführliche Informationen zum Schreiben des Manifests finden Sie unter [Schema für Leistungsindikatoren.](performance-counters-schema.md)
2. Verwenden Sie [CTRPP,](ctrpp.md) um den Vorlagencode zu generieren, den Sie in Ihren Anbieter einschließen. Der Vorlagencode enthält die Strukturen, die die Indikatorensätze definieren, die Funktionen [**CounterInitialize**](counterinitialize.md) und [**CounterCleanup**](countercleanup.md) sowie die Ressourcenzeichenfolgen.

   Ihr Anbieter muss die Funktionen [**CounterInitialize**](counterinitialize.md) und [**CounterCleanup**](countercleanup.md) aufrufen. **CounterInitialize** ruft die [**PerfStartProvider-Funktion**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) auf, um den Anbieter zu registrieren, und ruft auch die [**PerfSetCounterSetInfo-Funktion**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) auf, um den Indikatorsatz zu initialisieren. **CounterCleanup** ruft die [**PerfStopProvider-Funktion**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) auf, um die Registrierung des Anbieters zu entfernen.

3. Fügen Sie den Vorlagencode aus dem vorherigen Schritt in Ihr Projekt ein, und schließen Sie Ihren Anbieter ab.

   Um den Anbieter abzuschließen, müssen Sie die [**PerfCreateInstance-Funktion**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance) für jede Instanz des von Ihnen festgelegten Indikatorensatzes aufrufen.

   Um die Zählerwerte festzulegen, rufen Sie eine der folgenden Funktionen auf:

   - [**PerfSetULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
   - [**PerfSetULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
   - [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)

   Der Vorteil der Verwendung von [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue) besteht darin, dass Sie keinen Funktionsaufruf durchführen müssen, um den Indikatorwert festzulegen oder zu aktualisieren. Sie aktualisieren einfach Ihre lokale Indikatorvariable (die Variable, auf die die Verweispunkte verweisen), und Leistungsindikatoren verwenden den Zeiger, um auf den Indikatorwert zuzugreifen.

   Wenn Sie [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)nicht verwenden, können Sie die folgenden Funktionen verwenden, um den Indikatorwert zu erhöhen oder zu dekrementieren:

   - [**PerfDecrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
   - [**PerfDecrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
   - [**PerfIncrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
   - [**PerfIncrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)

   Bevor der Anbieter beendet wird, muss er die [**PerfDeleteInstance**](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance) für jede erstellte Indikatorsatzinstanz aufrufen.

   Wenn Sie  das Rückrufattribut im [**Provider-Element**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) im Manifest angegeben oder das **-NotificationCallback-Argument** beim Aufrufen von [CTRPP](ctrpp.md)verwendet haben, müssen Sie die [*ControlCallback-Rückruffunktion*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) implementieren. Sie übergeben die Rückruffunktion an [**CounterInitialize**](counterinitialize.md).

   Wenn Sie die **-MemoryRoutines** beim Aufrufen von [CTRPP](ctrpp.md)verwendet haben, müssen Sie die Rückruffunktionen [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) und [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) implementieren. Sie übergeben die Rückruffunktionen an [**CounterInitialize**](counterinitialize.md).

4. Verwenden Sie bei der Installation Ihres Anbieters das LodCtr-Tool, um den Namen der Binärdatei, die die lokalisierten Ressourcenzeichenfolgen und Ressourcen-IDs enthält, in die Registrierung zu schreiben. Ausführliche Informationen zur Verwendung von LodCtr finden Sie unter [Schema der Leistungsindikatoren.](performance-counters-schema.md)

5. Verwenden Sie beim Deinstallieren Ihres Anbieters das UnlodCtr-Tool, um die Informationen Ihres Anbieters aus der Registrierung zu entfernen.
