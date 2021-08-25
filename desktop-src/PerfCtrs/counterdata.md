---
description: Die CounterData-Tabelle enthält eine Zeile für jeden Leistungsindikator, der zu einem bestimmten Zeitpunkt erfasst wird. Es wird eine große Anzahl dieser Zeilen geben.
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: Counterdata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b352b9ec6bde6e644d80e7556ac46211212b66b4d92601deedaecaa5dd07344
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033990"
---
# <a name="counterdata"></a>Counterdata

Die **CounterData-Tabelle** enthält eine Zeile für jeden Leistungsindikator, der zu einem bestimmten Zeitpunkt erfasst wird. Es wird eine große Anzahl dieser Zeilen geben.

Die **CounterData-Tabelle** definiert die folgenden Felder:

-   **GUID:** GUID für dieses DataSet. Verwenden Sie diesen Schlüssel, um eine Verknüpfung mit der [**Tabelle DisplayToID**](displaytoid.md) zu erstellen.
-   **CounterID:** Identifiziert den Zähler. Verwenden Sie diesen Schlüssel, um eine Verknüpfung mit der [**CounterDetails-Tabelle**](counterdetails.md) zu erstellen.
-   **RecordIndex:** Der Beispielindex für einen bestimmten Indikatorbezeichner und eine Sammlungs-GUID. Der Wert erhöht sich für jedes aufeinander folgende Beispiel in dieser Protokolldatei.
-   **CounterDateTime:** Die Zeit, zu der die Sammlung gestartet wurde (UTC-Zeit).
-   **CounterValue:** Der formatierte Wert des Leistungsindikators. Dieser Wert kann für den ersten Datensatz 0 (null) sein, wenn der Indikator zwei Stichproben erfordert, um einen anzeigebaren Wert zu berechnen.
-   **FirstValueA:** Kombinieren Sie diesen 32-Bit-Wert mit dem **Wert von FirstValueB,** um das **FirstValue-Member** von [**PDH RAW COUNTER zu \_ \_ erstellen.**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) **FirstValueA** enthält die Bits in niedriger Reihenfolge.
-   **FirstValueB:** Kombinieren Sie diesen 32-Bit-Wert mit dem **Wert von FirstValueA,** um den **FirstValue-Member** von [**PDH RAW COUNTER zu \_ \_ erstellen.**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) **FirstValueB** enthält die hohen Bits.
-   **SecondValueA:** Kombinieren Sie diesen 32-Bit-Wert mit dem Wert **von SecondValueB,** um den **SecondValue-Member** von [**PDH \_ RAW COUNTER zu \_ erstellen.**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) **SecondValueA** enthält die Bits in niedriger Reihenfolge.
-   **SecondValueB:** Kombinieren Sie diesen 32-Bit-Wert mit dem Wert **von SecondValueA,** um den **SecondValue-Member** von [**PDH \_ RAW COUNTER zu \_ erstellen.**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) **SecondValueB** enthält die hohen Bits.

Die **Felder GUID,** **CounterID** und **RecordIndex** machen den Primärschlüssel für diese Tabelle aus.

 

 



