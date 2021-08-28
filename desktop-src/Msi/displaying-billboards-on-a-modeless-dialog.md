---
description: Bei einer Installation kann in einem Dialogfeld eine Sequenz von Bildern und Text angezeigt werden. In der Regel werden Tafeln verwendet, um den visuellen Effekt einer Diashow oder Animation zu erstellen, die den Benutzer über den Fortschritt einer Installation informiert.
ms.assetid: 6432ee7d-0da2-48be-b14c-d36a83a3bb1d
title: Anzeigen von Darstellungen in einem moduslosen Dialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badf81e2b6d0131d1224f10b19e8de3c06f173ef91e3b08f3a45f31aef52be11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086170"
---
# <a name="displaying-billboards-on-a-modeless-dialog"></a>Anzeigen von Darstellungen in einem moduslosen Dialog

Bei einer Installation kann in einem Dialogfeld eine Sequenz von Bildern und Text angezeigt werden. In der Regel werden Tafeln verwendet, um den visuellen Effekt einer Diashow oder Animation zu erstellen, die den Benutzer über den Fortschritt einer Installation informiert.

**So zeigen Sie Schilde in einem nicht moduslosen Dialog an**

1.  Schließen Sie einen Datensatz in [die Dialogfeldtabelle für](dialog-table.md) das dialogfeld ohne Modus ein, das die Tafel enthält. Nachdem ein Schild angezeigt wurde, gibt ein nicht modusloses Dialogfeld die Steuerung an den Installer zurück. Dadurch kann der Installer Nachrichten verarbeiten und das Dialogfeld und das Dialogfeld aktualisieren. Um ein modusloses Dialogfeld zu erstellen, legen Sie das Modale Dialogformatbit nicht im Feld Attribute der [Dialogtabelle fest.](dialog-table.md) Der folgende [Datensatz der Dialogfeldtabelle](dialog-table.md) gibt das Dialogfeld ActionDialog an.

    [Dialogtabelle](dialog-table.md) (partiell)

    | Dialog\_     | HCentering | VCentering | Breite | Höhe | Attribute | Titel  | Control \_ First | \_Standardsteuersteuersystem | Abbrechen \_ des Steuerelements |
    |--------------|------------|------------|-------|--------|------------|--------|----------------|------------------|-----------------|
    | ActionDialog | 50         | 50         | 480   | 240    | 5          | Aktion | Abbrechen         | Abbrechen           | Abbrechen          |

    

     

2.  Fügen Sie der Steuertabelle [einen Datensatz hinzu,](control-table.md) um anzugeben, dass im Dialogfeld eine Tafel angezeigt wird. Der Datensatz definiert die Größe und Position des Bereich im Dialogfeld, in dem die in der [BBControl-Tabelle](bbcontrol-table.md) aufgeführten Steuerelementen angezeigt werden sollen. Der folgende [Control Table-Datensatz](control-table.md) definiert die Position und Größe des Kastens im Dialogfeld ActionDialog.

    [Steuertabelle](control-table.md) (partiell)

    | Dialog\_     | Control   | type      | X   | J   | Breite | Höhe | Attribute |
    |--------------|-----------|-----------|-----|-----|-------|--------|------------|
    | ActionDialog | Billboard | Billboard | 0   | 110 | 480   | 130    | 1          |

    

     

3.  In [der Tabellentabelle Werden](billboard-table.md) die Ziersteuerelemente aufgeführt, und es wird angegeben, wann ein bestimmtes Steuerelement angezeigt wird. Fügen Sie der [Tabelle "Table Table" einen Datensatz für](billboard-table.md) jedes Steuerelement hinzu. Die [Tabellentabelle "Table" (Tabellen)](billboard-table.md) überwacht status-Meldungen, die während einer Installation gesendet werden. Ein Schild wird nur angezeigt, wenn eine Statusmeldung von den Aktionen gesendet wird, die in der Spalte Aktion der [Tabelle "Vorgang"](billboard-table.md)aufgeführt sind, und nur, wenn das Feature im Feld Feature für die Installation \_ ausgewählt ist. Nachdem ein Schild angezeigt wurde, bleibt es sichtbar, bis es von einem anderen Schild abgedeckt wird oder bis das Dialogfeld geschlossen wird. Wenn mehrere Tafeln für eine Aktion angegeben werden, werden sie nach und nach in der reihenfolge angezeigt, die durch das Feld Ordering angegeben wird. Die folgenden Tabelleneinträge zeigen beispielsweise zuerst BB1 und dann DIE BB2-Steuerelemente an, wenn die [Aktion InstallFiles](installfiles-action.md) ausgeführt wird und die QuickTest-Funktion für die Installation ausgewählt wurde. [](billboard-table.md) [](billboard-control.md)

    [Tabellentabelle](billboard-table.md) (partiell)

    | Billboard | Komponente   | Aktion       | Sortieren |
    |-----------|-----------|--------------|----------|
    | BB1       | Quicktest | InstallFiles | 1        |
    | BB2       | Quicktest | InstallFiles | 2        |

    

     

