---
description: ControlEvents sind analog zu Microsoft Windows Nachrichten in Win32-basierten Anwendungen.
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: Übersicht über ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2736c93a728e2419f2ac9c722be2149e6e3ac681c95428f3383570262eb583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045140"
---
# <a name="controlevent-overview"></a>Übersicht über ControlEvent

ControlEvents sind analog zu Microsoft Windows Nachrichten in Win32-basierten Anwendungen. Anstatt jedoch eine Rückruffunktion zu erstellen, um Windows-Nachrichten zu empfangen und Windows-Nachrichten mit der [SendMessage-Funktion](/windows/win32/api/winuser/nf-winuser-sendmessage) zu senden, veröffentlichen das Installationsprogramm der Benutzeroberfläche (UI) und steuerelemente [ControlEvents](control-events.md). Andere Steuerelemente und das Installationsprogramm können angegeben werden, um bestimmte ControlEvents zu abonnieren, die dann die Attribute des abonnierenden Steuerelements ändern. Um Arbeitssteuerelemente zu Dialogfeldern hinzuzufügen, gibt der Autor der Benutzeroberfläche die Veröffentlichung von ControlEvents in der [ControlEvent-Tabelle](controlevent-table.md) an und abonniert Steuerelemente für ControlEvents in der [EventMapping-Tabelle.](eventmapping-table.md)

Das Installationsprogramm veröffentlicht die folgenden Ereignisse zum Abonnieren von Steuerelementen, die in der [EventMapping-Tabelle aufgeführt sind.](eventmapping-table.md) Ein [ProgressBar-Steuerelement](progressbar-control.md) oder [Ein -Steuerelement](billboard-control.md) abonniert in der Regel SetProgress, der Rest wird von [Text-Steuerelementen abonniert.](text-control.md)

[ActionData ControlEvent](actiondata-controlevent.md)

[ActionText ControlEvent](actiontext-controlevent.md)

[SetProgress ControlEvent](setprogress-controlevent.md)

[TimeRemaining ControlEvent](timeremaining-controlevent.md)

[ScriptInProgress ControlEvent](scriptinprogress-controlevent.md)

Die folgenden Ereignisse werden vom -Steuerelement veröffentlicht, wenn die Elementauswahl in ein [SelectionTree-Steuerelement](selectiontree-control.md) oder [ein DirectoryList-Steuerelement verschoben wird.](directorylist-control.md) Abonnierende Steuerelemente müssen sich im gleichen Dialogfeld befinden und in der Tabelle EventMapping aufgeführt sein.

[IgnoreChange ControlEvent](ignorechange-controlevent.md)

[SelectionDescription ControlEvent](selectiondescription-controlevent.md)

[SelectionSize ControlEvent](selectionsize-controlevent.md)

[SelectionPath ControlEvent](selectionpath-controlevent.md)

[SelectionAction ControlEvent](selectionaction-controlevent.md)

[SelectionNoItems ControlEvent](selectionnoitems-controlevent.md)

Die folgenden ControlEvents können nach Eigenem Ermessen eines Benutzers veröffentlicht werden, indem sie mit einem [PushButton-Steuerelement](pushbutton-control.md) oder [einem CheckBox-Steuerelement](checkbox-control.md) in einem Dialogfeld interagieren. Das Kontrollkästchen-Steuerelement kann nur die Ereignisse AddLocal, AddSource, Remove, DoAction und SetProperty veröffentlichen. Mit Windows Installer-Versionen, die im Lieferumfang von Windows Server 2003 und höher enthalten sind, kann das [SelectionTree-Steuerelement](selectiontree-control.md) die ControlEvents DoAction, ControlEvent und SetProperty veröffentlichen. Der Autor der Benutzeroberfläche sollte das ControlEvent in der [ControlEvent-Tabelle auflisten.](controlevent-table.md) Der Benutzeroberflächenhandler des Installationsprogramms ist der Abonnent dieser Ereignisse.

