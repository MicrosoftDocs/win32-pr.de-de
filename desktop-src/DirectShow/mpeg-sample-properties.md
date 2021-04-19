---
description: MPEG-Beispiel Eigenschaften
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: MPEG-Beispiel Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c20df4b9285a77d00bd98bc6f21558f0d6b3c60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346408"
---
# <a name="mpeg-sample-properties"></a>MPEG-Beispiel Eigenschaften

MPEG-Beispiele weisen die folgenden Eigenschaften auf.

**Zeitstempel**

Nicht alle Beispiele haben Start-und Endzeit. Die Beispiel Endzeit für Paket-und Nutzlastdaten ist nicht hilfreich. Sie wird in der Regel auf die Startzeit plus 1 festgelegt. Für die Stichproben von MPEG-Paketen oder Nutzlastdaten wird ein Start-und Endzeit Wert festgelegt, wenn das System Schicht Paket, von dem Sie generiert werden, gültige PTS enthält.

Weitere Informationen zu Zeitstempeln finden Sie im Abschnitt 2.4.1 von ISO1 "-11172:" der Paket Header enthält möglicherweise Decodierung und/oder Präsentationszeit Stempel (DTS und PTS), die auf die erste Zugriffs Einheit im Paket verweisen. "

Bei MPEG- \_ Stream-Haupttypen ist die Startzeit die Byte Position des ersten Byte, bewertet bei 1 Byte pro Sekunde. Die Endzeit ist die Byte Position des letzten Bytes. Folglich sollten aufeinanderfolgende Stichproben die Endzeit des ersten Pakets aufweisen, das der Startzeit des nächsten Pakets entspricht. Bei Video-CD-Daten muss der Ursprung des Mediums dem Format einer Video-CD-Datei entsprechen, die von CDFS mit dem standardmäßigen Riff Block am Anfang verfügbar gemacht wird.

Bei MPEG-Video Paketen und Nutz Last Typen ist der Zeitstempel die Präsentationszeit für den ersten Videoframe, dessen Bild Start Code im Beispiel beginnt.

Bei MPEG-Audiopaketen und Nutz Last Typen ist der Zeitstempel die Präsentationszeit für den ersten audioframe, dessen Synchronisierungs Code im Beispiel beginnt.

Es wird davon ausgegangen, dass Paket-und Nutzlastdaten ohne Zeitstempel von den Behandlungs Filtern erfolgreich vorab durchgeführt werden können.

**Unterbrechungen**

Wenn eine Unterbrechung im Stream vorliegt (z. b. eine Lücke in den Echtzeitdaten oder ein Fehler in den Daten oder nach einer Suche), wird die Diskontinuität-Eigenschaft im nächsten Medien Beispiel festgelegt. Dadurch wird auch eine Zeitstempel Diskontinuität ermöglicht.

**Streamende-Benachrichtigungen**

Wenn der Decoder diese Benachrichtigung empfängt, muss er alle gepufferten Daten verarbeiten. Alle neuen Daten müssen dann mit der Diskontinuität-Eigenschaft beginnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MPEG-2-Unterstützung in DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



