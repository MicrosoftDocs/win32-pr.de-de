---
title: Berechnen von Bitraten- und Pufferfensterwerten für beliebige Streams
description: Berechnen von Bitraten- und Pufferfensterwerten für beliebige Streams
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- Streams, Bitraten
- Codecs, Berechnen von Bitraten für beliebige Streams
- Bitraten,Berechnen für beliebige Datenströme
- Streams, Berechnen von Bitraten für beliebige Datenströme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c86a866536bbe2565a3bc44bbe9f40743db26d948555bc6ec8a11eb60d7aa4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434484"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a>Berechnen von Bitraten- und Pufferfensterwerten für beliebige Streams

Das Berechnen der richtigen Bitrate und des Pufferfensters für einen beliebigen Streamtyp ist keine exakte Wissenschaftlichkeit. Ein einfacher Ansatz besteht darin, die Bitrate so festzulegen, dass sie der Größe des Streams dividiert durch seine Länge in Sekunden entspricht. Ein Stream mit insgesamt 68.000 Bits, die 20 Sekunden dauern, kann beispielsweise eine Bitrate von 3.400 Bits pro Sekunde (6.8.000 Bits/20 Sekunden = 3.400 Bits pro Sekunde) aufweisen.

Das Problem bei dieser einfachen Methode zum Zuweisen der Bitrate besteht darin, dass die Verteilung der Daten im Datenstrom nicht berücksichtigt wird. Viele beliebige Datenströme enthalten größere Datenmengen in Intervallen entlang der Zeitachse der Datei. Bildstreams enthalten beispielsweise Stichproben, die recht groß sind, aber in der Regel mehrere Sekunden voneinander entfernt sind. Das Pufferfenster muss festgelegt werden, um sicherzustellen, dass der Puffer nicht überläuft.

Multiplizieren Sie zum Überprüfen des Pufferfensters die Bitrate (Bits pro Sekunde) mit dem Pufferfenster (in Sekunden), und dividieren Sie durch 1000, um die Größe des Puffers für den Stream in Bits abzurufen. Stellen Sie dann sicher, dass die Puffergröße groß genug ist, um eine beliebige Kombination von Stichproben im Stream zu speichern, die in der Präsentationszeit kleiner als das Pufferfenster sind. Legen Sie im Zweifelsfall beide Werte etwas höher fest, als Sie glauben, dass Sie sie benötigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Puffern von Inhalten**](buffering-content.md)
</dt> <dt>

[**Konfigurieren beliebiger Streamtypen**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




