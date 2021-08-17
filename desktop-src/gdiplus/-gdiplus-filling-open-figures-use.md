---
description: Sie können einen Pfad ausfüllen, indem Sie die Adresse eines GraphicsPath-Objekts an die Graphics::FillPath-Methode übergeben.
ms.assetid: 4cf293cf-5155-4ce2-afeb-cc9ca9395764
title: Auffüllen von offenen Zahlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198a1a9e3a3cffa6aa5c0f3627c1415a54c8842c9f90a2ebdd6ebc2a9e0f3fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977540"
---
# <a name="filling-open-figures"></a>Auffüllen von offenen Zahlen

Sie können einen Pfad ausfüllen, indem Sie die Adresse eines [**GraphicsPath-Objekts**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) an die [**Graphics::FillPath-Methode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) übergeben. Die **Graphics::FillPath-Methode** füllt den Pfad entsprechend dem Füllmodus (alternativ oder Ziehmodus), der derzeit für den Pfad festgelegt ist. Wenn der Pfad offene Abbildungen enthält, wird der Pfad so gefüllt, als wären diese Abbildungen geschlossen. GDI+ schließt eine Figur, indem eine gerade Linie vom Endpunkt bis zum Anfangspunkt gezeichnet wird.

Im folgenden Beispiel wird ein Pfad erstellt, der eine offene Abbildung (einen Bogen) und eine geschlossene Abbildung (eine Ellipse) enthält. Die [**Graphics::FillPath-Methode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) füllt den Pfad gemäß dem Standardfüllmodus aus, der FillModeAlternate ist.


```
GraphicsPath path;

// Add an open figure.
path.AddArc(0, 0, 150, 120, 30, 120);

// Add an intrinsically closed figure.
path.AddEllipse(50, 50, 50, 100);

Pen pen(Color(128, 0, 0, 255), 5);
SolidBrush brush(Color(255, 255, 0, 0));

// The fill mode is FillModeAlternate by default.
graphics.FillPath(&brush, &path);
graphics.DrawPath(&pen, &path);
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes. Beachten Sie, dass der Pfad (gemäß FillModeAlternate) so gefüllt ist, als ob die geöffnete Figur durch eine gerade Linie vom Endpunkt bis zum Anfangspunkt geschlossen wäre.

![Abbildung einer hohen Ellipse, die die untere Hälfte einer breiten Ellipse überlappt; Die Union ist gefüllt, aber die Schnittmenge ist leer.](images/fillopenpath.png)

 

 



