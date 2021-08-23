---
description: Die Dialogtabelle enthält alle Dialoge, die sowohl im vollständigen als auch im reduzierten Modus auf der Benutzeroberfläche angezeigt werden.
ms.assetid: 981386dd-4fee-4003-8c62-16933cc5bd14
title: Dialogfeldtabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554bc551b41a7ebeaa8b63b2a0d1b74a0f55cfb1d7a087936a394a060286caba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692840"
---
# <a name="dialog-table"></a>Dialogfeldtabelle

Die Dialogtabelle enthält alle Dialoge, die sowohl im vollständigen als auch im reduzierten Modus auf der Benutzeroberfläche angezeigt werden.

Die Dialogtabelle enthält die folgenden Spalten.



| Spalte           | Typ                               | Key | Nullwerte zulässig |
|------------------|------------------------------------|-----|----------|
| Dialog           | [Identifier](identifier.md)       | J   | N        |
| HCentering       | [Integer](integer.md)             | N   | N        |
| VCentering       | [Integer](integer.md)             | N   | N        |
| Width            | [Integer](integer.md)             | N   | N        |
| Height           | [Integer](integer.md)             | N   | N        |
| Attribute       | [DoubleInteger](doubleinteger.md) | N   | J        |
| Titel            | [Formatiert](formatted.md)         | N   | J        |
| Zuerst \_ steuern   | [Identifier](identifier.md)       | N   | N        |
| \_Standardsteuerelement | [Identifier](identifier.md)       | N   | J        |
| Abbrechen von \_ Steuerelementen  | [Identifier](identifier.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Dialog"></span><span id="dialog"></span><span id="DIALOG"></span>Dialogfeld
</dt> <dd>

Der Primärschlüssel und der Name des Dialogfelds.

</dd> <dt>

<span id="HCentering"></span><span id="hcentering"></span><span id="HCENTERING"></span>HCentering
</dt> <dd>

Die horizontale Position des Dialogfelds.

Der Bereich ist 0 bis 100, mit 0 am linken Rand des Bildschirms und 100 am rechten Rand.

</dd> <dt>

<span id="VCentering"></span><span id="vcentering"></span><span id="VCENTERING"></span>VCentering
</dt> <dd>

Die vertikale Position des Dialogfelds.

Der Bereich ist 0 bis 100, wobei 0 am oberen Rand des Bildschirms und 100 am unteren Rand liegen.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Breite
</dt> <dd>

Die Breite der rechteckigen Begrenzung des Dialogfelds.

Diese Zahl muss nicht negativ sein.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Höhe
</dt> <dd>

Die Höhe der rechteckigen Begrenzung des Dialogfelds.

Diese Zahl muss nicht negativ sein.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute
</dt> <dd>

Ein 32-Bit-Wort, das die Attributflags angibt, die auf dieses Dialogfeld angewendet werden sollen.

Diese Zahl muss nicht negativ sein. Weitere Informationen finden Sie unter [Dialogformatbits.](dialog-style-bits.md)

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titel
</dt> <dd>

Eine lokalisierbare Textzeichenfolge, die den Titel angibt, der in der Titelleiste des Dialogfelds angezeigt werden soll.

</dd> <dt>

<span id="Control_First"></span><span id="control_first"></span><span id="CONTROL_FIRST"></span>Zuerst \_ steuern
</dt> <dd>

Ein externer Schlüssel für die zweite Spalte der [Steuertabelle](control-table.md).

Das Kombinieren dieses Felds mit dem Dialogfeld gibt ein eindeutiges Steuerelement in der [Steuerelementtabelle](control-table.md) an, das den Fokus erhält, wenn das Dialogfeld geöffnet wird. In der Regel kann dies ein [Bearbeitungssteuerelement,](edit-control.md) [ein SelectionTree-Steuerelement](selectiontree-control.md)oder ein anderes Steuerelement sein, das den Fokus erhalten kann. Wenn das [PushButton-Steuerelement](pushbutton-control.md) das einzige Steuerelement im Dialogfeld ist, das den Fokus erhalten kann, muss das im Feld ControlDefault eingegebene PushButton auch in das Feld Control First eingegeben werden. Diese Spalte wird in einem [Fehlerdialogfeld](error-dialog.md) ignoriert.

Da statischer Text nicht den Fokus erhalten kann, muss ein [Textsteuerelement,](text-control.md) das ein [Bearbeitungssteuerelement,](edit-control.md)ein [PathEdit-Steuerelement,](pathedit-control.md) [ein ListView-Steuerelement,](listview-control.md)ein [ComboBox-Steuerelement](combobox-control.md) oder ein [VolumeSelectCombo-Steuerelement](volumeselectcombo-control.md) beschreibt, zum ersten Steuerelement im Dialogfeld gemacht werden, um die Kompatibilität mit Sprachausgaben sicherzustellen.

</dd> <dt>

<span id="Control_Default"></span><span id="control_default"></span><span id="CONTROL_DEFAULT"></span>\_Standardsteuerelement
</dt> <dd>

Ein externer Schlüssel für die zweite Spalte der [Steuertabelle](control-table.md).

Das Kombinieren dieses Felds mit dem Dialogfeld gibt das Standardsteuerelement an, das beim Öffnen des Dialogfelds den Fokus erhält. In der Regel kann dies ein [PushButton-Steuerelement](pushbutton-control.md)sein. Wenn kein PushButton-Steuerelement im Dialogfeld den Fokus besitzt, entspricht die Rückgabetaste dem Klicken auf das Standardsteuerelement. Wenn diese Spalte leer gelassen wird, gibt es kein Standardsteuerelement. Diese Spalte wird in einem [Fehlerdialogfeld](error-dialog.md) ignoriert.

</dd> <dt>

<span id="Control_Cancel"></span><span id="control_cancel"></span><span id="CONTROL_CANCEL"></span>Abbrechen von \_ Steuerelementen
</dt> <dd>

Ein externer Schlüssel für die zweite Spalte der [Steuertabelle](control-table.md).

Das Kombinieren dieses Felds mit dem Dialogfeld gibt ein Steuerelement an, das die Installation abbricht. Dieses Steuerelement ist an Ereignisse in der [ControlEvent-Tabelle](controlevent-table.md) gekoppelt, die zum Abbrechen der Installation verwendet werden. Das Drücken der ESC-Taste oder das Klicken auf die Schaltfläche Schließen entspricht dem Klicken auf das Abbrechen-Steuerelement. Diese Spalte wird in einem [Fehlerdialogfeld](error-dialog.md) ignoriert.

zu ziehen und sie dort abzulegen.

Das Abbruchsteuerelement wird während des Rollbacks oder beim Entfernen gesicherter Dateien ausgeblendet. Der interne Benutzeroberflächenhandler blendet das Steuerelement beim Empfang einer INSTALLMESSAGE \_ COMMONDATA-Nachricht aus.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die ganzzahligen Werte für Breite und Höhe befinden sich in den [Installer-Einheiten,](installer-units.md)nicht in Dialogeinheiten.

Die beiden zentrierenden Werte werden für nachfolgende Dialogfelder in einer Assistentensequenz ignoriert. Dialogfeldpositionen werden vom Benutzer oder wie für das vorherige Dialogfeld festgelegt. Diese Dialogfeldsequenzen werden von [newDialog ControlEvent](newdialog-controlevent.md)erstellt.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE13](ice13.md)  
[ICE20](ice20.md)  
[ICE23](ice23.md)  
[ICE27](ice27.md)  
[ICE32](ice32.md)  
[ICE44](ice44.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
</dl>

 

 



