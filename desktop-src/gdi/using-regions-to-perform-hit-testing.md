---
description: Im Beispiel in Brushes werden Bereiche verwendet, um eine &\# 0034;zoomed&\# 0034; view of an 8- by 8-pixel monotonee Bitmap zu simulieren.
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: Verwenden von Regionen zum Ausführen von Treffertests
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d553eeaf37b954d0ec9d0b8897df98cf1a513d7ca7212ca82bc376afe1fc7163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558120"
---
# <a name="using-regions-to-perform-hit-testing"></a>Verwenden von Regionen zum Ausführen von Treffertests

Im Beispiel in [Brushes werden](brushes.md) Bereiche verwendet, um eine "vergrößerte" Ansicht einer 8- mal 8-Pixel-monofarbigen Bitmap zu simulieren. Durch Klicken auf die Pixel in dieser Bitmap erstellt der Benutzer einen benutzerdefinierten Pinsel, der für Zeichnungsvorgänge geeignet ist. Das Beispiel zeigt, wie Sie die [**PtInRegion-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) verwenden, um Treffertests durchzuführen, und die [**InvertRgn-Funktion,**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) um die Farben in einem Bereich rückgängig zu machen.

 

 



