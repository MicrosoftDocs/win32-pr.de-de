---
description: In einem Dialogfeld können während einer Installation eine Sequenz von Bildern und Text in einem Dialog angezeigt werden. In der Regel werden mithilfe von Billboards die visuellen Effekte einer Folien Anzeige oder-Animation erstellt, mit der der Benutzer über den Fortschritt einer Installation informiert wird.
ms.assetid: 6432ee7d-0da2-48be-b14c-d36a83a3bb1d
title: Anzeigen von Plakaten in einem nicht modalem Dialog Feld
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fd0ca40e47a8d52c16db7adde304177d4dc849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130689"
---
# <a name="displaying-billboards-on-a-modeless-dialog"></a>Anzeigen von Plakaten in einem nicht modalem Dialog Feld

In einem Dialogfeld können während einer Installation eine Sequenz von Bildern und Text in einem Dialog angezeigt werden. In der Regel werden mithilfe von Billboards die visuellen Effekte einer Folien Anzeige oder-Animation erstellt, mit der der Benutzer über den Fortschritt einer Installation informiert wird.

**So zeigen Sie in einem nicht modalem Dialogfeld**

1.  Fügen Sie einen Datensatz in die [Dialogfeld Tabelle](dialog-table.md) für das nicht Modelle Dialogfeld ein, das das Billboard enthält. Nachdem ein Billboard angezeigt wurde, gibt ein nicht modalem Dialogfeld die Steuerung an das Installationsprogramm zurück. Dadurch kann das Installationsprogramm Nachrichten verarbeiten und das Dialogfeld und das-Billboard aktualisieren. Um ein nicht modales Dialogfeld zu erstellen, legen Sie das modale Dialogfeld Format nicht im Feld Attribute der [Dialogfeld Tabelle](dialog-table.md)fest. Der folgende [Dialogfeld Tabellen](dialog-table.md) -Datensatz gibt das Dialogfeld "Aktions Dialogfeld" an

    [Dialog Feld Tabelle](dialog-table.md) (teilweise)

    | Dialog\_     | Hcentering | Vcentering | Breite | Höhe | Attribute | Titel  | \_Zuerst Steuern | Standard Steuerelement \_ | Abbrechen von Steuerelementen \_ |
    |--------------|------------|------------|-------|--------|------------|--------|----------------|------------------|-----------------|
    | Aktions Dialogfeld | 50         | 50         | 480   | 240    | 5          | Aktion | Abbrechen         | Abbrechen           | Abbrechen          |

    

     

2.  Fügen Sie der Steuerelement [Tabelle](control-table.md) einen Datensatz hinzu, um anzugeben, dass im Dialogfeld ein Plakat angezeigt werden soll. Der Datensatz definiert die Größe und die Position des Bereichs im Dialogfeld, in dem die in der Tabelle " [bbcontrol](bbcontrol-table.md) " aufgeführten Register Steuerelemente angezeigt werden sollen. Im folgenden [Steuerelement Tabellen](control-table.md) Daten Satz werden die Position und die Größe des Billboard im Dialogfeld "Aktions Dialogfeld" definiert.

    [Control-Tabelle](control-table.md) (partiell)

    | Dialog\_     | Control   | type      | X   | J   | Breite | Höhe | Attribute |
    |--------------|-----------|-----------|-----|-----|-------|--------|------------|
    | Aktions Dialogfeld | Billboard | Billboard | 0   | 110 | 480   | 130    | 1          |

    

     

