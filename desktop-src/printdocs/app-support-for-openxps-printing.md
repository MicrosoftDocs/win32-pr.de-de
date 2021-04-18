---
description: Openxps ist das Open XML Paper Specification-Format für Dokumente, das auf der Standardspezifikation der Europäischen Verpackungshersteller (ECMA) basiert.
ms.assetid: 52FB5B3F-BEBF-4851-8BE9-5DC7AE535313
title: App-Unterstützung für openxps-Druck
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914d8c365209ea3486bedd5e0352e63a8e31086f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351658"
---
# <a name="app-support-for-openxps-printing"></a><span data-ttu-id="97b99-103">App-Unterstützung für openxps-Druck</span><span class="sxs-lookup"><span data-stu-id="97b99-103">App Support for OpenXPS Printing</span></span>

<span data-ttu-id="97b99-104">Openxps ist das Open XML Paper Specification-Format für Dokumente, das auf der Standardspezifikation der Europäischen Computer Hersteller Zuordnungen (ECMA) basiert.</span><span class="sxs-lookup"><span data-stu-id="97b99-104">OpenXPS is the Open XML Paper Specification format for documents, and it’s based on the European Computer Manufacturers Association (ECMA) standard specification.</span></span>

<span data-ttu-id="97b99-105">Windows 8 bietet vollständige Unterstützung für den openxps-Druck über das V4-Druckertreiber Modell, parallel mit der kontinuierlichen Unterstützung für das Microsoft XPS-Format.</span><span class="sxs-lookup"><span data-stu-id="97b99-105">Windows 8 provides full support for OpenXPS printing via the v4 print driver model, side-by-side with continued support for the Microsoft XPS format.</span></span> <span data-ttu-id="97b99-106">Dieses Thema konzentriert sich auf den Teil dieser Unterstützung, der für Entwickler von Windows-Anwendungen relevant ist.</span><span class="sxs-lookup"><span data-stu-id="97b99-106">And this topic focuses on the portion of this support that is relevant to Windows application developers.</span></span> <span data-ttu-id="97b99-107">Informationen zu den Treiber Anforderungen für openxps-Unterstützung finden Sie unter [Treiberunterstützung für openxps](/windows-hardware/drivers/print/printer-driver-overview).</span><span class="sxs-lookup"><span data-stu-id="97b99-107">For information about driver requirements for OpenXPS support, see [Driver Support for OpenXPS](/windows-hardware/drivers/print/printer-driver-overview).</span></span>

## <a name="sending-xps-data-to-the-print-system"></a><span data-ttu-id="97b99-108">Senden von XPS-Daten an das Druck System</span><span class="sxs-lookup"><span data-stu-id="97b99-108">Sending XPS data to the Print System</span></span>

<span data-ttu-id="97b99-109">Es wird empfohlen, dass Sie [**iprintdocumentpackagetarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) verwenden, um alle XPS-Druckaufträge an das Drucksystem zu senden.</span><span class="sxs-lookup"><span data-stu-id="97b99-109">We recommend that you use [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) for sending all XPS print jobs to the print system.</span></span> <span data-ttu-id="97b99-110">**Iprintdocumentpackagetarget** akzeptiert das XPS-Objektmodell (OM) ohne Serialisierung und trägt so zur Verbesserung der Gesamtleistung bei.</span><span class="sxs-lookup"><span data-stu-id="97b99-110">**IPrintDocumentPackageTarget** accepts the XPS object model (OM) without serialization, and that helps to improve the overall performance.</span></span>

<span data-ttu-id="97b99-111">Im folgenden finden Sie eine kurze Zusammenfassung der **iprintdocumentpackagetarget** -Schnittstelle:</span><span class="sxs-lookup"><span data-stu-id="97b99-111">Here's a brief summary of the **IPrintDocumentPackageTarget** interface:</span></span>

-   <span data-ttu-id="97b99-112">Diese Schnittstelle unterstützt das Drucken aus angepassten Lösungen und Desktop Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="97b99-112">This interface supports printing from tailored solutions as well as desktop applications.</span></span>

