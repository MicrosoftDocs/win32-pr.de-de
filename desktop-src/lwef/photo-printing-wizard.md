---
title: Fotodruck-Assistent
description: Der Fotodruck-Assistent unterstützt Benutzer beim Drucken von Fotos, indem er eine benutzerfreundliche Assistenten Schnittstelle bereitstellt.
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- Fotodruck-Assistent
- IDropTarget, Fotodruck-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708f051f658739cebd08e4f8643e5dd7fc0c6f7f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390293"
---
# <a name="photo-printing-wizard"></a><span data-ttu-id="566fc-105">Fotodruck-Assistent</span><span class="sxs-lookup"><span data-stu-id="566fc-105">Photo Printing Wizard</span></span>

<span data-ttu-id="566fc-106">Der Fotodruck-Assistent unterstützt Benutzer beim Drucken von Fotos, indem er eine benutzerfreundliche Assistenten Schnittstelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="566fc-106">The Photo Printing Wizard helps users print photos by providing an easy-to-use wizard interface.</span></span> <span data-ttu-id="566fc-107">Der Assistent ermöglicht dem Benutzer die Angabe von Foto Druckgrößen und anderen Druckoptionen und sendet die Fotos dann an den Drucker.</span><span class="sxs-lookup"><span data-stu-id="566fc-107">The wizard enables the user to specify photo print sizes and other print options, and then sends the photos to the printer.</span></span> <span data-ttu-id="566fc-108">Der Assistent ist so konzipiert, dass er Programm gesteuert von jeder Anwendung aufgerufen werden kann, die Benutzern die Möglichkeit bietet, Fotos zu drucken und Größen und andere Druckoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="566fc-108">The wizard is designed so that it can be invoked programmatically by any application that wants to offer users the ability to print photos and specify sizing and other print options.</span></span> <span data-ttu-id="566fc-109">Der Fotodruck-Assistent ist unter Windows XP und Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="566fc-109">The Photo Printing Wizard is available on Windows XP and Windows Vista.</span></span>

