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
# <a name="clip-paths-and-graphic-effects"></a><span data-ttu-id="eb551-104">Clip Pfade und grafische Effekte</span><span class="sxs-lookup"><span data-stu-id="eb551-104">Clip Paths and Graphic Effects</span></span>

<span data-ttu-id="eb551-105">Eine Anwendung kann Clipping und Pfade verwenden, um besondere grafische Effekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="eb551-105">An application can use clipping and paths to create special graphic effects.</span></span> <span data-ttu-id="eb551-106">Die folgende Abbildung zeigt eine Text Zeichenfolge, die mit einer großen Arial-Schriftart gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="eb551-106">The following illustration shows a string of text drawn with a large Arial font.</span></span>

![Abbildung mit schwarzem Text auf weißem Hintergrund](images/cspth-02.png)

<span data-ttu-id="eb551-108">Die nächste Abbildung zeigt das Ergebnis der Auswahl des Texts als Clip Pfad und das Zeichnen von radialen Linien für einen Kreis, dessen Mitte sich oberhalb und Links von der Zeichenfolge befindet.</span><span class="sxs-lookup"><span data-stu-id="eb551-108">The next illustration shows the result of selecting the text as a clip path and drawing radial lines for a circle whose center is located above and left of the string.</span></span>

![Darstellung des gleichen Texts, aber mit Zeilen anstelle von Solid Black](images/cspth-03.png)

> [!Note]  
> <span data-ttu-id="eb551-110">Vor dem Hinzufügen von Text, der mit einer bitzugeordneten Schriftart erstellt wurde, zu einem Pfad wird von der Grafikgeräte Schnittstelle (Graphics Device Interface, GDI) eine Umwandlung der Schriftart in eine Kontur</span><span class="sxs-lookup"><span data-stu-id="eb551-110">Before graphics device interface (GDI) adds text created with a bitmapped font to a path, it converts the font to an outline or vector font.</span></span>

 

<span data-ttu-id="eb551-111">Eine Anwendung erstellt einen Clip Pfad, indem eine Pfad Klammer generiert und dann die [**selectclippath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="eb551-111">An application creates a clip path by generating a path bracket and then calling the [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) function.</span></span> <span data-ttu-id="eb551-112">Nachdem ein Clip Pfad in einem Domänen Controller ausgewählt wurde, wird die Ausgabe nur innerhalb der Rahmen des Pfads angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eb551-112">After a clip path is selected into a DC, output only appears within the borders of the path.</span></span>

<span data-ttu-id="eb551-113">Neben der Erstellung spezieller Grafikeffekte sind Clip-Pfade auch nützlich für Anwendungen, die Bilder als erweiterte Metadatendateien speichern.</span><span class="sxs-lookup"><span data-stu-id="eb551-113">In addition to creating special graphics effects, clip paths are also useful in applications that save images as enhanced metafiles.</span></span> <span data-ttu-id="eb551-114">Mithilfe eines Clip-Pfads kann eine Anwendung die Geräteunabhängigkeit sicherstellen, weil die zum Angeben eines Pfads verwendeten Einheiten logische Einheiten sind.</span><span class="sxs-lookup"><span data-stu-id="eb551-114">By using a clip path, an application is able to ensure device independence because the units used to specify a path are logical units.</span></span>

 

 



