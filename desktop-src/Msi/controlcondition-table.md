---
description: Mit der ControlCondition-Tabelle kann ein Autor spezielle Aktionen angeben, die basierend auf dem Ergebnis einer bedingten Anweisung auf Steuerelemente angewendet werden sollen. Bei Verwendung dieser Tabelle kann der Autor beispielsweise ein Steuerelement basierend auf der VersionNT-Eigenschaft ausblenden.
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: ControlCondition-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637d9470af21ad1f8a15c2697ba34a6c9866c822c21c6f3a85241bac1309f76b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105250"
---
# <a name="controlcondition-table"></a>ControlCondition-Tabelle

Mit der ControlCondition-Tabelle kann ein Autor spezielle Aktionen angeben, die basierend auf dem Ergebnis einer bedingten Anweisung auf Steuerelemente angewendet werden sollen. Bei Verwendung dieser Tabelle kann der Autor beispielsweise ein Steuerelement basierend auf der [**VersionNT-Eigenschaft ausblenden.**](versionnt.md)

Die ControlCondition-Tabelle enthält die folgenden Spalten.



| Spalte    | Typ                         | Key | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Dialog\_  | [Identifier](identifier.md) | J   | N        |
| Steuerelement\_ | [Identifier](identifier.md) | J   | N        |
| Aktion    | [Text](text.md)             | J   | N        |
| Bedingung | [Condition](condition.md)   | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogfeld\_
</dt> <dd>

Ein externer Schlüssel für die erste Spalte der [Dialogtabelle](dialog-table.md). Wenn Sie dieses Feld mit dem Feld Steuerelement \_ kombinieren, wird ein eindeutiges Steuerelement identifiziert.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Steuerung\_
</dt> <dd>

Ein externer Schlüssel für die zweite Spalte der [Control-Tabelle.](control-table.md) Durch Kombinieren dieses Felds identifiziert das Feld Dialog \_ ein eindeutiges Steuerelement.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Aktion
</dt> <dd>

Die Aktion, die für das Steuerelement übernommen werden soll. Die möglichen Aktionen sind in der folgenden Tabelle aufgeführt.



| Wert   | Bedeutung                     |
|---------|-----------------------------|
| Standard | Legen Sie das Steuerelement als Standard fest. |
| Disable | Deaktivieren Sie das Steuerelement.        |
| Aktivieren  | Aktivieren Sie das Steuerelement.         |
| Ausblenden    | Blendet das Steuerelement aus.           |
| Anzeigen    | Zeigt das Steuerelement an.        |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Zustand
</dt> <dd>

Eine bedingte Anweisung, die angibt, unter welchen Bedingungen die Aktion ausgelöst werden soll. Diese Spalte darf nicht leer gelassen werden. Wenn diese Anweisung nicht zu TRUE ausgewertet wird, wird die Aktion nicht stattfinden. Wenn sie auf 1 festgelegt ist, wird die Aktion immer angewendet. Informationen zur Syntax von bedingten Anweisungen finden Sie unter [Syntax für bedingte Anweisungen.](conditional-statement-syntax.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie ein [PushButton-Steuerelement](pushbutton-control.md) oder [CheckBox-Steuerelement](checkbox-control.md) basierend auf einer Bedingungsanweisung im Feld Bedingung der ControlCondition -Tabelle ausblenden und deaktivieren möchten, sollten Sie vier Datensätze für jedes Steuerelement verwenden, um das Steuerelement zu deaktivieren und auszublenden. Auf PushButton- oder CheckBox-Steuerelemente, die nur ausgeblendet wurden, kann weiterhin über Tastenkombinationen zugegriffen werden.

Die folgenden Datensätze blenden beispielsweise ControlA in DialogA aus und deaktivieren sie, wenn das Produkt installiert wird. Das Steuerelement ist sichtbar und aktiviert, wenn das Produkt nicht installiert ist.



| Dialog  | Control  | Aktion  | Bedingung                      |
|---------|----------|---------|--------------------------------|
| DialogA | Controla | Ausblenden    | [**Installiert**](installed.md) |
| DialogA | Controla | Disable | Installiert                      |
| DialogA | Controla | Anzeigen    | NICHT installiert                  |
| DialogA | Controla | Aktivieren  | NICHT installiert                  |



 

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



