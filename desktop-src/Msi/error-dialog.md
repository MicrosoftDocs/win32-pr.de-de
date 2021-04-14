---
description: Ein Fehler Dialogfeld ist ein modales Dialogfeld Feld, in dem eine Fehlermeldung angezeigt wird. In jeder Installation kann mehr als ein Fehler Dialogfeld vorhanden sein.
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: Fehler Dialogfeld
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a153f5e6ee38235f830937d794a9ca9b81314583
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527251"
---
# <a name="error-dialog"></a>Fehler Dialogfeld

Ein Fehler Dialogfeld ist ein modales Dialogfeld Feld, in dem eine Fehlermeldung angezeigt wird. In jeder Installation kann mehr als ein Fehler Dialogfeld vorhanden sein.

Eine ErrorDialog-Eigenschaft muss festgelegt werden, die angibt, welches Dialogfeld verwendet werden soll. Wenn diese Eigenschaft nicht festgelegt ist oder nicht auf ein gültiges Fehler Dialogfeld zeigt, werden die Fehlermeldungen nicht angezeigt. In diesem Fall wird der Fehler nur mit einer Warnung über das fehlende Dialogfeld protokolliert.

Für ein Fehler Dialogfeld muss das [Fehler Dialogfeld des Dialog](error-dialog-style-bit.md) Felds festgelegt sein. Das Dialogfeld muss über ein [Text Steuer](text-control.md) Element namens ErrorText verfügen. Der Datensatz für das Fehler Dialogfeld in der [Dialogfeld Tabelle](dialog-table.md) muss das ErrorText-Steuerelement in das erste Feld des Steuer Elements eingegeben haben \_ .

Das Dialogfeld muss sieben [Pushbuttons](pushbutton-control.md)enthalten. Alle diese Schaltflächen geben das [EndDialog](enddialog-controlevent.md) -ControlEvent in der [ControlEvent-Tabelle](controlevent-table.md)an. Jede Schaltfläche gibt eines der folgenden Attribute an: **errorabort**, **errorcancel**, **errorignore**, **errorno**, **errorok**, **errorretry**, **erroryes**.

> [!Note]  
> Der Fokus dieser Steuerelemente sollte nicht durch die Verwendung der nächsten Spalte des Steuer Elements \_ in der [Steuerelement Tabelle](control-table.md)verknüpft werden.

 

Diese Schaltflächen sollten in etwa der gleichen Position im Dialogfeld platziert werden, da bei der Erstellung nur eine Teilmenge dieser sieben Schaltflächen erstellt wird, abhängig von der Nachricht. Die X-Koordinate der Schaltflächen wird so geändert, dass die angezeigten Schaltflächen gleichmäßig verteilt sind. Die Y-Koordinate, die Höhe und die Breite der Schaltflächen sind unverändert. Da die Schaltflächen horizontal angeordnet werden, kann kein anderes Steuerelement im selben horizontalen Bereich des Dialog Felds platziert werden.

Wenn ein Fehler Dialogfeld angezeigt wird, werden die Felder Steuerelement \_ Standard und Steuerelement \_ Abbruch in der [Dialogfeld Tabelle](dialog-table.md) ignoriert. Das Steuerelement \_ First-Feld für ein Fehler Dialogfeld muss das ErrorText-Steuerelement angeben.

Wenn in diesem Dialogfeld ein [Symbol Steuer](icon-control.md) Element mit dem Namen erroricon enthalten ist, werden die folgenden standardmäßigen Windows-Symbole angezeigt:

-   IDI- \_ Fehler als Antwort auf imtfatalexit-Nachrichten.
-   IDI \_ -Warnung als Reaktion auf imterror-und imtwarning-Meldungen.
-   IDI- \_ Informationen als Reaktion auf imtoutofdiskspace-Nachrichten.

Das erroricon-Steuerelement sollte mit dem [FixedSize-Steuer](fixedsize-control-attribute.md) Element festgelegt werden, um eine nicht ordnungsgemäße Anpassung der standardmäßigen Windows-Symbole zu vermeiden.

 

 



