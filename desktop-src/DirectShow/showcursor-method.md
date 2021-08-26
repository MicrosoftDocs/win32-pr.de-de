---
description: Die ShowCursor-Methode macht den Cursor sichtbar, wenn sich das MSWebDVD-Objekt im Vollbildmodus befindet.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: ShowCursor-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3013392a5dcea2b3c4c9af8ee94d54c540814b5f4221563429ee7c837dcdddd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050520"
---
# <a name="showcursor-method"></a>ShowCursor-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `ShowCursor` -Methode macht den Cursor sichtbar, wenn sich das **MSWebDVD-Objekt** im Vollbildmodus befindet.

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

## <a name="remarks"></a>Hinweise

Wenn die DVD-Anzeige in den Vollbildmodus wechselt, verschwindet der Cursor innerhalb von 3 bis 5 Sekunden. Verwenden Sie diese Methode, um den Cursor wieder sichtbar zu machen, wenn die Steuerelementschaltflächen Ihrer Anwendung im Vollbildmodus sichtbar sind.

 

 



