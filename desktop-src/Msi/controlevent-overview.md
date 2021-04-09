---
description: ControlEvents entsprechen Microsoft Windows-Meldungen in Win32-basierten Anwendungen.
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: ControlEvent (Übersicht)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92f8662a87bf9040b6a811fc170c25a5cf62ad7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868464"
---
# <a name="controlevent-overview"></a>ControlEvent (Übersicht)

ControlEvents entsprechen Microsoft Windows-Meldungen in Win32-basierten Anwendungen. Anstatt jedoch eine Rückruffunktion zu erstellen, um Windows-Meldungen zu empfangen und Windows-Meldungen mit der [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion zu senden, veröffentlichen die Benutzeroberflächen-Installationsprogramme und Steuerelemente die [ControlEvents](control-events.md). Andere Steuerelemente und das Installationsprogramm können angegeben werden, um bestimmte ControlEvents zu abonnieren, die dann die Attribute des abonnierenden Steuer Elements ändern. Zum Hinzufügen von Arbeits Steuerelementen zu Dialogfeldern gibt der Autor der Benutzeroberfläche die Veröffentlichung von ControlEvents in der [Tabelle ControlEvent](controlevent-table.md) an und abonniert Steuerelemente für ControlEvents in der [Tabelle EventMapping](eventmapping-table.md).

Das Installationsprogramm veröffentlicht die folgenden Ereignisse für Abonnierungs Steuerelemente, die in der [Tabelle EventMapping](eventmapping-table.md)aufgeführt sind. Ein [ProgressBar-Steuer](progressbar-control.md) Element oder ein [Billboard-Steuer](billboard-control.md) Element abonniert in der Regel setProgress. der Rest wird von [Text Steuerelementen](text-control.md)abonniert.

[Aktions Daten-ControlEvent](actiondata-controlevent.md)

[Action Text ControlEvent](actiontext-controlevent.md)

[SetProgress ControlEvent](setprogress-controlevent.md)

[Timeremainung ControlEvent](timeremaining-controlevent.md)

[Scriptinprogress ControlEvent](scriptinprogress-controlevent.md)

Die folgenden Ereignisse werden vom-Steuerelement veröffentlicht, wenn die Elementauswahl in einem [SelectionTree-Steuer](selectiontree-control.md) Element oder einem [directerylist-Steuer](directorylist-control.md)Element verschoben wird. Abonniere Steuerelemente müssen sich im gleichen Dialogfeld befinden und in der Tabelle EventMapping aufgeführt werden.

[Ignorechange ControlEvent](ignorechange-controlevent.md)

[Selectiondescription ControlEvent](selectiondescription-controlevent.md)

[Selectionsize-ControlEvent](selectionsize-controlevent.md)

[Selectionpath ControlEvent](selectionpath-controlevent.md)

[Selectionaction ControlEvent](selectionaction-controlevent.md)

[Selectionnoitems ControlEvent](selectionnoitems-controlevent.md)

Die folgenden ControlEvents können nach dem Ermessen eines Benutzers veröffentlicht werden, indem Sie mit einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element oder [CheckBox-Steuer](checkbox-control.md) Element in einem Dialogfeld interagieren. Das CheckBox-Steuerelement kann nur die Ereignisse ADDLOCAL, addsource, Remove, doaction und SetProperty veröffentlichen. Bei Windows Installer Versionen, die mit Windows Server 2003 und höher ausgeliefert wurden, kann das [SelectionTree-Steuer](selectiontree-control.md) Element die ControlEvents doaction, ControlEvent und SetProperty veröffentlichen. Der Autor der Benutzeroberfläche sollte das ControlEvent in der [ControlEvent-Tabelle](controlevent-table.md)auflisten. Der Benutzeroberflächen Handler des Installers ist der Abonnent dieser Ereignisse.

[ADDLOCAL-ControlEvent](addlocal-controlevent.md)

[Addsource-ControlEvent](addsource-controlevent.md)

[Checkexistingtargetpath ControlEvent](checkexistingtargetpath-controlevent.md)

[Checktargetpath ControlEvent](checktargetpath-controlevent.md)

[Doaction ControlEvent](doaction-controlevent.md)

[Enablerollback-ControlEvent](enablerollback-controlevent.md)

[EndDialog-ControlEvent](enddialog-controlevent.md)

[Newdialog-ControlEvent](newdialog-controlevent.md)

[ControlEvent neu installieren](reinstall-controlevent.md)

[REINSTALLMODE-ControlEvent](reinstallmode-controlevent.md)

[ControlEvent entfernen](remove-controlevent.md)

[ControlEvent zurücksetzen](reset-controlevent.md)

[Setinstalllevel ControlEvent](setinstalllevel-controlevent.md)

[SetProperty-ControlEvent](setproperty-controlevent.md)

[Settargetpath ControlEvent](settargetpath-controlevent.md)

[Spawndialog-ControlEvent](spawndialog-controlevent.md)

[Spawnwaitdialog ControlEvent](spawnwaitdialog-controlevent.md)

[ValidateProductID ControlEvent](validateproductid-controlevent.md)

Ein [PUSHBUTTON-Steuer](pushbutton-control.md) Element kann die folgenden Ereignisse in einem Abonnierung [SelectionTree-Steuer](selectiontree-control.md) Element oder [directerylist-Steuer](directorylist-control.md) Element veröffentlichen, das sich im gleichen Dialogfeld befindet. Das PUSHBUTTON-Steuerelement sollte in der Tabelle ControlEvent aufgeführt werden, und die Abonnierungs Steuerelemente sollten in der Tabelle EventMapping aufgeführt werden.

[Selectionbrowse-ControlEvent](selectionbrowse-controlevent.md)

[Director-listup-ControlEvent](directorylistup-controlevent.md)

[Director-listnew ControlEvent](directorylistnew-controlevent.md)

[Director-listopen ControlEvent](directorylistopen-controlevent.md)

Steuerungs Ereignisse erfordern im Allgemeinen, dass die Benutzeroberfläche auf der [*vollständigen Benutzeroberfläche*](f-gly.md) ausgeführt wird. Die meisten ControlEvents können nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegenden Benutzeroberfläche*](b-gly.md) verwendet werden, da auf diesen Ebenen nur modaldialogfelder angezeigt werden. Die Ereignisse "Aktions Text", "addsource", "setProgress", "timeremaineing" und "scriptinprogress" sind Ausnahmen und funktionieren in reduzierter oder grundlegender Benutzeroberfläche. Weitere Informationen zu UI-Ebenen finden Sie unter [Benutzeroberflächen](user-interface-levels.md)Ebenen.

Sie können [benutzerdefinierte Aktionen](custom-actions.md) ausführen, indem Sie ein ControlEvent über ein [PUSHBUTTON-Steuer](pushbutton-control.md) Element oder ein [CheckBox-Steuer](checkbox-control.md)Element veröffentlichen. Fügen Sie der [Tabelle ControlEvent](controlevent-table.md) einen Datensatz mit den Namen des Dialog Felds und dem Steuerelement hinzu, das ControlEvent veröffentlicht. Dieses Steuerelement sollte ein [doaction-ControlEvent](doaction-controlevent.md) veröffentlichen, das den Installer benachrichtigt, um die benutzerdefinierte Aktion auszuführen. Auf Systemen unter Windows XP oder früher können Sie eine benutzerdefinierte Aktion nicht ausführen, indem Sie ein ControlEvent von einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlichen.

Weitere Informationen zu bestimmten ControlEvents finden Sie in der Liste der standardmäßigen [ControlEvents](control-events.md) in der [Benutzeroberflächen Referenz](user-interface-reference.md).

 

 
