---
description: In diesem Thema werden einige Aspekte beschrieben, die bei der Verwendung von Bibliotheken in Ihrem Programm zu beachten sind.
ms.assetid: 40ACC8F6-1416-4390-A8D7-8F924DC2C2FE
title: Verwenden von Bibliotheken in Ihrem Programm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2812a66b148d9bd16fc3951efab64a4d37afaaff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350358"
---
# <a name="using-libraries-in-your-program"></a>Verwenden von Bibliotheken in Ihrem Programm

In diesem Thema werden einige Aspekte beschrieben, die bei der Verwendung von Bibliotheken in Ihrem Programm zu beachten sind.

In diesem Thema:

-   [Übersicht über die Bibliothek Programmierung](#library-programming-overview)
-   [Programmieren mit Bibliotheken](#programming-with-libraries)
    -   [Verschieben von bekannten Ordnern in Bibliotheken](#moving-from-known-folders-to-libraries)
    -   [Heim Netzgruppe und freigegebene Bibliotheken](#homegroup-and-shared-libraries)
-   [Verwenden eines allgemeinen Datei Dialogfelds mit Bibliotheken](#using-a-common-file-dialog-box-with-libraries)
-   [Aktivieren der Bibliotheks Auswahl über die Benutzeroberfläche](#enabling-library-selection-from-the-user-interface)
-   [Zugreifen auf Bibliotheksinhalte in einem Programm](#accessing-library-content-in-a-program)
    -   [Zugreifen auf Bibliotheksinhalte mit der ishelllibrary-Schnittstelle](#accessing-library-content-with-the-ishelllibrary-interface)
    -   [Zugreifen auf Bibliotheksinhalte mit den Shell-APIs](#accessing-library-content-with-the-shell-apis)
-   [Speichern von Benutzer Inhalt in einer Bibliothek](#saving-user-content-in-a-library)
-   [Unterstützen von Drag & Drop-Vorgängen in einer Bibliothek](#supporting-drag-and-drop-operations-in-a-library)
-   [Synchronisierung mit einer Bibliothek](#keeping-in-sync-with-a-library)
    -   [Massenaktualisierung](#bulk-update)
    -   [Shell-API-Benachrichtigung](#shell-api-notification)
    -   [Dateisystem-API-Benachrichtigung](#file-system-api-notification)
-   [Zugehörige Themen](#related-topics)

## <a name="library-programming-overview"></a>Übersicht über die Bibliothek Programmierung

Mithilfe von Bibliotheken können Benutzer ihren dateibasierten Inhalt auf eine Weise organisieren, die für Sie von Bedeutung ist und nicht durch die Organisation des Dateisystems eingeschränkt ist. Wenn Ihr Programmbibliotheken unterstützt, ermöglicht es dem Benutzer, seinen Inhalt auf eine Weise zu finden, die für Sie sinnvoll ist, während eine Benutzeroberfläche angezeigt wird, die mit der Windows 7-Benutzeroberfläche konsistent ist. Bibliotheken erleichtern es Ihrem Programm außerdem, dateibasierten Inhalt zu finden, der in anderen Ordnern oder auf unterschiedlichen Computern gespeichert ist.

In den Themen in diesem Abschnitt wird beschrieben, wie Sie Ihrem Programm Bibliotheks Unterstützung hinzufügen und die neuen Funktionen nutzen können, die von Bibliotheken angeboten werden. Windows 7 bietet standardmäßig einige dieser Unterstützung. Wenn das Programm die üblichen Datei Dialogfelder, die derzeit verwendet werden, nicht ändert, ist es möglicherweise sehr wenig zusätzliche Programmierung erforderlich, um Bibliotheken zu unterstützen.

In diesem Abschnitt werden einige der wichtigsten Funktionen beschrieben, die von Bibliotheken bereitgestellt werden, sowie deren Unterstützung in Ihrem Programm. Mit diesen Informationen können Sie entscheiden, welche Features die beste Benutzer Leistung Ihres Programms bieten. Wenn das Programm die allgemeinen Datei Dialogfelder anpasst, können Sie anhand der Informationen in diesem Abschnitt festlegen, wie die neuen allgemeinen Datei Dialogfelder verwendet werden sollen, um Bibliotheken zu verwenden und entsprechende Funktionen in Windows 7 bereitzustellen.

## <a name="programming-with-libraries"></a>Programmieren mit Bibliotheken

Das Windows Shell-Programmiermodell beschreibt, wie ein Programm mit Windows Shell-Programmier Objekten interagiert. Dateisystem Objekte, z. b. Dateien und Verzeichnisse, werden von Windows-shellobjekten dargestellt, nicht jedoch alle Windows Shell-Objekte werden durch das Dateisystem dargestellt. Bibliotheken sind z. b. Windows-Shellobjekte, die keine Dateisystem Entsprechung aufweisen. Durch die Verwendung von Windows-shellobjekten in Ihrem Programm kann Ihr Programm auf alle Shellobjekte und nicht nur auf Dateisystem Objekte zugreifen.

Um die besten Ergebnisse zu erzielen, verwendet das Programm die [**shellbibliotheks-API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) , um mit Bibliotheken zu interagieren und auf ihren Inhalt zuzugreifen. Bibliotheken, die Dateisystem Elemente enthalten, wie z. b. Ordner und Dateien, sind Bibliotheken keine Dateisystem Elemente. Daher können Dateisystem-APIs nicht für den Zugriff auf Bibliotheksfunktionen oder Bibliotheksinhalte verwendet werden.

Wenn Sie über ein vorhandenes Programm verfügen, das zurzeit viele Dateisystem-APIs verwendet, kann Ihr Programm weiterhin Bibliotheksfunktionen nutzen. Die [**shellbibliotheks-API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) kann Dateisystem Verweise auf die Elemente bereitstellen, die in einer Bibliothek gefunden werden, und diese Dateisystem Verweise, wie z. b. der Dateiname und der Pfad, können an die vorhandenen Dateisystem-APIs in Ihrem vorhandenen Programm übermittelt werden.

### <a name="moving-from-known-folders-to-libraries"></a>Verschieben von bekannten Ordnern in Bibliotheken

Vor Windows 7 war es üblich, einen bekannten Ordner (z. b. den Ordner "eigene Dateien") als Standardordner in Datei speichern oder Datei Öffnungs Vorgängen zu verwenden. In Windows 7 sollte die entsprechende Bibliothek verwendet werden, damit der Benutzer in Ihrem Programm genauso wie bei anderen Windows 7-Programmen wie Windows Explorer arbeiten kann.

Wenn Sie zurzeit die Windows-Shell-API in Ihrem Programm verwenden, ist das Hinzufügen von Bibliotheks Unterstützung unkompliziert. Wenn Sie z. b. zurzeit die Funktion " [**shgetknownfolderitem**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem) " aufrufen, um den Speicherort des Ordners "eigene Dateien" abzurufen, können Sie den Wert von " [**KNOWNFOLDERID**](knownfolderid.md) " des bekannten Ordners "eigene Dokumente" durch den Wert " **KNOWNFOLDERID** " der entsprechenden Bibliothek ersetzen.

In der folgenden Tabelle wird die Beziehung zwischen den [**KNOWNFOLDERID**](knownfolderid.md) -Werten bekannter Ordner und dem **KNOWNFOLDERID** -Wert der entsprechenden Bibliothek in Windows 7 angezeigt. 

| KNOWNFOLDERID-Werte bekannter Ordner | Bibliothek KNOWNFOLDERID-Werte |
|-----------------------------------|------------------------------|
| Folderid- \_ Dokumente               | Folderid \_ documentslibrary   |
| Folderid- \_ Bilder                | Folderid \_ pictureslibrary    |
| Folderid- \_ Musik                   | Folderid \_ musiclibrary       |
| Folderid \_ recordebug              | Folderid \_ recordedtvlibrary  |



 

### <a name="homegroup-and-shared-libraries"></a>Heim Netzgruppe und freigegebene Bibliotheken

Das Hinzufügen von Bibliotheks Unterstützung zu Ihrem Programm ermöglicht die Unterstützung für freigegebene Bibliotheken in einer Heim Netzgruppe. Die Heim Netzgruppe wird durch Ihren [**KNOWNFOLDERID**](knownfolderid.md) -Wert von [**folderid \_ HomeGroup**](knownfolderid.md)identifiziert. Das Programm kann den privaten oder freigegebenen Standard Speicherort des Benutzers ermitteln, indem er den Wert von [**defaultsavefoldertype**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype) beim Aufrufen der [**ishelllibrary:: getdefaultsavefolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getdefaultsavefolder) -Methode festlegt.

## <a name="using-a-common-file-dialog-box-with-libraries"></a>Verwenden eines allgemeinen Datei Dialogfelds mit Bibliotheken

Mithilfe eines allgemeinen Datei Dialogfelds mit Bibliotheken wurde das Dialogfeld "common file" (Datei) für die Unterstützung von Bibliotheken in Windows 7 aktualisiert. In der folgenden Abbildung wird gezeigt, wie das Dialogfeld für die gemeinsame Datei einem Benutzer in Windows 7 angezeigt wird.

![Screenshot des Dialog Felds "allgemeine Datei" mit Bibliotheken](images/libraries-commonfiledialog.png)

In Windows 7 wird die neue Windows 7-Version des Dialog Felds automatisch angezeigt, wenn in Ihrem Programm derzeit ein gemeinsames Datei Dialogfeld angezeigt wird und die Dialogfeld Vorlage nicht geändert wird. Insbesondere beim Aufrufen der Dialogfeld Funktion für allgemeine Dateien müssen die **lpfnhook**-, **HINSTANCE**-, **lptemplatename** -Member der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur **null** sein, und die **ofn \_ ENABLEHOOK** -und **ofn \_ ENABLETEMPLATE** -Flags müssen klar sein.

In Windows 7 ersetzen die [**ifiledialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)-bezogenen Schnittstellen die Funktionen der allgemeinen Datei Dialogfelder, die in früheren Versionen von Windows verwendet wurden. Die früheren Funktionen für Datei Dialogfelder werden in Windows 7 weiterhin unterstützt, bieten aber nicht die komplette Windows 7-Benutzerfunktion, und Sie unterstützen keine Bibliotheken. Zu den neuen Funktionen, die von den **ifiledialog**-bezogenen Schnittstellen unterstützt werden, gehören:

-   Der Benutzer kann auf die Dateieigenschaften zugreifen, die vom Windows-Explorer von Windows 7 unterstützt werden, um die Dateien zu suchen und auszuwählen.
-   Das Programm kann Schnittstellen und Methoden aus der Shell-Namespace-API verwenden, um mit den Elementen zu arbeiten.
-   Das Programm kann ein Daten gesteuerungsanpassungs Modell anstelle eines Ressourcen Datei gesteuerten Anpassungs Modells verwenden, um den Dialogfeldern der allgemeinen Datei neue Steuerelemente hinzuzufügen.

Sie sollten die [**ifiledialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)-bezogenen Schnittstellen verwenden, wenn Folgendes der Fall ist:

-   Sie müssen das Dialogfeld "allgemeine Datei" für Ihr Programm in Windows 7 anpassen. Dies ermöglicht es Ihrem Programm, mit Bibliotheken zu arbeiten und die Anpassung des Dialog Felds zu unterstützen.
-   Sie möchten, dass der Benutzer in der Lage ist, mehrere Dateien aus einem allgemeinen Datei Dialogfeld auszuwählen. Dadurch wird sichergestellt, dass Sie die richtigen Pfade zum ausgewählten Objekt erhalten, da eine Bibliothek Inhalte enthalten kann, die in unterschiedlichen Ordnern gespeichert sind.

Weitere Informationen zu den [**ifiledialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)-bezogenen Schnittstellen finden Sie unter:

-   [**Ifiledialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)
-   [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)
-   [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)
-   [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)
-   [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)
-   [**Ifiledialogcontrolevents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents)

## <a name="enabling-library-selection-from-the-user-interface"></a>Aktivieren der Bibliotheks Auswahl über die Benutzeroberfläche

Wenn das Programm es dem Benutzer ermöglicht, einen Ordner (z. b. für Import-oder Exportfunktionen) in Windows 7 auszuwählen, sollte er es dem Benutzer ermöglichen, auch eine Bibliothek auszuwählen. Mit der [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) -Schnittstelle und der [**shbrowsforfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) -Funktion können Benutzer eine Bibliothek auswählen, wenn Sie aufgefordert werden, einen Ordner auszuwählen. Die **IFileOpenDialog** -Schnittstelle wird von der **shbrowseforfolder** -Funktion bevorzugt, da **IFileOpenDialog** die Benutzeroberfläche von Windows 7 unterstützt.

Um Benutzern das Auswählen von Ordnern bei Verwendung der [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) -Schnittstelle zu gestatten, nennen Sie "SetOptions" mit dem \_ festgelegten "Fos pickfolders"-Flag, und stellen Sie sicher, dass das Fos- \_ Flag für "


```C++
FILEOPENDIALOGOPTIONS fileOptions;

hr = fileOpenDialogBox->GetOptions(&fileOptions);
fileOptions = fileOptions | FOS_PICKFOLDERS | ~FOS_FORCEFILESYSTEM;
hr = fileOpenDialogBox->SetOptions(fileOptions);
```



Damit Benutzerordner auswählen können, wenn Sie die shbrowseforfolder-Funktion aufrufen, legen Sie im ulflags-Member der [**Browseinfo**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) -Struktur das BIF \_ usenewui-Flag fest, und deaktivieren Sie das Flag BIF-Rückrufe \_ .


```C++
BROWSEINFO    browseInfo;
browseInfo.ulFlags = BIF_USENEWUI | ~BIF_RETURNONLYFSDIRS;
// Set other member values
pidl = SHBrowseForFolder(&browseInfo);
```



## <a name="accessing-library-content-in-a-program"></a>Zugreifen auf Bibliotheksinhalte in einem Programm

Um auf den Inhalt einer Bibliothek zuzugreifen, müssen Sie die Windows-Shell-API verwenden. Funktionen der Dateisystem-API können nicht für den Zugriff auf Bibliotheksinhalte verwendet werden, da es sich bei Bibliotheken nicht um Dateisystem Objekte handelt. Wenn das Programm einen benutzerdefinierten Dateibrowser verwendet, der auf der Dateisystem-API basiert, ist es nicht möglich, Bibliotheken zu durchsuchen oder auf Bibliotheksinhalte zuzugreifen.

In diesem Abschnitt wird beschrieben, wie Sie auf Bibliotheksinhalte zugreifen können, sodass Sie die beste Methode zum Aktualisieren des Programms für die Arbeit mit Bibliotheken auswählen können.

### <a name="accessing-library-content-with-the-ishelllibrary-interface"></a>Zugreifen auf Bibliotheksinhalte mit der ishelllibrary-Schnittstelle

Die einfachste Möglichkeit für ein Programm, auf Bibliotheksinhalte zuzugreifen, ist die Verwendung der [**shellbibliotheks-API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary). Wenn Sie an einem Programm arbeiten, das die Dateisystem-API verwendet, kann die **shellbibliotheks-API** die Dateisystem Ordner einer Bibliothek zurückgeben, wodurch die Änderungen an Ihrem vorhandenen Programmcode minimiert werden.


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

Da die Bibliotheksobjekte Teil des shellprogrammierungs Modells sind, können Sie mit anderen Windows Shell-APIs verwendet werden. Beispielsweise können Sie die [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) -und [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle in Ihrem Programm zusammen mit zugehörigen Hilfsfunktionen verwenden, um auf die Inhalte einer Bibliothek auf die gleiche Weise zuzugreifen, wie Sie Ordner und Ordnerinhalte auflisten, um auf Inhalte mit den Dateisystem-APIs zuzugreifen.

Die Windows-Shell-APIs unterstützen zwei enumerationsmodi, um auf den Inhalt einer Bibliothek zuzugreifen:

-   **Enumeration durchsuchen**

    Browse Enumeration ist der standardenumerationsmodus und listet den Inhalt eines Bibliotheks Ordners auf. Löschen Sie das shcontf-Navigations Aufzählungs \_ \_ Flag, um diesen Modus zu verwenden.

-   **Navigationenumeration**

    Navigations Enumeration listet die Bibliotheks Ordner auf. Legen Sie das shcontf- \_ Navigations- \_ enum-Flag auf diesen Modus fest.

Wenn das Programm ein benutzerdefiniertes Struktur Steuerelement verwendet, um die Ordner des Benutzers zu durchsuchen, erhalten Sie durch das Auflisten der Ordner im Navigations-enumerationsmodus eine Liste der Ordner einer Bibliothek, die der Art und Weise entspricht, wie der Windows-Explorer Ordner in Windows 7 auflistet.

Beispiele dazu, wie diese Funktionen in einem Programm verwendet werden, finden Sie im shellstorage-Beispiel im Windows SDK.

## <a name="saving-user-content-in-a-library"></a>Speichern von Benutzer Inhalt in einer Bibliothek

Das Programm kann Benutzerinhalte in einer Bibliothek und in einem Ordner in der Bibliothek speichern. Ebenso kann der Benutzer in einem bestimmten Ordner in einer Bibliothek speichern oder einfach in der Bibliothek speichern.

Jede Bibliothek verfügt über einen Ordner, der als Standard Speicherort festgelegt ist. Der Standard Speicherort wird definiert, wenn die Bibliothek erstellt wird. Allerdings kann der Benutzer den Standard Speicherort erneut als einen beliebigen Ordner in der Bibliothek zuweisen. Der Benutzer muss zwar keinen Standard Speicherort konfigurieren, er kann jedoch geändert werden. Wenn der Benutzer den Ordner löscht, der derzeit als Standard Speicherort festgelegt ist, wird der nächste Ordner in der Bibliothek von der Bibliothek automatisch als Standard Speicherort konfiguriert.

Es gibt mehrere Möglichkeiten, wie Sie Benutzerinhalte in einer Bibliothek speichern können.

-   **Shell-API**

    Wenn Sie das shellprogrammierungs Modell verwenden und ein shellelement, das von einem [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem)-, IStorage-oder IStream-Objekt dargestellt wird, in einem Bibliotheksobjekt speichern, wird das shellelement automatisch am Standard Speicherort der Bibliothek gespeichert.

-   **Dateisystem-API**

    Wenn Sie über ein vorhandenes Programm verfügen, das viele Dateisystem-API-Aufrufe verwendet, können Sie einen Pfad zu dem Ordner erhalten, der als Standard Speicherort der Bibliothek definiert ist. Der Ordner Pfad kann dann an eine Dateisystem-API weitergeleitet werden.

Beispiele dazu, wie diese Funktionen in einem Programm verwendet werden, finden Sie im shellstorage-Beispiel im Windows SDK.

## <a name="supporting-drag-and-drop-operations-in-a-library"></a>Unterstützen von Drag & Drop-Vorgängen in einer Bibliothek

Wenn das Programm Drag & amp; Drop-Aktionen unterstützt, sollten diese aktualisiert werden, um die korrekte Bibliotheks Interaktion zu unterstützen. Wenn eine Datei in einer Bibliothek abgelegt wird, sollte die gelöschte Datei am Standard Speicherort gespeichert werden. Wenn ein Ordner in einer Bibliothek abgelegt wird, sollte der gelöschte Ordner der Bibliothek als neuer Ordner hinzugefügt werden. Wenn eine Datei in einem vorhandenen Ordner abgelegt wird, der nicht der Standard Speicherort ist, muss die Datei dem ausgewählten Ordner hinzugefügt werden.

Beispiele zum Hinzufügen von Bibliotheks Unterstützung für Ihre Programme Drag & amp; Drop-Funktionen finden Sie im Beispiel shelllibrarycommandline im Windows SDK.

## <a name="keeping-in-sync-with-a-library"></a>Synchronisierung mit einer Bibliothek

In diesem Thema wird beschrieben, wie ein Programm den Inhalt einer Bibliothek auf dem neuesten standhalten kann.

### <a name="bulk-update"></a>Massenaktualisierung

Da der Benutzer die Ordner einer Bibliothek interaktiv ändern kann, wenn das Programm nicht ausgeführt wird, sollte das Programm " [**shresolvelibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) " aufrufen, wenn es beginnt, Änderungen an der Bibliothek zu ermitteln und zu speichern. Die Shell-API stellt die Funktion " **shresolvelibrary** " bereit, mit der ein Programm den aktuellen Inhalt einer Bibliothek und die aktuellen Speicherorte aller Ordner, die in der Bibliothek enthalten sein können, erhalten.

Beachten Sie, dass " [**shresolvelibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) " eine blockierende Funktion ist, die abhängig von den Änderungen in der Bibliothek viel Zeit in Anspruch nehmen kann. Daher sollte es nicht von einem UI-Thread aufgerufen werden.

Nachdem das Programm auf den neuesten Stand gebracht wurde, kann es sich für Änderungs Benachrichtigungen registrieren, um eine aktuelle Ansicht zu erhalten.

### <a name="shell-api-notification"></a>Shell-API-Benachrichtigung

Die Windows-Shell-API stellt die [**shchangenotifyregister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) -Funktion bereit. Dies ist die bevorzugte Methode für nicht-Dienst Prozesse, um über eine Änderung in der Bibliothek benachrichtigt zu werden.

Um Änderungen an Elementen in einer Bibliothek mithilfe der Windows-Shell-API zu erkennen, rufen Sie [**shchangenotifyregister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) auf, um das Programm für Benachrichtigungen über Änderungen an Elementen in einem Bibliotheks Ordner zu registrieren. Diese Funktion kann Ihr Programm Benachrichtigen, wenn eine Änderung in einer Bibliothek oder nur in einer bestimmten Bibliothek vorliegt. Benachrichtigungen werden sofort gesendet, wenn eine Bibliothek geändert wird.

### <a name="file-system-api-notification"></a>Dateisystem-API-Benachrichtigung

Dateisystem Benachrichtigungen müssen bei Dienst Vorgängen verwendet werden.

Zum Erkennen von Änderungen an Elementen in einer Bibliothek mithilfe der Dateisystem-API können Sie die Ordner in der Bibliothek auflisten und [**findfirstchangenotififür**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) jeden zu überwachenden Ordner aufzurufen. Das Programm empfängt eine Benachrichtigung, wenn sich ein überwachter Ordner ändert. Um die Datei mit den Dateien zu suchen, die sich im Ordner geändert haben, rufen Sie "read [**directorychangesw**](/windows/win32/api/winbase/nf-winbase-readdirectorychangesw)" auf. Um Änderungen in der Bibliotheks Beschreibungsdatei zu erkennen, überwachen Sie den Ordner, in dem Sie enthalten ist. Die Bibliotheks Beschreibungsdatei befindet sich im Ordner [**folderid \_ Libraries**](knownfolderid.md) . Die Bibliotheks Beschreibungsdatei sollte jedoch nicht geöffnet oder geändert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Bibliotheken](library-leverage-to-manage-folders.md)
</dt> <dt>

[**Ishelllibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Shelllinks](./links.md)
</dt> <dt>

[Bekannte Ordner](known-folders.md)
</dt> <dt>

[Bibliotheks Beschreibungs Schema](library-schema-entry.md)
</dt> <dt>

[**IID \_ PPV-Argumente \_**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
