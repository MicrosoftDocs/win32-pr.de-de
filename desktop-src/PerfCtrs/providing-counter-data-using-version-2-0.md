---
description: Mit Version 2,0 haben Leistungsindikatoren die Architektur geändert, um den Prozess für die Bereitstellung von Leistungsindikator Daten für Consumer zu vereinfachen.
ms.assetid: 37f75b15-3f52-4259-a6d9-5a1a14f88379
title: Bereitstellen von Counter-Daten mit Version 2,0
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 67976c8a0b6c77582ed8c50c2e5cf753c77fcf6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349218"
---
# <a name="providing-counter-data-using-version-20"></a>Bereitstellen von Counter-Daten mit Version 2,0

Die Anbieter von modernen Leistungsdaten verwenden ein Manifest zum Definieren der Leistungsdaten und zum Verwalten von Daten im Kontext des Anbieters. Anbieter, die mit einem Manifest und Leistungs Anbieter-APIs implementiert werden, werden häufig als **v2-Anbieter** bezeichnet. Windows unterstützt Benutzermodus-v2-Anbieter unter Windows Vista oder höher und Kernel Modus-v2-Anbieter unter Windows 7 oder höher.

Auf dieser Seite werden Benutzermodus v2-Anbieter beschrieben. Weitere Informationen zu Kernel Modus-v2-Anbietern finden Sie unter [Kernel Mode Performance Monitoring](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).

Zur Laufzeit funktionieren v2-Anbieter wie folgt:

- Der Anbieter Prozess registriert sich selbst beim Windows-Leistungsindikator System, indem perfstartprovider und perfsetcountersetinfo aufgerufen werden. Der Anbieter stellt optional eine Rückruffunktion bereit, die über Consumeranforderungen benachrichtigt wird.
- Der Anbieter Prozess fügt mithilfe von perfkreateinstance und perfdelta eteinstance Instanzen nach Bedarf hinzu oder entfernt Sie. Der Anbieter aktualisiert Leistungswerte bei der Änderung mithilfe von perfset * * _-APIs.
- Ein Consumer sendet eine Anforderung an Daten aus einem CounterSet. Das System überprüft, ob der Aufrufer über Berechtigungen zum Sammeln der Daten verfügt. Das System verwendet dann einen Arbeits Thread, der im Anbieter Prozess ausgeführt wird, um die Anforderung zu verarbeiten, wobei die Rückruffunktion des Anbieters bei Bedarf aufgerufen wird. Der Arbeits Thread kopiert die gesammelten Daten in einen vom System verwalteten Puffer, und das System gibt die Daten dann an den Consumer zurück.

## <a name="steps-to-creating-a-provider"></a>Schritte zum Erstellen eines Anbieters

1. Schreiben Sie ein Manifest, das die vom Anbieter bereitgestellten gegen Daten definiert. Ausführliche Informationen zum Schreiben des Manifests finden Sie unter [Leistungsindikator Schema](performance-counters-schema.md).
2. Verwenden Sie [ctrpp](ctrpp.md) , um den Vorlagen Code zu generieren, den Sie in Ihren Anbieter einschließen. Der Vorlagen Code umfasst die Strukturen, die die Indikatorensätze definieren, die Funktionen [_ *counterinitialize* *](counterinitialize.md) und [**countercleanup**](countercleanup.md) sowie die Ressourcen Zeichenfolgen.

   Der Anbieter muss die Funktionen [**counterinitialize**](counterinitialize.md) und [**countercleanup**](countercleanup.md) aufzurufen. Die **counterinitialize** -Funktion Ruft die [**perfstartprovider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) -Funktion auf, um den Anbieter zu registrieren, und ruft auch die Funktion [**perfsetcountersetinfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) auf, um den Indikatorsatz zu initialisieren. Das **countercleanup** Ruft die [**perfstopprovider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) -Funktion auf, um die Registrierung des Anbieters zu entfernen.

3. Schließen Sie den Vorlagen Code aus dem vorherigen Schritt in Ihr Projekt ein, und vervollständigen Sie den Anbieter.

   Zum Vervollständigen des Anbieters müssen Sie die [**perfkreateinstance**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance) -Funktion für jede Instanz des von Ihnen bereitgestellten Leistungs Zählers aufrufen.

   Um die Werte für die Zählers festzulegen, müssen Sie eine der folgenden Funktionen aufzurufen:

   - [**Perfsetulongcountervalue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
   - [**Perfsetulonglongcountervalue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
   - [**Perfsetcounterref-Wert**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)

   Der Vorteil der Verwendung von [**perfsetcounterrefvalue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue) besteht darin, dass Sie keinen Funktions aufrufmachen müssen, um den Zählerwert festzulegen oder zu aktualisieren. Sie aktualisieren einfach die lokale Indikator Variable (die Variable, auf die die Verweis Punkte verweisen) und die Leistungsindikatoren verwenden den Zeiger, um auf den Indikator Wert zuzugreifen.

   Wenn Sie [**perfsetcounterrefvalue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)nicht verwenden, können Sie die folgenden Funktionen verwenden, um den Indikator Wert zu erhöhen oder zu verringern:

   - [**Perfdecrementulongcountervalue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
   - [**Perfdecrementulonglongcountervalue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
   - [**Perfinkrementulongcountervalue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
   - [**Perfinkrementulonglongcountervalue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)

   Bevor der Anbieter beendet wird, muss er den [**perfdelta eteinstance**](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance) für jede erstellte Instanz von Counter-Set-Instanz abrufen.

   Wenn Sie das **Rückruf** Attribut im [**Provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) -Element im Manifest angegeben oder das **-notificationcallback-** Argument beim Aufrufen von [ctrpp](ctrpp.md)verwendet haben, müssen Sie die [*controlcallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) -Rückruffunktion implementieren. Sie übergeben die Rückruffunktion an [**counterinitialize**](counterinitialize.md).

   Wenn Sie " **-memoryroutinen** " beim Aufrufen [von ctrpp](ctrpp.md)verwendet haben, müssen Sie die Rückruf Funktionen " [*zugscatememory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) " und " [*Freispeicher*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) " implementieren. Sie übergeben die Rückruf Funktionen an [**counterinitialize**](counterinitialize.md).

4. Verwenden Sie bei der Installation des Anbieters das lodctr-Tool, um den Namen der Binärdatei mit den lokalisierten Ressourcen Zeichenfolgen und Ressourcen-IDs in die Registrierung zu schreiben. Ausführliche Informationen zur Verwendung von lodctr finden Sie unter [Leistungsindikator Schema](performance-counters-schema.md).

5. Wenn Sie den Anbieter deinstallieren, verwenden Sie das unlodctr-Tool, um die Informationen des Anbieters aus der Registrierung zu entfernen.
