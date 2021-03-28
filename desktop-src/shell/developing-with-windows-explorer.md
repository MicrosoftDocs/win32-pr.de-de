---
description: Windows-Explorer ist eine leistungsstarke Anwendung zum Durchsuchen und Verwalten von Ressourcen.
ms.assetid: 879CE652-EDC0-4a14-925E-C83763133BE5
title: Entwickeln mit Windows-Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7b68d48f2d1becea23311847a5ce41b3776321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484387"
---
# <a name="developing-with-windows-explorer"></a>Entwickeln mit Windows-Explorer

Windows-Explorer ist eine leistungsstarke Anwendung zum Durchsuchen und Verwalten von Ressourcen. Der Zugriff auf den Windows-Explorer ist als integriertes Ganzes über Explorer.exe oder die [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) -Schnittstelle möglich. Windows Explorer (Explorer.exe) kann mit [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) oder einer ähnlichen Funktion als separater Prozess erzeugt werden.

> [!Note]  
> Die Befehlszeilenoptionen für Explorer.exe werden auf der Microsoft Windows-Support-Website im Artikel [Windows-Explorer-Command-Line Optionen](https://support.microsoft.com/kb/152457)dokumentiert.

 

Geöffnete Explorer-Fenster können mithilfe von [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID shellwindows) ermittelt und programmiert werden \_ , und neue Instanzen von Windows-Explorer können mithilfe von [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID \_ shellbrowserwindow) erstellt werden.

Im folgenden Codebeispiel wird veranschaulicht, wie das Windows-Explorer-Automatisierungs Modell zum Erstellen und ermitteln von Explorer-Fenstern verwendet werden kann, die ausgeführt werden.


```
#define _WIN32_WINNT 0x0600
#define _WIN32_IE 0x0700
#define _UNICODE

#include <windows.h>
#include <shobjidl.h>
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>
#include <propvarutil.h>
 
#pragma comment(lib, "shlwapi.lib")
#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "shell32.lib")
#pragma comment(lib, "propsys.lib")
 
// Use the Shell Windows object to find all of the explorer and IExplorer 
// windows and close them.
 
void CloseExplorerWindows()
{
    IShellWindows* psw;
    
    if (SUCCEEDED(CoCreateInstance(CLSID_ShellWindows, 
                                   NULL,  
                                   CLSCTX_LOCAL_SERVER, 
                                   IID_PPV_ARGS(&psw))))
    {
        VARIANT v = { VT_I4 };
        if (SUCCEEDED(psw->get_Count(&v.lVal)))
        {
            // Walk backward to make sure that the windows that close
            // do not cause the array to be reordered.
            while (--v.lVal >= 0)
            {
                IDispatch *pdisp;
                
                if (S_OK == psw->Item(v, &pdisp))
                {
                    IWebBrowser2 *pwb;
                    if (SUCCEEDED(pdisp->QueryInterface(IID_PPV_ARGS(&pwb))))
                    {
                        pwb->Quit();
                        pwb->Release();
                    }
                    pdisp->Release();
                }
            }
        }
        psw->Release();
    }
}
 
// Convert an IShellItem or IDataObject into a VARIANT that holds an IDList
// suitable for use with IWebBrowser2::Navigate2.
 
HRESULT InitVariantFromObject(IUnknown *punk, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetIDListFromObject(punk, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}
 
HRESULT ParseItemAsVariant(PCWSTR pszItem, IBindCtx *pbc, VARIANT *pvar)
{
    VariantInit(pvar);
 
    IShellItem *psi;
    HRESULT hr = SHCreateItemFromParsingName(pszItem, NULL, IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

HRESULT GetKnownFolderAsVariant(REFKNOWNFOLDERID kfid, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetKnownFolderIDList(kfid, 0, NULL, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}

HRESULT GetShellItemFromCommandLine(REFIID riid, void **ppv)
{
    *ppv = NULL;
    HRESULT hr = E_FAIL;

    int cArgs;
    PWSTR *ppszCmd = CommandLineToArgvW(GetCommandLineW(), &cArgs);
    if (ppszCmd && cArgs > 1)
    {
        WCHAR szSpec[MAX_PATH];
        StringCchCopyW(szSpec, ARRAYSIZE(szSpec), ppszCmd[1]);
        PathUnquoteSpacesW(szSpec);

        hr = szSpec[0] ? S_OK : E_FAIL;   // Protect against empty data
        if (SUCCEEDED(hr))
        {
            hr = SHCreateItemFromParsingName(szSpec, NULL, riid, ppv);
            if (FAILED(hr))
            {
                WCHAR szFolder[MAX_PATH];
                GetCurrentDirectoryW(ARRAYSIZE(szFolder), szFolder);

                hr = PathAppendW(szFolder, szSpec) ? S_OK : E_FAIL;
                if (SUCCEEDED(hr))
                {
                    hr = SHCreateItemFromParsingName(szFolder, NULL, riid, ppv);
                }
            }
        }
    }
    return hr;
}

HRESULT GetShellItemFromCommandLineAsVariant(VARIANT *pvar)
{
    VariantInit(pvar);

    IShellItem *psi;
    HRESULT hr = GetShellItemFromCommandLine(IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

void OpenWindow()
{
    IWebBrowser2 *pwb;
    HRESULT hr = CoCreateInstance(CLSID_ShellBrowserWindow, 
                                  NULL,
                                  CLSCTX_LOCAL_SERVER, 
                                  IID_PPV_ARGS(&pwb));
    if (SUCCEEDED(hr))
    {
        CoAllowSetForegroundWindow(pwb, 0);

        pwb->put_Left(100);
        pwb->put_Top(100);
        pwb->put_Height(600);
        pwb->put_Width(800);
 
        VARIANT varTarget = {0};
        hr = GetShellItemFromCommandLineAsVariant(&varTarget);
        if (FAILED(hr))
        {
            hr = GetKnownFolderAsVariant(FOLDERID_UsersFiles, &varTarget);
        }

        if (SUCCEEDED(hr))
        {
            VARIANT vEmpty = {0};
            hr = pwb->Navigate2(&varTarget, &vEmpty, &vEmpty, &vEmpty, &vEmpty);
            if (SUCCEEDED(hr))
            {
                pwb->put_Visible(VARIANT_TRUE);
            }
            VariantClear(&varTarget);
        }
        pwb->Release();
    }
}

int WINAPI WinMain(HINSTANCE, HINSTANCE, LPSTR, int)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |  COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CloseExplorerWindows();

        OpenWindow();

        CoUninitialize();
    }
    return 0;
}
```



Der Windows-Explorer-Client Bereich kann mithilfe der [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) -Schnittstelle gehostet werden. Die Steuerelemente Windows Explorer-Client und Namespace Tree sind Standardkomponenten von Windows Vista und höher. Entwickler können die Schnittstellen als Bausteine wieder verwenden. Diese Steuerelemente werden häufig verwendet, um angepasste explorergeeignete explorerelemente für die Problemdomäne zu erstellen.

Die Steuerelemente in Windows-Explorer werden in die folgenden Funktions Kategorien eingeteilt:

-   [Navigations Steuerelemente](#navigation-controls)
-   [Command-Steuerelemente für Befehle](#command-controls)
-   [Eigenschaften-und Vorschau Steuerelemente](#property-and-preview-controls)
-   [Filtern und Anzeigen von Steuerelementen](#filtering-and-view-controls)
-   [ListView-Steuerelement](#listview-control)

## <a name="navigation-controls"></a>Navigations Steuerelemente

Navigations Steuerelemente unterstützen Benutzer beim Bestimmen des Kontexts und Navigieren im zugeordneten logischen Domänen Bereich, dem sogenannten Pagespace. Der Pagespace für Windows-Explorer ist beispielsweise der Shellnamespace. Pagespaces bestehen aus null oder mehr Seiten.

In der folgenden Tabelle sind die Navigations Steuerelemente aufgeführt und beschrieben, die in Windows-Explorer in den Betriebssystemen Windows Vista und höher verfügbar sind.



| Navigations Steuerelement               | BESCHREIBUNG                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Adressleiste (Breadcrumb-Steuerelement) | Zeigt die Adresse der aktuellen Seite im Pagespace an. Sie können auf Breadcrumb-Schaltflächen klicken, um zu einem beliebigen Vorgänger im Pagespace zu navigieren. Benutzer können auch URLs und Pfade eingeben, um zu navigieren. |
| Ordnerstruktur                      | Stellt eine neue Version eines Tree-Steuer Elements bereit, das für große Seitenbereiche optimiert ist.                                                                                                                  |
| Reise                           | Ermöglicht die relative Navigation durch Webstil-Schaltflächen wie " **zurück** " und " **Vorwärts**".                                                                                                    |
| Titel                            | Zeigt den Namen und den Kontext des aktuellen Explorers an.                                                                                                                                            |
| Pagespace                        | Zeigt die aktuelle Verzweigung des Pagespace an. Seiten können nach verschiedenen Kriterien angeordnet werden. Benutzer können auf eine Seite klicken, um zu dieser zu navigieren.                                                        |



 

## <a name="command-controls"></a>Command-Steuerelemente für Befehle

Befehls Steuerelemente kündigen den Benutzern die Features und Funktionen von Windows Explorer. Diese Steuerelemente führen entweder allgemeine Aktionen oder Aktionen aus, die für ein ausgewähltes Element oder bestimmte Elemente spezifisch sind.



| Befehls Steuerelement | BESCHREIBUNG                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Symbolleiste         | Zeigt Schaltflächen für häufig verwendete Befehle an (eine neue Version einer Befehls Symbolleiste). Zu den Anpassungsoptionen zählen Dropdown-Schaltflächen, unterteilte Schaltflächen, optionaler beschreibender Text und ein Überlauf Bereich. |
| Hero            | Wird als einzelnes, optionales benutzerdefiniertes Steuerelement in der Mitte der Symbolleiste angezeigt. Er stellt den primären Befehl für den aktuellen Kontext dar.                                                             |
| Menüleiste        | Zeigt Befehle über Menüs an.                                                                                                                                                                   |
| Kontextmenü    | Listet eine Kontext relevante Teilmenge verfügbarer Befehle auf, die als Ergebnis des Rechtsklick auf ein Element angezeigt werden.                                                                               |



 

## <a name="property-and-preview-controls"></a>Eigenschaften-und Vorschau Steuerelemente

Eigenschaften-und Vorschau Steuerelemente werden verwendet, um Vorschau Elemente anzuzeigen und Element Eigenschaften anzuzeigen und zu bearbeiten.



| Control    | BESCHREIBUNG                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorschau    | Zeigt eine Vorschau des ausgewählten Elements an, z. b. eine Miniaturansicht oder ein Live Symbol.                                                                                                                                                                       |
| Eigenschaften | Zeigt die Eigenschaften des ausgewählten Elements an. Bei Mehrfachauswahl wird eine Zusammenfassung der Eigenschaften für die ausgewählte Gruppe von Elementen angezeigt. Bei einer null-Auswahl wird eine Zusammenfassung der Eigenschaften für die aktuelle Seite (Inhalt von ListView) angezeigt. |



 

## <a name="filtering-and-view-controls"></a>Filtern und Anzeigen von Steuerelementen

Filter-und Sicht Steuerelemente werden verwendet, um den Satz von Elementen in der ListView zu manipulieren und die Darstellung von Elementen in der ListView zu ändern.



| Control   | BESCHREIBUNG                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| Filtern    | Filtert oder ordnet Elemente in einer ListView auf der Grundlage von Eigenschaften an, die als Spalten aufgelistet sind. Wenn Sie auf eine Spalte klicken, wird diese Eigenschaft sortiert. |
| Wordwheel | Filtert dynamisch und inkrementell die angezeigten Elemente in einer ListView basierend auf einer Eingabetext Zeichenfolge.                      |
| Sicht      | Ermöglicht dem Benutzer das Ändern des Ansichtsmodus eines ListView-Steuer Elements. Ein Schieberegler kann verwendet werden, um die Symbolgröße zu bestimmen.                |



 

## <a name="listview-control"></a>ListView-Steuerelement

Das ListView-Steuerelement wird zum Anzeigen eines Satzes von Elementen in einem der vier Ansichtsmodi verwendet: Details, Kacheln, Symbole oder Panorama. Das ListView-Steuerelement ermöglicht es dem Benutzer auch, ein oder mehrere Elemente auszuwählen und zu aktivieren.

> [!Caution]  
> Obwohl einige dieser Steuerelemente Namen und/oder Funktionen aufweisen, die den im System. Windows. Controls-Namespace gefundenen Standard-Windows Presentation Foundation (WPF)-Steuerelementen ähneln, sind Sie unterschiedliche Klassen.

 

Diese separaten Steuerelemente arbeiten größtenteils über Ereignisse, die entweder durch eine Benutzerinteraktion oder durch die Steuerelemente selbst generiert werden. In der folgenden Tabelle werden die drei primären Ereignis Kategorien aufgeführt.



| Ereigniskategorie | Beispiel                                                       |
|----------------|---------------------------------------------------------------|
| Navigation     | Von einer Seite zu einer anderen wechseln.                               |
| Auswahl      | Ändern der aktuellen Auswahl in der ListView.               |
| Änderung anzeigen    | Ändern der Präsentations Reihenfolge oder des Ansichtsmodus in ListView. |



 

 

 
