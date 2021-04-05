---
title: Showdefaultcharakteriproperties-Methode
description: Showdefaultcharakteriproperties-Methode
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f055b2ca0f00e0a13c24ec95dc82509ae9c45b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709912"
---
# <a name="showdefaultcharacterproperties-method"></a>Showdefaultcharakteriproperties-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Zeigt die Eigenschaften des Standard Zeichens an.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent * * *. Showdefaultcharacters-Eigenschaften* *  \[ *X* , *Y*\]



| Teil | BESCHREIBUNG                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *X*  | Dies ist optional. Ein kurzer ganzzahliger Wert, der die horizontale (*X* ) Bildschirm Koordinate angibt, um das Fenster anzuzeigen. Diese Koordinate muss in Pixel angegeben werden. |
| *J*  | Dies ist optional. Ein kurzer *ganzzahliger* Wert, der die vertikale Bildschirm Koordinate (Y) angibt, um das Fenster anzuzeigen. Diese Koordinate muss in Pixel angegeben werden.    |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beim Aufrufen dieser Methode wird das standardmäßige Zeichen Eigenschaften Fenster (nicht das Eigenschaften Blatt "Microsoft-Agent") angezeigt. Wenn Sie die X-und Y-Koordinaten nicht angeben, wird das Fenster an der letzten Position angezeigt, an der es angezeigt wurde.

## <a name="see-also"></a>Weitere Informationen

[**Defaultcharacters-Änderungs Ereignis**](defaultcharacterchange-event.md)


 

 




