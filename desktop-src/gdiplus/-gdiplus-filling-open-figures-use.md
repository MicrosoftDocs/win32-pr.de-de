---
description: 'Sie können einen Pfad ausfüllen, indem Sie die Adresse eines GraphicsPath-Objekts an die Graphics:: FillPath-Methode übergeben.'
ms.assetid: 4cf293cf-5155-4ce2-afeb-cc9ca9395764
title: Auffüllen offener Abbildungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f4a4608b787d8b0af8b9e9c7100a43c0c76dc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565255"
---
# <a name="filling-open-figures"></a>Auffüllen offener Abbildungen

Sie können einen Pfad ausfüllen, indem Sie die Adresse eines [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekts an die [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) -Methode übergeben. Die **Graphics:: FillPath** -Methode füllt den Pfad gemäß dem Füll Modus (Alternative oder Auffüllung), der derzeit für den Pfad festgelegt ist. Wenn für den Pfad offene Abbildungen vorhanden sind, wird der Pfad so aufgefüllt, als ob diese Abbildungen geschlossen wurden. GDI+ schließt eine Abbildung, indem eine gerade Linie von ihrem Endpunkt zum Ausgangspunkt gezeichnet wird.

Im folgenden Beispiel wird ein Pfad erstellt, der über eine offene Abbildung (einen Bogen) und eine geschlossene Abbildung (eine Ellipse) verfügt. Die [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) -Methode füllt den Pfad gemäß dem Standard Füll Modus, der FillModeAlternate ist.


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



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes. Beachten Sie, dass Path (entsprechend FillModeAlternate) ausgefüllt wird, als ob die öffnende Figur durch eine gerade Linie von ihrem Endpunkt bis zum Ausgangspunkt geschlossen wurde.

![die Abbildung zeigt eine hohe Ellipse, die die untere Hälfte einer breiten Ellipse überlappt. die Union ist ausgefüllt, aber die Schnittmenge ist leer.](images/fillopenpath.png)

 

 



