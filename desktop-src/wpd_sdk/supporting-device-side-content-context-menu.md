---
title: Unterstützen von Geräte seitigem WPD-Inhalt (ContextMenu)
description: Unterstützen von Device-Side Inhalt
ms.assetid: 47fb7f49-9026-43c1-be46-8a520c048862
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b5e7029a6a772a5706eaf80270cc87ea83ab76b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353876"
---
# <a name="supporting-wpd-device-side-content"></a><span data-ttu-id="3468f-103">Unterstützen von Geräte seitigem WPD-Inhalt</span><span class="sxs-lookup"><span data-stu-id="3468f-103">Supporting WPD device-side content</span></span>

<span data-ttu-id="3468f-104">Da der Zugriff auf Geräte seitigen Inhalt über das Dateisystem in Windows Vista nicht möglich ist, müssen Sie entweder die Windows-Shell-API oder die WPD-API verwenden, um Daten für Geräte Objekte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3468f-104">Because device-side content is not accessible through the file system in Windows Vista, you'll need to use either the Windows Shell API or the WPD API to retrieve data for device objects.</span></span> <span data-ttu-id="3468f-105">Dies ist der primäre Unterschied zwischen einem normalen Kontextmenü Handler und einem WPD-Kontextmenü Handler.</span><span class="sxs-lookup"><span data-stu-id="3468f-105">This is the primary difference between a normal context menu handler and a WPD context menu handler.</span></span> <span data-ttu-id="3468f-106">Im folgenden Beispielcode wird das Abrufen von Geräte seitigem Inhalt mithilfe der Windows-Shell-API veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="3468f-106">The following sample code demonstrates the retrieval of device-side content using the Windows Shell API.</span></span>

<span data-ttu-id="3468f-107">Der erste Schritt ist die Initialisierung der Element Bezeichner Liste oder der PIDL.</span><span class="sxs-lookup"><span data-stu-id="3468f-107">The first step is the initialization of the item identifier list or PIDL.</span></span> <span data-ttu-id="3468f-108">(Diese Liste enthält den eindeutigen Bezeichner für das angegebene Geräte Objekt.)</span><span class="sxs-lookup"><span data-stu-id="3468f-108">(This list contains the unique identifier for the given device object.)</span></span>


```C++
HRESULT CWPDContextMenu::_InitializePIDLArray(IDataObject *pDataObj)
{
    if (m_cfHIDA == 0)
    {
        m_cfHIDA = (CLIPFORMAT)RegisterClipboardFormat(CFSTR_SHELLIDLIST);
    }

    STGMEDIUM   medium;
    FORMATETC   fmte = {m_cfHIDA, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};

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
                m_pida = pida;
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



<span data-ttu-id="3468f-109">Die Initialisierungsfunktion Ruft die \_ examinepidlarray-Funktion auf, die die Eigenschaften für das Objekt abruft, das durch eine PIDL im PIDL-Array identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="3468f-109">The initialization function calls the \_ExaminePIDLArray function, which retrieves the properties for object identified by a PIDL in the PIDL array.</span></span>


```C++
HRESULT CWPDContextMenu::_ExaminePIDLArray()
{
    CComPtr<IShellFolder2> spParentFolder;

    CComVariant  variant;

    LPITEMIDLIST pidl = NULL;
    HRESULT      hr = S_OK;
    UINT         index = 0;

    pidl = GetPIDL(m_pida, index);
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

        pidl = GetPIDL(m_pida, ++index);
    } while (pidl != NULL && index < m_pida->cidl);

Exit:
    UI_SAFE_ILFREE(pidl);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3468f-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3468f-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3468f-111">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="3468f-111">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



