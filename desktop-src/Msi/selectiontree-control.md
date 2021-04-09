---
description: Mit diesem Steuerelement kann ein Benutzer den Auswahl Status der in der Featuretabelle aufgeführten Features ändern.
ms.assetid: 0daf5b44-ba07-47f1-95d9-28c59f7cf985
title: SelectionTree-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5287736c3293c736d6d392ce8532b76ee7b62ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868836"
---
# <a name="selectiontree-control"></a>SelectionTree-Steuerelement

Mit diesem Steuerelement kann ein Benutzer den Auswahl Status der in der [Featuretabelle](feature-table.md)aufgeführten Features ändern. Das Steuerelement ist mit einer Zeichen folgen Wert Eigenschaft verknüpft, die der Benutzer durch das durch [Suchen-Dialog](browse-dialog.md)Feld festlegen kann. Sie können das Steuerelement einer Eigenschaft zuordnen, indem Sie den Namen der Eigenschaft in der Eigenschaften Spalte der [Steuerelement Tabelle](control-table.md)eingeben.

Das SelectionTree-Steuerelement veröffentlicht automatisch die folgenden [Steuerelement Ereignisse](control-events.md) unter Windows XP oder früheren Betriebssystemen. Das SelectionTree-Steuerelement veröffentlicht diese Ereignisse, wenn das ausgewählte Element von einem Knoten in einen anderen geändert wird. Wenn die Auswahl Struktur keine Knoten enthält, veröffentlicht das Steuerelement diese Ereignisse und löscht den Inhalt von Steuerelementen, die das Ereignis abonnieren. Diese ControlEvents müssen nicht in der [ControlEvent-Tabelle](controlevent-table.md)aufgeführt werden.



| Steuerungs Ereignis                                                 | BESCHREIBUNG                                                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Selectionaction](selectionaction-controlevent.md)           | Veröffentlicht eine Zeichenfolge aus der [UIText-Tabelle](uitext-table.md) , die das markierte Element beschreibt.      |
| [Selectionbrowse](selectionbrowse-controlevent.md)           | Generiert ein Dialogfeld zum Durchsuchen, mit dem der Pfad des hervorgehobenen Elements geändert wird.                     |
| [Selectiondescription](selectiondescription-controlevent.md) | Veröffentlicht eine Zeichenfolge aus der [Funktions Tabelle](feature-table.md) , in der das markierte Element beschrieben wird.    |
| [Selectionnoitems](selectionnoitems-controlevent.md)         | Löscht den beschreibenden Text oder deaktiviert die Schaltflächen eines veralteten Elements.                          |
| [Selectionpath](selectionpath-controlevent.md)               | Veröffentlicht den Pfad für das markierte Element.                                                       |
| [Selectionpathon](selectionpathon-controlevent.md)           | Veröffentlicht, ob dem aktuell ausgewählten Feature ein Auswahl Pfad zugeordnet ist. |
| [Selectionsize](selectionsize-controlevent.md)               | Veröffentlicht die Größe des hervorgehobenen Elements.                                                        |



 

