---
description: Die Put \_ Filter-Methode gibt einen Quell Filter an, der vom Medien Detektor verwendet werden soll.
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: Imediadet::p ut_Filter-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd07ee3e2a18dcceae752e3923fd5fbdc88c0313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370679"
---
# <a name="imediadetput_filter-method"></a><span data-ttu-id="95370-103">Imediadet::p UT- \_ Filter Methode</span><span class="sxs-lookup"><span data-stu-id="95370-103">IMediaDet::put\_Filter method</span></span>

> [!Note]  
> <span data-ttu-id="95370-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="95370-104">\[Deprecated.</span></span> <span data-ttu-id="95370-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="95370-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="95370-106">Die- `put_Filter` Methode gibt einen Quell Filter an, der vom Medien Detektor verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="95370-106">The `put_Filter` method specifies a source filter for the media detector to use.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95370-107">Fügen Sie den Quell Filter nicht zu Ihrem eigenen Filter Diagramm hinzu, oder verwenden Sie einen Filter, der bereits in einem Filter Diagramm vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="95370-107">Do not add the source filter to your own filter graph, or use a filter that is already in a filter graph.</span></span> <span data-ttu-id="95370-108">Das Medien Erkennungs Objekt erstellt automatisch ein internes Filter Diagramm, und das Platzieren des Filters in einem anderen Diagramm kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="95370-108">The media detector object automatically builds an internal filter graph, and putting the filter in another graph can cause unexpected results.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="95370-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="95370-109">Syntax</span></span>


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="95370-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="95370-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95370-111">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95370-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95370-112">Zeiger auf die **IUnknown** -Schnittstelle des Quell Filters.</span><span class="sxs-lookup"><span data-stu-id="95370-112">Pointer to the source filter's **IUnknown** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95370-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95370-113">Return value</span></span>

<span data-ttu-id="95370-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="95370-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="95370-115">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="95370-115">Possible values include the following:</span></span>



| <span data-ttu-id="95370-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="95370-116">Return code</span></span>                                                                                   | <span data-ttu-id="95370-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95370-117">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="95370-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="95370-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="95370-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="95370-119">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="95370-120"><dt>**E \_ nointerface**</dt></span><span class="sxs-lookup"><span data-stu-id="95370-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="95370-121">*NewVal* verweist nicht auf einen Filter.</span><span class="sxs-lookup"><span data-stu-id="95370-121">*newVal* does not point to a filter.</span></span><br/> |
| <dl> <span data-ttu-id="95370-122"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="95370-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="95370-123">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="95370-123">**NULL** pointer argument.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="95370-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95370-124">Remarks</span></span>

<span data-ttu-id="95370-125">Bei den meisten Anwendungen ist es einfacher, die [**\_ Dateiname-Methode imediadet::p UT**](imediadet-put-filename.md) mit dem Namen einer Quelldatei aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="95370-125">For most applications, it is simpler to call the [**IMediaDet::put\_Filename**](imediadet-put-filename.md) method with the name of a source file.</span></span>

> [!Note]  
> <span data-ttu-id="95370-126">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="95370-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="95370-127">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="95370-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="95370-128">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="95370-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95370-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95370-129">Requirements</span></span>



| <span data-ttu-id="95370-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95370-130">Requirement</span></span> | <span data-ttu-id="95370-131">Wert</span><span class="sxs-lookup"><span data-stu-id="95370-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95370-132">Header</span><span class="sxs-lookup"><span data-stu-id="95370-132">Header</span></span><br/>  | <dl> <span data-ttu-id="95370-133"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="95370-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="95370-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95370-134">Library</span></span><br/> | <dl> <span data-ttu-id="95370-135"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="95370-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95370-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95370-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95370-137">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="95370-137">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="95370-138">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="95370-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




