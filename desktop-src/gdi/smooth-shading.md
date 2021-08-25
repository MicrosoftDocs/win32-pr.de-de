---
description: Smooth Shading ist eine Methode zum Schattieren eines Bereichs mit einem Farbverlauf.
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: Smooth Shading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5bfa54fef8d0a6810a3230e88e4e3144f7ecf4b62f7313f5daf4213e948c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965200"
---
# <a name="smooth-shading"></a>Smooth Shading

*Smooth Shading* ist eine Methode zum Schattieren eines Bereichs mit einem Farbverlauf. Das Einschließen von Farbinformationen zusammen mit den Begrenzungen des Zeichnen-Primitivs gibt den Farbverlauf an. GDI interpoliert linear die Farbe des innerhalb des Primitiven, der an die Farbendpunkte übergeben wird. Farb- und Scheitelpunktinformationen sind in position-Informationen in der [**TRIVERTEX-Struktur**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) enthalten.

Verwenden Sie die [**GradientFill-Funktion,**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) um ein Dreieck oder eine Rechteckstruktur zu füllen. Um ein Dreieck mit smooth shading zu füllen, rufen Sie **GradientFill** mit den drei Dreiecksendpunkten auf. Um ein Rechteck mit smooth shading zu füllen, rufen Sie **GradientFill** mit den Oberen linken und unteren rechten Rechteckkoordinaten auf. **GradientFill** verweist auf die [**STRUKTUREN TRIVERTEX,**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) [**GRADIENT \_ RECT**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)und [**GRADIENT \_ TRIANGLE.**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle)

Ein Beispiel finden Sie unter [Zeichnen eines schattierten Dreiecks.](drawing-a-shaded-triangle.md)

 

 



