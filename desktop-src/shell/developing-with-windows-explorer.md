---
description: Windows Explorer ist eine leistungsstarke Anwendung für das Durchsuchen und Die Verwaltung von Ressourcen.
ms.assetid: 879CE652-EDC0-4a14-925E-C83763133BE5
title: Entwickeln mit Windows Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d00b513b3ee73c30b100cb4236d2c9fb327e1f9557d12ba86738ee9e910ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460183"
---
# <a name="developing-with-windows-explorer"></a>Entwickeln mit Windows Explorer

Windows Explorer ist eine leistungsstarke Anwendung für das Durchsuchen und Die Verwaltung von Ressourcen. Windows Auf den Explorer kann als integriertes Ganzes über Explorer.exe oder die [**IExplorerBrowser-Schnittstelle zugegriffen**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) werden. Windows Der Explorer (Explorer.exe) kann mit [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) oder einer ähnlichen Funktion als separater Prozess ausgeführt werden.

> [!Note]  
> Befehlszeilenoptionen für Explorer.exe sind auf der Microsoft Windows Support-Website im Artikel Windows [Explorer Command-Line dokumentiert.](https://support.microsoft.com/kb/152457)

 

Geöffnete Explorer-Fenster können mithilfe von [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID ShellWindows) gefunden und programmiert werden, und neue Instanzen von Windows Explorer können mithilfe von \_ [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID \_ ShellBrowserWindow) erstellt werden.

Das folgende Codebeispiel veranschaulicht, wie das Windows Explorer-Automatisierungsmodell verwendet werden kann, um ausgeführte Explorer-Fenster zu erstellen und zu entdecken.


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



Der Windows Explorer-Clientbereich kann über die [IExplorerBrowser-Schnittstelle gehostet](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) werden. Der Windows Explorer-Client und die Namespacestruktur-Steuerelemente sind Standardkomponenten von Windows Vista und höher. Entwickler können die Schnittstellen wiederverwenden, um Komponenten zu erstellen. Diese Steuerelemente werden häufig verwendet, um benutzerdefinierte Explorer zu erstellen, die für die Problemdomäne geeignet sind.

Die Steuerelemente im Windows Explorer werden in die folgenden Funktionalen Kategorien klassifiziert:

-   [Navigationssteuerelemente](#navigation-controls)
-   [Command-Steuerelemente für Befehle](#command-controls)
-   [Eigenschaften- und Vorschausteuerelemente](#property-and-preview-controls)
-   [Filtern und Anzeigen von Steuerelementen](#filtering-and-view-controls)
-   [Listview-Steuerelement](#listview-control)

## <a name="navigation-controls"></a>Navigationssteuerelemente

Navigationssteuerelemente unterstützen Benutzer beim Bestimmen des Kontexts und navigieren im zugeordneten logischen Domänenbereich, der als Pagespace bezeichnet wird. Beispielsweise ist der Pagespace für Windows Explorer der Shellnamespace. Pagespaces bestehen aus 0 (null) oder mehr Seiten.

In der folgenden Tabelle sind die Navigationssteuerelemente aufgeführt und beschrieben, die im Windows Explorer in den Betriebssystemen Windows Vista und höher verfügbar sind.



| Navigationssteuer steuerelement               | BESCHREIBUNG                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Adressleiste (Breadcrumb-Steuerelement) | Zeigt die Adresse der aktuellen Seite im Pagespace an. Sie können auf Breadcrumb-Schaltflächen klicken, um zu einem beliebigen Vorgänger im Pagespace zu navigieren. Benutzer können auch URLs und Pfade eingeben, um zu navigieren. |
| Ordnerstruktur                      | Stellt eine neue Version eines Struktursteuer steuerelements zur Optimierung für große Pagespaces zur Auswahl.                                                                                                                  |
| Reise                           | Ermöglicht die relative Navigation durch Schaltflächen im Webformat, z. **B. Zurück** und **Vorwärts.**                                                                                                    |
| Titel                            | Zeigt den aktuellen Explorernamen und -kontext an.                                                                                                                                            |
| Pagespace                        | Zeigt den aktuellen Branch des Seitenbereichs an. Seiten können nach unterschiedlichen Kriterien geordnet werden. Benutzer können auf eine Seite klicken, um zu ihr zu navigieren.                                                        |



 

## <a name="command-controls"></a>Command-Steuerelemente für Befehle

Befehlssteuerelemente geben den Benutzern die Features und Funktionen des Windows Explorer an. Diese Steuerelemente führen entweder allgemeine Aktionen oder Aktionen aus, die für ein oder mehrere ausgewählte Elemente spezifisch sind.



| Befehlssteuerung | BESCHREIBUNG                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Symbolleiste         | Zeigt Schaltflächen für häufig verwendete Befehle an (eine neue Version einer Befehlssymbolleiste). Zu den Anpassungsoptionen gehören Dropdownschaltflächen, geteilte Schaltflächen, optionaler beschreibender Text und ein Überlaufbereich. |
| Hero            | Wird als einzelnes, optionales benutzerdefiniertes Steuerelement in der Mitte der Symbolleiste angezeigt. Sie stellt den primären Befehl für den aktuellen Kontext dar.                                                             |
| Menüleiste        | Zeigt Befehle über Menüs an.                                                                                                                                                                   |
| Kontextmenü    | Listet eine kontextbezogene Teilmenge der verfügbaren Befehle auf, die als Ergebnis eines Rechtsklicks auf ein Element angezeigt werden.                                                                               |



 

## <a name="property-and-preview-controls"></a>Eigenschaften- und Vorschausteuerelemente

Eigenschaften- und Vorschausteuerelemente werden verwendet, um eine Vorschau von Elementen anzuzeigen und Elementeigenschaften anzuzeigen und zu bearbeiten.



| Control    | BESCHREIBUNG                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorschau    | Zeigt eine Vorschau des ausgewählten Elements an, z. B. eine Miniaturansicht oder ein Livesymbol.                                                                                                                                                                       |
| Eigenschaften | Zeigt Eigenschaften des ausgewählten Elements an. Bei mehrfacher Auswahl wird eine Zusammenfassung der Eigenschaften für die ausgewählte Gruppe von Elementen angezeigt. Bei einer NULL-Auswahl wird eine Zusammenfassung der Eigenschaften für die aktuelle Seite (Inhalt der Listenansicht) angezeigt. |



 

## <a name="filtering-and-view-controls"></a>Filtern und Anzeigen von Steuerelementen

Filter- und Ansichtssteuerelemente werden verwendet, um den Satz von Elementen in der Listenansicht zu bearbeiten und die Darstellung von Elementen in der Listenansicht zu ändern.



| Control   | BESCHREIBUNG                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| Filtern    | Filtert oder ordnet Elemente in einer Listenansicht basierend auf Eigenschaften an, die als Spalten aufgelistet sind. Wenn Sie auf eine Spalte klicken, wird nach dieser Eigenschaft sortiert. |
| Wordwheel | Filtert die angezeigten Elemente in einer Listenansicht dynamisch und inkrementell basierend auf einer Eingabetextzeichenfolge.                      |
| Sicht      | Ermöglicht dem Benutzer, den Ansichtsmodus eines ListView-Steuerelements zu ändern. Ein Schieberegler kann verwendet werden, um die Symbolgröße zu bestimmen.                |



 

## <a name="listview-control"></a>Listview-Steuerelement

Das Listview-Steuerelement wird verwendet, um eine Gruppe von Elementen in einem von vier Ansichtsmodi anzuzeigen: Details, Kacheln, Symbole oder Panorama. Mit dem Listview-Steuerelement kann der Benutzer auch ein oder mehrere Elemente auswählen und aktivieren.

> [!Caution]  
> Einige dieser Steuerelemente verfügen zwar über Namen und/oder Funktionen, die den im System Windows Presentation Foundation -Standardsteuerelementen (WPF) ähneln. Windows. Steuert den Namespace. Dabei handelt es sich um unterschiedliche Klassen.

 

Diese separaten Steuerelemente arbeiten größtenteils über Ereignisse zusammen, die entweder durch Benutzerinteraktion oder durch die Steuerelemente selbst generiert werden. In der folgenden Tabelle sind die drei primären Ereigniskategorien aufgeführt.



| Ereigniskategorie | Beispiel                                                       |
|----------------|---------------------------------------------------------------|
| Navigation     | Von einer Seite auf eine andere.                               |
| Auswahl      | Ändern der aktuellen Auswahl in der Listenansicht.               |
| Änderung anzeigen    | Ändern der Präsentations reihenfolge oder des Ansichtsmodus in der Listenansicht. |



 

 

 
