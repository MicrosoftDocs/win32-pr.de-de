---
description: Sie verwenden die PDH-Funktionen, um Leistungsdaten zu erfassen.
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: Verwenden der PDH-Funktionen zum Verarbeiten von Counter-Daten
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 431bf160ef6ca54b4a37363d7fe6ed48bb25d953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865088"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a>Verwenden der PDH-Funktionen zum Verarbeiten von Counter-Daten

Verwenden Sie die PDH-Funktionen, um Leistungsdaten zu erfassen. Die PDH-Funktionen sind einfacher zu verwenden als die [Registrierungsfunktionen](using-the-registry-functions-to-consume-counter-data.md) und können verwendet werden, um auf die Daten des Dienstanbietern v1 und v2 zuzugreifen. PDH verfügt über APIs zum Erfassen aktueller Leistungsdaten, zum Speichern von Leistungsdaten in Protokolldateien und zum Lesen von Daten aus Protokolldateien.

> [!Note]
> Wenn Sie Windows onecore-apps schreiben, können Sie die Funktionen für die Abstraktionsschicht der Leistungsdaten nicht verwenden. Verwenden Sie stattdessen [Perflib v2-consumerfunktionen](using-the-perflib-functions-to-consume-counter-data.md).

PDH ist eine API auf hoher Ebene, die das Sammeln von Leistungsdaten für Leistungsdaten vereinfacht. Es unterstützt die Abfrage Verarbeitung, das Zwischenspeichern von Metadaten, das Zuordnen von Instanzen zwischen Beispielen, das berechnen formatierter Werte aus unformatierten Werten, das Lesen von Daten aus Protokolldateien und das Speichern von Daten in Protokolldateien. PDH verwendet automatisch die [Registrierungsfunktionen](using-the-registry-functions-to-consume-counter-data.md) beim Sammeln von Daten von **v1-Anbietern** und verwendet die V2- [consumerfunktionen](using-the-perflib-functions-to-consume-counter-data.md) beim Sammeln von Daten von **v2-Anbietern**.

Führen Sie die folgenden Schritte aus, um Leistungsdaten mithilfe der PDH-Funktionen zu erfassen.

1. [Erstellen einer Abfrage](creating-a-query.md)
2. [Zähler zur Abfrage hinzufügen](creating-a-query.md)
3. [Erfassen der Leistungsdaten](collecting-performance-data.md)
4. [Anzeigen der Leistungsdaten](displaying-performance-data.md)
5. [Schließen der Abfrage](creating-a-query.md)

Sie können Leistungsdaten entweder aus echtzeitquellen oder Protokolldateien erfassen. Weitere Informationen zum Schreiben von Leistungsdaten in Protokolldateien finden Sie unter [Arbeiten mit Protokolldateien](working-with-log-files.md).

## <a name="see-also"></a>Siehe auch

- [Sammeln von Leistungsdaten](collecting-performance-data.md)
- [Leistungsindikatoren durchsuchen](browsing-counters.md)
- [Rückgabewerte der PDH-Schnittstelle werden überprüft](checking-pdh-interface-return-values.md)
- [Beispiele](examples.md)
