---
title: Verwenden von OLE in Rich Edit-Steuerelementen
description: Dieser Abschnitt enthält Informationen zur Verwendung von Object Linking and Embedding (OLE) in Rich Edit-Steuerelementen.
ms.assetid: bfcecbf5-cc35-47b8-a713-7e5fd03f60cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7868bd62044c87765a25f6033499460ed044e57
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "104101379"
---
# <a name="how-to-use-ole-in-rich-edit-controls"></a>Verwenden von OLE in Rich Edit-Steuerelementen

Dieser Abschnitt enthält Informationen zur Verwendung von Object Linking and Embedding (OLE) in Rich Edit-Steuerelementen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="use-a-rich-edit-interface"></a>Verwenden einer Rich Edit-Schnittstelle

Rich Edit-Steuerelemente machen einige ihrer Funktionen über Component Object Model (com)-Schnittstellen verfügbar. Indem Sie eine Schnittstelle von einem Steuerelement erhalten, haben Sie die Möglichkeit, mit anderen Objekten innerhalb des Steuer Elements zu arbeiten. Sie können diese Schnittstelle abrufen, indem Sie die [**\_ getoleinterface**](em-getoleinterface.md) -Nachricht von EM senden. Von der [**iricheditole**](/windows/desktop/api/Richole/nn-richole-iricheditole) -Schnittstelle aus können Sie dann Schnittstellen abrufen, die im [Text Objektmodell](text-object-model.md)verwendet werden.

Eine weitere Schnittstelle, [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), wird von Anwendungen implementiert, um das Verhalten des Steuer Elements zu definieren, wenn es mit Objekten interagiert.

### <a name="insert-an-object-into-a-rich-edit-control"></a>Einfügen eines Objekts in ein Rich Edit-Steuerelement

Im folgenden Codebeispiel wird ein Datei Objekt in ein Rich-Edit-Steuerelement eingefügt. Wenn ein Programm dem Dateityp auf dem Computer des Benutzers (z. b. Microsoft Excel für eine XLS-Datei) zugeordnet ist, wird der Inhalt der Datei im Steuerelement angezeigt. Andernfalls wird ein Symbol angezeigt.

1.  Holen Sie sich die [**iricheditole**](/windows/desktop/api/Richole/nn-richole-iricheditole) -Schnittstelle.

    ```
    BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
    {
        HRESULT hr;

        LPRICHEDITOLE pRichEditOle;
        SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);
        
        ...
    ```

    

2.  Erstellen Sie eine strukturierte Speicherung.

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

    

4.  Einen Zeiger auf die Anzeige Site erhalten.

    ```
        LPOLECLIENTSITE pClientSite;
        hr = pRichEditOle->GetClientSite(&pClientSite);
        
        ...
    ```

    

5.  Erstellen Sie das Objekt, und rufen Sie die **IUnknown** -Schnittstelle ab

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

    

6.  Holen Sie sich die IOleObject-Schnittstelle für das-Objekt.

    ```
        LPOLEOBJECT pObject;
        
        hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
        
        pUnk->Release();

        ...
    ```

    

7.  Um sicherzustellen, dass Verweise ordnungsgemäß gezählt werden, Benachrichtigen Sie das Objekt, dass es enthalten ist.

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

    

9.  Verschieben Sie die Einfügemarke an das Ende des Texts, und fügen Sie einen Wagen Rücklauf ein.

    ```
        SendMessage(hRichEdit, EM_SETSEL, 0, -1);
        
        DWORD dwStart, dwEnd;
        
        SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
        SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
        SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

        ...
    ```

    

10. Fügen Sie das-Objekt ein.

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

Anwendungen implementieren die [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) -Schnittstelle, um auf OLE-bezogene Abfragen oder Aktionen zu reagieren, die von einem Rich Edit-Steuerelement ausgeführt werden. Sie verknüpfen die Implementierung der-Schnittstelle mit dem-Steuerelement, indem Sie eine [**EM- \_**](em-setolecallback.md) Abmeldung senden. Das-Steuerelement ruft dann die Methoden für die Implementierung der-Schnittstelle nach Bedarf auf.

Beispielsweise wird [**queryaccept-Data**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) aufgerufen, wenn der Benutzer versucht, ein Objekt per Drag & amp; Drop in das Steuerelement einzufügen. Wenn die Anwendung die Daten akzeptieren kann, gibt die Implementierung der-Methode S \_ OK zurück; andernfalls wird ein Fehlercode zurückgegeben. Die-Methode kann auch andere Aktionen ausführen, z. b. den Benutzer warnen, dass Dateien dieses Typs nicht im Steuerelement abgelegt werden können.

## <a name="complete-insertobject-example-function"></a>Complete insertObject-Beispiel Funktion

Im folgenden Codebeispiel werden die vorherigen Code Ausschnitte veranschaulicht, die zu einer kompletten Funktion kombiniert werden, die die Fehlerbehandlung einschließt.


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

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




