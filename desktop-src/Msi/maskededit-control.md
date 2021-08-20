---
description: Das MaskedEdit-Steuerelement ist ein Bearbeitungsfeld-Steuerelement, das eine Maske im Textfeld des Steuerelements enthält. Sie können das Steuerelement einer Zeichenfolgenwerteigenschaft zuordnen, indem Sie den Eigenschaftennamen in die Spalte Eigenschaft der Steuertabelle eingeben.
ms.assetid: 8cc14683-3dbb-404f-87af-09a5f5b90b19
title: MaskedEdIt-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30a6490cf2eb05d001d00a1cd8b5b3d33520ea735ebe0d05f064d4053847b691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805105"
---
# <a name="maskededit-control"></a>MaskedEdIt-Steuerelement

Das MaskedEdit-Steuerelement ist ein Bearbeitungsfeld-Steuerelement, das eine Maske im Textfeld des Steuerelements enthält. Sie können das Steuerelement einer Zeichenfolgenwerteigenschaft zuordnen, indem Sie den Eigenschaftsnamen in die Spalte Eigenschaft der [Steuertabelle eingeben.](control-table.md)

Sie können das MaskedEdIt-Steuerelement verwenden, um eine Vorlage für die Benutzereingabe von Informationen wie einer Telefonnummer oder einem Produkt-ID-Code zu erstellen. Beispielsweise kann die [**PIDKEY-Eigenschaft**](pidkey.md) vom Benutzer über ein MaskedEdit-Steuerelement eingegeben werden, das durch Festlegen der [**PIDTemplate-Eigenschaft**](pidtemplate.md) auf eine Zeichenfolge wie die folgende angegeben wird:

12345<\#\#\# -%%%%%%%>@@@@@

Die Zeichenfolge definiert die Maskierungsvorlage für den Eintrag der [**PIDKEY-Eigenschaft**](pidkey.md) durch den Benutzer. Das sichtbare Segment der Zeichenfolge wird von einem Klammerpaar (<>) eingeschlossen.

In der folgenden Tabelle wurde die Syntax der Maske identifiziert.



