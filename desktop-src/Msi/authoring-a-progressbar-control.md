---
description: Windows Das Installationsprogramm enthält Funktionen zum Anzeigen einer Statusanzeige in einem Aktionsanzeigedialogfeld.
ms.assetid: cfc2d974-4f2d-4f52-9835-eab1dc091c9b
title: Erstellen eines ProgressBar-Steuerelements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1074744220bde8734fe0cd1f65aa1037ff1f0cb26763a11845a7ea7f1b58e507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066160"
---
# <a name="authoring-a-progressbar-control"></a>Erstellen eines ProgressBar-Steuerelements

Windows Das Installationsprogramm enthält Funktionen zum Anzeigen einer Statusanzeige in einem Aktionsanzeigedialogfeld. Das [ProgressBar-Steuerelement](progressbar-control.md) stellt die Installation einzelner Komponenten grafisch dar und meldet entweder die gesamt verstrichene Zeit relativ zur verbleibenden Zeit oder die ungefähre Gesamtzeit, die bis zum Abschluss der Installation verbleibt.

Um die für die Installation erwartete Gesamtzeit zu ermitteln, verfolgt das Installationsprogramm die gesamten Fortschritts-Ticks nach, die von jeder Aktion während der Generierung des Ausführungsskripts erwartet werden. Wenn die Skriptgenerierung abgeschlossen ist, wird die Fortschritts-Tick-Summe gespeichert, und die Installation beginnt.

Statusmeldungen, die die verstrichene Anzahl von Fortschritts-Ticks beschreiben, werden an den aktiven Meldungshandler gesendet, wenn jede Aktion im Skript ausgeführt wird. Bei jeder Statusmeldung überträgt das Installationsprogramm ein [SetProgress ControlEvent](setprogress-controlevent.md) an das derzeit aktive Dialogfeld. Die Benutzeroberflächensequenz sollte erstellt werden, um das Aktionsanzeigedialogfeld während der Skriptausführung zu erstellen, um die SetProgress ControlEvent-Meldungen vom Installationsprogramm zu empfangen.

Wenn das Aktionsanzeigedialogfeld ein SetProgress ControlEvent empfängt, wird die [EventMapping-Tabelle](eventmapping-table.md) auf Steuerelemente überprüft, die ControlEvent abonnieren. Das ProgressBar-Steuerelement im Dialogfeld aktionsanzeige wird mit dem in der Spalte Attribute angegebenen Statussteuersteuerattribut abonniert. Das Progress Control-Attribut gibt an, dass dem ProgressBar-Steuerelement die Werte "ticksSoFar" und "totalTicks" zusammen mit dem SetProgress ControlEvent übergeben werden. Das Statusleisten-Steuerelement verwendet diese Informationen, um die grafische Leiste für eine Installation von links nach rechts und für einen [Rollbackvorgang](rollback-installation.md) von rechts nach links zu schreitet.

Darüber hinaus überträgt das Installationsprogramm für jede Statusmeldung ein [TimeRemaining ControlEvent.](timeremaining-controlevent.md) Die verbleibende Gesamtzeit für die Installation wird durch die berechnung der Ausführungsrate bestimmt. Dies ist die Gesamtanzahl der Ticks, die geteilt durch die Gesamtzeit seit Beginn der Installation verstrichen sind. Die verbleibenden Gesamtteilstriche dividiert durch die Ausführungsrate geben die ungefähre verbleibende Zeit an.

Wenn das Aktionsanzeigedialogfeld das TimeRemaining ControlEvent empfängt, sucht es erneut in der EventMapping-Tabelle nach steuerelementen, die abonniert sind. Um die verbleibende Zeit anzuzeigen, muss ein [Text-Steuerelement](text-control.md) das TimeRemaining ControlEvent mit dem in der Spalte Attribute angegebenen [TimeRemaining-Steuerelementattribut](timeremaining-control-attribute.md) abonniert werden.

Das abonnierte Text-Steuerelement fragt die [UIText-Tabelle](uitext-table.md) nach einer parametrisierten Vorlagenzeichenfolge namens "TimeRemaining" ab. Diese Zeichenfolge verfügt über zwei Parameter: \[ 1 \] für Minuten und \[ 2 für \] Sekunden. Das Text-Steuerelement konvertiert jeden Wert in Minuten und Sekunden, wertet die TimeRemaining-Vorlagenzeichenfolge aus und aktualisiert das Textsteuerfeld mit den neuen Informationen.

Wenn die Anzeigeebene der Benutzeroberfläche auf "Basic" oder "Lower" festgelegt ist, zeigt das Installationsprogramm ein Standarddialogfeld mit einer Statusanzeige und einem TimeRemaining-Textfeld an. Weitere Informationen finden Sie unter [Benutzeroberfläche Levels](user-interface-levels.md).

 

 



