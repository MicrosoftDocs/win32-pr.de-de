---
description: Bevor Sie ein Namespace Objekt verwenden können, benötigen Sie eine Möglichkeit, es zu identifizieren.
ms.assetid: 54225481-a147-4d29-a642-24c9b59fc3ac
title: Die ID eines Ordners wird erhalten.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2e62454bf27f2c203f59aecb325cefe6537d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994734"
---
# <a name="getting-a-folders-id"></a>Die ID eines Ordners wird erhalten.

Bevor Sie ein Namespace Objekt verwenden können, benötigen Sie eine Möglichkeit, es zu identifizieren. Dies bedeutet, dass entweder der Zeiger auf eine Element Bezeichner Liste (PIDL) oder im Fall von Dateisystemobjekten der Pfad erhalten wird. In diesem Abschnitt werden zwei der einfacheren Methoden zum Abrufen von Objekt-IDs erläutert.

Verwenden Sie die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle für einen leistungsstärkeren Ansatz, der mit einem beliebigen Ordner funktioniert. Weitere [Informationen finden Sie unter Informationen zum Inhalt eines Ordners](folder-info.md) .

-   [Das Dialog Feld "openfiles"](#the-openfiles-dialog-box)
-   [Das Dialog Feld "shbrowsforfolder"](#the-shbrowseforfolder-dialog-box)
-   [Besondere Ordner und CSIDLs](#special-folders-and-csidls)
-   [Ein einfaches Beispiel für die Verwendung von CSIDLs und shbrowcforfolder](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a>Das Dialog Feld "openfiles"

Um dem Benutzer zu ermöglichen, im-Namespace zu navigieren und einen Ordner auszuwählen, kann die Anwendung die [**ifiledialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) -Schnittstelle verwenden. Wenn Sie diese Schnittstelle mit dem Flag " **Fos \_ pickfolders** " aufrufen, wird das Dialogfeld " [Dateien öffnen](../dlgbox/open-and-save-as-dialog-boxes.md) " im Modus "Pick Folders" geöffnet.

Für Windows Vista und höher ist dies die empfohlene Methode zum Auswählen von Ordnern.

## <a name="the-shbrowseforfolder-dialog-box"></a>Das Dialog Feld "shbrowsforfolder"

Um dem Benutzer zu ermöglichen, im-Namespace zu navigieren und einen Ordner auszuwählen, kann die Anwendung einfach [**shbrowseforfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera)aufrufen. Durch Aufrufen dieser Funktion wird ein Dialogfeld mit einer Benutzeroberfläche gestartet, das ähnlich wie die allgemeinen Dialogfelder [Öffnen oder SaveAs](../dlgbox/open-and-save-as-dialog-boxes.md) funktioniert.

Wenn der Benutzer einen Ordner auswählt, gibt [**shbrowsforfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) die voll qualifizierte PIDL und den anzeigen amen des Ordners zurück. Wenn sich der Ordner im Dateisystem befindet, kann die Anwendung die PIDL in einen Pfad konvertieren, indem Sie [**shgetpathfromittlerlist**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista)aufrufen. Die Anwendung kann auch den Bereich der Ordner einschränken, aus denen der Benutzer auswählen kann, indem er einen Stamm Ordner angibt. Nur Ordner, die sich unterhalb des Stamms im-Namespace befinden, werden angezeigt. Die folgende Abbildung zeigt das Dialogfeld **shbrowseforfolder** , wobei der Stamm Ordner auf Programme festgelegt ist.

![Screenshot des Dialog Felds "Ordner suchen"](images/shell1.png)

Ein einfaches Beispiel für die Verwendung von " [**shbrowsforfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) " wird später bereitgestellt.

## <a name="special-folders-and-csidls"></a>Besondere Ordner und CSIDLs

Eine Reihe häufig verwendeter Ordner werden vom System als *spezielle* Ordner bezeichnet. Diese Ordner haben einen klar definierten Zweck, und die meisten sind auf allen Systemen vorhanden. Auch wenn Sie nicht anfänglich vorhanden sind, werden Ihre Namen und Speicherorte weiterhin definiert, sodass Sie später hinzugefügt werden können. Die Sammlung spezieller Ordner umfasst alle standardmäßigen virtuellen Ordner des Systems, z. b. Drucker, eigene Dokumente und Netzwerkumgebung. Es enthält auch eine Reihe von standardmäßigen Dateisystem Ordnern, wie z. b. Programme und System.

Obwohl die Ordner eine Standardkomponente aller Systeme sind, können Ihre Namen und Speicherorte im-Namespace variieren. Beispielsweise ist das System Verzeichnis c: \\ Winnt \\ system32 auf einigen Systemen und C: \\ Windows \\ system32 auf anderen Systemen. In der Vergangenheit stellten Umgebungsvariablen den Namen und den Speicherort eines speziellen Ordners auf einem bestimmten System fest. Die Shell bietet nun eine robustere und flexiblere Möglichkeit, spezielle Ordner, [**CSIDLs**](csidl.md), zu identifizieren. Sie sollten Sie in der Regel anstelle von Umgebungsvariablen verwenden.

CSIDLs stellen eine einheitliche Möglichkeit dar, um spezielle Ordner unabhängig von Ihrem Namen oder Speicherort auf einem bestimmten System zu identifizieren und zu lokalisieren. Im Gegensatz zu Umgebungsvariablen können CSIDLs sowohl mit virtuellen Ordnern als auch mit Dateisystem Ordnern verwendet werden. Jedem speziellen Ordner ist eine eindeutige CSIDL zugewiesen. Beispielsweise verfügt der Ordner "Programme Dateisystem" über eine CSIDL von **CSIDL- \_ Programm \_ Dateien**, und der virtuelle Ordner der Netzwerkumgebung verfügt über eine CSIDL des **CSIDL- \_ Netzwerks**.

Eine CSIDL wird in Verbindung mit einer von mehreren Shellfunktionen verwendet, um die PIDL eines speziellen Ordners oder den Pfad eines speziellen Dateisystem Ordners abzurufen. Wenn der Ordner auf einem System nicht vorhanden ist, kann die Anwendung erzwingen, dass er erstellt wird, indem er die CSIDL mit dem **CSIDL- \_ Flag \_ Create** kombiniert. Die CSIDL kann an die folgenden Funktionen übergeben werden:

-   [**Shgetfolderlocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation): Ruft die PIDL eines speziellen Ordners ab.
-   [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha): Ruft den Pfad eines speziellen Dateisystem Ordners ab.

Beachten Sie, dass diese beiden Funktionen mit Version 5,0 der Shell eingeführt wurden und die Funktionen " [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) " und " [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) " ersetzen.

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a>Ein einfaches Beispiel für die Verwendung von CSIDLs und shbrowcforfolder

Die folgende Beispiel Funktion, pidlbrowse, veranschaulicht die Verwendung von CSIDLs zum Abrufen der PIDL eines Ordners und das Verwenden von [**shbrowsforfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) , um den Benutzer zum Auswählen eines Ordners zu verwenden. Er gibt die PIDL und den anzeigen amen des ausgewählten Ordners zurück.


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



Die aufrufenden Anwendung übergibt ein Fenster Handle, das von [**shbrowseforfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera)benötigt wird. Der *ncsidl* -Parameter ist eine optionale CSIDL, die verwendet wird, um einen Stamm Ordner anzugeben. Es werden nur Ordner unter dem Stamm Ordner in der Hierarchie angezeigt. Die zuvor gezeigte Abbildung wurde durch Aufrufen dieser Funktion generiert, wobei *ncsidl* auf **CSIDL- \_ Programm \_ Dateien** festgelegt wurde. Die aufrufenden Anwendung übergibt auch den Zeichen folgen Puffer *pszDisplayName*, um den anzeigen amen des ausgewählten Ordners zu speichern, wenn pidlbrowse zurückgibt. Es liegt in der Verantwortung der aufrufenden Anwendung, die von **shbrowseforfolder** zurückgegebene idlist mithilfe von " [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)" freizugeben.

 

 
