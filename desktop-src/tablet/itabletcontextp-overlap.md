---
description: Verschiebt einen Tablet-Kontext an die Vorder-oder Rückseite der Eingabe Warteschlange.
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: 'Itabletcontextp:: überlappungsmethode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.Overlap
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: b009bc08dddb15bc7aa5b12c8846ea66c4a52e56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359472"
---
# <a name="itabletcontextpoverlap-method"></a><span data-ttu-id="f0ded-103">Itabletcontextp:: überlappungsmethode</span><span class="sxs-lookup"><span data-stu-id="f0ded-103">ITabletContextP::Overlap method</span></span>

<span data-ttu-id="f0ded-104">Verschiebt einen Tablet-Kontext an die Vorder-oder Rückseite der Eingabe Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="f0ded-104">Moves a tablet context to the front or back of the input queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ded-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0ded-105">Syntax</span></span>


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a><span data-ttu-id="f0ded-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0ded-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0ded-107">*btop* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0ded-107">*bTop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ded-108">Gibt an, ob der Tablet-Kontext an den oberen oder unteren Rand der Eingabe Warteschlange verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0ded-108">Indicates if the tablet context should be moved to the top or bottom of the input queue.</span></span>

</dd> <dt>

<span data-ttu-id="f0ded-109">*pdwtcid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0ded-109">*pdwtcid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ded-110">Der Tablet-Kontext Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="f0ded-110">The tablet context identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0ded-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0ded-111">Return value</span></span>

<span data-ttu-id="f0ded-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f0ded-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f0ded-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f0ded-113">Return code</span></span>                                                                            | <span data-ttu-id="f0ded-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0ded-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="f0ded-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ded-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="f0ded-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="f0ded-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="f0ded-117"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ded-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="f0ded-118">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f0ded-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f0ded-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0ded-119">Requirements</span></span>



| <span data-ttu-id="f0ded-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0ded-120">Requirement</span></span> | <span data-ttu-id="f0ded-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f0ded-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ded-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0ded-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f0ded-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0ded-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f0ded-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0ded-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f0ded-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f0ded-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f0ded-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0ded-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0ded-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f0ded-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0ded-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0ded-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ded-129">**Itabletcontextp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f0ded-129">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