| Zeichen | Bedeutung                                                                                                                                                                                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <      | Das linke Ende des sichtbaren Segments der Vorlage. Dieses Zeichen und alles auf der linken Seite werden in der Benutzeroberfläche ausgeblendet. Die Vorlage darf nicht mehr als eine Instanz dieses Zeichens enthalten.                                                                               |
| >      | Das rechte Ende des sichtbaren Segments der Vorlage. Dieses Zeichen und alles auf der rechten Seite werden auf der Benutzeroberfläche ausgeblendet. Dieses Zeichen wird während der Validierung durch einen Bindestrich ersetzt. Wenn ein sichtbares Segment mit < beginnt, muss es mit einem übereinstimmenden >. |
| \#        | Dieses Zeichen kann eine Ziffer (Ziffer) sein.                                                                                                                                                                                                                                                    |
| %         | Dieses Zeichen kann eine alternative Ziffer (Ziffer) sein, die es der Maske ermöglicht, die Art und Weise zu steuern, wie eine benutzerdefinierte Aktion Felder unterscheidet.                                                                                                                                                          |
| @         | Dieses Zeichen kann eine zufällige Ziffer (Zahl) sein. Dieses Zeichen sollte nicht im sichtbaren Teil der Vorlage angezeigt werden.                                                                                                                                                                       |
| &         | Dieses Zeichen kann ein beliebiges Zeichen sein.                                                                                                                                                                                                                                                        |
| ^         | Dieses Zeichen kann ein alternatives Zeichen sein, mit dem die Maske steuern kann, wie eine benutzerdefinierte Aktion Felder unterscheidet.                                                                                                                                                                |
| ?         | Dieses Zeichen kann ein alternatives Zeichen sein, mit dem die Maske steuern kann, wie eine benutzerdefinierte Aktion Felder unterscheidet.                                                                                                                                                                |
| \`        | Zeichen mit Akzenten (ASCII-Wert 96) können ein alternatives Zeichen darstellen, das es der Maske ermöglicht, die Art und Weise zu steuern, wie eine benutzerdefinierte Aktion \` Felder unterscheidet.                                                                                                                                 |
| \_        | Dieses Zeichen ist ein literales Unterstrichzeichen.                                                                                                                                                                                                                                           |
| =         | Dieses Zeichen ist das Feldabschlusszeichen. Dieser muss auf \# , %, ^oder \` folgen. Dadurch wird eine weitere Eingabeposition vom gleichen Typ wie die vorherigen Positionen erstellt und das Feld mit einem Trennzeichen "-" beendet.                                                                                 |



 

Jedes andere Zeichen wird als literale Konstante behandelt.

Für Zeichen, die bearbeitet werden können, erstellt das Steuerelement separate Bearbeitungsfenster mit einem Fenster für jeden Block zusammenhängender Zeichen der gleichen Art.

## <a name="control-attributes"></a>Steuerelementattribute

Um den Wert eines Attributs zu ändern, das ein Ereignis verwendet, abonnieren Sie das Steuerelement für ein Control-Ereignis in der [EventMapping-Tabelle,](eventmapping-table.md) und listen Sie den Attributbezeichner in der Spalte Attribut auf. Geben Sie den Bezeichner des Control-Ereignisses in der Spalte Ereignis ein. Sie können die folgenden Attribute mit dem MaskedEdit-Steuerelement verwenden.



| attribute                                                          | Hexadezimales Bit                  | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Dies ist der Name einer indirekten Eigenschaft, die dem Steuerelement zugeordnet ist. Wenn das indirekte Attributbit festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft mit diesem Namen an oder ändert diesen. Wenn das indirekte Attributbit festgelegt ist, ist dieser Name auch der Wert der Eigenschaft, die in der Property -Spalte der [Steuertabelle aufgeführt ist.](control-table.md)                                                                                                                                   |
| [Position](position-control-attribute.md)                         |                                  | Position des Steuerelements im Dialogfeld. Geben Sie die Steuerelementbreite, -höhe und -koordinaten der linken Ecke des Steuerelements in die Spalten Width, Height, X und Y der [Steuertabelle ein.](control-table.md) Verwenden [Sie Installationseinheiten](installer-units.md) für Länge und Entfernung.<br/>                                                                                                                                                                                                            |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Dies ist der Name der Eigenschaft, die diesem Steuerelement zugeordnet ist. Wenn das indirekte Attributbit nicht festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft mit diesem Namen an oder ändert diesen. Dieses Attribut wird in der Spalte Eigenschaft der [Steuertabelle angegeben.](control-table.md)                                                                                                                                                                                                           |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Der aktuelle Wert der Eigenschaft, die von diesem Steuerelement angezeigt oder geändert wird. Wenn das indirekte Attributbit nicht festgelegt ist, ist dies der Wert von PropertyName. Wenn das indirekte Attributbit festgelegt ist, ist dies der Wert von IndirectPropertyName. Wenn sich das Attribut ändert, spiegelt das Steuerelement den neuen Wert wider.                                                                                                                                                                                                |
| [Text](text-control-attribute.md)                                 |                                  | Stellen Sie der Zeichenfolge der angezeigten Zeichen { style} oder {&style} voran, um die Schriftart und den \\ Schriftschnitt einer Textzeichenfolge zu setzen. Dabei ist style ein Bezeichner, der in der Spalte Style der [TextStyle-Tabelle aufgeführt ist.](textstyle-table.md) Wenn keines dieser Eigenschaften vorhanden ist, die [**DefaultUIFont-Eigenschaft**](defaultuifont.md) jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet. Die Zeichenfolge, die die Maskierungsvorlage angibt, folgt diesem Präfix und verwendet die zuvor in diesem Thema beschriebene Syntax. |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Ausgeblendetes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das Bitwort [](control-table.md) der Spalte Attribute in die Steuertabelle ein, um das Steuerelement beim Erstellen sichtbar oder ausgeblendet zu machen.<br/> Sie können ein Steuerelement auch mithilfe der [ControlCondition-Tabelle ausblenden oder anzeigen.](controlcondition-table.md)<br/>                                                                                                                                                                 |
| [Aktiviert](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Steuerelement in einem deaktivierten Zustand. Steuerelement in einem aktivierten Zustand.<br/> Fügen Sie dieses Bit in das Bitwort in die Spalte Attribute der [Steuertabelle](control-table.md) ein, um das Steuerelement bei der Erstellung zu aktivieren.<br/> Sie können ein Steuerelement auch mithilfe der [ControlCondition-Tabelle aktivieren oder deaktivieren.](controlcondition-table.md)<br/>                                                                                                                                                          |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Zeigt den standardmäßigen visuellen Stil an. Zeigt das Steuerelement mit einem versenkten 3D-Look an.<br/> Schließen Sie diese Bits in das Bitwort in die Spalte Attribute der [Steuertabelle ein.](control-table.md)<br/>                                                                                                                                                                                                                                                                                          |
| [Indirekt](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Das -Steuerelement zeigt den Wert der -Eigenschaft in der Property -Spalte der Steuertabelle an [oder ändert diesen.](control-table.md) Das -Steuerelement zeigt den Wert der Eigenschaft an, deren Bezeichner in der Spalte Eigenschaft der Steuertabelle aufgeführt ist, [oder ändert diesen.](control-table.md)<br/> Bestimmt, ob indirekt auf die Eigenschaft verwiesen wird, die diesem Steuerelement zugeordnet ist.<br/>                                                                                                 |



 

## <a name="remarks"></a>Hinweise

Das MaskedEdit-Steuerelement erstellt ein übergeordnetes Fenster der **BUTTON-Klasse** mit den Formaten **BS \_ OWNERDRAW** und **WS \_ EX \_ CONTROLPARENT.** In diesem Fenster werden mehrere untergeordnete Fenster erstellt.

-   Für konstante Textteile werden statische Fenster mit den **Formaten SS \_ LEFT** und **WS \_ CHILD** erstellt.
-   Für bearbeitbare Felder wird ein EDIT-Fenster mit den **Formaten WS \_ CHILD,** **WS \_ BORDER** und **WS \_ TABSTOP** erstellt.
-   Bei numerischen Feldern hat das Fenster auch das **ES \_ NUMBER-Format.**

Mit den Feldern "alternate digit", "%" und "alternate alphanumeric" (^, ?) und "alternate alphanumeric" können benutzerdefinierte Aktionen zwischen Feldern auf eine Weise unterscheiden, die durch die Maske gesteuert werden kann, z. B. ^ kann für Felder verwendet werden, die Großbuchstaben enthalten \` sollen.

 

 




