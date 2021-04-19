---
description: Die setlocked-Methode legt den Bearbeitungs Zustand des-Objekts auf gesperrt oder entsperrt fest.
ms.assetid: 801b8bf0-5c7a-4122-9038-6b0d8bdc5da3
title: 'Iamtimelineobj:: setlocked-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b8707aa86b651553dde2f9f9b57c84169a9969b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359690"
---
# <a name="iamtimelineobjsetlocked-method"></a><span data-ttu-id="c0ddf-103">Iamtimelineobj:: setlocked-Methode</span><span class="sxs-lookup"><span data-stu-id="c0ddf-103">IAMTimelineObj::SetLocked method</span></span>

> [!Note]  
> <span data-ttu-id="c0ddf-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-104">\[Deprecated.</span></span> <span data-ttu-id="c0ddf-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="c0ddf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c0ddf-106">Die `SetLocked` -Methode legt den Bearbeitungs Zustand des-Objekts auf gesperrt oder entsperrt fest.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-106">The `SetLocked` method sets the object's editing state to locked or unlocked.</span></span>

<span data-ttu-id="c0ddf-107">Ein gesperrter Zustand zeigt an, dass das Objekt nicht bearbeitet werden sollte. ein Entsperrter Zustand gibt an, dass das Objekt bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-107">A locked state indicates that the object should not be edited; an unlocked state indicates that the object can be edited.</span></span> <span data-ttu-id="c0ddf-108">Die Zeitachse erzwingt die Sperre nicht.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-108">The timeline does not enforce the lock.</span></span> <span data-ttu-id="c0ddf-109">Die Einstellung gesperrt ist nur für die praktische Verwendung der Anwendung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-109">The locked setting exists only for the convenience of the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ddf-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0ddf-110">Syntax</span></span>


```C++
HRESULT SetLocked(
   BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="c0ddf-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0ddf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0ddf-112">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="c0ddf-112">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="c0ddf-113">Boolescher Wert, der den Bearbeitungs Zustand des-Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-113">Boolean value that specifies the object's editing state.</span></span> <span data-ttu-id="c0ddf-114">**True** gibt an, dass das Objekt gesperrt ist und nicht bearbeitet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-114">If **TRUE**, the object is locked and should not be edited.</span></span> <span data-ttu-id="c0ddf-115">Wenn der Wert **false** ist, wird das Objekt entsperrt und kann bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-115">If **FALSE**, the object is unlocked and can be edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0ddf-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0ddf-116">Return value</span></span>

<span data-ttu-id="c0ddf-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c0ddf-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0ddf-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0ddf-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c0ddf-120">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c0ddf-121">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c0ddf-122">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c0ddf-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0ddf-123">Requirements</span></span>



| <span data-ttu-id="c0ddf-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0ddf-124">Requirement</span></span> | <span data-ttu-id="c0ddf-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c0ddf-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ddf-126">Header</span><span class="sxs-lookup"><span data-stu-id="c0ddf-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c0ddf-127"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c0ddf-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c0ddf-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c0ddf-128">Library</span></span><br/> | <dl> <span data-ttu-id="c0ddf-129"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="c0ddf-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0ddf-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0ddf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ddf-131">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c0ddf-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="c0ddf-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="c0ddf-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




