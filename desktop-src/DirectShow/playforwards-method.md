---
description: Die playforward-Methode startet die Wiedergabe von der aktuellen Position mit der angegebenen Geschwindigkeit.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: Playforward-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d49d8d6d80613c4dd5b2b8a374002b37d9baa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746793"
---
# <a name="playforwards-method"></a>Playforward-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Mit der-Methode wird die `PlayForwards` Wiedergabe von der aktuellen Position mit der angegebenen Geschwindigkeit gestartet.

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*ngeschwindigkeit*
</dt> <dd>

Gibt die Geschwindigkeit an, mit der als ganzzahliger Wert abgespielt werden soll. Dieser Wert ist ein Multiplikator – 1.0 ist eine normale Wiedergabegeschwindigkeit. 2,0 ist eine doppelte Geschwindigkeit, 0,5 ist halb Geschwindigkeit usw. Wenn "**nspeed**" nicht gleich 1,0 ist, wird das audiobild stumm geschaltet, und das Teilbild ist deaktiviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Playrückwärts**](playbackwards-method.md)
</dt> </dl>

 

 



