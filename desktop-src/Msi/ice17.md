---
description: ICE17 überprüft die im Beispiel am Ende dieses Themas gezeigten Situationen.
ms.assetid: a1d9a6e9-4d21-4544-a813-dc82e11f5a26
title: ICE17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e9714edebd666173a82c75fc6e8fed54a511c64adaa387013648b2f190e88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529200"
---
# <a name="ice17"></a>ICE17

ICE17 überprüft die im Beispiel am Ende dieses Themas gezeigten Situationen.

## <a name="result"></a>Ergebnis

ICE17 zeigt eine Fehler- oder Warnmeldung für jede der Situationen im Beispiel an. Beispiele für solche Meldungen sind in der folgenden Tabelle dargestellt.



| ICE17-Fehler oder -Warnung                                                                                                                                                                                                             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PushButton: Button1 of Dialog: MyDialog does not have an event defined in the ControlEvent table. Fehler <br/>                                                                                                                | Es gibt ein [Pushbutton-Steuerelement,](pushbutton-control.md) das nicht in der [ControlEvent-Tabelle](controlevent-table.md)aufgeführt ist. Wenn ICE17 diesen Fehler für ein PushButton-Steuerelement zurückgibt, für das das **Attribut Enable Control** oder das Visible **Control-Attribut** nicht in der Spalte Attribute der [Control-Tabelle](control-table.md)festgelegt ist, überprüfen Sie, ob das Steuerelement auch über einen Eintrag in der [ControlCondition-Tabelle](controlcondition-table.md)verfügt. Das Steuerelement kann unerwartet aktiviert oder sichtbar werden, wenn sich der Wert in der Spalte Bedingung in True, Enable oder Show ändert.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| Bitmap: Bitmap1 des Steuerelements: Bitmap1 des Dialogs: MyDialog ist nicht in der Binärtabelle enthalten. Fehler <br/>                                                                                                                              | Es gibt ein [Bitmap-Steuerelement](bitmap-control.md) oder [Symbolsteuerelement,](icon-control.md)aber die entsprechende Bitmap oder das entsprechende Symbol ist nicht in der [Binärtabelle](binary-table.md)aufgeführt. Fügen Sie der Binärtabelle die Bitmap oder das Symbol hinzu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| RadioButtonGroup: RadioButton1 of Control: RadioButton1 of Dialog: MyDialog is not in the RadioButton table. Warnung <br/>                                                                                                   | Es gibt ein [RadioButtonGroup-Steuerelement](radiobuttongroup-control.md) mit Werten in der Property-Spalte und der Attribute -Spalte der [Control-Tabelle](control-table.md). Das [indirekte](indirect-control-attribute.md) Bit ist in der Spalte Attribute nicht festgelegt. ICE17 gibt eine Warnung aus, da das Installationsprogramm den Wert der Eigenschaft als Fremdschlüssel in der RadioButton-Tabelle verwendet, der Wert jedoch im Primärschlüssel dieser Tabelle fehlt. Wenn das [indirekte](indirect-control-attribute.md) Bit festgelegt ist, wird die für das Steuerelement aufgelistete Eigenschaft nicht als -Eigenschaft verwendet. stattdessen wird sie als Name der Eigenschaft verwendet, die tatsächlich verwendet wird.<br/> Diese Warnung kann ignoriert werden, wenn das Steuerelement zur Laufzeit erstellt wird. Beispielsweise wird das [ListBox-Steuerelement](listbox-control.md) für im [FilesInUse-Dialogfeld](filesinuse-dialog.md) nur zur Laufzeit erstellt, wenn während der Installation Dateien verwendet werden.<br/> |
| ListBox: ListBox1 des Steuerelements: ListBox1 des Dialogfelds: MyDialog befindet sich nicht in der ListBox-Tabelle. Warnung <br/>                                                                                                                        | Es gibt ein [ListBox-Steuerelement](listbox-control.md) mit einem Wert in der Property -Spalte der [Control-Tabelle,](control-table.md) für das das [indirekte](indirect-control-attribute.md) Bit nicht in der Spalte Attribute festgelegt ist. ICE17 gibt eine Warnung aus, da das Installationsprogramm den Wert der Eigenschaft als Fremdschlüssel in der [ListBox-Tabelle](listbox-table.md)verwendet, der Wert jedoch im Primärschlüssel dieser Tabelle fehlt. Wenn das [indirekte](indirect-control-attribute.md) Bit festgelegt ist, ändert das Steuerelement den Wert einer Eigenschaft mit einem Namen, der dem Wert der diesem Steuerelement zugeordneten Eigenschaft entspricht.<br/> Diese Warnung kann ignoriert werden, wenn das Steuerelement zur Laufzeit erstellt wird. Beispielsweise wird das [ListBox-Steuerelement](listbox-control.md) für im [FilesInUse-Dialogfeld](filesinuse-dialog.md) nur zur Laufzeit erstellt, wenn während der Installation Dateien verwendet werden.<br/>                                |
| ComboBox: ComboBox1 des Steuerelements: ComboBox1 des Dialogfelds: ByDialog ist nicht in der ComboBox-Tabelle Warning enthalten <br/>                                                                                                                     | Es gibt ein [ComboBox-Steuerelement](combobox-control.md) mit einem Wert in der Property -Spalte der [Control-Tabelle,](control-table.md) für das das [indirekte](indirect-control-attribute.md) Bit nicht in der Spalte Attribute festgelegt ist. ICE17 gibt eine Warnung aus, da das Installationsprogramm den Wert der Eigenschaft als Fremdschlüssel in der [ComboBox-Tabelle](combobox-table.md)verwendet, der Wert jedoch im Primärschlüssel dieser Tabelle fehlt. Wenn das [indirekte](indirect-control-attribute.md) Bit festgelegt ist, ändert das Steuerelement den Wert einer Eigenschaft mit einem Namen, der dem Wert der diesem Steuerelement zugeordneten Eigenschaft entspricht.<br/> Diese Warnung kann ignoriert werden, wenn das Steuerelement zur Laufzeit erstellt wird. Beispielsweise wird das [ListBox-Steuerelement](listbox-control.md) für im [FilesInUse-Dialogfeld](filesinuse-dialog.md) nur zur Laufzeit erstellt, wenn während der Installation Dateien verwendet werden.<br/>                            |
| ListView: ListView1 des Steuerelements: ListView1 des Dialogs: MyDialog befindet sich nicht in der ListView-Tabelle. Warnung <br/>                                                                                                                    | Es gibt ein [ListView-Steuerelement](listview-control.md) mit einem Wert in der Property -Spalte der [Control-Tabelle,](control-table.md) für das das [indirekte](indirect-control-attribute.md) Bit nicht in der Spalte Attribute festgelegt ist. ICE17 gibt eine Warnung aus, da das Installationsprogramm den Wert der Eigenschaft als Fremdschlüssel in der [ListView-Tabelle](listview-table.md)verwendet, der Wert jedoch im Primärschlüssel dieser Tabelle fehlt. Wenn das [indirekte](indirect-control-attribute.md) Bit festgelegt ist, ändert das Steuerelement den Wert einer Eigenschaft mit einem Namen, der dem Wert der diesem Steuerelement zugeordneten Eigenschaft entspricht.<br/> Diese Warnung kann ignoriert werden, wenn das Steuerelement zur Laufzeit erstellt wird. Beispielsweise wird das [ListBox-Steuerelement](listbox-control.md) für im [FilesInUse-Dialogfeld](filesinuse-dialog.md) nur zur Laufzeit erstellt, wenn während der Installation Dateien verwendet werden.<br/>                            |
| Bitmap: 'Bitmap2' for Control: 'Button2' of Dialog: 'MyDialog' not found in Binary table Error <br/>                                                                                                                         | Es gibt ein [Pushbutton-Steuerelement](pushbutton-control.md) oder ein [Kontrollkästchen-Steuerelement,](checkbox-control.md) für das die Text -Spalte der [Control-Tabelle](control-table.md) keinen Fremdschlüssel im Datensatz der [Binärtabelle](binary-table.md) enthält, die die Bitmap oder das Symbol enthält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Bitmap: 'Bitmap3' for Control: 'RadioButton2' of Dialog: 'MyDialog' not found in Binary table or<br/> Symbol: 'Icon1' for Control: 'RadioButton3' of Dialog: 'MyDialog' not found in Binary table<br/> Fehler <br/> | Es gibt ein [RadioButtonGroup-Steuerelement,](radiobuttongroup-control.md) für das die Text-Spalte der [RadioButton-Tabelle](radiobutton-table.md) keinen Fremdschlüssel im Datensatz der [Binary-Tabelle](binary-table.md) enthält, die die Bitmap oder das Symbol enthält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Bildsteuerelement: "Button3" des Dialogs: "MyDialog" hat sowohl das Symbol als auch das Bitmap-Attribut "Error" festgelegt. <br/>                                                                                                                     | Es gibt ein [PushButton-,](pushbutton-control.md) [CheckBox-](checkbox-control.md)oder [RadioButtonGroup-Steuerelement,](radiobuttongroup-control.md) bei dem sowohl das [Icon-Bit](icon-control-attribute.md) als auch das [Bitmap-Bit](bitmap-control-attribute.md) in der Attributes -Spalte der [Control-Tabelle](control-table.md)festgelegt ist. Beide Attribute können nicht zusammen festgelegt werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="example"></a>Beispiel

