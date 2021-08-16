---
title: Unterstützen von geräteseitigem Inhalt (PropertySheet)
description: Erfahren Sie, wie Sie die Windows Shell-API oder die WPD-API verwenden, um Daten für Geräteobjekte zu erhalten, auf die über das Dateisystem in Windows Vista nicht zugegriffen werden kann.
ms.assetid: ea11f8e6-fb53-46e4-b210-2dae33cdc056
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451bf63c1270b121cf909fa5ee07aff62cc3b83aa0e0d031cae61005f725c197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842567"
---
# <a name="supporting-device-side-content"></a>Unterstützen von geräteseitigem Inhalt

Da auf geräteseitige Inhalte nicht über das Dateisystem in Windows Vista zugegriffen werden kann, müssen Sie entweder die Windows Shell-API oder die WPD-API verwenden, um Daten für Geräteobjekte abzurufen. Dies ist der Hauptunterschied zwischen einem normalen Eigenschaftenblatthandler und einem WPD-Eigenschaftenblatthandler. Der folgende Beispielcode veranschaulicht das Abrufen geräteseitiger Inhalte mithilfe der Windows Shell-API.

Der erste Schritt ist die Initialisierung der Elementbezeichnerliste oder PIDL. (Diese Liste enthält den eindeutigen Bezeichner für das gegebene Geräteobjekt.)


```C++
HRESULT CWPDPropSheet::_InitializePIDLArray(IDataObject *pDataObj)
{
    if (m_cfHIDA == 0)
    {
        m_cfHIDA = (CLIPFORMAT)RegisterClipboardFormat(CFSTR_SHELLIDLIST);
    }

    STGMEDIUM   medium;
    FORMATETC   fmte = {m_cfHIDA, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};

    m_pPropInfo = (PROPINFO*)LocalAlloc(LPTR, sizeof(PROPINFO));
    if (m_pPropInfo == NULL)
        return E_OUTOFMEMORY;

    AddRef_PropInfo(m_pPropInfo);

    HRESULT hr = pDataObj->GetData(&fmte, &medium);
    if (SUCCEEDED(hr))
    {
        SIZE_T cb = GlobalSize(medium.hGlobal);
        CIDA *pida = (CIDA*)GlobalAlloc(GPTR, cb);
        if (pida)
        {
            void *pv = GlobalLock(medium.hGlobal);
            if (pv != NULL)
            {
                CopyMemory(pida, pv, cb);
                GlobalUnlock(medium.hGlobal);
                m_pPropInfo->pida = pida;
                _ExaminePIDLArray();
            }
            else
            {
                hr = E_UNEXPECTED;
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
        ReleaseStgMedium(&medium);
    }

    return hr;
}
```



Die Initialisierungsfunktion ruft die ExaminePIDLArray-Funktion auf, die die Eigenschaften für das Objekt abruft, das durch eine PIDL im \_ PIDL-Array identifiziert wird.


```C++
HRESULT CWPDPropSheet::_ExaminePIDLArray()
{
    CComPtr<IShellFolder2> spParentFolder;

    CComVariant  variant;

    LPITEMIDLIST pidl = NULL;
    HRESULT      hr = S_OK;
    UINT         index = 0;

    pidl = GetPIDL(m_pPropInfo->pida, index);
    if (pidl)
    {
        hr = SHBindToParent(pidl, IID_PPV_ARGS(&spParentFolder), NULL);
        IF_FAILED_JUMP(hr, Exit);
    }

    do
    {
        CComPtr<IPropertySetStorage> spSetStorage;
        CComPtr<IPropertyStorage>    spPropStorage;

        // Get the IpropertySetStorage interface for this PIDL. This method could also
        // be used to retrieve an IPortableDevice interface to allow more low-level interaction
        // with the WPD API.
        hr = spParentFolder->BindToObject(ILFindLastID(pidl), NULL, IID_PPV_ARGS(&spSetStorage));
        if (SUCCEEDED(hr))
        {
            hr = spSetStorage->Open(WPD_FUNCTIONAL_OBJECT_PROPERTIES_V1, STGM_READ, &spPropStorage);
            if (SUCCEEDED(hr))
            {
                PROPVARIANT PropVar = {0};
                PROPSPEC    PropSpec = {0};

                PropSpec.ulKind = PRSPEC_PROPID;
                PropSpec.propid = 2; // WPD_FUNCTIONAL_OBJECT_CATEGORY

                PropVariantInit(&PropVar);

                hr = spPropStorage->ReadMultiple(1, &PropSpec, &PropVar);
                if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                {
                    // The PIDL array contains a non-file object.
                    // This means we don't want to take over the
                    // default menu action.
                    m_bPIDAContainsOnlyFiles = FALSE;
                    PropVariantClear(&PropVar);
                    break;
                }
                else
                {
                    CComPtr<IPropertyStorage>    spObjectProperties;
                    hr = spSetStorage->Open(WPD_OBJECT_PROPERTIES_V1, STGM_READ, &spObjectProperties);
                    if (SUCCEEDED(hr))
                    {
                        PropSpec.ulKind = PRSPEC_PROPID;
                        PropSpec.propid = 7; // WPD_OBJECT_CONTENT_TYPE
                        
                        PropVariantClear(&PropVar);
                        hr = spObjectProperties->ReadMultiple(1, &PropSpec, &PropVar);
                        if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                        {
                            if (IsEqualGUID(*PropVar.puuid, WPD_CONTENT_TYPE_FOLDER))
                            {
                                // The PIDL array contains a folder object.
                                // This means we don't want to take over the
                                // default menu action.
                                m_bPIDAContainsOnlyFiles = FALSE;
                                PropVariantClear(&PropVar);
                                break;
                            }
                        }
                    }
                }

                PropVariantClear(&PropVar);
            }
        }

        UI_SAFE_ILFREE(pidl);

        pidl = GetPIDL(m_pPropInfo->pida, ++index);
    } while (pidl != NULL && index < m_pPropInfo->pida->cidl);

Exit:
    UI_SAFE_ILFREE(pidl);
    return hr;
}
```



