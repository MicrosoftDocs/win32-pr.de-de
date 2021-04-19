---
description: Aktualisiert den Tablet-Digitalisierer auf Fenster Speicherort-Mapping-Koordinaten.
ms.assetid: 2984b87b-620e-4e5d-a3cc-4c3f4c89bae3
title: 'Itabletcontextp:: trackinputrect-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.TrackInputRect
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 4529263b81933651db35b88262b11e979d39e6f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353945"
---
# <a name="itabletcontextptrackinputrect-method"></a><span data-ttu-id="5209c-103">Itabletcontextp:: trackinputrect-Methode</span><span class="sxs-lookup"><span data-stu-id="5209c-103">ITabletContextP::TrackInputRect method</span></span>

<span data-ttu-id="5209c-104">Aktualisiert den Tablet-Digitalisierer auf Fenster Speicherort-Mapping-Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="5209c-104">Updates the tablet digitizer to window location mapping coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="5209c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5209c-105">Syntax</span></span>


```C++
HRESULT TrackInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a><span data-ttu-id="5209c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5209c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5209c-107">*prcinput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5209c-107">*prcInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5209c-108">Das neue Eingabefenster Rechteck nach dem Aktualisieren der Zuordnung zwischen der Fenster-und der Digitalisierungs Koordinate.</span><span class="sxs-lookup"><span data-stu-id="5209c-108">The new input window rectangle after updating the mapping between the window and digitizer coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5209c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5209c-109">Return value</span></span>

<span data-ttu-id="5209c-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5209c-110">This method can return one of these values.</span></span>



| <span data-ttu-id="5209c-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5209c-111">Return code</span></span>                                                                            | <span data-ttu-id="5209c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5209c-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="5209c-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5209c-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="5209c-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="5209c-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="5209c-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="5209c-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="5209c-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="5209c-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5209c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5209c-117">Remarks</span></span>

<span data-ttu-id="5209c-118">Wenn die Position des Fensters auf dem Bildschirm geändert wird, wird diese Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5209c-118">Call this method anytime the location of the window on the screen changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="5209c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5209c-119">Requirements</span></span>



| <span data-ttu-id="5209c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5209c-120">Requirement</span></span> | <span data-ttu-id="5209c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5209c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5209c-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5209c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5209c-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5209c-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5209c-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5209c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5209c-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5209c-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5209c-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5209c-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="5209c-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5209c-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5209c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5209c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5209c-129">**Itabletcontextp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5209c-129">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




