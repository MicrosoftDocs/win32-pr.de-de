---
description: Das Dialogfeld Durchsuchen ermöglicht dem Benutzer die Auswahl eines Verzeichnisses. Das Verzeichnis muss nicht vorhanden sein und kann mit diesem Steuerelement erstellt werden.
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: Dialog Feld durchsuchen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f6d3c3d95caec7e9a439621f6741b0dceb0c83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393609"
---
# <a name="browse-dialog"></a>Dialog Feld durchsuchen

Das Dialogfeld Durchsuchen ermöglicht dem Benutzer die Auswahl eines Verzeichnisses. Das Verzeichnis muss nicht vorhanden sein und kann mit diesem Steuerelement erstellt werden.

Diese Art von Dialogfeld enthält im Allgemeinen die folgenden drei Steuerelemente. Diese Steuerelemente sind mit derselben Eigenschaft verbunden. Diese Eigenschaft ist der Pfad, der ausgewählt wird.

-   Ein [pathedit-Steuer](pathedit-control.md) Element, um den Endabschnitt des Pfads auszuwählen. Dieses Steuerelement kann den Fokus nicht verlieren, wenn das eingegebene Ende auf dem aktuellen Volume nicht gültig ist.
-   Ein [directoriycombo-Steuer](directorycombo-control.md) Element, um den derzeit ausgewählten Pfad anzuzeigen, der vom Steuerelement "pathedit" angezeigt wird. Dieses Steuerelement zeigt nicht das letzte Segment des Pfads an.
-   Ein [Director List-Steuer](directorylist-control.md) Element, das die Ordner unterhalb des Verzeichnisses anzeigt, das zurzeit von directoriycombo angezeigt wird. Dadurch kann auch ein Ordner angezeigt werden, der noch nicht erstellt wurde.

Das Dialogfeld Durchsuchen enthält normalerweise auch ein [directoriycombo-Steuer](directorycombo-control.md) Element, das die anzuzeigenden Volumetypen angibt. Es ist üblich, dass alle Volumetypen im Dialogfeld Durchsuchen angezeigt werden.

Dialogfelder durchsuchen enthalten in der Regel drei [PUSHBUTTON](pushbutton-control.md)-Steuerelemente. Diese Schaltflächen sind mit ihren jeweiligen ControlEvents in der [ControlEvent-Tabelle](controlevent-table.md)verknüpft. Diese Schaltflächen werden zum Aktivieren der folgenden Steuerelement Optionen verwendet.



| Control-Option | ControlEvent                                            |
|----------------|---------------------------------------------------------|
| Eine Ebene nach oben   | [Directoren](directorylistup-controlevent.md)     |
| Neuer Ordner     | [Directoriylistnew](directorylistnew-controlevent.md)   |
| Öffnen           | [Directoriylistopen](directorylistopen-controlevent.md) |



 

Damit die Option neuer Ordner mit einem nicht standardmäßigen Ordnernamen funktioniert, muss der Pfad des neuen Ordners in der [UIText-Tabelle](uitext-table.md)angegeben werden. Die Pfad Zeichenfolge sollte das \| Formular "kurzdateiname Long Dateiname" für den Dateinamen verwenden. Verwenden Sie z. b. einen Dateinamen wie "myprod ~ 1 \| My Fabulous Product". Weitere Informationen zum Format des Datei namens finden Sie unter Datentyp der [Dateiname](filename.md) -Spalte. Wenn der Pfad in der UIText-Tabelle nicht vorhanden ist oder wenn er auf einen ungültigen Wert festgelegt ist, wird er standardmäßig auf den Wert "fldr \| New Folder" festgelegt. Die Schaltfläche **neuer Ordner** kann weggelassen werden, wenn das Dialogfeld nur vorhandene Ordner suchen muss.

 

 



