---
description: Das MaskedEdit-Steuerelement ist ein Bearbeitungsfeld-Steuerelement, das eine Maske im Textfeld des Steuer Elements enthält. Sie können das Steuerelement einer Zeichen folgen Wert Eigenschaft zuordnen, indem Sie den Eigenschaftsnamen in die Eigenschafts Spalte der Steuerelement Tabelle eingeben.
ms.assetid: 8cc14683-3dbb-404f-87af-09a5f5b90b19
title: Maskedebug-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7568df9969ebabab6311e519d0a5a625feb8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364265"
---
# <a name="maskededit-control"></a>Maskedebug-Steuerelement

Das MaskedEdit-Steuerelement ist ein Bearbeitungsfeld-Steuerelement, das eine Maske im Textfeld des Steuer Elements enthält. Sie können das Steuerelement einer Zeichen folgen Wert Eigenschaft zuordnen, indem Sie den Eigenschaftsnamen in die Eigenschafts Spalte der [Steuerelement Tabelle](control-table.md)eingeben.

Sie können das MaskedEdit-Steuerelement verwenden, um eine Vorlage für den Benutzereintrag von Informationen zu erstellen, z. b. eine Telefonnummer oder einen Product ID-Code. Die [**PIDKEY**](pidkey.md) -Eigenschaft kann z. b. vom Benutzer über ein masketodit-Steuerelement eingegeben werden, das durch Festlegen der [**pidtemplate**](pidtemplate.md) -Eigenschaft auf eine Zeichenfolge wie die folgende festgelegt wird:

12345<\#\#\# -%%%%%%%>@@@@@

Die Zeichenfolge definiert die Maskierungs Vorlage für den Eintrag der [**PIDKEY**](pidkey.md) -Eigenschaft durch den Benutzer. Das sichtbare Segment der Zeichenfolge wird durch ein paar aus Klammern (<>) eingeschlossen.

In der folgenden Tabelle ist die Syntax der Maske angegeben.