-   <span data-ttu-id="97b99-113">Bei Desktops-apps kann dies anstelle von [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97b99-113">For desktops apps, this can be used in place of [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).</span></span>

-   <span data-ttu-id="97b99-114">Verfügbar unter Windows 7 mit Service Pack 1 (SP1) + Platt Form Update und Windows 8.</span><span class="sxs-lookup"><span data-stu-id="97b99-114">Available on Windows 7 with Service Pack 1 (SP1) + Platform Update, and Windows 8.</span></span>

-   <span data-ttu-id="97b99-115">Fügen Sie " *documenttarget. h* " in Projekte ein, um diese APIs zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="97b99-115">Include *DocumentTarget.h* in projects to use these APIs.</span></span>

<span data-ttu-id="97b99-116">Anwendungen, die openxps-Dokumente verwenden, sollten beachten, dass der MIME-Typ für openxps wie folgt aussieht:</span><span class="sxs-lookup"><span data-stu-id="97b99-116">Applications that consume OpenXPS documents should note that the MIME type for OpenXPS is as follows:</span></span>

<dl> <span data-ttu-id="97b99-117">Anwendungs- \\ oxps</span><span class="sxs-lookup"><span data-stu-id="97b99-117">application\\oxps</span></span>  
</dl>

## <a name="sending-openxps-data-to-the-xps-print-api"></a><span data-ttu-id="97b99-118">Senden von openxps-Daten an die XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="97b99-118">Sending OpenXPS data to the XPS Print API</span></span>

<span data-ttu-id="97b99-119">Für openxps-spezifisch akzeptiert XPS OM sowohl msxps als auch openxps und stellt Methoden für die Konvertierung und Serialisierung in beide Formate bereit.</span><span class="sxs-lookup"><span data-stu-id="97b99-119">Specific to OpenXPS, XPS OM accepts both MSXPS and OpenXPS, and provides methods for conversion and serialization to either format.</span></span> <span data-ttu-id="97b99-120">Dies ermöglicht es Anwendungsentwicklern, bei Bedarf agnostisch des Ziel Treibers zu sein.</span><span class="sxs-lookup"><span data-stu-id="97b99-120">This allows application developers to be agnostic of the target driver, if they want.</span></span> <span data-ttu-id="97b99-121">Dies bedeutet auch, dass App-Entwickler immer Druckaufträge als XPS OM an entweder StartXpsPrintJob1 oder idocumentpackagetarget übermitteln können und dabei wissen, dass das Drucksystem jede erforderliche Konvertierung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="97b99-121">This also means that app developers can always submit print jobs as XPS OM to either StartXpsPrintJob1 or IDocumentPackageTarget, knowing that the print system will handle any necessary conversion.</span></span>

<span data-ttu-id="97b99-122">Natürlich wird durch das verhindern der Konvertierung zwischen XPS-Formaten die End-to-End-Leistung verbessert.</span><span class="sxs-lookup"><span data-stu-id="97b99-122">Of course, preventing conversion between XPS formats will improve end-to-end performance.</span></span> <span data-ttu-id="97b99-123">Der Entwickler kann den folgenden Registrierungsschlüssel aus der Anwendung überprüfen, um das bevorzugte XPS-Format des Ziel Druckertreibers zu ermitteln:</span><span class="sxs-lookup"><span data-stu-id="97b99-123">From the application, the developer can check the following registry key to determine the preferred XPS format of the targeted print driver:</span></span>

``` syntax
HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Print\Printers\[PrintDriverName]\PrintDriverData\XpsFormat
```

<span data-ttu-id="97b99-124">Sobald das bevorzugte XPS-Format festgelegt wurde, kann die Anwendung XPS OM-Objekte bereitstellen, für die keine Konvertierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="97b99-124">Once the preferred XPS format has been determined, the application can provide XPS OM objects that will not require conversion.</span></span> <span data-ttu-id="97b99-125">Besonders Hinweis ist die Verwendung von HD-Foto in msxps und jpeer-XR in openxps.</span><span class="sxs-lookup"><span data-stu-id="97b99-125">Of particular note is the use of HD Photo in MSXPS and JPEGXR in OpenXPS.</span></span> <span data-ttu-id="97b99-126">Die Konvertierung von jpgxr in HD Photo ist relativ einfach, da der Hauptunterschied in dieser Konvertierung darin besteht, dass das HD-Foto vier Steuerungs Bits ignoriert, die von jpeer GXR benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="97b99-126">Converting from JPEGXR to HD Photo is relatively lightweight since the primary difference in this conversion is that HD Photo ignores 4 control bits that JPEGXR requires.</span></span> <span data-ttu-id="97b99-127">Allerdings muss bei der Umstellung von HD-Fotos in jpgxr das gesamte Bild erneut codiert werden, um die erforderlichen Steuerungs Bits zu generieren.</span><span class="sxs-lookup"><span data-stu-id="97b99-127">However, converting from HD Photo to JPEGXR requires the entire image to be re-encoded in order to generate the required control bits.</span></span> <span data-ttu-id="97b99-128">Dadurch wird die Kompatibilität mit openxps durch das Bereitstellen von jpeer-XR-Images für hochauflösende Images sichergestellt, und die Konvertierungs Kosten des Images für msxps werden minimiert.</span><span class="sxs-lookup"><span data-stu-id="97b99-128">Thus, providing JPEGXR images for high-resolution images will ensure compatibility with OpenXPS and minimize the conversion cost of the image for MSXPS.</span></span>

<span data-ttu-id="97b99-129">Der *xpsobjectmodel \_ 1. h* -Header definiert die zusätzlichen APIs und Objekte für openxps.</span><span class="sxs-lookup"><span data-stu-id="97b99-129">The *Xpsobjectmodel\_1.h* header defines the additional APIs and objects for OpenXPS.</span></span> <span data-ttu-id="97b99-130">Und die IXpsOMObjectFactory1-Schnittstelle stellt zusätzliche Methoden für die Bild Konvertierung bereit.</span><span class="sxs-lookup"><span data-stu-id="97b99-130">And the IXpsOMObjectFactory1 interface provides additional methods for image conversion.</span></span> <span data-ttu-id="97b99-131">Hier ist die Syntax:</span><span class="sxs-lookup"><span data-stu-id="97b99-131">Here's the syntax:</span></span>


```C++
IXpsOMObjectFactory1->ConvertHDPhotoToJpegXR(IXpsOMImageResource *imageResource);

IXpsOMObjectFactory1->ConvertJpegXRToHDPhoto(IXpsOMImageResource *imageResource);
```



<span data-ttu-id="97b99-132">Windows 8 bietet die folgenden neuen und aktualisierten Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="97b99-132">Windows 8 provides the following new and updated enumerations.</span></span>

<span data-ttu-id="97b99-133">Neue Enumeration:</span><span class="sxs-lookup"><span data-stu-id="97b99-133">New enumeration:</span></span>

<dl>

[<span data-ttu-id="97b99-134">**XPS \_ - \_ Dokumenttyp**</span><span class="sxs-lookup"><span data-stu-id="97b99-134">**XPS\_DOCUMENT\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)  
</dl>

<span data-ttu-id="97b99-135">Aktualisierte Enumeration</span><span class="sxs-lookup"><span data-stu-id="97b99-135">Updated enumeration</span></span>

<dl>

[<span data-ttu-id="97b99-136">**XPS \_ - \_ Bildtyp**</span><span class="sxs-lookup"><span data-stu-id="97b99-136">**XPS\_IMAGE\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)  
</dl>

<span data-ttu-id="97b99-137">Die neuen GetDocumentType-Methoden ermöglichen es einer Anwendung, das XPS-Format von Dokumenten zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="97b99-137">The new GetDocumentType methods allow an application to determine the XPS format of documents.</span></span> <span data-ttu-id="97b99-138">Diese sind in [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1)und [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="97b99-138">These are available in [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1), and [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1).</span></span> <span data-ttu-id="97b99-139">Im folgenden finden Sie eine Liste der Methoden.</span><span class="sxs-lookup"><span data-stu-id="97b99-139">Here's a list of the methods.</span></span>

<dl>

[<span data-ttu-id="97b99-140">**IXpsOMObjectFactory1:: getdocumenttypefromfile**</span><span class="sxs-lookup"><span data-stu-id="97b99-140">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)  
[<span data-ttu-id="97b99-141">**IXpsOMObjectFactory1:: getdocumenttypefromstream**</span><span class="sxs-lookup"><span data-stu-id="97b99-141">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)  
[<span data-ttu-id="97b99-142">**IXpsOMPackage1:: GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="97b99-142">**IXpsOMPackage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)  
[<span data-ttu-id="97b99-143">**IXpsOMPage1:: GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="97b99-143">**IXpsOMPage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)  
</dl>

<span data-ttu-id="97b99-144">Windows 8 bietet die folgenden neuen Fehlercodes für die Unterstützung von openxps:</span><span class="sxs-lookup"><span data-stu-id="97b99-144">Windows 8 provides the following new error codes in support of OpenXPS:</span></span>

<dl> <span data-ttu-id="97b99-145">nicht \_ \_ übereinstimmender XPS- \_ Namespace.</span><span class="sxs-lookup"><span data-stu-id="97b99-145">XPS\_E\_MISMATCHED\_NAMESPACE.</span></span> <dl> <span data-ttu-id="97b99-146">Dieser Fehler wird zurückgegeben, wenn ein nicht übereinstimmender Namespace vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="97b99-146">This error is returned, if there is a mismatched namespace.</span></span>  
</dl> </dd> XPS\_E\_ABSOLUTE\_REFERENCE. <dl> <span data-ttu-id="97b99-147">Dieser Fehler wird zurückgegeben, wenn msxps absolute URIs in internen verweisen verwendet oder versucht, interne Verweise zu verwenden, um im Stream zu serialisieren.</span><span class="sxs-lookup"><span data-stu-id="97b99-147">This error is returned if MSXPS uses absolute URIs in internal references, or attempts to use internal references to serialize in the stream.</span></span> <span data-ttu-id="97b99-148">Dies liegt daran, dass XPS OM relative URIs generiert.</span><span class="sxs-lookup"><span data-stu-id="97b99-148">That is because XPS OM generates relative URIs.</span></span> <span data-ttu-id="97b99-149">Obwohl msxps sowohl relative als auch absolute URIs unterstützt, erfordert openxps relative URIs.</span><span class="sxs-lookup"><span data-stu-id="97b99-149">And although MSXPS supports both relative and absolute URIs, OpenXPS requires relative URIs.</span></span>  
</dl> </dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="97b99-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97b99-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97b99-151">Treiberunterstützung für openxps</span><span class="sxs-lookup"><span data-stu-id="97b99-151">Driver Support for OpenXPS</span></span>](/windows-hardware/drivers/print/printer-driver-overview)
</dt> <dt>

[<span data-ttu-id="97b99-152">**Iprintdocumentpackagetarget**</span><span class="sxs-lookup"><span data-stu-id="97b99-152">**IPrintDocumentPackageTarget**</span></span>](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)
</dt> <dt>

[<span data-ttu-id="97b99-153">**IXpsOMObjectFactory1:: getdocumenttypefromfile**</span><span class="sxs-lookup"><span data-stu-id="97b99-153">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)
</dt> <dt>

[<span data-ttu-id="97b99-154">**IXpsOMObjectFactory1:: getdocumenttypefromstream**</span><span class="sxs-lookup"><span data-stu-id="97b99-154">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)
</dt> <dt>

[<span data-ttu-id="97b99-155">**IXpsOMPackage1:: GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="97b99-155">**IXpsOMPackage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)
</dt> <dt>

[<span data-ttu-id="97b99-156">**IXpsOMPage1:: GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="97b99-156">**IXpsOMPage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)
</dt> <dt>

[<span data-ttu-id="97b99-157">**XPS \_ - \_ Dokumenttyp**</span><span class="sxs-lookup"><span data-stu-id="97b99-157">**XPS\_DOCUMENT\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)
</dt> <dt>

[<span data-ttu-id="97b99-158">**XPS \_ - \_ Bildtyp**</span><span class="sxs-lookup"><span data-stu-id="97b99-158">**XPS\_IMAGE\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)
</dt> </dl>

 

 