3.  In der [Tabelle "Billboard](billboard-table.md) " sind die Billboard-Steuerelemente aufgelistet, und es wird angegeben, wann ein bestimmtes Steuerelement Fügen Sie der Tabelle " [Billboard](billboard-table.md) " einen Datensatz für jedes Billboard-Steuerelement hinzu. In der [Tabelle "Billboard](billboard-table.md) " werden während einer Installation gesendete Fortschrittsmeldungen überwacht. Ein Billboard wird nur angezeigt, wenn eine Statusmeldung von den in der Spalte Aktion der [Tabelle](billboard-table.md)"Aktion" aufgelisteten Aktionen gesendet wird, und nur, wenn die Funktion im Feld "Feature" \_ für die Installation ausgewählt ist. Nachdem ein Billboard angezeigt wird, bleibt es sichtbar, bis es von einem anderen Billboard abgedeckt oder das Dialogfeld geschlossen wird. Wenn für eine Aktion mehrere festgelegte festgelegt wurden, werden Sie nacheinander in der Reihenfolge angezeigt, die durch das Bestell Feld angegeben wird. Beispielsweise zeigen die folgenden Einträge in der [Tabelle](billboard-table.md) "BB1" zuerst das und dann das BB2-Steuerelement " [Billboard](billboard-control.md) " an, wenn die [InstallFiles](installfiles-action.md) -Aktion ausgeführt wird und die Schnelltest Funktion für die Installation ausgewählt wurde.

    [Billboard-Tabelle](billboard-table.md) (partiell)

    | Billboard | Funktion   | Aktion       | Sortieren |
    |-----------|-----------|--------------|----------|
    | BB1       | QuickTest | InstallFiles | 1        |
    | BB2       | QuickTest | InstallFiles | 2        |

    

     

4.  Die [Tabelle "bbcontrol](bbcontrol-table.md) " gibt die Steuerelemente an, die zu den in der [Tabelle "Billboard](billboard-table.md)" aufgelisteten Billboard-Steuer [Elementen](billboard-control.md) gehören. Das [Text Steuer](text-control.md)Element, das [Bitmap-Steuer](bitmap-control.md)Element und das [Symbol Steuer](icon-control.md) Element sind die einzigen Typen von Steuerelementen, die auf einem Billboard wechseln können. Auf jedem Billboard können mehrere Steuerelemente platziert werden. Geben Sie den Namen des Billboard im Feld "Billboard" \_ der [Tabelle "bbcontrol](bbcontrol-table.md) " genau so ein, wie es in der [Tabelle "Billboard](billboard-table.md)" angezeigt wird.

    Jede Steuerelement Position wird als Koordinaten der linken oberen Ecke des-Steuer Elements angegeben. Der Ursprung des Koordinatensystems befindet sich in der linken oberen Ecke des Billboard-Steuer Elements und nicht in einer Ecke des Dialog Felds. Die Koordinaten befinden sich in den installereinheiten und nicht in den Dialog Einheiten. Eine installereinheit ist gleich 1-zwölfte Höhe des 10-Punkt-MS Sans Serif-Schrift Grads. In der folgenden [Tabelle "bbcontrol](bbcontrol-table.md) " werden Steuerelemente an die Register Bänder gebunden

    [Bbcontrol-Tabelle](bbcontrol-table.md) (partiell)

    | Billboard | Bbcontrol | type   | X   | J   | Breite | Höhe | Attribute | Text             |
    |-----------|-----------|--------|-----|-----|-------|--------|------------|------------------|
    | BB1       | Text      | Text   | 100 | 30  | 280   | 280    | 3          | Erstes Billboard  |
    | BB1       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Software         |
    | BB1       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Musik            |
    | BB2       | Text      | Text   | 100 | 30  | 280   | 20     | 3          | Zweites Billboard |
    | BB2       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Musik            |
    | BB2       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Software         |

    

     

5.  Wenn Sie im Dialogfeld "action Dialog" ein Billboard-Steuerelement anzeigen möchten, müssen Sie das Billboard-Steuerelement für [setProgress ControlEvent](setprogress-controlevent.md) abonnieren, indem Sie der [Tabelle EventMapping](eventmapping-table.md)einen Datensatz hinzufügen. Wenn das Installationsprogramm das setProgress ControlEvent veröffentlicht, das in der Ereignis Spalte angegeben ist, legt das Installationsprogramm das im Feld Attribut angegebene Steuerelement Attribut fest. Das Ereignisfeld enthält den Zeichen folgen Bezeichner (ohne Anführungszeichen) des setProgress ControlEvent. Das Attribut Feld enthält den Zeichen folgen Bezeichner (ohne Anführungszeichen) des festzulegenden Attributs. Die Felder "Dialog" und "Steuerelement" \_ \_ identifizieren das Billboard-Steuerelement und sollten diesen Feldern in der [Steuerelement Tabelle](control-table.md)entsprechen. Beispielsweise wird in der folgenden [EventMapping-Tabelle](eventmapping-table.md) ein-Steuerelement für ein-Ereignis abonniert.

    [EventMapping-Tabelle](eventmapping-table.md) (partiell)

    | Dialog\_     | Steuerelement\_ | Ereignis       | Attribut |
    |--------------|-----------|-------------|-----------|
    | Aktions Dialogfeld | Billboard | SetProgress | Fortschritt  |

    

     

 

 



