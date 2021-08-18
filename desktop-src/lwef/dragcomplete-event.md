---
title: DragComplete-Ereignis
description: DragComplete-Ereignis
ms.assetid: b48e7097-9d9d-4eab-9dfc-68dbc9793382
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df5ec931a8d5f303dbc1eff5c2f97c018486c4b2fa7326de3e70fbf47a949aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976670"
---
# <a name="dragcomplete-event"></a>DragComplete-Ereignis

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn der Benutzer das Ziehen eines Zeichens abgeschlossen hat.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Sub-Agent** \_ DragComplete* *  **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y**)**



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Gibt die ID des gezogenen Zeichens als Zeichenfolge zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Schaltfläche*      | Gibt eine ganze Zahl zurück, die die Schaltfläche identifiziert, die gedrückt und freigegeben wurde, um das Ereignis zu verursachen. Das Button-Argument ist ein Bitfeld mit Bits, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entspricht. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Es wird nur eines der Bits festgelegt, was die Schaltfläche angibt, die das Ereignis verursacht hat.                                                                                                                                                                                                                                                                                |
| *Shift*       | Gibt eine ganze Zahl zurück, die dem Zustand der UMSCHALT-, STRG- und ALT-Tasten entspricht, wenn die im Schaltflächenargument angegebene Schaltfläche gedrückt oder losgelassen wird. Ein Bit wird festgelegt, wenn der Schlüssel aus ist. Das Shift-Argument ist ein Bitfeld mit den am wenigsten signifikanten Bits, die der UMSCHALTTASTE (Bit 0), der STRG-TASTE (Bit 1) und der ALT-Taste (Bit 2) entspricht. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Das Shift-Argument gibt den Zustand dieser Schlüssel an. Einige, alle oder keine der Bits können festgelegt werden, was darauf hinweist, dass einige, alle oder keine der Tasten gedrückt werden. Wenn z. B. sowohl STRG als auch ALT gedrückt werden, wäre der Wert der Verschiebung 6. |
| *X,Y*         | Gibt eine ganze Zahl zurück, die die aktuelle Position des Mauszeigers angibt. Die X- und Y-Werte werden immer in Pixeln relativ zur oberen linken Ecke des Bildschirms ausgedrückt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Dieses Ereignis wird nur an den eingabeaktiven Client eines Zeichens gesendet. Wenn der Benutzer ein Zeichen ohne eingabeaktiven Client zieht, legt der Server seinen letzten eingabeaktiven Client als aktuellen eingabeaktiven Client fest, sendet das [**ActivateInput-Ereignis**](activateinput-event.md) an diesen Client und sendet dann die [**DragStart-**](dragstart-event.md) und **DragComplete-Ereignisse.**

### <a name="see-also"></a>Weitere Informationen

[**DragStart-Ereignis**](dragstart-event.md)


 

 




