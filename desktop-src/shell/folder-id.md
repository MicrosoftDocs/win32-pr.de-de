---
description: Bevor Sie ein Namespaceobjekt verwenden können, benötigen Sie eine Möglichkeit, es zu identifizieren.
ms.assetid: 54225481-a147-4d29-a642-24c9b59fc3ac
title: Abrufen der ID eines Ordners
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d75051d52f0dfcee54b6365a8f546d2cbda2c3b5f7c0f4b6fbbc19fa1e40c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459009"
---
# <a name="getting-a-folders-id"></a>Abrufen der ID eines Ordners

Bevor Sie ein Namespaceobjekt verwenden können, benötigen Sie eine Möglichkeit, es zu identifizieren. Dies bedeutet, entweder den Zeiger auf eine Elementbezeichnerliste (PIDL) oder im Fall von Dateisystemobjekten den Pfad zu erhalten. In diesem Abschnitt werden zwei der einfacheren Methoden zum Abrufen von Objekt-IDs erläutert.

Verwenden Sie die [**IShellFolder-Schnittstelle,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) um einen leistungsfähigeren Ansatz zu erhalten, der mit jedem Ordner funktioniert. Weitere Informationen finden Sie unter [Abrufen von Informationen zum Inhalt](folder-info.md) eines Ordners.

