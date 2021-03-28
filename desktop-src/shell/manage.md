---
description: Die Shell bietet eine Reihe von Methoden zum Verwalten von Dateisystemen.
ms.assetid: d9ffda6f-adc0-44a3-b410-e23bf5f4f165
title: Verwalten des Dateisystems
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404b456ce1f26c128e6c3fc3bc9971672378a0d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342429"
---
# <a name="managing-the-file-system"></a>Verwalten des Dateisystems

Die Shell bietet eine Reihe von Methoden zum Verwalten von Dateisystemen. Die Shell stellt eine Funktion, " [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)", bereit, die es einer Anwendung ermöglicht, Dateien Programm gesteuert zu verschieben, zu kopieren, umzubenennen und zu löschen. Die Shell unterstützt auch einige zusätzliche Dateiverwaltungsfunktionen.

-   HTML-Dokumente können mit verwandten Dateien, z. b. Grafikdateien oder Stylesheets, *verbunden* werden. Wenn das Dokument verschoben oder kopiert wird, werden die verbundenen Dateien auch automatisch verschoben oder kopiert.
-   Für Systeme, die für mehr als einen Benutzer verfügbar sind, können Dateien pro Benutzer verwaltet werden. Benutzer haben einfachen Zugriff auf Ihre Datendateien, jedoch nicht auf Dateien, die anderen Benutzern angehören.
-   Wenn Dokument Dateien hinzugefügt oder geändert werden, können Sie der Liste der zuletzt geöffneten Dokumente der Shell hinzugefügt werden. Wenn der Benutzer im Startmenü auf den Befehl **Dokumente** klickt, wird eine Liste mit Links zu den Dokumenten angezeigt.

In diesem Dokument wird erläutert, wie diese Technologien zur Dateiverwaltung funktionieren. Anschließend wird erläutert, wie die Shell zum Verschieben, kopieren, umbenennen und Löschen von Dateien und zum Verwalten von Objekten im Papierkorb verwendet werden kann.

