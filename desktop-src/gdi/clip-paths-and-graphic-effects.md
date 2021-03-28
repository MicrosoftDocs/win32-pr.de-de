---
description: Eine Anwendung kann Clipping und Pfade verwenden, um besondere grafische Effekte zu erstellen. Die folgende Abbildung zeigt eine Text Zeichenfolge, die mit einer großen Arial-Schriftart gezeichnet wird.
ms.assetid: fda0d627-406c-44f9-9061-7aea3e2d7f66
title: Clip Pfade und grafische Effekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8156a8670747175502b2385e6c24a340345a54f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528391"
---
# <a name="clip-paths-and-graphic-effects"></a>Clip Pfade und grafische Effekte

Eine Anwendung kann Clipping und Pfade verwenden, um besondere grafische Effekte zu erstellen. Die folgende Abbildung zeigt eine Text Zeichenfolge, die mit einer großen Arial-Schriftart gezeichnet wird.

![Abbildung mit schwarzem Text auf weißem Hintergrund](images/cspth-02.png)

Die nächste Abbildung zeigt das Ergebnis der Auswahl des Texts als Clip Pfad und das Zeichnen von radialen Linien für einen Kreis, dessen Mitte sich oberhalb und Links von der Zeichenfolge befindet.

![Darstellung des gleichen Texts, aber mit Zeilen anstelle von Solid Black](images/cspth-03.png)

> [!Note]  
> Vor dem Hinzufügen von Text, der mit einer bitzugeordneten Schriftart erstellt wurde, zu einem Pfad wird von der Grafikgeräte Schnittstelle (Graphics Device Interface, GDI) eine Umwandlung der Schriftart in eine Kontur

 

Eine Anwendung erstellt einen Clip Pfad, indem eine Pfad Klammer generiert und dann die [**selectclippath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) -Funktion aufgerufen wird. Nachdem ein Clip Pfad in einem Domänen Controller ausgewählt wurde, wird die Ausgabe nur innerhalb der Rahmen des Pfads angezeigt.

Neben der Erstellung spezieller Grafikeffekte sind Clip-Pfade auch nützlich für Anwendungen, die Bilder als erweiterte Metadatendateien speichern. Mithilfe eines Clip-Pfads kann eine Anwendung die Geräteunabhängigkeit sicherstellen, weil die zum Angeben eines Pfads verwendeten Einheiten logische Einheiten sind.

 

 



