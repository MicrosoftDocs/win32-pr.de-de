---
description: Die transgetcount-Methode ruft die Anzahl der Übergänge für dieses Objekt ab.
ms.assetid: f7fb4a99-c841-4680-b7f1-e4d887f12707
title: 'Iamtimelinetransable:: transgetcount-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 81b5fc6301b319b8716a6db25fce2b1e5c2d4961
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354804"
---
# <a name="iamtimelinetransabletransgetcount-method"></a><span data-ttu-id="3e145-103">Iamtimelinetransable:: transgetcount-Methode</span><span class="sxs-lookup"><span data-stu-id="3e145-103">IAMTimelineTransable::TransGetCount method</span></span>

> [!Note]  
> <span data-ttu-id="3e145-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3e145-104">\[Deprecated.</span></span> <span data-ttu-id="3e145-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="3e145-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3e145-106">Die- `TransGetCount` Methode ruft die Anzahl der Übergänge für dieses-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="3e145-106">The `TransGetCount` method retrieves the number of transitions on this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e145-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e145-107">Syntax</span></span>


```C++
HRESULT TransGetCount(
   long *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="3e145-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e145-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e145-109">*pCount*</span><span class="sxs-lookup"><span data-stu-id="3e145-109">*pCount*</span></span> 
</dt> <dd>

<span data-ttu-id="3e145-110">Empfängt die Anzahl der Übergänge.</span><span class="sxs-lookup"><span data-stu-id="3e145-110">Receives the number of transitions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e145-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e145-111">Return value</span></span>

<span data-ttu-id="3e145-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="3e145-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3e145-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3e145-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e145-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e145-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3e145-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="3e145-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3e145-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="3e145-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3e145-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3e145-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3e145-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e145-118">Requirements</span></span>



| <span data-ttu-id="3e145-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e145-119">Requirement</span></span> | <span data-ttu-id="3e145-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3e145-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e145-121">Header</span><span class="sxs-lookup"><span data-stu-id="3e145-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3e145-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="3e145-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3e145-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3e145-123">Library</span></span><br/> | <dl> <span data-ttu-id="3e145-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="3e145-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e145-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e145-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e145-126">**Iamtimelinetransable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3e145-126">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="3e145-127">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="3e145-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




