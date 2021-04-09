---
description: Die Counter Data-Tabelle enthält eine Zeile für jeden Indikator, der zu einem bestimmten Zeitpunkt erfasst wird. Es wird eine große Anzahl dieser Zeilen angezeigt.
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: Gegen Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4604ce9886a6c4e3caa847dcf41a2d50b46d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865127"
---
# <a name="counterdata"></a>Gegen Daten

Die **Counter Data** -Tabelle enthält eine Zeile für jeden Indikator, der zu einem bestimmten Zeitpunkt erfasst wird. Es wird eine große Anzahl dieser Zeilen angezeigt.

Die **Counter Data** -Tabelle definiert die folgenden Felder:

-   **GUID:** GUID für dieses DataSet. Verwenden Sie diesen Schlüssel, um mit der [**displaytoid**](displaytoid.md) -Tabelle zu verknüpfen.
-   **Counter ID:** Identifiziert den-Wert. Verwenden Sie diesen Schlüssel, um mit der [**Counter Details**](counterdetails.md) -Tabelle zu verknüpfen.
-   **RecordIndex:** Der Beispiel Index für einen bestimmten Indikator Bezeichner und eine Sammlungs-GUID. Der Wert erhöht sich für jedes nachfolgende Beispiel in dieser Protokolldatei.
-   **Counterdatetime:** Der Zeitpunkt, zu dem die Sammlung gestartet wurde, in UTC-Zeit.
-   **CounterValue:** Der formatierte Wert des Zählers. Dieser Wert kann für den ersten Datensatz 0 (null) sein, wenn der Leistungs Besatz zwei Stichproben benötigt, um einen anzeigbaren Wert zu berechnen.
-   **Firstvaluea:** Kombinieren Sie diesen 32-Bit-Wert mit dem Wert von **firstvalueb** , um den **FirstValue** -Member des [**PDH- \_ rohleistungs \_ Zählers**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)zu erstellen. **Firstvaluea** enthält die Bits mit niedriger Reihenfolge.
-   **Firstvalueb:** Kombinieren Sie diesen 32-Bit-Wert mit dem Wert von **firstvaluea** , um den **FirstValue** -Member des [**PDH- \_ rohleistungs \_ Zählers**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)zu erstellen. **Firstvalueb** enthält die hohen Bestell Bits.
-   **Secondvaluea:** Kombinieren Sie diesen 32-Bit-Wert mit dem Wert **secondvalueb** , um den **SecondValue** -Member des [**PDH- \_ rohleistungs \_ Zählers**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)zu erstellen. **Secondvaluea** enthält die Bits mit niedriger Reihenfolge.
-   **Secondvalueb:** Kombinieren Sie diesen 32-Bit-Wert mit dem Wert **secondvaluea** , um den **SecondValue** -Member des [**PDH- \_ rohleistungs \_ Zählers**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)zu erstellen. **Secondvalueb** enthält die hohen Bestell Bits.

Die Felder **GUID**, **counterId** und **recordIndex** bilden den Primärschlüssel für diese Tabelle.

 

 



