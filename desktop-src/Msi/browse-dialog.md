---
description: Über das Dialogfeld Durchsuchen kann der Benutzer ein Verzeichnis auswählen. Das Verzeichnis muss nicht vorhanden sein und kann mit diesem Steuerelement erstellt werden.
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: Dialogfeld "Durchsuchen"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7caceb8e10bc99a9edd8fa5b828efa2e5cbc8b4ed7164d40e2235e19c098199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380712"
---
# <a name="browse-dialog"></a>Dialogfeld "Durchsuchen"

Über das Dialogfeld Durchsuchen kann der Benutzer ein Verzeichnis auswählen. Das Verzeichnis muss nicht vorhanden sein und kann mit diesem Steuerelement erstellt werden.

Diese Art von Dialogfeld enthält in der Regel die folgenden drei Steuerelemente. Diese Steuerelemente sind mit derselben Eigenschaft verbunden. Diese Eigenschaft ist der pfad, der ausgewählt wird.

-   Ein [PathEdit-Steuerelement,](pathedit-control.md) um den Abschnitt tail des Pfads auszuwählen. Dieses Steuerelement kann den Fokus nicht verlieren, wenn das eingegebene Ende auf dem aktuellen Volume nicht gültig ist.
-   Ein [DirectoryCombo-Steuerelement,](directorycombo-control.md) um den aktuell ausgewählten Pfad anzuzeigen, der vom PathEdit-Steuerelement angezeigt wird. Dieses Steuerelement zeigt nicht das letzte Segment des Pfads an.
-   Ein [DirectoryList-Steuerelement,](directorylist-control.md) um die Ordner unterhalb des Verzeichnisses anzuzeigen, das derzeit von DirectoryCombo angezeigt wird. Dadurch kann auch ein Ordner angezeigt werden, der noch nicht erstellt wurde.

Ein Dialogfeld Durchsuchen enthält in der Regel auch ein [DirectoryCombo-Steuerelement,](directorycombo-control.md) das die anzuzeigenden Volumetypen angibt. Es ist üblich, dass alle Volumetypen in einem Dialogfeld Durchsuchen angezeigt werden.

Dialogfelder zum Durchsuchen enthalten in der Regel drei [PushButton-Steuerelemente.](pushbutton-control.md) Diese Schaltflächen sind mit ihren jeweiligen ControlEvents in der [ControlEvent-Tabelle verknüpft.](controlevent-table.md) Diese Schaltflächen werden zum Aktivieren der folgenden Steuerelementoptionen verwendet.



| Steuerungsoption | ControlEvent                                            |
|----------------|---------------------------------------------------------|
| Eine Ebene nach oben   | [DirectoryListUp](directorylistup-controlevent.md)     |
| Neuer Ordner     | [DirectoryListNew](directorylistnew-controlevent.md)   |
| Öffnen           | [DirectoryListOpen](directorylistopen-controlevent.md) |



 

Damit die Option Neuer Ordner mit einem nicht standardmäßigen Ordnernamen funktioniert, muss der Pfad des neuen Ordners in der [UIText-Tabelle angegeben werden.](uitext-table.md) Die Pfadzeichenfolge sollte das Formular "Short file name \| long file name" für den Dateinamen verwenden. Verwenden Sie z. B. einen Dateinamen wie "MyProd~1 \| My 1 My Product". Weitere Informationen zum Dateiformat finden Sie unter [Filename](filename.md) column data type (Datentyp der Dateinamenspalte). Wenn der Pfad nicht in der UIText-Tabelle vorhanden oder auf einen ungültigen Wert festgelegt ist, wird er standardmäßig auf den Wert "Fldr \| New Folder" festgelegt. Die **Schaltfläche Neuer Ordner** kann weggelassen werden, wenn das Dialogfeld nur nach vorhandenen Ordnern suchen muss.

 

 



