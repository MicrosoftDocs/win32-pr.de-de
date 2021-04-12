---
title: DblClick-Ereignis
description: DblClick-Ereignis
ms.assetid: 81ed5396-a2dc-49fe-820f-61ca0935fe85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b900b8a8b79345c50749a4355deeb05fdc1220
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310580"
---
# <a name="dblclick-event"></a>DblClick-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn der Benutzer auf ein Zeichen doppelklickt.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub** *Agent * * * \_ DblClick* *  **(ByVal** - *Kenn zeichenkennung*, **ByVal-** *Schaltfläche*, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y ** * *)*



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Merkmal-ID* | Gibt die ID des doppelt angeklickten Zeichens als Zeichenfolge zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| *Schaltfläche*      | Gibt eine ganze Zahl zurück, die die Schaltfläche angibt, die zum Auslösen des Ereignisses gedrückt und freigegeben wurde. Das Schaltflächen Argument ist ein Bitfeld mit Bits, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 und 4. Es wird nur einer der Bits festgelegt, der die Schaltfläche angibt, die das Ereignis verursacht hat. Wenn das Zeichen ein Symbol für die Taskleiste enthält und Bit13 ebenfalls festgelegt ist, ist der Klick auf dem Task leisten Symbol aufgetreten.                                                                                                                                                                       |
| *Shift*       | Gibt eine ganze Zahl zurück, die dem Zustand der UMSCHALTTASTE, der STRG-Taste und der Alt-Taste entspricht, wenn die im Schaltflächen Argument angegebene Schaltfläche gedrückt oder freigegeben wird. Ein Bit ist festgelegt, wenn der Schlüssel nicht angezeigt wird. Beim Shift-Argument handelt es sich um ein Bitfeld mit den geringsten signifikanten Bits, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 und 4. Das Shift-Argument gibt den Zustand dieser Schlüssel an. Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden. Wenn z. b. STRG und Alt gedrückt wurden, ist der Wert von Shift 6. |
| *X, Y*         | Gibt eine ganze Zahl zurück, die die aktuelle Position des Mauszeigers angibt. Die X-und Y-Werte werden in Relation zur oberen linken Ecke des Bildschirms immer in Pixel ausgedrückt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird nur an den Eingabe aktiven Client eines Zeichens gesendet. Wenn der Benutzer auf ein Zeichen oder ein Task leisten Symbol ohne Eingabe aktiven Client doppelklickt, sendet der Server das Ereignis an den letzten Eingabe aktiven Client. Wenn das Zeichen sichtbar ([sichtbar](visible-property.md)  =  **true**) ist, wird der aktive Client auch als aktueller Eingabe aktiver Client festgelegt, das [**activateinput**](activateinput-event.md) -Ereignis an den Client gesendet und dann das **DblClick** -Ereignis gesendet. Wenn das Zeichen ausgeblendet ist (Visible = **false**) und der Benutzer mit Schaltfläche 1 auf das Task leisten Symbol des Zeichens doppelklickt, wird auch automatisch das Zeichen angezeigt.

 

 




