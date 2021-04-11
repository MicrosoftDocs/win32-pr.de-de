---
title: Online Druck-Assistent
description: Der Windows Vista-Online Druck-Assistent unterstützt Benutzer beim Sortieren von Fotos aus teilnehmenden Online Druck-Einzelhandels Händlern.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Online Druck-Assistent
- Symbole, Online Druck-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8536eea7a51eddb2dbb46d10c9291a60edfdc74e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315093"
---
# <a name="online-printing-wizard"></a><span data-ttu-id="ee570-105">Online Druck-Assistent</span><span class="sxs-lookup"><span data-stu-id="ee570-105">Online Printing Wizard</span></span>

<span data-ttu-id="ee570-106">Der Windows Vista-Online Druck-Assistent unterstützt Benutzer beim Sortieren von Fotos aus teilnehmenden Online Druck-Einzelhandels Händlern.</span><span class="sxs-lookup"><span data-stu-id="ee570-106">The Windows Vista Online Printing Wizard helps users order prints of photos from participating online printing retailers.</span></span> <span data-ttu-id="ee570-107">Dieser Assistent ist so konzipiert, dass er Programm gesteuert von jeder Anwendung aufgerufen werden kann, die Benutzern die Möglichkeit bietet, Fotos von Fotos zu bestellen.</span><span class="sxs-lookup"><span data-stu-id="ee570-107">This wizard is designed so that it can be invoked programmatically by any application that wants to offer users the ability to order prints of photos.</span></span> <span data-ttu-id="ee570-108">Der Fotodruck-Assistent ist unter Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ee570-108">The Photo Printing Wizard is available on Windows Vista.</span></span> <span data-ttu-id="ee570-109">Pix für Windows</span><span class="sxs-lookup"><span data-stu-id="ee570-109">PIX for Windows</span></span>