[AddLocal ControlEvent](addlocal-controlevent.md)

[AddSource ControlEvent](addsource-controlevent.md)

[CheckExistingTargetPath ControlEvent](checkexistingtargetpath-controlevent.md)

[CheckTargetPath ControlEvent](checktargetpath-controlevent.md)

[DoAction ControlEvent](doaction-controlevent.md)

[EnableRollback ControlEvent](enablerollback-controlevent.md)

[EndDialog ControlEvent](enddialog-controlevent.md)

[NewDialog ControlEvent](newdialog-controlevent.md)

[Installieren Sie ControlEvent neu.](reinstall-controlevent.md)

[ReinstallMode ControlEvent](reinstallmode-controlevent.md)

[ControlEvent entfernen](remove-controlevent.md)

[ControlEvent zurücksetzen](reset-controlevent.md)

[SetInstallLevel ControlEvent](setinstalllevel-controlevent.md)

[SetProperty ControlEvent](setproperty-controlevent.md)

[SetTargetPath ControlEvent](settargetpath-controlevent.md)

[SpawnDialog ControlEvent](spawndialog-controlevent.md)

[SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md)

[ValidateProductID ControlEvent](validateproductid-controlevent.md)

Ein [PushButton-Steuerelement](pushbutton-control.md) kann die folgenden Ereignisse in einem abonnierenden [SelectionTree-](selectiontree-control.md) oder [DirectoryList-Steuerelement](directorylist-control.md) veröffentlichen, das sich im gleichen Dialogfeld befindet. Das PushButton-Steuerelement sollte in der ControlEvent-Tabelle aufgeführt werden, und die abonnierenden Steuerelemente sollten in der EventMapping-Tabelle aufgeführt werden.

[SelectionBrowse ControlEvent](selectionbrowse-controlevent.md)

[DirectoryListUp ControlEvent](directorylistup-controlevent.md)

[DirectoryListNeues ControlEvent](directorylistnew-controlevent.md)

[DirectoryListOpen ControlEvent](directorylistopen-controlevent.md)

Steuerungsereignisse erfordern in der Regel, dass die Benutzeroberfläche auf der [*vollständigen Benutzeroberflächenebene ausgeführt*](f-gly.md) wird. Die meisten ControlEvents funktionieren [](r-gly.md) nicht [](b-gly.md) mit einer reduzierten Benutzeroberfläche oder einfachen Benutzeroberfläche, da diese Ebenen nur moduslose Dialogfelder anzeigen. Die Ereignisse ActionText, AddSource, SetProgress, TimeRemaining und ScriptInProgress sind Ausnahmen und funktionieren auf einer reduzierten oder einfachen Benutzeroberfläche. Weitere Informationen zu Benutzeroberflächenebenen finden Sie unter [Benutzeroberfläche Levels](user-interface-levels.md).

Sie können [benutzerdefinierte Aktionen ausführen,](custom-actions.md) indem Sie ein ControlEvent über ein [PushButton-Steuerelement](pushbutton-control.md) oder ein [Kontrollkästchen-Steuerelement veröffentlichen.](checkbox-control.md) Fügen Sie der [ControlEvent-Tabelle einen Datensatz mit](controlevent-table.md) den Namen des Dialogfelds und dem Steuerelement hinzu, das controlEvent veröffentlicht. Dieses Steuerelement sollte ein [DoAction ControlEvent veröffentlichen,](doaction-controlevent.md) das das Installationsprogramm benachrichtigt, um die benutzerdefinierte Aktion ausführen zu können. Auf Windows XP- oder früheren Systemen können Sie keine benutzerdefinierte Aktion ausführen, indem Sie ein ControlEvent aus einem [SelectionTree-Steuerelement veröffentlichen.](selectiontree-control.md)

Weitere Informationen zu bestimmten ControlEvents finden Sie in der Liste der [ControlEvents-Standardereignisse](control-events.md) in [Benutzeroberfläche Referenz.](user-interface-reference.md)

 

 
