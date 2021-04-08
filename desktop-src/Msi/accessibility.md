---
description: Autoren sollten die Tabellen und Felder in der folgenden Liste beachten, wenn Sie Ihre Benutzeroberfläche so entwerfen, dass Sie mit Active Accessibility Richtlinien konform ist.
ms.assetid: 516e504e-7895-4388-a38e-fd2fc7dfd61d
title: Barrierefreiheit (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46325c11337ef1e1db6f2da5728f06f9d4ee0649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864528"
---
# <a name="accessibility-windows-installer"></a>Barrierefreiheit (Windows Installer)

Autoren sollten die Tabellen und Felder in der folgenden Liste beachten, wenn Sie Ihre Benutzeroberfläche so entwerfen, dass Sie mit Active Accessibility Richtlinien konform ist. Die Benutzeroberfläche eines Installer-Pakets sollte den Zugriff auf die Anwendung oder das Produkt für alle Benutzer vereinfachen.

-   Der QuickInfo-Text ist in der Hilfe Spalte der [Steuerelement Tabelle](control-table.md)enthalten. Dieser Text wird von Bildschirmlesern für Steuerelemente angezeigt, die ein Bild enthalten.
-   Das Textfeld der [Steuerelement Tabelle](control-table.md) für die Steuerelemente " [volumecostlist](volumecostlist-control.md)", " [ListView](listview-control.md)", " [directorylist](directorylist-control.md) " und " [SelectionTree](selectiontree-control.md) " wird nie angezeigt. Stattdessen kann Sie von den Hilfsprogrammen für die Bildschirm Überprüfung als Beschreibung des Steuer Elements gelesen werden. Personen, die die visuellen Informationen nicht auf dem Bildschirm verwenden können, können die Informationen mithilfe eines Hilfsprogramms für die Bildschirm Überprüfung interpretieren. Screenreview-Hilfsprogramme (auch als Screenreader-Programme oder sprach Zugriffs Dienstprogramme bezeichnet) übernehmen die angezeigten Informationen auf dem Bildschirm und leiten Sie über alternative Medien weiter, wie z. b. die Sprachausgabe oder eine aktualisierbare brailledarstellung.
-   Steuerelemente in Dialogfeldern sollten mit dem Steuerelement \_ Next-Feld der [Steuerelement Tabelle](control-table.md)verknüpft werden. Die Steuerelemente müssen so verfasst werden, dass Sie alle mithilfe der Tab-Taste erreicht werden können.
-   Tastenkombinationen sollten bereitgestellt werden, um direkt auf Steuerelemente zugreifen zu können.
-   Die in der Benutzeroberfläche angezeigte Textfarbe wird in der [TextStyle-Tabelle](textstyle-table.md)festgelegt. Wenn die ausgewählte Textfarbe zu nah an der des Hintergrunds liegt, wird die Farbauswahl des Texts ignoriert.
-   Textgröße und-Schriftart werden in der [TextStyle-Tabelle](textstyle-table.md)festgelegt. Für Pakete, die für den asiatischen Markt vorgesehen sind, sollten größere Schriftart Größen verwendet werden. Beispielsweise ist ein Schrift Grad von 10 Punkten, der für englischen Text lesbar ist, für Chinesisch möglicherweise nicht unbedingt true.
-   Für die Steuerelemente " [Edit](edit-control.md)", " [pathedit](pathedit-control.md)", " [ListView](listview-control.md)", " [ComboBox](combobox-control.md) " oder " [volumeselectcombo](volumeselectcombo-control.md)" nehmen die Sprachausgaben "accName" und "accKeyboardShortcut" aus einem [Text Steuer](text-control.md) Element, das dem Steuerelement in der \_ nächsten Sequenz des Dialog Felds Wenn eine Verknüpfung vorhanden ist, nimmt die Bildschirm Sprachausgabe aus dem Textfeld des Text-Steuer Elements und von "accKeyboardShortcut" aus der Tastenkombination im Textfeld den Namen "accName".
-   Da statischer Text keinen Fokus haben kann, muss ein [Text Steuer](text-control.md) Element, das ein [Edit](edit-control.md)-, [pathedit](pathedit-control.md)-, [ListView](listview-control.md)-, [ComboBox](combobox-control.md) -oder [volumeselectcombo-Steuer](volumeselectcombo-control.md) Element beschreibt, das erste Steuerelement im Dialogfeld sein, um die Kompatibilität mit Bildschirmlesern sicherzustellen.
-   Für ein [PUSHBUTTON-Steuer](pushbutton-control.md) Element, das ein Symbol oder Bitmapbild anzeigt, werden accName und accKeyboardShortcut im Hilfe Feld des [Steuerelement Tabellen](control-table.md) Datensatzes auf der linken Seite des Trenn Zeichens angegeben \| .
-   Vermeiden Sie die Verwendung von Text Steuerelementen auf weißen Bitmaps, da der Text unter hoher Kontrast Schwarz unsichtbar werden kann.
-   Fügen Sie kein schwarzes Text-Steuerelement auf einem Hintergrund ein, bei dem es sich um ein alle weiß Bitmap-Bild handelt. Dieser Text ist für einen Benutzer, der die Windows-Anzeige in hoher Kontrast Schwarz ändert, nicht sichtbar.
-   Fügen Sie kein White Text-Steuerelement auf einem Hintergrund ein, bei dem es sich um ein alle schwarze Bitmap-Bild handelt. Dieser Text ist für einen Benutzer, der die Windows-Anzeige in hoher Kontrast weiß, nicht sichtbar.
-   Platzieren Sie keine transparenten [Text Steuerelemente](text-control.md) oberhalb von farbigen Bitmaps. Der Text ist möglicherweise nicht sichtbar, wenn der Benutzer das Anzeige Farbschema ändert. Beispielsweise kann Text unsichtbar werden, wenn der Benutzer den hohen Kontrast Parameter für Barrierefreiheit festlegt.
-   Beachten Sie, dass sich der Fokus auf einem Dialogfeld nicht auf ein [RadioButton Group-Steuer](radiobuttongroup-control.md) Element bezieht, bis eine der Schaltflächen in der Gruppe ausgewählt wurde. Legen Sie eine der Schaltflächen als Standardeinstellung für das Steuerelement fest, um die Registerkarte Fokus auf diese Schaltflächen Gruppe zu setzen.
-   Zum Bereitstellen von Bildschirm Leseprogrammen mit zusätzlichem beschreibenden Text zu einem [RadioButton Group-Steuer](radiobuttongroup-control.md)Element. Befolgen Sie das Beispiel unter [Hinzufügen von zusätzlichem Text zu](adding-extra-text-to-radio-buttons.md)Options Feldern.
-   Die relative Größe von Dialogfeldern, Steuerelementen und Schriftarten kann sich je nach ausgewähltem Schrift Grad ändern. Weitere Informationen finden Sie unter [Installations Einheiten](installer-units.md). Um die korrekte Anzeige von Text und Steuerelementen auf der Benutzeroberfläche sicherzustellen, sollten Setup Entwickler ihre Anwendung immer mit allen verwendeten Schriftgrößen testen.

 

 



