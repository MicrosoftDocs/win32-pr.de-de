---
description: Die Methode "Write texmlfile" übersetzt eine Zeitachse in XML und schreibt die XML-Daten in eine Datei.
ms.assetid: 0a269e3d-6ca3-401e-bc22-6b4e8aacdbc9
title: 'IXml2Dex:: Write texmlfile-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e8710ecb142adefbdb472bf0c18a2329e818210
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358752"
---
# <a name="ixml2dexwritexmlfile-method"></a><span data-ttu-id="04b4a-103">IXml2Dex:: Write texmlfile-Methode</span><span class="sxs-lookup"><span data-stu-id="04b4a-103">IXml2Dex::WriteXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="04b4a-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="04b4a-104">\[Deprecated.</span></span> <span data-ttu-id="04b4a-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="04b4a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="04b4a-106">Die `WriteXMLFile` -Methode übersetzt eine Zeitachse in XML und schreibt die XML-Daten in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="04b4a-106">The `WriteXMLFile` method translates a timeline to XML and writes the XML data to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b4a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="04b4a-107">Syntax</span></span>


```C++
HRESULT WriteXMLFile(
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="04b4a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="04b4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04b4a-109">*ptimeline*</span><span class="sxs-lookup"><span data-stu-id="04b4a-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="04b4a-110">Zeiger auf die **IUnknown** -Schnittstelle des Timeline-Objekts.</span><span class="sxs-lookup"><span data-stu-id="04b4a-110">Pointer to the timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="04b4a-111">*FileName*</span><span class="sxs-lookup"><span data-stu-id="04b4a-111">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="04b4a-112">Eine Zeichenfolge, die den Namen der zu schreibenden Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="04b4a-112">String that specifies the name of the file to write.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04b4a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04b4a-113">Return value</span></span>

<span data-ttu-id="04b4a-114">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung der-Schnittstelle abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="04b4a-114">Returns an **HRESULT** value that depends on the implementation of the interface.</span></span> <span data-ttu-id="04b4a-115">Das **HRESULT** kann eine der folgenden Standard Konstanten oder andere nicht aufgelistete Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="04b4a-115">The **HRESULT** can include one of the following standard constants, or other values not listed.</span></span>



| <span data-ttu-id="04b4a-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="04b4a-116">Return code</span></span>                                                                                   | <span data-ttu-id="04b4a-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04b4a-117">Description</span></span>                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="04b4a-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="04b4a-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="04b4a-119">Das Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="04b4a-119">Argument is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="04b4a-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="04b4a-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="04b4a-121">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="04b4a-121">Insufficient memory.</span></span><br/> |
| <dl> <span data-ttu-id="04b4a-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="04b4a-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="04b4a-123">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="04b4a-123">Success.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="04b4a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04b4a-124">Remarks</span></span>

<span data-ttu-id="04b4a-125">Diese Methode generiert eine XML-Datei, die alle Komponenten in der Zeitachse darstellt.</span><span class="sxs-lookup"><span data-stu-id="04b4a-125">This method generates an XML file that represents all the components in the timeline.</span></span>

> [!Note]  
> <span data-ttu-id="04b4a-126">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="04b4a-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="04b4a-127">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="04b4a-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="04b4a-128">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="04b4a-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="04b4a-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04b4a-129">Requirements</span></span>



| <span data-ttu-id="04b4a-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04b4a-130">Requirement</span></span> | <span data-ttu-id="04b4a-131">Wert</span><span class="sxs-lookup"><span data-stu-id="04b4a-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04b4a-132">Version</span><span class="sxs-lookup"><span data-stu-id="04b4a-132">Version</span></span><br/> | <span data-ttu-id="04b4a-133">Internet Explorer 4,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="04b4a-133">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="04b4a-134">Header</span><span class="sxs-lookup"><span data-stu-id="04b4a-134">Header</span></span><br/>  | <dl> <span data-ttu-id="04b4a-135"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="04b4a-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="04b4a-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="04b4a-136">Library</span></span><br/> | <dl> <span data-ttu-id="04b4a-137"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="04b4a-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04b4a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04b4a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b4a-139">**IXml2Dex-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="04b4a-139">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="04b4a-140">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="04b4a-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




