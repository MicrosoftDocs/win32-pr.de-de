---
description: In diesem Thema werden einige der Dinge beschrieben, die bei der Verwendung von Bibliotheken in Ihrem Programm zu berücksichtigen sind.
ms.assetid: 40ACC8F6-1416-4390-A8D7-8F924DC2C2FE
title: Verwenden von Bibliotheken in Ihrem Programm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2c76c4ce8bf9114d7294b257c03bcc62adecc947a3d7e651d6f94fa8876d4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821110"
---
# <a name="using-libraries-in-your-program"></a>Verwenden von Bibliotheken in Ihrem Programm

In diesem Thema werden einige der Dinge beschrieben, die bei der Verwendung von Bibliotheken in Ihrem Programm zu berücksichtigen sind.

In diesem Thema:

-   [Übersicht über die Bibliotheksprogrammierung](#library-programming-overview)
-   [Programmieren mit Bibliotheken](#programming-with-libraries)
    -   [Verschieben von bekannten Ordnern zu Bibliotheken](#moving-from-known-folders-to-libraries)
    -   [HomeGroup und freigegebene Bibliotheken](#homegroup-and-shared-libraries)
-   [Verwenden eines allgemeinen Dateidialogfelds mit Bibliotheken](#using-a-common-file-dialog-box-with-libraries)
-   [Aktivieren der Bibliotheksauswahl über die Benutzeroberfläche](#enabling-library-selection-from-the-user-interface)
-   [Zugreifen auf Bibliotheksinhalte in einem Programm](#accessing-library-content-in-a-program)
    -   [Zugreifen auf Bibliotheksinhalte mit der IShellLibrary-Schnittstelle](#accessing-library-content-with-the-ishelllibrary-interface)
    -   [Zugreifen auf Bibliotheksinhalte mit den Shell-APIs](#accessing-library-content-with-the-shell-apis)
-   [Speichern von Benutzerinhalten in einer Bibliothek](#saving-user-content-in-a-library)
-   [Supporting drag-and-drop operations in a library](#supporting-drag-and-drop-operations-in-a-library)
-   [Synchronisieren mit einer Bibliothek](#keeping-in-sync-with-a-library)
    -   [Massenaktualisierung](#bulk-update)
    -   [Shell-API-Benachrichtigung](#shell-api-notification)
    -   [Dateisystem-API-Benachrichtigung](#file-system-api-notification)
-   [Zugehörige Themen](#related-topics)

## <a name="library-programming-overview"></a>Übersicht über die Bibliotheksprogrammierung

Bibliotheken ermöglichen es Benutzern, ihre dateibasierten Inhalte so zu organisieren, dass sie für sie aussagekräftig sind und nicht durch die Organisation des Dateisystems eingeschränkt werden. Wenn Ihr Programm Bibliotheken unterstützt, ermöglicht es dem Benutzer, seine Inhalte auf eine Weise zu finden, die für sie sinnvoll ist, während eine Benutzeroberfläche angezeigt wird, die mit der Windows 7-Benutzeroberfläche konsistent ist. Bibliotheken erleichtern es Ihrem Programm auch, dateibasierte Inhalte zu finden, die in verschiedenen Ordnern oder auf verschiedenen Computern gespeichert sind.

In den Themen in diesem Abschnitt wird beschrieben, wie Sie Ihrem Programm Bibliotheksunterstützung hinzufügen und die neuen Funktionen nutzen können, die Bibliotheken bieten. Windows 7 bietet standardmäßig einige dieser Unterstützung. Wenn ihr Programm die allgemeinen Dateidialogfelder, die es derzeit verwendet, nicht ändert, ist möglicherweise nur sehr wenig zusätzliche Programmierung erforderlich, um Bibliotheken zu unterstützen.

In diesem Abschnitt werden einige der wichtigsten Features beschrieben, die Bibliotheken bereitstellen, und wie sie in Ihrem Programm unterstützt werden. Mit diesen Informationen können Sie entscheiden, welche Features die beste Benutzererfahrung ihres Programms bieten. Wenn Ihr Programm die allgemeinen Dateidialogfelder anpasst, können Sie mithilfe der Informationen in diesem Abschnitt bestimmen, wie sie die neuen allgemeinen Dateidialogfelder verwenden, um Bibliotheken zu verwenden und entsprechende Funktionen in Windows 7 bereitstellen.

## <a name="programming-with-libraries"></a>Programmieren mit Bibliotheken

Das Windows Shell-Programmiermodell beschreibt, wie ein Programm mit Windows Shell-Programmierobjekten interagiert. Während Dateisystemobjekte wie Dateien und Verzeichnisse durch Windows Shell-Objekte dargestellt werden, werden nicht alle Windows Shell-Objekte durch das Dateisystem dargestellt. Bibliotheken sind z. B. Windows Shell-Objekte, die kein Dateisystemäquivalent haben. Wenn Windows Shellobjekte in Ihrem Programm verwenden, kann Das Programm auf alle Shellobjekte und nicht nur auf Dateisystemobjekte zugreifen.

Um die besten Ergebnisse zu erzielen, verwendet Ihr Programm die [**Shellbibliotheks-API,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) um mit Bibliotheken zu interagieren und auf ihre Inhalte zuzugreifen. Bibliotheken enthalten Dateisystemelemente wie Ordner und Dateien, Bibliotheken sind jedoch keine Dateisystemelemente. Daher können Dateisystem-APIs nicht für den Zugriff auf Bibliotheksfeatures oder Bibliotheksinhalte verwendet werden.

Wenn Sie über ein vorhandenes Programm verfügen, das derzeit viele Dateisystem-APIs verwendet, kann Ihr Programm weiterhin Bibliotheksfunktionen nutzen. Die [**Shellbibliotheks-API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) kann Dateisystemverweise auf die Elemente bereitstellen, die sich in einer Bibliothek befinden, und diese Dateisystemverweise, z. B. der Dateiname und der Pfad, können an die vorhandenen Dateisystem-APIs übergeben werden, die sich in Ihrem vorhandenen Programm befinden.

### <a name="moving-from-known-folders-to-libraries"></a>Verschieben von bekannten Ordnern zu Bibliotheken

Vor Windows 7 war es üblich, einen bekannten Ordner, z. B. den Ordner Eigene Dokumente, als Standardordner in Dateispeicher- oder Dateiöffnungsvorgängen zu verwenden. In Windows 7 sollte die entsprechende Bibliothek verwendet werden, damit der Benutzer in Ihrem Programm die gleiche Erfahrung hat wie bei anderen Windows 7-Programmen, z. B. dem Windows Explorer.

Wenn Sie derzeit die shell Windows-API in Ihrem Programm verwenden, ist das Hinzufügen von Bibliotheksunterstützung einfach. Wenn Sie beispielsweise derzeit die [**SHGetKnownFolderItem-Funktion**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem) aufrufen, um den Speicherort des Eigene Dokumente-Ordners zu erhalten, können Sie den [**KNOWNFOLDERID-Wert**](knownfolderid.md) des bekannten Eigene Dokumente-Ordners durch den **KNOWNFOLDERID-Wert** der entsprechenden Bibliothek ersetzen.

Die folgende Tabelle zeigt die Beziehung zwischen den [**KNOWNFOLDERID-Werten**](knownfolderid.md) bekannter Ordner und dem **KNOWNFOLDERID-Wert** der entsprechenden Bibliothek in Windows 7. 

| Known Folder KNOWNFOLDERID-Werte | KNOWNFOLDERID-Bibliothekswerte |
|-----------------------------------|------------------------------|
| \_FOLDERID-Dokumente               | FOLDERID \_ DocumentsLibrary   |
| FOLDERID \_ Pictures                | FOLDERID \_ PicturesLibrary    |
| \_FOLDERID-Musik                   | FOLDERID \_ MusicLibrary       |
| FOLDERID \_ RecordedTV              | FOLDERID \_ RecordedTVLibrary  |



 

### <a name="homegroup-and-shared-libraries"></a>HomeGroup und freigegebene Bibliotheken

Das Hinzufügen von Bibliotheksunterstützung zu Ihrem Programm ermöglicht die Unterstützung freigegebener Bibliotheken in einer HomeGroup. Die HomeGroup wird durch ihren [**KNOWNFOLDERID-Wert**](knownfolderid.md) [**von FOLDERID \_ HomeGroup identifiziert.**](knownfolderid.md) Ihr Programm kann den privaten oder freigegebenen Standardspeicherort des Benutzers ermitteln, indem der [**DEFAULTSAVEFOLDERTYPE-Wert**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype) im Aufruf der [**IShellLibrary::GetDefaultSaveFolder-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getdefaultsavefolder) festgelegt wird.

## <a name="using-a-common-file-dialog-box-with-libraries"></a>Verwenden eines allgemeinen Dateidialogfelds mit Bibliotheken

Verwenden eines allgemeinen Dateidialogfelds mit Bibliotheken Das Dialogfeld "Allgemeine Datei" wurde aktualisiert, um Bibliotheken in Windows 7 zu unterstützen. Die folgende Abbildung zeigt, wie das Allgemeine Dateidialogfeld einem Benutzer in Windows 7 angezeigt wird.

![Screenshot des Dialogfelds "Allgemeine Datei" mit Bibliotheken](images/libraries-commonfiledialog.png)

In Windows 7 zeigt das Programm automatisch die neue Windows 7-Version des Dialogfelds an, wenn es derzeit ein allgemeines Dateidialogfeld anzeigt und die Dialogfeldvorlage nicht ändert oder die Ereignisse ein hookt. Insbesondere müssen die Member **lpfnHook**, **hInstance** und **lpTemplatename** der [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) im Aufruf der Allgemeinen Dateidialogfeldfunktion **NULL** sein, und die **Flags OFN \_ ENABLEHOOK** und **OFN \_ ENABLETEMPLATE** müssen eindeutig sein.

In Windows 7 ersetzen die [**IFileDialog-bezogenen**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)Schnittstellen die allgemeinen Dateidialogfeldfunktionen, die in früheren Versionen von verwendet Windows. Die früheren allgemeinen Dateidialogfeldfunktionen werden in Windows 7 weiterhin unterstützt, bieten jedoch nicht die vollständige Windows 7-Benutzeroberfläche und unterstützen keine Bibliotheken. Zu den neuen Features, die von **IFileDialog-bezogenen** Schnittstellen unterstützt werden, gehören:

-   Der Benutzer kann auf die dateieigenschaften zugreifen, die von Windows 7 Windows Explorer unterstützt werden, um die Dateien zu suchen und auszuwählen.
-   Das Programm kann Schnittstellen und Methoden aus der Shell-Namespace-API verwenden, um mit den Elementen zu arbeiten.
-   Das Programm kann ein datengesteuertes Anpassungsmodell anstelle eines ressourcendateigesteuerten Anpassungsmodells verwenden, um den allgemeinen Dateidialogfeldern neue Steuerelemente hinzuzufügen.

Sie sollten die [**IFileDialog-bezogenen**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)Schnittstellen verwenden, wenn:

-   Sie müssen das Allgemeine Dateidialogfeld für Ihr Programm in Windows 7 anpassen. Dadurch kann Ihr Programm mit Bibliotheken arbeiten und das Anpassen des Dialogfelds unterstützen.
-   Sie möchten, dass der Benutzer mehrere Dateien aus einem allgemeinen Dateidialogfeld auswählen kann. Dadurch wird sichergestellt, dass Sie die richtigen Pfade zum ausgewählten Objekt erhalten, da eine Bibliothek Inhalte enthalten kann, die in verschiedenen Ordnern gespeichert sind.

Weitere Informationen zu den [**IFileDialog-bezogenen**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)Schnittstellen finden Sie unter:

-   [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)
-   [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)
-   [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)
-   [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)
-   [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)
-   [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents)

## <a name="enabling-library-selection-from-the-user-interface"></a>Aktivieren der Bibliotheksauswahl über die Benutzeroberfläche

Wenn das Programm es dem Benutzer ermöglicht, in Windows 7 einen Ordner auszuwählen, z. B. für Import- oder Exportfunktionen, sollte es dem Benutzer auch ermöglichen, eine Bibliothek auszuwählen. Mit [**der IFileOpenDialog-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) und der [**SHBrowseForFolder-Funktion**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) kann der Benutzer eine Bibliothek auswählen, wenn er zur Auswahl eines Ordners aufgefordert wird. Die **IFileOpenDialog-Schnittstelle** wird der **SHBrowseForFolder-Funktion** vorgezogen, da **IFileOpenDialog** die Windows 7-Benutzeroberfläche unterstützt.

Damit Benutzer Ordner auswählen können, wenn sie die [**IFileOpenDialog-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) verwenden, rufen Sie SetOptions mit dem festgelegten FOS PICKFOLDERS-Flag auf, und stellen Sie sicher, dass das \_ FLAG FOS \_ FORCEFILESYSTEM klar ist.


```C++
FILEOPENDIALOGOPTIONS fileOptions;

hr = fileOpenDialogBox->GetOptions(&fileOptions);
fileOptions = fileOptions | FOS_PICKFOLDERS | ~FOS_FORCEFILESYSTEM;
hr = fileOpenDialogBox->SetOptions(fileOptions);
```



Damit Benutzer beim Aufrufen der SHBrowseForFolder-Funktion Ordner auswählen können, legen Sie im ulFlags-Member der [**BROWSEINFO-Struktur**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) das BIF USENEWUI-Flag fest, und löschen Sie das \_ \_ BIF-Flag RETURNONLYFSDIRS.


```C++
BROWSEINFO    browseInfo;
browseInfo.ulFlags = BIF_USENEWUI | ~BIF_RETURNONLYFSDIRS;
// Set other member values
pidl = SHBrowseForFolder(&browseInfo);
```



## <a name="accessing-library-content-in-a-program"></a>Zugreifen auf Bibliotheksinhalte in einem Programm

Um auf den Inhalt einer Bibliothek zuzugreifen, müssen Sie die Windows Shell-API verwenden. Funktionen der Dateisystem-API können nicht für den Zugriff auf Bibliotheksinhalte verwendet werden, da Bibliotheken keine Dateisystemobjekte sind. Wenn Ihr Programm einen benutzerdefinierten Dateibrowser verwendet, der auf der Dateisystem-API basiert, kann es keine Bibliotheken durchsuchen oder auf Bibliotheksinhalte zugreifen.

In diesem Abschnitt wird beschrieben, wie Sie auf Bibliotheksinhalte zugreifen können, damit Sie die beste Möglichkeit auswählen können, Ihr Programm für die Arbeit mit Bibliotheken zu aktualisieren.

### <a name="accessing-library-content-with-the-ishelllibrary-interface"></a>Zugreifen auf Bibliotheksinhalte mit der IShellLibrary-Schnittstelle

Die einfachste Möglichkeit für ein Programm, auf Bibliotheksinhalte zuzugreifen, ist die Verwendung der [**Shellbibliotheks-API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary). Wenn Sie an einem Programm arbeiten, das die Dateisystem-API verwendet, kann die **Shellbibliotheks-API** die Dateisystemordner einer Bibliothek zurückgeben, wodurch die Änderung des vorhandenen Programmcodes minimiert wird.


```C++
IShellLibrary *picturesLibrary;

hr = SHLoadLibraryFromKnownFolder(FOLDERID_PicturesLibrary, 
                                  STGM_READ, 
                                  IID_PPV_ARGS(&picturesLibrary));

// picturesLibrary now points to the user's picture library
    
IShellItemArray *pictureFolders; 

hr = pslLibrary->GetFolders(LFF_FORCEFILESYSTEM, IID_PPV_ARGS(&pictureFolders));

// pictureFolders now contains an array of Shell items that
// represent the folders found in the user's pictures library
```



### <a name="accessing-library-content-with-the-shell-apis"></a>Zugreifen auf Bibliotheksinhalte mit den Shell-APIs

Da die Bibliotheksobjekte Teil des Shell-Programmiermodells sind, können sie mit anderen Windows Shell-APIs verwendet werden. Beispielsweise können Sie die [**IShellItem-**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) und [**IShellFolder-Schnittstellen**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) in Ihrem Programm zusammen mit verwandten Hilfsfunktionen verwenden, um auf die Inhalte einer Bibliothek auf die gleiche Weise zuzugreifen, wie Sie Ordner und Ordnerinhalte auflisten würden, um auf Inhalte mit den Dateisystem-APIs zuzugreifen.

Die Windows Shell-APIs unterstützen zwei Enumerationsmodi für den Zugriff auf den Inhalt einer Bibliothek:

-   **Durchsuchen der Enumeration**

    Die Durchsuchenenumeration ist der Standardenumerationsmodus und listet den Inhalt eines Bibliotheksordners auf. Löschen Sie das SHCONTF \_ \_ NAVIGATION-ENUM-Flag, um diesen Modus zu verwenden.

-   **Navigationsenumeration**

    Die Navigationsenumeration listet die Bibliotheksordner auf. Legen Sie das SHCONTF \_ \_ NAVIGATION-ENUM-Flag so fest, dass dieser Modus verwendet wird.

Wenn Ihr Programm ein benutzerdefiniertes Struktursteuerelement verwendet, um in den Ordnern des Benutzers zu navigieren, erhalten Sie beim Auflisten der Ordner im Navigationsenumerationsmodus eine Liste der Ordner einer Bibliothek, die mit der Aufzählung von Ordnern im Windows Explorer in Windows 7 konsistent ist.

Beispiele für die Verwendung dieser Features in einem Programm finden Sie im ShellStorage-Beispiel im Windows SDK.

## <a name="saving-user-content-in-a-library"></a>Speichern von Benutzerinhalten in einer Bibliothek

Ihr Programm kann Benutzerinhalte sowohl in einer Bibliothek als auch in einem Ordner in der Bibliothek speichern. Ebenso kann der Benutzer in einem bestimmten Ordner in einer Bibliothek speichern oder einfach in der Bibliothek speichern.

Jede Bibliothek verfügt über einen Ordner, der als Standardspeicherort festgelegt ist. Der Standardspeicherort wird definiert, wenn die Bibliothek erstellt wird. der Benutzer kann den Standardspeicherort jedoch einem beliebigen Ordner in der Bibliothek zuweisen. Der Benutzer muss zwar keinen Standardspeicherort konfigurieren, hat aber die Möglichkeit, ihn zu ändern. Wenn der Benutzer den Ordner löscht, der derzeit als Standardspeicherort festgelegt ist, konfiguriert die Bibliothek automatisch den nächsten Ordner in der Bibliothek als Standardspeicherort.

Es gibt mehrere Möglichkeiten, Benutzerinhalte in einer Bibliothek zu speichern.

-   **Shell-API**

    Wenn Sie das Shell-Programmiermodell verwenden und ein Shellelement, wie durch [**ein IShellItem,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem)IStorage oder IStream dargestellt, in einem Bibliotheksobjekt speichern, wird das Shellelement automatisch am Standardspeicherort der Bibliothek gespeichert.

-   **Dateisystem-API**

    Wenn Sie über ein vorhandenes Programm verfügen, das viele Dateisystem-API-Aufrufe verwendet, können Sie einen Pfad zu dem Ordner abrufen, der als Standardspeicherort der Bibliothek definiert ist. Der Ordnerpfad kann dann an eine Dateisystem-API übergeben werden.

Beispiele für die Verwendung dieser Features in einem Programm finden Sie im ShellStorage-Beispiel im Windows SDK.

## <a name="supporting-drag-and-drop-operations-in-a-library"></a>Unterstützen von Drag & Drop-Vorgängen in einer Bibliothek

Wenn Ihr Programm Drag & Drop-Aktionen unterstützt, sollten diese aktualisiert werden, um die richtige Bibliotheksinteraktion zu unterstützen. Wenn eine Datei in einer Bibliothek abgelegt wird, sollte die gelöschte Datei am Standardspeicherort gespeichert werden. Wenn ein Ordner in einer Bibliothek abgelegt wird, sollte der gelöschte Ordner der Bibliothek als neuer Ordner hinzugefügt werden. Wenn eine Datei in einem vorhandenen Ordner abgelegt wird, der nicht der Standardspeicherort ist, sollte die Datei dem ausgewählten Ordner hinzugefügt werden.

Beispiele zum Hinzufügen von Bibliotheksunterstützung für die Drag & Drop-Funktionalität Ihrer Programme finden Sie im ShellLibraryCommandLine-Beispiel im Windows SDK.

## <a name="keeping-in-sync-with-a-library"></a>Synchronisierung mit einer Bibliothek

In diesem Thema wird beschrieben, wie ein Programm seine Ansicht des Inhalts einer Bibliothek auf dem neuesten Stand halten kann.

### <a name="bulk-update"></a>Massenaktualisierung

Da der Benutzer die Ordner einer Bibliothek interaktiv ändern kann, wenn das Programm nicht ausgeführt wird, sollte das Programm [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) aufrufen, wenn es beginnt, Änderungen an der Bibliothek zu ermitteln und zu speichern. Die Shell-API stellt die **SHResolveLibrary-Funktion** bereit, mit der ein Programm den aktuellen Inhalt einer Bibliothek und die aktuellen Speicherorte aller Ordner abrufen kann, die die Bibliothek enthalten kann.

Beachten Sie, dass [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) eine blockierende Funktion ist, die abhängig von den Änderungen in der Bibliothek lange dauern kann. Daher sollte er nicht von einem UI-Thread aufgerufen werden.

Nachdem das Programm auf den neuesten Stand gebracht wurde, kann es sich für Änderungsbenachrichtigungen registrieren, um eine aktuelle Ansicht beizubehalten.

### <a name="shell-api-notification"></a>Shell-API-Benachrichtigung

Die Windows Shell-API stellt die [**SHChangeNotifyRegister-Funktion**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) bereit. Dies ist die bevorzugte Methode für Nicht-Dienstprozesse, um über eine Änderung in der Bibliothek benachrichtigt zu werden.

Um Änderungen an Elementen in einer Bibliothek mithilfe der Windows Shell-API zu erkennen, rufen Sie [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) auf, um Ihr Programm für Benachrichtigungen über Änderungen an Elementen in einem Bibliotheksordner zu registrieren. Diese Funktion kann Ihr Programm benachrichtigen, wenn eine Änderung in einer Bibliothek oder nur in einer bestimmten Bibliothek vorliegt. Benachrichtigungen werden sofort gesendet, wenn eine Bibliothek geändert wird.

### <a name="file-system-api-notification"></a>Dateisystem-API-Benachrichtigung

Dateisystembenachrichtigungen müssen in Dienstprozessen verwendet werden.

Um Änderungen an Elementen in einer Bibliothek mithilfe der Dateisystem-API zu erkennen, müssen Sie die Ordner in der Bibliothek aufzählen und [**FindFirstChangeNotification**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) für jeden zu überwachenden Ordner aufrufen. Ihr Programm erhält eine Benachrichtigung, wenn sich ein überwachter Ordner ändert. Rufen Sie [**ReadDirectoryChangesW**](/windows/win32/api/winbase/nf-winbase-readdirectorychangesw)auf, um die dateispezifische Datei zu finden, die sich im Ordner geändert hat. Um Änderungen in der Bibliotheksbeschreibungsdatei zu erkennen, überwachen Sie den Ordner, in dem sie enthalten ist. Die Bibliotheksbeschreibungsdatei befindet sich im Ordner [**FOLDERID \_ Libraries.**](knownfolderid.md) Die Bibliotheksbeschreibungsdatei sollte jedoch nicht geöffnet oder geändert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Bibliotheken](library-leverage-to-manage-folders.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Shelllinks](./links.md)
</dt> <dt>

[Bekannte Ordner](known-folders.md)
</dt> <dt>

[Bibliotheksbeschreibungsschema](library-schema-entry.md)
</dt> <dt>

[**IID \_ PPV \_ ARGS**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
