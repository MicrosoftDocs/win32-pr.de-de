---
description: Zum Bearbeiten eines Bilds, das in einer erweiterten Metadatei gespeichert ist, muss eine Anwendung die im folgenden Verfahren beschriebenen Aufgaben ausführen.
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: Bearbeiten einer erweiterten Metadatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86dc9cc609d616bf82ae3f0a13d8d63e827e3eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130784"
---
# <a name="editing-an-enhanced-metafile"></a>Bearbeiten einer erweiterten Metadatei

Zum Bearbeiten eines Bilds, das in einer erweiterten Metadatei gespeichert ist, muss eine Anwendung die im folgenden Verfahren beschriebenen Aufgaben ausführen.

**So bearbeiten Sie ein Bild, das in einer erweiterten Metadatei gespeichert ist**

1.  Verwenden Sie Treffer Tests, um die Cursor Koordinaten zu erfassen und die Position des Objekts (Linie, Bogen, Rechteck, Ellipse, Polygon oder unregelmäßige Form) abzurufen, die der Benutzer ändern möchte.
2.  Konvertieren Sie diese Koordinaten in logische (oder weltweite) Einheiten.
3.  Nennen Sie die [**enumenhmetafile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) -Funktion, und untersuchen Sie jeden Metadateidatensatz.
4.  Bestimmen Sie, ob ein bestimmter Datensatz einer GDI-Zeichnungs Funktion entspricht.
5.  Wenn dies der Fall ist, stellen Sie fest, ob die im Datensatz gespeicherten Koordinaten der Zeile, dem Bogen, der Ellipse oder einem anderen Grafik Element entsprechen, das die vom Benutzer angegebenen Koordinaten überschneidet.
6.  Wenn Sie den Datensatz ermitteln, der der Ausgabe entspricht, die der Benutzer ändern möchte, löschen Sie das Objekt auf dem Bildschirm, das dem ursprünglichen Datensatz entspricht.
7.  Löschen Sie den entsprechenden Datensatz aus der Metadatendatei, und speichern Sie einen Zeiger auf den Speicherort.
8.  Ermöglicht dem Benutzer das erneute zeichnen oder Ersetzen des Objekts.
9.  Konvertieren Sie die GDI-Funktionen, die zum Zeichnen des neuen Objekts verwendet werden, in einen oder mehrere Enhanced-Metafile-Datensätze.
10. Speichern Sie diese Datensätze in der erweiterten Metadatei.

 

 



