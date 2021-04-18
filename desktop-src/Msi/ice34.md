---
description: ICE34 überprüft, ob jedes Optionsfeld für jedes RadioButton Group-Steuerelement über eine Eigenschaft in der Eigenschafts Spalte der RadioButton-Tabelle verfügt, die die Optionsfeld Gruppe angibt.
ms.assetid: 23a88a5a-89e9-47bc-9c0a-6101ce03123c
title: ICE34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7723cb530397eae66374b0f218db9ad8505195a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358567"
---
# <a name="ice34"></a>ICE34

ICE34 überprüft, ob jedes Optionsfeld für jedes RadioButton [Group-Steuer](radiobuttongroup-control.md) Element über eine Eigenschaft in der Eigenschafts Spalte der Radio [Button-Tabelle](radiobutton-table.md) verfügt, die die Optionsfeld Gruppe angibt. ICE34 überprüft, ob diese Eigenschaft vorhanden und auf einen Standardwert in der [Eigenschaften Tabelle](property-table.md) festgelegt ist, der einem der Optionsfeld Werte der Gruppe in der Spalte Wert der Tabelle RadioButton entspricht.

Eine Optionsfeld Gruppe muss über einen Standardwert verfügen, damit Benutzer mithilfe der Tab-Taste eine Auswahl treffen können. Dies ist für die richtige Benutzer Barrierefreiheit erforderlich.

ICE34 meldet fehlende Tabellen.

## <a name="result"></a>Ergebnis

ICE34 senden Sie eine Fehlermeldung, wenn ein Optionsfeld vorhanden ist, das eine ungültige Eigenschaft angibt.

## <a name="example"></a>Beispiel

ICE34 meldet die folgenden Fehler für das gezeigte Beispiel.



| ICE34-Fehler                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Das Steuerelement dialoga. Control2 muss über eine-Eigenschaft verfügen, da es vom Typ RadioButtonGroup ist.                                                                                      | Es gibt ein [RadioButton Group-Steuer](radiobuttongroup-control.md)Element, ohne dass das [indirekte Steuerungs](indirect-control-attribute.md) Bit in der Spalte Attribute der [Steuerelement Tabelle](control-table.md)festgelegt ist, die in der Spalte Eigenschaft nicht über eine Eigenschaft verfügt. |
| Möglicherweise ist kein gültiger Standardwert für die RadioButtonGroup mithilfe der Property3-Eigenschaft. Der Wert muss als Option in der Tabelle RadioButton Group aufgeführt werden.                 | Es gibt einen Standardwert für eine Eigenschaft, die in der Spalte Wert der [Eigenschaften Tabelle](property-table.md) angegeben ist, die nicht einer der Werte für die Optionsfeld Gruppe ist, die in der Spalte Wert der [RadioButton-Tabelle](radiobutton-table.md)angegeben ist.                  |
| Property propertyb muss definiert werden, da es sich um eine indirekte Eigenschaft eines RadioButton Group-Steuer Elements dialoga. Control4                                                       | Die Eigenschaft, auf die diese RadioButton-Gruppe verweist, ist eine indirekte Eigenschaft, und der Wert der indirekten Eigenschaft ist nicht eine der Optionen für die RadioButton-Gruppe.                                                                                                       |
| Möglicherweise ist kein gültiger Standardwert für die PropertyA-Eigenschaft. Die-Eigenschaft ist eine indirekte RadioButtonGroup-Eigenschaft des Steuer Elements dialoga. Control5 (über die Property5-Eigenschaft). | Der Wert der indirekten Eigenschaft, auf die über das-Steuerelement verwiesen wird, ist keiner der Standardwerte für diese RadioButtonGroup.                                                                                                                                                    |



 

[Control-Tabelle](control-table.md) (partiell)



| Dialog  | Control  | type             | Attribute | Eigenschaft  |
|---------|----------|------------------|------------|-----------|
| Dialoga | Control1 | RadioButtonGroup | 0          | Property1 |
| Dialoga | Control2 | RadioButtonGroup | 0          |           |
| Dialoga | Control3 | RadioButtonGroup | 0          | Property3 |
| Dialoga | Control4 | RadioButtonGroup | 8          | Property4 |
| Dialoga | Control5 | RadioButtonGroup | 8          | Property5 |



 

[Eigenschaften Tabelle](property-table.md) (partiell)



| Eigenschaft  | Wert     |
|-----------|-----------|
| Property1 | Ja       |
| Property3 | Vielleicht     |
| Property4 | Propertyb |
| Property5 | PropertyA |
| PropertyA | Vielleicht     |



 

[RadioButton-Tabelle](radiobutton-table.md) (partiell)



| Eigenschaft  | Auftrag | Wert |
|-----------|-------|-------|
| Property1 | 1     | Ja   |
| Property1 | 2     | jetzt   |
| Eigenschaft2 | 1     | Ja   |
| Eigenschaft2 | 2     | Nein    |
| Property3 | 1     | Ja   |
| Property3 | 2     | Nein    |
| Property4 | 1     | Ja   |
| Property4 | 2     | Nein    |
| PropertyA | 1     | Ja   |
| PropertyA | 2     | Nein    |
| Propertyb | 1     | Ja   |
| Propertyb | 2     | Nein    |



 

Um die von diesem Ice gemeldeten Fehler zu beheben, überprüfen Sie Folgendes:

-   Jeder RadioButton-Steuerelement Eintrag ohne den indirekten Attribut Satz verfügt über eine Eigenschaft, die in der Eigenschafts Spalte aufgeführt ist:
-   Jede dieser Eigenschaften hat mindestens einen entsprechenden Eintrag in der RadioButton-Tabelle.
-   Jede dieser Eigenschaften wird in der Eigenschaften Tabelle mit einem Wert definiert, der eine der Optionen aus der RadioButton-Tabelle ist.
-   Jede Eigenschaft, auf die in der Eigenschafts Spalte eines RadioButton-Steuer Elements mit dem indirekten Attribut Satz verwiesen wird, wird in der Eigenschaften Tabelle definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



