---
title: Berechnen von Bitraten-und Puffer Fenster Werten für beliebige Streams
description: Berechnen von Bitraten-und Puffer Fenster Werten für beliebige Streams
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- Streams, Bitraten
- Codecs, berechnen von Bitraten für beliebige Streams
- Bitraten, berechnen für beliebige Streams
- Streams, berechnen von Bitraten für beliebige Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d704352d414b1fe5079fb068593c2d0d8b2f8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036388"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a>Berechnen von Bitraten-und Puffer Fenster Werten für beliebige Streams

Das Berechnen der richtigen Bitrate und des Puffer Fensters für einen beliebigen Streamtyp ist keine exakte Wissenschaft. Ein einfacher Ansatz ist die Festlegung der Bitrate entsprechend der Größe des Streams dividiert durch die Länge in Sekunden. Beispielsweise kann ein Datenstrom, der insgesamt 68000 Bits mit einer Dauer von 20 Sekunden enthält, eine Bitrate von 3400 Bits pro Sekunde aufweisen (68000 Bits/20 Sekunden = 3400 Bits pro Sekunde).

Das Problem bei dieser einfachen Methode zum Zuweisen der Bitrate besteht darin, dass die Verteilung der Daten innerhalb des Streams nicht berücksichtigt wird. Viele beliebige Streams enthalten größere Datenmengen in Intervallen entlang der Zeitachse der Datei. Bild Datenströme verfügen z. b. über Beispiele, die recht groß sind, aber in der Regel mehrere Sekunden voneinander entfernt sind. Das Puffer Fenster muss festgelegt werden, um sicherzustellen, dass der Puffer keinen Überlauf verursacht.

Um das Puffer Fenster zu überprüfen, Multiplizieren Sie die Bitrate (Bits pro Sekunde) mit dem Puffer Fenster (in Sekunden), und teilen Sie durch 1000, um die Größe des Puffers für den Datenstrom in Bits zu erhalten. Stellen Sie dann sicher, dass die Puffergröße groß genug ist, um eine beliebige Kombination von Beispielen im Stream aufzunehmen, die kleiner sind als das Puffer Fenster, das in der Präsentationszeit abweicht. Legen Sie im Zweifelsfall beide Werte etwas höher fest, als Sie vermuten, dass Sie Sie benötigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Pufferung von Inhalten**](buffering-content.md)
</dt> <dt>

[**Konfigurieren beliebiger Streamtypen**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




