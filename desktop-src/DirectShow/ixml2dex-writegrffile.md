---
description: Die Methode "Write-grffile" schreibt ein Filter Diagramm in eine Datei im GRF-Format.
ms.assetid: 2064d2d7-34ac-465c-ae09-d125c670d0e8
title: 'IXml2Dex:: Beschreib tegrffile-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteGrfFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a411540d95a7313070a643b7b1895b564a49e089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351331"
---
# <a name="ixml2dexwritegrffile-method"></a><span data-ttu-id="84704-103">IXml2Dex:: Beschreib tegrffile-Methode</span><span class="sxs-lookup"><span data-stu-id="84704-103">IXml2Dex::WriteGrfFile method</span></span>

> [!Note]  
> <span data-ttu-id="84704-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="84704-104">\[Deprecated.</span></span> <span data-ttu-id="84704-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="84704-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="84704-106">Die- `WriteGrfFile` Methode schreibt ein Filter Diagramm in eine Datei im GRF-Format.</span><span class="sxs-lookup"><span data-stu-id="84704-106">The `WriteGrfFile` method writes a filter graph to a file in .grf format.</span></span>

## <a name="syntax"></a><span data-ttu-id="84704-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="84704-107">Syntax</span></span>


```C++
HRESULT WriteGrfFile(
   IUnknown *pGraph,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="84704-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="84704-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84704-109">*PGraph*</span><span class="sxs-lookup"><span data-stu-id="84704-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="84704-110">Zeiger auf die **IUnknown** -Schnittstelle des Filter Diagramms.</span><span class="sxs-lookup"><span data-stu-id="84704-110">Pointer to the filter graph's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="84704-111">*FileName*</span><span class="sxs-lookup"><span data-stu-id="84704-111">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="84704-112">Eine Zeichenfolge, die den Namen der zu schreibenden Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="84704-112">String that specifies the name of the file to write.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84704-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84704-113">Return value</span></span>

<span data-ttu-id="84704-114">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung der-Schnittstelle abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="84704-114">Returns an **HRESULT** value that depends on the implementation of the interface.</span></span> <span data-ttu-id="84704-115">HRESULT kann eine der folgenden Standard Konstanten oder andere nicht aufgelistete Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="84704-115">HRESULT can include one of the following standard constants, or other values not listed.</span></span>



| <span data-ttu-id="84704-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="84704-116">Return code</span></span>                                                                                  | <span data-ttu-id="84704-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84704-117">Description</span></span>                     |
|----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="84704-118"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="84704-118"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="84704-119">Fehler.</span><span class="sxs-lookup"><span data-stu-id="84704-119">Failure.</span></span><br/>             |
| <dl> <span data-ttu-id="84704-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="84704-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="84704-121">Das Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="84704-121">Argument is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="84704-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="84704-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="84704-123">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="84704-123">Success.</span></span><br/>             |



 

<span data-ttu-id="84704-124">Diese Methode kann auch Fehlercodes zurückgeben, die von internen Aufrufen der Methoden **IStorage:: foratestream** und **ipersistent:: Save** generiert werden.</span><span class="sxs-lookup"><span data-stu-id="84704-124">This method can also return error codes generated by internal calls to the **IStorage::CreateStream** and **IPersist::Save** methods.</span></span> <span data-ttu-id="84704-125">Weitere Informationen finden Sie unter Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="84704-125">For more information, see the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="84704-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84704-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="84704-127">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="84704-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="84704-128">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="84704-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="84704-129">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="84704-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="84704-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84704-130">Requirements</span></span>



| <span data-ttu-id="84704-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84704-131">Requirement</span></span> | <span data-ttu-id="84704-132">Wert</span><span class="sxs-lookup"><span data-stu-id="84704-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84704-133">Version</span><span class="sxs-lookup"><span data-stu-id="84704-133">Version</span></span><br/> | <span data-ttu-id="84704-134">Internet Explorer 4,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="84704-134">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="84704-135">Header</span><span class="sxs-lookup"><span data-stu-id="84704-135">Header</span></span><br/>  | <dl> <span data-ttu-id="84704-136"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="84704-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="84704-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="84704-137">Library</span></span><br/> | <dl> <span data-ttu-id="84704-138"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="84704-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84704-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84704-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84704-140">**IXml2Dex-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="84704-140">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="84704-141">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="84704-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




