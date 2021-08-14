---
title: Resource-Definition-Anweisungen
description: Die Ressourcendefinitionsanweisungen definieren die Ressourcen, die der Ressourcencompiler in die Ressource eingibt (. Res)-Datei.
ms.assetid: f96b8c1e-8188-40b7-8eda-c13b61b8fc41
keywords:
- Ressourcencompiler, Ressourcendefinitionsanweisungen
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

Die Ressourcendefinitionsanweisungen definieren die Ressourcen, die der Ressourcencompiler in die Ressource eingibt (. Res)-Datei. Nach dem . Die RES-Datei ist mit der ausführbaren Datei verknüpft. Die Anwendung kann ihre Ressourcen bei Bedarf zur Laufzeit laden. Alle Ressourcenanweisungen ordnen einer bestimmten Ressource einen identifizierenden Namen oder eine Bestimmte Zahl zu.

Die Ressourcendefinitionsanweisungen können in die folgenden Kategorien unterteilt werden:

-   Ressourcen
-   Steuerelemente
-   Anweisungen

In den folgenden Tabellen werden die Ressourcendefinitionsanweisungen beschrieben.

## <a name="resources"></a>Ressourcen



| Ressource                                      | BESCHREIBUNG                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Beschleuniger**](accelerators-resource.md) | Definiert Tastenkombinationen für die Menütaste.                                                                                                                                                  |
| [**Bitmap**](bitmap-resource.md)             | Definiert eine Bitmap, indem sie benannt und der Name der Datei angegeben wird, die sie enthält. (Um eine bestimmte Bitmap zu verwenden, fordert die Anwendung sie anhand des Namens an.)                          |
| [**Cursor**](cursor-resource.md)             | Definiert einen Cursor oder animierten Cursor, indem er ihn benennt und den Namen der Datei angibt, die ihn enthält. (Um einen bestimmten Cursor zu verwenden, fordert die Anwendung ihn anhand des Namens an.)       |
| [**DIALOG**](dialog-resource.md)             | Definiert eine Vorlage, die eine Anwendung zum Erstellen von Dialogfeldern verwenden kann.                                                                                                          |
| [**Dialogex**](dialogex-resource.md)         | Definiert eine Vorlage, die eine Anwendung zum Erstellen von Dialogfeldern verwenden kann.                                                                                                          |
| [**Schriftart**](font-resource.md)                 | Gibt den Namen einer Datei an, die eine Schriftart enthält.                                                                                                                              |
| [**Html**](html-resource.md)                 | Gibt eine HTML-Datei an.                                                                                                                                                         |
| [**Symbol**](icon-resource.md)                 | Definiert ein Symbol oder ein animiertes Symbol, indem es benannt und der Name der Datei angegeben wird, die es enthält. (Um ein bestimmtes Symbol zu verwenden, fordert die Anwendung es anhand des Namens an.)            |
| [**Menü**](menu-resource.md)                 | Definiert die Darstellung und Funktion eines Menüs.                                                                                                                                  |
| [**MENUEX**](menuex-resource.md)             | Definiert die Darstellung und Funktion eines Menüs.                                                                                                                                  |
| [**MESSAGETABLE**](messagetable-resource.md) | Definiert eine Meldungstabelle, indem sie benannt und der Name der Datei angegeben wird, die sie enthält. Die Datei ist eine binäre Ressourcendatei, die vom Nachrichtencompiler generiert wird.                |
| [**Popup**](popup-resource.md)               | Definiert ein Menüelement, das Menüelemente und Untermenüs enthalten kann.                                                                                                                   |
| **PLUGPLAY**                                  | Veraltet.                                                                                                                                                                       |
| [**Rcdata**](rcdata-resource.md)             | Definiert Datenressourcen. Mit Datenressourcen können Sie Binärdaten in die ausführbare Datei einschließen.                                                                                      |
| [**Stringtable**](stringtable-resource.md)   | Definiert Zeichenfolgenressourcen. Zeichenfolgenressourcen sind Unicode- oder ASCII-Zeichenfolgen, die aus der ausführbaren Datei geladen werden können.                                                            |
| **TEXTINCLUDE**                               | Eine spezielle Ressource, die von Visual C++ interpretiert wird. Weitere Informationen finden Sie unter [TN035.](/cpp/mfc/tn035-using-multiple-resource-files-and-header-files-with-visual-cpp?view=vs-2019)                                        |
| **TYPELIB**                                   | Eine spezielle Ressource, die mit den Linkeroptionen [/TLBID](/cpp/build/reference/tlbid-specify-resource-id-for-typelib?view=vs-2019) und [/TLBOUT](/cpp/build/reference/tlbout-name-dot-tlb-file?view=vs-2019) verwendet wird. |
| [**Benutzerdefiniert**](user-defined-resource.md) | Definiert eine Ressource, die anwendungsspezifische Daten enthält.                                                                                                                     |
| [**VERSIONINFO**](versioninfo-resource.md)   | Definiert eine Versionsinformationsressource. Enthält Informationen wie die Versionsnummer, das beabsichtigte Betriebssystem usw.                                                  |
| **Vxd**                                       | Veraltet.                                                                                                                                                                       |



 

