---
description: Das Beispiel in Pinseln verwendet Bereiche zum Simulieren eines &\# 0034; vergrößert&\# 0034; Ansicht einer 8-Bit-Monochrom-Bitmap mit 8 Pixeln.
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: Verwenden von Regionen zum Durchführen von Treffer Tests
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb50ca1f837213b85619af381b86c2bd76efcbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215647"
---
# <a name="using-regions-to-perform-hit-testing"></a>Verwenden von Regionen zum Durchführen von Treffer Tests

Im Beispiel in [Pinseln](brushes.md) werden Bereiche verwendet, um eine "Zoomansicht" einer 8-Bit-monochrome Bitmap zu simulieren. Durch Klicken auf die Pixel in dieser Bitmap erstellt der Benutzer einen benutzerdefinierten Pinsel, der für Zeichnungsvorgänge geeignet ist. Das Beispiel zeigt, wie die [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) -Funktion zum Ausführen von Treffer Tests und die [**invertrgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) -Funktion verwendet wird, um die Farben in einem Bereich umzukehren.

 

 



