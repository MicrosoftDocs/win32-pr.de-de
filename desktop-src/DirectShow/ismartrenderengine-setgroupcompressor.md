---
description: Gibt einen Komprimierungs Filter an, der beim Rendern der angegebenen Gruppe verwendet werden soll.
ms.assetid: ba717cac-c5a8-4821-a5f0-dd9d5fe4834e
title: 'Ismartrenderengine:: setgroupcompressor-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.SetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9cb02a9d8daf7e6ba74a45299daa9d45ab63d5db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367139"
---
# <a name="ismartrenderenginesetgroupcompressor-method"></a><span data-ttu-id="89fe0-103">Ismartrenderengine:: setgroupcompressor-Methode</span><span class="sxs-lookup"><span data-stu-id="89fe0-103">ISmartRenderEngine::SetGroupCompressor method</span></span>

> [!Note]  
> <span data-ttu-id="89fe0-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="89fe0-104">\[Deprecated.</span></span> <span data-ttu-id="89fe0-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="89fe0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="89fe0-106">Gibt einen Komprimierungs Filter an, der beim Rendern der angegebenen Gruppe verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="89fe0-106">Specifies a compression filter to use when rendering the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="89fe0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="89fe0-107">Syntax</span></span>


```C++
HRESULT SetGroupCompressor(
   long        Group,
   IBaseFilter *pCompressor
);
```



## <a name="parameters"></a><span data-ttu-id="89fe0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="89fe0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89fe0-109">*Gruppieren*</span><span class="sxs-lookup"><span data-stu-id="89fe0-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="89fe0-110">Der null basierte Index der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="89fe0-110">Zero-based index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="89fe0-111">*pkompressor*</span><span class="sxs-lookup"><span data-stu-id="89fe0-111">*pCompressor*</span></span> 
</dt> <dd>

<span data-ttu-id="89fe0-112">Ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Komprimierungs Filters.</span><span class="sxs-lookup"><span data-stu-id="89fe0-112">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the compression filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89fe0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89fe0-113">Return value</span></span>

<span data-ttu-id="89fe0-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="89fe0-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="89fe0-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="89fe0-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="89fe0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89fe0-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="89fe0-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="89fe0-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="89fe0-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="89fe0-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="89fe0-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="89fe0-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="89fe0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89fe0-120">Requirements</span></span>



| <span data-ttu-id="89fe0-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89fe0-121">Requirement</span></span> | <span data-ttu-id="89fe0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="89fe0-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89fe0-123">Header</span><span class="sxs-lookup"><span data-stu-id="89fe0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="89fe0-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="89fe0-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="89fe0-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="89fe0-125">Library</span></span><br/> | <dl> <span data-ttu-id="89fe0-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="89fe0-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89fe0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89fe0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89fe0-128">**Ismartrenderengine-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="89fe0-128">**ISmartRenderEngine Interface**</span></span>](ismartrenderengine.md)
</dt> <dt>

[<span data-ttu-id="89fe0-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="89fe0-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




