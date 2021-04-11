---
title: Resource-Definition-Anweisungen
description: Die Ressourcen Definitions Anweisungen definieren die Ressourcen, die der Ressourcen Compiler in die Ressource einfügt (. Res-Datei).
ms.assetid: f96b8c1e-8188-40b7-8eda-c13b61b8fc41
keywords:
- Ressourcen Compiler, Ressourcen Definitions Anweisungen
- TEXTINCLUDE-Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8887c002bc3564288eb99fdb373ac26c286d1bf7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948729"
---
# <a name="resource-definition-statements"></a>Resource-Definition-Anweisungen

Die Ressourcen Definitions Anweisungen definieren die Ressourcen, die der Ressourcen Compiler in die Ressource einfügt (. Res-Datei). Nach dem. Die res-Datei ist mit der ausführbaren Datei verknüpft. die Anwendung kann Ihre Ressourcen bei Bedarf zur Laufzeit laden. Alle Ressourcen Anweisungen ordnen einen identifizierenden Namen oder eine Identifikationsnummer einer bestimmten Ressource zu.

Die Ressourcen Definitions Anweisungen können in die folgenden Kategorien unterteilt werden:

-   Ressourcen
-   Steuerelemente
-   Anweisungen

In den folgenden Tabellen werden die Ressourcen Definitions Anweisungen beschrieben.

## <a name="resources"></a>Ressourcen



| Resource                                      | BESCHREIBUNG                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Accelerators**](accelerators-resource.md) | Definiert Menü Zugriffstasten.                                                                                                                                                  |
| [**Bitmap**](bitmap-resource.md)             | Definiert eine Bitmap, indem Sie Sie benennt und den Namen der Datei angibt, in der Sie enthalten ist. (Um eine bestimmte Bitmap zu verwenden, fordert die Anwendung Sie anhand des Namens an.)                          |
| [**Hand**](cursor-resource.md)             | Definiert einen Cursor oder einen animierten Cursor, indem er Sie benennt und den Namen der Datei angibt, in der Sie enthalten ist. (Um einen bestimmten Cursor zu verwenden, fordert die Anwendung ihn anhand des Namens an.)       |
| [**Dialog**](dialog-resource.md)             | Definiert eine Vorlage, die von einer Anwendung zum Erstellen von Dialogfeldern verwendet werden kann.                                                                                                          |
| [**DIALOGEX**](dialogex-resource.md)         | Definiert eine Vorlage, die von einer Anwendung zum Erstellen von Dialogfeldern verwendet werden kann.                                                                                                          |
| [**Raster**](font-resource.md)                 | Gibt den Namen einer Datei an, die eine Schriftart enthält.                                                                                                                              |
| [**HTML**](html-resource.md)                 | Gibt eine HTML-Datei an.                                                                                                                                                         |
| [**Angezeigt**](icon-resource.md)                 | Definiert ein Symbol oder animiertes Symbol, indem es benannt wird und den Namen der Datei angibt, in der es enthalten ist. (Um ein bestimmtes Symbol zu verwenden, fordert die Anwendung es anhand des Namens an.)            |
| [**Stehen**](menu-resource.md)                 | Definiert das Aussehen und die Funktion eines Menüs.                                                                                                                                  |
| [**Menuex**](menuex-resource.md)             | Definiert das Aussehen und die Funktion eines Menüs.                                                                                                                                  |
| [**Messagetable**](messagetable-resource.md) | Definiert eine Nachrichten Tabelle, indem Sie Sie benennt und den Namen der Datei angibt, in der Sie enthalten ist. Bei der Datei handelt es sich um eine binäre Ressourcen Datei, die vom Nachrichten Compiler generiert wird.                |
| [**Up**](popup-resource.md)               | Definiert ein Menü Element, das Menü Elemente und Untermenüs enthalten kann.                                                                                                                   |
| **Plugplay**                                  | Veraltet.                                                                                                                                                                       |
| [**RCDATA**](rcdata-resource.md)             | Definiert Datenressourcen. Mit Datenressourcen können Sie Binärdaten in die ausführbare Datei einschließen.                                                                                      |
| [**STRINGTABLE**](stringtable-resource.md)   | Definiert Zeichen folgen Ressourcen. Zeichen folgen Ressourcen sind Unicode-oder ASCII-Zeichen folgen, die aus der ausführbaren Datei geladen werden können.                                                            |
| **TEXTINCLUDE**                               | Eine spezielle Ressource, die von Visual C++ interpretiert wird. Weitere Informationen finden Sie unter [TN035](/cpp/mfc/tn035-using-multiple-resource-files-and-header-files-with-visual-cpp?view=vs-2019).                                        |
| **TYPELIB**                                   | Eine spezielle Ressource, die mit den Linkeroptionen [/TLBID](/cpp/build/reference/tlbid-specify-resource-id-for-typelib?view=vs-2019) und [/TLBOUT](/cpp/build/reference/tlbout-name-dot-tlb-file?view=vs-2019) verwendet wird. |
| [**Benutzer definiert**](user-defined-resource.md) | Definiert eine Ressource, die anwendungsspezifische Daten enthält.                                                                                                                     |
| [**VERSIONINFO**](versioninfo-resource.md)   | Definiert eine Versions Informations Ressource. Enthält Informationen wie die Versionsnummer, das beabsichtigte Betriebssystem usw.                                                  |
| **VXD**                                       | Veraltet.                                                                                                                                                                       |



 

