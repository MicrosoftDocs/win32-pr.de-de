---
description: Eine Farbpalette ist ein Array, das Farb Werte enthält, die die Farben identifizieren, die derzeit auf dem Ausgabegerät angezeigt oder gezeichnet werden können.
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: Farbpaletten (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6da2aab08d2b482eb678e8541ec166156b78f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130812"
---
# <a name="color-palettes-windows-gdi"></a>Farbpaletten (Windows GDI)

Eine Farbpalette ist ein Array, das Farb Werte enthält, die die Farben identifizieren, die derzeit auf dem Ausgabegerät angezeigt oder gezeichnet werden können. Farbpaletten werden von Geräten verwendet, die viele Farben erzeugen können, jedoch nur eine Teilmenge dieser zu einem bestimmten Zeitpunkt anzeigen oder zeichnen können. Bei solchen Geräten verwaltet das System eine *Systempalette* , um die aktuellen Farben des Geräts zu verfolgen und zu verwalten. Anwendungen haben keinen direkten Zugriff auf die Systempalette. Stattdessen ordnet das System den einzelnen Geräte Kontexten eine Standardpalette zu. Anwendungen können die Farben in der Standardpalette verwenden oder Ihre eigenen Farben definieren, indem Sie *logische Paletten* erstellen und Sie einzelnen Geräte Kontexten zuordnen.

Eine Anwendung kann ermitteln, ob ein Gerät Farbpaletten unterstützt, indem das RC- \_ palettenbit im RasterCaps-Wert überprüft wird, der von der [**getdebug**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion zurückgegeben wird.

 

 



