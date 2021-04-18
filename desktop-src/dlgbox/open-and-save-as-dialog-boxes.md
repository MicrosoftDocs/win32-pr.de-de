---
title: Dialog Felder "Öffnen" und "Speichern unter"
description: Im Dialogfeld öffnen können Benutzer das Laufwerk, das Verzeichnis und den Namen einer Datei oder einer Gruppe von Dateien angeben, die geöffnet werden sollen.
ms.assetid: 5676ca9d-daca-40bf-8881-def2ff841c58
keywords:
- Allgemeine Dialog Feld Bibliothek
- Allgemeine Dialogfelder
- Dialogfeld Öffnen
- Speichern unter (Dialogfeld)
- Dialogfeld "Öffnen" wird angepasst
- Dialogfeld "Speichern unter" anpassen
- Dialogfelder, öffnen
- Dialogfelder, speichern unter
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: bc2977a5f91abde32a78c722a7a7c7b6b4a23ffd
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106364407"
---
# <a name="open-and-save-as-dialog-boxes"></a>Dialog Felder "Öffnen" und "Speichern unter"

> [!NOTE]
> Die Funktion " [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) " wird im [Beispiel "Datei wird verwendet](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse)" veranschaulicht.

\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt. Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]

Im Dialogfeld **Öffnen** können Benutzer das Laufwerk, das Verzeichnis und den Namen einer Datei oder einer Gruppe von Dateien angeben, die geöffnet werden sollen. Sie erstellen und zeigen ein Dialogfeld **Öffnen** an, indem Sie eine [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur initialisieren und die Struktur an die [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) -Funktion übergeben.

Im Dialogfeld **Speichern** unter können Benutzer das Laufwerk, das Verzeichnis und den Namen einer Datei angeben, die gespeichert werden soll. Das Dialogfeld **Speichern** unter wird erstellt und angezeigt, indem eine [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur initialisiert und die Struktur an die [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) -Funktion übergeben wird.

Die Dialogfelder "im Explorer-Format **Öffnen** " und " **Speichern** unter" bieten Funktionen für die Benutzeroberfläche, die dem Windows-Explorer ähneln. Das System unterstützt jedoch weiterhin alte Dialogfelder " **Öffnen** " und " **Speichern** unter" für Anwendungen, die mit der Benutzeroberfläche im alten Stil konsistent sein müssen.

Zusätzlich zu den Unterschieden in der Darstellung unterscheiden sich die Dialogfelder im Explorer-Stil und im alten Stil bei der Verwendung von benutzerdefinierten Vorlagen und Hook-Prozeduren zum Anpassen der Dialogfelder. Die Dialogfelder im Explorer-Stil und im alten Stil weisen jedoch das gleiche Verhalten für die meisten grundlegenden Vorgänge auf, wie z. b. das Angeben eines Datei namens Filters, das Überprüfen der Eingabe des Benutzers und das erhalten des vom Benutzer angegebenen Datei namens. Weitere Informationen zu den Dialogfeldern im Explorer-Stil und im alten Stil finden Sie im [Dialogfeld "öffnen und speichern](#open-and-save-as-dialog-box-customization)unter".

Die folgende Abbildung zeigt ein typisches Dialogfeld zum **Öffnen** von Explorer-Stil.

![Datei öffnen (Dialogfeld)](images/opendialogboxxp.png)

Die folgende Abbildung zeigt ein typisches Dialogfeld " **Speichern** unter" im Explorer-Format.

![Datei speichern (Dialogfeld)](images/saveasdialogboxxp.png)

Wenn der Benutzer einen Dateinamen angibt und auf die Schaltfläche **OK** klickt, gibt [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) oder [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) den Wert **true** zurück. Der Puffer, auf den der **lpstraufile** -Member der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur verweist, enthält den vollständigen Pfad und Dateinamen, die vom Benutzer angegeben werden.

Wenn der Benutzer das Dialogfeld " **Öffnen** " oder " **Speichern** unter" abbricht oder ein Fehler auftritt, gibt die Funktion " **false**" zurück. Um die Ursache des Fehlers zu ermitteln, rufen Sie die [**kommdlgextendecoderror**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) -Funktion auf, um den erweiterten Fehlerwert abzurufen. Wenn der **lpstrinfile** -Puffer zu klein ist, um den vollständigen Namen zu erhalten, gibt **commdlgextendederror** **fnerr \_ bufferdeosmall** zurück, und die ersten 2 Bytes des Puffers, auf den der **lpstrinfile** -Member verweist, werden auf einen ganzzahligen Wert festgelegt, der die Größe angibt, die zum Empfangen des vollständigen

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Dateinamen und Verzeichnisse](#file-names-and-directories)
-   [Filter](#filters)
-   [Datei-und Verzeichnis Validierung](#file-and-directory-validation)
-   [Öffnen und speichern unter (Dialog Feld)](#open-and-save-as-dialog-box-customization)
-   [Hook-Verfahren im Explorer-Stil](#explorer-style-hook-procedures)
-   [Benutzerdefinierte Vorlagen im Explorer-Stil](#explorer-style-custom-templates)
-   [Steuerelement Bezeichner im Explorer-Stil](#explorer-style-control-identifiers)
-   [Anpassen von Old-Style-Dialog Feldern](#customizing-old-style-dialog-boxes)

## <a name="file-names-and-directories"></a>Dateinamen und Verzeichnisse

Die Informationen in diesem Abschnitt gelten für die Dialogfelder "Explorer" und " **Öffnen** " und " **Speichern** unter" im alten Stil.

Vor dem Aufrufen der Funktionen [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) oder [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) muss das **lpstrefile** -Member der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur auf den Puffer zeigen, um den Dateinamen zu erhalten. Der **nmaxfile** -Member muss die Größe des **lpstraufile** -Puffers in Zeichen angeben. Für eine ANSI-Funktion ist dies die Anzahl von Bytes, aber für eine Unicode-Funktion ist dies die Anzahl der Zeichen.

Wenn der Benutzer einen Dateinamen angibt und auf die Schaltfläche **OK** klickt, werden im Dialogfeld das ausgewählte Laufwerk, das Verzeichnis und der Dateiname in den **lpstraufile** -Puffer kopiert. Die-Funktion legt auch die Member **nfileoffset** und **nfileextension** auf die Offsets (in Zeichen) vom Anfang des Puffers auf den Dateinamen und die Dateinamenerweiterung fest.

Wenn Sie nur den Dateinamen und die Erweiterung abrufen möchten, legen Sie den **lpstraufiletitle** -Member so fest, dass er auf einen Puffer verweist, und legen Sie den **nmaxfiletitle** -Member auf die Größe des Puffers in Zeichen fest. Alternativ können Sie den **lpstraufile** -Puffer in einem Aufrufen der [**GetFileTitle**](/windows/desktop/api/Commdlg/nf-commdlg-getfiletitlea) -Funktion übergeben, um den anzeigen amen der ausgewählten Datei abzurufen. Beachten Sie jedoch, dass der von **GetFileTitle** zurückgegebene Dateiname nur eine Erweiterung enthält, wenn dies die Benutzereinstellung für die Anzeige von Dateinamen ist.

Im Dialogfeld wird das aktuelle Verzeichnis für den aufrufenden Prozess als Ausgangs Verzeichnis verwendet, aus dem Dateien und Verzeichnisse angezeigt werden. Verwenden Sie die Funktionen [**GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) und [**SetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) , um das aktuelle Verzeichnis eines Prozesses zu erhalten und zu ändern. Verwenden Sie zum Angeben eines anderen ursprünglichen Verzeichnisses, ohne das aktuelle Verzeichnis zu ändern, das **lpstrauinitialdir** -Element, um den Namen eines Verzeichnisses anzugeben. Im Dialogfeld wird automatisch das aktuelle Verzeichnis geändert, wenn der Benutzer ein anderes Laufwerk oder Verzeichnis auswählt. Um zu verhindern, dass das Dialogfeld das aktuelle Verzeichnis ändert, legen Sie das **ofn \_ nochangedir** -Flag fest. Dieses Flag verhindert nicht, dass der Benutzerverzeichnisse ändert, um nach einer Datei zu suchen.

Zum Angeben einer Standarddatei Namen Erweiterung verwenden Sie den **lpstraudefext** -Member. Wenn der Benutzer einen Dateinamen angibt, der keine Erweiterung enthält, wird im Dialogfeld die Standard Erweiterung hinzugefügt. Wenn Sie eine Standard Erweiterung angeben und der Benutzer einen Dateinamen mit einer anderen Erweiterung angibt, legt das Dialogfeld das **ofn \_ extensiondifferent** -Flag fest.

Damit der Benutzer mehr als eine Datei aus einem Verzeichnis auswählen kann, legen Sie das ofn-Flag " **\_ AllowMultiSelect** " fest. Aus Kompatibilitätsgründen mit älteren Anwendungen wird im Dialogfeld standardmäßige Mehrfachauswahl die Benutzeroberfläche im alten Stil verwendet. Um das Dialogfeld Mehrfachauswahl im Explorer-Format anzuzeigen, müssen Sie auch das **ofn- \_ Explorer** -Flag festlegen.

Wenn der Benutzer mehr als eine Datei auswählt, gibt der Puffer, auf den der **lpstrinfile** -Member verweist, den Pfad zum aktuellen Verzeichnis gefolgt von den Dateinamen der ausgewählten Dateien zurück. Der **nfileoffset** -Member ist der Offset zum ersten Dateinamen, und der **nfileextension** -Member wird nicht verwendet. In der folgenden Tabelle werden die Unterschiede zwischen explorerstil-und alten Dialogfeldern beim Zurückgeben von mehreren Dateinamen beschrieben.



| Dialog Feld Stil            | BESCHREIBUNG                                                                                                                                                                                                               |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dialogfelder im Explorer-Stil | Die Verzeichnis-und Dateinamen Zeichenfolgen sind durch **null** getrennte Zeichen folgen mit einem zusätzlichen **null** -Zeichen nach dem letzten Dateinamen. Dieses Format ermöglicht es den Dialogfeldern im Explorer-Stil, lange Dateinamen zurückzugeben, die Leerzeichen enthalten. |
| Alte Dialogfelder      | Die Verzeichnis-und Dateinamen Zeichenfolgen werden durch Leerzeichen voneinander getrennt. Für Dateinamen mit Leerzeichen verwendet die Funktion kurze Dateinamen.                                                                                              |



 

Sie können die [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) -Funktion verwenden, um zwischen langen und kurzen Dateinamen zu konvertieren.

Wenn Sie " **ofn \_ AllowMultiSelect** " angeben und der Benutzer nur eine Datei auswählt, enthält die **LpstrFile** -Zeichenfolge kein Trennzeichen zwischen dem Pfad und dem Dateinamen.

## <a name="filters"></a>Filter

Die Informationen in diesem Abschnitt gelten für die Dialogfelder "Explorer" und "altes Format **Öffnen** " und " **Speichern** unter".

Sie können Dateinamen Filter bereitstellen, um dem Benutzer zu helfen, die Dateinamen einzuschränken, die im Dialogfeld angezeigt werden. Ein Datei namens Filter besteht aus einem Paar von auf NULL endenden Zeichen folgen, einer Beschreibung und einem Muster, das jeweils mit dem anderen verkettet ist. Im Dialogfeld wird die Beschreibung angezeigt, mit der der Benutzer den zu verwendenden Filter auswählen können. Außerdem wird das Muster verwendet, um die anzuzeigenden Dateien auszuwählen.

Zum Angeben der Filter legen Sie den **lpstraufilter** -Member der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur so fest, dass er auf einen Puffer verweist, der ein Array von Zeichen folgen Paaren enthält. Auf die letzte Zeichenfolge im Array muss ein zusätzliches NULL Zeichen folgen.

Eine Muster Zeichenfolge kann eine Kombination aus gültigen Dateinamen Zeichen und dem Sternchen ( \* ) sein. Das Sternchen ist ein Platzhalter, der eine beliebige Kombination gültiger Dateinamen Zeichen darstellt. Im Dialogfeld werden nur die Dateien angezeigt, die dem Muster entsprechen. Wenn Sie mehrere Muster für dieselbe Beschreibung angeben möchten, müssen Sie ein Semikolon verwenden (;) , wenn die Muster getrennt werden sollen. Beachten Sie, dass Leerzeichen in der Muster Zeichenfolge unerwartete Ergebnisse verursachen können.

Im folgenden Code Fragment werden zwei Filter angegeben. Der Filter mit der Beschreibung "Source" weist zwei Muster auf. Wenn der Benutzer diesen Filter auswählt, werden im Dialogfeld nur Dateien angezeigt, die über das verfügen. C und. CXX-Erweiterungen. Beachten Sie, dass in der Programmiersprache C eine Zeichenfolge, die in doppelte Anführungszeichen eingeschlossen ist, auf NULL endet.


```
OPENFILENAME ofn;       // common dialog box structure

ofn.lpstrFilter = "Source\0*.C;*.CXX\0All\0*.*\0"
ofn.nFilterIndex = 1;
```



Der **nfilterindex** -Member der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur gibt einen Index an, der angibt, welcher Filter zuerst vom Dialogfeld verwendet wird. Der erste Filter im Puffer weist den Index 1, den zweiten 2 usw. auf. Wenn der Benutzer den Filter während der Verwendung des Dialog Felds ändert, wird der **nfilterindex** -Member bei der Rückgabe auf den Index des ausgewählten Filters festgelegt.

Sie können einen benutzerdefinierten Filter erstellen, indem Sie den **lpstraucustomfilter** -Member auf die Adresse eines Puffers festlegen, der einen einzelnen Filter enthält, und indem Sie den **nmaxcustfilter** -Member auf die Größe des Puffers in Zeichen oder Bytes festlegen. Im Dialogfeld wird der benutzerdefinierte Filter immer am Anfang der Filterliste platziert, und bei der Rückgabe wird der Musterteil des Filters immer mit dem Muster des Filters aktualisiert, der vom Benutzer ausgewählt wurde.

In Dialogfeldern im Explorer-Stil kann sich die Standard Erweiterung ändern, wenn der Benutzer einen anderen Filter auswählt. , Wenn der Benutzer einen Filter auswählt, dessen erstes Muster das Formular ist \* .*xxx* (das heißt, die Erweiterung enthält kein Platzhalter Zeichen). das Dialogfeld verwendet *xxx* als Standard Erweiterung. Dies tritt nur dann auf, wenn Sie im **lpstraudefext** -Member der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur eine Standard Erweiterung angegeben haben. Beispielsweise, wenn der Benutzer "Quelle 0" auswählt \\ \* . C; \* . CXX \\ 0 "Filter, die Standard Erweiterung wird in" C "geändert. Wenn Sie den Filter jedoch als "Quelle 0" definiert \\ haben \* . C \* \\ 0 ", die Standard Erweiterung würde sich nicht ändern, da die Erweiterung einen Platzhalter enthält.

Die [**CDN \_ includeitem**](cdn-includeitem.md) -Benachrichtigungs Meldung bietet eine weitere Möglichkeit, die Namen zu filtern, die im Dialogfeld angezeigt werden. Um diese Meldung zu verwenden, geben Sie eine [**ofnhuokproc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) -Hook-Prozedur an, und geben Sie das **ofn \_ enableinclubezeichtifisflag** in der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur an, wenn Sie das Dialogfeld erstellen. Jedes Mal, wenn der Benutzer einen Ordner öffnet, sendet das Dialogfeld für jedes Element im neu geöffneten Ordner eine **CDN- \_ includeitem** -Benachrichtigung an Ihre Hook-Prozedur. Der Rückgabewert der Hook-Prozedur gibt an, ob das Dialogfeld das Element in der Elementliste des Ordners anzeigen soll.

## <a name="file-and-directory-validation"></a>Datei-und Verzeichnis Validierung

Sofern nicht anders angegeben, gelten die Informationen in diesem Abschnitt sowohl für Explorer-als auch für die Dialogfelder **Öffnen** und **Speichern** unter im alten Stil.

Im Dialogfeld werden vom Benutzer typisierte Dateinamen automatisch überprüft, um sicherzustellen, dass die Namen nur gültige Zeichen enthalten. Um die Überprüfung der Datei namens Zeichen zu überschreiben, legen Sie das **ofn \_ novalidate** -Flag fest.

Um zu erzwingen, dass das Dialogfeld überprüft, ob der Benutzer den Namen einer vorhandenen Datei angegeben hat, legen Sie das Flag **ofn \_ filemustexist** fest. Um die Überprüfung zu erzwingen, dass der angegebene Pfad vorhanden ist, legen Sie das Flag **ofn \_ pathmustexist** fest. Wenn Sie das Flag **ofn \_ deateprompt** festlegen, wird der Benutzer im Dialogfeld zur Eingabe der Berechtigung aufgefordert, eine nicht vorhandene Datei zu erstellen. Wenn dieses Flag festgelegt ist und der Benutzer eine neue Datei erstellt, wird das Dialogfeld geschlossen, und die Funktion gibt den angegebenen Namen zurück. Andernfalls bleibt das Dialogfeld geöffnet.

Wenn Sie das Dialogfeld **Speichern** unter verwenden, können Sie das Dialogfeld weiterleiten, um den Benutzer zur Eingabe der Berechtigung zum Überschreiben einer vorhandenen Datei aufzufordern, indem Sie das Flag **ofn \_ xx-prompt** festlegen.

Standardmäßig wird im Dialogfeld eine Testdatei der Länge 0 (null) erstellt, um zu bestimmen, ob eine neue Datei im ausgewählten Verzeichnis erstellt werden kann. Um die Erstellung dieser Testdatei zu verhindern, legen Sie das **ofn \_ notestfilecreate** -Flag fest.

Wenn Sie eine Hook-Prozedur aktivieren, wird das Hook-Verfahren im Dialogfeld benachrichtigt, wenn für den vom Benutzer angegebenen Dateinamen eine Netzwerkfreigabe Verletzung auftritt. Wenn Sie das Flag **ofn \_ Explorer** festlegen, sendet das Dialogfeld die [**CDN- \_ shareverletzungs**](cdn-shareviolation.md) -Nachricht an die Hook-Prozedur. Wenn Sie den **ofn- \_ Explorer** nicht festlegen, sendet das Dialogfeld die registrierte [**sharevistring**](sharevistring.md) -Nachricht an die Hook-Prozedur. Um zu verhindern, dass das Dialogfeld Benachrichtigungen für Freigabe Verletzungen sendet, legen Sie das **ofn \_ shareaware** -Flag fest.

Wenn der Benutzer das Kontrollkästchen Schreibgeschützt aktiviert, **legt das Dialogfeld \_ das Flag "** schreibgeschützt" bei Rückgabe fest. Wenn Sie das Kontrollkästchen als schreibgeschützt **Öffnen** ausblenden möchten, legen Sie das Flag **ofn \_ hidereadonly** fest. Um zu verhindern, dass das Dialogfeld Namen vorhandener Dateien zurückgibt, die über das schreibgeschützte Attribut verfügen, legen Sie das **ofn \_ noreadonlyreturn** -Flag fest.

Legen Sie den **ofn \_ nodereferencelinks** -Wert fest, um zu verhindern, dass das Dialogfeld Link Dateien dereferenzieren kann. In diesem Fall wird im Dialogfeld anstelle des Namens der Datei, auf die die Linkdatei verweist, der Name der Linkdatei zurückgegeben.

## <a name="open-and-save-as-dialog-box-customization"></a>Öffnen und speichern unter (Dialog Feld)

Sie können ein Dialogfeld " **Öffnen** " oder " **Speichern** unter" anpassen, indem Sie eine Hook-Prozedur, eine benutzerdefinierte Vorlage oder beides bereitstellen. Die Explorer-und alten Versionen der Dialogfelder unterscheiden sich jedoch bei der Verwendung von benutzerdefinierten Vorlagen und Hook-Prozeduren.

Weitere Informationen zum Anpassen eines Explorer-Dialog Felds finden Sie unter [Hook-Prozeduren im Explorer-](#explorer-style-hook-procedures)Stil, [benutzerdefinierte Vorlagen im Explorer-](#explorer-style-custom-templates)Stil und [Steuerelement-](#explorer-style-control-identifiers)IDs im Explorer-Stil. Weitere Informationen zum Anpassen eines Dialog Felds für eine alte Art finden Sie unter [Anpassen Old-Style Dialogfeldern](#customizing-old-style-dialog-boxes).

In der folgenden Tabelle werden die Unterschiede zwischen den beiden Stilen zusammengefasst.



| Anpassung                  | BESCHREIBUNG                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hook-Prozedur im Explorer-Stil  | Die Hook-Prozedur empfängt Benachrichtigungs Meldungen, die über das allgemeine Dialogfeld gesendet werden, sowie Meldungen für alle zusätzlichen Steuerelemente, die Sie durch Angabe einer untergeordneten Dialogfeld Vorlage definiert haben Die Hook-Prozedur empfängt keine Nachrichten für die Standard Steuerelemente des Standard Dialogfelds. |
| Benutzerdefinierte Vorlage im Explorer-Stil | Das System verwendet die benutzerdefinierte Vorlage, um ein untergeordnetes Dialogfeld zu erstellen. Die Vorlage kann zusätzliche Steuerelemente definieren und den Speicherort des Clusters von Standard Steuerelementen angeben. Die benutzerdefinierte Vorlage ersetzt nicht die Standardvorlage.                                          |
| Hook-Prozedur im alten Stil       | Die Hook-Prozedur empfängt alle Nachrichten, die an das Dialogfeld gesendet werden, einschließlich Meldungen für die Standard Steuerelemente und alle benutzerdefinierten Steuerelemente. Die Hook-Prozedur empfängt auch registrierte Nachrichten, die vom Dialogfeld "Allgemein" gesendet werden.                                                         |
| Benutzerdefinierte Vorlage im alten Stil      | Die benutzerdefinierte Vorlage ersetzt die Standardvorlage. Erstellen Sie die benutzerdefinierte Vorlage, indem Sie die in der Datei "FileOpen. Dlg" angegebene Standardvorlage ändern.                                                                                                                                  |



 

Der Standard Titel für Dialogfelder im Explorer-Stil und im alten Stil ist entweder "**Öffnen**" oder "**Speichern** unter". Um den Titel zu ändern, geben Sie den neuen Titel im **lpstrintitle** -Member der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur an.

Die Registrierungs Struktur des **aktuellen HKEY- \_ \_ Benutzers** eines Benutzers kann Werte enthalten, die den Inhalt der Dialogfelder **Öffnen** und **Speichern** unter im Explorer-Stil anpassen. Diese Registrierungseinträge wirken sich nur auf die Dialogfelder aus, die für den der Registrierungs Struktur zugeordneten Benutzer angezeigt werden.

Um die Funktionen der Dialogfelder Explorer-Stil **Öffnen** und **Speichern** unter auszublenden, kann ein Administrator die Werte in der folgenden Tabelle unter diesem Unterschlüssel festlegen:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Comdlg32
```



| Wertname       | Wert | Bedeutung                                  |
|------------------|-------|------------------------------------------|
| **Noplacesbar**  | 1     | Blendet die leisten Leiste aus.                    |
| **Noflemru**    | 1     | Blendet die Liste der zuletzt verwendeten (MRU) aus. |
| **Nobackbutton** | 1     | Blendet die Schaltfläche **zurück** aus.               |



 

Der Inhalt der Leiste " **Plätze** " wird durch den Inhalt des folgenden unter Schlüssels bestimmt:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Comdlg32
                     Placesbar
```

Derzeit können nur fünf Einträge unter diesem Schlüssel vorhanden sein, und der Wert/Name-Index ist NULL basiert. Die Namen für die Einträge sollten Place0, Place1, place2, Place3 und Place4 lauten. Die Werte der Einträge können " **reg \_ DWORD**", " **reg \_ SZ**" oder " **reg \_ Expand \_ SZ** values" lauten, mit denen die Orte identifiziert werden, die in die leisten Leiste eingeschlossen werden sollen



| Werttyp                         | Bedeutung                                                                                                   |
|------------------------------------|-----------------------------------------------------------------------------------------------------------|
| **REG \_ DWORD**                     | Ein CSIDL-Wert, der einen Ordner identifiziert. Eine Liste der CSIDL-Werte finden Sie unter [**CSIDL Values**](../shell/csidl.md). |
| **Reg \_ SZ** oder **reg \_ Expand \_ SZ** | Eine NULL-terminierte Zeichenfolge, die einen gültigen Pfad angibt.                                                     |



 

## <a name="explorer-style-hook-procedures"></a>Explorer-Style Hook-Verfahren

Sie können das Dialogfeld Explorer-Stil **Öffnen** oder **Speichern** unter Anpassen, indem Sie eine Hook-Prozedur, eine benutzerdefinierte Vorlage oder beides bereitstellen. Wenn Sie eine Hook-Prozedur für ein Dialogfeld im Explorer-Format bereitstellen, erstellt das System ein Dialogfeld, das ein untergeordnetes Element des Standard Dialogfelds ist. Die Hook-Prozedur fungiert als Dialogfeld Prozedur für das untergeordnete Dialogfeld. Dieses untergeordnete Dialogfeld basiert auf der benutzerdefinierten Vorlage oder auf einer Standardvorlage, wenn keine Angabe erfolgt. Weitere Informationen finden Sie unter [benutzerdefinierte Vorlagen im Explorer-Stil](#explorer-style-custom-templates).

Verwenden Sie die [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur, wenn Sie das Dialogfeld erstellen, um eine Hook-Prozedur für ein Dialogfeld " **Öffnen** " oder " **Speichern** unter" im Explorer-Format zu aktivieren. Legen Sie **die ofn-Flags \_ ENABLEHOOK** und **ofn \_ Explorer** im **Flags** -Member fest, und geben Sie die Adresse einer [**ofnhuokproc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) -Hook-Prozedur im **lpfnhook** -Member an. Wenn Sie eine Hook-Prozedur bereitstellen und das **ofn- \_ Explorer** -Flag weglassen, müssen Sie eine [**ofnhuokprocoldstyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) -Hook-Prozedur verwenden, und Sie erhalten die Benutzeroberfläche im alten Stil. Weitere Informationen finden Sie unter [Anpassen Old-Style Dialog Feldern](#customizing-old-style-dialog-boxes).

Eine Hook-Prozedur im Explorer-Stil empfängt eine Reihe von Nachrichten, während das Dialogfeld geöffnet ist. Dabei handelt es sich z. B. um:

-   Die " [**WM \_ InitDialog**](wm-initdialog.md) "-Meldung und andere Standard Dialogfeld-Meldungen, wie z. b. die Steuer Meldung " [**WM \_ ctlcolordlg**](wm-ctlcolordlg.md) "
-   Ein Satz von [**WM \_**](../controls/wm-notify.md) -Benachrichtigungs Meldungen, die Aktionen angeben, die vom Benutzer oder von anderen Dialogfeld Ereignissen ausgeführt wurden.
-   Meldungen für alle zusätzlichen Steuerelemente, die Sie definiert haben, indem Sie eine untergeordnete Dialogfeld Vorlage angeben.

Außerdem gibt es eine Reihe von Nachrichten, die Sie an ein Dialogfeld im Explorer-Stil senden können, um Informationen zu erhalten oder um das Verhalten und die Darstellung des Dialog Felds zu steuern.

Wenn Sie eine Hook-Prozedur für ein Dialogfeld im Explorer-Format bereitstellen, wird durch die Standard Dialogfeld Prozedur ein untergeordnetes Dialogfeld erstellt, wenn die [**WM- \_ InitDialog**](wm-initdialog.md) -Nachricht von der Standard Dialogfelder verarbeitet wird. Die Hook-Prozedur fungiert als Dialogfeld Prozedur für das untergeordnete Dialogfeld. Zu diesem Zeitpunkt empfängt die Hook-Prozedur eine eigene **WM \_ InitDialog** -Nachricht mit dem *LPARAM* -Parameter, der auf die Adresse der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur festgelegt ist, die zum Initialisieren des Dialog Felds verwendet wird. Nachdem das untergeordnete Dialogfeld die Verarbeitung der eigenen **WM- \_ InitDialog** -Nachricht abgeschlossen hat, verschiebt die Standard Dialogfeld Prozedur bei Bedarf die Standard Steuerelemente, um Platz für alle zusätzlichen Steuerelemente des untergeordneten Dialog Felds zu schaffen. Die Standard Dialogfeld Prozedur sendet dann die [**CDN \_ initdone**](cdn-initdone.md) -Benachrichtigungs Meldung an die Hook-Prozedur.

Die Hook-Prozedur [**empfängt \_ WM**](../controls/wm-notify.md) -Benachrichtigungs Meldungen, die angeben, welche Aktionen der Benutzer im Dialogfeld durchgeführt hat. Sie können einige dieser Meldungen verwenden, um das Verhalten des Dialog Felds zu steuern. Die Hook-Prozedur empfängt z. b. die [**CDN- \_ FileOk**](cdn-fileok.md) -Nachricht, wenn der Benutzer einen Dateinamen auswählt und auf die Schaltfläche **OK** klickt. Als Antwort auf diese Nachricht kann die Hook-Prozedur die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion verwenden, um den ausgewählten Namen abzulehnen, und das Dialogfeld erzwingen, dass das Dialogfeld geöffnet bleibt.

Der *LPARAM* -Parameter für jede [**WM- \_ Benachrichtigungs**](../controls/wm-notify.md) Meldung ist ein Zeiger auf eine [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -oder [**ofnotifyex**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) -Struktur, die die Aktion definiert. Das **Code** Element im-Header dieser Struktur enthält eine der folgenden Benachrichtigungs Meldungen.



| Nachricht                                           | Bedeutung                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CDN- \_ Datei OK**](cdn-fileok.md)                 | Der Benutzer hat auf die Schaltfläche **OK** geklickt. Das Dialogfeld wird geschlossen.                                                                                                                                                                                                                          |
| [**CDN- \_ FolderChange**](cdn-folderchange.md)     | Der Benutzer hat einen neuen Ordner oder ein neues Verzeichnis geöffnet.                                                                                                                                                                                                                                                     |
| [**CDN- \_ Hilfe**](cdn-help.md)                     | Der Benutzer hat auf die Schaltfläche " **Hilfe** " geklickt.                                                                                                                                                                                                                                                          |
| [**CDN \_ includeitem**](cdn-includeitem.md)       | Bestimmt, ob ein Element angezeigt werden soll. Wenn der Benutzer einen neuen Ordner oder ein neues Verzeichnis öffnet, sendet das System diese Benachrichtigung für jedes Element im Ordner oder Verzeichnis. Das System sendet diese Benachrichtigung nur dann, wenn das **ofn \_ enableinclubezeichtify** -Flag festgelegt wurde.                          |
| [**CDN \_ initdone**](cdn-initdone.md)             | Das System hat die Initialisierung des Dialog Felds abgeschlossen, und das Dialogfeld hat die Verarbeitung der " [**WM \_ InitDialog**](wm-initdialog.md) "-Meldung abgeschlossen. Außerdem hat das System das Anordnen von Steuerelementen im Dialogfeld "Allgemein" abgeschlossen, um Platz für die Steuerelemente des untergeordneten Dialog Felds (sofern vorhanden) zu schaffen. |
| [**CDN \_ selChange**](cdn-selchange.md)           | Der Benutzer hat eine neue Datei oder einen neuen Ordner in der Datei Liste ausgewählt.                                                                                                                                                                                                                                     |
| [**CDN- \_ share-Verletzung**](cdn-shareviolation.md) | Im Dialogfeld Allgemein ist eine Freigabe Verletzung der Datei aufgetreten, die zurückgegeben werden soll.                                                                                                                                                                                                        |
| [**CDN- \_ Typänderung**](cdn-typechange.md)         | Der Benutzer hat einen neuen Dateityp aus der Liste der Dateitypen ausgewählt.                                                                                                                                                                                                                                 |



 

Diese [**WM \_ -Benachrichtigungs**](../controls/wm-notify.md) Meldungen ersetzen die registrierten Nachrichten [**fileokstring**](fileokstring.md), [**lbselchstring**](lbselchstring.md), [**sharevistring**](sharevistring.md)und [**helpmsgstring**](helpmsgstring.md) , die von früheren Versionen der Dialogfelder **Öffnen** und **Speichern** unter verwendet werden. Die Hook-Prozedur empfängt jedoch auch die abgeleitete Nachricht nach der **WM- \_ Benachrichtigungs** Meldung, wenn die **WM- \_ Benachrichtigungs** Verarbeitung nicht " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) " verwendet, um einen **\_ msgresult** -Wert ungleich 0 (null) festzulegen.

Zum Abrufen von Informationen über den Status des Dialog Felds oder zum Steuern des Verhaltens und der Darstellung des Dialog Felds kann die Hook-Prozedur die folgenden Meldungen an das Dialogfeld senden.



| Nachricht                                             | Bedeutung                                                                                                                                                                                                                  |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CDM \_ GetFilePath**](cdm-getfilepath.md)         | Ruft den Pfad und den Dateinamen der ausgewählten Datei ab.                                                                                                                                                                   |
| [**CDM \_ getfolderidlist**](cdm-getfolderidlist.md) | Ruft die Liste der Element Bezeichner ab, die dem aktuellen Ordner entspricht, der vom Dialogfeld geöffnet wurde. Weitere Informationen zu elementbezeichnerlisten finden [Sie unter Einführung in den Shellnamespace](/windows/desktop/shell/namespace-intro). |
| [**CDM \_ GetFolderPath**](cdm-getfolderpath.md)     | Ruft den Pfad des aktuellen Ordners oder Verzeichnisses für das Dialogfeld ab.                                                                                                                                                |
| [**CDM \_ getSpec**](cdm-getspec.md)                 | Ruft den Dateinamen (ohne den Pfad) der Datei ab, die derzeit im Dialogfeld ausgewählt ist.                                                                                                                       |
| [**CDM- \_ hidecontrol**](cdm-hidecontrol.md)         | Blendet das angegebene Steuerelement aus.                                                                                                                                                                                             |
| [**CDM \_ setcontroltext**](cdm-setcontroltext.md)   | Legt den Text im angegebenen Steuerelement fest.                                                                                                                                                                                  |
| [**CDM- \_ setdefext**](cdm-setdefext.md)             | Legt die standardmäßige Dateinamenerweiterung für das Dialogfeld fest.                                                                                                                                                                 |



 

## <a name="explorer-style-custom-templates"></a>Explorer-Style benutzerdefinierter Vorlagen

Verwenden Sie die [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur, um zusätzliche Steuerelemente für ein Dialogfeld " **Öffnen** " oder " **Speichern** unter" im Explorer-Format anzugeben, um eine Vorlage für ein untergeordnetes Dialogfeld anzugeben, das die zusätzlichen Steuerelemente enthält Wenn die untergeordnete Dialogfeld Vorlage eine Ressource in einer Anwendung oder einer Dynamic Link Library ist, legen Sie das **ofn \_ ENABLETEMPLATE** -Flag im **Flags** -Member fest, und verwenden Sie die **HINSTANCE** -und **lptemplatename** -Member der-Struktur, um das Modul und den Ressourcennamen zu identifizieren. Wenn sich die Vorlage bereits im Arbeitsspeicher befindet, legen Sie das Flag **ofn \_ enabletemplatehandle** fest, und verwenden Sie das **HINSTANCE** -Element, um das Speicher Objekt zu identifizieren, das die Vorlage enthält. Wenn Sie eine untergeordnete Dialogfeld Vorlage für ein Dialogfeld im Explorer-Format bereitstellen, müssen Sie auch das **ofn- \_ Explorer** -Flag festlegen. Andernfalls geht das System davon aus, dass Sie eine Ersatz Vorlage für ein Dialogfeld für eine alte Art bereitstellen. Wenn Sie zusätzliche Steuerelemente bereitstellen, müssen Sie in der Regel auch eine [Hook-Prozedur im Explorer-Stil](#explorer-style-hook-procedures) zur Verarbeitung von Nachrichten für die neuen Steuerelemente bereitstellen.

Sie können die untergeordnete Dialogfeld Vorlage genauso wie jede andere Vorlage erstellen, mit dem Unterschied, dass Sie die Stile " **WS \_ Child** " und " **WS \_ clipneben** " angeben müssen und die Steuerelemente der **DS \_ 3dlook** -und **DS- \_ Steuer** Elemente angeben müssen. Das System erfordert den untergeordneten WS-Stil, da die Vorlage ein untergeordnetes Dialogfeld des Standard Dialogfelds " **Öffnen** " oder " **Speichern** unter" definiert. **\_** Der **WS \_ Clip-** Stil stellt sicher, dass das untergeordnete Dialogfeld keines der Steuerelemente im Standard Dialogfeld zeichnet. Der **DS \_ 3dlook-** Stil stellt sicher, dass die Darstellung der Steuerelemente im untergeordneten Dialogfeld mit den Steuerelementen im Standard Dialogfeld übereinstimmt. Der **DS- \_ Steuer** Element Stil stellt sicher, dass der Benutzer die Registerkarte und andere Navigationstasten verwenden kann, um zwischen allen Steuerelementen (Standard oder Benutzer definiert) im angepassten Dialogfeld zu wechseln.

Um Platz für die neuen Steuerelemente zu schaffen, erweitert das System das Standard Dialogfeld um die Breite und Höhe des benutzerdefinierten Dialog Felds. Standardmäßig werden alle Steuerelemente im Dialogfeld Benutzer definiert unter den Steuerelementen im Standard Dialogfeld positioniert. Sie können diese Standard Positionierung jedoch außer Kraft setzen, indem Sie ein statisches Text Steuerelement in die benutzerdefinierte Dialogfeld Vorlage einschließen und diesem den Steuerelement-ID-Wert **stc32** zuweisen. (Dieser Wert wird in der Dlgs. h-Header Datei definiert.) In diesem Fall verwendet das System das-Steuerelement als Bezugspunkt, um zu bestimmen, wo die neuen Steuerelemente positioniert werden sollen. Alle neuen Steuerelemente oberhalb und Links vom **stc32** -Steuerelement werden mit der gleichen Menge oberhalb und Links von den Steuerelementen im Standard Dialogfeld positioniert. Die neuen Steuerelemente unterhalb und rechts vom **stc32** -Steuerelement werden unterhalb und rechts von den Standard Steuerelementen positioniert. Im Allgemeinen wird jedes neue Steuerelement so positioniert, dass es dieselbe Position relativ zu den Standard Steuerelementen hat wie das **stc32** -Steuerelement. Um Platz für diese neuen Steuerelemente zu schaffen, fügt das System nach Bedarf den Bereich links, rechts, unten und oben im Standard Dialogfeld ein.

Das System erfordert, dass die Hook-Prozedur alle für das benutzerdefinierte Dialogfeld vorgesehenen Meldungen verarbeitet und somit die gleichen Fenster Meldungen an die Hook-Prozedur wie jede andere Dialogfeld Prozedur sendet. Die Hook-Prozedur empfängt z. b. [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldungen, wenn der Benutzer im Dialogfeld Benutzer definiert auf Schaltflächen-Steuerelemente klickt. Die Hook-Prozedur ist für das Initialisieren dieser Steuerelemente und das Abrufen von Werten aus den Steuerelementen zuständig, wenn das Dialogfeld geschlossen wird. Beachten Sie, dass das System die Steuerelemente noch nicht an ihre endgültigen Positionen verschoben hat, wenn die Hook-Prozedur die " [**WM \_ InitDialog**](wm-initdialog.md) "-Meldung empfängt.

Die Standard Dialogfeld Prozedur verarbeitet Nachrichten für alle Steuerelemente im Standard Dialogfeld, aber die Hook-Prozedur empfängt die Benachrichtigungs Meldungen für Benutzeraktionen für diese Steuerelemente, wie im [Explorer-Style-Hook-Prozeduren](#explorer-style-hook-procedures)beschrieben.

## <a name="explorer-style-control-identifiers"></a>Explorer-Style Steuerelement Bezeichner

Das Windows Software Development Kit (SDK) stellt die Standard Dialogfeld Vorlage für die alten Dialogfelder bereit, enthält jedoch nicht die Standardvorlage für die Dialogfelder im Explorer-Stil. Der Grund hierfür ist, dass Sie mit den Dialogfeldern im Explorer-Stil eigene Steuerelemente hinzufügen können, aber das Ändern der Vorlage für die Standard Steuerelemente nicht unterstützen. In einigen Fällen müssen Sie jedoch möglicherweise die Steuerelement Bezeichner kennen, die in den Standardvorlagen verwendet werden. Beispielsweise ist für die Nachrichten [**CDM \_ hidecontrol**](cdm-hidecontrol.md) und [**CDM \_ setcontroltext**](cdm-setcontroltext.md) ein Steuerelement Bezeichner erforderlich.

In der folgenden Tabelle werden die Bezeichner der Standard Steuerelemente in den Dialogfeldern **Öffnen** und **Speichern** unter im Explorer angezeigt. Die Bezeichner sind Konstanten, die in "Dlgs. h" und "Winuser. h" definiert sind.



| Steuerelement Bezeichner | Beschreibung des Steuer Elements                                                                                                                                                                                                                                                                        |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **chx1**           | Das Kontrollkästchen "schreibgeschützt"                                                                                                                                                                                                                                                                    |
| **cmb1**           | Dropdown-Kombinations Feld, in dem die Liste der Dateityp Filter angezeigt wird                                                                                                                                                                                                                            |
| **stc2**           | Bezeichnung für das Kombinations Feld " **cmb1** "                                                                                                                                                                                                                                                           |
| **cmb2**           | Dropdown-Kombinations Feld, das das aktuelle Laufwerk oder den aktuellen Ordner anzeigt und dem Benutzer das Auswählen eines zu öffnenden Laufwerks oder Ordners ermöglicht                                                                                                                                                                |
| **stc4**           | Bezeichnung für das Kombinations Feld " **cmb2** "                                                                                                                                                                                                                                                           |
| **cmb13**          | Das Dropdown-Kombinations Feld, in dem der Name der aktuellen Datei angezeigt wird, ermöglicht dem Benutzer, den Namen einer zu öffnenden Datei einzugeben und eine Datei auszuwählen, die vor kurzem geöffnet oder gespeichert wurde. Dies gilt für frühere Explorer-kompatible Anwendungen ohne Hook oder Dialogfeld Vorlage. Mit **edt1** vergleichen. |
| **edt1**           | Bearbeitungs Steuerelement, das den Namen der aktuellen Datei anzeigt oder es dem Benutzer ermöglicht, den Namen der zu öffnenden Datei einzugeben. Mit **cmb13** vergleichen.                                                                                                                                                  |
| **stc3**           | Bezeichnung für das **cmb13** -Kombinations Feld und das edt1-Bearbeitungs Steuerelement                                                                                                                                                                                                                                |
| **lst1**           | Listenfeld, das den Inhalt des aktuellen Laufwerks oder Ordners anzeigt                                                                                                                                                                                                                         |
| **stc1**           | Bezeichnung für das **lst1** -Listenfeld                                                                                                                                                                                                                                                            |
| **IDOK**           | Schaltfläche " **OK** " (Schaltfläche "Push")                                                                                                                                                                                                                                                    |
| **IDCANCEL**       | Schaltfläche " **Abbrechen** " (Schaltfläche "Push")                                                                                                                                                                                                                                                |
| **pshHelp**        | Schaltfläche " **Hilfe** " (Schaltfläche "Push")                                                                                                                                                                                                                                                  |



 

## <a name="customizing-old-style-dialog-boxes"></a>Anpassen von Old-Style-Dialog Feldern

Sie können das Dialogfeld " **Öffnen** " oder "Speichern unter" **im** alten Stil anpassen, indem Sie eine Hook-Prozedur vom Typ " [*ofnhookprocoldstyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) " bereitstellen, die Nachrichten oder Benachrichtigungen empfängt, die für die Standardprozedur Sie können auch eine benutzerdefinierte Vorlage bereitstellen, die anstelle der Standardvorlage verwendet werden soll. Die mit den Dialogfeldern im alten Stil verwendeten Hook-Prozeduren und-Vorlagen ähneln den in den anderen allgemeinen Dialogfeldern verwendeten Hook-Prozeduren und Vorlagen. Weitere Informationen finden Sie unter [Hook-Prozeduren für allgemeine Dialog Felder](customizing-common-dialog-boxes.md) und [benutzerdefinierte Vorlagen](customizing-common-dialog-boxes.md).

Verwenden Sie die [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur, wenn Sie das Dialogfeld erstellen, um eine Hook-Prozedur für ein Dialogfeld " **Öffnen** " oder " **Speichern** unter" im alten Stil zu aktivieren. Legen Sie das **ofn \_ ENABLEHOOK** -Flag im **Flags** -Member fest, und geben Sie die Adresse einer Hook-Prozedur [*ofnhuokprocoldstyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) im **lpfnhook** -Member an. Die Dialogfeld Prozedur sendet eine [**WM \_ InitDialog**](wm-initdialog.md) -Nachricht an die Hook-Prozedur, bei der der Parameter *param* auf die Adresse der **OpenFileName** -Struktur festgelegt ist, die zum Initialisieren des Dialog Felds verwendet wird.

Sie können die [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur verwenden, um eine benutzerdefinierte Vorlage für das Dialogfeld **Öffnen** oder **Speichern** unter anzugeben, die anstelle der Standardvorlage verwendet werden soll. Wenn Ihre benutzerdefinierte Vorlage eine Ressource in einer Anwendung oder einer Dynamic Link Library ist, legen Sie das **ofn \_ ENABLETEMPLATE** -Flag im **Flags** -Element fest, und verwenden Sie die **HINSTANCE** -und **lptemplatename** -Member der-Struktur, um das Modul und den Ressourcennamen zu identifizieren. Wenn die benutzerdefinierte Vorlage bereits im Arbeitsspeicher vorhanden ist, legen Sie das Flag **ofn \_ enabletemplatehandle** fest, und verwenden Sie das **HINSTANCE** -Element, um das Speicher Objekt zu identifizieren, das die Vorlage enthält. Erstellen Sie die benutzerdefinierte Vorlage, indem Sie die in der Datei "FileOpen. Dlg" angegebene Standardvorlage ändern. Die Steuerelement-IDs, die in den standardmäßigen Dialog Vorlagen zum Suchen und Ersetzen verwendet werden, werden in der Datei "Dlgs. h" definiert.

Standardmäßig werden in den Funktionen " [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) " und " [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) " die Dialogfelder "Explorer-Style" angezeigt. Wenn Sie ein Dialogfeld im alten Stil anzeigen möchten, müssen Sie eine [**ofnhuokprocoldstyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) -Hook-Prozedur bereitstellen und sicherstellen, dass das **ofn \_ Explorer** -Flag nicht im **Flags** -Member der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur festgelegt ist.

Wenn Sie das Flag **ofn \_ Explorer** festlegen, behandelt das System eine Hook-Prozedur oder eine benutzerdefinierte Vorlage als eine Anpassung im Explorer. Weitere Informationen zum Anpassen eines Explorer-Dialog Felds finden Sie unter [benutzerdefinierte Vorlagen im Explorer-Stil](#explorer-style-custom-templates).

## <a name="see-also"></a>Siehe auch

* [Beispiel für "Datei wird verwendet"](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse)
