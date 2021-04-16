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
# <a name="supporting-device-side-content"></a><span data-ttu-id="2a054-103">Unterstützung von Geräte seitigem Inhalt</span><span class="sxs-lookup"><span data-stu-id="2a054-103">Supporting device-side content</span></span>

<span data-ttu-id="2a054-104">Da der Zugriff auf Geräte seitigen Inhalt über das Dateisystem in Windows Vista nicht möglich ist, müssen Sie entweder die Windows-Shell-API oder die WPD-API verwenden, um Daten für Geräte Objekte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2a054-104">Because device-side content is not accessible through the file system in Windows Vista, you'll need to use either the Windows Shell API or the WPD API to retrieve data for device objects.</span></span> <span data-ttu-id="2a054-105">Dies ist der primäre Unterschied zwischen einem normalen Eigenschaften Blatt Handler und einem WPD-Eigenschaften Blatt Handler.</span><span class="sxs-lookup"><span data-stu-id="2a054-105">This is the primary difference between a normal property sheet handler and a WPD property sheet handler.</span></span> <span data-ttu-id="2a054-106">Im folgenden Beispielcode wird das Abrufen von Geräte seitigem Inhalt mithilfe der Windows-Shell-API veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2a054-106">The following sample code demonstrates the retrieval of device-side content using the Windows Shell API.</span></span>

<span data-ttu-id="2a054-107">Der erste Schritt ist die Initialisierung der Element Bezeichner Liste oder der PIDL.</span><span class="sxs-lookup"><span data-stu-id="2a054-107">The first step is the initialization of the item identifier list or PIDL.</span></span> <span data-ttu-id="2a054-108">(Diese Liste enthält den eindeutigen Bezeichner für das angegebene Geräte Objekt.)</span><span class="sxs-lookup"><span data-stu-id="2a054-108">(This list contains the unique identifier for the given device object.)</span></span>


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



<span data-ttu-id="2a054-109">Die Initialisierungsfunktion Ruft die \_ examinepidlarray-Funktion auf, die die Eigenschaften für das Objekt abruft, das durch eine PIDL im PIDL-Array identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2a054-109">The initialization function calls the \_ExaminePIDLArray function, which retrieves the properties for object identified by a PIDL in the PIDL array.</span></span>


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



<span data-ttu-id="2a054-110">Zusätzlich zur Initialisierung und Verarbeitung der Element Bezeichner-Liste muss Ihre Anwendung die ishellpropsheetext:: replacepage-Methode implementieren und die entsprechenden Ersatz Handler einfügen.</span><span class="sxs-lookup"><span data-stu-id="2a054-110">In addition to the initialization and processing of the item identifier list, your application will need to implement the IShellPropSheetExt::ReplacePage method and insert the appropriate replacement handlers.</span></span> <span data-ttu-id="2a054-111">Diese Methode wird von der Windows-Shell jedes Mal aufgerufen, wenn ein ersetzbares Eigenschaften Blatt angezeigt wird. Dadurch erhält die Anwendung die Möglichkeit, einen entsprechenden Ersatz Handler aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2a054-111">The Windows Shell calls this method each time it is about to display a replaceable property sheet, giving your application a chance to invoke a corresponding replacement handler.</span></span> <span data-ttu-id="2a054-112">Das niedrige Wort des ersten Parameters für die replacepage-Methode ist ein Bezeichner für das angegebene Eigenschaften Blatt, das in Windows angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2a054-112">The low word of the first parameter to the ReplacePage method is an identifier for the given property sheet that Windows is about to display.</span></span> <span data-ttu-id="2a054-113">Die Werte, die im unteren Wort des ersten Parameters übergeben werden, entsprechen den Werten, die in der Datei "wpdshellextension. h" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2a054-113">The values passed in the low word of the first parameter correspond to values defined in the file WpdShellExtension.h.</span></span> <span data-ttu-id="2a054-114">Diese Werte und ihre Beschreibungen werden in der folgenden Tabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a054-114">These values and their descriptions appear in the following table.</span></span>



