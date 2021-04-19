---
description: Die Methode "Read xmlfile" lädt eine XML-Projektdatei.
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: 'IXml2Dex:: infoxmlfile-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.ReadXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5b0fb5104e56afbcc4dd25e28981f0c382d7888e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370812"
---
# <a name="ixml2dexreadxmlfile-method"></a><span data-ttu-id="e7404-103">IXml2Dex:: infoxmlfile-Methode</span><span class="sxs-lookup"><span data-stu-id="e7404-103">IXml2Dex::ReadXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="e7404-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e7404-104">\[Deprecated.</span></span> <span data-ttu-id="e7404-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e7404-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e7404-106">Die- `ReadXMLFile` Methode lädt eine XML-Projektdatei.</span><span class="sxs-lookup"><span data-stu-id="e7404-106">The `ReadXMLFile` method loads an XML project file.</span></span> <span data-ttu-id="e7404-107">Diese Methode erstellt Instanzen aller-Objekte, die in der XML-Datei ausgedrückt werden, fügt Sie in die Zeitachse ein und wendet alle für die Zeitachse angegebenen Attribute an, wie z. b. die Framerate oder die Standard Effekte.</span><span class="sxs-lookup"><span data-stu-id="e7404-107">This method creates instances of all the objects expressed in the XML file and inserts them into the timeline, as well as applying any attributes given for the timeline, such as frame rate or default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7404-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7404-108">Syntax</span></span>


```C++
HRESULT ReadXMLFile(
   IUnknown *pTimeline,
   BSTR     XMLName
);
```



## <a name="parameters"></a><span data-ttu-id="e7404-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7404-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7404-110">*ptimeline*</span><span class="sxs-lookup"><span data-stu-id="e7404-110">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="e7404-111">Zeiger auf die **IUnknown** -Schnittstelle eines Timeline-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e7404-111">Pointer to a timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="e7404-112">*XMLName*</span><span class="sxs-lookup"><span data-stu-id="e7404-112">*XMLName*</span></span> 
</dt> <dd>

<span data-ttu-id="e7404-113">Eine Zeichenfolge, die den Namen der zu ladenden Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="e7404-113">String that specifies the name of the file to load.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7404-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7404-114">Return value</span></span>

<span data-ttu-id="e7404-115">Gibt einen HRESULT-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e7404-115">Returns an HRESULT value.</span></span> <span data-ttu-id="e7404-116">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="e7404-116">Possible values include the following.</span></span>



| <span data-ttu-id="e7404-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e7404-117">Return code</span></span>                                                                                                  | <span data-ttu-id="e7404-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7404-118">Description</span></span>                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="e7404-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e7404-119"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="e7404-120">Erfolg</span><span class="sxs-lookup"><span data-stu-id="e7404-120">Success</span></span><br/>             |
| <dl> <span data-ttu-id="e7404-121"><dt>**VFW \_ E \_ ungültiges \_ Datei \_ Format.**</dt></span><span class="sxs-lookup"><span data-stu-id="e7404-121"><dt>**VFW\_E\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="e7404-122">Ungültiges Dateiformat</span><span class="sxs-lookup"><span data-stu-id="e7404-122">Invalid file format</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e7404-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7404-123">Remarks</span></span>

<span data-ttu-id="e7404-124">Diese Methode löscht keine vorhandenen Objekte aus der Zeitachse, bevor die neuen Objekte eingefügt werden, die in der XML-Datei definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e7404-124">This method does not clear existing objects from the timeline before it inserts the new objects defined in the XML file.</span></span> <span data-ttu-id="e7404-125">Wenn Sie eine vorhandene Zeitachse aktualisieren müssen, müssen Sie zuerst [**iamtimeline:: clearallgroups**](iamtimeline-clearallgroups.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e7404-125">If you need to refresh an existing timeline, call [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md) first.</span></span>

> [!Note]  
> <span data-ttu-id="e7404-126">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e7404-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e7404-127">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e7404-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e7404-128">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7404-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e7404-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7404-129">Requirements</span></span>



| <span data-ttu-id="e7404-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7404-130">Requirement</span></span> | <span data-ttu-id="e7404-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e7404-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7404-132">Version</span><span class="sxs-lookup"><span data-stu-id="e7404-132">Version</span></span><br/> | <span data-ttu-id="e7404-133">Internet Explorer 4,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e7404-133">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="e7404-134">Header</span><span class="sxs-lookup"><span data-stu-id="e7404-134">Header</span></span><br/>  | <dl> <span data-ttu-id="e7404-135"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e7404-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e7404-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e7404-136">Library</span></span><br/> | <dl> <span data-ttu-id="e7404-137"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e7404-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7404-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7404-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7404-139">**IXml2Dex-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e7404-139">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="e7404-140">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e7404-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