Beginnend mit den Windows Server 2003-Systemen veröffentlichen SelectionTree-Steuerelemente alle Ereignisse in der obigen Tabelle und veröffentlichen außerdem eine [doaction ControlEvent](doaction-controlevent.md) -oder [SetProperty ControlEvent](setproperty-controlevent.md). Der [Tabelle "ControlEvent](controlevent-table.md) " müssen Datensätze hinzugefügt werden, um doaction-oder SetProperty-ControlEvents zu veröffentlichen.



| Steuerungs Ereignis                               | BESCHREIBUNG                                        |
|---------------------------------------------|----------------------------------------------------|
| [DoAction](doaction-controlevent.md)       | Benachrichtigt den Installer, eine benutzerdefinierte Aktion auszuführen. |
| [SetProperty](setproperty-controlevent.md) | Legt eine Eigenschaft auf einen neuen Wert fest.                    |



 

Ab Windows Installer Version 3,0 veröffentlichen SelectionTree-Steuerelemente ein Ereignis, das [benutzerdefinierte Aktionen](custom-actions.md) ausführt, die in der [ControlEvent-Tabelle](controlevent-table.md)aufgeführt sind. Das SelectionTree-Steuerelement veröffentlicht dieses Ereignis immer dann, wenn sich die Featureauswahl im Steuerelement ändert oder wenn ein anderer Auswahl Zustand für die aktuelle Funktion ausgewählt wird. Die benutzerdefinierten Aktionen werden jedes Mal ausgeführt, wenn das Ereignis veröffentlicht wird. Das SelectionTree-Steuerelement sendet Informationen an die benutzerdefinierte Aktion, indem die Werte der folgenden Eigenschaften festgelegt werden. Alle diese Eigenschaften werden alle gelöscht, wenn das SelectionTree-Steuerelement geschlossen wird.

**Windows Installer 2,0:** Nicht unterstützt. Das SelectionTree-Steuerelement veröffentlicht das Ereignis nicht und legt die folgenden Eigenschaften nicht fest.



| Eigenschaft                                | BESCHREIBUNG                                                                                                                                                      |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Msiselectiontreeselectedfeature         | Der Name der ausgewählten Funktion im Funktionsfeld der [Funktions Tabelle](feature-table.md).                                                                      |
| Msiselectiontreeselectedaction          | Der Installations Aktions Status der ausgewählten Funktion. Der Wert ist möglicherweise "InstallState \_ Missing", "InstallState \_ local", "InstallState \_ Source" oder "InstallState" \_ angekündigt. |
| Msiselectontreechildren-Anzahl            | Anzahl der direkt untergeordneten Knoten.                                                                                                                                    |
| Msiselectiontreeinstallingchildren encount | Anzahl direkter untergeordneter Knoten, bei denen InstallState \_ local, InstallState \_ Source oder InstallState \_ angekündigt ist.                                                    |
| Msiselectiontreeselectedcost            | Kosten für die Installation der ausgewählten Funktion in Einheiten von 512 Byte.                                                                                                   |
| Msiselectiontreechildren encost            | Kosten für die Installation aller untergeordneten Funktionen in Einheiten von 512 Byte.                                                                                              |
| Msiselectiontreeselectedpath            | Der Pfad, in dem das ausgewählte Feature installiert wird. Nur definiert, wenn die Funktion als "InstallState local" installiert wird \_ .                                       |



 

> [!Note]
>
> Der Inhalt des Textfelds der Steuerelement [Tabelle](control-table.md) wird nie durch das SelectionTree-Steuerelement angezeigt. Stattdessen gibt dieses Feld den Text Stil an, der vom Steuerelement angezeigt wird, und enthält eine Beschreibung des Steuer Elements, das von den Hilfsprogrammen für die Bildschirm Überprüfung verwendet wird. Um die Schriftart und den Schrift Schnitt einer Text Zeichenfolge festzulegen, stellen Sie die Zeichenfolge der angezeigten Zeichen mit "{ \\ Style}" oder "{&*Style*}" vor. Dabei ist Style ein Bezeichner, der in der TextStyle-Spalte der [TextStyle-Tabelle](textstyle-table.md)aufgeführt ist. Wenn keines dieser beiden vorhanden ist, die [**defaultuifont**](defaultuifont.md) -Eigenschaft jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet. Die folgenden Informationen werden von den Hilfsprogrammen der Bildschirm Überprüfung als Beschreibung des Steuer Elements gelesen. Siehe [Barrierefreiheit](accessibility.md).

 

## <a name="control-attributes"></a>Steuerelement Attribute

Mit diesem Steuerelement können Sie die folgenden Attribute verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement einem ControlEvent in der [EventMapping-Tabelle](eventmapping-table.md) , und Listen Sie den Bezeichner des Attributs in der Attribut-Spalte auf. Geben Sie den Bezeichner des ControlEvent in der Ereignis Spalte ein.



| Attribut Bezeichner                                               | Hexadezimales Bit                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Derekpropertyname](indirectpropertyname-control-attribute.md) |                                  | Der Name einer indirekten Eigenschaft, die dem Steuerelement zugeordnet ist. Wenn das indirekte Attribut Bit festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft mit diesem Namen an oder ändert ihn. Wenn das indirekte Attribut Bit festgelegt ist, ist dieser Name auch der Wert der Eigenschaft, die in der Eigenschafts Spalte der [Steuerelement Tabelle](control-table.md)aufgeführt ist.                                    |
| [Position](position-control-attribute.md)                         |                                  | Position des-Steuer Elements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der Steuerelemente der linken Ecke des Steuer Elements in die Spalten Width, Height, X und Y der [Steuerelement Tabelle](control-table.md)ein. Verwenden Sie die [Installer-Einheiten](installer-units.md) für Länge und Entfernung.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Der Name der Eigenschaft, die diesem Steuerelement zugeordnet ist. Wenn das indirekte Attribut Bit nicht festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft mit diesem Namen an oder ändert ihn. Dieses Attribut wird in der-Eigenschaften Spalte der [Steuerelement Tabelle](control-table.md)angegeben.                                                                                                    |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Aktueller Wert der Eigenschaft, die von diesem Steuerelement angezeigt oder geändert wird. Wenn das indirekte Attribut Bit nicht festgelegt ist, ist dies der Wert von PropertyName. Wenn das indirekte Attribut Bit festgelegt ist, ist dies der Wert von deretpropertyname. Wenn sich das Attribut ändert, spiegelt das-Steuerelement den neuen Wert wider.                                                                           |
| [Text](text-control-attribute.md)                                 |                                  | Zeigt Text in Screenreader gemäß dem Text an, der in die Text-Spalte der [Steuerelement Tabelle](control-table.md)eingegeben wurde. Siehe [Barrierefreiheit](accessibility.md).                                                                                                                                                                                                          |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Verborgenes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das bitwort der Attributspalte in der [Steuerelement Tabelle](control-table.md) ein, damit das Steuerelement bei der Erstellung sichtbar oder ausgeblendet wird.<br/> Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" ausblenden oder anzeigen.<br/>                                     |
| [Aktiviert](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Steuerelement in deaktiviertem Zustand. Steuerelement im aktivierten Zustand.<br/> Fügen Sie dieses Bit in das bitwort in die Spalte Attribute des [Steuer](control-table.md) Elements ein, um das Steuerelement bei der Erstellung zu aktivieren.<br/> Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" aktivieren oder deaktivieren.<br/>                                   |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Zeigt den visuellen Standardstil an. Zeigt das Steuerelement mit einem abgesenkten 3D-Bild an.<br/> Fügen Sie diese Bits in das bitwort in die Spalte Attribute der [Steuerelement Tabelle](control-table.md)ein.<br/>                                                                                                                                                             |
| [Indirekt](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Das-Steuerelement zeigt den Wert der-Eigenschaft in der-Eigenschaften Spalte der [Steuerelement Tabelle](control-table.md)an oder ändert ihn. Das-Steuerelement zeigt den Wert der-Eigenschaft an oder ändert den Wert der-Eigenschaft, die den Bezeichner enthält<br/> Bestimmt, ob indirekt auf die diesem Steuerelement zugeordnete Eigenschaft verwiesen wird.<br/> |
| [Rtlro](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | Der Text im Steuerelement wird in der Lesefolge von links nach rechts angezeigt. Der Text im Steuerelement wird in der Lesefolge von rechts nach links angezeigt.<br/>                                                                                                                                                                                                                              |
| [Rechtsbündig](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | Der Text im-Steuerelement wird linksbündig ausgerichtet. Der Text im-Steuerelement wird rechtsbündig ausgerichtet.<br/>                                                                                                                                                                                                                                                                       |
| [Leftscroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | Die Scrollleiste befindet sich auf der rechten Seite des-Steuer Elements. Die Scrollleiste befindet sich auf der linken Seite des-Steuer Elements.<br/>                                                                                                                                                                                                                                         |
| [Bidi](bidi-control-attribute.md)                                 | 0x000000e0                       | Legen Sie diesen Wert für eine Kombination der Attribute [rtlro](rtlro-control-attribute.md), [rightausgerichtete](rightaligned-control-attribute.md)und [leftscroll](leftscroll-control-attribute.md) fest.                                                                                                                                                                          |



 

## <a name="remarks"></a>Bemerkungen

Dieses Steuerelement kann \_ mithilfe der Funktion "up- [**windowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " aus der Klasse "WC TreeView" erstellt werden. Es verfügt über den WS-Rahmen, die **Fernseh- \_ haslines**, die **Fernseh- \_ hasschaltflächen**, den TVs- **\_ linesAtRoot**, den **TVs \_ disabledragdrop**-, den **TV- \_ showselalways**-, **den WS \_** **\_ Child**-, **WS \_ Tabstopps**-und **\_**

Die Auswahl Struktur wird nur aufgefüllt, wenn die Aktion " [costinitialize](costinitialize-action.md) " und die [Aktion "costfinalize](costfinalize-action.md) " aufgerufen wurden.

Die folgende Zeichenfolge in der [UIText-Tabelle](uitext-table.md) bezieht sich auf dieses Steuerelement.



| Begriff                                                                                                         | BESCHREIBUNG                                                    |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="AbsentPath"></span><span id="absentpath"></span><span id="ABSENTPATH"></span>Absentpath<br/> | Der Pfad, der für ein Element im nicht vorhandenen Zustand angezeigt wird.<br/> |



 

Die folgenden sechs Zeichen folgen werden verwendet, um die Anzahl der ausgewählten untergeordneten Elemente und die Größe anzuzeigen, die dem markierten Element zugeordnet ist:

-   Selchildcostpos
-   Selchildcostnetg
-   Selparser-costpospos
-   Selparser-costposneg
-   Selparser-costnegpos
-   Selparameentcostnegneg

Die folgenden Zeichen folgen werden verwendet, um die verfügbaren Auswahl Optionen für ein Element in einem Popupmenü anzuzeigen:

-   Menumissing
-   Menulocal
-   Menucd
-   Menunetwork
-   Menualllocal
-   Menuallcd
-   Menuallnetwork

Die folgenden Zeichen folgen werden verwendet, um die aktuelle Auswahl in der [selectiondescription](selectiondescription-controlevent.md) -ControlEvent zu erläutern.

-   Selabsentmissing
-   Selabsentlocal
-   Selabsentcd
-   Selabsentnetwork
-   Sellocalmissing
-   Selloczuweisung
-   Sellocalcd
-   Sellocalnetwork
-   Selcdabgesendet
-   Selnetworkmissing
-   Selcdlocal
-   Selnetworklocal
-   Selcdcd
-   Selnetworknetwork

Die folgenden vier lokalisierten Zeichen folgen werden zum Formatieren der Größe einer Datei verwendet:

-   Byte
-   KB
-   MB
-   GB

 

 
