---
description: Die Methode "kreateemptynode" erstellt ein neues Zeitachsen Objekt.
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: 'Iamtimeline:: erkreateemptynode-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.CreateEmptyNode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 894126bea8f40537602aa1fe8898038245215914
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370639"
---
# <a name="iamtimelinecreateemptynode-method"></a><span data-ttu-id="dc330-103">Iamtimeline:: erkreateemptynode-Methode</span><span class="sxs-lookup"><span data-stu-id="dc330-103">IAMTimeline::CreateEmptyNode method</span></span>

> [!Note]  
> <span data-ttu-id="dc330-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="dc330-104">\[Deprecated.</span></span> <span data-ttu-id="dc330-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="dc330-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dc330-106">Die- `CreateEmptyNode` Methode erstellt ein neues Timeline-Objekt.</span><span class="sxs-lookup"><span data-stu-id="dc330-106">The `CreateEmptyNode` method creates a new timeline object.</span></span>

<span data-ttu-id="dc330-107">Verwenden Sie diese Methode, um Zeitachsen Objekte anstelle der **cokreatanstance** -Funktion zu erstellen, da diese Methode wichtige Initialisierungs Routinen ausführt.</span><span class="sxs-lookup"><span data-stu-id="dc330-107">Use this method to create timeline objects, rather than the **CoCreateInstance** function, because this method performs important initialization routines.</span></span> <span data-ttu-id="dc330-108">Jedes Objekt, das von dieser Methode erstellt wird, unterstützt mindestens die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle sowie andere Schnittstellen, die für diesen Objekttyp spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="dc330-108">Every object created by this method supports at least the [**IAMTimelineObj**](iamtimelineobj.md) interface, along with other interfaces specific to that type of object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc330-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc330-109">Syntax</span></span>


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="dc330-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc330-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc330-111">*ppobj* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dc330-111">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc330-112">Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des neuen Objekts.</span><span class="sxs-lookup"><span data-stu-id="dc330-112">Receives a pointer to the new object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="dc330-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="dc330-113">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="dc330-114">Member des enumerierten Typs der [**Zeitachse \_ \_**](timeline-major-type.md) , der den Typ des zu erstellenden Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="dc330-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc330-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc330-115">Return value</span></span>

<span data-ttu-id="dc330-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="dc330-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dc330-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dc330-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc330-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc330-118">Remarks</span></span>

<span data-ttu-id="dc330-119">Fügen Sie das neue-Objekt nicht zu einer anderen Timeline-Instanz hinzu.</span><span class="sxs-lookup"><span data-stu-id="dc330-119">Do not add the new object to another timeline instance.</span></span> <span data-ttu-id="dc330-120">Jedes Objekt in einer Zeitachse muss von dieser Zeitachse erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="dc330-120">Every object in a timeline must be created by that timeline.</span></span>

<span data-ttu-id="dc330-121">Wenn die Methode erfolgreich ausgeführt wird, weist die zurückgegebene [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="dc330-121">If the method succeeds, the [**IAMTimelineObj**](iamtimelineobj.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="dc330-122">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="dc330-122">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="dc330-123">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="dc330-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dc330-124">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="dc330-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dc330-125">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dc330-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dc330-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc330-126">Requirements</span></span>



| <span data-ttu-id="dc330-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc330-127">Requirement</span></span> | <span data-ttu-id="dc330-128">Wert</span><span class="sxs-lookup"><span data-stu-id="dc330-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc330-129">Header</span><span class="sxs-lookup"><span data-stu-id="dc330-129">Header</span></span><br/>  | <dl> <span data-ttu-id="dc330-130"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="dc330-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dc330-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc330-131">Library</span></span><br/> | <dl> <span data-ttu-id="dc330-132"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="dc330-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc330-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc330-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc330-134">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="dc330-134">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="dc330-135">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="dc330-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




