---
description: Die GetGroup-Methode ruft eine angegebene Gruppe ab.
ms.assetid: 4ff651e5-a3aa-4da9-af23-a3a2bdbf7c5b
title: 'Iamtimeline:: GetGroup-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1241a125698cf78c1138d9264ecd8c73ff78056c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366918"
---
# <a name="iamtimelinegetgroup-method"></a><span data-ttu-id="68f03-103">Iamtimeline:: GetGroup-Methode</span><span class="sxs-lookup"><span data-stu-id="68f03-103">IAMTimeline::GetGroup method</span></span>

> [!Note]  
> <span data-ttu-id="68f03-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="68f03-104">\[Deprecated.</span></span> <span data-ttu-id="68f03-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="68f03-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="68f03-106">Die- `GetGroup` Methode ruft eine angegebene Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="68f03-106">The `GetGroup` method retrieves a specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="68f03-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="68f03-107">Syntax</span></span>


```C++
HRESULT GetGroup(
  [out] IAMTimelineObj **ppGroup,
        long           WhichGroup
);
```



## <a name="parameters"></a><span data-ttu-id="68f03-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="68f03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68f03-109">*ppgroup* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="68f03-109">*ppGroup* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68f03-110">Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="68f03-110">Receives a pointer to the group's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="68f03-111">*Whichgroup*</span><span class="sxs-lookup"><span data-stu-id="68f03-111">*WhichGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="68f03-112">Der Index der abzurufenden Gruppe, basierend auf der Reihenfolge, in der die Gruppen der Zeitachse hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="68f03-112">Index of the group to retrieve, based on the order in which the groups were added to the timeline.</span></span> <span data-ttu-id="68f03-113">Die erste Gruppe, die der Zeitachse hinzugefügt wird, hat einen Index von 0.</span><span class="sxs-lookup"><span data-stu-id="68f03-113">The first group added to the timeline has an index of 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68f03-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68f03-114">Return value</span></span>

<span data-ttu-id="68f03-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="68f03-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="68f03-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="68f03-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="68f03-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68f03-117">Remarks</span></span>

<span data-ttu-id="68f03-118">Wenn die Methode erfolgreich ausgeführt wird, weist die zurückgegebene **iamtimelineobj** -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="68f03-118">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="68f03-119">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="68f03-119">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="68f03-120">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="68f03-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="68f03-121">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="68f03-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="68f03-122">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="68f03-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="68f03-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68f03-123">Requirements</span></span>



| <span data-ttu-id="68f03-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68f03-124">Requirement</span></span> | <span data-ttu-id="68f03-125">Wert</span><span class="sxs-lookup"><span data-stu-id="68f03-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68f03-126">Header</span><span class="sxs-lookup"><span data-stu-id="68f03-126">Header</span></span><br/>  | <dl> <span data-ttu-id="68f03-127"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="68f03-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="68f03-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="68f03-128">Library</span></span><br/> | <dl> <span data-ttu-id="68f03-129"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="68f03-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68f03-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68f03-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68f03-131">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="68f03-131">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="68f03-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="68f03-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