-   [<span data-ttu-id="ee570-110">Vom Online Druck-Assistenten bereitgestellte Funktionen</span><span class="sxs-lookup"><span data-stu-id="ee570-110">Features Provided by the Online Print Wizard</span></span>](#features-provided-by-the-online-print-wizard)
-   [<span data-ttu-id="ee570-111">Unterstützte Foto Dateiformate</span><span class="sxs-lookup"><span data-stu-id="ee570-111">Supported Photo File Formats</span></span>](#supported-photo-file-formats)
-   [<span data-ttu-id="ee570-112">Programm gesteuertes Starten des Online Druck-Assistenten</span><span class="sxs-lookup"><span data-stu-id="ee570-112">Programmatically Launching the Online Print Wizard</span></span>](#programmatically-launching-the-online-print-wizard)
-   [<span data-ttu-id="ee570-113">Zugreifen auf das Symbol für den Online Druck-Assistenten</span><span class="sxs-lookup"><span data-stu-id="ee570-113">Accessing the Online Print Wizard Icon</span></span>](#accessing-the-online-print-wizard-icon)
-   [<span data-ttu-id="ee570-114">MRU-Eigenschaften des Online Druck-Assistenten</span><span class="sxs-lookup"><span data-stu-id="ee570-114">Online Print Wizard MRU Properties</span></span>](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a><span data-ttu-id="ee570-115">Vom Online Druck-Assistenten bereitgestellte Funktionen</span><span class="sxs-lookup"><span data-stu-id="ee570-115">Features Provided by the Online Print Wizard</span></span>

<span data-ttu-id="ee570-116">Der Windows Vista-Online Druck-Assistent ermöglicht Benutzern das Sortieren von Druck Vorgängen aus einer Auswahl von teilnehmenden Online Druck-Einzelhandels Händlern.</span><span class="sxs-lookup"><span data-stu-id="ee570-116">The Windows Vista Online Printing Wizard enables users to order prints from a selection of participating online printing retailers.</span></span> <span data-ttu-id="ee570-117">Wenn der Assistent aufgerufen wird, wird Folgendes ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="ee570-117">When invoked, the wizard:</span></span>

1.  <span data-ttu-id="ee570-118">Akzeptiert eine Datei oder eine Liste von Dateien, für die gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ee570-118">Accepts a file or list of files for which prints are to be ordered.</span></span>
2.  <span data-ttu-id="ee570-119">Ruft automatisch die aktuelle Liste der teilnehmenden Online Druck Händler ab und ermöglicht dem Benutzer, den Einzelhändler auszuwählen, von dem die Foto Abdrücke gekauft werden.</span><span class="sxs-lookup"><span data-stu-id="ee570-119">Automatically retrieves the current list of participating online printing retailers, and enables the user to select the retailer from which to purchase the photo prints.</span></span>
3.  <span data-ttu-id="ee570-120">Führt den Benutzer durch den Prozess oder die Reihenfolge der Ausdrucke.</span><span class="sxs-lookup"><span data-stu-id="ee570-120">Guides the user through the process or ordering prints.</span></span>

<span data-ttu-id="ee570-121">Jede Anwendung kann von den Funktionen profitieren, die vom Windows Vista-Online Druck-Assistenten angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="ee570-121">Any application can benefit from the features offered by the Windows Vista Online Printing Wizard.</span></span> <span data-ttu-id="ee570-122">Eine Anwendung muss nur die Datei oder Dateien übergeben, für die gedruckt werden, und der Assistent führt den Benutzer durch den Bestellvorgang.</span><span class="sxs-lookup"><span data-stu-id="ee570-122">An application need only pass in the file or files for which prints will be ordered, and the wizard guides the user through the ordering process.</span></span>

<span data-ttu-id="ee570-123">Die folgende Abbildung zeigt den Windows Vista-Online Druck-Assistenten, der eine Beispielliste der teilnehmenden Online Druck-Einzelhändler anzeigt.</span><span class="sxs-lookup"><span data-stu-id="ee570-123">The following figure shows the Windows Vista Online Printing Wizard displaying an example list of participating online printing retailers.</span></span>

![der Windows Vista-Online Druck-Assistent](images/opw.png)

## <a name="supported-photo-file-formats"></a><span data-ttu-id="ee570-125">Unterstützte Foto Dateiformate</span><span class="sxs-lookup"><span data-stu-id="ee570-125">Supported Photo File Formats</span></span>

<span data-ttu-id="ee570-126">Der Windows Vista-Online Druck-Assistent unterstützt alle Bild Dateiformate, für die ein WIC-Codec (Windows Imaging Component) installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ee570-126">The Windows Vista Online Printing Wizard supports any image file format for which a Windows Imaging Component (WIC) codec is installed.</span></span> <span data-ttu-id="ee570-127">WIC bietet mehrere Standard-Codecs, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="ee570-127">WIC provides several standard codecs, including:</span></span>

-   <span data-ttu-id="ee570-128">Bitmap (BMP)</span><span class="sxs-lookup"><span data-stu-id="ee570-128">Bitmap (BMP)</span></span>
-   <span data-ttu-id="ee570-129">GIF (Graphics Interchange Format)</span><span class="sxs-lookup"><span data-stu-id="ee570-129">Graphics Interchange Format (GIF)</span></span>
-   <span data-ttu-id="ee570-130">Symbol Format (ICO)</span><span class="sxs-lookup"><span data-stu-id="ee570-130">Icon Format (ICO)</span></span>
-   <span data-ttu-id="ee570-131">JPEG (Joint Photographic Experts Group)</span><span class="sxs-lookup"><span data-stu-id="ee570-131">Joint Photographic Experts Group (JPEG)</span></span>
-   <span data-ttu-id="ee570-132">PNG (Portable Network Graphics)</span><span class="sxs-lookup"><span data-stu-id="ee570-132">Portable Network Graphics (PNG)</span></span>
-   <span data-ttu-id="ee570-133">TIFF (Tagged Image File Format)</span><span class="sxs-lookup"><span data-stu-id="ee570-133">Tagged Image File Format (TIFF)</span></span>
-   <span data-ttu-id="ee570-134">Windows Media-Fotoformat</span><span class="sxs-lookup"><span data-stu-id="ee570-134">Windows Media Photo format</span></span>

<span data-ttu-id="ee570-135">Weitere Informationen zu WIC-und WIC-Codecs finden Sie unter [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="ee570-135">For more information about WIC and WIC codecs, see [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).</span></span>

<span data-ttu-id="ee570-136">Dateiformate, die von Online Druck-Einzelhändlern unterstützt werden, variieren je nach Einzelhändler möglicherweise unterstützt ein bestimmter Einzelhändler nicht alle Dateiformate, die vom Windows Vista-Online Druck-Assistenten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ee570-136">File formats supported by online printing retailers vary from retailer to retailer; it is possible that a particular retailer may not support all of the file formats supported by the Windows Vista Online Printing Wizard.</span></span> <span data-ttu-id="ee570-137">Wenn der Benutzer versucht, Druck in einem Format zu sortieren, das vom ausgewählten Einzelhändler nicht unterstützt wird, benachrichtigt der Windows Vista-Online Druck-Assistent den Benutzer, dass der ausgewählte Einzelhändler das Format der übermittelten Dateien nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ee570-137">If the user attempts to order prints in a format that is not supported by the selected retailer, the Windows Vista Online Printing Wizard notifies the user that the selected retailer does not support the submitted file format.</span></span>

## <a name="programmatically-launching-the-online-print-wizard"></a><span data-ttu-id="ee570-138">Programm gesteuertes Starten des Online Druck-Assistenten</span><span class="sxs-lookup"><span data-stu-id="ee570-138">Programmatically Launching the Online Print Wizard</span></span>

<span data-ttu-id="ee570-139">Um den Windows Vista-Online Druck-Assistenten aufzurufen, rufen Sie die [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle mit der folgenden Klassen Kennung (CLSID) auf:</span><span class="sxs-lookup"><span data-stu-id="ee570-139">To invoke the Windows Vista Online Printing Wizard, call the [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface with the following class identifier (CLSID):</span></span>


```
CLSID_PublishDropTarget
```



<span data-ttu-id="ee570-140">Diese CLSID ist in "shobjidl. h" und "shobjidl. idl" definiert.</span><span class="sxs-lookup"><span data-stu-id="ee570-140">This CLSID is defined in Shobjidl.h and Shobjidl.idl.</span></span> <span data-ttu-id="ee570-141">Die Dateien, die vom Windows Vista-Online Druck-Assistenten verarbeitet werden sollen, werden in einem [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) -Objekt angegeben.</span><span class="sxs-lookup"><span data-stu-id="ee570-141">The files to be processed by the Windows Vista Online Printing Wizard are specified in an [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) object.</span></span>

<span data-ttu-id="ee570-142">Im folgenden Codebeispiel wird veranschaulicht, wie der Windows Vista-Online Druck-Assistent aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ee570-142">The following code example demonstrates how to invoke the Windows Vista Online Printing Wizard.</span></span>


```
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PublishDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



## <a name="accessing-the-online-print-wizard-icon"></a><span data-ttu-id="ee570-143">Zugreifen auf das Symbol für den Online Druck-Assistenten</span><span class="sxs-lookup"><span data-stu-id="ee570-143">Accessing the Online Print Wizard Icon</span></span>

<span data-ttu-id="ee570-144">Der Windows Vista-Online Druck-Assistent exportiert ein Symbol, auf das zugegriffen werden kann und das von Anwendungen angezeigt wird, die es aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ee570-144">The Windows Vista Online Printing Wizard exports an icon that can be accessed and displayed by applications which call it.</span></span> <span data-ttu-id="ee570-145">In der folgenden Abbildung ist das Symbol für den Windows Vista-Online Druck-Assistenten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ee570-145">The following figure shows the Windows Vista Online Printing Wizard icon.</span></span>

![Symbol für den Windows Vista-Online Druck-Assistenten](images/opw-icon.png)

<span data-ttu-id="ee570-147">Im folgenden Codebeispiel wird veranschaulicht, wie der Index für das Windows Vista-Online Druck-Assistenten Symbol abgerufen wird, indem die **opwicon** -Eigenschaft gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="ee570-147">The following code example demonstrates how to retrieve the index for the Windows Vista Online Printing Wizard icon by reading the **OPWIcon** property.</span></span>


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;

spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

// Read the icon index from the properties set. 
CComVariant vtIcon;
int nIndex;
hr = spPropsBag->Read(L"OPWIcon", &vtIcon, NULL);

if SUCCEEDED(hr)
{
    nIndex = vtIcon.lVal;
}
```



## <a name="online-print-wizard-mru-properties"></a><span data-ttu-id="ee570-148">MRU-Eigenschaften des Online Druck-Assistenten</span><span class="sxs-lookup"><span data-stu-id="ee570-148">Online Print Wizard MRU Properties</span></span>

<span data-ttu-id="ee570-149">Der Windows Vista-Online Druck-Assistent definiert drei Eigenschaften, die mit dem zuletzt verwendeten (MRU) Online Druck-Einzelhändler verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="ee570-149">The Windows Vista Online Printing Wizard defines three properties that are related to the most recently used (MRU) online printing retailer.</span></span>



| <span data-ttu-id="ee570-150">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="ee570-150">Property Name</span></span> | <span data-ttu-id="ee570-151">Eigenschafts Wert/-Funktion</span><span class="sxs-lookup"><span data-stu-id="ee570-151">Property Value/Function</span></span>                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee570-152">**Mruicon**</span><span class="sxs-lookup"><span data-stu-id="ee570-152">**MRUIcon**</span></span>   | <span data-ttu-id="ee570-153">Der Index des Symbols für den zuletzt verwendeten Online Druck-Einzelhändler kann aus dieser Eigenschaft gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="ee570-153">The index of the icon for the most recently used online printing retailer can be read from this property.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="ee570-154">**Mruname**</span><span class="sxs-lookup"><span data-stu-id="ee570-154">**MRUName**</span></span>   | <span data-ttu-id="ee570-155">Der Name des zuletzt verwendeten Online Druck-Einzelhandels Händlers kann aus dieser Eigenschaft gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="ee570-155">The name of the most recently used online printing retailer can be read from this property.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="ee570-156">**Usemru**</span><span class="sxs-lookup"><span data-stu-id="ee570-156">**UseMRU**</span></span>    | <span data-ttu-id="ee570-157">Ein **variabler** **VT- \_ boolescher** Wert, der angibt, ob der Assistent die Auswahl Seite für den Online Druck-Einzelhandel überspringen soll, und stattdessen nur den zuletzt verwendeten Online Druck Händler verwenden.</span><span class="sxs-lookup"><span data-stu-id="ee570-157">A **VARIANT** **VT\_BOOL** value indicating whether the wizard should skip the online printing retailer selection page, and just use the most recently used online printing retailer instead.</span></span> <span data-ttu-id="ee570-158">Legen Sie diese Eigenschaft auf **Variant \_ true** fest, um die Auswahl Seite für den Händler zu überspringen</span><span class="sxs-lookup"><span data-stu-id="ee570-158">Set this property to **VARIANT\_TRUE** to skip the retailer selection page.</span></span> |



 

<span data-ttu-id="ee570-159">Im folgenden Codebeispiel wird veranschaulicht, wie die usemru-Eigenschaft festgelegt wird, sodass der Windows Vista-Online Druck-Assistent die Auswahl Seite für den Online Druck-Einzelhandel umgeht und automatisch den zuletzt verwendeten Einzelhändler auswählt.</span><span class="sxs-lookup"><span data-stu-id="ee570-159">The following code example demonstrates how to set the UseMRU property so the Windows Vista Online Printing Wizard bypasses the online printing retailer selection page and automatically selects the most recently used retailer.</span></span>


```
// A data object that contains the list of photos to order prints for.
IDataObject* pDataObject;

// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Set the UserMRU property to true to skip retailer selection and use 
// the MRU retailer instead.    
CComQIPtr<IPropertyBag> spPropsBag(spDropTarget);
if(spPropsBag) 
{
    VARIANT varTrue = {0};
    varTrue.vt = VT_BOOL;
    varTrue.boolVal = VARIANT_TRUE;
    spPropsBag->Write(L"UseMRU", &varTrue);
}

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);
```



<span data-ttu-id="ee570-160">Im folgenden Codebeispiel wird veranschaulicht, wie die Eigenschaften mruname und mruicon gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="ee570-160">The following code example demonstrates how to read the MRUName and MRUIcon properties.</span></span>


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;
spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

CComVariant vtMRUName, vtMRUIconIndex;
CComBSTR bstrMRUName;
int nMRUIconIndex;

// Get the MRU name value.
hr = spPropsBag->Read(L"MRUName", &vtMRUName, NULL);
if SUCCEEDED(hr) 
{
    bstrMRUName = vtMRUName.bstrVal;
}

// Get the MRU icon index value.
hr = spPropsBag->Read(L"MRUIcon", &vtMRUIconIndex, NULL);
if SUCCEEDED(hr)
{
    nMRUIconIndex = vtMRUIconIndex.lVal;
}
```



 

 