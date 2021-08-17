---
title: DragStart-Ereignis
description: DragStart-Ereignis
ms.assetid: fef0ae05-1958-45c6-8260-107c47b5fa92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 835ffc22e23643d306b361977a4bbe8b04e6481f8a577c3c2cef959b4be46ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963090"
---
# <a name="dragstart-event"></a>DragStart-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn der Benutzer mit dem Ziehen eines Zeichens beginnt.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Sub-Agent** \_ DragStart* *  **(ByVal** *CharacterID*, **(ByVal-Schaltfläche,**  **(ByVal-Umschalt,**  **(ByVal** *X*, **(ByVal** *Y))**



| Teil          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Gibt die ID des geklickten Zeichens als Zeichenfolge zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Schaltfläche*      | Gibt eine ganze Zahl zurück, die die Schaltfläche identifiziert, die gedrückt und losgelassen wurde, um das Ereignis zu verursachen. Das Schaltflächenargument ist ein Bitfeld mit Bits, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Es wird nur eines der Bits festgelegt, das die Schaltfläche angibt, die das Ereignis verursacht hat.                                                                                                                                                                                                                                                                                |
| *Shift*       | Gibt eine ganze Zahl zurück, die dem Zustand der UMSCHALT-, STRG- und ALT-Taste entspricht, wenn die im Schaltflächenargument angegebene Schaltfläche gedrückt oder losgelassen wird. Wenn der Schlüssel ausgeschaltet ist, wird ein Bit festgelegt. Das Shift-Argument ist ein Bitfeld mit den am wenigsten signifikanten Bits, die der UMSCHALTTASTE (Bit 0), der STRG-Taste (Bit 1) und der ALT-Taste (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Das Shift-Argument gibt den Zustand dieser Schlüssel an. Einige, alle oder keine der Bits können festgelegt werden, was darauf hinweist, dass einige, alle oder keine der Tasten gedrückt werden. Wenn z. B. sowohl STRG als auch ALT gedrückt würden, wäre der Wert von SHIFT 6. |
| *X,Y*         | Gibt eine ganze Zahl zurück, die die aktuelle Position des Mauszeigers angibt. Die X- und Y-Werte werden immer in Pixel ausgedrückt, relativ zur oberen linken Ecke des Bildschirms.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Dieses Ereignis wird nur an den eingabeaktiven Client eines Zeichens gesendet. Wenn der Benutzer ein Zeichen ohne eingabeaktiven Client zieht, legt der Server seinen letzten eingabeaktiven Client als aktuellen eingabeaktiven Client fest, sendet das [**ActivateInput-Ereignis**](activateinput-event.md) an diesen Client und sendet dann das **DragStart-Ereignis.**

### <a name="see-also"></a>Weitere Informationen

[**DragComplete-Ereignis**](dragcomplete-event.md)


 

 




