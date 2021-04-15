---
description: Die Play-Methode gibt den aktuellen DVD-Titel wieder.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Play-Methode (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62323c9c86be476a35977dadf554bbfca3bca91
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521296"
---
# <a name="play-method-directshow"></a>Play-Methode (DirectShow)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `Play` Methode gibt den aktuellen DVD-Titel wieder.

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn die Wiedergabe angehalten oder beendet wird und [**enableresetonstopp**](enableresetonstop-property.md) den Wert true aufweist, wird die Wiedergabe mit normaler Geschwindigkeit am aktuellen Speicherort durch den Aufruf von **Play** wieder aufgenommen. Wenn die Wiedergabe angehalten und **enableresetonend** auf false festgelegt ist, wird durch das Aufrufen von **Play** die Festplatte am Anfang des ersten Titels abgespielt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Fortsetzen**](resume-method.md)
</dt> </dl>

 

 



