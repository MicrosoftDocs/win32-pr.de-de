---
description: Die GetVideoSize-Methode ruft die nativen Videodimensionen ab.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: GetVideoSize-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21746242211357e9e58e825d8e217799953dd569e91765acabe11fc2252d17c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536590"
---
# <a name="getvideosize-method"></a>GetVideoSize-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `GetVideoSize` -Methode ruft die nativen Videodimensionen ab.

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a>Rückgabewert

Gibt ein [DVDRect-Objekt](dvdrect-object.md) zurück, das vier Lese-/Schreibeigenschaften enthält: (oben links) x; (oben links) y, Breite und Höhe. Die **x-** und **y-Eigenschaften** werden auf 0 (null) festgelegt, und die anderen beiden Eigenschaften spiegeln die Breite und Höhe des Videorechtecks wider, wie auf dem Datenträger erstellt.

 

 



