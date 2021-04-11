---
description: Die canstep-Methode bestimmt, ob der MPEG-2-Decoder im lokalen System einen Frame Schritt in einer angegebenen Richtung ausführen kann.
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: Canstep-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506e7436e5ec79947aceeca69891e52074cf2ea7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041157"
---
# <a name="canstep-method"></a>Canstep-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `CanStep` -Methode bestimmt, ob der MPEG-2-Decoder im lokalen System Frame-Step in einer angegebenen Richtung ausführen kann.

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bdirection*
</dt> <dd>

Boolescher Wert, der als Flag verwendet wird, um die Richtung (vorwärts oder rückwärts) der Rahmen Schritt Fähigkeit des Decoders anzugeben.



| Wert | BESCHREIBUNG                                          |
|-------|------------------------------------------------------|
| true  | Kann der Decoder einen Schritt rückwärts ausführen?                           |
| false | Kann der Decoder einen Schritt vorwärts ausführen? Dies ist der Standardwert. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den booleschen Wert true zurück, wenn der Decoder in die angegebene Richtung wechseln kann, andernfalls false.

## <a name="remarks"></a>Bemerkungen

Nicht alle Hardware-MPEG-2-Decoder unterstützen die neuen Frame Step-Funktionen in DirectShow® 8,0. Diese Methode fragt den Decoder nach seinen Frame-Step-Funktionen ab. Wenn der Decoder Frame-Stepping ausführen kann, kann eine Anwendung die [**Step**](step-method.md) -Methode verwenden, um Frames schrittweise zu durchlaufen. Diese Methode gibt immer **true** zurück, wenn ein Software Decoder verwendet wird.

 

 



