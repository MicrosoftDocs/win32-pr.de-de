---
description: Mit dem Microsoft XPS Document Writer (MXDW) können Benutzer XPS-Dokument Dateien erstellen, indem Sie Sie aus jeder Windows-Anwendung drucken.
ms.assetid: 1fa50337-2df7-48d3-a179-0ca5ae3dfda3
title: MXDW-Konfigurationseinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4026a99baa33ec50bc3ad129ef6610a428f83ab
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106366382"
---
# <a name="mxdw-configuration-settings"></a><span data-ttu-id="c2017-103">MXDW-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="c2017-103">MXDW Configuration Settings</span></span>

<span data-ttu-id="c2017-104">Mit dem Microsoft XPS Document Writer (MXDW) können Benutzer XPS-Dokument Dateien erstellen, indem Sie Sie aus jeder Windows-Anwendung drucken.</span><span class="sxs-lookup"><span data-stu-id="c2017-104">The Microsoft XPS Document Writer (MXDW) enables users to create XPS document files by printing from any Windows application.</span></span> <span data-ttu-id="c2017-105">Anwendungsentwickler können die folgenden Ausgabeeinstellungen von MXDW mithilfe der PrintTicket-und Print-Funktionen des [Druck Schemas](./printschema.md)steuern.</span><span class="sxs-lookup"><span data-stu-id="c2017-105">Applications developers can control the following output settings of the MXDW using the PrintTicket and PrintCapabilities parts of the [Print Schema](./printschema.md).</span></span>

## <a name="jobinterleaving"></a><span data-ttu-id="c2017-106">Jobinterleaving</span><span class="sxs-lookup"><span data-stu-id="c2017-106">JobInterleaving</span></span>

