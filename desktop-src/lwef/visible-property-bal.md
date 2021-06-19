---
title: Visible-Eigenschaft (Balloon-Objekt)
description: Erfahren Sie mehr über die Visible-Eigenschaft des Balloon-Objekts, die die sichtbare Einstellung für das Wort balloon für das angegebene Zeichen zurückgibt oder legt.
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac587fa649f2a8ccb5ea83ddc077050a8548d2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396325"
---
# <a name="visible-property-balloon-object"></a>Visible-Eigenschaft (Balloon-Objekt)

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die sichtbare Einstellung für das Wort balloon für das angegebene Zeichen zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Balloon.Visible* *  \[  =  *boolean*\]



| Teil      | Beschreibung                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der an gibt, ob das Wort Balloon sichtbar ist.<br/> **True** Die Sprechblase ist sichtbar.<br/> **False** Die Sprechblase ist ausgeblendet.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie [](speak-method.md) einem Speak- oder [**Think-Aufruf**](think-method.md) mit einer -Anweisung folgen, um zu versuchen, die -Eigenschaft des Sprechblasens zu ändern, wirkt sich dies möglicherweise nicht auf den Sichtbar-Zustand des Balloons aus, da der **Speak-** oder **Think-Aufruf** in die Warteschlange gestellt wird, aber der Aufruf, der den sichtbaren Zustand des Balloons ansteuert, nicht. Legen Sie diesen Wert daher nur fest, wenn **sich keine Speak-** oder **Think-Aufrufe** in der Warteschlange des Zeichens befinden.

Wenn Sie versuchen, diese Eigenschaft während des Sprechens, Verschiebens oder Ziehens des Zeichens zu setzen, wird die Eigenschafteneinstellung erst wirksam, wenn der vorherige Vorgang abgeschlossen ist.

Durch Aufrufen [**der Speak-**](speak-method.md) [**und Think-Methoden**](think-method.md) wird der Balloon automatisch sichtbar, und die [**Visible-Eigenschaft**](visible-property.md) wird auf **True (Wahr) festlegen.** Wenn die AutoHide-Eigenschaft des Zeichens aktiviert ist, wird die Sprechblase automatisch ausgeblendet, nachdem der Ausgabetext gesprochen wurde. Wenn Sie auf ein Zeichen klicken oder ziehen, das derzeit nicht spricht, wird der Balloon auch dann automatisch ausblendet, wenn die Einstellung AutoHide deaktiviert ist. Sie können die Einstellung AutoHide des Zeichens ändern, indem Sie die [**Style-Eigenschaft**](style-property.md) des Balloons verwenden.

### <a name="see-also"></a>Weitere Informationen

[**Style-Eigenschaft**](style-property.md)


 

 





