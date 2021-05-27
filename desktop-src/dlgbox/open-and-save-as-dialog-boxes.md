---
title: Dialogfelder "Öffnen und Speichern unter"
description: Im Dialogfeld Öffnen können Benutzer das Laufwerk, das Verzeichnis und den Namen einer Datei oder eines Dateisatzes angeben, die geöffnet werden sollen.
ms.assetid: 5676ca9d-daca-40bf-8881-def2ff841c58
keywords:
- Allgemeine Dialogfeldbibliothek
- Allgemeine Dialogfelder
- Dialogfeld Öffnen
- Speichern unter (Dialogfeld)
- Anpassen des Dialogfelds "Öffnen"
- Anpassen des Dialogfelds "Speichern unter"
- Dialogfelder, Öffnen
- Dialogfelder,Speichern unter
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: be957276f0d5a6370bb53aca4b1af5052b422011
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548885"
---
# <a name="open-and-save-as-dialog-boxes"></a>Dialogfelder "Öffnen und Speichern unter"

> [!NOTE]
> Die [**GetOpenFileName-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) wird im [Beispiel File is in use](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse)veranschaulicht.

\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** allgemein durch das [Dialogfeld "Allgemeines Element"](../shell/common-file-dialog.md)ersetzt. Es wird empfohlen, die Dialogfeld-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]

Im Dialogfeld **Öffnen** können Benutzer das Laufwerk, das Verzeichnis und den Namen einer Datei oder eines Dateisatzes angeben, die geöffnet werden sollen. Sie erstellen und zeigen ein Dialogfeld **Öffnen** an, indem Sie eine [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) initialisieren und die Struktur an die [**GetOpenFileName-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) übergeben.

Im Dialogfeld **Speichern unter** kann der Benutzer das Laufwerk, das Verzeichnis und den Namen einer datei angeben, die gespeichert werden soll. Sie erstellen und zeigen ein Dialogfeld **Speichern unter** an, indem Sie eine [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) initialisieren und die Struktur an die [**GetSaveFileName-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) übergeben.

Die Dialogfelder **Öffnen** und **Speichern unter** im Explorer-Stil bieten Benutzeroberflächenfeatures, die dem Windows-Explorer ähneln. Das System unterstützt jedoch weiterhin die Dialogfelder **Öffnen** und **Speichern unter** im alten Stil für Anwendungen, die mit der alten Benutzeroberfläche konsistent sein müssen.

