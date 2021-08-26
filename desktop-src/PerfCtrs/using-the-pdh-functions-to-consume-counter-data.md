---
description: Sie verwenden die PDH-Funktionen, um Leistungsdaten zu sammeln.
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: Verwenden der PDH-Funktionen zum Nutzen von Indikatordaten
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 6c506e3c7a73a94a6bc3c282920e17504e28dedb42e0e3bee8a6f05a1e77ebbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033190"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a>Verwenden der PDH-Funktionen zum Nutzen von Indikatordaten

Verwenden Sie die PDH-Funktionen, um Leistungsdaten zu sammeln. Die PDH-Funktionen sind einfacher zu verwenden als die [Registrierungsfunktionen](using-the-registry-functions-to-consume-counter-data.md) und können für den Zugriff auf Indikatordaten sowohl für V1- als auch für V2-Anbieter verwendet werden. PDH verfügt über APIs zum Sammeln aktueller Leistungsdaten, Speichern von Leistungsdaten in Protokolldateien und Lesen von Daten aus Protokolldateien.

> [!Note]
> Sie können die Funktionen der Leistungsdatenhilfs-Abstraktionsebene nicht verwenden, wenn Sie Windows OneCore-Apps schreiben. Verwenden Sie stattdessen [die PerfLib V2-Consumerfunktionen](using-the-perflib-functions-to-consume-counter-data.md).

PDH ist eine high-level-API, die das Sammeln von Leistungsindikatordaten vereinfacht. Sie unterstützt Sie bei der Abfrageparsierung, beim Zwischenspeichern von Metadaten, beim Abgleichen von Instanzen zwischen Stichproben, beim Berechnen formatierter Werte aus Rohwerten, beim Lesen von Daten aus Protokolldateien und beim Speichern von Daten in Protokolldateien. PDH verwendet beim Sammeln von Daten von **V1-Anbietern** automatisch die [Registrierungsfunktionen](using-the-registry-functions-to-consume-counter-data.md) und beim Sammeln von Daten von **V2-Anbietern** die [V2-Consumerfunktionen.](using-the-perflib-functions-to-consume-counter-data.md)

Führen Sie die folgenden Schritte aus, um Leistungsdaten mithilfe der PDH-Funktionen zu sammeln.

1. [Erstellen einer Abfrage](creating-a-query.md)
2. [Hinzufügen von Leistungsindikatoren zur Abfrage](creating-a-query.md)
3. [Sammeln der Leistungsdaten](collecting-performance-data.md)
4. [Anzeigen der Leistungsdaten](displaying-performance-data.md)
5. [Schließen der Abfrage](creating-a-query.md)

Sie können Leistungsdaten aus Echtzeitquellen oder Protokolldateien sammeln. Weitere Informationen zum Schreiben von Leistungsdaten in Protokolldateien finden Sie unter [Arbeiten mit Protokolldateien.](working-with-log-files.md)

## <a name="see-also"></a>Siehe auch

- [Sammeln von Leistungsdaten](collecting-performance-data.md)
- [Durchsuchen von Indikatoren](browsing-counters.md)
- [Überprüfen der Rückgabewerte der PDH-Schnittstelle](checking-pdh-interface-return-values.md)
- [Beispiele](examples.md)
