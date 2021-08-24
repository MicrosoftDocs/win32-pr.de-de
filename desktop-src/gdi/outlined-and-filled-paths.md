---
description: Eine Anwendung kann die Kontur eines Pfads zeichnen, indem sie die StrokePath-Funktion aufruft. Sie kann das Innere eines Pfads durch Aufrufen der FillPath-Funktion füllen und den Pfad durch Aufrufen der StrokeAndFillPath-Funktion konturieren und ausfüllen.
ms.assetid: e3e82676-3095-43f0-9fb4-959f925e66c2
title: Umrandete und ausgefüllte Pfade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9660221eb1ef9d7ecf80d1d48ae18c8b234e76e5af3b30dba3323ee6feac3bc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831600"
---
# <a name="outlined-and-filled-paths"></a>Umrandete und ausgefüllte Pfade

Eine Anwendung kann die Kontur eines Pfads zeichnen, indem sie die [**StrokePath-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) aufruft. Sie kann das Innere eines Pfads durch Aufrufen der [**FillPath-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) füllen und den Pfad durch Aufrufen der [**StrokeAndFillPath-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) konturieren und ausfüllen.

Wenn eine Anwendung einen Pfad ausfüllt, verwendet das System den aktuellen Füllmodus des Domänencontrollers. Eine Anwendung kann diesen Modus abrufen, indem sie die [**GetPolyFillMode-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) aufruft, und sie kann einen neuen Füllmodus festlegen, indem sie die [**SetPolyFillMode-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) aufruft. Eine Beschreibung der beiden Füllmodi finden Sie unter [Regionen.](regions.md)

Die folgende Abbildung zeigt den Kreuzabschnitt eines Objekts, das von einer CAD-Anwendung (Computer-Aided Design) mit Pfaden erstellt wurde, die sowohl umrandet als auch ausgefüllt wurden.

![Abbildung der abschnittsübergreifenden Ansicht eines Objekts mit verschiedenen Teilen, die durch unterschiedliche Füllmuster gekennzeichnet sind](images/cspth-01.png)

 

 