Neben dem Unterschied in der Darstellung unterscheiden sich die Dialogfelder im Explorer-Stil und im alten Stil durch die Verwendung von benutzerdefinierten Vorlagen und Hookprozes zum Anpassen der Dialogfelder. Die Dialogfelder im Explorer- und alten Stil weisen jedoch das gleiche Verhalten für die meisten grundlegenden Vorgänge auf, z. B. das Angeben eines Dateinamenfilters, das Überprüfen der Benutzereingabe und das Abrufen des vom Benutzer angegebenen Dateinamens. Weitere Informationen zu den Dialogfeldern im Explorer- und alten Stil finden Sie unter Öffnen und Speichern [unter Anpassung des Dialogfelds](#open-and-save-as-dialog-box-customization).

Die folgende Abbildung zeigt ein typisches Dialogfeld **"Öffnen" im** Explorer-Stil.

![Dialogfeld "Datei öffnen"](images/opendialogboxxp.png)

Die folgende Abbildung zeigt ein typisches Dialogfeld "Speichern **unter"** im Explorer-Stil.

![Dialogfeld "Datei speichern"](images/saveasdialogboxxp.png)

Wenn der Benutzer einen Dateinamen angibt und auf die **Schaltfläche OK** klickt, gibt [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) oder [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) **TRUE zurück.** Der Puffer, auf den der **lpstrFile-Member** der [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) zeigt, enthält den vollständigen Pfad und Dateinamen, die vom Benutzer angegeben werden.

Wenn der Benutzer das Dialogfeld **Öffnen** oder **Speichern unter** abbricht oder ein Fehler auftritt, gibt die Funktion **FALSE zurück.** Um die Ursache des Fehlers zu ermitteln, rufen Sie die [**CommDlgExtendedError-Funktion auf,**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) um den erweiterten Fehlerwert abzurufen. Wenn der **lpstrFile-Puffer** zu klein ist, um den vollständigen Namen zu erhalten, gibt **CommDlgExtendedError** **FNERR \_ BUFFERTOOSMALL** zurück, und die ersten 2 Bytes des Puffers, auf die das **lpstrFile-Element** zeigt, werden auf einen ganzzahligen Wert festgelegt, der die größe angibt, die zum Empfangen des vollständigen Namens erforderlich ist.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Dateinamen und Verzeichnisse](#file-names-and-directories)
-   [Filter](#filters)
-   [Datei- und Verzeichnisüberprüfung](#file-and-directory-validation)
-   [Anpassen des Dialogfelds "Öffnen und Speichern unter"](#open-and-save-as-dialog-box-customization)
-   [Hook-Prozeduren im Explorer-Stil](#explorer-style-hook-procedures)
-   [Benutzerdefinierte Vorlagen im Explorer-Stil](#explorer-style-custom-templates)
-   [Steuerelementbezeichner im Explorer-Stil](#explorer-style-control-identifiers)
-   [Anpassen Old-Style Dialogfeldern](#customizing-old-style-dialog-boxes)

## <a name="file-names-and-directories"></a>Dateinamen und Verzeichnisse

Die Informationen in diesem Abschnitt gelten sowohl für  Dialogfelder im Explorer-Stil als auch für Dialogfelder im alten **Und-Format** öffnen und speichern unter.

Vor dem Aufrufen der Funktionen [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) oder [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) muss der **lpstrFile-Member** der [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) auf den Puffer verweisen, um den Dateinamen zu erhalten. Der **nMaxFile-Member** muss die Größe des **lpstrFile-Puffers** in Zeichen angeben. Für eine ANSI-Funktion ist dies die Anzahl von Bytes, für eine Unicode-Funktion jedoch die Anzahl der Zeichen.

Wenn der Benutzer einen Dateinamen angibt und auf die Schaltfläche **OK** klickt, kopiert das Dialogfeld das ausgewählte Laufwerk, das verzeichnis und den Dateinamen in den **lpstrFile-Puffer.** Die -Funktion legt auch die Member **nFileOffset** und **nFileExtension** auf die Offsets in Zeichen vom Anfang des Puffers bis zum Dateinamen bzw. zur Dateinamenerweiterung fest.

Um nur den Dateinamen und die Erweiterung abzurufen, legen Sie den **lpstrFileTitle-Member** so fest, dass er auf einen Puffer verweist, und legen Sie den **nMaxFileTitle-Member** auf die Größe des Puffers in Zeichen fest. Alternativ können Sie den **lpstrFile-Puffer** in einem Aufruf der [**GetFileTitle-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-getfiletitlea) übergeben, um den Anzeigenamen der ausgewählten Datei abzurufen. Beachten Sie jedoch, dass der dateiname, den **GetFileTitle** zurückgibt, nur dann eine Erweiterung enthält, wenn dies die Einstellung des Benutzers zum Anzeigen von Dateinamen ist.

Das Dialogfeld verwendet das aktuelle Verzeichnis für den aufrufenden Prozess als erstes Verzeichnis, aus dem Dateien und Verzeichnisse angezeigt werden. Verwenden Sie die Funktionen [**GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) und [**SetCurrentDirectory,**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) um das aktuelle Verzeichnis eines Prozesses abzurufen und zu ändern. Um ein anderes Anfangsverzeichnis anzugeben, ohne das aktuelle Verzeichnis zu ändern, verwenden Sie den **LpstrInitialDir-Member,** um den Namen eines Verzeichnisses anzugeben. Das Dialogfeld ändert automatisch Ihr aktuelles Verzeichnis, wenn der Benutzer ein anderes Laufwerk oder Verzeichnis auswählt. Um zu verhindern, dass das Dialogfeld Ihr aktuelles Verzeichnis ändert, legen Sie das **FLAG OFN \_ NOCHANGEDIR** fest. Dieses Flag verhindert nicht, dass der Benutzer Verzeichnisse ändert, um eine Datei zu finden.

Um eine Standarddateinamenerweiterung anzugeben, verwenden Sie **den lpstrDefExt-Member.** Wenn der Benutzer einen Dateinamen angibt, der keine Erweiterung hat, fügt das Dialogfeld die Standarderweiterung hinzu. Wenn Sie eine Standarderweiterung angeben und der Benutzer einen Dateinamen mit einer anderen Erweiterung angibt, legt das Dialogfeld das **OFN \_ EXTENSIONDIFFERENT-Flag** fest.

Damit der Benutzer mehr als eine Datei aus einem Verzeichnis auswählen kann, legen Sie das **OFN \_ ALLOWMULTISELECT-Flag** fest. Zur Kompatibilität mit älteren Anwendungen verwendet das Standarddialogfeld für mehrfache Auswahl die Benutzeroberfläche im alten Stil. Um ein Dialogfeld mit mehrfacher Auswahl im Explorer-Stil anzuzeigen, müssen Sie auch das **\_ OFN-EXPLORER-Flag** festlegen.

Wenn der Benutzer mehrere Dateien auswählt, gibt der Puffer, auf den der **lpstrFile-Member** zeigt, den Pfad zum aktuellen Verzeichnis zurück, gefolgt von den Dateinamen der ausgewählten Dateien. Das **nFileOffset-Member** ist der Offset zum ersten Dateinamen, und das **nFileExtension-Member** wird nicht verwendet. In der folgenden Tabelle wird der Unterschied zwischen Dialogfeldern im Explorer- und alten Stil bei der Rückgabe mehrerer Dateinamen beschrieben.



| Dialogfeldformat            | Beschreibung                                                                                                                                                                                                               |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dialogfelder im Explorer-Stil | Die Verzeichnis- und Dateinamenzeichenfolgen sind **durch NULL** getrennt, und es wird ein zusätzliches **NULL-Zeichen** nach dem Namen der letzten Datei verwendet. Mit diesem Format können dialogfelder im Explorer-Stil lange Dateinamen zurückgeben, die Leerzeichen enthalten. |
| Dialogfelder im alten Stil      | Die Verzeichnis- und Dateinamenzeichenfolgen werden durch Leerzeichen getrennt. Für Dateinamen mit Leerzeichen verwendet die Funktion kurze Dateinamen.                                                                                              |



 

Sie können die [**FindFirstFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) verwenden, um zwischen langen und kurzen Dateinamen zu konvertieren.

Wenn Sie **OFN \_ ALLOWMULTISELECT** angeben und der Benutzer nur eine Datei auswählt, verfügt die **lpstrFile-Zeichenfolge** nicht über ein Trennzeichen zwischen Pfad und Dateiname.

## <a name="filters"></a>Filter

Die Informationen in diesem Abschnitt gelten sowohl für die Dialogfelder Im Explorer-Stil als auch im alten Stil **Öffnen** und **Speichern unter.**

Sie können Dateinamenfilter bereitstellen, um den Benutzer beim Einschränken der Dateinamen zu unterstützen, die im Dialogfeld angezeigt werden. Ein Dateinamenfilter besteht aus einem Paar von NULL-terminierten Zeichenfolgen, einer Beschreibung und einem Muster, die mit der anderen verkettet sind. Im Dialogfeld wird die Beschreibung angezeigt, mit der der Benutzer auswählen kann, welcher Filter verwendet werden soll. und verwendet das Muster, um die anzuzeigende Datei auszuwählen.

Um die Filter anzugeben, legen Sie den **lpstrFilter-Member** der [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) so fest, dass er auf einen Puffer zeigt, der ein Array von Filterzeichenfolgenpaaren enthält. Auf die letzte Zeichenfolge im Array muss ein zusätzliches NULL-Zeichen folgen.

Eine Musterzeichenfolge kann eine Kombination aus gültigen Dateinamenzeichen und dem Sternchen ( \* ) sein. Das Sternchen ist ein Platzhalter, der eine beliebige Kombination gültiger Dateinamenzeichen darstellt. Im Dialogfeld werden nur die Dateien angezeigt, die dem Muster entsprechen. Um mehrere Muster für dieselbe Beschreibung anzugeben, müssen Sie ein Semikolon (;) , um die Muster zu trennen. Beachten Sie, dass Leerzeichen in der Musterzeichenfolge zu unerwarteten Ergebnissen führen können.

Das folgende Codefragment gibt zwei Filter an. Der Filter mit der Beschreibung "Quelle" weist zwei Muster auf. Wenn der Benutzer diesen Filter auswählt, zeigt das Dialogfeld nur Dateien mit dem an. C und . CXX-Erweiterungen. Beachten Sie, dass in der Programmiersprache C eine Zeichenfolge, die in doppelte Anführungszeichen eingeschlossen ist, NULL-terminiert ist.


```
OPENFILENAME ofn;       // common dialog box structure

ofn.lpstrFilter = "Source\0*.C;*.CXX\0All\0*.*\0"
ofn.nFilterIndex = 1;
```



Der **nFilterIndex-Member** der [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) gibt einen Index an, der angibt, welcher Filter das Dialogfeld anfänglich verwendet. Der erste Filter im Puffer weist den Index 1, den zweiten 2 usw. auf. Wenn der Benutzer den Filter während der Verwendung des Dialogfelds ändert, wird das **Element nFilterIndex** bei der Rückgabe auf den Index des ausgewählten Filters festgelegt.

Sie können einen benutzerdefinierten Filter erstellen, indem Sie das **lpstrCustomFilter-Member** auf die Adresse eines Puffers festlegen, der einen einzelnen Filter enthält, und indem Sie das **nMaxCustFilter-Member** auf die Größe des Puffers in Zeichen oder Bytes festlegen. Das Dialogfeld platziert den benutzerdefinierten Filter immer am Anfang der Filterliste und aktualisiert bei der Rückgabe immer den Musterteil des Filters mit dem Muster aus dem vom Benutzer ausgewählten Filter.

Bei Dialogfeldern im Explorer-Stil kann sich die Standarderweiterung ändern, wenn der Benutzer einen anderen Filter auswählt. Wenn der Benutzer einen Filter auswählt, dessen erstes Muster das Formular \* hat.*xxx* (d. h. die Erweiterung enthält kein Platzhalterzeichen), verwendet das Dialogfeld *xxx* als Standarderweiterung. Dies tritt nur auf, wenn Sie eine Standarderweiterung im **lpstrDefExt-Member** der [**OPENFILENAME-Struktur angegeben**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) haben. Wenn der Benutzer z. B. "Quelle \\ 0 " auswählt. \* C; \* . CXX \\ 0"-Filter, die Standarderweiterung wird in "C" geändert. Wenn Sie den Filter jedoch als "Quelle \\ 0 " definiert \* haben. C \* \\ 0", würde sich die Standarderweiterung nicht ändern, da die Erweiterung einen Platzhalter enthält.

Die [**CDN \_ INCLUDEITEM-Benachrichtigungsmeldung**](cdn-includeitem.md) bietet eine weitere Möglichkeit, die im Dialogfeld angezeigten Namen zu filtern. Um diese Meldung zu verwenden, geben Sie eine [**OFNHookProc-Hookprozedur**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) an, und geben Sie das **OFN \_ ENABLEINCLUDENOTIFY-Flag** in der [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) an, wenn Sie das Dialogfeld erstellen. Jedes Mal, wenn der Benutzer einen Ordner öffnet, sendet das Dialogfeld für jedes Element im neu geöffneten Ordner eine **CDN \_ INCLUDEITEM-Benachrichtigung** an Die Hookprozedur. Der Rückgabewert der Hookprozedur gibt an, ob das Dialogfeld das Element in der Elementliste des Ordners anzeigen soll.

## <a name="file-and-directory-validation"></a>Datei- und Verzeichnisüberprüfung

Sofern nicht anders angegeben, gelten die Informationen in diesem Abschnitt sowohl für Dialogfelder im Explorer- als auch im alten Stil im **Format** Öffnen **und** Speichern unter.

Im Dialogfeld werden vom Benutzer eingegebene Dateinamen automatisch überprüft, um sicherzustellen, dass die Namen nur gültige Zeichen enthalten. Um die Überprüfung von Dateinamenzeichen zu überschreiben, legen Sie das **FLAG OFN \_ NOVALIDATE** fest.

Um zu erzwingen, dass das Dialogfeld überprüft, ob der Benutzer den Namen einer vorhandenen Datei angegeben hat, legen Sie das **FLAG OFN \_ FILEMUSTEXIST** fest. Um die Überprüfung zu erzwingen, ob der angegebene Pfad vorhanden ist, legen Sie das **FLAG OFN \_ PATHMUSTEXIST** fest. Wenn Sie das **FLAG OFN \_ CREATEPROMPT** festlegen, fordert das Dialogfeld den Benutzer zur Berechtigung zum Erstellen einer nicht vorhandenen Datei auf. Wenn dieses Flag festgelegt ist und der Benutzer eine neue Datei erstellt, wird das Dialogfeld geschlossen, und die Funktion gibt den angegebenen Namen zurück. Andernfalls bleibt das Dialogfeld geöffnet.

Wenn Sie das Dialogfeld **Speichern unter** verwenden, können Sie das Dialogfeld anweisen, den Benutzer zur Eingabe der Berechtigung zum Überschreiben einer vorhandenen Datei aufzufordern, indem Sie das **FLAG OFN \_ OVERWRITEPROMPT** festlegen.

Standardmäßig erstellt das Dialogfeld eine Testdatei der Länge 0 (null), um zu bestimmen, ob eine neue Datei im ausgewählten Verzeichnis erstellt werden kann. Um die Erstellung dieser Testdatei zu verhindern, legen Sie das **FLAG OFN \_ NOTESTFILECREATE** fest.

Wenn Sie eine Hookprozedur aktivieren, benachrichtigt das Dialogfeld Ihre Hookprozedur, wenn eine Netzwerkfreigabeverletzung für den vom Benutzer angegebenen Dateinamen auftritt. Wenn Sie das **\_ OFN-EXPLORER-Flag** festlegen, sendet das Dialogfeld die [**CDN \_ SHAREVIOLATION-Nachricht**](cdn-shareviolation.md) an die Hookprozedur. Wenn Sie **OFN \_ EXPLORER** nicht festlegen, sendet das Dialogfeld die registrierte [**SHAREVISTRING-Nachricht**](sharevistring.md) an die Hookprozedur. Um zu verhindern, dass das Dialogfeld Benachrichtigungen zu Freigabeverletzungen sendet, legen Sie das **OFN \_ SHAREAWARE-Flag** fest.

Wenn der Benutzer das Kontrollkästchen Schreibgeschützt aktiviert, legt das Dialogfeld das **FLAG OFN \_ READONLY** bei der Rückgabe fest. Um das Kontrollkästchen Als schreibgeschützt **öffnen** auszublenden, legen Sie das **FLAG OFN \_ HIDEREADONLY** fest. Um zu verhindern, dass das Dialogfeld Namen vorhandener Dateien mit dem schreibgeschützten Attribut zurücksendet, legen Sie das **OFN \_ NOREADONLYRETURN-Flag** fest.

Um zu verhindern, dass das Dialogfeld Linkdateien dereferenziert, legen Sie **den OFN \_ NODEREFERENCELINKS-Wert** fest. In diesem Fall gibt das Dialogfeld anstelle des Namens der Datei, auf die die Linkdatei verweist, den Namen der Linkdatei zurück.

## <a name="open-and-save-as-dialog-box-customization"></a>Anpassen des Dialogfelds "Öffnen und Speichern unter"

Sie können ein Dialogfeld **Öffnen oder** **Speichern unter** anpassen, indem Sie eine Hookprozedur, eine benutzerdefinierte Vorlage oder beides bereitstellen. Die Versionen der Dialogfelder im Explorer-Stil und im alten Stil unterscheiden sich jedoch in der Verwendung benutzerdefinierter Vorlagen und Hook-Prozeduren.

Informationen zum Anpassen eines Dialogfelds im Explorer-Stil finden Sie unter Hook-Prozeduren im [Explorer-Stil,](#explorer-style-hook-procedures)benutzerdefinierte Vorlagen im [Explorer-Stil](#explorer-style-custom-templates)und [Steuerelementbezeichner im Explorer-Stil.](#explorer-style-control-identifiers) Informationen zum Anpassen eines Dialogfelds im alten Stil finden Sie unter Anpassen Old-Style [Dialogfeldern](#customizing-old-style-dialog-boxes).

In der folgenden Tabelle sind die Unterschiede zwischen den beiden Stilen zusammengefasst.



| Anpassung                  | Beschreibung                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hookprozedur im Explorer-Stil  | Die Hookprozedur empfängt Benachrichtigungsmeldungen, die vom allgemeinen Dialogfeld gesendet werden, sowie Meldungen für alle zusätzlichen Steuerelemente, die Sie durch Angeben einer untergeordneten Dialogvorlage definiert haben. Die Hookprozedur erhält keine Nachrichten für die Standardsteuerelemente des Standarddialogfelds. |
| Benutzerdefinierte Vorlage im Explorer-Stil | Das System verwendet die benutzerdefinierte Vorlage, um ein untergeordnetes Dialogfeld zu erstellen. Die Vorlage kann zusätzliche Steuerelemente definieren und den Speicherort des Clusters von Standardsteuerelementen angeben. Die benutzerdefinierte Vorlage ersetzt nicht die Standardvorlage.                                          |
| Hookprozedur im alten Stil       | Die Hookprozedur empfängt alle nachrichten, die an das Dialogfeld gesendet werden, einschließlich Nachrichten für die Standardsteuerelemente und alle benutzerdefinierten Steuerelemente. Die Hookprozedur empfängt auch registrierte Nachrichten, die vom allgemeinen Dialogfeld gesendet werden.                                                         |
| Benutzerdefinierte Vorlage im alten Stil      | Die benutzerdefinierte Vorlage ersetzt die Standardvorlage. Erstellen Sie die benutzerdefinierte Vorlage, indem Sie die in der Datei Fileopen.dlg angegebene Standardvorlage ändern.                                                                                                                                  |



 

Der Standardtitel für Dialogfelder im Explorer- und alten Stil ist entweder **"Öffnen"** oder **"Speichern unter".** Um den Titel zu ändern, geben Sie den neuen Titel im **lpstrTitle-Member** der [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) an.

Die Registrierungsstruktur **HKEY \_ CURRENT \_ USER** eines Benutzers kann Werte enthalten,  die den Inhalt der Dialogfelder Öffnen und Speichern unter im **Explorer-Stil** anpassen. Diese Registrierungseinträge wirken sich nur auf die Dialogfelder aus, die für den Benutzer angezeigt werden, der der Registrierungsstruktur zugeordnet ist.

Ein Administrator kann die  Werte  in der folgenden Tabelle unter diesem Unterschlüssel festlegen, um Funktionen von Dialogfeldern im Explorer-Stil zu öffnen und speichern unter auszublenden:

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
| **NoPlacesBar**  | 1     | Blendet die Stellenleiste aus.                    |
| **NoFileMRU**    | 1     | Blendet die Liste Zuletzt verwendet (MRU) aus. |
| **NoBackButton** | 1     | Blendet die **Schaltfläche Zurück** aus.               |



 

Der Inhalt der **Leiste Orte** wird durch den Inhalt des folgenden Unterschlüssels bestimmt:

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

Derzeit können unter diesem Schlüssel nur fünf Einträge enthalten sein, und der Wert-/Namensindex ist null-basiert. Die Namen für die Einträge sollten Place0, Place1, Place2, Place3 und Place4 sein. Die Werte der Einträge können **REG \_ DWORD-,** **REG \_ SZ-** oder **REG EXPAND \_ \_ SZ-Werte** sein, die Orte identifizieren, die in die Stellenleiste ein-/ausdehnen sollen.



| Werttyp                         | Bedeutung                                                                                                   |
|------------------------------------|-----------------------------------------------------------------------------------------------------------|
| **REG \_ DWORD**                     | Ein CSIDL-Wert, der einen Ordner identifiziert. Eine Liste der CSIDL-Werte finden Sie unter [**CSIDL-Werte.**](../shell/csidl.md) |
| **REG \_ SZ** oder **REG EXPAND \_ \_ SZ** | Eine auf NULL endende Zeichenfolge, die einen gültigen Pfad angibt.                                                     |



 

## <a name="explorer-style-hook-procedures"></a>Explorer-Style Hookprozessen

Sie können das Dialogfeld **Öffnen** oder **Speichern** unter im Explorer-Stil anpassen, indem Sie eine Hookprozedur, eine benutzerdefinierte Vorlage oder beides bereitstellen. Wenn Sie eine Hookprozedur für ein Dialogfeld im Explorer-Stil bereitstellen, erstellt das System ein Dialogfeld, das ein untergeordnetes Element des Standarddialogfelds ist. Die Hookprozedur fungiert als Dialogprozedur für das untergeordnete Dialogfeld. Dieses untergeordnete Dialogfeld basiert auf der benutzerdefinierten Vorlage oder auf einer Standardvorlage, wenn keine bereitgestellt wird. Weitere Informationen finden Sie unter Benutzerdefinierte Vorlagen im [Explorer-Stil.](#explorer-style-custom-templates)

Um eine Hookprozedur für ein **Dialogfeld** im Explorer-Stil **zu** aktivieren, verwenden Sie beim Erstellen des Dialogfelds die [**OPENFILENAME-Struktur.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) Legen Sie die **FLAGS OFN \_ ENABLEHOOK** und **OFN \_ EXPLORER** im **Flags-Member** fest, und geben Sie die Adresse einer [**OFNHookProc-Hookprozedur**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) im **lpfnHook-Member** an. Wenn Sie eine Hookprozedur angeben und das **\_ OFN-EXPLORER-Flag** weglassen, müssen Sie eine [**OFNHookProcOldStyle-Hookprozedur**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) verwenden, und Sie erhalten die Benutzeroberfläche im alten Stil. Weitere Informationen finden Sie unter [Anpassen von Old-Style Dialogfeldern.](#customizing-old-style-dialog-boxes)

Eine Hookprozedur im Explorer-Stil empfängt eine Vielzahl von Nachrichten, während das Dialogfeld geöffnet ist. Dabei handelt es sich z. B. um:

-   Die [**WM \_ INITDIALOG-Nachricht**](wm-initdialog.md) und andere Standarddialogfeldmeldungen, z. B. die [**WM \_ CTLCOLORDLG-Steuerelementfarbmeldung.**](wm-ctlcolordlg.md)
-   Eine Reihe von [**WM NOTIFY-Benachrichtigungsmeldungen, \_**](../controls/wm-notify.md) die auf Aktionen hinweisen, die vom Benutzer oder anderen Dialogfeldereignissen ausgeführt werden.
-   Meldungen für alle zusätzlichen Steuerelemente, die Sie durch Angeben einer Vorlage für untergeordnete Dialoge definiert haben.

Darüber hinaus gibt es eine Reihe von Nachrichten, die Sie an ein Dialogfeld im Explorer-Stil senden können, um Informationen abzurufen oder das Verhalten und die Darstellung des Dialogfelds zu steuern.

Wenn Sie eine Hookprozedur für ein Dialogfeld im Explorer-Stil bereitstellen, erstellt die Standarddialogfeldprozedur ein untergeordnetes Dialogfeld, wenn die Standarddialogprozedur die [**WM \_ INITDIALOG-Meldung**](wm-initdialog.md) verarbeitet. Die Hookprozedur fungiert als Dialogprozedur für das untergeordnete Dialogfeld. Zu diesem Zeitpunkt empfängt die Hookprozedur eine eigene **WM \_ INITDIALOG-Nachricht,** bei der der *lParam-Parameter* auf die Adresse der [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) festgelegt ist, die zum Initialisieren des Dialogfelds verwendet wird. Nachdem der untergeordnete Dialog die Verarbeitung seiner eigenen **WM \_ INITDIALOG-Nachricht** abgeschlossen hat, verschiebt die Standarddialogprozedur bei Bedarf die Standardsteuerelemente, um Platz für zusätzliche Steuerelemente des untergeordneten Dialogfelds zu machen. Die Standarddialogprozedur sendet dann die [**CDN \_ INITDONE-Benachrichtigungsnachricht**](cdn-initdone.md) an die Hookprozedur.

Die Hookprozedur [**empfängt WM \_ NOTIFY-Benachrichtigungen,**](../controls/wm-notify.md) die vom Benutzer im Dialogfeld durchgeführte Aktionen angeben. Sie können einige dieser Meldungen verwenden, um das Verhalten des Dialogfelds zu steuern. Beispielsweise empfängt die Hookprozedur die [**CDN \_ FILEOK-Meldung,**](cdn-fileok.md) wenn der Benutzer einen Dateinamen auswählt und auf die **Schaltfläche OK** klickt. Als Reaktion auf diese Meldung kann die Hookprozedur die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) verwenden, um den ausgewählten Namen abzulehnen und zu erzwingen, dass das Dialogfeld geöffnet bleibt.

Der *lParam-Parameter* für jede [**WM \_ NOTIFY-Nachricht**](../controls/wm-notify.md) ist ein Zeiger auf eine [**OFNOTIFY-**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) oder [**OFNOTIFYEX-Struktur,**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) die die Aktion definiert. Der **Code** member im Header dieser Struktur enthält eine der folgenden Benachrichtigungsmeldungen.



| Nachricht                                           | Bedeutung                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CDN \_ FILEOK**](cdn-fileok.md)                 | Der Benutzer hat auf die Schaltfläche **OK** geklickt. Das Dialogfeld wird geschlossen.                                                                                                                                                                                                                          |
| [**CDN \_ FOLDERCHANGE**](cdn-folderchange.md)     | Der Benutzer hat einen neuen Ordner oder ein neues Verzeichnis geöffnet.                                                                                                                                                                                                                                                     |
| [**\_CDN-HILFE**](cdn-help.md)                     | Der Benutzer hat auf die Schaltfläche **Hilfe** geklickt.                                                                                                                                                                                                                                                          |
| [**CDN \_ INCLUDEITEM**](cdn-includeitem.md)       | Bestimmt, ob ein Element angezeigt werden soll. Wenn der Benutzer einen neuen Ordner oder ein neues Verzeichnis öffnet, sendet das System diese Benachrichtigung für jedes Element im Ordner oder Verzeichnis. Das System sendet diese Benachrichtigung nur, wenn das **FLAG OFN \_ ENABLEINCLUDENOTIFY** festgelegt wurde.                          |
| [**CDN \_ INITDONE**](cdn-initdone.md)             | Das System hat die Initialisierung des Dialogfelds abgeschlossen, und das Dialogfeld hat die Verarbeitung der [**WM \_ INITDIALOG-Meldung**](wm-initdialog.md) abgeschlossen. Außerdem hat das System die Anordnung von Steuerelementen im allgemeinen Dialogfeld abgeschlossen, um Platz für die Steuerelemente des untergeordneten Dialogfelds zu schaffen (sofern vorhanden). |
| [**CDN \_ SELCHANGE**](cdn-selchange.md)           | Der Benutzer hat eine neue Datei oder einen neuen Ordner aus der Dateiliste ausgewählt.                                                                                                                                                                                                                                     |
| [**CDN \_ SHAREVIOLATION**](cdn-shareviolation.md) | Im allgemeinen Dialogfeld ist ein Freigabeverstoß für die Datei aufgetreten, die zurückgegeben werden soll.                                                                                                                                                                                                        |
| [**CDN \_ TYPECHANGE**](cdn-typechange.md)         | Der Benutzer hat einen neuen Dateityp aus der Liste der Dateitypen ausgewählt.                                                                                                                                                                                                                                 |



 

Diese [**WM \_ NOTIFY-Meldungen**](../controls/wm-notify.md) ersetzen die registrierten Meldungen [**FILEOKSTRING,**](fileokstring.md) [**LBSELCHSTRING,**](lbselchstring.md) [**SHAREVISTRING**](sharevistring.md)und [**HELPMSGSTRING,**](helpmsgstring.md) die von früheren Versionen der Dialogfelder **Öffnen** und **Speichern unter** verwendet wurden. Die Hookprozedur empfängt jedoch auch die abgelöste Nachricht nach der **WM \_ NOTIFY-Nachricht,** wenn die **WM \_ NOTIFY-Verarbeitung** [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) nicht verwendet, um einen **\_ DWL-MSGRESULT-Wert** ungleich 0 festzulegen.

Um Informationen zum Status des Dialogfelds abzurufen oder das Verhalten und die Darstellung des Dialogfelds zu steuern, kann die Hookprozedur die folgenden Meldungen an das Dialogfeld senden.



| Nachricht                                             | Bedeutung                                                                                                                                                                                                                  |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CDM \_ GETFILEPATH**](cdm-getfilepath.md)         | Ruft den Pfad und den Dateinamen der ausgewählten Datei ab.                                                                                                                                                                   |
| [**CDM \_ GETFOLDERIDLIST**](cdm-getfolderidlist.md) | Ruft die Elementbezeichnerliste ab, die dem aktuellen Ordner entspricht, den das Dialogfeld geöffnet hat. Weitere Informationen zu Elementbezeichnerlisten finden Sie unter [Einführung in den Shellnamespace](/windows/desktop/shell/namespace-intro). |
| [**CDM \_ GETFOLDERPATH**](cdm-getfolderpath.md)     | Ruft den Pfad des aktuellen Ordners oder Verzeichnisses für das Dialogfeld ab.                                                                                                                                                |
| [**CDM \_ GETSPEC**](cdm-getspec.md)                 | Ruft den Dateinamen (ohne den Pfad) der datei ab, die derzeit im Dialogfeld ausgewählt ist.                                                                                                                       |
| [**CDM \_ HIDECONTROL**](cdm-hidecontrol.md)         | Blendet das angegebene Steuerelement aus.                                                                                                                                                                                             |
| [**CDM \_ SETCONTROLTEXT**](cdm-setcontroltext.md)   | Legt den Text im angegebenen Steuerelement fest.                                                                                                                                                                                  |
| [**CDM \_ SETDEFEXT**](cdm-setdefext.md)             | Legt die Standarddateinamenerweiterung für das Dialogfeld fest.                                                                                                                                                                 |



 

## <a name="explorer-style-custom-templates"></a>Explorer-Style von benutzerdefinierten Vorlagen

Verwenden Sie zum Definieren zusätzlicher  Steuerelemente für das Dialogfeld Öffnen oder Speichern unter im Explorer-Stil die [**OPENFILENAME-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) um eine Vorlage für ein untergeordnetes Dialogfeld anzugeben, das die zusätzlichen Steuerelemente enthält.  Wenn Ihre untergeordnete Dialogvorlage eine Ressource in einer Anwendung oder Dynamic Link Library ist, legen Sie das **OFN \_ ENABLETEMPLATE-Flag** im **Flags-Element** fest, und verwenden Sie die **Elemente hInstance** und **lpTemplateName** der Struktur, um das Modul und den Ressourcennamen zu identifizieren. Wenn sich die Vorlage bereits im Arbeitsspeicher befindet, legen Sie das **OFN \_ ENABLETEMPLATEHANDLE-Flag** fest, und verwenden Sie den **hInstance-Member,** um das Speicherobjekt zu identifizieren, das die Vorlage enthält. Wenn Sie eine untergeordnete Dialogfeldvorlage für ein Dialogfeld im Explorer-Stil bereitstellen, müssen Sie auch das **\_ OFN-EXPLORER-Flag** festlegen. Andernfalls geht das System davon aus, dass Sie eine Ersatzvorlage für ein Dialogfeld im alten Stil bereitstellen. Wenn Sie zusätzliche Steuerelemente bereitstellen, müssen Sie in der Regel auch eine Hookprozedur im [Explorer-Stil](#explorer-style-hook-procedures) bereitstellen, um Nachrichten für die neuen Steuerelemente zu verarbeiten.

Sie können ihre untergeordnete Dialogfeldvorlage wie jede andere Vorlage erstellen, mit der Ausnahme, dass Sie die **Formate WS \_ CHILD** und **WS \_ CLIPSIBLINGS** angeben müssen und die **Stile DS \_ 3DLOOK** und **DS \_ CONTROL** angeben sollten. Das System erfordert den **WS \_ CHILD-Stil,** da Ihre Vorlage ein untergeordnetes Dialogfeld des Standarddialogfelds **Öffnen** oder **Speichern unter** definiert. Der **WS \_ CLIPSIBLINGS-Stil** stellt sicher, dass das untergeordnete Dialogfeld keine Steuerelemente im Standarddialogfeld zeichnet. Der **DS \_ 3DLOOK-Stil** stellt sicher, dass die Darstellung der Steuerelemente im untergeordneten Dialogfeld mit den Steuerelementen im Standarddialogfeld konsistent ist. Der **DS \_ CONTROL-Stil** stellt sicher, dass der Benutzer die TAB-TASTE und andere Navigationsschlüssel verwenden kann, um zwischen allen Steuerelementen (Standard oder benutzerdefiniert) im benutzerdefinierten Dialogfeld zu wechseln.

Um Platz für die neuen Steuerelemente zu schaffen, erweitert das System das Standarddialogfeld um die Breite und Höhe des benutzerdefinierten Dialogfelds. Standardmäßig werden alle Steuerelemente aus dem benutzerdefinierten Dialogfeld unterhalb der Steuerelemente im Standarddialogfeld positioniert. Sie können diese Standardpositionierung jedoch überschreiben, indem Sie ein statisches Textsteuerelement in Ihre benutzerdefinierte Dialogfeldvorlage einschließen und ihm den Steuerelementbezeichnerwert **stc32** zuweisen. (Dieser Wert wird in der Headerdatei Dlgs.h definiert.) In diesem Fall verwendet das System das -Steuerelement als Bezugspunkt, um zu bestimmen, wo die neuen Steuerelemente positioniert werden sollen. Alle neuen Steuerelemente oberhalb und links vom **stc32-Steuerelement** werden in der gleichen Menge oberhalb und links von den Steuerelementen im Standarddialogfeld positioniert. Neue Steuerelemente unten und rechts vom **stc32-Steuerelement** befinden sich unten und rechts neben den Standardsteuerelementen. Im Allgemeinen wird jedes neue Steuerelement so positioniert, dass es relativ zu den Standardsteuerelementen die gleiche Position hat wie das **stc32-Steuerelement.** Um Platz für diese neuen Steuerelemente zu schaffen, fügt das System nach Bedarf Platz auf der linken, rechten, unteren und oberen Seite des Standarddialogfelds hinzu.

Das System erfordert die Hookprozedur, um alle Für das benutzerdefinierte Dialogfeld vorgesehenen Nachrichten zu verarbeiten, und sendet daher die gleichen Fenstermeldungen an die Hookprozedur wie für jede andere Dialogfeldprozedur. Beispielsweise empfängt die Hookprozedur [**WM \_ COMMAND-Meldungen,**](/windows/desktop/menurc/wm-command) wenn der Benutzer im benutzerdefinierten Dialogfeld auf Schaltflächensteuerelemente klickt. Die Hookprozedur ist für das Initialisieren dieser Steuerelemente und das Abrufen von Werten aus den Steuerelementen zuständig, wenn das Dialogfeld geschlossen wird. Beachten Sie, dass das System die Steuerelemente noch nicht an die endgültigen Positionen verschoben hat, wenn die Hookprozedur die [**WM \_ INITDIALOG-Meldung**](wm-initdialog.md) empfängt.

Die Standarddialogfeldprozedur verarbeitet Meldungen für alle Steuerelemente im Standarddialogfeld, aber die Hookprozedur empfängt die Benachrichtigungsmeldungen für Benutzeraktionen für diese Steuerelemente, wie unter Hookprozeduren im [Explorer-Stil beschrieben.](#explorer-style-hook-procedures)

## <a name="explorer-style-control-identifiers"></a>Explorer-Style Steuerelementbezeichner

Das Windows Software Development Kit (SDK) stellt die Standarddialogfeldvorlage für die Dialogfelder im alten Stil bereit, enthält jedoch nicht die Standardvorlage für die Dialogfelder im Explorer-Stil. Dies liegt daran, dass Sie in den Dialogfeldern im Explorer-Stil eigene Steuerelemente hinzufügen können, aber das Ändern der Vorlage für die Standardsteuerelemente nicht unterstützen. In einigen Fällen müssen Sie jedoch möglicherweise die Steuerelementbezeichner kennen, die in den Standardvorlagen verwendet werden. Beispielsweise erfordern die [**CDM \_ HIDECONTROL-**](cdm-hidecontrol.md) und [**CDM \_ SETCONTROLTEXT-Meldungen**](cdm-setcontroltext.md) einen Steuerelementbezeichner.

Die folgende Tabelle zeigt die Bezeichner der Standardsteuerelemente in den Dialogfeldern Öffnen und **Speichern** unter im Explorer-Stil.  Die Bezeichner sind Konstanten, die in Dlgs.h und Winuser.h definiert sind.



| Steuerelementbezeichner | Beschreibung des Steuerelements                                                                                                                                                                                                                                                                        |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **chx1**           | Das Kontrollkästchen "Schreibgeschützt"                                                                                                                                                                                                                                                                    |
| **cmb1**           | Dropdown-Kombinationsfeld, in dem die Liste der Dateitypfilter angezeigt wird                                                                                                                                                                                                                            |
| **stc2**           | Bezeichnung für das **Kombinationsfeld cmb1**                                                                                                                                                                                                                                                           |
| **cmb2**           | Dropdown-Kombinationsfeld, das das aktuelle Laufwerk oder den aktuellen Ordner anzeigt und es dem Benutzer ermöglicht, ein Laufwerk oder einen Ordner auszuwählen, das geöffnet werden soll.                                                                                                                                                                |
| **stc4**           | Bezeichnung für das **Kombinationsfeld cmb2**                                                                                                                                                                                                                                                           |
| **cmb13**          | Dropdown-Kombinationsfeld, in dem der Name der aktuellen Datei angezeigt wird, der Benutzer den Namen einer zu öffnenden Datei eingeben und eine Datei auswählen kann, die vor Kurzem geöffnet oder gespeichert wurde. Dies gilt für frühere Explorer-kompatible Anwendungen ohne Hook- oder Dialogvorlage. Vergleichen Sie mit **edt1**. |
| **edt1**           | Bearbeitungssteuerelement, das den Namen der aktuellen Datei anzeigt oder es dem Benutzer ermöglicht, den Namen der zu öffnende Datei einzugeben. Vergleichen Sie mit **cmb13**.                                                                                                                                                  |
| **stc3**           | Bezeichnung für das **Kombinationsfeld cmb13** und das edt1-Bearbeitungssteuerelement                                                                                                                                                                                                                                |
| **lst1**           | Listenfeld, in dem der Inhalt des aktuellen Laufwerks oder Ordners angezeigt wird                                                                                                                                                                                                                         |
| **stc1**           | Bezeichnung für das Listenfeld **lst1**                                                                                                                                                                                                                                                            |
| **IDOK**           | Die Befehlsschaltfläche **OK** (Schaltfläche "Push")                                                                                                                                                                                                                                                    |
| **IDCANCEL**       | Schaltfläche **"Befehl abbrechen"** (Schaltfläche "Push")                                                                                                                                                                                                                                                |
| **pshHelp**        | Schaltfläche **"Hilfebefehl"** (Schaltfläche "Push")                                                                                                                                                                                                                                                  |



 

## <a name="customizing-old-style-dialog-boxes"></a>Anpassen Old-Style Dialogfeldern

Sie können ein altes  Dialogfeld **"Öffnen"** oder "Speichern unter" anpassen, indem Sie eine [*OFNHookProcOldStyle-Hookprozedur*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) bereitstellen, die Nachrichten oder Benachrichtigungen empfängt, die für die Standarddialogfeldprozedur vorgesehen sind. Sie können auch eine benutzerdefinierte Vorlage bereitstellen, die statt der Standardvorlage verwendet werden soll. Die hook-Prozeduren und -Vorlagen, die mit den Dialogfeldern im alten Stil verwendet werden, ähneln denen, die mit den anderen allgemeinen Dialogfeldern verwendet werden. Weitere Informationen finden Sie unter [Hook procedures for Common Dialog Boxes (Hookverfahren für allgemeine Dialogfelder)](customizing-common-dialog-boxes.md) und Custom Templates [(Benutzerdefinierte Vorlagen).](customizing-common-dialog-boxes.md)

Verwenden Sie beim Erstellen des  Dialogfelds  die [**OPENFILENAME-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) um eine Hookprozedur für ein Altes Dialogfeld "Öffnen" oder "Speichern unter" zu aktivieren. Legen Sie **das OFN \_ ENABLEHOOK-Flag** im **Flags-Member** fest, und geben Sie die Adresse einer [*OFNHookProcOldStyle-Hookprozedur*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) im **lpfnHook-Member** an. Die Dialogfeldprozedur sendet eine [**WM \_ INITDIALOG-Nachricht**](wm-initdialog.md) an die Hookprozedur, bei der der *Parameter Param* auf die Adresse der **OPENFILENAME-Struktur** festgelegt ist, die zum Initialisieren des Dialogfelds verwendet wird.

Sie können die [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) verwenden,  um  eine benutzerdefinierte Vorlage anzugeben, die im Dialogfeld Öffnen oder Speichern unter statt der Standardvorlage verwendet werden soll. Wenn Ihre benutzerdefinierte Vorlage eine Ressource in einer Anwendung oder Dynamic Link Library ist, legen Sie das **OFN \_ ENABLETEMPLATE-Flag** im **Flags-Element** fest, und verwenden Sie die **Elemente hInstance** und **lpTemplateName** der Struktur, um das Modul und den Ressourcennamen zu identifizieren. Wenn sich Ihre benutzerdefinierte Vorlage bereits im Arbeitsspeicher befindet, legen Sie das **OFN \_ ENABLETEMPLATEHANDLE-Flag** fest, und verwenden Sie das **hInstance-Element,** um das Speicherobjekt zu identifizieren, das die Vorlage enthält. Erstellen Sie die benutzerdefinierte Vorlage, indem Sie die in der Datei Fileopen.dlg angegebene Standardvorlage ändern. Die Steuerelementbezeichner, die in den Standardmäßigen Dialogfeldvorlagen suchen und ersetzen verwendet werden, werden in der Datei Dlgs.h definiert.

Standardmäßig zeigen die Funktionen [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) und [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) die Dialogfelder im Explorer-Stil an. Wenn Sie ein Dialogfeld im alten Stil anzeigen möchten, müssen Sie eine [**OFNHookProcOldStyle-Hookprozedur**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) bereitstellen und sicherstellen, dass das **\_ OFN-EXPLORER-Flag** nicht im **Flags-Member** der [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) festgelegt ist.

Wenn Sie das **\_ OFN-EXPLORER-Flag** festlegen, behandelt das System eine Hookprozedur oder eine benutzerdefinierte Vorlage als Anpassung im Explorer-Stil. Informationen zum Anpassen eines Dialogfelds im Explorer-Stil finden Sie unter Benutzerdefinierte Vorlagen im [Explorer-Stil.](#explorer-style-custom-templates)

## <a name="see-also"></a>Siehe auch

* [Beispiel für Datei wird verwendet](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse)