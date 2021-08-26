---
description: Mit diesem Steuerelement kann ein Benutzer den Auswahlzustand der in der Tabelle Feature aufgeführten Features ändern.
ms.assetid: 0daf5b44-ba07-47f1-95d9-28c59f7cf985
title: SelectionTree-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 894a7d90829172c29a6f1df1ffc4139cc0bf6c540bd49193c3cc2f3a396891ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040350"
---
# <a name="selectiontree-control"></a>SelectionTree-Steuerelement

Mit diesem Steuerelement kann ein Benutzer den Auswahlstatus der in der [Featuretabelle](feature-table.md)aufgeführten Features ändern. Das -Steuerelement ist einer Zeichenfolgenwerteigenschaft zugeordnet, die der Benutzer über das [Dialogfeld Durchsuchen](browse-dialog.md)festlegen kann. Sie können das Steuerelement einer Eigenschaft zuordnen, indem Sie den Namen der Eigenschaft in der Property -Spalte der [Control-Tabelle](control-table.md)eingeben.

Das SelectionTree-Steuerelement veröffentlicht automatisch die folgenden [Steuerelementereignisse](control-events.md) auf Windows XP oder früheren Betriebssystemen. Das SelectionTree-Steuerelement veröffentlicht diese Ereignisse, wenn das ausgewählte Element von einem Knoten auf einen anderen geändert wird. Wenn die Auswahlstruktur keine Knoten enthält, veröffentlicht das Steuerelement diese Ereignisse und löscht den Inhalt der Steuerelemente, die das Ereignis abonnieren. Diese ControlEvents müssen nicht in der [ControlEvent-Tabelle](controlevent-table.md)aufgeführt werden.



| Steuerungsereignis                                                 | BESCHREIBUNG                                                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [SelectionAction](selectionaction-controlevent.md)           | Veröffentlicht eine Zeichenfolge aus der [UIText-Tabelle,](uitext-table.md) die das hervorgehobene Element beschreibt.      |
| [SelectionBrowse](selectionbrowse-controlevent.md)           | Generiert ein Dialogfeld Durchsuchen, in dem der Pfad des hervorgehobenen Elements geändert wird.                     |
| [SelectionDescription](selectiondescription-controlevent.md) | Veröffentlicht eine Zeichenfolge aus der [Featuretabelle,](feature-table.md) die das hervorgehobene Element beschreibt.    |
| [SelectionNoItems](selectionnoitems-controlevent.md)         | Löscht den beschreibenden Text oder deaktiviert die Schaltflächen eines veralteten Elements.                          |
| [SelectionPath](selectionpath-controlevent.md)               | Veröffentlicht den Pfad für das hervorgehobene Element.                                                       |
| [SelectionPathOn](selectionpathon-controlevent.md)           | Veröffentlicht, ob dem aktuell ausgewählten Feature ein Auswahlpfad zugeordnet ist. |
| [SelectionSize](selectionsize-controlevent.md)               | Veröffentlicht die Größe des hervorgehobenen Elements.                                                        |



 

Ab den Windows Server 2003-Systemen veröffentlichen SelectionTree-Steuerelemente alle Ereignisse in der obigen Tabelle und veröffentlichen zusätzlich ein [DoAction ControlEvent](doaction-controlevent.md) oder ein [SetProperty ControlEvent.](setproperty-controlevent.md) Datensätze müssen der [ControlEvent-Tabelle](controlevent-table.md) hinzugefügt werden, um DoAction oder SetProperty ControlEvents zu veröffentlichen.



| Steuerungsereignis                               | BESCHREIBUNG                                        |
|---------------------------------------------|----------------------------------------------------|
| [DoAction](doaction-controlevent.md)       | Benachrichtigt das Installationsprogramm, eine benutzerdefinierte Aktion auszuführen. |
| [SetProperty](setproperty-controlevent.md) | Legt eine Eigenschaft auf einen neuen Wert fest.                    |



 

Ab Windows Installer Version 3.0 veröffentlichen SelectionTree-Steuerelemente ein Ereignis, das [benutzerdefinierte Aktionen](custom-actions.md) ausführt, die in der [ControlEvent-Tabelle](controlevent-table.md)aufgeführt sind. Das SelectionTree-Steuerelement veröffentlicht dieses Ereignis immer dann, wenn sich die Funktionsauswahl im Steuerelement ändert oder wenn ein anderer Auswahlzustand für das aktuelle Feature ausgewählt wird. Die benutzerdefinierten Aktionen werden jedes Mal ausgeführt, wenn das Ereignis veröffentlicht wird. Das SelectionTree-Steuerelement sendet Informationen an die benutzerdefinierte Aktion, indem die Werte der folgenden Eigenschaften festgelegt werden. Alle diese Eigenschaften werden gelöscht, wenn das SelectionTree-Steuerelement geschlossen wird.

**Windows Installer 2.0:** Wird nicht unterstützt. Das SelectionTree-Steuerelement veröffentlicht das Ereignis nicht und legt die folgenden Eigenschaften nicht fest.



