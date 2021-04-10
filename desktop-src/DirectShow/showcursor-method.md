---
description: Die ShowCursor-Methode macht den Cursor sichtbar, wenn sich das mswebdvd-Objekt im Vollbildmodus befindet.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: ShowCursor-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917c1d0d2724259fc19baf72ab6b3844cddc3419
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860315"
---
# <a name="showcursor-method"></a>ShowCursor-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `ShowCursor` Methode macht den Cursor sichtbar, wenn sich das **mswebdvd** -Objekt im Vollbildmodus befindet.

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*
</dt> <dd>

Gibt an, ob der Cursor als boolescher Wert angezeigt werden soll.



| Wert | BESCHREIBUNG            |
|-------|------------------------|
| true  | Cursor wird angezeigt.        |
| false | Cursor nicht anzeigen |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn die DVD-Anzeige in den Vollbildmodus wechselt, verschwindet der Cursor innerhalb von 3 bis 5 Sekunden. Verwenden Sie diese Methode, um den Cursor wieder sichtbar zu machen, wenn die Steuerelemente der Anwendung im Vollbildmodus sichtbar sind.

 

 