Weitere Informationen zu vordefinierten MFC-Ressourcen finden Sie unter [TN023](/cpp/mfc/tn023-standard-mfc-resources?view=vs-2019) und [TN024](/cpp/mfc/tn024-mfc-defined-messages-and-resources?view=vs-2019).

## <a name="controls"></a>Steuerelemente



| Control                                            | BESCHREIBUNG                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**AUTO3STATE**](auto3state-control.md)           | Erstellt ein automatisches Kontrollkästchen-Steuerelement mit drei Zuständen.                         |
| [**AUTOCHECKBOX**](autocheckbox-control.md)       | Erstellt ein automatisches Kontrollkästchen-Steuerelement.                                     |
| [**AUTORADIOBUTTON**](autoradiobutton-control.md) | Erstellt ein automatisches Optionsfeld-Steuerelement.                                  |
| [**Markieren**](checkbox-control.md)               | Erstellt ein Kontrollkästchen-Steuerelement.                                                |
| [**ComboBox**](combobox-control.md)               | Erstellt ein Kombinations Feld-Steuerelement.                                                |
| [**Steuerelement**](control-control.md)                 | Erstellt ein Anwendungs definiertes Steuerelement.                                     |
| [**CTEXT**](ctext-control.md)                     | Erstellt ein zentriertes Text Steuerelement.                                            |
| [**DEFPUSHBUTTON**](defpushbutton-control.md)     | Erstellt ein Standardmäßiges PUSHBUTTON-Steuerelement.                                       |
| [**EDITTEXT**](edittext-control.md)               | Erstellt ein Bearbeitungs Steuerelement.                                                    |
| [**GroupBox**](groupbox-control.md)               | Erstellt ein Gruppenfeld-Steuerelement.                                                |
| [**Angezeigt**](icon-control.md)                       | Erstellt ein Symbol Steuerelement. Dieses Steuerelement ist ein Symbol, das in einem Dialogfeld angezeigt wird. |
| [**ListBox**](listbox-control.md)                 | Erstellt ein Listenfeld-Steuerelement.                                                 |
| [**LTEXT**](ltext-control.md)                     | Erstellt ein Links Bündiges Text Steuerelement.                                        |
| [**PUSHBOX**](pushbox-control.md)                 | Erstellt ein Steuerelement für die PUSHBOX.                                                 |
| [**PUSHBUTTON**](pushbutton-control.md)           | Erstellt ein Push-Schaltflächen-Steuerelement.                                              |
| [**RadioButton**](radiobutton-control.md)         | Erstellt ein Optionsfeld-Steuerelement.                                             |
| [**Rtext**](rtext-control.md)                     | Erstellt ein rechts Bündiges Steuerelement.                                            |
| [**SCROLLLEISTE**](scrollbar-control.md)             | Erstellt ein ScrollBar-Steuerelement.                                               |
| [**STATE3**](state3-control.md)                   | Erstellt ein Kontrollkästchen-Steuerelement mit drei Zuständen.                                    |



 

## <a name="statements"></a>Anweisungen



| -Anweisung.                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Unter**](caption-statement.md)                 | Legt den Titel für ein Dialogfeld fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Charakteristik**](characteristics-statement.md) | Gibt Informationen zu einer Ressource an, die von einem Tool verwendet werden kann, mit dem Ressourcen Definitions Dateien gelesen oder geschrieben werden können.                                                                                                                                                                                                                                                                                                                                                                           |
| [**Klassi**](class-statement.md)                     | Legt die Klasse des Dialog Felds fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ExStyle**](exstyle-statement.md)                 | Legt den erweiterten Fenster Stil des Dialog Felds fest.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Raster**](font-statement.md)                       | Legt die Schriftart fest, mit der das System Text für das Dialogfeld zeichnet.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Kurse**](language-statement.md)               | Legt die Sprache für alle Ressourcen bis zur nächsten [**sprach**](language-statement.md) Anweisung oder am Ende der Datei fest. Wenn die **Language** -Anweisung vor dem Anfang des Texts einer Zugriffstasten [**-,**](accelerators-resource.md) [**Dialog**](dialog-resource.md)-, [**Menü**](menu-resource.md)-, [**RCDATA**](rcdata-resource.md)-oder [**STRINGTABLE**](stringtable-resource.md) -Ressourcendefinition angezeigt wird, gilt die angegebene Sprache nur für diese Ressource. |
| [**Stehen**](menu-statement.md)                       | Legt das Menü für das Dialogfeld fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**MENUITEM**](menuitem-statement.md)               | Definiert ein Menü Element.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Vorbild**](style-statement.md)                     | Legt den Fenster Stil für das Dialogfeld fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**Version**](version-statement.md)                 | Gibt Versionsinformationen für eine Ressource an, die von einem Tool verwendet werden kann, mit dem Ressourcen Definitions Dateien gelesen oder geschrieben werden können.                                                                                                                                                                                                                                                                                                                                                                     |



 

 

 