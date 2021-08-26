---
description: Um ein in einer erweiterten Metadatei gespeichertes Bild zu bearbeiten, muss eine Anwendung die im folgenden Verfahren beschriebenen Aufgaben ausführen.
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: Bearbeiten einer erweiterten Metadatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a052be915d966d90a0189376de7e1ff6e27831ebc9c44a0ff6af266b37fa65f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015580"
---
# <a name="editing-an-enhanced-metafile"></a>Bearbeiten einer erweiterten Metadatei

Um ein in einer erweiterten Metadatei gespeichertes Bild zu bearbeiten, muss eine Anwendung die im folgenden Verfahren beschriebenen Aufgaben ausführen.

**So bearbeiten Sie ein in einer erweiterten Metadatei gespeichertes Bild**

1.  Verwenden Sie Treffertests, um die Cursorkoordinaten zu erfassen und die Position des Objekts (Linie, Bogen, Rechteck, Ellipse, Polygon oder unregelmäßige Form) abzurufen, das der Benutzer ändern möchte.
2.  Konvertieren Sie diese Koordinaten in logische Einheiten (oder Welteinheiten).
3.  Rufen Sie die [**EnumEnhMetaFile-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) auf, und untersuchen Sie jeden Metadateidatensatz.
4.  Bestimmen Sie, ob ein angegebener Datensatz einer GDI-Zeichnungsfunktion entspricht.
5.  Wenn dies der Wert ist, bestimmen Sie, ob die im Datensatz gespeicherten Koordinaten der Linie, dem Bogen, der Ellipse oder einem anderen Grafikelement entsprechen, das die vom Benutzer angegebenen Koordinaten überschneidet.
6.  Wenn Sie den Datensatz finden, der der Ausgabe entspricht, die der Benutzer ändern möchte, löschen Sie das Objekt auf dem Bildschirm, das dem ursprünglichen Datensatz entspricht.
7.  Löschen Sie den entsprechenden Datensatz aus der Metadatei, und speichern Sie einen Zeiger auf den Speicherort.
8.  Erlauben Sie dem Benutzer, das Objekt neu zu bzw. zu ersetzen.
9.  Konvertieren Sie die GDI-Funktionen, die zum Zeichnen des neuen Objekts verwendet werden, in einen oder mehrere enhanced-metafile-Datensätze.
10. Store datensätze in der erweiterten Metadatei.

 

 