-   [Dateiverwaltung pro Benutzer](#per-user-file-management)
-   [Ordner "eigene Dokumente" und "eigene Bilder"](#my-documents-and-my-pictures-folders)
-   [Verbundene Dateien](#connected-files)
-   [Verschieben, kopieren, umbenennen und Löschen von Dateien](#moving-copying-renaming-and-deleting-files)
    -   [Benachrichtigen der Shell](#notifying-the-shell)
-   [Einfaches Beispiel für die Verwaltung von Dateien mit SHFileOperation](#simple-example-of-managing-files-with-shfileoperation)
-   [Hinzufügen von Dateien zur Liste der zuletzt geöffneten Dokumente in der Shell](#adding-files-to-the-shells-list-of-recent-documents)

## <a name="per-user-file-management"></a>Per-User Dateiverwaltung

Mit der Windows 2000-Shell können Dateien einem bestimmten Benutzer zugeordnet werden, damit die Dateien von anderen Benutzern ausgeblendet werden. Im Hinblick auf das Dateisystem werden die Dateien im Profilordner des Benutzers gespeichert, in der Regel C: \\ Dokumente und Einstellungen \\ *username* \\ auf Windows 2000-Systemen. Diese Funktion ermöglicht es vielen Personen, denselben Computer zu verwenden, während der Datenschutz Ihrer Dateien von anderen Benutzern gewahrt bleibt. Verschiedene Benutzer können unterschiedliche Programme zur Verfügung stellen. Sie bietet außerdem eine einfache Möglichkeit für Administratoren und Anwendungen, wie z. b. Initialisierungsdateien (INI) oder Verknüpfungs Dateien (LNK-Dateien) zu speichern. Anwendungen können auf diese Weise für jeden Benutzer einen anderen Zustand beibehalten und den jeweiligen Zustand bei Bedarf problemlos wiederherstellen. Es gibt auch einen Profilordner zum Speichern von Informationen, die allen Benutzern gemeinsam sind.

Da es nicht möglich ist, zu bestimmen, welcher Benutzer angemeldet ist und wo sich die Dateien befinden, sind die standardmäßigen benutzerspezifischen Ordner spezielle Ordner und werden durch eine [**CSIDL**](csidl.md)identifiziert. Beispielsweise handelt es sich bei der CSIDL für den Ordner für benutzerspezifische Programmdateien um CSIDL- \_ Programme. Wenn Ihre Anwendung " [**shgetfolderlocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) " oder " [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) " mit einer der benutzerspezifischen CSIDLs aufruft, gibt die Funktion den Zeiger auf eine Element Bezeichner Liste (PIDL) oder einen Pfad zurück, der dem aktuell angemeldeten Benutzer entspricht. Wenn die Anwendung den Pfad oder die PIDL des Profilordners abrufen muss, ist die zugehörige CSIDL **CSIDL- \_ Profil**.

## <a name="my-documents-and-my-pictures-folders"></a>Ordner "eigene Dokumente" und "eigene Bilder"

Eines der Standardsymbole, die auf dem Desktop gefunden werden, sind **meine Dokumente**. Wenn Sie diesen Ordner öffnen, enthält er die Dokument Dateien des aktuellen Benutzers. Die Desktop Instanz von "eigene Dokumente" ist ein virtueller Ordner – ein Alias zum Speicherort des Dateisystems, in dem die Dokumente des Benutzers physisch gespeichert werden –, der sich direkt unterhalb des Desktops in der Namespace Hierarchie befindet.

Der Zweck der Ordner "eigene Dokumente" und "eigene Bilder" besteht darin, Benutzern eine einfache und sichere Möglichkeit zur Verfügung zu stellen, um den Benutzern den Zugriff auf Ihre Dokument-und Bilddateien auf einem System mit mehreren Benutzern zu ermöglichen Jedem Benutzer werden separate Dateisystem Ordner für seine Dateien zugewiesen. Beispielsweise ist der Speicherort des Ordners "Dokumente" eines Benutzers im Dateisystem in der Regel etwa "C: \\ Dokumente und Einstellungen \\ *username* \\ My Documents". Es ist nicht erforderlich, dass Benutzer etwas über den physischen Speicherort Ihrer Dateisystem Ordner wissen. Der Zugriff auf die Dateien erfolgt einfach über das Symbol "eigene Dokumente".

> [!Note]  
> Meine Dokumente ermöglicht einem Benutzer den Zugriff auf seine eigenen Dateien, jedoch nicht auf die eines anderen Benutzers. Wenn mehrere Benutzer denselben Computer verwenden, kann ein Administrator Benutzer aus dem Teil des Dateisystems, in dem die Dateien gespeichert werden, sperren. Benutzer können daher mit ihren eigenen Dokumenten über den Ordner "eigene Dateien", aber nicht über Dokumente, die anderen Benutzern angehören, arbeiten.

 

Es ist in der Regel nicht erforderlich, dass eine Anwendung weiß, welcher Benutzer angemeldet ist oder wo sich der Ordner "eigene Dateien" des Benutzers befindet. Stattdessen kann die Anwendung die PIDL des Desktop Symbols "My Documents" abrufen, indem die [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) -Methode des Desktops aufgerufen wird. Der zum Identifizieren des Ordners "eigene Dokumente" verwendete namens Name ist kein Dateipfad, sondern: {450d8fba-ad25-11D0-98a8-0800361b1103}. Der Ausdruck in Klammern ist die Textform der GUID "eigene Dokumente". Zum Abrufen der PIDL von "eigene Dokumente" sollte Ihre Anwendung z. b. diesen **IShellFolder::P arsedisplayname** verwenden.


```C++
hr = psfDeskTop->ParseDisplayName(NULL, 
                                  NULL, 
                                  L"::{450d8fba-ad25-11d0-98a8-0800361b1103}", 
                                  &chEaten, 
                                  &pidlDocFiles, 
                                  NULL);
```



Sobald Ihre Anwendung über die PIDL "eigene Dateien" verfügt, kann Sie den Ordner genauso behandeln wie einen normalen Dateisystem Ordner – das Aufzählen von Elementen, das Durchführen von Bindungen und das Ausführen beliebiger gültiger Ordner Vorgänge. Die Shell ordnet Änderungen in "eigene Dokumente" oder Unterordner den entsprechenden Dateisystem Ordnern automatisch zu.

Wenn Ihre Anwendung Zugriff auf den eigentlichen Dateisystem Ordner benötigt, der die Dokumente des aktuellen Benutzers enthält, übergeben Sie CSIDL \_ persönlich an [**shgetfolderlocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation). Die-Funktion gibt die PIDL des Dateisystem Ordners zurück, der im Ordner "eigene Dateien" des aktuellen Benutzers angezeigt wird.

## <a name="connected-files"></a>Verbundene Dateien

HTML-Dokumente verfügen häufig über eine Reihe von zugeordneten Grafikdateien, eine Stylesheet-Datei, mehrere Microsoft JScript-Dateien (kompatibel mit ECMA 262-Sprachspezifikation) usw. Wenn Sie das primäre HTML-Dokument verschieben oder kopieren, sollten Sie auch die zugehörigen Dateien verschieben oder kopieren, um Unterbrechungen zu vermeiden. Leider gab es bisher keine einfache Methode, um zu ermitteln, welche Dateien mit einem anderen HTML-Dokument verknüpft sind, außer durch die Analyse ihrer Inhalte. Um dieses Problem zu beheben, bietet Windows 2000 eine einfache Möglichkeit, ein primäres HTML-Dokument mit der zugehörigen Gruppe zugeordneter Dateien zu *verbinden* . Wenn die Dateiverbindung aktiviert ist und das Dokument verschoben oder kopiert wird, werden alle zugehörigen Dateien mit dem Dokument verknüpft.

Um eine Gruppe verbundener Dateien zu erstellen, muss das primäre Dokument die Dateinamenerweiterung ". htm" oder ". html" aufweisen. Erstellen Sie einen Unterordner des übergeordneten Ordners des primären Dokuments. Der Name des unter Ordners muss der Name des primären Dokuments sein, abzüglich der Erweiterung. htm oder. html, gefolgt von einer der unten aufgeführten Erweiterungen. Die am häufigsten verwendeten Erweiterungen sind ". Files" oder " \_ Files". Wenn das primäre Dokument beispielsweise MyDoc.htm benannt ist, wird durch Benennen des unter Ordners "MyDoc \_ Files" der Unterordner als Container für die verbundenen Dateien des Dokuments definiert. Wenn das primäre Dokument verschoben oder kopiert wird, werden auch der Unterordner und die zugehörigen Dateien verschoben oder kopiert.

Für einige Sprachen ist es möglich, eine lokalisierte Entsprechung von " \_ Files" zu verwenden, um einen Unterordner für verbundene Dateien zu erstellen. In der folgenden Tabelle werden die gültigen Zeichen folgen aufgelistet, die an einen Dokumentnamen angehängt werden können, um einen Unterordner mit verbundenen Dateien zu erstellen. Beachten Sie, dass einige dieser Zeichen folgen "-" als erstes Zeichen anstelle von " \_ " oder "." aufweisen.



|              |               |                 |               |
|--------------|---------------|-----------------|---------------|
| " \_ archivos" | " \_ Architekt"  | " \_ bestanden"   | " \_ bylos"     |
| "----Dateien"   | " \_ datoteke"  | " \_ dosyalar"    | " \_ elemei"    |
| " \_ failid"   | " \_ schlägt fehl"     | " \_ fajlovi"     | " \_ fcheiros" |
| " \_ Filter" | "-Filer"      | ". Files"        | " \_ Dateien"     |
| " \_ file"     | " \_ fitxzer"   | " \_ fitxategiak" | " \_ Pliki"     |
| " \_ soubory"  | " \_ tiedostot" |                 |               |



 

> [!Note]  
> Diese Funktion ist für den Fall der Erweiterung sensibel. Beispielsweise wird für das oben genannte Beispiel ein Unterordner mit dem Namen "MyDoc \_ Files" nicht mit MyDoc.htm verbunden.

 

Ob die Dateiverbindung aktiviert oder deaktiviert ist, wird von einem **reg \_ DWORD** -Wert (nofilefolderconnection) des folgenden Registrierungsschlüssels gesteuert.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
```

Dieser Wert ist normalerweise nicht definiert, und die Dateiverbindung ist aktiviert. Falls erforderlich, können Sie die Dateiverbindung deaktivieren, indem Sie diesen Wert dem Schlüssel hinzufügen und ihn auf 1 festlegen. Legen Sie nofilefolderconnection auf NULL fest, um die Dateiverbindung erneut zu aktivieren.

> [!Note]  
> Die Dateiverbindung sollte normalerweise aktiviert sein, da andere Anwendungen von ihr abhängig sein können. Deaktivieren Sie die Dateiverbindung nur, wenn dies unbedingt erforderlich ist

 

## <a name="moving-copying-renaming-and-deleting-files"></a>Verschieben, kopieren, umbenennen und Löschen von Dateien

Der Namespace ist nicht statisch, und Anwendungen müssen im Allgemeinen das Dateisystem verwalten, indem Sie einen der folgenden Vorgänge ausführen.

-   Kopieren eines Objekts in einen anderen Ordner.
-   Verschieben eines Objekts in einen anderen Ordner.
-   Löschen eines Objekts.
-   Umbenennen eines Objekts.

Diese Vorgänge werden alle mit [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)ausgeführt. Diese Funktion nimmt eine oder mehrere Quelldateien an und erzeugt entsprechende Zieldateien. Im Fall des Löschvorgangs versucht das System, die gelöschten Dateien in den Papierkorb einzufügen.

Es ist auch möglich, Dateien mithilfe der [Drag & Drop](dragdrop.md) -Funktionalität zu verschieben.

Um die-Funktion zu verwenden, müssen Sie die Member einer [**shfileopstruct**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) -Struktur ausfüllen und an " [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)" übergeben. Die Schlüsselmember der Struktur sind **pfrom** und **PTO**.

Der **pfrom** -Member ist eine Zeichenfolge mit doppelten **null**-terminierten Zeichenfolge, die mindestens einen Quell Dateinamen enthält. Bei diesen Namen kann es sich entweder um voll qualifizierte Pfade oder um standardmäßige DOS-Platzhalter wie \* . \* handeln. Obwohl dieser Member als eine **null**-terminierte Zeichenfolge deklariert ist, wird er als Puffer verwendet, um mehrere Dateinamen aufzunehmen. Jeder Dateiname muss mit dem üblichen einzelnen **null** -Zeichen beendet werden. Ein zusätzliches **null** -Zeichen muss an das Ende des endgültigen namens angehängt werden, um das Ende von **pfrom** anzugeben.

Der **PTO** -Member ist eine Zeichenfolge mit doppelten **null**-terminierten Zeichen folgen, ähnlich wie **pfrom**. Der **PTO** -Member enthält die Namen eines oder mehrerer voll qualifizierter Zielnamen. Sie werden auf die gleiche Weise wie für **pfrom** in **PTO** gepackt. Wenn **PTO** mehrere Namen enthält, müssen Sie auch das **FOF \_ multidestfiles** -Flag im **fFlags** -Member festlegen. Die Verwendung von **PTO** hängt von dem Vorgang ab, wie hier beschrieben.

-   Wenn bei Kopier-und Verschiebungs Vorgängen alle Dateien in ein einzelnes Verzeichnis gelangen, enthält **PTO** den voll qualifizierten Verzeichnisnamen. Wenn die Dateien an verschiedene Ziele übergeben werden, kann **PTO** auch einen voll qualifizierten Verzeichnis-oder Dateinamen für jede Quelldatei enthalten. Wenn ein Verzeichnis nicht vorhanden ist, wird es vom System erstellt.
-   Für Umbenennungs Vorgänge enthält **PTO** einen voll qualifizierten Pfad für jede Quelldatei in **pfrom**.
-   Für Löschvorgänge wird **PTO** nicht verwendet.

### <a name="notifying-the-shell"></a>Benachrichtigen der Shell

Benachrichtigen Sie die Shell über die Änderung, nachdem Sie mithilfe von [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) Dateien verschoben, kopiert, umbenannt oder gelöscht haben, oder nachdem Sie eine andere Aktion ausgeführt haben, die sich auf den-Namespace auswirkt. Zu den Aktionen, die von der Benachrichtigung begleitet werden sollten, gehören die folgenden:

-   Hinzufügen oder Löschen von Dateien oder Ordnern.
-   Verschieben, kopieren oder Umbenennen von Dateien oder Ordnern.
-   Ändern einer Datei Zuordnung.
-   Ändern von Dateiattributen.
-   Hinzufügen oder Entfernen von Laufwerken oder Speichermedien.
-   Erstellen oder Deaktivieren eines freigegebenen Ordners.
-   Die System Abbild Liste wird geändert.

Eine Anwendung benachrichtigt die Shell durch Aufrufen von [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) mit den Details zu geänderten Änderungen. Die Shell kann dann das Image des Namespaces aktualisieren, um den neuen Zustand exakt widerzuspiegeln.

## <a name="simple-example-of-managing-files-with-shfileoperation"></a>Einfaches Beispiel für die Verwaltung von Dateien mit SHFileOperation

Die folgende Beispiel Konsolenanwendung veranschaulicht die Verwendung von [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) zum Kopieren von Dateien aus einem Verzeichnis in ein anderes Verzeichnis. Die Quell-und Zielverzeichnisse "c: \\ My \_ docs" und "c: \\ My Docs2" \_ sind aus Gründen der Einfachheit in der Anwendung hart codiert.


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



Die Anwendung ruft zuerst einen Zeiger auf die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle des Desktops ab. Anschließend ruft er die PIDL des Quell Verzeichnisses ab, indem er den voll qualifizierten Pfad an [**IShellFolder::P ar\displayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)übergibt. Beachten Sie, dass **IShellFolder::P ARL Display Name** erfordert, dass der Pfad des Verzeichnisses eine Unicode-Zeichenfolge ist. Die Anwendung bindet dann an das Quellverzeichnis und verwendet die **IShellFolder** -Schnittstelle zum Abrufen der [**ienumittellist**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) -Schnittstelle eines Enumeratorobjekts.

Bei der Enumeration der einzelnen Dateien im Quellverzeichnis wird [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) zum Abrufen des Namens verwendet. Das Flag "shgdn \_ forparamesing" ist festgelegt, was bewirkt, dass **IShellFolder:: GetDisplayNameOf** den voll qualifizierten Pfad der Datei zurückgibt. Die Dateipfade, einschließlich der abschließenden **null** -Zeichen, werden in einem einzelnen Array, *szsourcefiles*, verkettet. Ein zweites **null** -Zeichen wird an den endgültigen Pfad angehängt, um das Array ordnungsgemäß zu beenden.

Nachdem die Enumeration fertiggestellt wurde, weist die Anwendung Werte einer [**shfi**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) -Struktur Struktur zu. Beachten Sie, dass das Array, das **PTO** zugewiesen ist, um das Ziel anzugeben, auch durch einen doppelten **null**-Wert beendet werden muss. In diesem Fall ist Sie einfach in der Zeichenfolge enthalten, die **PTO** zugewiesen wird. Da es sich hierbei um eine Konsolenanwendung handelt, werden die Flags "FOF \_ Silent", "FOF \_ noconfirmation" und "FOF \_ noconfirmmkdir" so festgelegt, dass alle angezeigten Dialogfelder unterdrückt werden. Nachdem [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) zurückgegeben wurde, wird [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) aufgerufen, um die Shell über die Änderung zu benachrichtigen. Die Anwendung führt dann die übliche Bereinigung durch und gibt zurück.

## <a name="adding-files-to-the-shells-list-of-recent-documents"></a>Hinzufügen von Dateien zur Liste der zuletzt geöffneten Dokumente in der Shell

Die Shell verwaltet eine Liste der zuletzt hinzugefügten oder geänderten Dokumente für jeden Benutzer. Der Benutzer kann eine Liste mit Links zu diesen Dateien anzeigen, indem er im Startmenü auf Dokumente klickt. Wie bei meinen Dokumenten verfügt jeder Benutzer über ein Dateisystem Verzeichnis, um die tatsächlichen Verknüpfungen zu speichern. Zum Abrufen der PIDL des aktuellen Verzeichnisses des aktuellen Benutzers kann die Anwendung " [**shgetfolderlocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) " mit der aktuellen CSIDL-Datei aufrufen \_ oder " [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) " aufrufen, um den Pfad abzurufen.

Die Anwendung kann den Inhalt des aktuellen Ordners mithilfe der zuvor in diesem Dokument beschriebenen Techniken auflisten. Eine Anwendung sollte den Inhalt des Ordners jedoch nicht so ändern, als ob es sich um einen normalen Dateisystem Ordner handelt. Wenn dies der Fall ist, wird die Liste der zuletzt geöffneten Dokumente der Shell nicht ordnungsgemäß aktualisiert, und die Änderungen werden im Startmenü nicht angezeigt. Stattdessen kann die Anwendung " [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)" aufgerufen werden, um einen Dokument Link zum aktuellen Ordner eines Benutzers hinzuzufügen. Die Shell fügt dem entsprechenden Dateisystem Ordner einen Link hinzu und aktualisiert die Liste der zuletzt geöffneten Dokumente und das Startmenü. Sie können diese Funktion auch verwenden, um den Ordner zu löschen.

 

 
