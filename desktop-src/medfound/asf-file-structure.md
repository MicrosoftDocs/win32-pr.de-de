---
description: In diesem Thema wird die Struktur einer ASF-Datei (Advanced Systems Format) beschrieben.
ms.assetid: 4a817efa-5452-46bf-8921-2ba199c21949
title: Struktur der ASF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672067b5f933884326038a93b6d4538c68558856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524672"
---
# <a name="asf-file-structure"></a><span data-ttu-id="84f1b-103">Struktur der ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="84f1b-103">ASF File Structure</span></span>

<span data-ttu-id="84f1b-104">In diesem Thema wird die Struktur einer ASF-Datei (Advanced Systems Format) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="84f1b-104">This topic describes the structure of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="84f1b-105">Ausführliche Informationen zu ASF-Dateien finden Sie in der [ASF-Spezifikation](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="84f1b-105">For detailed information about ASF files, download the [ASF Specification](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span> <span data-ttu-id="84f1b-106">Sie können auch das [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) -Tool verwenden, um die Struktur einer vorhandenen ASF-Datei anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="84f1b-106">You can also use the [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) tool to see the structure of an existing ASF file.</span></span>

<span data-ttu-id="84f1b-107">Die Basiseinheit der Organisation für ASF-Dateien wird als *Objekt* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="84f1b-107">The base unit of organization for ASF files is called an *object*.</span></span> <span data-ttu-id="84f1b-108">Ein Objekt vom Typ "ASF File" enthält die folgenden Daten.</span><span class="sxs-lookup"><span data-stu-id="84f1b-108">An ASF file object contains the following data.</span></span>



| <span data-ttu-id="84f1b-109">Daten</span><span class="sxs-lookup"><span data-stu-id="84f1b-109">Data</span></span>                                                        | <span data-ttu-id="84f1b-110">Size</span><span class="sxs-lookup"><span data-stu-id="84f1b-110">Size</span></span>     |
|-------------------------------------------------------------|----------|
| <span data-ttu-id="84f1b-111">Eine GUID, die das Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="84f1b-111">A GUID that identifies the object.</span></span>                          | <span data-ttu-id="84f1b-112">128 Bits</span><span class="sxs-lookup"><span data-stu-id="84f1b-112">128 bits</span></span> |
| <span data-ttu-id="84f1b-113">Die Größe des Objekts.</span><span class="sxs-lookup"><span data-stu-id="84f1b-113">The size of the object.</span></span>                                     | <span data-ttu-id="84f1b-114">64 Bits.</span><span class="sxs-lookup"><span data-stu-id="84f1b-114">64-bits.</span></span> |
| <span data-ttu-id="84f1b-115">Objektdaten.</span><span class="sxs-lookup"><span data-stu-id="84f1b-115">Object data.</span></span> <span data-ttu-id="84f1b-116">Die Objektdaten können andere ASF-Objekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="84f1b-116">The object data can contain other ASF objects.</span></span> | <span data-ttu-id="84f1b-117">Verschiedene Ursachen.</span><span class="sxs-lookup"><span data-stu-id="84f1b-117">Varies.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="84f1b-118">Ein ASF-Datei Objekt ist einfach ein Datenblock.</span><span class="sxs-lookup"><span data-stu-id="84f1b-118">An ASF file object is simply a chunk of data.</span></span> <span data-ttu-id="84f1b-119">Es handelt sich nicht um ein Objekt im Computer Programmier Sinn.</span><span class="sxs-lookup"><span data-stu-id="84f1b-119">It is not an object in the computer programming sense.</span></span>

 

<span data-ttu-id="84f1b-120">Eine ASF-Datei enthält drei Typen von Datei Objekten der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="84f1b-120">An ASF file contains three types of top-level file objects.</span></span>



| <span data-ttu-id="84f1b-121">ASF-Datei Objekt</span><span class="sxs-lookup"><span data-stu-id="84f1b-121">ASF File Object</span></span>                                                                                                                      | <span data-ttu-id="84f1b-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84f1b-122">Description</span></span>                                          |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="84f1b-123"><span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Header Objekt</span><span class="sxs-lookup"><span data-stu-id="84f1b-123"><span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Header Object</span></span><br/>         | <span data-ttu-id="84f1b-124">Enthält Informationen zur ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="84f1b-124">Contains information about the ASF file.</span></span><br/>  |
| <span data-ttu-id="84f1b-125"><span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Datenobjekt</span><span class="sxs-lookup"><span data-stu-id="84f1b-125"><span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Data Object</span></span><br/>                     | <span data-ttu-id="84f1b-126">Enthält Pakete von Mediendaten.</span><span class="sxs-lookup"><span data-stu-id="84f1b-126">Contains packets of media data.</span></span><br/>           |
| <span data-ttu-id="84f1b-127"><span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Index Objekt (e)</span><span class="sxs-lookup"><span data-stu-id="84f1b-127"><span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Index Object(s)</span></span><br/> | <span data-ttu-id="84f1b-128">Enthält mindestens einen Index.</span><span class="sxs-lookup"><span data-stu-id="84f1b-128">Contains one or more indexes.</span></span> <span data-ttu-id="84f1b-129">(Optional.)</span><span class="sxs-lookup"><span data-stu-id="84f1b-129">(Optional.)</span></span><br/> |



 

<span data-ttu-id="84f1b-130">Das folgende Diagramm zeigt die Struktur der ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="84f1b-130">The following diagram shows the ASF file structure.</span></span>

![Diagramm, das die Struktur der ASF-Datei, einschließlich der Elemente innerhalb des Headers, der Daten und des Indexes, anzeigt](images/asf-components04.png)

<span data-ttu-id="84f1b-132">Dieses Diagramm wird nicht zum Skalieren gezeichnet. in der Regel besteht das Datenobjekt aus dem größten Teil der Datei.</span><span class="sxs-lookup"><span data-stu-id="84f1b-132">This diagram is not drawn to scale; typically the Data Object comprises most of the file.</span></span>

### <a name="header-object"></a><span data-ttu-id="84f1b-133">Header Objekt</span><span class="sxs-lookup"><span data-stu-id="84f1b-133">Header Object</span></span>

<span data-ttu-id="84f1b-134">Das Header Objekt ist obligatorisch und wird am Anfang jeder ASF-Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84f1b-134">The Header Object is mandatory and appears at the beginning of every ASF file.</span></span> <span data-ttu-id="84f1b-135">Sie enthält globale Dateiattribute und Informationen zu den Datenströmen in der ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="84f1b-135">It contains global file attributes and information about the streams in the ASF file.</span></span> <span data-ttu-id="84f1b-136">Diese Informationen werden verwendet, um die Daten in der Datei zu interpretieren und wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="84f1b-136">This information is used to interpret and play the data in the file.</span></span>

<span data-ttu-id="84f1b-137">Das Header Objekt enthält mehrere madatory-unter Objekte:</span><span class="sxs-lookup"><span data-stu-id="84f1b-137">The Header Object contains several madatory sub-objects:</span></span>

-   <span data-ttu-id="84f1b-138">Das Dateieigenschaften Objekt beschreibt globale Attribute der Datei, z. b. die Dateigröße, die Wiedergabedauer, die Anzahl von Datenpaketen, die minimale und die maximale Paketgröße und die maximale Bitrate.</span><span class="sxs-lookup"><span data-stu-id="84f1b-138">The File Properties Object describes global attributes of the file, such as the file size, play duration, number of data packets, minimum and maximum packet size, and maximum bit rate.</span></span>
-   <span data-ttu-id="84f1b-139">Das Header Erweiterungs Objekt ermöglicht das Hinzufügen zusätzlicher Funktionen zu einer ASF-Datei, während die Abwärtskompatibilität beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="84f1b-139">The Header Extension Object enables additional functionality to be added to an ASF file while maintaining backward compatibility.</span></span>
-   <span data-ttu-id="84f1b-140">Das Stream Properties-Objekt beschreibt einen Stream in der Datei.</span><span class="sxs-lookup"><span data-stu-id="84f1b-140">The Stream Properties Object describes one stream in the file.</span></span> <span data-ttu-id="84f1b-141">Eine ASF-Datei muss mindestens einen Stream und somit mindestens ein Stream Properties-Objekt enthalten.</span><span class="sxs-lookup"><span data-stu-id="84f1b-141">An ASF file must contain at least one stream, and therefore at least one Stream Properties Object.</span></span>

<span data-ttu-id="84f1b-142">Das Header Objekt kann zusätzliche optionale Informationen enthalten, einschließlich Metadaten über die Datei (z. b. Titel und Autor), eine Liste der Codecs, die zum Codieren der Datei verwendet werden, sowie Informationen zum Inhalts Schutz.</span><span class="sxs-lookup"><span data-stu-id="84f1b-142">The Header Object can contain additional optional information, including metadata about the file (such as title and author), a list of the codecs used to encode the file, and content protection information.</span></span>

### <a name="data-object"></a><span data-ttu-id="84f1b-143">Datenobjekt</span><span class="sxs-lookup"><span data-stu-id="84f1b-143">Data Object</span></span>

<span data-ttu-id="84f1b-144">Das ASF-Datenobjekt enthält alle Mediendaten für die ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="84f1b-144">The ASF Data Object contains all of the media data for the ASF file.</span></span> <span data-ttu-id="84f1b-145">Dieses Objekt ist obligatorisch und muss dem ASF-Header Objekt folgen.</span><span class="sxs-lookup"><span data-stu-id="84f1b-145">This object is mandatory and must follow the ASF Header Object.</span></span>

<span data-ttu-id="84f1b-146">Das Datenobjekt wird in Daten *Pakete* aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="84f1b-146">The Data Object is divided into data *packets*.</span></span> <span data-ttu-id="84f1b-147">Jedes Paket enthält Daten für einen oder mehrere Datenströme in der Datei.</span><span class="sxs-lookup"><span data-stu-id="84f1b-147">Each packet contains data for one or several streams in the file.</span></span> <span data-ttu-id="84f1b-148">Ein Datenpaket enthält einen datenpaketheader, der Informationen zur Paketverarbeitung bereitstellt, gefolgt von den Nutzlastdaten der tatsächlichen digitalen Mediendaten.</span><span class="sxs-lookup"><span data-stu-id="84f1b-148">A data packet contains a data packet header that provides packet parsing information, followed by the payload data the actual digital media data.</span></span> <span data-ttu-id="84f1b-149">Allen Datenpaketen ist eine Präsentationszeit zugeordnet, die in der empfangenen Reihenfolge angeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="84f1b-149">All of the data packets have a presentation time associated with it and are arranged in the order received.</span></span>

<span data-ttu-id="84f1b-150">Informationen zum Inhalt des Datenobjekts, z. b. Paketgröße und Paket Anzahl, werden im Header Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="84f1b-150">Information about the contents of the Data Object, such as the packet size and packet count, is stored in the Header Object.</span></span>

### <a name="index-object"></a><span data-ttu-id="84f1b-151">Index-Objekt</span><span class="sxs-lookup"><span data-stu-id="84f1b-151">Index Object</span></span>

<span data-ttu-id="84f1b-152">Das Index Objekt ist optional und ist das letzte Objekt in der ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="84f1b-152">The Index Object is optional and is the last object in the ASF file.</span></span> <span data-ttu-id="84f1b-153">Eine ASF-Datei kann mehr als ein Index Objekt enthalten.</span><span class="sxs-lookup"><span data-stu-id="84f1b-153">An ASF file can contain more than one Index Object.</span></span> <span data-ttu-id="84f1b-154">Das Index-Objekt bietet zeitbasierten zufälligen Zugriff auf das ASF-Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="84f1b-154">The Index Object provides time-based random access into the ASF Data Object.</span></span>

<span data-ttu-id="84f1b-155">Ein einfaches Index Objekt ist ein anderer Indextyp.</span><span class="sxs-lookup"><span data-stu-id="84f1b-155">A Simple Index Object is another type of index.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84f1b-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="84f1b-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84f1b-157">Unterstützung von ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84f1b-157">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




