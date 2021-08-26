---
description: Die SetClipVideoRect-Methode zoomt die Videoanzeige auf das angegebene Unterobjekt.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: SetClipVideoRect-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7741a2604ed1c2896b105295020893e23b447e3fa6f6ab7c53def92aa508c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078870"
---
# <a name="setclipvideorect-method"></a>SetClipVideoRect-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `SetClipVideoRect` -Methode zoomt die Videoanzeige auf das angegebene Unterobjekt.

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*
</dt> <dd>

Gibt ein [DVDRect-Objekt](dvdrect-object.md) an, das das Clippingrechteck enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Wenn Sie ein neues Clippingrechteck festlegen, vergrößert das Objekt diesen Bereich so, dass er in die Gesamtanzeigedimensionen der Anwendung passt. Dadurch wird der Effekt vergrößert, der in einem bestimmten Bereich des Bildschirms vergrößert wird. Um das Rechteck anzugeben, erstellen Sie ein neues [DVDRect-Objekt,](dvdrect-object.md) und füllen Sie dessen Eigenschaften aus.

Das gängigste Rechteck für die Videoanzeige ist 720 x 540.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetClipVideoRect**](getclipvideorect-method.md)
</dt> </dl>

 

 