[Steuertabelle](control-table.md) (partiell)



| Dialog\_ | Control      | Typ             | Attribute | Eigenschaft     | Text       |
|----------|--------------|------------------|------------|--------------|------------|
| MyDialog | Schaltfläche1      | Pushbutton       | 0          |              | OK         |
| MyDialog | Bitmap1      | Bitmap           | 0          |              | Bitmap1    |
| MyDialog | Radiobutton1 | RadioButtonGroup | 0          | Radiobutton1 |            |
| MyDialog | ListBox1     | ListBox          | 0          | ListBox1     |            |
| MyDialog | ComboBox1    | Kombinationsfeld         | 0          | ComboBox1    |            |
| MyDialog | ListView1    | ListView         | 0          | ListView1    |            |
| MyDialog | Schaltfläche 2      | Pushbutton       | 262144     |              | Bitmap2    |
| MyDialog | RadioButton2 | RadioButtonGroup | 262144     |              | Property2  |
| MyDialog | RadioButton3 | RadioButtonGroup | 524288     |              | Property3  |
| MyDialog | Schaltfläche 3      | Pushbutton       | 786432     |              | Mehrdeutig1 |



 

[RadioButton-Tabelle](radiobutton-table.md) (partiell)



| Eigenschaft\_ | Auftrag | Text    |
|------------|-------|---------|
| Property2  | 1     | Bitmap3 |
| Property3  | 2     | Symbol1   |



 

Die folgenden Tabellen sind leer:

-   [ControlEvent-Tabelle](controlevent-table.md)
-   [ListBox-Tabelle](listbox-table.md)
-   [ComboBox-Tabelle](combobox-table.md)
-   [ListView-Tabelle](listview-table.md)
-   [Binäre Tabelle](binary-table.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




