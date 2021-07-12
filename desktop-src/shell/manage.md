---
description: Die Shell bietet eine Reihe von Möglichkeiten zum Verwalten von Dateisystemen.
ms.assetid: d9ffda6f-adc0-44a3-b410-e23bf5f4f165
title: Verwalten des Dateisystems
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0f3b47e17e691c540a9775f3b8588b311b9878
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581618"
---
# <a name="managing-the-file-system"></a>Verwalten des Dateisystems

Die Shell bietet eine Reihe von Möglichkeiten zum Verwalten von Dateisystemen. Die Shell stellt die Funktion [**SHFileOperation bereit,**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)mit der eine Anwendung Dateien programmgesteuert verschieben, kopieren, umbenennen und löschen kann. Die Shell unterstützt auch einige zusätzliche Dateiverwaltungsfunktionen.

-   HTML-Dokumente können mit verwandten Dateien wie Grafikdateien oder Stylesheets *verbunden* werden. Wenn das Dokument verschoben oder kopiert wird, werden die verbundenen Dateien ebenfalls automatisch verschoben oder kopiert.
-   Für Systeme, die für mehrere Benutzer verfügbar sind, können Dateien pro Benutzer verwaltet werden. Benutzer haben einfachen Zugriff auf ihre Datendateien, aber nicht auf Dateien, die anderen Benutzern gehören.
-   Wenn Dokumentdateien hinzugefügt oder geändert werden, können sie der Shell-Liste der zuletzt verwendeten Dokumente hinzugefügt werden. Wenn der Benutzer auf dem Startmenü auf den Befehl **Dokumente** klickt, wird eine Liste mit Links zu den Dokumenten angezeigt.

In diesem Dokument wird erläutert, wie diese Dateiverwaltungstechnologien funktionieren. Anschließend wird beschrieben, wie Sie die Shell zum Verschieben, Kopieren, Umbenennen und Löschen von Dateien verwenden und objekte im Papierkorb verwalten.

