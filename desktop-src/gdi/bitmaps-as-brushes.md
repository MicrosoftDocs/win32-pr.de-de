---
description: Eine Reihe von Funktionen verwenden den aktuell ausgewählten Pinsel in einem Gerätekontext, um bitmapvorgänge auszuführen.
ms.assetid: 98fb2fd5-9cf4-4016-9e30-ec724e77cebc
title: Bitmaps als Pinsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c693e3c144dec2d26eccca1f1b628252dea187c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215215"
---
# <a name="bitmaps-as-brushes"></a>Bitmaps als Pinsel

Eine Reihe von Funktionen verwenden den aktuell ausgewählten Pinsel in einem Gerätekontext, um bitmapvorgänge auszuführen. Beispielsweise wird der Pinsel mit der [**patblt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) -Funktion in einem rechteckigen Bereich innerhalb eines Fensters repliziert, und die Funktion zum [**Auffüllen**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) repliziert den Pinsel innerhalb eines Bereichs in einem Fenster, das durch die angegebene Farbe begrenzt ist (im Gegensatz zu **patblt** werden bei der über **flufill** -Funktion nicht rechteckige Formen aufgefüllt).

Die [**flufill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) -Funktion repliziert den Pinsel innerhalb eines Bereichs, der durch eine angegebene Farbe begrenzt ist. Anders als bei der [**patblt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) -Funktion kombiniert die über **flufill** -Funktion jedoch nicht die Farbdaten für den Pinsel mit den Farbdaten für die Pixel auf der Anzeige. Dadurch wird einfach die Farbe aller Pixel innerhalb des eingeschlossenen Bereichs auf der Anzeige auf die Farbe des Pinsels festgelegt, der derzeit im Gerätekontext ausgewählt ist.

 

 



