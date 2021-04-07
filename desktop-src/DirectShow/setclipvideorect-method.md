---
description: Die setclipvideorect-Methode zoomt die Videoanzeige in das angegebene unter Rechteck.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: Setclipvideorect-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7f4b003ef20b82f1e783ebf074e8bbd5cc793
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746296"
---
# <a name="setclipvideorect-method"></a>Setclipvideorect-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Mit der- `SetClipVideoRect` Methode wird die Videoanzeige in das angegebene unter Rechteck vergrößert.

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*orect*
</dt> <dd>

Gibt ein [dvdrect](dvdrect-object.md) -Objekt an, das das Clippingrechteck enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Beim Festlegen eines neuen clippingrechtecks vergrößert das Objekt den Bereich, sodass er in die Gesamt Anzeige Dimensionen der Anwendung passt. Dadurch wird die Auswirkung auf einen bestimmten Bereich des Bildschirms vergrößert. Um das Rechteck anzugeben, erstellen Sie ein neues [dvdrect](dvdrect-object.md) -Objekt, und füllen Sie seine Eigenschaften aus.

Das häufigste Rechteck für die Videoanzeige ist 720 x 540.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getclipvideorect**](getclipvideorect-method.md)
</dt> </dl>

 

 



