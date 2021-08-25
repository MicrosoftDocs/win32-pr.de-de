---
description: Eine Reihe von Funktionen verwendet den pinsel, der derzeit in einem Gerätekontext ausgewählt ist, um Bitmapvorgänge auszuführen.
ms.assetid: 98fb2fd5-9cf4-4016-9e30-ec724e77cebc
title: Bitmaps als Pinsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee8e218180ab646de1c9c8ff622be1bcc268df73f6f4bb0b6df82482c9a2c851
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944250"
---
# <a name="bitmaps-as-brushes"></a>Bitmaps als Pinsel

Eine Reihe von Funktionen verwendet den pinsel, der derzeit in einem Gerätekontext ausgewählt ist, um Bitmapvorgänge auszuführen. Beispielsweise repliziert die [**PatBlt-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) den Pinsel in einem rechteckigen Bereich innerhalb eines Fensters, und die [**FloodFill-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) repliziert den Pinsel innerhalb eines Bereichs in einem Fenster, das durch die angegebene Farbe begrenzt ist (im Gegensatz zu **PatBlt** füllt **FloodFill** nicht überschneidende Formen).

Die [**FloodFill-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) repliziert den Pinsel innerhalb eines Bereichs, der durch eine angegebene Farbe begrenzt ist. Im Gegensatz zur [**PatBlt-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) kombiniert **FloodFill** jedoch nicht die Farbdaten für den Pinsel mit den Farbdaten für die Pixel auf der Anzeige. Sie legt einfach die Farbe aller Pixel innerhalb des eingeschlossenen Bereichs auf der Anzeige auf die Farbe des Pinsels fest, der derzeit im Gerätekontext ausgewählt ist.

 

 