<span data-ttu-id="c2017-107">Die jobinterleaving-Einstellung steuert die Inhalts Austausch Reihenfolge für die XPS-Dokumente.</span><span class="sxs-lookup"><span data-stu-id="c2017-107">The JobInterleaving setting controls the content interleaving order for the XPS Documents.</span></span> <span data-ttu-id="c2017-108">Weitere Informationen zum Überschreiben von Aufträgen finden Sie in der [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="c2017-108">For information about job interleaving, see the [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span> <span data-ttu-id="c2017-109">MXDW unterstützt die folgenden beiden Optionen für diese Einstellung:</span><span class="sxs-lookup"><span data-stu-id="c2017-109">MXDW supports the following two options for this setting:</span></span>

-   <span data-ttu-id="c2017-110">**Off** : bei dieser Option wird die Überlappungen deaktiviert, sodass alle Daten für jedes Inhalts Element im Dokument zusammenhängend sind, wodurch die Effizienz des zufälligen Zugriffs verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="c2017-110">**Off** - This option disables interleaving so that all data for each content element in the document is contiguous, which improves the efficiency of random access.</span></span> <span data-ttu-id="c2017-111">Diese Option eignet sich am besten zum Anzeigen eines XPS-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="c2017-111">This option is best for viewing an XPS document.</span></span>
-   <span data-ttu-id="c2017-112">**On** : diese Option ermöglicht das überlappen, sodass Daten für jedes Inhalts Element untergliedert und neu angeordnet werden, um eine effizientere sequenzielle Verarbeitung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c2017-112">**On** - This option enables interleaving so that data for each content element is broken up and reordered for more efficient sequential processing.</span></span> <span data-ttu-id="c2017-113">Diese Option eignet sich am besten für das herunterladen und Drucken von Web.</span><span class="sxs-lookup"><span data-stu-id="c2017-113">This option is best for web download and printing.</span></span>

<span data-ttu-id="c2017-114">Das folgende Beispiel ist ein Beispiel für die printfunktionen-XML-Datei, die die jobinterleaving-Einstellung enthält.</span><span class="sxs-lookup"><span data-stu-id="c2017-114">The following example is an example of the PrintCapabilities XML that includes the JobInterleaving setting.</span></span>


```XML
<psf:Feature name="ns0000:JobInterleaving">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Interleaving</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:OFF" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">Off - Best for viewing</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:ON" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">On - Best for the web/printing</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



<span data-ttu-id="c2017-115">Die PrintTicket-XML-Datei ist ähnlich, mit der Ausnahme, dass Sie eine bestimmte Option angibt.</span><span class="sxs-lookup"><span data-stu-id="c2017-115">The PrintTicket XML is similar, except that it specifies a particular option.</span></span> <span data-ttu-id="c2017-116">Weitere Informationen finden Sie im [Druck Schema](./printschema.md) .</span><span class="sxs-lookup"><span data-stu-id="c2017-116">See the [Print Schema](./printschema.md) for details.</span></span>

<span data-ttu-id="c2017-117">Da jobinterleaving nicht zu den [öffentlichen Schlüsselwörtern des Print-Schemas](./print-schema-public-keywords.md)gehört, müssen Sie eine Deklaration des Namespace (in diesem Fall "ns0000" im **Print-Funktionen** -Tag (oder **PrintTicket**) am Anfang des Printworks-Dokuments (oder PrintTicket) einschließen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="c2017-117">Since JobInterleaving is not one of the [Print Schema Public Keywords](./print-schema-public-keywords.md), you must include a declaration of the namespace (in this case "ns0000" in the **PrintCapabilities** (or **PrintTicket**) tag at the beginning of the PrintCapabilities (or PrintTicket) document, as shown in the following example:</span></span>


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a><span data-ttu-id="c2017-118">Jobimagetype</span><span class="sxs-lookup"><span data-stu-id="c2017-118">JobImageType</span></span>

<span data-ttu-id="c2017-119">Jobimagetype steuert das Ausgabeformat von eingebetteten Bitmapformaten.</span><span class="sxs-lookup"><span data-stu-id="c2017-119">JobImageType controls the output format of embedded bitmap formats.</span></span> <span data-ttu-id="c2017-120">MXDW unterstützt die folgenden vier Optionen für diese Einstellung:</span><span class="sxs-lookup"><span data-stu-id="c2017-120">MXDW supports the following four options for this setting:</span></span>

-   <span data-ttu-id="c2017-121">**Jpeghigh** : diese Option gibt das JPEG-Bild mit einer hohen Komprimierungs Ebene an.</span><span class="sxs-lookup"><span data-stu-id="c2017-121">**JPEGHigh** - This option specifies the JPEG image with a high level of compression.</span></span> <span data-ttu-id="c2017-122">Diese Option erzeugt die kleinste Dateigröße, jedoch die niedrigste Bildqualität.</span><span class="sxs-lookup"><span data-stu-id="c2017-122">This option produces the smallest file size, but the lowest image quality.</span></span>
-   <span data-ttu-id="c2017-123">**Jpegmed** : diese Option gibt das JPEG-Bild mit mittlerer Komprimierungs Ebene an.</span><span class="sxs-lookup"><span data-stu-id="c2017-123">**JPEGMed** - This option specifies the JPEG image with a medium level of compression.</span></span> <span data-ttu-id="c2017-124">Diese Option bietet ein optimales Gleichgewicht zwischen Dateigröße und Bildqualität.</span><span class="sxs-lookup"><span data-stu-id="c2017-124">This option provides the best balance of file size and image quality.</span></span>
-   <span data-ttu-id="c2017-125">**Jpeglow** : diese Option gibt das JPEG-Bild mit einer geringen Komprimierungs Ebene an.</span><span class="sxs-lookup"><span data-stu-id="c2017-125">**JPEGLow** - This option specifies the JPEG image with a low level of compression.</span></span> <span data-ttu-id="c2017-126">Mit dieser Option wird die Dateigröße und hohe Bildqualität am geringsten reduziert.</span><span class="sxs-lookup"><span data-stu-id="c2017-126">This option produces the least reduction in file size and high image quality.</span></span>
-   <span data-ttu-id="c2017-127">**PNG** : diese Option gibt das PNG-Bildformat mit Verlust loser Komprimierung an.</span><span class="sxs-lookup"><span data-stu-id="c2017-127">**PNG** - This option specifies the PNG image format with lossless compression.</span></span> <span data-ttu-id="c2017-128">Diese Option erzeugt die größte Dateigröße und die höchste Bildqualität.</span><span class="sxs-lookup"><span data-stu-id="c2017-128">This option produces the largest file size and the highest image quality.</span></span>

<span data-ttu-id="c2017-129">Die printfunktionen-XML-Datei der Einstellung "jobimagetype" wird unten angezeigt:</span><span class="sxs-lookup"><span data-stu-id="c2017-129">The PrintCapabilities XML of the JobImageType setting appears below:</span></span>


```XML
<psf:Feature name="ns0000:JobImageType">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Images</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:JPEGHigh" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Maximum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGMed" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
        <psf:Value xsi:type="xsd:string">JPG - Medium compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGLow" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Minimum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:PNG" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">PNG - Lossless compression</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



<span data-ttu-id="c2017-130">Die PrintTicket-XML-Datei ist ähnlich, mit der Ausnahme, dass Sie eine bestimmte Option angibt.</span><span class="sxs-lookup"><span data-stu-id="c2017-130">The PrintTicket XML is similar, except that it specifies a particular option.</span></span> <span data-ttu-id="c2017-131">Weitere Informationen finden Sie im [Druck Schema](./printschema.md) .</span><span class="sxs-lookup"><span data-stu-id="c2017-131">See the [Print Schema](./printschema.md) for details.</span></span>

<span data-ttu-id="c2017-132">Da jobimagetype kein öffentliches Schlüsselwort für den [Druck Schema](./print-schema-public-keywords.md)ist, müssen Sie eine Deklaration des Namespaces (in diesem Fall "ns0000" in das **Print-Funktionen** -Tag (oder **PrintTicket**) am Anfang des Printworks-Dokuments (oder PrintTicket) einschließen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="c2017-132">Since JobImageType is not one of the [Print Schema Public Keywords](./print-schema-public-keywords.md), you must include a declaration of the namespace (in this case "ns0000" in the **PrintCapabilities** (or **PrintTicket**) tag at the beginning of the PrintCapabilities (or PrintTicket) document, as shown in the following example:</span></span>


```XML
<psf:PrintTicket 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="related-topics"></a><span data-ttu-id="c2017-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c2017-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2017-134">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="c2017-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="c2017-135">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="c2017-135">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[<span data-ttu-id="c2017-136">Druck Schema</span><span class="sxs-lookup"><span data-stu-id="c2017-136">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="c2017-137">XPS-Spezifikation und Lizenz Downloads</span><span class="sxs-lookup"><span data-stu-id="c2017-137">XPS Specification and License Downloads</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
