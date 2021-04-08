---
description: In der Tabelle ControlCondition kann ein Autor spezielle Aktionen angeben, die auf die Steuerelemente basierend auf dem Ergebnis einer Bedingungs Anweisung angewendet werden sollen. Wenn Sie diese Tabelle verwenden, könnte der Autor z. b. ein Steuerelement auf der Grundlage der VersionNT-Eigenschaft ausblenden.
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: ControlCondition-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 671dcdee6e2ed1067c51a04084693c276b8db2d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960157"
---
# <a name="controlcondition-table"></a>ControlCondition-Tabelle

In der Tabelle ControlCondition kann ein Autor spezielle Aktionen angeben, die auf die Steuerelemente basierend auf dem Ergebnis einer Bedingungs Anweisung angewendet werden sollen. Wenn Sie diese Tabelle verwenden, könnte der Autor z. b. ein Steuerelement auf der Grundlage der [**VersionNT**](versionnt.md) -Eigenschaft ausblenden.

Die Tabelle "ControlCondition" enthält die folgenden Spalten.



| Spalte    | Typ                         | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Dialog\_  | [Bezeichner](identifier.md) | J   | N        |
| Steuerelement\_ | [Bezeichner](identifier.md) | J   | N        |
| Aktion    | [Text](text.md)             | J   | N        |
| Bedingung | [Condition](condition.md)   | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_
</dt> <dd>

Ein externer Schlüssel für die erste Spalte der [Dialog Feld Tabelle](dialog-table.md). Durch kombinieren dieses Felds mit dem Steuerelement Feld wird ein eindeutiges \_ Steuerelement identifiziert.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Steuerelement\_
</dt> <dd>

Ein externer Schlüssel für die zweite Spalte der [Steuerelement Tabelle](control-table.md). Durch kombinieren dieses Felds wird das Dialog \_ Feld mit einem eindeutigen Steuerelement identifiziert.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel
</dt> <dd>

Die Aktion, die für das-Steuerelement ausgeführt werden soll. Die möglichen Aktionen sind in der folgenden Tabelle aufgeführt.



| Wert   | Bedeutung                     |
|---------|-----------------------------|
| Standard | Legen Sie das Steuerelement als Standard fest. |
| Deaktivieren | Deaktivieren Sie das-Steuerelement.        |
| Aktivieren  | Aktivieren Sie das-Steuerelement.         |
| Ausblenden    | Blenden Sie das Steuerelement aus.           |
| Anzeigen    | Zeigen Sie das Steuerelement an.        |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage
</dt> <dd>

Eine Bedingungs Anweisung, die angibt, unter welchen Bedingungen die Aktion ausgelöst werden soll. Diese Spalte darf nicht leer bleiben. Wenn diese Anweisung nicht als true ausgewertet wird, wird die Aktion nicht ausgeführt. Wenn der Wert auf 1 festgelegt ist, wird die Aktion immer angewendet. Weitere Informationen zur Syntax von Bedingungs Anweisungen finden Sie unter [Syntax für bedingte](conditional-statement-syntax.md)Anweisungen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie ein [PUSHBUTTON-Steuer](pushbutton-control.md) Element oder ein CheckBox- [Steuer](checkbox-control.md) Element auf der Grundlage einer Bedingungs Anweisung im Bedingungs Feld der ControlCondition-Tabelle ausblenden und deaktivieren möchten, sollten Sie für jedes Steuerelement vier Datensätze verwenden, um das Steuerelement zu deaktivieren und das Steuerelement auszublenden. Auf PUSHBUTTON-oder CheckBox-Steuerelemente, die nur ausgeblendet wurden, kann weiterhin über Tastenkombinationen zugegriffen werden.

Die folgenden Datensätze Blenden z. b. die ControlA in dialoga aus und deaktivieren Sie, wenn das Produkt installiert wird. Das-Steuerelement ist sichtbar und wird aktiviert, wenn das Produkt nicht installiert ist.



| Dialog  | Control  | Aktion  | Bedingung                      |
|---------|----------|---------|--------------------------------|
| Dialoga | ControlA | Ausblenden    | [**Installiert**](installed.md) |
| Dialoga | ControlA | Deaktivieren | Installiert                      |
| Dialoga | ControlA | Anzeigen    | Nicht installiert                  |
| Dialoga | ControlA | Aktivieren  | Nicht installiert                  |



 

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