-   [Dateiverwaltung pro Benutzer](#per-user-file-management)
-   [Ordner "Eigene Dokumente" und "Meine Bilder"](#my-documents-and-my-pictures-folders)
-   [Verbundene Dateien](#connected-files)
-   [Verschieben, Kopieren, Umbenennen und Löschen von Dateien](#moving-copying-renaming-and-deleting-files)
    -   [Benachrichtigen der Shell](#notifying-the-shell)
-   [Einfaches Beispiel für die Verwaltung von Dateien mit SHFileOperation](#simple-example-of-managing-files-with-shfileoperation)
-   [Hinzufügen von Dateien zur Shellliste zuletzt verwendeter Dokumente](#adding-files-to-the-shells-list-of-recent-documents)

## <a name="per-user-file-management"></a>Per-User Dateiverwaltung

Die Windows 2000 Shell ermöglicht die Zuordnung von Dateien zu einem bestimmten Benutzer, sodass die Dateien für andere Benutzer ausgeblendet bleiben. Im Hinblick auf das Dateisystem werden die Dateien im Profilordner des Benutzers gespeichert, in der Regel C: \\ Dokumente und Einstellungen \\ *Benutzername* \\ auf Windows 2000-Systemen. Dieses Feature ermöglicht es vielen Personen, denselben Computer zu verwenden und gleichzeitig den Datenschutz ihrer Dateien von anderen Benutzern zu wahren. Für verschiedene Benutzer können unterschiedliche Programme verfügbar sein. Außerdem bietet es Administratoren und Anwendungen eine einfache Möglichkeit, z.B. Initialisierungs- (.ini) oder Linkdateien (LNK) zu speichern. Anwendungen können daher einen anderen Zustand für jeden Benutzer beibehalten und diesen bestimmten Zustand bei Bedarf problemlos wiederherstellen. Es gibt auch einen Profilordner zum Speichern von Informationen, die allen Benutzern gemeinsam sind.

Da es unpraktisch ist, zu bestimmen, welcher Benutzer angemeldet ist und wo sich seine Dateien befinden, handelt es sich bei den Standardordnern pro Benutzer um spezielle Ordner, die durch eine [**CSIDL**](csidl.md)identifiziert werden. Die CSIDL für den Ordner Programme pro Benutzer lautet z. B. CSIDL \_ PROGRAMS. Wenn Ihre Anwendung [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) oder [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) mit einer der CSIDLs pro Benutzer aufruft, gibt die Funktion den Zeiger auf eine Elementbezeichnerliste (PIDL) oder einen Pfad zurück, der dem derzeit angemeldeten Benutzer entspricht. Wenn Ihre Anwendung den Pfad oder die PIDL des Profilordners abrufen muss, lautet die CSIDL **CSIDL \_ PROFILE.**

## <a name="my-documents-and-my-pictures-folders"></a>Ordner "Eigene Dokumente" und "Meine Bilder"

Eines der Standardsymbole auf dem Desktop ist **Eigene Dokumente**. Wenn Sie diesen Ordner öffnen, enthält er die Dokumentdateien des aktuellen Benutzers. Die Desktopinstanz von Eigene Dokumente ist ein virtueller Ordner – ein Alias für den Dateisystemspeicherort, der zum physischen Speichern der Benutzerdokumente verwendet wird – direkt unterhalb des Desktops in der Namespacehierarchie.

Der Zweck der Ordner "Eigene Dokumente" und "Meine Bilder" besteht darin, Benutzern einen einfachen und sicheren Zugriff auf ihre Dokument- und Bilddateien auf einem System mit mehreren Benutzern zu ermöglichen. Jedem Benutzer werden separate Dateisystemordner für seine Dateien zugewiesen. Der Speicherort des Ordners "documents" eines Benutzers im Dateisystem ist beispielsweise in etwa wie folgt: C: \\ Dokumente und Einstellungen \\ *Benutzername* \\ Eigene Dokumente. Es ist nicht erforderlich, dass Benutzer etwas über den physischen Speicherort ihrer Dateisystemordner wissen. Sie greifen einfach über das symbol Eigene Dokumente auf ihre Dateien zu.

> [!Note]  
> Eigene Dokumente ermöglicht es einem Benutzer, auf seine eigenen Dateien zuzugreifen, jedoch nicht auf die Dateien eines anderen Benutzers. Wenn mehrere Personen denselben Computer verwenden, kann ein Administrator Benutzer aus dem Teil des Dateisystems sperren, in dem die eigentlichen Dateien gespeichert sind. Benutzer können daher über den Ordner Eigene Dokumente an ihren eigenen Dokumenten arbeiten, aber nicht an Dokumenten, die anderen Benutzern gehören.

 

Es ist in der Regel nicht erforderlich, dass eine Anwendung weiß, welcher Benutzer angemeldet ist oder wo sich der ordner Eigene Dokumente des Benutzers im Dateisystem befindet. Stattdessen kann Ihre Anwendung die PIDL des Eigene Dokumente Desktopsymbols abrufen, indem sie die [**IShellFolder::P arseDisplayName-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) des Desktops aufruft. Der Analysename zum Identifizieren des Eigene Dokumente Ordners ist kein Dateipfad, sondern ::{450d8fba-ad25-11d0-98a8-0800361b1103}. Der Ausdruck in Klammern ist die Textform der Eigene Dokumente GUID. Um beispielsweise die PIDL von Eigene Dokumente abzurufen, sollte Ihre Anwendung diesen Aufruf von **IShellFolder::P arseDisplayName** verwenden.


```C++
hr = psfDeskTop->ParseDisplayName(NULL, 
                                  NULL, 
                                  L"::{450d8fba-ad25-11d0-98a8-0800361b1103}", 
                                  &chEaten, 
                                  &pidlDocFiles, 
                                  NULL);
```



Sobald Ihre Anwendung über die Eigene Dokumente PIDL verfügt, kann sie den Ordner genauso verarbeiten wie einen normalen Dateisystemordner– Aufzählen von Elementen, Analysieren, Binden und Ausführen anderer gültiger Ordnervorgänge. Die Shell ordnet Änderungen in Eigene Dokumente oder ihren Unterordnern automatisch den entsprechenden Dateisystemordnern zu.

Wenn Ihre Anwendung Zugriff auf den eigentlichen Dateisystemordner benötigt, der die Dokumente des aktuellen Benutzers enthält, übergeben Sie CSIDL \_ PERSONAL an [**SHGetFolderLocation.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) Die Funktion gibt die PIDL des Dateisystemordners zurück, der im ordner Eigene Dokumente des aktuellen Benutzers angezeigt wird.

## <a name="connected-files"></a>Verbundene Dateien

HTML-Dokumente verfügen häufig über eine Reihe von zugeordneten Grafikdateien, eine Stylesheetdatei, mehrere Microsoft JScript-Dateien (kompatibel mit ECMA 262-Sprachspezifikationen) usw. Wenn Sie das primäre HTML-Dokument verschieben oder kopieren, möchten Sie in der Regel auch die zugehörigen Dateien verschieben oder kopieren, um Breaking Links zu vermeiden. Leider gab es bisher keine einfache Möglichkeit, zu bestimmen, welche Dateien mit einem bestimmten HTML-Dokument verknüpft sind, außer durch Die Analyse ihrer Inhalte. Um dieses Problem zu beheben, bietet Windows 2000 eine einfache Möglichkeit, ein primäres HTML-Dokument mit der zugehörigen Dateigruppe zu *verbinden.* Wenn die Dateiverbindung aktiviert ist, werden beim Verschieben oder Kopieren des Dokuments alle verbundenen Dateien mit dem Dokument verknüpft.

Um eine Gruppe verbundener Dateien zu erstellen, muss das primäre Dokument über eine .htm oder .html Dateinamenerweiterung verfügen. Erstellen Sie einen Unterordner des übergeordneten Ordners des primären Dokuments. Der Name des Unterordners muss der Name des primären Dokuments sein, abzüglich der .htm oder .html Erweiterung, gefolgt von einer der unten aufgeführten Erweiterungen. Die am häufigsten verwendeten Erweiterungen sind ".files" oder \_ "files". Wenn das primäre Dokument beispielsweise MyDoc.htm genannt wird, definiert der Unterordner mit dem Namen "MyDoc-Dateien" \_ den Unterordner als Container für die verbundenen Dateien des Dokuments. Wenn das primäre Dokument verschoben oder kopiert wird, werden der Unterordner und seine Dateien ebenfalls verschoben oder kopiert.

Für einige Sprachen ist es möglich, eine lokalisierte Entsprechung von \_ "files" zu verwenden, um einen Unterordner für verbundene Dateien zu erstellen. In der folgenden Tabelle sind die gültigen Zeichenfolgen aufgeführt, die an einen Dokumentnamen angefügt werden können, um einen verbundenen Dateiunterordner zu erstellen. Beachten Sie, dass einige dieser Zeichenfolgen als erstes Zeichen "-" anstelle von \_ "" oder "." aufweisen.



:::row:::
   :::column span="":::
      \_"archivos"
   :::column-end:::
   :::column span="":::
      \_"arquivos"
   :::column-end:::
   :::column span="":::
      \_"bestanden"
   :::column-end:::
   :::column span="":::
      \_"bylos"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      "-Dateien"
   :::column-end:::
   :::column span="":::
      \_"datoteke"
   :::column-end:::
   :::column span="":::
      \_"dosyalar"
   :::column-end:::
   :::column span="":::
      \_"elemei"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      \_"failid"
   :::column-end:::
   :::column span="":::
      \_"fails" (Fehler)
   :::column-end:::
   :::column span="":::
      " \_ fajlovi"
   :::column-end:::
   :::column span="":::
      \_"fichafs"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      \_"fichiers"
   :::column-end:::
   :::column span="":::
      "-filer"
   :::column-end:::
   :::column span="":::
      ".files"
   :::column-end:::
   :::column span="":::
      \_"files"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      \_"file"
   :::column-end:::
   :::column span="":::
      \_"fitxers"
   :::column-end:::
   :::column span="":::
      \_"fitxatezweigk"
   :::column-end:::
   :::column span="":::
      \_"pliki"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      \_"soubory"
   :::column-end:::
   :::column span="":::
      " \_ tiedostot"
   :::column-end:::
   :::column span="":::
   :::column-end:::
   :::column span="":::
   :::column-end:::
:::row-end:::



 

> [!Note]  
> Bei diesem Feature wird die Groß-/Kleinschreibung der Erweiterung beachtet. Beispielsweise wird für das oben angegebene Beispiel ein Unterordner mit dem Namen "MyDoc \_ Files" nicht mit MyDoc.htm verbunden.

 

Ob die Dateiverbindung aktiviert oder deaktiviert ist, wird durch den **REG \_ DWORD-Wert** NoFileFolderConnection des folgenden Registrierungsschlüssels gesteuert.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
```

Dieser Wert ist normalerweise nicht definiert, und die Dateiverbindung ist aktiviert. Bei Bedarf können Sie die Dateiverbindung deaktivieren, indem Sie diesen Wert zum Schlüssel hinzufügen und auf 1 festlegen. Um die Dateiverbindung erneut zu aktivieren, legen Sie NoFileFolderConnection auf 0 (null) fest.

> [!Note]  
> Die Dateiverbindung sollte normalerweise aktiviert werden, da andere Anwendungen davon abhängig sein können. Deaktivieren Sie die Dateiverbindung nur, wenn dies unbedingt erforderlich ist.

 

## <a name="moving-copying-renaming-and-deleting-files"></a>Verschieben, Kopieren, Umbenennen und Löschen von Dateien

Der Namespace ist nicht statisch, und Anwendungen müssen das Dateisystem häufig verwalten, indem sie einen der folgenden Vorgänge ausführen.

-   Kopieren eines Objekts in einen anderen Ordner.
-   Verschieben eines Objekts in einen anderen Ordner.
-   Löschen eines Objekts.
-   Umbenennen eines Objekts.

Diese Vorgänge werden alle mit [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)ausgeführt. Diese Funktion verwendet eine oder mehrere Quelldateien und erzeugt entsprechende Zieldateien. Im Fall des Löschvorgangs versucht das System, die gelöschten Dateien in den Papierkorb zu speichern.

It is also possible to move files using the [drag-and-drop](dragdrop.md) functionality.

Um die Funktion zu verwenden, müssen Sie die Member einer [**SHFILEOPSTRUCT-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) ausfüllen und an [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)übergeben. Die Schlüsselmember der -Struktur sind **pFrom** und **pTo.**

Der **pFrom-Member** ist eine mit **doppelt NULL** endende Zeichenfolge, die einen oder mehrere Quelldateinamen enthält. Diese Namen können entweder vollqualifizierte Pfade oder STANDARD-DOS-Platzhalter wie \* \* sein. Obwohl dieser Member als null-terminierte Zeichenfolge deklariert ist, wird er als Puffer für mehrere Dateinamen verwendet. Jeder Dateiname muss durch das übliche einzelne **NULL-Zeichen** beendet werden. Ein zusätzliches **NULL-Zeichen** muss am Ende des endgültigen Namens angefügt werden, um das Ende von **pFrom** anzugeben.

Der **pTo-Member** ist eine doppelt **null-terminierte** Zeichenfolge, ähnlich wie **pFrom.** Der **pTo-Member** enthält die Namen von einem oder mehreren vollqualifizierten Zielnamen. Sie werden auf die gleiche Weise wie für **pFrom** in **pTo** gepackt. Wenn **pTo** mehrere Namen enthält, müssen Sie auch das **FOF \_ MULTIDESTFILES-Flag** im **fFlags-Member** festlegen. Die Verwendung von **pTo** hängt vom Vorgang ab, wie hier beschrieben.

-   Wenn alle Dateien für Kopier- und Verschiebevorgänge in ein einzelnes Verzeichnis verschoben werden, enthält **pTo** den vollqualifizierten Verzeichnisnamen. Wenn die Dateien an andere Ziele gelangen, kann **pTo** auch ein vollqualifiziertes Verzeichnis oder einen Dateinamen für jede Quelldatei enthalten. Wenn kein Verzeichnis vorhanden ist, erstellt das System es.
-   Für Umbenennungsvorgänge enthält **pTo** einen vollqualifizierten Pfad für jede Quelldatei in **pFrom.**
-   Für Löschvorgänge wird **pTo** nicht verwendet.

### <a name="notifying-the-shell"></a>Benachrichtigen der Shell

Benachrichtigen Sie die Shell über die Änderung, nachdem [**Sie SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) zum Verschieben, Kopieren, Umbenennen oder Löschen von Dateien verwendet oder eine andere Aktion ausgeführt haben, die sich auf den Namespace auswirkt. Aktionen, die von Benachrichtigungen begleitet werden sollten, umfassen Folgendes:

-   Hinzufügen oder Löschen von Dateien oder Ordnern.
-   Verschieben, Kopieren oder Umbenennen von Dateien oder Ordnern.
-   Ändern einer Dateizuordnung.
-   Ändern von Dateiattributen.
-   Hinzufügen oder Entfernen von Laufwerken oder Speichermedien.
-   Erstellen oder Deaktivieren eines freigegebenen Ordners.
-   Ändern der Systemimageliste.

Eine Anwendung benachrichtigt die Shell, indem [**sie SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) mit den Details der Änderungen aufruft. Die Shell kann dann ihr Image des Namespace aktualisieren, um den neuen Zustand genau widerzuspiegeln.

## <a name="simple-example-of-managing-files-with-shfileoperation"></a>Einfaches Beispiel für die Verwaltung von Dateien mit SHFileOperation

Die folgende Beispielkonsolenanwendung veranschaulicht die Verwendung von [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) zum Kopieren von Dateien aus einem Verzeichnis in ein anderes. Die Quell- und Zielverzeichnisse C: \\ My \_ Docs und C: \\ My Docs2 sind der Einfachheit \_ halber hart in die Anwendung codiert.


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>

int main(void)
{
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfDocFiles = NULL;
    LPITEMIDLIST pidlDocFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IEnumIDList *ppenum = NULL;
    SHFILEOPSTRUCT sfo;
    STRRET strDispName;
    TCHAR szParseName[MAX_PATH];
    TCHAR szSourceFiles[256];
    int i;
    int iBufPos = 0;
    ULONG chEaten;
    ULONG celtFetched;
    size_t ParseNameSize = 0;
    HRESULT hr;
    

    szSourceFiles[0] = '\0';
    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->ParseDisplayName(NULL, NULL, L"c:\\My_Docs", 
         &chEaten, &pidlDocFiles, NULL);
    hr = psfDeskTop->BindToObject(pidlDocFiles, NULL, IID_IShellFolder, 
         (LPVOID *) &psfDocFiles);
    hr = psfDeskTop->Release();

    hr = psfDocFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, 
         &ppenum);

    while( (hr = ppenum->Next(1,&pidlItems, &celtFetched)) == S_OK 
       && (celtFetched) == 1)
    {
        psfDocFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, 
            &strDispName);
        StrRetToBuf(&strDispName, pidlItems, szParseName, MAX_PATH);
        
        hr = StringCchLength(szParseName, MAX_PATH, &ParseNameSize);
        
        if (SUCCEEDED(hr))
        {
            for(i=0; i<=ParseNameSize; i++)
            {
                szSourceFiles[iBufPos++] = szParseName[i];
            }
            CoTaskMemFree(pidlItems);
        }
    }
    ppenum->Release();
    
    szSourceFiles[iBufPos] = '\0';

    sfo.hwnd = NULL;
    sfo.wFunc = FO_COPY;
    sfo.pFrom = szSourceFiles;
    sfo.pTo = "c:\\My_Docs2\0";
    sfo.fFlags = FOF_SILENT | FOF_NOCONFIRMATION | FOF_NOCONFIRMMKDIR;

    hr = SHFileOperation(&sfo);
    
    SHChangeNotify(SHCNE_UPDATEDIR, SHCNF_PATH, (LPCVOID) "c:\\My_Docs2", 0);

    CoTaskMemFree(pidlDocFiles);
    psfDocFiles->Release();

    return 0;
}
```



Die Anwendung ruft zunächst einen Zeiger auf die [**IShellFolder-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) des Desktops ab. Anschließend wird die PIDL des Quellverzeichnisses abgerufen, indem der vollqualifizierte Pfad an [**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)übergeben wird. Beachten Sie, dass **IShellFolder::P arseDisplayName** erfordert, dass der Pfad des Verzeichnisses eine Unicode-Zeichenfolge ist. Die Anwendung bindet dann an das Quellverzeichnis und verwendet die **IShellFolder-Schnittstelle,** um die [**IEnumIDList-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) eines Enumeratorobjekts abzurufen.

Da jede Datei im Quellverzeichnis aufzählt, wird [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) verwendet, um ihren Namen abzurufen. Das Flag SWSDN \_ FORPARSING ist festgelegt, wodurch **IShellFolder::GetDisplayNameOf** den vollqualifizierten Pfad der Datei zurückgibt. Die Dateipfade, einschließlich der abschließenden **NULL-Zeichen,** werden zu einem einzelnen Array verkettet, *szSourceFiles.* Ein zweites **NULL-Zeichen** wird an den endgültigen Pfad angefügt, um das Array ordnungsgemäß zu beenden.

Nach Abschluss der Enumeration weist die Anwendung einer [**SHFILEOPSTRUCT-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) Werte zu. Beachten Sie, dass das Array, das **pTo** zum Angeben des Ziels zugewiesen ist, ebenfalls mit einem doppelten **NULL-Wert** beendet werden muss. In diesem Fall ist sie einfach in der Zeichenfolge enthalten, die **pTo** zugewiesen ist. Da es sich um eine Konsolenanwendung handelt, werden die Flags FOF \_ SILENT, FOF \_ NOCONFIRMATION und FOF \_ NOCONFIRMMKDIR so festgelegt, dass alle angezeigten Dialogfelder unterdrückt werden. Nachdem [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) zurückgegeben wurde, wird [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) aufgerufen, um die Shell über die Änderung zu benachrichtigen. Anschließend führt die Anwendung die übliche Bereinigung aus und gibt zurück.

## <a name="adding-files-to-the-shells-list-of-recent-documents"></a>Hinzufügen von Dateien zur Shellliste zuletzt verwendeter Dokumente

Die Shell verwaltet eine Liste der zuletzt hinzugefügten oder geänderten Dokumente für jeden Benutzer. Der Benutzer kann eine Liste mit Links zu diesen Dateien anzeigen, indem er im Startmenü auf Dokumente klickt. Wie bei Eigene Dokumente verfügt jeder Benutzer über ein Dateisystemverzeichnis, in dem die tatsächlichen Links gespeichert werden können. Um die PIDL des Zuletzt verwendeten Verzeichnisses des aktuellen Benutzers abzurufen, kann Ihre Anwendung [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) mit CSIDL \_ RECENT aufrufen oder [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) aufrufen, um seinen Pfad abzurufen.

Ihre Anwendung kann den Inhalt des Ordners Zuletzt verwendet mithilfe der weiter oben in diesem Dokument beschriebenen Verfahren aufzählen. Eine Anwendung sollte den Inhalt des Ordners jedoch nicht so ändern, als wäre es ein normaler Dateisystemordner. In diesem Falle wird die Shell-Liste der letzten Dokumente nicht ordnungsgemäß aktualisiert, und die Änderungen werden nicht im Startmenü widergespiegelt. Um stattdessen einen Dokumentlink zum Ordner Zuletzt verwendet eines Benutzers hinzuzufügen, kann Ihre Anwendung [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)aufrufen. Die Shell fügt einen Link zum entsprechenden Dateisystemordner hinzu und aktualisiert die Liste der zuletzt verwendeten Dokumente und die Startmenü. Sie können diese Funktion auch verwenden, um den Ordner zu löschen.

 

 
