---
description: Obwohl eine Anwendung Farbe ohne Berücksichtigung der Farbfunktionen des Geräts verwenden kann, ist die resultierende Ausgabe möglicherweise nicht so informativ und ansprechend wie die Ausgabe, für die die Farbe sorgfältig ausgewählt wird.
ms.assetid: 008c8a8e-3456-4727-9b27-00b20ae880a2
title: Farbannäherungen und Dithering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9733259aff787856ac9c6fed68f708c3b580c6200b65652424264eef3c73d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761967"
---
# <a name="color-approximations-and-dithering"></a>Farbannäherungen und Dithering

Obwohl eine Anwendung Farbe ohne Berücksichtigung der Farbfunktionen des Geräts verwenden kann, ist die resultierende Ausgabe möglicherweise nicht so informativ und ansprechend wie die Ausgabe, für die die Farbe sorgfältig ausgewählt wird. Nur wenige Geräte garantieren ggf. eine genaue Übereinstimmung für jeden möglichen Farbwert. Wenn eine Anwendung daher eine Farbe anfordert, die das Gerät nicht generieren kann, nähert sich das System dieser Farbe mithilfe einer Farbe, die das Gerät generieren kann. Wenn eine Anwendung beispielsweise versucht, einen roten Stift für einen Schwarz-Weiß-Drucker zu erstellen, erhält sie einen schwarzen Stift, stattdessen verwendet das System Schwarz als Näherung für Rot.

Eine Anwendung kann mithilfe der [**GetColor-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestcolor) ermitteln, ob das System eine bestimmte Farbe annähert. Die Funktion verwendet einen Farbwert und gibt den Farbwert der am nächsten übereinstimmenden Farbe zurück, die das Gerät generieren kann. Welche Methode das System verwendet, um diese Näherung zu bestimmen, hängt vom Gerätetreiber und seinen Farbfunktionen ab. In den meisten Fällen ist die gesamte Intensität der geschätzten Farbe der der angeforderten Farbe am nächsten.

Wenn eine Anwendung einen Stift erstellt oder die Farbe für Text festlegt, entspricht das System immer einer Farbe, wenn keine genaue Übereinstimmung vorhanden ist. Wenn eine Anwendung einen volltonigen Pinsel erstellt, versucht das System möglicherweise, die angeforderte Farbe durch Dithering zu simulieren. *Beim Dithering* wird eine Farbe simuliert, indem zwei oder mehr Farben in einem Muster abwechselnd verwendet werden. Beispielsweise können verschiedene Schattierungen von Rosa simuliert werden, indem verschiedene Kombinationen aus Rot und Weiß abwechselnd verwendet werden. Abhängig von den Farben und dem Muster kann das Dithering sinnvolle Simulationen erzeugen. Sie ist besonders nützlich für monocolore Geräte, da sie die Anzahl der verfügbaren "Farben" weit über einfaches Schwarz-Weiß hinaus erweitert.

Welche Methode zum Erstellen von farbengebundenen Farben verwendet wird, hängt vom Gerätetreiber ab. Die meisten Gerätetreiber verwenden einen Standard-Ditheringalgorithmus, der ein Muster generiert, das auf den Intensitätswerten der angeforderten Farben Rot, Grün und Blau basiert. Im Allgemeinen wird jede angeforderte Farbe, die nicht vom Gerät generiert werden kann, einer Simulation unterzogen, aber eine Anwendung wird nicht benachrichtigt, wenn das System eine Farbe simuliert. Darüber hinaus kann eine Anwendung den Ditheringalgorithmus des Gerätetreibers nicht ändern oder ändern. Eine Anwendung kann den Algorithmus jedoch umgehen, indem Musterpinsel erstellt und verwendet werden. Auf diese Weise erstellt die Anwendung ihre eigenen geblendeten Farben, indem Sie Volltonfarben in der Bitmap kombinieren, die sie zum Erstellen des Pinsels verwendet.

 

 