Weitere Informationen zu vordefinierten MFC-Ressourcen finden Sie unter [TN023](/cpp/mfc/tn023-standard-mfc-resources?view=vs-2019) und [TN024.](/cpp/mfc/tn024-mfc-defined-messages-and-resources?view=vs-2019)

## <a name="controls"></a>Steuerelemente



| Control                                            | BESCHREIBUNG                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**AUTO3STATE**](auto3state-control.md)           | Erstellt ein automatisches Kontrollkästchen-Steuerelement mit drei Zuständen.                         |
| [**AUTOCHECKBOX**](autocheckbox-control.md)       | Erstellt ein automatisches Kontrollkästchen-Steuerelement.                                     |
| [**AUTORADIOBUTTON**](autoradiobutton-control.md) | Erstellt ein automatisches Optionsfeld-Steuerelement.                                  |
| [**Checkbox**](checkbox-control.md)               | Erstellt ein Kontrollkästchen-Steuerelement.                                                |
| [**Combobox**](combobox-control.md)               | Erstellt ein Kombinationsfeld-Steuerelement.                                                |
| [**Steuerung**](control-control.md)                 | Erstellt ein anwendungsdefiniertes Steuerelement.                                     |
| [**CTEXT**](ctext-control.md)                     | Erstellt ein zentriertes Textsteuerelement.                                            |
| [**Defpushbutton**](defpushbutton-control.md)     | Erstellt ein Standard-Pushbutton-Steuerelement.                                       |
| [**Edittext**](edittext-control.md)               | Erstellt ein Bearbeitungssteuerelement.                                                    |
| [**Groupbox**](groupbox-control.md)               | Erstellt ein Gruppenfeld-Steuerelement.                                                |
| [**Symbol**](icon-control.md)                       | Erstellt ein Symbolsteuerelement. Dieses Steuerelement ist ein Symbol, das in einem Dialogfeld angezeigt wird. |
| [**Listbox**](listbox-control.md)                 | Erstellt ein Listenfeld-Steuerelement.                                                 |
| [**Ltext**](ltext-control.md)                     | Erstellt ein linksbündig ausgerichtetes Textsteuerelement.                                        |
| [**PUSHBOX**](pushbox-control.md)                 | Erstellt ein Pushbox-Steuerelement.                                                 |
| [**Pushbutton**](pushbutton-control.md)           | Erstellt ein Schaltflächen-Steuerelement.                                              |
| [**Radiobutton**](radiobutton-control.md)         | Erstellt ein Optionsfeld-Steuerelement.                                             |
| [**Rtext**](rtext-control.md)                     | Erstellt ein rechtsbündig ausgerichtetes Steuerelement.                                            |
| [**SCROLLLEISTE**](scrollbar-control.md)             | Erstellt ein Bildlaufleisten-Steuerelement.                                               |
| [**STATE3**](state3-control.md)                   | Erstellt ein Kontrollkästchen-Steuerelement mit drei Zuständen.                                    |



 

## <a name="statements"></a>Anweisungen



| -Anweisung.                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Beschriftung**](caption-statement.md)                 | Legt den Titel für ein Dialogfeld fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Merkmale**](characteristics-statement.md) | Gibt Informationen zu einer Ressource an, die von Einem Tool verwendet werden kann, das Ressourcendefinitionsdateien lesen oder schreiben kann.                                                                                                                                                                                                                                                                                                                                                                           |
| [**Klasse**](class-statement.md)                     | Legt die Klasse des Dialogfelds fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**EXSTYLE**](exstyle-statement.md)                 | Legt den erweiterten Fensterstil des Dialogfelds fest.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Schriftart**](font-statement.md)                       | Legt die Schriftart fest, mit der das System Text für das Dialogfeld zeichnet.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Sprache**](language-statement.md)               | Legt die Sprache für alle Ressourcen auf die nächste [**LANGUAGE-Anweisung**](language-statement.md) oder das Ende der Datei fest. Wenn die **LANGUAGE-Anweisung** vor dem Anfang des Textkörpers einer [**ACCELERATORS-,**](accelerators-resource.md) [**DIALOG-,**](dialog-resource.md) [**MENU-,**](menu-resource.md) [**RCDATA-**](rcdata-resource.md)oder [**STRINGTABLE-Ressourcendefinition**](stringtable-resource.md) angezeigt wird, gilt die angegebene Sprache nur für diese Ressource. |
| [**Menü**](menu-statement.md)                       | Legt das Menü für das Dialogfeld fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Menuitem**](menuitem-statement.md)               | Definiert ein Menüelement.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Stil**](style-statement.md)                     | Legt den Fensterstil für das Dialogfeld fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**Version**](version-statement.md)                 | Gibt Versionsinformationen für eine Ressource an, die von Tools verwendet werden können, die Ressourcendefinitionsdateien lesen oder schreiben können.                                                                                                                                                                                                                                                                                                                                                                     |



 

 

 