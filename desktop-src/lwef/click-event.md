---
title: Click-Ereignis
description: Click-Ereignis
ms.assetid: 772029d5-97b6-49d8-a989-04f0fc429aca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3956d19e833a3e0a5f71192b2846ef9cb270ad10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388580"
---
# <a name="click-event"></a>Click-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn der Benutzer auf ein Zeichen oder das Zeichen Symbol klickt.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub** *Agent * * * \_ Click* *  **(ByVal** - *Kenn zeichenkennung*, **ByVal-** *Schaltfläche*, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y ** * *)*



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Merkmal-ID* | Gibt die ID des angeklickten Zeichens als Zeichenfolge zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Schaltfläche*      | Gibt eine ganze Zahl zurück, die die Schaltfläche angibt, die zum Auslösen des Ereignisses gedrückt und freigegeben wurde. Das Schaltflächen Argument ist ein Bitfeld mit Bits, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 und 4. Es wird nur einer der Bits festgelegt, der die Schaltfläche angibt, die das Ereignis verursacht hat. Wenn das Zeichen ein Task leisten Symbol enthält und Bit 13 ebenfalls festgelegt ist, ist der Klick auf dem Task leisten Symbol aufgetreten.                                                                                                                                                                      |
| *Shift*       | Gibt eine ganze Zahl zurück, die dem Zustand der UMSCHALTTASTE, der STRG-Taste und der Alt-Taste entspricht, wenn die im Schaltflächen Argument angegebene Schaltfläche gedrückt oder freigegeben wird. Ein Bit ist festgelegt, wenn der Schlüssel nicht angezeigt wird. Beim Shift-Argument handelt es sich um ein Bitfeld mit den geringsten signifikanten Bits, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 und 4. Das Shift-Argument gibt den Zustand dieser Schlüssel an. Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden. Wenn z. b. STRG und Alt gedrückt wurden, ist der Wert von Shift 6. |
| *X, Y*         | Gibt eine ganze Zahl zurück, die die aktuelle Position des Mauszeigers angibt. Die X-und Y-Werte werden in Relation zur oberen linken Ecke des Bildschirms immer in Pixel ausgedrückt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird nur an den Eingabe aktiven Client eines Zeichens gesendet. Wenn der Benutzer auf ein Zeichen oder das zugehörige Task leisten Symbol ohne Eingabe aktiven Client klickt, sendet der Server das Ereignis an seinen aktiven Client. Wenn das Zeichen sichtbar ist ([**sichtbar**](visible-property.md)  =  **true**), legt die Aktion des Benutzers auch den letzten Eingabe aktiven Client des Zeichens als aktuellen Eingabe aktiven Client fest, sendet das [**activateinput**](activateinput-event.md) -Ereignis an diesen Client und sendet dann das **Click** -Ereignis. Wenn das Zeichen ausgeblendet ist (**sichtbar**  =  **false**) und der Benutzer mithilfe von Schaltfläche 1 auf das Task leisten Symbol des Zeichens klickt, wird das Zeichen ebenfalls automatisch angezeigt.

> [!Note]  
> Wenn Sie auf ein Zeichen klicken, werden nicht alle anderen Zeichen Ausgaben (alle Zeichen) deaktiviert. Wenn Sie jedoch die Abhör Taste drücken, wird die Ausgabe des aktiven Zeichens geleert, und das [**requestcomplete**](requestcomplete-event.md) -Ereignis wird ausgelöst, wobei eine Anforderung übergeben wird [. Status](status-property.md) , der angibt, dass die Warteschlange des Clients unterbrochen wurde.

 

 

 




