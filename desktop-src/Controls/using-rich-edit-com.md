---
title: Verwenden von OLE in Rich Edit-Steuerelementen
description: Dieser Abschnitt enthält Informationen zur Verwendung von Objektverknüpfung und -einbettung (OLE) in Rich-Edit-Steuerelementen.
ms.assetid: bfcecbf5-cc35-47b8-a713-7e5fd03f60cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d825a9876005cadb20e4fc7717f766582ab12224f4f86995319357875d24230
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119311680"
---
# <a name="how-to-use-ole-in-rich-edit-controls"></a>Verwenden von OLE in Rich Edit-Steuerelementen

Dieser Abschnitt enthält Informationen zur Verwendung von Objektverknüpfung und -einbettung (OLE) in Rich-Edit-Steuerelementen.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="use-a-rich-edit-interface"></a>Verwenden einer Rich Edit-Schnittstelle

Umfangreiche Bearbeitungssteuerelemente machen einige ihrer Funktionen über Component Object Model (COM)-Schnittstellen verfügbar. Durch das Abrufen einer Schnittstelle aus einem Steuerelement erhalten Sie die Möglichkeit, mit anderen Objekten innerhalb des Steuerelements zu arbeiten. Sie können diese Schnittstelle abrufen, indem Sie die [**EM \_ GETOLEINTERFACE-Nachricht**](em-getoleinterface.md) senden. Über die [**IRichEditOle-Schnittstelle**](/windows/desktop/api/Richole/nn-richole-iricheditole) können Sie dann Schnittstellen abrufen, die im [Textobjektmodell verwendet werden.](text-object-model.md)

Eine andere Schnittstelle, [**IRichEditOleCallback,**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)wird von Anwendungen implementiert, um das Verhalten des Steuerelements zu definieren, wenn es mit Objekten interagiert.

### <a name="insert-an-object-into-a-rich-edit-control"></a>Einfügen eines Objekts in ein Rich Edit-Steuerelement

Im folgenden Codebeispiel wird ein Dateiobjekt in ein Rich-Edit-Steuerelement eingefügt. Wenn ein Programm dem Dateityp auf dem Computer des Benutzers zugeordnet ist (z. B. Microsoft Excel für eine .xls-Datei), wird der Inhalt der Datei im -Steuerelement angezeigt. Andernfalls wird ein Symbol angezeigt.

1.  Erhalten Sie [**die IRichEditOle-Schnittstelle.**](/windows/desktop/api/Richole/nn-richole-iricheditole)

    ```
    BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
    {
        HRESULT hr;

        LPRICHEDITOLE pRichEditOle;
        SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);
        
        ...
    ```

    

2.  Erstellen Sie strukturierten Speicher.

    ```
        LPLOCKBYTES pLockBytes = NULL;
        hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);
        
        LPSTORAGE pStorage;
        hr = StgCreateDocfileOnILockBytes(pLockBytes, 
                                          STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
                                          0, &pStorage);
        ...
    ```

    

3.  Richten Sie das Datenformat ein.

    ```
        FORMATETC formatEtc;
        
        formatEtc.cfFormat = 0;
        formatEtc.ptd      = NULL;
        formatEtc.dwAspect = DVASPECT_CONTENT;
        formatEtc.lindex   = -1;
        formatEtc.tymed    = TYMED_NULL;
        
        ...
    ```

    

4.  Sie erhalten einen Zeiger auf die Anzeigewebsite.

    ```
        LPOLECLIENTSITE pClientSite;
        hr = pRichEditOle->GetClientSite(&pClientSite);
        
        ...
    ```

    

5.  Erstellen Sie das -Objekt, und rufen Sie dessen **IUnknown-Schnittstelle** ab.

    ```
        LPUNKNOWN pUnk;
        CLSID clsid = CLSID_NULL;
        
        hr = OleCreateFromFile(clsid, 
                               pszFileName, 
                               IID_IUnknown, 
                               OLERENDER_DRAW, 
                               &formatEtc, 
                               pClientSite, 
                               pStorage, 
                               (void**)&pUnk);
        
        pClientSite->Release();
                  
        ...
    ```

    

6.  Sie können die IOleObject-Schnittstelle für das -Objekt erhalten.

    ```
        LPOLEOBJECT pObject;
        
        hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
        
        pUnk->Release();

        ...
    ```

    

7.  Um sicherzustellen, dass Verweise ordnungsgemäß gezählt werden, benachrichtigen Sie das Objekt, dass es enthalten ist.

    ```
        OleSetContainedObject(pObject, TRUE);

        ...
    ```

    

