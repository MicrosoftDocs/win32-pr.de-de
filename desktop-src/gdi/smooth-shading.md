---
description: Smooth Schattierung ist eine Methode zum Schattieren einer Region mit einem Farbverlauf.
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: Smooth-Schattierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b73738c03147083099a5070e61fe21ca5cac76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217046"
---
# <a name="smooth-shading"></a>Smooth-Schattierung

*Smooth Schattierung* ist eine Methode zum Schattieren einer Region mit einem Farbverlauf. Durch Einschließen von Farbinformationen, zusammen mit den Begrenzungen des Zeichnungs primitiven, wird der Farbverlauf angegeben. GDI linear interpoliert die Farbe des Inneren des primitiven, das an die Farb Endpunkte weitergegeben wurde. Farb-und Vertex-Informationen sind in der-Struktur der [**dreiseitigen**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) Position in Positionsinformationen enthalten.

Verwenden Sie die [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) -Funktion, um ein Dreieck oder eine Rechteck Struktur auszufüllen. Zum Auffüllen eines Dreiecks mit Smooth Schattierung aufrufen Sie **GradientFill** mit den drei Dreieck Endpunkten. Zum Auffüllen eines Rechtecks mit Smooth Schattierung aufrufen Sie **GradientFill** mit den linken oberen und unteren rechten Rechteck Koordinaten. **GradientFill** verweist auf die [**trivertex**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)-, [**\_ gradientenrect**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)-und [**Gradient- \_ Dreiecks**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) Strukturen.

Ein Beispiel finden Sie unter [Zeichnen eines schattierten Dreiecks](drawing-a-shaded-triangle.md).

 

 



