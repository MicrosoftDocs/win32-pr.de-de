---
title: Resource-Definition-Anweisungen
description: Die Resource Definition-Anweisungen definieren die Ressourcen, die der Ressourcencompiler in die Ressource (. Res)-Datei.
ms.assetid: f96b8c1e-8188-40b7-8eda-c13b61b8fc41
keywords:
- Ressourcencompiler,Resource Definition-Anweisungen
- TEXTINCLUDE-Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4937eb9d5fb9bba7b174aa9543be8b3f2eb41c90c6bc20a72650114f57fb4fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869906"
---
# <a name="resource-definition-statements"></a>Resource-Definition-Anweisungen

Die Resource Definition-Anweisungen definieren die Ressourcen, die der Ressourcencompiler in die Ressource (. Res)-Datei. Nach dem . Die Res-Datei ist mit der ausführbaren Datei verknüpft. Die Anwendung kann ihre Ressourcen bei Bedarf zur Laufzeit laden. Alle Ressourcen-Anweisungen ordnen einer bestimmten Ressource einen identifizierenden Namen oder eine Nummer zu.

Die Resource Definition-Anweisungen können in die folgenden Kategorien unterteilt werden:

-   Ressourcen
-   Steuerelemente
-   Anweisungen

In den folgenden Tabellen werden die Resource Definition-Anweisungen beschrieben.

## <a name="resources"></a>Ressourcen



| Ressource                                      | Beschreibung                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Beschleuniger**](accelerators-resource.md) | Definiert Tastenkombinationen für menüs.                                                                                                                                                  |
| [**Bitmap**](bitmap-resource.md)             | Definiert eine Bitmap durch Benennen und Angeben des Namens der Datei, in der sie enthalten ist. (Um eine bestimmte Bitmap zu verwenden, fordert die Anwendung sie über den Namen an.)                          |
| [**Cursor**](cursor-resource.md)             | Definiert einen Cursor oder animierten Cursor durch Benennen und Angeben des Namens der Datei, in der er enthalten ist. (Um einen bestimmten Cursor zu verwenden, fordert die Anwendung ihn über den Namen an.)       |
| [**DIALOG**](dialog-resource.md)             | Definiert eine Vorlage, mit der eine Anwendung Dialogfelder erstellen kann.                                                                                                          |
| [**Dialogex**](dialogex-resource.md)         | Definiert eine Vorlage, mit der eine Anwendung Dialogfelder erstellen kann.                                                                                                          |
| [**Schriftart**](font-resource.md)                 | Gibt den Namen einer Datei an, die eine Schriftart enthält.                                                                                                                              |
| [**Html**](html-resource.md)                 | Gibt eine HTML-Datei an.                                                                                                                                                         |
| [**Symbol**](icon-resource.md)                 | Definiert ein Symbol oder animiertes Symbol, indem es benennen und den Namen der Datei angeben, in der es enthalten ist. (Um ein bestimmtes Symbol zu verwenden, fordert die Anwendung es über den Namen an.)            |
| [**Menü**](menu-resource.md)                 | Definiert die Darstellung und Funktion eines Menüs.                                                                                                                                  |
| [**MENUEX**](menuex-resource.md)             | Definiert die Darstellung und Funktion eines Menüs.                                                                                                                                  |
| [**MESSAGETABLE**](messagetable-resource.md) | Definiert eine Meldungstabelle durch Benennen und Angeben des Namens der Datei, in der sie enthalten ist. Die Datei ist eine binäre Ressourcendatei, die vom Nachrichtencompiler generiert wird.                |
| [**Popup**](popup-resource.md)               | Definiert ein Menüelement, das Menüelemente und Untermenüs enthalten kann.                                                                                                                   |
| **PLUGPLAY**                                  | Veraltet.                                                                                                                                                                       |
| [**Rcdata**](rcdata-resource.md)             | Definiert Datenressourcen. Mit Datenressourcen können Sie Binärdaten in die ausführbare Datei ein include.                                                                                      |
| [**Stringtable**](stringtable-resource.md)   | Definiert Zeichenfolgenressourcen. Zeichenfolgenressourcen sind Unicode- oder ASCII-Zeichenfolgen, die aus der ausführbaren Datei geladen werden können.                                                            |
| **TEXTINCLUDE**                               | Eine spezielle Ressource, die von der -Visual C++. Weitere Informationen finden Sie unter [TN035](/cpp/mfc/tn035-using-multiple-resource-files-and-header-files-with-visual-cpp?view=vs-2019).                                        |
| **TYPELIB**                                   | Eine spezielle Ressource, die mit den Linkeroptionen [/TLBID](/cpp/build/reference/tlbid-specify-resource-id-for-typelib?view=vs-2019) und [/TLBOUT](/cpp/build/reference/tlbout-name-dot-tlb-file?view=vs-2019) verwendet wird. |
| [**Benutzerdefiniert**](user-defined-resource.md) | Definiert eine Ressource, die anwendungsspezifische Daten enthält.                                                                                                                     |
| [**VERSIONINFO**](versioninfo-resource.md)   | Definiert eine Versionsinformationsressource. Enthält Informationen wie die Versionsnummer, das vorgesehene Betriebssystem und so weiter.                                                  |
| **Vxd**                                       | Veraltet.                                                                                                                                                                       |



 

