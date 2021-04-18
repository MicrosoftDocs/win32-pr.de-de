---
description: Die getlocked-Methode ruft den Bearbeitungsstatus des Objekts ab (gesperrt oder entsperrt).
ms.assetid: ecd258db-36bf-41b6-9bdf-537efcf0a46a
title: 'Iamtimelineobj:: getlocked-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 472b7dedbdbd879d4fa49fe874fb9178d0ccdee4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365579"
---
# <a name="iamtimelineobjgetlocked-method"></a><span data-ttu-id="7df96-103">Iamtimelineobj:: getlocked-Methode</span><span class="sxs-lookup"><span data-stu-id="7df96-103">IAMTimelineObj::GetLocked method</span></span>

> [!Note]  
> <span data-ttu-id="7df96-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="7df96-104">\[Deprecated.</span></span> <span data-ttu-id="7df96-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="7df96-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7df96-106">Die `GetLocked` -Methode ruft den Bearbeitungs Zustand des-Objekts (gesperrt oder entsperrt) ab.</span><span class="sxs-lookup"><span data-stu-id="7df96-106">The `GetLocked` method retrieves the object's editing state (locked or unlocked).</span></span> <span data-ttu-id="7df96-107">Ein gesperrter Zustand zeigt an, dass das Objekt nicht bearbeitet werden sollte. ein Entsperrter Zustand gibt an, dass das Objekt bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7df96-107">A locked state indicates that the object should not be edited; an unlocked state indicates that the object can be edited.</span></span> <span data-ttu-id="7df96-108">Die Zeitachse erzwingt die Sperre nicht.</span><span class="sxs-lookup"><span data-stu-id="7df96-108">The timeline does not enforce the lock.</span></span> <span data-ttu-id="7df96-109">Die Einstellung gesperrt ist nur für die praktische Verwendung der Anwendung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7df96-109">The locked setting exists only for the convenience of the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="7df96-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7df96-110">Syntax</span></span>


```C++
 GetLocked(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="7df96-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7df96-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7df96-112">*pVal*</span><span class="sxs-lookup"><span data-stu-id="7df96-112">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="7df96-113">Empfängt den Bearbeitungs Zustand des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7df96-113">Receives the object's editing state.</span></span> <span data-ttu-id="7df96-114">Wenn der Wert **true** ist, wird das Objekt gesperrt und sollte nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="7df96-114">If the value is **TRUE**, the object is locked and should not be edited.</span></span> <span data-ttu-id="7df96-115">Wenn der Wert **false** ist, wird das Objekt entsperrt und kann bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="7df96-115">If **FALSE**, the object is unlocked and can be edited.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7df96-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7df96-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7df96-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="7df96-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7df96-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="7df96-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7df96-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7df96-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7df96-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7df96-120">Requirements</span></span>



| <span data-ttu-id="7df96-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7df96-121">Requirement</span></span> | <span data-ttu-id="7df96-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7df96-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7df96-123">Header</span><span class="sxs-lookup"><span data-stu-id="7df96-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7df96-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7df96-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7df96-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7df96-125">Library</span></span><br/> | <dl> <span data-ttu-id="7df96-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="7df96-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7df96-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7df96-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df96-128">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7df96-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="7df96-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="7df96-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




