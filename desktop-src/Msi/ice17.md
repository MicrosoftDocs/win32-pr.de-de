---
description: ICE17 prüft, ob die im Beispiel am Ende dieses Themas gezeigten Situationen angezeigt werden.
ms.assetid: a1d9a6e9-4d21-4544-a813-dc82e11f5a26
title: ICE17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c296273e1de5ae633b2708c92cf0376018e6d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866300"
---
# <a name="ice17"></a>ICE17

ICE17 prüft, ob die im Beispiel am Ende dieses Themas gezeigten Situationen angezeigt werden.

## <a name="result"></a>Ergebnis

ICE17 zeigt eine Fehler-oder Warnmeldung für jede der Situationen im Beispiel an. In der folgenden Tabelle sind Beispiele für solche Meldungen aufgeführt.



| ICE17-Fehler oder-Warnung                                                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PUSHBUTTON: Button1 of Dialog: in der Tabelle "ControlEvent" ist kein Ereignis definiert. Fehler <br/>                                                                                                                | Es gibt ein [PUSHBUTTON-Steuer](pushbutton-control.md) Element, das in der [ControlEvent-Tabelle](controlevent-table.md)nicht aufgeführt ist. Wenn ICE17 diesen Fehler auf einem PUSHBUTTON zurückgibt, für den das **Enable Control** -Attribut oder das **Visible-Steuer** Element Attribut nicht in der Attribute-Spalte der [Steuerelement Tabelle](control-table.md)festgelegt ist, überprüfen Sie, ob das Steuerelement auch über einen Eintrag in der [Tabelle ControlCondition](controlcondition-table.md)verfügt. Das Steuerelement kann unerwartet aktiviert oder sichtbar werden, wenn der Wert in der Spalte Bedingung in true, Enable oder Show geändert wird.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| Bitmap: bitmap1 of Control: bitmap1 of Dialog: MyDialog ist nicht in der binären Tabelle. Fehler <br/>                                                                                                                              | Es gibt ein [Bitmap-Steuer](bitmap-control.md) Element oder ein [Symbol Steuer](icon-control.md)Element, aber das entsprechende Bitmap-oder-Symbol ist nicht in der [binären Tabelle](binary-table.md)aufgeführt. Fügen Sie der Binär Tabelle das Bitmap-oder-Symbol hinzu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| RadioButtonGroup: RadioButton1 of Control: RadioButton1 of Dialog: MyDialog ist nicht in der RadioButton-Tabelle. Warnung <br/>                                                                                                   | Ein [RadioButton Group-Steuer](radiobuttongroup-control.md) Element mit Werten in der Eigenschafts Spalte und der Attribut Spalte der [Steuerelement Tabelle](control-table.md)ist vorhanden. Das [indirekte](indirect-control-attribute.md) Bit ist nicht in der Spalte Attribute festgelegt. ICE17 gibt eine Warnung aus, da das Installationsprogramm den Wert der Eigenschaft als Fremdschlüssel in der RadioButton-Tabelle verwendet, der Wert jedoch nicht im Primärschlüssel dieser Tabelle vorhanden ist. Wenn das [indirekte](indirect-control-attribute.md) Bit festgelegt ist, wird die für das Steuerelement aufgeführte Eigenschaft nicht als Eigenschaft verwendet. Stattdessen wird Sie als Name der Eigenschaft verwendet, die tatsächlich verwendet wird.<br/> Diese Warnung kann ignoriert werden, wenn das Steuerelement zur Laufzeit erstellt wird. Beispielsweise wird das [ListBox-Steuer](listbox-control.md) Element für im [FilesInUse-Dialog](filesinuse-dialog.md) Feld nur zur Laufzeit erstellt, wenn Dateien während der Installation verwendet werden.<br/> |
| ListBox: ListBox1 of Control: ListBox1 of Dialog: MyDialog ist nicht in der ListBox-Tabelle. Warnung <br/>                                                                                                                        | Es gibt ein [ListBox-Steuer](listbox-control.md) Element mit einem Wert in der Eigenschafts Spalte der [Steuerelement Tabelle](control-table.md) , für das das [indirekte](indirect-control-attribute.md) Bit nicht in der Spalte Attribute festgelegt ist. ICE17 gibt eine Warnung aus, da das Installationsprogramm den Wert der Eigenschaft als Fremdschlüssel in der [ListBox-Tabelle](listbox-table.md)verwendet, der Wert jedoch im Primärschlüssel dieser Tabelle fehlt. Wenn das [indirekte](indirect-control-attribute.md) Bit festgelegt ist, ändert das Steuerelement den Wert einer Eigenschaft, die einen Namen hat, der dem Wert der Eigenschaft entspricht, die diesem Steuerelement zugeordnet ist.<br/> Diese Warnung kann ignoriert werden, wenn das Steuerelement zur Laufzeit erstellt wird. Beispielsweise wird das [ListBox-Steuer](listbox-control.md) Element für im [FilesInUse-Dialog](filesinuse-dialog.md) Feld nur zur Laufzeit erstellt, wenn Dateien während der Installation verwendet werden.<br/>                                |
| ComboBox: comboBox1 of Control: comboBox1 of Dialog: bydialog nicht in der ComboBox-Tabellen Warnung <br/>                                                                                                                     | Es gibt ein [ComboBox-Steuer](combobox-control.md) Element mit einem Wert in der Eigenschafts Spalte der [Steuerelement Tabelle](control-table.md) , für das das [indirekte](indirect-control-attribute.md) Bit nicht in der Spalte Attribute festgelegt ist. ICE17 gibt eine Warnung aus, da das Installationsprogramm den Wert der Eigenschaft als Fremdschlüssel in der [ComboBox-Tabelle](combobox-table.md)verwendet, der Wert jedoch nicht im Primärschlüssel dieser Tabelle vorhanden ist. Wenn das [indirekte](indirect-control-attribute.md) Bit festgelegt ist, ändert das Steuerelement den Wert einer Eigenschaft, die einen Namen hat, der dem Wert der Eigenschaft entspricht, die diesem Steuerelement zugeordnet ist.<br/> Diese Warnung kann ignoriert werden, wenn das Steuerelement zur Laufzeit erstellt wird. Beispielsweise wird das [ListBox-Steuer](listbox-control.md) Element für im [FilesInUse-Dialog](filesinuse-dialog.md) Feld nur zur Laufzeit erstellt, wenn Dateien während der Installation verwendet werden.<br/>                            |
| ListView: listView1 of Control: listView1 of Dialog: MyDialog ist nicht in der ListView-Tabelle. Warnung <br/>                                                                                                                    | Es gibt ein [ListView-Steuer](listview-control.md) Element mit einem Wert in der Eigenschafts Spalte der [Steuerelement Tabelle](control-table.md) , für das das [indirekte](indirect-control-attribute.md) Bit nicht in der Spalte Attribute festgelegt ist. ICE17 gibt eine Warnung aus, da das Installationsprogramm den Wert der Eigenschaft als Fremdschlüssel in der [ListView-Tabelle](listview-table.md)verwendet, der Wert jedoch nicht im Primärschlüssel dieser Tabelle vorhanden ist. Wenn das [indirekte](indirect-control-attribute.md) Bit festgelegt ist, ändert das Steuerelement den Wert einer Eigenschaft, die einen Namen hat, der dem Wert der Eigenschaft entspricht, die diesem Steuerelement zugeordnet ist.<br/> Diese Warnung kann ignoriert werden, wenn das Steuerelement zur Laufzeit erstellt wird. Beispielsweise wird das [ListBox-Steuer](listbox-control.md) Element für im [FilesInUse-Dialog](filesinuse-dialog.md) Feld nur zur Laufzeit erstellt, wenn Dateien während der Installation verwendet werden.<br/>                            |
| Bitmap: ' Bitmap2 ' für Steuerung: ' Button2 ' des Dialog Felds: ' MyDialog ' wurde in Binär Tabellen Fehler nicht gefunden. <br/>                                                                                                                         | Es gibt ein [PUSHBUTTON-Steuer](pushbutton-control.md) Element oder ein [CheckBox-Steuer](checkbox-control.md) Element, für das die Text-Spalte der [Steuerelement Tabelle](control-table.md) keinen Fremdschlüssel in den Datensatz der [binären Tabelle](binary-table.md) enthält, in der die Bitmap oder das Symbol enthalten ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Bitmap: ' Bitmap3 ' für Steuerelement: ' radioButton2 ' des Dialog Felds: ' MyDialog ' wurde in der Binär Tabelle nicht gefunden.<br/> Symbol: "icon1" für das Steuerelement: "radioButton3" des Dialog Felds: "MyDialog" wurde in der Binär Tabelle nicht gefunden.<br/> Fehler <br/> | Es gibt ein [RadioButton Group-Steuer](radiobuttongroup-control.md) Element, für das die Text-Spalte der [RadioButton-Tabelle](radiobutton-table.md) keinen Fremdschlüssel in den Datensatz der [binären Tabelle](binary-table.md) enthält, in der die Bitmap oder das Symbol enthalten ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Bild-Steuerelement: ' Button3 ' des Dialog Felds: ' MyDialog ' weist sowohl Symbol-als auch bitmapattribute auf. <br/>                                                                                                                     | Es gibt ein [Push Button](pushbutton-control.md)-Steuerelement, ein [CheckBox](checkbox-control.md)-Steuerelement oder ein [RadioButton Group](radiobuttongroup-control.md) -Steuerelement, für das in der Spalte Attribute der [Steuerelement Tabelle](control-table.md)das [Symbol](icon-control-attribute.md) Bit oder [bitmapbit](bitmap-control-attribute.md) festgelegt ist. Beide Attribute können nicht gleichzeitig festgelegt werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="example"></a>Beispiel