Weitere Informationen zu vordefinierten MFC-Ressourcen finden Sie unter [TN023](/cpp/mfc/tn023-standard-mfc-resources?view=vs-2019) und [TN024](/cpp/mfc/tn024-mfc-defined-messages-and-resources?view=vs-2019).

## <a name="controls"></a>Steuerelemente



| Control                                            | Beschreibung                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**AUTO3STATE**](auto3state-control.md)           | Erstellt ein automatisches Kontrollkästchen-Steuerelement mit drei Status.                         |
| [**AUTOCHECKBOX**](autocheckbox-control.md)       | Erstellt ein automatisches Kontrollkästchen-Steuerelement.                                     |
| [**AUTOGRAMMBUTTON**](autoradiobutton-control.md) | Erstellt ein automatisches Optionsfeld-Steuerelement.                                  |
| [**Checkbox**](checkbox-control.md)               | Erstellt ein Kontrollkästchen-Steuerelement.                                                |
| [**Combobox**](combobox-control.md)               | Erstellt ein Kombinationsfeld-Steuerelement.                                                |
| [**Steuerung**](control-control.md)                 | Erstellt ein anwendungsdefiniertes Steuerelement.                                     |
| [**CTEXT**](ctext-control.md)                     | Erstellt ein Steuerelement mit zentriertem Text.                                            |
| [**Defpushbutton**](defpushbutton-control.md)     | Erstellt ein Standard-Pushbutton-Steuerelement.                                       |
| [**Edittext**](edittext-control.md)               | Erstellt ein Bearbeitungssteuer steuerelement.                                                    |
| [**Groupbox**](groupbox-control.md)               | Erstellt ein Gruppenfeld-Steuerelement.                                                |
| [**Symbol**](icon-control.md)                       | Erstellt ein Symbolsteuerzeichen. Dieses Steuerelement ist ein Symbol, das in einem Dialogfeld angezeigt wird. |
| [**Listbox**](listbox-control.md)                 | Erstellt ein Listenfeld-Steuerelement.                                                 |
| [**Ltext**](ltext-control.md)                     | Erstellt ein linksbündig ausgerichtetes Textsteuerfeld.                                        |
| [**PUSHBOX**](pushbox-control.md)                 | Erstellt ein Pushbox-Steuerelement.                                                 |
| [**Pushbutton**](pushbutton-control.md)           | Erstellt ein Schaltflächen-Steuerelement.                                              |
| [**Radiobutton**](radiobutton-control.md)         | Erstellt ein Optionsfeld-Steuerelement.                                             |
| [**Rtext**](rtext-control.md)                     | Erstellt ein rechtsbündiges Steuerelement.                                            |
| [**SCROLLLEISTE**](scrollbar-control.md)             | Erstellt ein Bildlaufleisten-Steuerelement.                                               |
| [**STATE3**](state3-control.md)                   | Erstellt ein Kontrollkästchen-Steuerelement mit drei Status.                                    |



 

## <a name="statements"></a>Anweisungen



| -Anweisung.                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Beschriftung**](caption-statement.md)                 | Legt den Titel für ein Dialogfeld fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Merkmale**](characteristics-statement.md) | Gibt Informationen zu einer Ressource an, die von Tools verwendet werden können, die Ressourcendefinitionsdateien lesen oder schreiben können.                                                                                                                                                                                                                                                                                                                                                                           |
| [**Klasse**](class-statement.md)                     | Legt die Klasse des Dialogfelds fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**EXSTYLE**](exstyle-statement.md)                 | Legt den erweiterten Fensterstil des Dialogfelds fest.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Schriftart**](font-statement.md)                       | Legt die Schriftart fest, mit der das System Text für das Dialogfeld zeichnet.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Sprache**](language-statement.md)               | Legt die Sprache für alle Ressourcen bis zur nächsten [**LANGUAGE-Anweisung**](language-statement.md) oder bis zum Ende der Datei fest. Wenn die **LANGUAGE-Anweisung** vor dem Anfang des Textkörpers einer [**ACCELERATORS-,**](accelerators-resource.md) [**DIALOG-,**](dialog-resource.md) [**MENU-,**](menu-resource.md) [**RCDATA-**](rcdata-resource.md)oder [**STRINGTABLE-Ressourcendefinition**](stringtable-resource.md) angezeigt wird, gilt die angegebene Sprache nur für diese Ressource. |
| [**Menü**](menu-statement.md)                       | Legt das Menü für das Dialogfeld fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Menuitem**](menuitem-statement.md)               | Definiert ein Menüelement.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Stil**](style-statement.md)                     | Legt den Fensterstil für das Dialogfeld fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**Version**](version-statement.md)                 | Gibt Versionsinformationen für eine Ressource an, die von Tools verwendet werden können, die Ressourcendefinitionsdateien lesen oder schreiben können.                                                                                                                                                                                                                                                                                                                                                                     |



 

 

 