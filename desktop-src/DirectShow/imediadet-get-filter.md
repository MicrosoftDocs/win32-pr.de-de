---
description: Die get \_ Filter-Methode ruft einen Zeiger auf den Quell Filter ab, der derzeit vom Medien Erkennungs Modul verwendet wird.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: 'Imediadet:: get_Filter-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f80b5d5021ca7f04cd56dc319fb5416c3361108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352071"
---
# <a name="imediadetget_filter-method"></a><span data-ttu-id="43985-103">Imediadet:: get- \_ Filter Methode</span><span class="sxs-lookup"><span data-stu-id="43985-103">IMediaDet::get\_Filter method</span></span>

> [!Note]  
> <span data-ttu-id="43985-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="43985-104">\[Deprecated.</span></span> <span data-ttu-id="43985-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="43985-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="43985-106">Die- `get_Filter` Methode ruft einen Zeiger auf den Quell Filter ab, der derzeit vom Medien Erkennungs Modul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="43985-106">The `get_Filter` method retrieves a pointer to the source filter currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="43985-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="43985-107">Syntax</span></span>


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a><span data-ttu-id="43985-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="43985-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43985-109">*ppval* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="43985-109">*ppVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="43985-110">Empfängt einen Zeiger auf die **IUnknown** -Schnittstelle des Filters.</span><span class="sxs-lookup"><span data-stu-id="43985-110">Receives a pointer to the filter's **IUnknown** interface.</span></span> <span data-ttu-id="43985-111">Wenn kein Quell Filter verwendet wird, wird der Wert auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="43985-111">If no source filter is in use, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43985-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43985-112">Return value</span></span>

<span data-ttu-id="43985-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="43985-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="43985-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="43985-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="43985-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43985-115">Remarks</span></span>

<span data-ttu-id="43985-116">Wenn der Wert der-Methode zurückgegeben wird, verfügt die **IUnknown** -Schnittstelle über einen ausstehenden Verweis Zähler, wenn *\* ppval* nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="43985-116">When the method returns, if *\*ppVal* is not **NULL**, the **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="43985-117">Geben Sie die Schnittstelle frei, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="43985-117">Release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="43985-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="43985-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="43985-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="43985-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="43985-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="43985-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43985-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43985-121">Requirements</span></span>



| <span data-ttu-id="43985-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43985-122">Requirement</span></span> | <span data-ttu-id="43985-123">Wert</span><span class="sxs-lookup"><span data-stu-id="43985-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43985-124">Header</span><span class="sxs-lookup"><span data-stu-id="43985-124">Header</span></span><br/>  | <dl> <span data-ttu-id="43985-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="43985-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="43985-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="43985-126">Library</span></span><br/> | <dl> <span data-ttu-id="43985-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="43985-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43985-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43985-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43985-129">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="43985-129">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="43985-130">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="43985-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




