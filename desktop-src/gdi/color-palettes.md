---
description: Eine Farbpalette ist ein Array, das Farbwerte enthält, die die Farben identifizieren, die derzeit auf dem Ausgabegerät angezeigt oder gezeichnet werden können.
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: Farbpaletten (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81079ac94b40de98bc1c53098a8b9d1654f90d0d855397ac38d11311e9741e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761957"
---
# <a name="color-palettes-windows-gdi"></a>Farbpaletten (Windows GDI)

Eine Farbpalette ist ein Array, das Farbwerte enthält, die die Farben identifizieren, die derzeit auf dem Ausgabegerät angezeigt oder gezeichnet werden können. Farbpaletten werden von Geräten verwendet, die viele Farben generieren können, aber nur eine Teilmenge dieser Farben zu einem bestimmten Zeitpunkt anzeigen oder zeichnen können. Für solche Geräte verwaltet das System eine *Systempalette,* um die aktuellen Farben des Geräts nachzuverfolgen und zu verwalten. Anwendungen haben keinen direkten Zugriff auf die Systempalette. Stattdessen ordnet das System jedem Gerätekontext eine Standardpalette zu. Anwendungen können die Farben in der Standardpalette verwenden oder eigene Farben definieren, indem *sie logische Paletten* erstellen und sie einzelnen Gerätekontexten zuordnen.

Eine Anwendung kann bestimmen, ob ein Gerät Farbpaletten unterstützt, indem sie \_ im RASTERCAPS-Wert, der von der [**GetDeviceCaps-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) zurückgegeben wird, nach dem RC PALETTE-Bit sucht.

 

 



