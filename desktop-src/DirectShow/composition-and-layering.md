---
description: Komposition und Ebenenerstellung
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: Komposition und Ebenenerstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7dce1e1df87b5ffc5c65e9090c6fb7266b972d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346390"
---
# <a name="composition-and-layering"></a>Komposition und Ebenenerstellung

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

In einer Auflistung von Spuren hat der erste Titel die niedrigste Priorität (Priorität 0), und jede nachfolgende Spur hat eine Priorität, die eine Ebene höher ist. Auf jeder Prioritätsstufe blenden die Quell Clips in dieser Nachverfolgung die Quell Clips in den nachstehenden Spuren aus, es sei denn, diese Ebene enthält auch einen Übergang. Daher können Sie sich vorstellen, dass es beim Rendern mehrere Durchgänge gibt.

Zuerst wird Track 0 gerendert. Es gibt keine "unter"-Nachverfolgung 0, sodass leere Bereiche als solides schwarzes Bild gerendert werden. Übergänge in dieser Ebene treten zwischen dem schwarzen Bild und der Nachverfolgung 0 oder umgekehrt auf. Des legt den Titel 1 auf der Nachverfolgung 0 fest und erzeugt dabei alle Übergänge zwischen den beiden Titeln. Das Ergebnis ist die Zusammensetzung der beiden Titel. Anschließend wird Track 2 auf diesem zusammengesetzten platziert. Übergänge auf dieser Ebene treten zwischen dem zusammengesetzten und dem Track 2 auf. Der Prozess wird fortgesetzt, bis die letzte (höchste Priorität) nachverfolgt wird.

Wenn mehrere Spuren zusammengeführt werden, Verhalten Sie sich wie ein einzelner Track (virtueller Titel genannt). Das Kompositions Objekt kapselt dieses Verhalten, sodass komplexe Übergänge möglich sind. Beispielsweise kann ein Videoclip auf einen zweiten Clip gesetzt werden, während der zusammengesetzte (beide Clips und das Löschen) zu einem dritten Clip werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einführung in DirectShow-Bearbeitungs Dienste](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



