---
description: Eine Anwendung kann Clipping und Pfade verwenden, um spezielle grafische Effekte zu erstellen. Die folgende Abbildung zeigt eine Textzeichenfolge, die mit einer großen Arial-Schriftart gezeichnet wird.
ms.assetid: fda0d627-406c-44f9-9061-7aea3e2d7f66
title: ClipPfade und grafische Effekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c80605f4dc58846f3a9e8440801d46768384c103ff6e3f9df5e3d448d9b12aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038158"
---
# <a name="clip-paths-and-graphic-effects"></a>ClipPfade und grafische Effekte

Eine Anwendung kann Clipping und Pfade verwenden, um spezielle grafische Effekte zu erstellen. Die folgende Abbildung zeigt eine Textzeichenfolge, die mit einer großen Arial-Schriftart gezeichnet wird.

![Abbildung mit schwarzem Text auf weißem Hintergrund](images/cspth-02.png)

Die nächste Abbildung zeigt das Ergebnis der Auswahl des Texts als Ausschneidepfad und zeichnen radiale Linien für einen Kreis, dessen Mitte sich über und links von der Zeichenfolge befindet.

![Abbildung, die den gleichen Text zeigt, aber mit Zeilen anstelle von voll schwarzem Text gefüllt ist](images/cspth-03.png)

> [!Note]  
> Bevor GDI (Graphics Device Interface) einem Pfad Text hinzufügt, der mit einer Bitmapschriftart erstellt wurde, wird die Schriftart in eine Kontur- oder Vektorschriftart konvertiert.

 

Eine Anwendung erstellt einen Clippfad, indem sie eine Pfadklammer generiert und dann die [**SelectClipPath-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) aufruft. Nachdem ein Ausschneidepfad in einem DC ausgewählt wurde, wird die Ausgabe nur innerhalb der Rahmen des Pfads angezeigt.

Neben der Erstellung spezieller Grafikeffekte sind Clippfade auch in Anwendungen nützlich, die Bilder als erweiterte Metadateien speichern. Mithilfe eines Clippfads kann eine Anwendung die Geräteunabhängigkeit sicherstellen, da es sich bei den einheiten, die zum Angeben eines Pfads verwendet werden, um logische Einheiten handelt.

 

 



