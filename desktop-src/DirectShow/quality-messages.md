---
description: Qualitätsnachrichten
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: Qualitätsnachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15224e147d363a6cf3f3a55971d35a3d6596d95f07b9897ab1f258cc7febad48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747700"
---
# <a name="quality-messages"></a>Qualitätsnachrichten

Qualitätsmeldungen werden mit der [**Quality-Struktur**](/windows/win32/api/strmif/ns-strmif-quality) definiert. Diese Struktur enthält die folgenden Member:

-   **Typ:** Definiert durch die [**QualityMessageType-Enumeration;**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) entweder Fyl, das angibt, dass der Filter zu wenig Daten empfängt, oder Überflutung, was angibt, dass der Filter zu viele Daten empfängt.
-   **Anteil:** Die angeforderte Anpassung der Datenrate von einer Baseline von 1.000. Beispielsweise gibt 750 75 % und 1500 150 % an.
-   **Spät:** Referenzzeit, die angibt, wie spät das letzte Beispiel eingetroffen ist. Der Wert ist negativ, wenn die Stichprobe früh eingetroffen ist.
-   **TimeStamp:** Der Zeitstempel des letzten Beispiels.

Angenommen, ein Beispiel mit einem Zeitstempel von 240 Millisekunden (ms) erreicht den Renderer bei 280 ms Streamzeit. Der Renderer erstellt eine Qualitätsmeldung vom Typ Fyl. Das Beispiel ist 40 ms spät eingetroffen, sodass **das Late-Mitglied** 400000 ist. (Alle Verweiszeiten liegen in Einheiten von 100 Nanosekunden.) Das **TimeStamp-Member** ist 2400000.

Für das **Proportion-Member** kann der Renderer einen laufenden Durchschnitt verwenden, um den Wert zu berechnen. Möglicherweise sind die Beispiele zur Zeit eintreffen, und dieses Beispiel ist eine Anomalie. In diesem Fall fordert der Renderer möglicherweise nur eine kleine Korrektur an. Andererseits kann der Renderer eine größere Korrektur anfordern, wenn Die Beispiele ständig zu spät sind.

Die Qualitätskontrolle erfolgt über die [**IQualityControl-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) Sie enthält zwei Methoden.

-   [**Benachrichtigen:**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)Sendet eine Qualitätsnachricht.
-   [**SetSink:**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink)Gibt einen benutzerdefinierten Qualitäts-Manager an.

Ein Objekt, das **IQualityControl implementiert,** empfängt Qualitätsnachrichten über seine **Notify-Methode.** Er kann entweder die Nachricht verarbeiten oder die Nachricht an ein anderes Objekt übergeben. Wenn die Anwendung die **SetSink-Methode** des Objekts aufruft, sollte das Objekt die Qualitätskontrolle an den angegebenen Qualitäts-Manager delegieren.

 

 



