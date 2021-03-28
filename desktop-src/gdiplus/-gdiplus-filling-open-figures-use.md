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
# <a name="filling-open-figures"></a><span data-ttu-id="2be1e-103">Auffüllen offener Abbildungen</span><span class="sxs-lookup"><span data-stu-id="2be1e-103">Filling Open Figures</span></span>

<span data-ttu-id="2be1e-104">Sie können einen Pfad ausfüllen, indem Sie die Adresse eines [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekts an die [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="2be1e-104">You can fill a path by passing the address of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object to the [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method.</span></span> <span data-ttu-id="2be1e-105">Die **Graphics:: FillPath** -Methode füllt den Pfad gemäß dem Füll Modus (Alternative oder Auffüllung), der derzeit für den Pfad festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2be1e-105">The **Graphics::FillPath** method fills the path according to the fill mode (alternate or winding) currently set for the path.</span></span> <span data-ttu-id="2be1e-106">Wenn für den Pfad offene Abbildungen vorhanden sind, wird der Pfad so aufgefüllt, als ob diese Abbildungen geschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="2be1e-106">If the path has any open figures, the path is filled as if those figures were closed.</span></span> <span data-ttu-id="2be1e-107">GDI+ schließt eine Abbildung, indem eine gerade Linie von ihrem Endpunkt zum Ausgangspunkt gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="2be1e-107">GDI+ closes a figure by drawing a straight line from its ending point to its starting point.</span></span>

<span data-ttu-id="2be1e-108">Im folgenden Beispiel wird ein Pfad erstellt, der über eine offene Abbildung (einen Bogen) und eine geschlossene Abbildung (eine Ellipse) verfügt.</span><span class="sxs-lookup"><span data-stu-id="2be1e-108">The following example creates a path that has one open figure (an arc) and one closed figure (an ellipse).</span></span> <span data-ttu-id="2be1e-109">Die [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) -Methode füllt den Pfad gemäß dem Standard Füll Modus, der FillModeAlternate ist.</span><span class="sxs-lookup"><span data-stu-id="2be1e-109">The [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method fills the path according to the default fill mode, which is FillModeAlternate.</span></span>


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



<span data-ttu-id="2be1e-110">Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.</span><span class="sxs-lookup"><span data-stu-id="2be1e-110">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="2be1e-111">Beachten Sie, dass Path (entsprechend FillModeAlternate) ausgefüllt wird, als ob die öffnende Figur durch eine gerade Linie von ihrem Endpunkt bis zum Ausgangspunkt geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="2be1e-111">Note that path is filled (according to FillModeAlternate) as if the open figure were closed by a straight line from its ending point to its starting point.</span></span>

![die Abbildung zeigt eine hohe Ellipse, die die untere Hälfte einer breiten Ellipse überlappt. die Union ist ausgefüllt, aber die Schnittmenge ist leer.](images/fillopenpath.png)

 

 



