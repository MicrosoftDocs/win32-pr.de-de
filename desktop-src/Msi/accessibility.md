---
description: Autoren sollten die Tabellen und Felder in der folgenden Liste kennen, wenn sie ihre Benutzeroberfläche so entwerfen, dass sie den Active Accessibility entspricht.
ms.assetid: 516e504e-7895-4388-a38e-fd2fc7dfd61d
title: Barrierefreiheit (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8811d47bc7288e966ca5d536b435611c79fd81f3a38fa0b2dbdd422b5939a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078230"
---
# <a name="accessibility-windows-installer"></a>Barrierefreiheit (Windows Installer)

Autoren sollten die Tabellen und Felder in der folgenden Liste kennen, wenn sie ihre Benutzeroberfläche so entwerfen, dass sie den Active Accessibility entspricht. Die Benutzeroberfläche eines Installationspakets sollte allen Benutzern den Zugriff auf die Anwendung oder das Produkt erleichtern.

-   QuickInfo-Text ist in der Hilfespalte der [Control-Tabelle enthalten.](control-table.md) Dieser Text wird von Sprachlesebildschirmen für Steuerelemente angezeigt, die ein Bild enthalten.
-   Das Textfeld der [Control-Tabelle](control-table.md) für die [Steuerelemente VolumeCostList,](volumecostlist-control.md) [ListView,](listview-control.md) [DirectoryList](directorylist-control.md) und [SelectionTree](selectiontree-control.md) wird nie angezeigt. Stattdessen kann es von Bildschirmüberprüfungs-Hilfsprogrammen als Beschreibung des Steuerelements gelesen werden. Personen, die die visuellen Informationen auf dem Bildschirm nicht verwenden können, können die Informationen mithilfe eines Bildschirmüberprüfungs-Hilfsprogramms interpretieren. Hilfsprogramme für die Bildschirmüberprüfung (auch als Sprachausgabeprogramme oder Sprachzugriffs-Hilfsprogramme bezeichnet) verwenden die angezeigten Informationen auf dem Bildschirm und richten sie über alternative Medien wie synthetisierte Sprache oder eine auffrischbare Braille-Anzeige ein.
-   Steuerelemente in Dialogfeldern sollten mithilfe des Felds Steuerelement \_ Weiter der [Steuertabelle verknüpft werden.](control-table.md) Die Steuerelemente müssen so verfasst werden, dass sie alle mithilfe der TAB-TASTE erreicht werden können.
-   Tastenkombinationen sollten für den direkten Zugriff auf Steuerelemente bereitgestellt werden.
-   Die auf der Benutzeroberfläche angezeigte Textfarbe wird in der [TextStyle-Tabelle festgelegt.](textstyle-table.md) Wenn die ausgewählte Textfarbe zu nah an der des Hintergrunds liegt, wird die Farbauswahl des Texts ignoriert.
-   Textgröße und Schriftart werden in der [TextStyle-Tabelle festgelegt.](textstyle-table.md) Größere Schriftgrößen sollten für Pakete verwendet werden, die für den asiatisch-markt bestimmt sind. Beispielsweise ist ein Schriftgrad von 10 Punkten, der für englischen Text lesbar ist, möglicherweise nicht unbedingt auf Chinesisch zutreffen.
-   Für [edit-,](edit-control.md) [PathEdit-,](pathedit-control.md) [ListView-,](listview-control.md) [ComboBox-](combobox-control.md) oder [VolumeSelectCombo-Steuerelemente](volumeselectcombo-control.md)verwenden Sprachleser accName und accKeyboardShortcut aus einem [Textsteuerfeld,](text-control.md) das dem Steuerelement in der Sequenz Nächste Steuerung des Dialogfelds voran stehen \_ muss. Die Sprachausgabe verwendet accName aus dem Textfeld des Text-Steuerelements und accKeyboardShortcut aus der Tastenkombination im Textfeld, wenn eine Verknüpfung vorhanden ist.
-   Da statischer Text den [](text-control.md) Fokus nicht übernehmen kann, muss ein Text-Steuerelement, das ein [Edit-,](edit-control.md) [PathEdit-,](pathedit-control.md) [ListView-,](listview-control.md) [ComboBox-](combobox-control.md) oder [VolumeSelectCombo-Steuerelement](volumeselectcombo-control.md) beschreibt, als erstes Steuerelement im Dialogfeld verwendet werden, um die Kompatibilität mit Sprachbildschirmen sicherzustellen.
-   Für ein [PushButton-Steuerelement,](pushbutton-control.md) das ein Symbol oder bitmap-Bild anzeigt, werden accName und [](control-table.md) accKeyboardShortcut im Hilfefeld des Datensatzes Steuertabelle links neben dem Trennzeichen \| angegeben.
-   Vermeiden Sie die Verwendung von Textsteuerelementen über weißen Bitmaps, da unter hoher Kontrast Schwarz der Text unsichtbar werden kann.
-   Legen Sie kein schwarzes Textsteuerfeld auf einen Hintergrund, bei dem es sich um ein weißes Bitmapbild handelt. Dieser Text ist für einen Benutzer nicht sichtbar, der die Windows in hoher Kontrast ändert.
-   Setzen Sie ein Weißtext-Steuerelement nicht auf einen Hintergrund, bei dem es sich um ein ganz schwarzes Bitmapbild handelt. Dieser Text ist für einen Benutzer nicht sichtbar, der die Windows in weiß hoher Kontrast ändert.
-   Platzieren Sie transparente [Textsteuerelemente nicht](text-control.md) über farbigen Bitmaps. Der Text ist möglicherweise nicht sichtbar, wenn der Benutzer das Anzeigefarbschema ändert. Beispielsweise kann Text unsichtbar werden, wenn der Benutzer den Parameter für hohen Kontrast für die Barrierefreiheit festgibt.
-   Beachten Sie, dass der Fokus auf einem Dialogfeld erst dann zu einem [RadioButtonGroup-Steuerelement](radiobuttongroup-control.md) führt, wenn eine der Schaltflächen in der Gruppe ausgewählt wurde. Um die Fokusregisterkarte zu dieser Schaltflächengruppe zu machen, geben Sie eine der Schaltflächen als Standardeinstellung für das Steuerelement an.
-   Um Sprachausgabeprogrammen zusätzlichen beschreibenden Text zu einem [RadioButtonGroup-Steuerelement zur Verfügung zu stellen.](radiobuttongroup-control.md) Befolgen Sie das Beispiel unter [Hinzufügen von zusätzlichem Text zu Optionsfeldern.](adding-extra-text-to-radio-buttons.md)
-   Die relative Größe von Dialogen, Steuerelementen und Schriftarten kann sich abhängig vom gewählten Schriftgrad ändern. Weitere Informationen finden Sie unter [Installationseinheiten.](installer-units.md) Um die korrekte Anzeige von Text und Steuerelementen auf der Benutzeroberfläche sicherzustellen, sollten Setupentwickler ihre Anwendung immer mit allen Schriftgraden testen, die verwendet werden können.

 

 



