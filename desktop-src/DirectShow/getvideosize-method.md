---
description: Die getvideosize-Methode ruft die nativen Video Dimensionen ab.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: Getvideosize-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b96d01c3f22eaae78a442f3496f3c7c7416eac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340098"
---
# <a name="getvideosize-method"></a>Getvideosize-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `GetVideoSize` Methode ruft die nativen Video Dimensionen ab.

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a>Rückgabewert

Gibt ein [dvdrect](dvdrect-object.md) -Objekt zurück, das vier Lese-/Schreibeigenschaften enthält: (oben links) x; (oben links) y, Breite und Höhe. Die **x** -und **y** -Eigenschaften werden auf 0 (null) festgelegt, und die anderen beiden Eigenschaften reflektieren die Breite und Höhe des Video Rechtecks, das auf der Festplatte erstellt wurde

 

 



