---
description: Um eine Form mit einer Volltonfarbe zu füllen, erstellen Sie ein SolidBrush-Objekt, und übergeben Sie dann die Adresse dieses SolidBrush-Objekts als Argument an eine der Füllmethoden der Graphics-Klasse.
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: Auffüllen einer Form mit einer Volltonfarbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ad3ecb5efb3bde32f696db8b97319d89834886eb63a70cd45289e49db03863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036718"
---
# <a name="filling-a-shape-with-a-solid-color"></a>Auffüllen einer Form mit einer Volltonfarbe

Um eine Form mit einer Volltonfarbe zu füllen, erstellen Sie ein [**SolidBrush-Objekt,**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) und übergeben Sie dann die Adresse dieses **SolidBrush-Objekts** als Argument an eine der Füllmethoden der [**Graphics-Klasse.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Das folgende Beispiel zeigt, wie eine Ellipse mit der Farbe Rot auffüllt:


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



Im vorherigen Beispiel verwendet der [**SolidBrush-Konstruktor**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) einen [**Color-Objektverweis**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) als einziges Argument. Die vom Color-Konstruktor verwendeten **Werte** stellen die Alpha-, Rot-, Grün- und Blaukomponenten der Farbe dar. Jeder dieser Werte muss im Bereich von 0 bis 255 liegen. Der erste 255 gibt an, dass die Farbe vollständig deckend ist, und der zweite 255 gibt an, dass die rote Komponente mit voller Intensität ist. Die beiden Nullen geben an, dass die grünen und blauen Komponenten beide eine Intensität von 0 haben.

Die vier Zahlen (0, 0, 100, 60), die an die [**Graphics::FillEllipse-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) übergeben werden, geben die Position und Größe des umgebundenen Rechtecks für die Ellipse an. Das Rechteck hat eine obere linke Ecke von (0, 0), eine Breite von 100 und eine Höhe von 60.

 

 
