---
title: Visible-Eigenschaft (Sprechblasen Objekt)
description: Visible-Eigenschaft
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba58993a3328a4c99dbe7da43b43460f6048bf57
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039909"
---
# <a name="visible-property-balloon-object"></a>Visible-Eigenschaft (Sprechblasen Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die sichtbare Einstellung für die Word-Sprechblase für das angegebene Zeichen zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*Agent ***. Zeichen (**"* Merkmal-ID *" * *). Sprechblase. sichtbarer* *  \[  =  *boolescher* Wert\]



| Teil      | BESCHREIBUNG                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der angibt, ob die Wort Sprechblase sichtbar ist.<br/> **True** Die Sprechblase ist sichtbar.<br/> **False** Die Sprechblase ist ausgeblendet.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Gespräch [**oder einen**](speak-method.md) Ansichts Versuch mit einer-Anweisung befolgen, um zu versuchen, die-Eigenschaft der Sprechblase zu ändern, wirkt sich dies möglicherweise nicht auf den sichtbaren Zustand **der Sprechblase** aus, da der **Sprech** -oder [**der Ansichts**](think-method.md) Rückruf in die Warteschlange eingereiht wird Legen Sie diesen Wert daher nur dann fest, wenn sich keine **Sprech** **-oder Aufruf** Anrufe in der Warteschlange des Zeichens befinden.

Wenn Sie versuchen, diese Eigenschaft festzulegen, während das Zeichen gerade gesprochen, bewegt oder gezogen wird, wird die Einstellung der Eigenschaft erst wirksam, wenn der vorherige Vorgang abgeschlossen ist.

Durch [**das Aufrufen**](visible-property.md) der Methoden "sprechen" und " [**Think**](think-method.md) " wird der [**Sprech**](speak-method.md) Blasen automatisch angezeigt Wenn die Eigenschaft für das automatische Ausblenden des Sprechers des Zeichens aktiviert ist, wird die Sprechblase automatisch ausgeblendet, nachdem der Ausgabetext gesprochen wurde. Durch Klicken oder Ziehen eines Zeichens, das derzeit nicht gesprochen wird, wird auch dann automatisch die Sprechblase ausgeblendet, wenn die Einstellung für das automatische ausblenden deaktiviert ist. Sie können die Einstellung für das automatische Ausblenden des Zeichens mithilfe der [**Style**](style-property.md) -Eigenschaft des sprechenden-Objekts ändern.

### <a name="see-also"></a>Weitere Informationen

[**Style-Eigenschaft**](style-property.md)


 

 