8.  Richten Sie Objektinformationen ein.

    ```
        REOBJECT reobject = { sizeof(REOBJECT)};
        
        hr = pObject->GetUserClassID(&clsid);
        
        reobject.clsid    = clsid;
        reobject.cp       = REO_CP_SELECTION;
        reobject.dvaspect = DVASPECT_CONTENT;
        reobject.dwFlags  = REO_RESIZABLE | REO_BELOWBASELINE;
        reobject.dwUser   = 0;
        reobject.poleobj  = pObject;
        reobject.polesite = pClientSite;
        reobject.pstg     = pStorage;
        
        SIZEL sizel       = { 0 };
        reobject.sizel    = sizel;

        ...
    ```

    

9.  Verschieben Sie das Caret- an das Ende des Texts, und fügen Sie einen Wagenrücklauf hinzu.

    ```
        SendMessage(hRichEdit, EM_SETSEL, 0, -1);
        
        DWORD dwStart, dwEnd;
        
        SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
        SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
        SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

        ...
    ```

    

10. Fügen Sie das -Objekt ein.

    ```
        hr = pRichEditOle->InsertObject(&reobject);

        ...
    ```

    

11. Bereinigen

    ```
        pObject->Release();
        
        pRichEditOle->Release();

        return TRUE;
        
    }
    ```

    

### <a name="using-iricheditolecallback"></a>Verwenden von IRichEditOleCallback

Anwendungen implementieren die [**IRichEditOleCallback-Schnittstelle,**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) um auf OLE-bezogene Abfragen oder Aktionen zu reagieren, die von einem Rich-Edit-Steuerelement ausgeführt werden. Sie ordnen die Implementierung der -Schnittstelle dem -Steuerelement zu, indem Sie eine [**EM \_ SETOLECALLBACK-Nachricht**](em-setolecallback.md) senden. Das -Steuerelement ruft dann methoden für Ihre Implementierung der -Schnittstelle entsprechend auf.

[**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) wird beispielsweise aufgerufen, wenn der Benutzer versucht, ein Objekt zu ziehen oder in das Steuerelement einfüge. Wenn Ihre Anwendung die Daten akzeptieren kann, gibt Ihre Implementierung der -Methode S \_ OK zurück. Andernfalls wird ein Fehlercode zurückgegeben. Die -Methode kann auch eine andere Aktion ergreifen, z. B. den Benutzer warnen, dass Dateien dieses Typs nicht in das Steuerelement platziert werden können.

## <a name="complete-insertobject-example-function"></a>Vollständige InsertObject-Beispielfunktion

Im folgenden Codebeispiel werden die vorherigen Codeausschnitte in einer vollständigen Funktion kombiniert, die die Fehlerbehandlung umfasst.


```C++
BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
{
    HRESULT hr;

    LPRICHEDITOLE pRichEditOle;
    SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);

    if (pRichEditOle == NULL)
    {
        return FALSE;
    }

    LPLOCKBYTES pLockBytes = NULL;
    hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPSTORAGE pStorage;
    hr = StgCreateDocfileOnILockBytes(pLockBytes, 
           STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
           0, &pStorage);

    if (FAILED(hr))
    {
        return FALSE;
    }

    FORMATETC formatEtc;
    formatEtc.cfFormat = 0;
    formatEtc.ptd = NULL;
    formatEtc.dwAspect = DVASPECT_CONTENT;
    formatEtc.lindex = -1;
    formatEtc.tymed = TYMED_NULL;

    LPOLECLIENTSITE pClientSite;
    hr = pRichEditOle->GetClientSite(&pClientSite);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPUNKNOWN pUnk;
    CLSID clsid = CLSID_NULL;

    hr = OleCreateFromFile(clsid, pszFileName, IID_IUnknown, OLERENDER_DRAW, 
           &formatEtc, pClientSite, pStorage, (void**)&pUnk);

    pClientSite->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPOLEOBJECT pObject;
    hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
    pUnk->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    OleSetContainedObject(pObject, TRUE);
    REOBJECT reobject = { sizeof(REOBJECT)};
    hr = pObject->GetUserClassID(&clsid);

    if (FAILED(hr))
    {
        pObject->Release();
        return FALSE;
    }

    reobject.clsid = clsid;
    reobject.cp = REO_CP_SELECTION;
    reobject.dvaspect = DVASPECT_CONTENT;
    reobject.dwFlags = REO_RESIZABLE | REO_BELOWBASELINE;
    reobject.dwUser = 0;
    reobject.poleobj = pObject;
    reobject.polesite = pClientSite;
    reobject.pstg = pStorage;
    SIZEL sizel = { 0 };
    reobject.sizel = sizel;

    SendMessage(hRichEdit, EM_SETSEL, 0, -1);
    DWORD dwStart, dwEnd;
    SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
    SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
    SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

    hr = pRichEditOle->InsertObject(&reobject);
    pObject->Release();
    pRichEditOle->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }
    
    return TRUE;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




