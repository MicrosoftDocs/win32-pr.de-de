---
description: Tritt auf, wenn der Cursor über den Tablet-Digitalisierer bewegt wird.
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: 'Itableteventsink:: Cursor move-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorMove
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f6950e0b30c1b8fc8ccf3e60a8aaa05b9eeb3215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364231"
---
# <a name="itableteventsinkcursormove-method"></a><span data-ttu-id="0d13b-103">Itableteventsink:: Cursor move-Methode</span><span class="sxs-lookup"><span data-stu-id="0d13b-103">ITabletEventSink::CursorMove method</span></span>

<span data-ttu-id="0d13b-104">Tritt auf, wenn der Cursor über den Tablet-Digitalisierer bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="0d13b-104">Occurs when the cursor moves over the tablet digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d13b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d13b-105">Syntax</span></span>


```C++
HRESULT CursorMove(
   TABLET_CONTEXT_ID tcid,
   CURSOR_ID         cid,
   HWND              hWnd,
   LONG              xPos,
   LONG              yPos
);
```



## <a name="parameters"></a><span data-ttu-id="0d13b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d13b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d13b-107">*TCID*</span><span class="sxs-lookup"><span data-stu-id="0d13b-107">*tcid*</span></span> 
</dt> <dd>

<span data-ttu-id="0d13b-108">Eindeutiger dentifier des Tablet-Digitalisierungsprogramms.</span><span class="sxs-lookup"><span data-stu-id="0d13b-108">Unique dentifier of the tablet digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="0d13b-109">*zid*</span><span class="sxs-lookup"><span data-stu-id="0d13b-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="0d13b-110">Eindeutiger Bezeichner des Tablettstifts.</span><span class="sxs-lookup"><span data-stu-id="0d13b-110">Unique identifier of the tablet stylus.</span></span>

</dd> <dt>

<span data-ttu-id="0d13b-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="0d13b-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="0d13b-112">Das Fenster, in dem der Cursor verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="0d13b-112">The window over which the cursor moved.</span></span>

</dd> <dt>

<span data-ttu-id="0d13b-113">*XPos*</span><span class="sxs-lookup"><span data-stu-id="0d13b-113">*xPos*</span></span> 
</dt> <dd>

<span data-ttu-id="0d13b-114">Die X-Position des Tablettstifts.</span><span class="sxs-lookup"><span data-stu-id="0d13b-114">The X position of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="0d13b-115">*YPos*</span><span class="sxs-lookup"><span data-stu-id="0d13b-115">*yPos*</span></span> 
</dt> <dd>

<span data-ttu-id="0d13b-116">Die Y-Position des Tablettstifts.</span><span class="sxs-lookup"><span data-stu-id="0d13b-116">The Y position of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d13b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d13b-117">Return value</span></span>

<span data-ttu-id="0d13b-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0d13b-118">This method can return one of these values.</span></span>



| <span data-ttu-id="0d13b-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0d13b-119">Return code</span></span>                                                                            | <span data-ttu-id="0d13b-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d13b-120">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="0d13b-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0d13b-121"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0d13b-122">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="0d13b-122">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="0d13b-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="0d13b-123"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0d13b-124">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0d13b-124">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0d13b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d13b-125">Requirements</span></span>



| <span data-ttu-id="0d13b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d13b-126">Requirement</span></span> | <span data-ttu-id="0d13b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0d13b-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d13b-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d13b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0d13b-129">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d13b-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0d13b-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d13b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0d13b-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0d13b-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0d13b-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0d13b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="0d13b-133"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d13b-133"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d13b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d13b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d13b-135">**Itableteventsink-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0d13b-135">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




