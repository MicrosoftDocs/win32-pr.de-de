---
description: Entwickler von Installationspaketen können eine Benutzeroberfläche erstellen, die die in diesem Thema beschriebenen Steuerelemente enthält.
ms.assetid: ed9fa158-9dad-4d2d-8153-78122b19a34e
title: Steuerelemente (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec286adf25c0642ae044bfd0b89e66182ef6839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350248"
---
# <a name="controls-windows-installer"></a>Steuerelemente (Windows Installer)

Entwickler von Installationspaketen können eine Benutzeroberfläche erstellen, die die in diesem Thema beschriebenen Steuerelemente enthält. Informationen zum Hinzufügen eines bestimmten Steuer Elements zu einem Dialogfeld finden Sie im Thema für dieses Steuerelement und im Abschnitt [Hinzufügen von Steuerelementen und Text](adding-controls-and-text.md).

Einige Steuerelemente, z. b. CheckBox und ComboBox, sind mit einer Eigenschaft verknüpft, die in der-Eigenschaften Spalte der [Steuerelement Tabelle](control-table.md)angegeben ist. Ein Benutzer ändert den Wert dieser Eigenschaft, indem er mit dem-Steuerelement interagiert. Passive Steuerelemente, wie z. b. "Billboard" und "Bitmap", sind keiner solchen Eigenschaft zugeordnet.

Aus Sicherheitsgründen können private Eigenschaften von Benutzern, die mit der Benutzeroberfläche interagieren, nicht geändert werden. Damit eine Eigenschaft von der Benutzeroberfläche festgelegt werden kann, muss es sich um eine öffentliche Eigenschaft und in Großbuchstaben handeln. Siehe auch [Informationen zu Eigenschaften](about-properties.md).

In einigen Fällen kann ein Steuerelement beim Abbrechen eines Dialogs falsch neu gezeichnet werden. Dies muss mit der Reihenfolge geschehen, in der die Steuerelemente \_ nach dem Entfernen des Abbrechen-Dialog Felds WM-Paint-Meldungen empfangen. Um dieses Problem zu beheben, versuchen Sie, die Reihenfolge der Steuerelemente in der Steuerelement Tabelle zu ändern.



| Steuerelementname                                       | Zugehörige Eigenschaft | Kurze Beschreibung des Steuer Elements                                                                                                                                                          |
|----------------------------------------------------|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Billboard](billboard-control.md)                 | Nein                  | Zeigt auf der Grundlage von Fortschrittsmeldungen an.                                                                                                                                       |
| [Bitmap](bitmap-control.md)                       | Nein                  | Zeigt ein statisches Bild einer Bitmap an.                                                                                                                                                |
| [CheckBox](checkbox-control.md)                   | Ja                 | Ein Kontrollkästchen mit zwei Zuständen.                                                                                                                                                                |
| [ComboBox](combobox-control.md)                   | Ja                 | Eine Dropdown Liste mit einem Bearbeitungsfeld.                                                                                                                                                  |
| [Directoriycombo](directorycombo-control.md)       | Ja                 | Wählen Sie alle außer dem letzten Segment des Pfads aus.                                                                                                                                       |
| [Directoren auflisten](directorylist-control.md)         | Ja                 | Zeigt die Ordner unterhalb des Hauptteils von Path an.                                                                                                                                         |
| [Bearbeiten](edit-control.md)                           | Ja                 | Ein reguläres Bearbeitungsfeld für eine beliebige Zeichenfolge oder ganze Zahl.                                                                                                                                       |
| [GroupBox](groupbox-control.md)                   | Nein                  | Zeigt ein Rechteck an, in dem andere Steuerelemente gruppiert werden.                                                                                                                             |
| [Link](hyperlink-control.md)                 | Nein                  | Zeigt einen HTML-Link zu einer Adresse an, die im Standardbrowser geöffnet wird. **[Windows Installer 4,5 und früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.<br/> |
| [Symbol:](icon-control.md)                           | Nein                  | Zeigt ein statisches Bild eines Symbols an.                                                                                                                                                 |
| [Line](line-control.md)                           | Nein                  | Zeigt eine horizontale Linie an.                                                                                                                                                           |
| [ListBox](listbox-control.md)                     | Ja                 | Eine Dropdown Liste ohne Bearbeitungsfeld.                                                                                                                                               |
| [ListView](listview-control.md)                   | Ja                 | Zeigt eine Spalte mit Werten mit Symbolen für die Auswahl an.                                                                                                                                 |
| [MaskedEdit](maskededit-control.md)               | Ja                 | Ein Bearbeitungsfeld mit einer Maske im Textfeld.                                                                                                                                          |
| [Pathetin](pathedit-control.md)                   | Ja                 | Zeigt den Ordnernamen oder den gesamten Pfad in einem Bearbeitungsfeld an.                                                                                                                                 |
| [ProgressBar-Steuerelement](progressbar-control.md)     | Nein                  | Balkendiagramm, das die Länge ändert, während es Fortschrittsmeldungen empfängt.                                                                                                                       |
| [PUSHBUTTON](pushbutton-control.md)               | Nein                  | Zeigt eine grundlegende pushschaltfläche an.                                                                                                                                                         |
| [RadioButtonGroup](radiobuttongroup-control.md)   | Ja                 | Eine Gruppe von Options Feldern.                                                                                                                                                             |
| [Scrollabletext](scrollabletext-control.md)       | Nein                  | Zeigt eine lange Text Zeichenfolge an.                                                                                                                                                       |
| [SelectionTree](selectiontree-control.md)         | Ja                 | Zeigt Informationen aus der Funktions Tabelle an und ermöglicht dem Benutzer das Ändern des Auswahl Zustands.                                                                                     |
| [Text](text-control.md)                           | Nein                  | Zeigt statischen Text an.                                                                                                                                                                 |
| [Volumecostlist](volumecostlist-control.md)       | Nein                  | Zeigt Kosteninformationen auf verschiedenen Volumes an.                                                                                                                                    |
| [Volumeselectcombo](volumeselectcombo-control.md) | Ja                 | Wählt das Volume aus einer alphabetischen Liste aus.                                                                                                                                             |



 

 

 