Zusätzlich zur Initialisierung und Verarbeitung der Elementbezeichnerliste muss Ihre Anwendung die IShellPropSheetExt::ReplacePage-Methode implementieren und die entsprechenden Ersetzungshandler einfügen. Die Windows Shell ruft diese Methode jedes Mal auf, wenn ein ersetzbares Eigenschaftenblatt angezeigt wird, was Ihrer Anwendung die Möglichkeit gibt, einen entsprechenden Ersatzhandler aufrufen. Das niedrige Wort des ersten Parameters für die ReplacePage-Methode ist ein Bezeichner für das gegebene Eigenschaftenblatt, Windows angezeigt werden soll. Die im unteren Wort des ersten Parameters übergebenen Werte entsprechen den Werten, die in der Datei WpdShellExtension.h definiert sind. Diese Werte und ihre Beschreibungen sind in der folgenden Tabelle aufgeführt.



| Wert                                  | Beschreibung                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| WPDNSE \_ \_ PROPSHEET-GERÄT \_ ALLGEMEIN     | Entspricht der Registerkarte "Allgemein" für das Gerät.                              |
| WPDNSE \_ PROPSHEET \_ STORAGE \_ ALLGEMEIN    | Entspricht der Registerkarte "Allgemein" für ein Speicherobjekt, das auf dem Gerät gefunden wurde.    |
| WPDNSE \_ \_ PROPSHEET-INHALT \_ ALLGEMEIN    | Entspricht der Registerkarte "Allgemein" für das Inhaltsobjekt, das auf dem Gerät gefunden wurde.      |
| WPDNSE \_ \_ PROPSHEET-INHALTSVERWEISE \_ | Entspricht der Registerkarte "Verweise" für ein Inhaltsobjekt, das auf dem Gerät gefunden wurde. |
| WPDNSE \_ \_ PROPSHEET-INHALTSRESSOURCEN \_  | Entspricht der Registerkarte "Ressourcen" für ein Inhaltsobjekt, das auf dem Gerät gefunden wurde.  |
| WPDNSE PROPSHEET CONTENT DETAILS (WPDNSE \_ \_ \_ PROPSHEET-INHALTSDETAILS)    | Entspricht einer Detailregisterkarte für ein Inhaltsobjekt, das auf dem Gerät gefunden wurde.      |



 

In der Beispiel-Eigenschaftenblatterweiterung ruft die ReplacePage-Methode zwei Ersetzungshandler auf: \_ ReplaceDeviceGeneral und \_ ReplaceContentReferences. Diese Handler ersetzen das allgemeine Gerät und die Registerkarten für Inhaltsverweise in den erweiterbaren Eigenschaftenblättern.


```C++
STDMETHODIMP CWPDPropSheet::ReplacePage(UINT uPageID, LPFNADDPROPSHEETPAGE lpfnReplacePage, LPARAM lParam)
{
    HRESULT       hr = S_OK;

    if (LOWORD(uPageID) == WPDNSE_PROPSHEET_DEVICE_GENERAL)
    {
        hr = _ReplaceDeviceGeneral(HIWORD(uPageID), lpfnReplacePage, lParam);
    }
    else if (LOWORD(uPageID) == WPDNSE_PROPSHEET_CONTENT_REFERENCES)
    {
        hr = _ReplaceContentReferences(HIWORD(uPageID), lpfnReplacePage, lParam);
    }

    return hr;
}
```



Da ein Benutzer mehrere Geräte auswählen kann, muss eine Anwendung das von IShellExtInit::Initialize zurückgegebene PIDL-Array speichern und dann das hohe Wort des ersten Parameters in ReplacePage untersuchen. Der Wert 0 (null) in diesem hohen Wort entspricht dem ersten Element im PIDL-Array, der Wert 1 entspricht dem zweiten Element und so weiter. In der ReplacePage-Funktion der Beispielanwendung wird dieser hohe Wortwert an beide Ersetzungshandler übergeben. Diese Handler verwenden wiederum diesen Wert, um ein bestimmtes Gerät zu identifizieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