| <span data-ttu-id="2a054-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2a054-115">Value</span></span>                                  | <span data-ttu-id="2a054-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a054-116">Description</span></span>                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="2a054-117">wpdnse- \_ propsheet- \_ Gerät \_ Allgemein</span><span class="sxs-lookup"><span data-stu-id="2a054-117">WPDNSE\_PROPSHEET\_DEVICE\_GENERAL</span></span>     | <span data-ttu-id="2a054-118">Entspricht der Registerkarte Allgemein für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="2a054-118">Corresponds to the general tab for the device.</span></span>                              |
| <span data-ttu-id="2a054-119">wpdnse- \_ propsheet- \_ Speicher ( \_ Allgemein)</span><span class="sxs-lookup"><span data-stu-id="2a054-119">WPDNSE\_PROPSHEET\_STORAGE\_GENERAL</span></span>    | <span data-ttu-id="2a054-120">Entspricht der Registerkarte Allgemein für ein Speicher Objekt, das sich auf dem Gerät befindet.</span><span class="sxs-lookup"><span data-stu-id="2a054-120">Corresponds to the general tab for a storage object found on the device.</span></span>    |
| <span data-ttu-id="2a054-121">wpdnse- \_ propsheet- \_ Inhalt \_ Allgemein</span><span class="sxs-lookup"><span data-stu-id="2a054-121">WPDNSE\_PROPSHEET\_CONTENT\_GENERAL</span></span>    | <span data-ttu-id="2a054-122">Entspricht der Registerkarte Allgemein für das Inhalts Objekt, das auf dem Gerät gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="2a054-122">Corresponds to the general tab for content object found on the device.</span></span>      |
| <span data-ttu-id="2a054-123">Verweise auf wpdnse- \_ propsheet- \_ Inhalte \_</span><span class="sxs-lookup"><span data-stu-id="2a054-123">WPDNSE\_PROPSHEET\_CONTENT\_REFERENCES</span></span> | <span data-ttu-id="2a054-124">Entspricht der Registerkarte Verweise für ein Inhalts Objekt, das sich auf dem Gerät befindet.</span><span class="sxs-lookup"><span data-stu-id="2a054-124">Corresponds to the references tab for a content object found on the device.</span></span> |
| <span data-ttu-id="2a054-125">wpdnse- \_ propsheet- \_ Inhalts \_ Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2a054-125">WPDNSE\_PROPSHEET\_CONTENT\_RESOURCES</span></span>  | <span data-ttu-id="2a054-126">Entspricht der Registerkarte Ressourcen für ein Inhalts Objekt, das sich auf dem Gerät befindet.</span><span class="sxs-lookup"><span data-stu-id="2a054-126">Corresponds to the resources tab for a content object found on the device.</span></span>  |
| <span data-ttu-id="2a054-127">Details zum wpdnse- \_ propsheet- \_ Inhalt \_</span><span class="sxs-lookup"><span data-stu-id="2a054-127">WPDNSE\_PROPSHEET\_CONTENT\_DETAILS</span></span>    | <span data-ttu-id="2a054-128">Entspricht einer Registerkarte "Details" für ein Inhalts Objekt, das sich auf dem Gerät befindet.</span><span class="sxs-lookup"><span data-stu-id="2a054-128">Corresponds to a details tab for a content object found on the device.</span></span>      |



 

<span data-ttu-id="2a054-129">In der Beispiel-Eigenschaften Blatt Erweiterung ruft die replacepage-Methode zwei Ersatz Handler auf: \_ replacedevicegeneral und \_ replacecontentreferences.</span><span class="sxs-lookup"><span data-stu-id="2a054-129">In the sample property sheet extension, the ReplacePage method invokes two replacement handlers: \_ReplaceDeviceGeneral and \_ReplaceContentReferences.</span></span> <span data-ttu-id="2a054-130">Diese Handler ersetzen die Registerkarten Allgemeines Gerät und Inhalts Verweise in den Extensible-Eigenschaften Blättern.</span><span class="sxs-lookup"><span data-stu-id="2a054-130">These handlers replace the general device and the content references tabs in the extensible property sheets.</span></span>


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



<span data-ttu-id="2a054-131">Da ein Benutzer mehrere Geräte auswählen kann, muss eine Anwendung das von ishellextinit:: Initialize zurückgegebene PIDL-Array speichern und dann das hohe Wort des ersten Parameters auf replacepage überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2a054-131">Because it is possible for a user to select multiple devices, an application will need to save the PIDL array returned by IShellExtInit::Initialize and then examine the high word of the first parameter to ReplacePage.</span></span> <span data-ttu-id="2a054-132">Der Wert 0 (null) in diesem hohen Wort entspricht dem ersten Element im PIDL-Array, wobei der Wert 1 dem zweiten Element entspricht usw.</span><span class="sxs-lookup"><span data-stu-id="2a054-132">A value of zero in this high word corresponds to the first element in the PIDL array, a value of one corresponds to the second element, and so on.</span></span> <span data-ttu-id="2a054-133">In der replacepage-Funktion der Beispielanwendung wird dieser Wert für das hohe Wort an beide Austausch Handler weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="2a054-133">In the sample application's ReplacePage function, this high word value is passed to both replacement handlers.</span></span> <span data-ttu-id="2a054-134">Diese Handler verwenden diesen Wert wiederum, um ein bestimmtes Gerät zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2a054-134">These handlers, in turn, use this value to identify a particular device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a054-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2a054-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a054-136">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="2a054-136">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