-   [Dialogfeld "OpenFiles"](#the-openfiles-dialog-box)
-   [ShBrowseForFolder (Dialogfeld)](#the-shbrowseforfolder-dialog-box)
-   [Spezielle Ordner und CSIDLs](#special-folders-and-csidls)
-   [Ein einfaches Beispiel für die Verwendung von CSIDLs und SHBrowseForFolder](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a>Dialogfeld "OpenFiles"

Damit der Benutzer durch den Namespace navigieren und einen Ordner auswählen kann, kann Ihre Anwendung die [**IFileDialog-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) verwenden. Wenn Sie diese Schnittstelle mit **dem FOS \_ PICKFOLDERS-Flag** aufrufen, wird das allgemeine Dialogfeld Dateien öffnen im Modus "Ordner auswählen" gestartet. [](../dlgbox/open-and-save-as-dialog-boxes.md)

Für Windows Vista und höher ist dies die empfohlene Methode zum Auswählen von Ordnern.

## <a name="the-shbrowseforfolder-dialog-box"></a>ShBrowseForFolder (Dialogfeld)

Damit der Benutzer durch den Namespace navigieren und einen Ordner auswählen kann, kann Ihre Anwendung [**einfach SHBrowseForFolder aufrufen.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) Durch Aufrufen dieser Funktion wird ein Dialogfeld mit einer Benutzeroberfläche gestartet, die in etwa wie die allgemeinen Dialogfelder Öffnen oder [Speichern Funktioniert.](../dlgbox/open-and-save-as-dialog-boxes.md)

Wenn der Benutzer einen Ordner auswählt, [**gibt SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) die vollqualifizierte PIDL und den Anzeigenamen des Ordners zurück. Wenn sich der Ordner im Dateisystem befindet, kann die Anwendung die PIDL durch Aufrufen von [**SHGetPathFromIDList in einen Pfad konvertieren.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista) Die Anwendung kann auch den Bereich von Ordnern einschränken, aus denen der Benutzer auswählen kann, indem ein Stammordner angegeben wird. Es werden nur Ordner angezeigt, die sich unterhalb dieses Stamms im Namespace befinden. Die folgende Abbildung zeigt das **Dialogfeld SHBrowseForFolder,** bei dem der Stammordner auf Programme festgelegt ist.

![Screenshot des Dialogfelds "Ordner suchen"](images/shell1.png)

Ein einfaches Beispiel für die Verwendung von [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) wird später bereitgestellt.

## <a name="special-folders-and-csidls"></a>Spezielle Ordner und CSIDLs

Eine Reihe häufig verwendeter Ordner wird vom *System* als speziell festgelegt. Diese Ordner haben einen klar definierten Zweck, und die meisten davon sind auf allen Systemen vorhanden. Auch wenn sie anfänglich nicht vorhanden sind, sind ihre Namen und Speicherorte weiterhin definiert, sodass sie später hinzugefügt werden können. Die Sammlung spezieller Ordner umfasst alle standardmäßigen virtuellen Ordner des Systems, z. B. Drucker, Eigene Dokumente und Netzwerkumgebung. Es enthält auch eine Reihe von Standarddateisystemordnern, z. B. Programme und System.

Obwohl die Ordner eine Standardkomponente aller Systeme sind, können ihre Namen und Speicherorte im Namespace variieren. Das Verzeichnis System ist beispielsweise C: \\ Winnt System32 auf einigen Systemen \\ und C: \\ Windows \\ System32 auf anderen. In der Vergangenheit boten Umgebungsvariablen eine Möglichkeit, den Namen und Speicherort eines speziellen Ordners auf einem bestimmten System zu bestimmen. Die Shell bietet jetzt eine stabilere und flexiblere Möglichkeit zum Identifizieren von speziellen Ordnern, [**CSIDLs.**](csidl.md) Sie sollten sie im Allgemeinen anstelle von Umgebungsvariablen verwenden.

CSIDLs bieten eine einheitliche Möglichkeit zum Identifizieren und Suchen von speziellen Ordnern, unabhängig von ihrem Namen oder Speicherort in einem bestimmten System. Im Gegensatz zu Umgebungsvariablen können CSIDLs mit virtuellen Ordnern sowie Dateisystemordnern verwendet werden. Jedem speziellen Ordner ist eine eindeutige CSIDL zugewiesen. Der Dateisystemordner Programme verfügt beispielsweise über eine CSIDL von **CSIDL \_ PROGRAM \_ FILES,** und der virtuelle Ordner Network Neighborhood hat die CSIDL **CSIDL \_ NETWORK.**

Eine CSIDL wird in Verbindung mit einer von mehreren Shellfunktionen verwendet, um die PIDL eines speziellen Ordners oder den Pfad eines speziellen Dateisystemordners abzurufen. Wenn der Ordner auf einem System nicht vorhanden ist, kann Ihre Anwendung erzwingen, dass er erstellt wird, indem seine CSIDL mit **CSIDL \_ FLAG CREATE kombiniert \_ wird.** Die CSIDL kann an die folgenden Funktionen übergeben werden:

-   [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation): Ruft die PIDL eines speziellen Ordners ab.
-   [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha): Ruft den Pfad eines speziellen Dateisystemordners ab.

Beachten Sie, dass diese beiden Funktionen mit Version 5.0 der Shell eingeführt wurden und die [**ShGetSpecialFolderLocation-**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) und [**SHGetSpecialFolderPath-Funktionen**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) ab ersetzt haben.

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a>Ein einfaches Beispiel für die Verwendung von CSIDLs und SHBrowseForFolder

Die folgende Beispielfunktion, PidlBrowse, veranschaulicht die Verwendung von CSIDLs zum Abrufen der PIDL eines Ordners und die Verwendung [**von SHBrowseForFolder,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) damit der Benutzer einen Ordner auswählt. Sie gibt die PIDL und den Anzeigenamen des ausgewählten Ordners zurück.


```
LPITEMIDLIST PidlBrowse(HWND hwnd, int nCSIDL, LPSTR pszDisplayName)
{
    LPITEMIDLIST pidlRoot = NULL;
    LPITEMIDLIST pidlSelected = NULL;
    BROWSEINFO bi = {0};

    if(nCSIDL)
    {
        SHGetFolderLocation(hwnd, nCSIDL, NULL, NULL, &pidlRoot);
    }

    else
    {
        pidlRoot = NULL;
    }

    bi.hwndOwner = hwnd;
    bi.pidlRoot = pidlRoot;
    bi.pszDisplayName = pszDisplayName;
    bi.lpszTitle = "Choose a folder";
    bi.ulFlags = 0;
    bi.lpfn = NULL;
    bi.lParam = 0;

    pidlSelected = SHBrowseForFolder(&bi);

    if(pidlRoot)
    {
        CoTaskMemFree(pidlRoot);
    }

    return pidlSelected;
}
```



Die aufrufende Anwendung übergibt ein Fensterhand handle, das von [**SHBrowseForFolder benötigt wird.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) Der *nCSIDL-Parameter* ist eine optionale CSIDL, die zum Angeben eines Stammordners verwendet wird. Nur Ordner unterhalb des Stammordners in der Hierarchie werden angezeigt. Die zuvor gezeigte Abbildung wurde durch Aufrufen dieser Funktion generiert, bei der *nCSIDL* auf **CSIDL \_ PROGRAM FILES festgelegt \_ ist.** Die aufrufende Anwendung übergibt außerdem den Zeichenfolgenpuffer *pszDisplayName,* um den Anzeigenamen des ausgewählten Ordners zu speichern, wenn PidlBrowse zurückgegeben wird. Es liegt in der Verantwortung der aufrufenden Anwendung, die von **SHBrowseForFolder** zurückgegebene IDList mithilfe von [**CoTaskMemFree freizu geben.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)

 

 
