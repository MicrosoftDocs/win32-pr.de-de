---
title: ShowDefaultCharacterProperties-Methode
description: ShowDefaultCharacterProperties-Methode
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d19f92f555038fe4c13c7a752d49bf35a04b70964f6110d881976af3e72a8c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746306"
---
# <a name="showdefaultcharacterproperties-method"></a>ShowDefaultCharacterProperties-Methode

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Zeigt die Eigenschaften des Standardzeichens an.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent**. ShowDefaultCharacterProperties* *  \[ *X* , *Y*\]



| Teil | Beschreibung                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *X*  | Optional. Ein kurzer ganzzahliger Wert, der die horizontale Bildschirmkoordinate (*X* ) angibt, um das Fenster anzuzeigen. Diese Koordinate muss in Pixel angegeben werden. |
| *J*  | Optional. Ein kurzer ganzzahliger Wert, der die vertikale Bildschirmkoordinate (*Y*) angibt, um das Fenster anzuzeigen. Diese Koordinate muss in Pixel angegeben werden.    |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beim Aufrufen dieser Methode wird das Standardzeicheneigenschaftenfenster (nicht das Microsoft Agent-Eigenschaftenblatt) angezeigt. Wenn Sie die X- und Y-Koordinaten nicht angeben, wird das Fenster an der letzten Position angezeigt, an der es angezeigt wurde.

## <a name="see-also"></a>Weitere Informationen

[**DefaultCharacterChange-Ereignis**](defaultcharacterchange-event.md)


 

 