[Control-Tabelle](control-table.md) (partiell)



| Dialog\_ | Control      | type             | Attribute | Eigenschaft     | Text       |
|----------|--------------|------------------|------------|--------------|------------|
| MyDialog | Schaltfläche1      | PUSHBUTTON       | 0          |              | OK         |
| MyDialog | Bitmap1      | Bitmap           | 0          |              | Bitmap1    |
| MyDialog | RadioButton1 | RadioButtonGroup | 0          | RadioButton1 |            |
| MyDialog | ListBox1     | ListBox          | 0          | ListBox1     |            |
| MyDialog | ComboBox1    | Kombinationsfeld         | 0          | ComboBox1    |            |
| MyDialog | ListView1    | ListView         | 0          | ListView1    |            |
| MyDialog | Button2      | PUSHBUTTON       | 262144     |              | Bitmap2    |
| MyDialog | RadioButton2 | RadioButtonGroup | 262144     |              | Eigenschaft2  |
| MyDialog | RadioButton3 | RadioButtonGroup | 524288     |              | Property3  |
| MyDialog | Button3      | PUSHBUTTON       | 786432     |              | Ambiguous1 |



 

[RadioButton-Tabelle](radiobutton-table.md) (partiell)



| Eigenschaft\_ | Auftrag | Text    |
|------------|-------|---------|
| Eigenschaft2  | 1     | Bitmap3 |
| Property3  | 2     | Icon1   |



 

Die folgenden Tabellen sind leer:

-   [ControlEvent-Tabelle](controlevent-table.md)
-   [ListBox-Tabelle](listbox-table.md)
-   [ComboBox-Tabelle](combobox-table.md)
-   [ListView-Tabelle](listview-table.md)
-   [Binäre Tabelle](binary-table.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