| Zeichen | Bedeutung                                                                                                                                                                                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <      | Das linke Ende des sichtbaren Segments der Vorlage. Dieses Zeichen und alles auf der linken Seite werden in der Benutzeroberfläche ausgeblendet. In der Vorlage darf nicht mehr als eine Instanz dieses Zeichens vorhanden sein.                                                                               |
| >      | Das rechte Ende des sichtbaren Segments der Vorlage. Dieses Zeichen und alles auf der rechten Seite werden in der Benutzeroberfläche ausgeblendet. Dieses Zeichen wird während der Validierung durch einen Bindestrich ersetzt. Wenn ein sichtbares Segment mit < beginnt, muss es mit einem übereinstimmenden > beendet werden. |
| \#        | Bei diesem Zeichen kann es sich um eine Ziffer (Numeral) handeln.                                                                                                                                                                                                                                                    |
| %         | Bei diesem Zeichen kann es sich um eine Alternative Ziffer (Numeral) handeln, mit der die Maske steuern kann, wie Felder von einer benutzerdefinierten Aktion unterschieden werden.                                                                                                                                                          |
| @         | Bei diesem Zeichen kann es sich um eine zufällige Ziffer (Numeral) handeln. Dieses Zeichen sollte nicht im sichtbaren Teil der Vorlage angezeigt werden.                                                                                                                                                                       |
| &         | Dabei kann es sich um ein beliebiges Zeichen handeln.                                                                                                                                                                                                                                                        |
| ^         | Bei diesem Zeichen kann es sich um ein alternatives Zeichen handeln, mit dem die Maske steuern kann, wie Felder von einer benutzerdefinierten Aktion unterschieden werden.                                                                                                                                                                |
| ?         | Bei diesem Zeichen kann es sich um ein alternatives Zeichen handeln, mit dem die Maske steuern kann, wie Felder von einer benutzerdefinierten Aktion unterschieden werden.                                                                                                                                                                |
| \`        | \` Gewichtungs Zeichen (ASCII-Wert 96) können ein alternatives Zeichen darstellen, das es der Maske ermöglicht, die Art und Weise zu steuern, in der eine benutzerdefinierte Aktion Felder unterscheidet.                                                                                                                                 |
| \_        | Dieses Zeichen ist ein literalunterstrich.                                                                                                                                                                                                                                           |
| =         | Dieses Zeichen ist das Feld Abschluss Zeichen. Dieser muss auf \# ,%, ^ oder folgen \` . Dadurch wird eine weitere Eingabe Position desselben Typs wie die vorangehenden Positionen erstellt, und das Feld mit dem Trennzeichen "-" wird beendet.                                                                                 |



 

Jedes andere Zeichen wird als Literalkonstante behandelt.

Für Zeichen, die bearbeitet werden können, erstellt das Steuerelement separate Bearbeitungsfenster mit einem Fenster für jeden Block von zusammenhängenden Zeichen derselben Art.

## <a name="control-attributes"></a>Steuerelement Attribute

Wenn Sie den Wert eines Attributs ändern möchten, das ein Ereignis verwendet, abonnieren Sie das Steuerelement in der [Tabelle EventMapping](eventmapping-table.md) einem Steuerungs Ereignis, und Listen Sie den Attribut Bezeichner in der Attribut-Spalte auf. Geben Sie den Bezeichner des Steuerelement Ereignisses in der Ereignis Spalte ein. Sie können die folgenden Attribute mit dem maskedebug-Steuerelement verwenden.



| Attribut                                                          | Hexadezimales Bit                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Derekpropertyname](indirectpropertyname-control-attribute.md) |                                  | Dies ist der Name einer indirekten Eigenschaft, die dem Steuerelement zugeordnet ist. Wenn das indirekte Attribut Bit festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft an, die diesen Namen aufweist, oder ändert ihn. Wenn das indirekte Attribut Bit festgelegt ist, ist dieser Name auch der Wert der Eigenschaft, die in der Eigenschafts Spalte der [Steuerelement Tabelle](control-table.md)aufgeführt ist.                                                                                                                                   |
| [Position](position-control-attribute.md)                         |                                  | Position des-Steuer Elements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der Steuerelemente der linken Ecke des Steuer Elements in die Spalten Width, Height, X und Y der [Steuerelement Tabelle](control-table.md)ein. Verwenden Sie die [Installer-Einheiten](installer-units.md) für Länge und Entfernung.<br/>                                                                                                                                                                                                            |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Dies ist der Name der Eigenschaft, die diesem Steuerelement zugeordnet ist. Wenn das indirekte Attribut Bit nicht festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft an, die diesen Namen aufweist, oder ändert ihn. Dieses Attribut wird in der-Eigenschaften Spalte der [Steuerelement Tabelle](control-table.md)angegeben.                                                                                                                                                                                                           |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Aktueller Wert der Eigenschaft, die von diesem Steuerelement angezeigt oder geändert wird. Wenn das indirekte Attribut Bit nicht festgelegt ist, ist dies der Wert von PropertyName. Wenn das indirekte Attribut Bit festgelegt ist, ist dies der Wert von deretpropertyname. Wenn sich das Attribut ändert, spiegelt das-Steuerelement den neuen Wert wider.                                                                                                                                                                                                |
| [Text](text-control-attribute.md)                                 |                                  | Um die Schriftart und den Schrift Schnitt einer Text Zeichenfolge festzulegen, stellen Sie die Zeichenfolge der angezeigten Zeichen mit "{ \\ Style}" oder "{&Style}" vor. Dabei ist Style ein Bezeichner, der in der Style-Spalte der [TextStyle-Tabelle](textstyle-table.md)aufgeführt ist. Wenn keines dieser beiden vorhanden ist, die [**defaultuifont**](defaultuifont.md) -Eigenschaft jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet. Die Zeichenfolge, die die Maskierungs Vorlage angibt, folgt diesem Präfix und verwendet die zuvor in diesem Thema beschriebene Syntax. |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Verborgenes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das bitwort der Spalte Attribute der [Tabelle](control-table.md) "Attribute" ein, damit das Steuerelement beim Erstellen sichtbar oder ausgeblendet wird.<br/> Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" ausblenden oder anzeigen.<br/>                                                                                                                                                                 |
| [Aktiviert](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Steuerelement in deaktiviertem Zustand. Steuerelement im aktivierten Zustand.<br/> Fügen Sie dieses Bit in das bitwort in die Spalte Attribute der [Steuerelement Tabelle](control-table.md) ein, um das Steuerelement bei der Erstellung zu aktivieren.<br/> Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" aktivieren oder deaktivieren.<br/>                                                                                                                                                          |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Zeigt den visuellen Standardstil an. Zeigt das Steuerelement mit einem abgesenkten 3D-Bild an.<br/> Fügen Sie diese Bits in das bitwort in die Spalte Attribute der [Steuerelement Tabelle](control-table.md)ein.<br/>                                                                                                                                                                                                                                                                                          |
| [Indirekt](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Das-Steuerelement zeigt den Wert der-Eigenschaft in der-Eigenschaften Spalte der [Steuerelement Tabelle](control-table.md)an oder ändert ihn. Das-Steuerelement zeigt den Wert der-Eigenschaft an oder ändert den Wert der-Eigenschaft, [die den](control-table.md)Bezeichner enthält<br/> Bestimmt, ob indirekt auf die Eigenschaft verwiesen wird, die diesem Steuerelement zugeordnet ist.<br/>                                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Mit dem MaskedEdit-Steuerelement wird ein übergeordnetes Fenster der **Button** -Klasse mit den Stilen " **\_ Besitzers** " und " **WS \_ Ex \_ controlparent** " erstellt. In diesem Fenster werden mehrere untergeordnete Fenster erstellt.

-   Bei konstanten Textteilen werden statische Fenster mit den untergeordneten Werten " **SS \_ left** " und " **WS \_** " erstellt.
-   Für bearbeitbare Felder wird ein Bearbeitungsfenster mit den Stilen **WS \_ Child**, **WS \_ Border** und **WS \_ Tabstopps** erstellt.
-   Bei numerischen Feldern hat das Fenster auch den **es- \_ Zahlen** Stil.

Mit den alternativen Ziffern,% und alternativen alphanumerischen Zeichen (^,? und) können \` benutzerdefinierte Aktionen zwischen Feldern auf eine Weise unterscheiden, die von der Maske gesteuert werden kann. beispielsweise kann ^ für Felder verwendet werden, die Großbuchstaben sein sollten.

 

 




