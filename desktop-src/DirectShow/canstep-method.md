---
description: Die CanStep-Methode bestimmt, ob der MPEG-2-Decoder auf dem lokalen System die Frameschritte in einer bestimmten Richtung ausführen kann.
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: CanStep-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ff6ca29443e059cd5ebfbbb553f67cf50b1cb13e1bc8d7199ac6cfae704cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017588"
---
# <a name="canstep-method"></a>CanStep-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `CanStep` -Methode bestimmt, ob der MPEG-2-Decoder auf dem lokalen System die Frameschritte in einer bestimmten Richtung ausführen kann.

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*
</dt> <dd>

Boolescher Wert, der als Flag verwendet wird, um die Richtung (vorwärts oder rückwärts) der Frameschrittfähigkeit des Decoders anzugeben.



| Wert | BESCHREIBUNG                                          |
|-------|------------------------------------------------------|
| true  | Kann der Decoder rückwärts gehen?                           |
| false | Kann der Decoder einen Schritt nach vorn gehen? Dies ist der Standardwert. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den booleschen Wert true zurück, wenn der Decoder in die angegebene Richtung gehen kann, andernfalls FALSE.

## <a name="remarks"></a>Hinweise

Nicht alle MPEG-2-Hardwaredecoder unterstützen die neuen Frameschrittfunktionen in DirectShow® 8.0. Diese Methode fragt den Decoder nach seinen Frameschrittfunktionen ab. Wenn der Decoder die Frameschritte ausführen kann, kann eine Anwendung die [**Step-Methode**](step-method.md) verwenden, um Frames schrittweise zu durchlaufen. Diese Methode gibt immer **TRUE** zurück, wenn ein Softwaredecoder verwendet wird.

 

 



