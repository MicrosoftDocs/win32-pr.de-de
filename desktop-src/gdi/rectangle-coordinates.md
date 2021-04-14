---
description: Eine Anwendung muss eine Rect-Struktur verwenden, um ein Rechteck zu definieren.
ms.assetid: 93c63dcb-6c8e-4c8b-aa19-6f8952d75e2e
title: Rechteck Koordinaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8a3fbc3f42c6d69a3d0eac6555b85fbfc1eecb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993902"
---
# <a name="rectangle-coordinates"></a>Rechteck Koordinaten

Eine Anwendung muss eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur verwenden, um ein Rechteck zu definieren. Die-Struktur gibt die Koordinaten zweier Punkte an: die linke obere und untere rechte Ecke des Rechtecks. Die Seiten des Rechtecks werden von diesen beiden Punkten erweitert und sind parallel zur x-und y-Achse.

Die Koordinaten Werte für ein Rechteck werden als ganze Zahlen mit Vorzeichen ausgedrückt. Der Koordinaten Wert der rechten Seite eines Rechtecks muss größer sein als der Wert der linken Seite. Ebenso muss der Koordinaten Wert des unteren Werts größer als der obere Wert sein.

Da Anwendungen Rechtecke für viele verschiedene Zwecke verwenden können, verwenden die Rechteck Funktionen keine explizite Maßeinheit. Stattdessen werden alle Rechteck Koordinaten und-Dimensionen in signierten, logischen Werten angegeben. Der Mapping-Modus und die Funktion, in der das Rechteck verwendet wird, bestimmen die Maßeinheiten. Weitere Informationen zu Koordinaten und Karten Modi finden Sie unter [Koordinaten Bereiche und Transformationen](coordinate-spaces-and-transformations.md).

 

 