| Eigenschaft                                | BESCHREIBUNG                                                                                                                                                      |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MsiSelectionTreeSelectedFeature         | Der Name des ausgewählten Features im Feld Feature der [Tabelle Feature](feature-table.md).                                                                      |
| MsiSelectionTreeSelectedAction          | Der Installationsaktionsstatus des ausgewählten Features. Der Wert kann INSTALLSTATE \_ ABSENT, INSTALLSTATE \_ LOCAL, INSTALLSTATE \_ SOURCE oder INSTALLSTATE \_ ADVERTISED sein. |
| MsiSelectonTreeChildrenCount            | Anzahl der direkten untergeordneten Knoten.                                                                                                                                    |
| MsiSelectionTreeInstallingChildrenCount | Anzahl der direkten untergeordneten Knoten, die INSTALLSTATE \_ LOCAL, INSTALLSTATE \_ SOURCE oder INSTALLSTATE \_ ADVERTISED sind.                                                    |
| MsiSelectionTreeSelectedCost            | Kosten für die Installation des ausgewählten Features in Einheiten von 512 Byte.                                                                                                   |
| MsiSelectionTreeChildrenCost            | Kosten für die Installation aller untergeordneten Features in Einheiten von 512 Byte.                                                                                              |
| MsiSelectionTreeSelectedPath            | Pfad, unter dem das ausgewählte Feature installiert wird. Wird nur definiert, wenn das Feature als INSTALLSTATE LOCAL installiert \_ wird.                                       |



 

> [!Note]
>
> Der Inhalt des Felds Text der [Control-Tabelle](control-table.md) wird nie vom SelectionTree-Steuerelement angezeigt. Stattdessen gibt dieses Feld den Textstil an, der vom Steuerelement angezeigt werden soll, und enthält eine Beschreibung des Steuerelements, das von Bildschirmüberprüfungs-Hilfsprogrammen verwendet wird. Um die Schriftart und den Schriftschnitt einer Textzeichenfolge festzulegen, stellen Sie der Zeichenfolge der angezeigten Zeichen { \\ style} oder {&*Format*} voran. Wobei style ein Bezeichner ist, der in der TextStyle-Spalte der [TextStyle-Tabelle](textstyle-table.md)aufgeführt ist. Wenn keines davon vorhanden ist, die [**DefaultUIFont-Eigenschaft**](defaultuifont.md) jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet. Die folgenden Informationen werden von Bildschirmüberprüfungs-Hilfsprogrammen als Beschreibung des Steuerelements gelesen. Weitere Informationen finden Sie [unter Barrierefreiheit.](accessibility.md)

 

## <a name="control-attributes"></a>Steuerelementattribute

Sie können die folgenden Attribute mit diesem Steuerelement verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement für ein ControlEvent in der [EventMapping-Tabelle,](eventmapping-table.md) und listen Sie den Bezeichner des Attributs in der Spalte Attribute auf. Geben Sie den Bezeichner des ControlEvent in der Spalte Ereignis ein.



| Attributbezeichner                                               | Hexadezimalbit                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Name einer indirekten Eigenschaft, die dem Steuerelement zugeordnet ist. Wenn das Indirekte Attributbit festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft mit diesem Namen an oder ändert diesen. Wenn das Indirekte Attributbit festgelegt ist, ist dieser Name auch der Wert der Eigenschaft, die in der Property -Spalte der [Control-Tabelle](control-table.md)aufgeführt ist.                                    |
| [Position](position-control-attribute.md)                         |                                  | Position des Steuerelements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der linken Ecke des Steuerelements in die Spalten Width, Height, X und Y der [Control-Tabelle](control-table.md)ein. Verwenden Sie [Installationseinheiten](installer-units.md) für Länge und Entfernung.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Name der Eigenschaft, die diesem Steuerelement zugeordnet ist. Wenn das Indirekte Attributbit nicht festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft mit diesem Namen an oder ändert diesen. Dieses Attribut wird in der Property -Spalte der [Control-Tabelle](control-table.md)angegeben.                                                                                                    |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Aktueller Wert der Eigenschaft, die von diesem Steuerelement angezeigt oder geändert wird. Wenn das Indirekte Attributbit nicht festgelegt ist, ist dies der Wert von PropertyName. Wenn das Indirekte Attributbit festgelegt ist, ist dies der Wert von IndirectPropertyName. Wenn sich das Attribut ändert, spiegelt das Steuerelement den neuen Wert wider.                                                                           |
| [Text](text-control-attribute.md)                                 |                                  | Zeigt Text in Screenreadern entsprechend dem Text an, der in die Text -Spalte der [Control-Tabelle](control-table.md)eingegeben wurde. Weitere Informationen finden Sie [unter Barrierefreiheit.](accessibility.md)                                                                                                                                                                                                          |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Ausgeblendetes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das Bitwort der Attributes -Spalte in die [Control-Tabelle](control-table.md) ein, um das Steuerelement beim Erstellen sichtbar oder ausgeblendet zu machen.<br/> Sie können ein Steuerelement auch mithilfe der [ControlCondition-Tabelle](controlcondition-table.md)ausblenden oder anzeigen.<br/>                                     |
| [Aktiviert](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Steuerelement in einem deaktivierten Zustand. Steuerelement in einem aktivierten Zustand.<br/> Fügen Sie dieses Bit in das Bitwort in die Spalte Attribute des [Steuerelements](control-table.md) ein, um das Steuerelement bei der Erstellung zu aktivieren.<br/> Sie können ein Steuerelement auch mithilfe der [ControlCondition-Tabelle aktivieren oder deaktivieren.](controlcondition-table.md)<br/>                                   |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Zeigt den standardmäßigen visuellen Stil an. Zeigt das Steuerelement mit einem versenkten 3D-Look an.<br/> Schließen Sie diese Bits in das Bitwort in die Spalte Attribute der [Control-Tabelle ein.](control-table.md)<br/>                                                                                                                                                             |
| [Indirekt](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Das -Steuerelement zeigt den Wert der -Eigenschaft in der Property -Spalte der [Control-Tabelle](control-table.md)an oder ändert diesen. Das -Steuerelement zeigt den Wert der Eigenschaft an, in der der Bezeichner in der Spalte Eigenschaft der Control-Tabelle aufgeführt ist, oder ändert diesen.<br/> Bestimmt, ob indirekt auf die diesem Steuerelement zugeordnete Eigenschaft verwiesen wird.<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | Text im Steuerelement wird in der Lese reihenfolge von links nach rechts angezeigt. Text im Steuerelement wird in der Lese reihenfolge von rechts nach links angezeigt.<br/>                                                                                                                                                                                                                              |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | Text im Steuerelement wird linksbündig ausgerichtet. Text im Steuerelement wird rechtsbündig ausgerichtet.<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | Die Scrollleiste befindet sich auf der rechten Seite des Steuerelements. Die Scrollleiste befindet sich auf der linken Seite des Steuerelements.<br/>                                                                                                                                                                                                                                         |
| [Bidi](bidi-control-attribute.md)                                 | 0x000000E0                       | Legen Sie diesen Wert für eine Kombination der [Attribute RTLRO,](rtlro-control-attribute.md) [RightAligned](rightaligned-control-attribute.md)und [LeftScroll](leftscroll-control-attribute.md) fest.                                                                                                                                                                          |



 

## <a name="remarks"></a>Hinweise

Dieses Steuerelement kann mithilfe der CreateWindowEx-Funktion aus der WC \_ [**TREEVIEW-Klasse erstellt**](/windows/win32/api/winuser/nf-winuser-createwindowexa) werden. Sie verfügt über die Formate **WS \_ BORDER,** **TVS \_ HASLINES,** **\_ TVS HASBUTTONS,** **\_ TVS LINESATROOT, TVS** **\_ DISABLEDRAGDROP,** **TVS \_ SHOWSELALWAYS,** **WS \_ CHILD,** **WS \_ TABSTOP** und **WS \_ GROUP.**

Die Auswahlstruktur wird nur aufgefüllt, wenn die [Aktion CostInitialize](costinitialize-action.md) und [die Aktion CostFinalize](costfinalize-action.md) aufgerufen wurden.

Die folgende Zeichenfolge in der [UIText-Tabelle](uitext-table.md) bezieht sich auf dieses Steuerelement.



| Begriff                                                                                                         | BESCHREIBUNG                                                    |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="AbsentPath"></span><span id="absentpath"></span><span id="ABSENTPATH"></span>AbsentPath<br/> | Der Pfad, der für ein Element im fehlenden Zustand angezeigt wird.<br/> |



 

Die folgenden sechs Zeichenfolgen werden verwendet, um die Anzahl der ausgewählten unteren Elemente und die dem hervorgehobenen Element zugeordnete Größe anzuzeigen:

-   SelChildCostPos
-   SelChildCostNeg
-   SelParentCostPosPos
-   SelParentCostPosNeg
-   SelParentCostNegPos
-   SelParentCostNegNeg

Die folgenden Zeichenfolgen werden verwendet, um die verfügbaren Auswahloptionen für ein Element in einem Popupmenü anzuzeigen:

-   MenuAbsent
-   MenuLocal
-   MenuCD
-   MenuNetwork
-   MenuAllLocal
-   MenuAllCD
-   MenuAllNetwork

Die folgenden Zeichenfolgen werden verwendet, um die aktuelle Auswahl im [SelectionDescription](selectiondescription-controlevent.md) ControlEvent zu erläutern.

-   SelAbsentAbsent
-   SelAbsentLocal
-   SelAbsentCD
-   SelAbsentNetwork
-   SelLocalAbsent
-   SelLocalLocal
-   SelLocalCD
-   SelLocalNetwork
-   SelCDAbsent
-   SelNetworkAbsent
-   SelCDLocal
-   SelNetworkLocal
-   SelCDCD
-   SelNetworkNetwork

Die folgenden vier lokalisierten Zeichenfolgen werden zum Formatieren der Größe einer Datei verwendet:

-   Byte
-   KB
-   MB
-   GB

 

 
