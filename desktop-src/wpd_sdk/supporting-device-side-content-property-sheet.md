---
title: Unterstützung von Geräte seitigem Inhalt (PropertySheet)
description: Unterstützen von Device-Side Inhalt
ms.assetid: ea11f8e6-fb53-46e4-b210-2dae33cdc056
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7e054e4c545acd8f34583da5cd9ef3af347643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347418"
---
# <a name="supporting-device-side-content"></a>Unterstützung von Geräte seitigem Inhalt

Da der Zugriff auf Geräte seitigen Inhalt über das Dateisystem in Windows Vista nicht möglich ist, müssen Sie entweder die Windows-Shell-API oder die WPD-API verwenden, um Daten für Geräte Objekte abzurufen. Dies ist der primäre Unterschied zwischen einem normalen Eigenschaften Blatt Handler und einem WPD-Eigenschaften Blatt Handler. Im folgenden Beispielcode wird das Abrufen von Geräte seitigem Inhalt mithilfe der Windows-Shell-API veranschaulicht.

Der erste Schritt ist die Initialisierung der Element Bezeichner Liste oder der PIDL. (Diese Liste enthält den eindeutigen Bezeichner für das angegebene Geräte Objekt.)


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



Die Initialisierungsfunktion Ruft die \_ examinepidlarray-Funktion auf, die die Eigenschaften für das Objekt abruft, das durch eine PIDL im PIDL-Array identifiziert wird.


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



Zusätzlich zur Initialisierung und Verarbeitung der Element Bezeichner-Liste muss Ihre Anwendung die ishellpropsheetext:: replacepage-Methode implementieren und die entsprechenden Ersatz Handler einfügen. Diese Methode wird von der Windows-Shell jedes Mal aufgerufen, wenn ein ersetzbares Eigenschaften Blatt angezeigt wird. Dadurch erhält die Anwendung die Möglichkeit, einen entsprechenden Ersatz Handler aufzurufen. Das niedrige Wort des ersten Parameters für die replacepage-Methode ist ein Bezeichner für das angegebene Eigenschaften Blatt, das in Windows angezeigt wird. Die Werte, die im unteren Wort des ersten Parameters übergeben werden, entsprechen den Werten, die in der Datei "wpdshellextension. h" definiert sind. Diese Werte und ihre Beschreibungen werden in der folgenden Tabelle angezeigt.



| Wert                                  | BESCHREIBUNG                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| wpdnse- \_ propsheet- \_ Gerät \_ Allgemein     | Entspricht der Registerkarte Allgemein für das Gerät.                              |
| wpdnse- \_ propsheet- \_ Speicher ( \_ Allgemein)    | Entspricht der Registerkarte Allgemein für ein Speicher Objekt, das sich auf dem Gerät befindet.    |
| wpdnse- \_ propsheet- \_ Inhalt \_ Allgemein    | Entspricht der Registerkarte Allgemein für das Inhalts Objekt, das auf dem Gerät gefunden wurde.      |
| Verweise auf wpdnse- \_ propsheet- \_ Inhalte \_ | Entspricht der Registerkarte Verweise für ein Inhalts Objekt, das sich auf dem Gerät befindet. |
| wpdnse- \_ propsheet- \_ Inhalts \_ Ressourcen  | Entspricht der Registerkarte Ressourcen für ein Inhalts Objekt, das sich auf dem Gerät befindet.  |
| Details zum wpdnse- \_ propsheet- \_ Inhalt \_    | Entspricht einer Registerkarte "Details" für ein Inhalts Objekt, das sich auf dem Gerät befindet.      |



 

In der Beispiel-Eigenschaften Blatt Erweiterung ruft die replacepage-Methode zwei Ersatz Handler auf: \_ replacedevicegeneral und \_ replacecontentreferences. Diese Handler ersetzen die Registerkarten Allgemeines Gerät und Inhalts Verweise in den Extensible-Eigenschaften Blättern.


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



Da ein Benutzer mehrere Geräte auswählen kann, muss eine Anwendung das von ishellextinit:: Initialize zurückgegebene PIDL-Array speichern und dann das hohe Wort des ersten Parameters auf replacepage überprüfen. Der Wert 0 (null) in diesem hohen Wort entspricht dem ersten Element im PIDL-Array, wobei der Wert 1 dem zweiten Element entspricht usw. In der replacepage-Funktion der Beispielanwendung wird dieser Wert für das hohe Wort an beide Austausch Handler weitergegeben. Diese Handler verwenden diesen Wert wiederum, um ein bestimmtes Gerät zu identifizieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



