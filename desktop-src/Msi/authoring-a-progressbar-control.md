---
description: Windows Installer enthält Funktionen zum Anzeigen einer Statusanzeige in einem Aktions Anzeige Dialogfeld.
ms.assetid: cfc2d974-4f2d-4f52-9835-eab1dc091c9b
title: Erstellen eines ProgressBar-Steuer Elements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b872ed2dd36fb8ed04ee48fd69e4680fce002a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864459"
---
# <a name="authoring-a-progressbar-control"></a>Erstellen eines ProgressBar-Steuer Elements

Windows Installer enthält Funktionen zum Anzeigen einer Statusanzeige in einem Aktions Anzeige Dialogfeld. Das [ProgressBar-Steuer](progressbar-control.md) Element stellt die Installation einzelner Komponenten grafisch dar und meldet entweder die insgesamt verstrichene Zeit relativ zur verbleibenden Zeit oder die ungefähre gesamte Zeit, die bis zum Abschluss der Installation verbleiben.

Um die Gesamtzeit zu bestimmen, die für die Installation geplant ist, verfolgt das Installationsprogramm die gesamten Status Ticks, die von den einzelnen Aktionen während der Generierung des Ausführungs Skripts erwartet werden. Wenn die Skript Generierung abgeschlossen ist, wird der Status Tick Total (Gesamtwert) gespeichert, und die Installation beginnt.

Fortschrittsmeldungen mit der verstrichenen Anzahl von Status Ticks werden an den aktiven Nachrichten Handler gesendet, wenn jede Aktion im Skript ausgeführt wird. Bei jeder Statusmeldung überträgt das Installationsprogramm einen [setProgress-ControlEvent](setprogress-controlevent.md) an das momentan aktive Dialogfeld. Die UI-Sequenz sollte erstellt werden, um das Dialogfeld Aktions Anzeige während der Skriptausführung zu erstellen, um die setProgress ControlEvent-Meldungen vom Installationsprogramm zu empfangen.

Wenn das Dialogfeld Aktions Anzeige ein setProgress ControlEvent empfängt, überprüft es die [EventMapping-Tabelle](eventmapping-table.md) auf alle Steuerelemente, die das ControlEvent-Element abonniert haben. Das ProgressBar-Steuerelement im Dialogfeld Aktions Anzeige wird mit dem in der Spalte Attribute angegebenen Attribut für die Fortschritts Steuerung abonniert. Das Progress Control-Attribut gibt an, dass das ProgressBar-Steuerelement zusammen mit dem setProgress ControlEvent die Werte "tickssofar" und "totalticks" übergeben wird. Das Statusanzeige-Steuerelement verwendet diese Informationen, um die grafische Leiste von links nach rechts für eine-Installation und von rechts nach Links für einen [Rollback](rollback-installation.md) -Vorgang zu verschieben.

Außerdem überträgt das Installationsprogramm für jede Statusmeldung ein [timeremainung-ControlEvent](timeremaining-controlevent.md) . Die gesamte verbleibende Zeit für die Installation wird durch die erste Berechnung der Ausführungsrate bestimmt, d. h. die Gesamtanzahl der verstrichenen Ticks, dividiert durch die Gesamtzeit seit Beginn der Installation. Die verbleibenden Ticks, die durch die Ausführungsrate geteilt werden, geben die ungefähre verbleibende Zeit an.

Wenn das Dialogfeld Aktions Anzeige das timeremaindingcontrolevent empfängt, sucht es erneut in der Tabelle EventMapping nach den abonnierenden Steuerelementen. Um die verbleibende Zeit anzuzeigen, muss ein [Text Steuer](text-control.md) Element für das timeremainingcontrolevent-Steuerelement mit dem [timeremainung-Steuer](timeremaining-control-attribute.md) Element, das in der Attribut Spalte angegeben ist, abonniert werden.

Das abonnierte Text Steuerelement fragt die [UIText-Tabelle](uitext-table.md) nach einer parametrisierten Vorlagen Zeichenfolge mit dem Namen "timeremainung" ab. Diese Zeichenfolge hat zwei Parameter: \[ 1 \] für Minuten und \[ 2 \] für Sekunden. Das Text Steuerelement konvertiert jeden Wert in Minuten und Sekunden, wertet die timeremainung-Vorlagen Zeichenfolge aus und aktualisiert das Text Steuerelement mit den neuen Informationen.

Wenn die Anzeige Ebene für die Benutzeroberfläche auf Basic oder niedriger festgelegt ist, zeigt das Installationsprogramm ein Standard Dialogfeld an, das eine Statusanzeige und ein timeremainung-Textfeld enthält. Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

 

 