4.  Die [BBControl-Tabelle](bbcontrol-table.md) gibt die Steuerelemente an, die zu den [Steuerelementen gehören,](billboard-control.md) die in der [Tabelle "Table" aufgeführt sind.](billboard-table.md) Das [Textsteuerfeld,](text-control.md) [das Bitmap-Steuerelement](bitmap-control.md)und das [Symbolsteuerelemente](icon-control.md) sind die einzigen Arten von Steuerelementen, die auf einer Leiste verwendet werden können. Auf jedem Schild können mehrere Steuerelemente platziert werden. Geben Sie den Namen des Tafeln in das Feld \_ ["BbControl"](bbcontrol-table.md) der BBControl-Tabelle genau so ein, wie er in der Tabelle ["Table" angezeigt wird.](billboard-table.md)

    Jede Steuerelementposition wird als Koordinaten der oberen linken Ecke des Steuerelements angegeben. Der Ursprung des Koordinatensystems befindet sich in der oberen linken Ecke des Steuerelements und nicht in einer Ecke des Dialogfelds. Die Koordinaten befinden sich in Installationseinheiten, nicht in Dialogeinheiten. Eine Installer-Einheit entspricht einem Zwölftel der Höhe des 10-Punkt-MS Sans Serif-Schriftgrads. In den folgenden [BBControl-Tabellendatensätzen](bbcontrol-table.md) werden Steuerelemente mit Denkelementen verbunden.

    [BBControl-Tabelle](bbcontrol-table.md) (partiell)

    | Billboard | BBControl | type   | X   | J   | Breite | Höhe | Attribute | Text             |
    |-----------|-----------|--------|-----|-----|-------|--------|------------|------------------|
    | BB1       | Text      | Text   | 100 | 30  | 280   | 280    | 3          | First Mans  |
    | BB1       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Software         |
    | BB1       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Musik            |
    | BB2       | Text      | Text   | 100 | 30  | 280   | 20     | 3          | Zweiter Manding |
    | BB2       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Musik            |
    | BB2       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Software         |

    

     

5.  Um im Dialogfeld ActionDialog ein Steuerelement anzuzeigen, müssen Sie das Steuerelement ["ControlEvent" von "SetProgress"](setprogress-controlevent.md) abonnieren, indem Sie der [EventMapping-Tabelle](eventmapping-table.md)einen Datensatz hinzufügen. Wenn der Installer das setProgress ControlEvent veröffentlicht, das in der Spalte Ereignis angegeben ist, legt der Installer das Steuerelementattribut fest, das im Feld Attribut angegeben ist. Das Feld Ereignis enthält den Zeichenfolgenbezeichner (ohne Anführungszeichen) des SetProgress ControlEvent. Das Attributfeld enthält den Zeichenfolgenbezeichner (ohne Anführungszeichen) des festzulegenden Attributs. Die Felder Dialog \_ und Steuerelement identifizieren das Steuerelement \_ "Steuerelement" und sollten mit den Feldern in der [Steuerelementtabelle](control-table.md)übereinstimmen. Beispielsweise abonniert die folgende [EventMapping-Tabelle](eventmapping-table.md) ein -Steuerelement für ein Ereignis.

    [EventMapping-Tabelle](eventmapping-table.md) (partiell)

    | Dialog\_     | Steuerelement\_ | Ereignis       | attribute |
    |--------------|-----------|-------------|-----------|
    | ActionDialog | Billboard | SetProgress | Fortschritt  |

    

     

 

 