-   [<span data-ttu-id="566fc-110">Vom Photo Print-Assistenten bereitgestellte Funktionen</span><span class="sxs-lookup"><span data-stu-id="566fc-110">Features Provided by the Photo Print Wizard</span></span>](#features-provided-by-the-photo-print-wizard)
-   [<span data-ttu-id="566fc-111">Unterstützte Foto Dateiformate</span><span class="sxs-lookup"><span data-stu-id="566fc-111">Supported Photo File Formats</span></span>](#supported-photo-file-formats)
-   [<span data-ttu-id="566fc-112">Programm gesteuertes Starten des Foto Druck-Assistenten</span><span class="sxs-lookup"><span data-stu-id="566fc-112">Programmatically Launching the Photo Print Wizard</span></span>](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a><span data-ttu-id="566fc-113">Vom Photo Print-Assistenten bereitgestellte Funktionen</span><span class="sxs-lookup"><span data-stu-id="566fc-113">Features Provided by the Photo Print Wizard</span></span>

<span data-ttu-id="566fc-114">Der Fotodruck-Assistent bietet mehrere Optionen, die möglicherweise nicht in allgemeinen Drucker Dialogfeldern verfügbar sind, wie z. b. Vorlagen mit mehreren Layouts mit exakten Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="566fc-114">The Photo Printing Wizard offers several options that may not be available on common printer dialogs, such as multi-layout templates with accurate dimensions.</span></span> <span data-ttu-id="566fc-115">Mithilfe der Layoutvorlagen können Benutzer den im Papier Druck Papier verfügbaren Speicherplatz optimal nutzen.</span><span class="sxs-lookup"><span data-stu-id="566fc-115">The layout templates enable users to make the most efficient use of the space available on photographic printing paper.</span></span> <span data-ttu-id="566fc-116">Weitere Optionen, die über den Foto Druck-Assistenten angegeben oder darauf zugegriffen werden können, sind:</span><span class="sxs-lookup"><span data-stu-id="566fc-116">Other options that can be specified or accessed through the Photo Print Wizard include:</span></span>

-   <span data-ttu-id="566fc-117">Auswählen eines Druckers aus einer Liste der verfügbaren Drucker oder virtuellen Druck Ziele (z. b. Microsoft XPS Document Writer).</span><span class="sxs-lookup"><span data-stu-id="566fc-117">Selecting a printer from a list of available printers or virtual printing destinations (for example, Microsoft XPS Document Writer).</span></span> <span data-ttu-id="566fc-118">Unter Windows Vista sind möglicherweise die folgenden Optionen verfügbar, abhängig von den Funktionen des Druckers oder des virtuellen Druck Ziels:</span><span class="sxs-lookup"><span data-stu-id="566fc-118">On Windows Vista, the following options may be available, depending on the capabilities of the printer or virtual printing destination:</span></span>
    -   <span data-ttu-id="566fc-119">Papierformat.</span><span class="sxs-lookup"><span data-stu-id="566fc-119">Paper size.</span></span> <span data-ttu-id="566fc-120">Beispiel: "Letter", "Legal", "a3".</span><span class="sxs-lookup"><span data-stu-id="566fc-120">For example, "Letter", "Legal", "A3".</span></span>
    -   <span data-ttu-id="566fc-121">Druckqualität in Bezug auf die unterstützten dpi-Auflösungen (dpi pro Zoll).</span><span class="sxs-lookup"><span data-stu-id="566fc-121">Print quality, in terms of supported dots per inch (dpi) resolutions.</span></span>
    -   <span data-ttu-id="566fc-122">Papiertyp.</span><span class="sxs-lookup"><span data-stu-id="566fc-122">Paper type.</span></span> <span data-ttu-id="566fc-123">Beispiel: "Plain" oder "Glossy".</span><span class="sxs-lookup"><span data-stu-id="566fc-123">For example, "Plain" or "Glossy".</span></span>
-   <span data-ttu-id="566fc-124">Starten der Druckeinstellungen und-Eigenschaften für einen bestimmten Drucker.</span><span class="sxs-lookup"><span data-stu-id="566fc-124">Launching the printing preferences and properties for a particular printer.</span></span>
-   <span data-ttu-id="566fc-125">Festlegen der **Kopien jedes Bilds** (unter Windows Vista) oder der Häufigkeit **, mit der die einzelnen Bild** -Drehfeld Werte (auf Windows XP) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="566fc-125">Setting the **Copies of each picture** (on Windows Vista) or **Number of times to use each picture** (on Windows XP) spin box values.</span></span>
-   <span data-ttu-id="566fc-126">Angeben einer Drucklayoutvorlage.</span><span class="sxs-lookup"><span data-stu-id="566fc-126">Specifying a print layout template.</span></span> <span data-ttu-id="566fc-127">Beispielsweise druckt ein **vollständiges Foto** oder eine **Brieftasche**.</span><span class="sxs-lookup"><span data-stu-id="566fc-127">For example, **Full page photo** or **Wallet prints**.</span></span>
-   <span data-ttu-id="566fc-128">Auswählen der Option **Bild an Frame anpassen** (nur unter Windows Vista verfügbar).</span><span class="sxs-lookup"><span data-stu-id="566fc-128">Selecting the **Fit picture to frame** option (available on Windows Vista only).</span></span>
-   <span data-ttu-id="566fc-129">Anzeigen einer Vorschau auf das gedruckte Foto mit den derzeit angegebenen Optionen.</span><span class="sxs-lookup"><span data-stu-id="566fc-129">Previewing the printed photo with the currently specified options.</span></span>
-   <span data-ttu-id="566fc-130">Zugriffsmöglichkeiten für erweiterte Druckoptionen, z. b. **für die Druck** -und **Farbverwaltung** (nur unter Windows Vista verfügbar).</span><span class="sxs-lookup"><span data-stu-id="566fc-130">Accesssing advanced print options, such as **Sharpen for printing** and **Color management** (available on Windows Vista only).</span></span>

<span data-ttu-id="566fc-131">Jede Anwendung kann von den Funktionen und der Foto Druckfunktion profitieren, die der Fotodruck-Assistent anbietet.</span><span class="sxs-lookup"><span data-stu-id="566fc-131">Any application can benefit from the features and photo printing capability offered by the Photo Printing Wizard.</span></span> <span data-ttu-id="566fc-132">Eine Anwendung kann die zu druckenden Dateien übergeben.</span><span class="sxs-lookup"><span data-stu-id="566fc-132">An application can pass in the files to be printed.</span></span> <span data-ttu-id="566fc-133">Der Fotodruck-Assistent kümmert sich um die Vorbereitung der Datei für den Druck basierend auf den vom Benutzer angegebenen Optionen und sendet die vorbereiteten Dateien an den Drucker.</span><span class="sxs-lookup"><span data-stu-id="566fc-133">The Photo Printing Wizard then takes care of preparing the file for printing based on the options specified by the user and sends the prepared files to the printer.</span></span>

<span data-ttu-id="566fc-134">In der folgenden Abbildung wird die Schnittstelle für den Foto Druck-Assistenten unter Windows Vista angezeigt</span><span class="sxs-lookup"><span data-stu-id="566fc-134">The following figure shows the Photo Printing Wizard interface on Windows Vista</span></span>

![der Foto Druck-Assistent unter Windows Vista](images/ppw-vista.png)

<span data-ttu-id="566fc-136">In der folgenden Abbildung wird die Schnittstelle für den Foto Druck-Assistenten unter Windows XP angezeigt</span><span class="sxs-lookup"><span data-stu-id="566fc-136">The following figure shows the Photo Printing Wizard interface on Windows XP</span></span>

![der Foto Druck-Assistent unter Windows XP](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a><span data-ttu-id="566fc-138">Unterstützte Foto Dateiformate</span><span class="sxs-lookup"><span data-stu-id="566fc-138">Supported Photo File Formats</span></span>

<span data-ttu-id="566fc-139">Unter Windows XP unterstützt der Foto Druck-Assistent alle Grafikdatei Formate, die von Windows GDI+ unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="566fc-139">On Windows XP, the Photo Print Wizard supports all graphics file formats that are supported by Windows GDI+.</span></span> <span data-ttu-id="566fc-140">Derzeit umfassen folgende Dateiformate:</span><span class="sxs-lookup"><span data-stu-id="566fc-140">Currently, these file formats include:</span></span>

-   <span data-ttu-id="566fc-141">Bitmap (BMP)</span><span class="sxs-lookup"><span data-stu-id="566fc-141">Bitmap (BMP)</span></span>
-   <span data-ttu-id="566fc-142">GIF (Graphics Interchange Format)</span><span class="sxs-lookup"><span data-stu-id="566fc-142">Graphics Interchange Format (GIF)</span></span>
-   <span data-ttu-id="566fc-143">JPEG (Joint Photographic Experts Group)</span><span class="sxs-lookup"><span data-stu-id="566fc-143">Joint Photographic Experts Group (JPEG)</span></span>
-   <span data-ttu-id="566fc-144">Austauschbare Bilddatei (EXIF)</span><span class="sxs-lookup"><span data-stu-id="566fc-144">Exchangeable Image File (EXIF)</span></span>
-   <span data-ttu-id="566fc-145">PNG (Portable Network Graphics)</span><span class="sxs-lookup"><span data-stu-id="566fc-145">Portable Network Graphics (PNG)</span></span>
-   <span data-ttu-id="566fc-146">TIFF (Tagged Image File Format)</span><span class="sxs-lookup"><span data-stu-id="566fc-146">Tagged Image File Format (TIFF)</span></span>

<span data-ttu-id="566fc-147">Weitere Informationen zu Grafikdatei Formaten, die von GDI+ unterstützt werden, finden Sie unter [Typen von Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md).</span><span class="sxs-lookup"><span data-stu-id="566fc-147">For more information about graphics file formats supported by GDI+, see [Types of Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md).</span></span>

<span data-ttu-id="566fc-148">Unter Windows Vista unterstützt der Foto Druck-Assistent alle Bild Dateiformate, für die ein Windows Imaging Component (WIC)-Codec installiert ist.</span><span class="sxs-lookup"><span data-stu-id="566fc-148">On Windows Vista, the Photo Print Wizard supports any image file format for which a Windows Imaging Component (WIC) codec is installed.</span></span> <span data-ttu-id="566fc-149">WIC bietet mehrere Standard-Codecs, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="566fc-149">WIC provides several standard codecs, including:</span></span>

-   <span data-ttu-id="566fc-150">Bitmap (BMP)</span><span class="sxs-lookup"><span data-stu-id="566fc-150">Bitmap (BMP)</span></span>
-   <span data-ttu-id="566fc-151">GIF</span><span class="sxs-lookup"><span data-stu-id="566fc-151">GIF</span></span>
-   <span data-ttu-id="566fc-152">Symbol Format (ICO)</span><span class="sxs-lookup"><span data-stu-id="566fc-152">Icon Format (ICO)</span></span>
-   <span data-ttu-id="566fc-153">JPEG</span><span class="sxs-lookup"><span data-stu-id="566fc-153">JPEG</span></span>
-   <span data-ttu-id="566fc-154">PNG</span><span class="sxs-lookup"><span data-stu-id="566fc-154">PNG</span></span>
-   <span data-ttu-id="566fc-155">TIFF</span><span class="sxs-lookup"><span data-stu-id="566fc-155">TIFF</span></span>
-   <span data-ttu-id="566fc-156">Windows Media-Fotoformat</span><span class="sxs-lookup"><span data-stu-id="566fc-156">Windows Media Photo format</span></span>

<span data-ttu-id="566fc-157">Weitere Informationen zu WIC-und WIC-Codecs finden Sie unter [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="566fc-157">For more information about WIC and WIC codecs, see [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)</span></span>

## <a name="programmatically-launching-the-photo-print-wizard"></a><span data-ttu-id="566fc-158">Programm gesteuertes Starten des Foto Druck-Assistenten</span><span class="sxs-lookup"><span data-stu-id="566fc-158">Programmatically Launching the Photo Print Wizard</span></span>

<span data-ttu-id="566fc-159">Um den Fotodruck-Assistenten aufzurufen, rufen Sie die [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle mit der folgenden Klassen Kennung (CLSID) auf:</span><span class="sxs-lookup"><span data-stu-id="566fc-159">To invoke the Photo Printing Wizard, call the [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface with the following class identifier (CLSID):</span></span>


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



<span data-ttu-id="566fc-160">Die Dateien, die vom Fotodruck-Assistenten verarbeitet werden sollen, werden in einem [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) -Objekt angegeben.</span><span class="sxs-lookup"><span data-stu-id="566fc-160">The files to be processed by the Photo Printing Wizard are specified in an [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) object.</span></span>

<span data-ttu-id="566fc-161">Im folgenden Codebeispiel wird veranschaulicht, wie der Fotodruck-Assistent aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="566fc-161">The following code example demonstrates how to invoke the Photo Printing Wizard.</span></span>


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
            
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PrintPhotosDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



 

 