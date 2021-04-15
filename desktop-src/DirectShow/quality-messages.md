---
description: Qualitäts Meldungen
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: Qualitäts Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b290833be7550e255590a5bcda449ce19743c0b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521328"
---
# <a name="quality-messages"></a>Qualitäts Meldungen

Qualitäts Meldungen werden mit der [**Qualitäts**](/windows/win32/api/strmif/ns-strmif-quality) Struktur definiert. Diese Struktur enthält die folgenden Member:

-   **Typ:** Definiert durch die [**qualitymessagetype**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) -Enumeration. entweder eine Hungersnot, die angibt, dass der Filter zu wenig Daten empfängt, oder Überflutung, was darauf hinweist, dass der Filter zu viele Daten empfängt.
-   **Proportional:** Die angeforderte Anpassung in der Datenrate von der Baseline 1000. 750 gibt beispielsweise an, dass 75% und 1500 150% betragen.
-   **Spät:** Verweis Zeit, die angibt, wie spät das letzte Beispiel erreicht wurde. Der Wert ist negativ, wenn das Beispiel früh eingetroffen ist.
-   **Zeitstempel:** Der Zeitstempel für das letzte Beispiel.

Nehmen wir beispielsweise an, dass ein Beispiel mit einem Zeitstempel von 240 Millisekunden (MS) den Renderer bei 280 ms, streamzeit erreicht. Der Renderer erstellt eine Qualitäts Nachricht vom Typ Hungersnot. Das Beispiel wurde 40 ms nach dem Ende erreicht, sodass das **späte** Mitglied 400000 ist. (Alle Verweis Zeiten befinden sich in 100-Nanosecond-Einheiten.) Der **timestamp** -Member ist 2,4 Millionen.

Für das **proportional** Element kann der Renderer einen laufenden Durchschnitt verwenden, um den Wert zu berechnen. Möglicherweise sind Beispiele in der Zeit eingetroffen, und dieses Beispiel ist eine Anomalie. In diesem Fall kann der Renderer nur eine kleine Korrektur anfordern. Wenn die Stichproben dagegen konsistent sind, kann der Renderer eine größere Korrektur anfordern.

Die Qualitätskontrolle wird durch die [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) -Schnittstelle behandelt. Sie enthält zwei Methoden.

-   [**Benachrichtigen**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): sendet eine Qualitäts Nachricht.
-   [**Setsink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): gibt einen benutzerdefinierten Quality Manager an.

Ein Objekt, das **iqualitycontrol** implementiert, empfängt Qualitäts Nachrichten über seine **Benachrichtigungs** Methode. Die Nachricht kann entweder verarbeitet oder an ein anderes Objekt übergeben werden. Wenn die Anwendung die **setsink** -Methode des Objekts aufruft, sollte das Objekt die Qualitätskontrolle an den angegebenen Quality Manager delegieren.

 

 



