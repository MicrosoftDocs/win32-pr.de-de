---
description: MPEG-Beispieleigenschaften
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: MPEG-Beispieleigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78872b41c579f6af594280b064bfbefc65ef13e8b9d4abf8c21ba9b19613bcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075790"
---
# <a name="mpeg-sample-properties"></a>MPEG-Beispieleigenschaften

MPEG-Beispiele weisen die folgenden Merkmale auf.

**Zeitstempel**

Nicht alle Beispiele haben Start- und Stoppzeiten. Die Beispielstoppzeit für Paket- und Nutzlastdaten ist nicht hilfreich. sie wird in der Regel auf die Startzeit plus eins festgelegt. Für MPEG-Paket- oder Nutzlastdatenbeispiele wird eine Start- und Beendigungszeit festgelegt, wenn das Systemebenenpaket, aus dem sie generiert werden, über ein gültiges PTS verfügt.

Weitere Informationen zu Zeitstempeln finden Sie im Abschnitt 2.4.1 von ISO1-11172: "Der Paketheader kann Decodierungs- und/oder Präsentationszeitstempel (DTS und PTS) enthalten, die auf die erste Zugriffseinheit im Paket verweisen."

Bei \_ MPEG Stream-Haupttypen ist die Startzeit die Byteposition des ersten Byte, bewertet mit 1 Byte pro Sekunde. Die Beendigungszeit ist die Byteposition des letzten Byte. Daher sollte für aufeinanderfolgende Stichproben die Beendigungszeit des ersten Pakets gleich der Startzeit des nächsten Pakets sein. Bei Video-CD Daten muss der Ursprung des Mediums mit dem Format einer Video-CD-Datei übereinstimmen, die von CDFS mit dem standardmäßigen CSV-Block am Anfang verfügbar gemacht wird.

Bei MPEG-Videopaket- und Nutzlasttypen ist der Zeitstempel die Präsentationszeit für den ersten Videoframe, dessen Bildstartcode im Beispiel beginnt.

Bei MPEG-Audiopaket- und Nutzlasttypen ist der Zeitstempel die Präsentationszeit für den ersten Audioframe, dessen Synchronisierungscode im Beispiel beginnt.

Es wird davon ausgegangen, dass Paket- und Nutzlastdaten ohne Zeitstempel erfolgreich von den Behandlungsfiltern vorabrolliert werden können.

**Unterbrechungen**

Wenn der Datenstrom unterbrochen wird (z. B. eine Lücke in den Echtzeitdaten oder ein Fehler in den Daten oder nach einer Suche), wird die Diskontinuitätseigenschaft im nächsten Medienbeispiel festgelegt. Dies ermöglicht auch eine Zeitstempel-Diskontinuität.

**End-of-Stream-Benachrichtigungen**

Wenn der Decoder diese Benachrichtigung empfängt, muss er alle gepufferten Daten verarbeiten. Alle neuen Daten müssen dann mit der Diskontinuitätseigenschaft beginnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MPEG-2-Unterstützung in DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



