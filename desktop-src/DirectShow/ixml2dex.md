---
description: Die IXml2Dex-Schnittstelle speichert und lädt DirectShow-Projektdateien (Bearbeitungs Dienste) in Extensible Markup Language (XML). Diese Schnittstelle stellt auch Methoden zum Lesen und Schreiben von DirectShow Graph-Dateien (. GRF) bereit.
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: IXml2Dex-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac15110aa1482c37a835ae874057a792e310fc2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361476"
---
# <a name="ixml2dex-interface"></a><span data-ttu-id="c8ba5-104">IXml2Dex-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c8ba5-104">IXml2Dex interface</span></span>

> [!Note]  
> <span data-ttu-id="c8ba5-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-105">\[Deprecated.</span></span> <span data-ttu-id="c8ba5-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="c8ba5-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c8ba5-107">Die `IXml2Dex` -Schnittstelle speichert und lädt [DirectShow](directshow-editing-services.md) -Projektdateien (Bearbeitungs Dienste) in Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="c8ba5-107">The `IXml2Dex` interface saves and loads [DirectShow Editing Services](directshow-editing-services.md) (DES) project files in Extensible Markup Language (XML).</span></span> <span data-ttu-id="c8ba5-108">Diese Schnittstelle stellt auch Methoden zum Lesen und Schreiben von DirectShow Graph-Dateien (. GRF) bereit.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-108">This interface also provides methods for reading and writing DirectShow graph (.grf) files.</span></span>

## <a name="members"></a><span data-ttu-id="c8ba5-109">Member</span><span class="sxs-lookup"><span data-stu-id="c8ba5-109">Members</span></span>

<span data-ttu-id="c8ba5-110">Die **IXml2Dex** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-110">The **IXml2Dex** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c8ba5-111">**IXml2Dex** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c8ba5-111">**IXml2Dex** also has these types of members:</span></span>

-   [<span data-ttu-id="c8ba5-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="c8ba5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c8ba5-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="c8ba5-113">Methods</span></span>

<span data-ttu-id="c8ba5-114">Die **IXml2Dex** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-114">The **IXml2Dex** interface has these methods.</span></span>



| <span data-ttu-id="c8ba5-115">Methode</span><span class="sxs-lookup"><span data-stu-id="c8ba5-115">Method</span></span>                                                      | <span data-ttu-id="c8ba5-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8ba5-116">Description</span></span>                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="c8ba5-117">**Copyxml**</span><span class="sxs-lookup"><span data-stu-id="c8ba5-117">**CopyXML**</span></span>](ixml2dex-copyxml.md)                         | <span data-ttu-id="c8ba5-118">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-118">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="c8ba5-119">**"Kreategraphfromfile"**</span><span class="sxs-lookup"><span data-stu-id="c8ba5-119">**CreateGraphFromFile**</span></span>](ixml2dex-creategraphfromfile.md) | <span data-ttu-id="c8ba5-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-120">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="c8ba5-121">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="c8ba5-121">**Delete**</span></span>](ixml2dex-delete.md)                           | <span data-ttu-id="c8ba5-122">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-122">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="c8ba5-123">**Pastexml**</span><span class="sxs-lookup"><span data-stu-id="c8ba5-123">**PasteXML**</span></span>](ixml2dex-pastexml.md)                       | <span data-ttu-id="c8ba5-124">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-124">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="c8ba5-125">**"Pastexmlfile"**</span><span class="sxs-lookup"><span data-stu-id="c8ba5-125">**PasteXMLFile**</span></span>](ixml2dex-pastexmlfile.md)               | <span data-ttu-id="c8ba5-126">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-126">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="c8ba5-127">**ReadXml**</span><span class="sxs-lookup"><span data-stu-id="c8ba5-127">**ReadXML**</span></span>](ixml2dex-readxml.md)                         | <span data-ttu-id="c8ba5-128">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-128">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="c8ba5-129">**"Infodatei"**</span><span class="sxs-lookup"><span data-stu-id="c8ba5-129">**ReadXMLFile**</span></span>](ixml2dex-readxmlfile.md)                 | <span data-ttu-id="c8ba5-130">Lädt eine XML-Projektdatei.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-130">Loads an XML project file.</span></span><br/>                                      |
| [<span data-ttu-id="c8ba5-131">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="c8ba5-131">**Reset**</span></span>](ixml2dex-reset.md)                             | <span data-ttu-id="c8ba5-132">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-132">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="c8ba5-133">**Schreibgrffile**</span><span class="sxs-lookup"><span data-stu-id="c8ba5-133">**WriteGrfFile**</span></span>](ixml2dex-writegrffile.md)               | <span data-ttu-id="c8ba5-134">Schreibt ein Filter Diagramm in eine Datei im GRF-Format.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-134">Writes a filter graph to a file in .grf format.</span></span><br/>                 |
| [<span data-ttu-id="c8ba5-135">**WriteXml**</span><span class="sxs-lookup"><span data-stu-id="c8ba5-135">**WriteXML**</span></span>](ixml2dex-writexml.md)                       | <span data-ttu-id="c8ba5-136">Übersetzt eine Zeitachse in eine XML-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-136">Translates a timeline to an XML string.</span></span><br/>                         |
| [<span data-ttu-id="c8ba5-137">**"Write texmlfile"**</span><span class="sxs-lookup"><span data-stu-id="c8ba5-137">**WriteXMLFile**</span></span>](ixml2dex-writexmlfile.md)               | <span data-ttu-id="c8ba5-138">Übersetzt eine Zeitachse in XML und schreibt die XML-Daten in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-138">Translates a timeline to XML and writes the XML data to a file.</span></span><br/> |
| [<span data-ttu-id="c8ba5-139">**Schreib texmlpart**</span><span class="sxs-lookup"><span data-stu-id="c8ba5-139">**WriteXMLPart**</span></span>](ixml2dex-writexmlpart.md)               | <span data-ttu-id="c8ba5-140">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-140">Not implemented.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="c8ba5-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8ba5-141">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c8ba5-142">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c8ba5-143">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c8ba5-144">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c8ba5-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8ba5-145">Requirements</span></span>



| <span data-ttu-id="c8ba5-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8ba5-146">Requirement</span></span> | <span data-ttu-id="c8ba5-147">Wert</span><span class="sxs-lookup"><span data-stu-id="c8ba5-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ba5-148">Version</span><span class="sxs-lookup"><span data-stu-id="c8ba5-148">Version</span></span><br/> | <span data-ttu-id="c8ba5-149">Internet Explorer 4,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c8ba5-149">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="c8ba5-150">Header</span><span class="sxs-lookup"><span data-stu-id="c8ba5-150">Header</span></span><br/>  | <dl> <span data-ttu-id="c8ba5-151"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c8ba5-151"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c8ba5-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c8ba5-152">Library</span></span><br/> | <dl> <span data-ttu-id="c8ba5-153"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="c8ba5-153"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
