---
title: Click-Ereignis
description: Click-Ereignis
ms.assetid: 772029d5-97b6-49d8-a989-04f0fc429aca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc10726c91612a6d43c4b7f8ceb0509fc347904f1328c9b99a3ec05d8e2eb0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480186"
---
# <a name="click-event"></a>Click-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn der Benutzer auf ein Zeichen oder das Symbol des Zeichens klickt.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Sub-Agent: \_ Klicken Sie auf* *  **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *SHIFT*, **ByVal** *X*, **ByVal** *Y))**



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Gibt die ID des geklickten Zeichens als Zeichenfolge zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Schaltfläche*      | Gibt eine ganze Zahl zurück, die die Schaltfläche identifiziert, die gedrückt und losgelassen wurde, um das Ereignis zu verursachen. Das Schaltflächenargument ist ein Bitfeld mit Bits, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Es wird nur eines der Bits festgelegt, das die Schaltfläche angibt, die das Ereignis verursacht hat. Wenn das Zeichen ein Taskleistensymbol enthält und bit 13 ebenfalls festgelegt ist, ist der Klick auf das Taskleistensymbol erfolgt.                                                                                                                                                                      |
| *Shift*       | Gibt eine ganze Zahl zurück, die dem Zustand der UMSCHALT-, STRG- und ALT-Taste entspricht, wenn die im Schaltflächenargument angegebene Schaltfläche gedrückt oder losgelassen wird. Wenn der Schlüssel ausgeschaltet ist, wird ein Bit festgelegt. Das Shift-Argument ist ein Bitfeld mit den am wenigsten signifikanten Bits, die der UMSCHALTTASTE (Bit 0), der STRG-Taste (Bit 1) und der ALT-Taste (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Das Shift-Argument gibt den Zustand dieser Schlüssel an. Einige, alle oder keine der Bits können festgelegt werden, was darauf hinweist, dass einige, alle oder keine der Tasten gedrückt werden. Wenn z. B. sowohl STRG als auch ALT gedrückt würden, wäre der Wert von SHIFT 6. |
| *X,Y*         | Gibt eine ganze Zahl zurück, die die aktuelle Position des Mauszeigers angibt. Die X- und Y-Werte werden immer in Pixel ausgedrückt, relativ zur oberen linken Ecke des Bildschirms.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Dieses Ereignis wird nur an den eingabeaktiven Client eines Zeichens gesendet. Wenn der Benutzer auf ein Zeichen oder sein Taskleistensymbol ohne eingabeaktiven Client klickt, sendet der Server das Ereignis an seinen aktiven Client. Wenn das Zeichen sichtbar ist ([**Visible**](visible-property.md)  =  **True**), legt die Aktion des Benutzers auch den letzten eingabeaktiven Client des Zeichens als aktuellen eingabeaktiven Client fest, sendet das [**ActivateInput-Ereignis**](activateinput-event.md) an diesen Client und sendet dann das **Click-Ereignis.** Wenn das Zeichen ausgeblendet ist **(Visible**  =  **False**), und der Benutzer mithilfe von Schaltfläche 1 auf das Taskleistensymbol des Zeichens klickt, wird das Zeichen ebenfalls automatisch angezeigt.

> [!Note]  
> Durch Klicken auf ein Zeichen werden nicht alle anderen Zeichenausgaben (alle Zeichen) deaktiviert. Wenn Sie jedoch die Taste Lauschen drücken, wird die Ausgabe des eingabeaktiven Zeichens geleert, und das [**RequestComplete-Ereignis**](requestcomplete-event.md) wird ausgelöst. Dabei wird ein [Request.Status](status-property.md) übergeben, der angibt, dass die Warteschlange des Clients unterbrochen wurde.

 

 

 




