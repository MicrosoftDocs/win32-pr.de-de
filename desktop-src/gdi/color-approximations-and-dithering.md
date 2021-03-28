---
description: Obwohl eine Anwendung Farben ohne Berücksichtigung der Farbfunktionen des Geräts verwenden kann, ist die resultierende Ausgabe möglicherweise nicht so informativ und zufrieden wie die Ausgabe, für die die Farbe sorgfältig ausgewählt wird.
ms.assetid: 008c8a8e-3456-4727-9b27-00b20ae880a2
title: Farb Näherungen und Dithering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72e28dbc3ce20a42b53b5ff060d950719e2d861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130824"
---
# <a name="color-approximations-and-dithering"></a>Farb Näherungen und Dithering

Obwohl eine Anwendung Farben ohne Berücksichtigung der Farbfunktionen des Geräts verwenden kann, ist die resultierende Ausgabe möglicherweise nicht so informativ und zufrieden wie die Ausgabe, für die die Farbe sorgfältig ausgewählt wird. Nur wenige, falls vorhanden, garantieren Geräte eine genaue Entsprechung für jeden möglichen Farbwert. Wenn eine Anwendung eine Farbe anfordert, die vom Gerät nicht generiert werden kann, wird die entsprechende Farbe vom System mit einer vom Gerät generierten Farbe angezeigt. Wenn z. b. eine Anwendung versucht, einen roten Stift für einen schwarz-und einen weißen Drucker zu erstellen, erhält Sie einen schwarzen Stift, stattdessen verwendet das System schwarz als Näherung für rot.

Eine Anwendung kann ermitteln, ob das System eine bestimmte Farbe anweist, indem die [**GetNearestColor**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestcolor) -Funktion verwendet wird. Die Funktion nimmt einen Farbwert an und gibt den Farbwert der nächstgelegenen übereinstimmenden Farbe zurück, die vom Gerät generiert werden kann. Die Methode, die das System verwendet, um diese Näherung zu ermitteln, hängt vom Gerätetreiber und seinen Farbfunktionen ab. In den meisten Fällen ist die Gesamtintensität der Näherung der Farbe der angeforderten Farbe am nächsten.

Wenn eine Anwendung einen Stift erstellt oder die Farbe für Text festlegt, gleicht das System immer eine Farbe, wenn keine genaue Entsprechung vorhanden ist. Wenn eine Anwendung einen Pinsel mit voll Tonfarbe erstellt, versucht das System möglicherweise, die angeforderte Farbe durch Dithering zu simulieren. Das *Dithering* simuliert eine Farbe, indem zwei oder mehr Farben in einem Muster abwechselnd angezeigt werden. Beispielsweise können verschiedene Schattierungen von Rosa simuliert werden, indem verschiedene Kombinationen von rot und weiß abwechselnd angezeigt werden. Abhängig von den Farben und dem Muster kann das Dithering sinnvolle Simulationen bewirken. Dies ist besonders nützlich für monochrome Geräte, da dadurch die Anzahl der verfügbaren "Farben" erweitert wird

Die Methode, mit der Dithering-Farben erstellt werden, hängt vom Gerätetreiber ab. Die meisten Gerätetreiber verwenden einen standardmäßigen Dithering-Algorithmus, der auf der Grundlage der Intensität Werte der angeforderten roten, grünen und blauen Farben ein Muster generiert. Im Allgemeinen unterliegen alle angeforderten Farben, die nicht vom Gerät generiert werden können, Simulationen, aber eine Anwendung wird nicht benachrichtigt, wenn das System eine Farbe simuliert. Darüber hinaus kann eine Anwendung den Dithering-Algorithmus des Gerätetreibers nicht ändern oder ändern. Eine Anwendung kann den Algorithmus jedoch durch Erstellen und Verwenden von Muster Pinseln umgehen. Auf diese Weise erstellt die Anwendung eigene Dithering-Farben durch Kombinieren von voll Tonfarben in der Bitmap, die zum Erstellen des Pinsels verwendet werden.

 

 



