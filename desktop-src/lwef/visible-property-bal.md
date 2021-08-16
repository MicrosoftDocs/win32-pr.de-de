---
title: Visible-Eigenschaft (Balloon-Objekt)
description: Erfahren Sie mehr über die Visible-Eigenschaft des Balloon-Objekts, das die sichtbare Einstellung für den Wortsprechblasen für das angegebene Zeichen zurückgibt oder festlegt.
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101d454f90e01ebcf31619b935d1b90512648baf33a11883b6b971c3178fb871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975480"
---
# <a name="visible-property-balloon-object"></a>Visible-Eigenschaft (Balloon-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die sichtbare Einstellung für die Wortsprechblase für das angegebene Zeichen zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Balloon.Visible* *  \[  =  *boolean*\]



| Teil      | BESCHREIBUNG                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der angibt, ob die Wortsprechblase sichtbar ist.<br/> **True** Die Sprechblase ist sichtbar.<br/> **False** Die Sprechblase ist ausgeblendet.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie einem [**Speak-**](speak-method.md) oder [**Think-Aufruf**](think-method.md) mit einer -Anweisung folgen, um zu versuchen, die -Eigenschaft des Sprechblasens zu ändern, wirkt sich dies möglicherweise nicht auf den Visible-Zustand des Balloons aus, da der **Speak-** oder **Think-Aufruf** in die Warteschlange eingereiht wird, der Aufruf, der den sichtbaren Zustand des Balloons festlegt, jedoch nicht. Legen Sie diesen Wert daher nur fest, wenn sich keine **Speak-** oder **Think-Aufrufe** in der Warteschlange des Zeichens befinden.

Wenn Sie versuchen, diese Eigenschaft festzulegen, während das Zeichen spricht, bewegt oder gezogen wird, wird die Eigenschafteneinstellung erst wirksam, wenn der vorherige Vorgang abgeschlossen ist.

Wenn Sie die [**Methoden Speak**](speak-method.md) und [**Think**](think-method.md) aufrufen, wird der Sprechblasen automatisch sichtbar, und die [**Visible-Eigenschaft**](visible-property.md) wird auf **True** festgelegt. Wenn die AutoHide-Sprechblaseneigenschaft des Zeichens aktiviert ist, wird die Sprechblase automatisch ausgeblendet, nachdem der Ausgabetext gesprochen wurde. Durch Klicken oder Ziehen eines Zeichens, das derzeit nicht spricht, wird der Sprechblasen automatisch ausgeblendet, auch wenn die AutoHide-Einstellung deaktiviert ist. Sie können die AutoHide-Einstellung des Zeichens mithilfe der [**Style-Eigenschaft**](style-property.md) des Balloons ändern.

### <a name="see-also"></a>Weitere Informationen

[**Style-Eigenschaft**](style-property.md)


 

 





