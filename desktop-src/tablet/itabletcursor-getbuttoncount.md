---
description: Ruft die Anzahl der Schaltflächen auf dem Tablettstift ab.
ms.assetid: ae4ce670-769a-4f00-b728-285020f09934
title: 'Itabletcursor:: getbuttoncount-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButtonCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 08fdf24b2a0b69b7830a683786f18fc5df0805b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363733"
---
# <a name="itabletcursorgetbuttoncount-method"></a><span data-ttu-id="5ea56-103">Itabletcursor:: getbuttoncount-Methode</span><span class="sxs-lookup"><span data-stu-id="5ea56-103">ITabletCursor::GetButtonCount method</span></span>

<span data-ttu-id="5ea56-104">Ruft die Anzahl der Schaltflächen auf dem Tablettstift ab.</span><span class="sxs-lookup"><span data-stu-id="5ea56-104">Retrieves the number of buttons on the tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ea56-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ea56-105">Syntax</span></span>


```C++
HRESULT GetButtonCount(
  [out] ULONG *pcButtons
);
```



## <a name="parameters"></a><span data-ttu-id="5ea56-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ea56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ea56-107">*pcbuttons* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5ea56-107">*pcButtons* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ea56-108">Die Anzahl der Schaltflächen auf dem Tablettstift.</span><span class="sxs-lookup"><span data-stu-id="5ea56-108">The count of buttons on the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ea56-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ea56-109">Return value</span></span>

<span data-ttu-id="5ea56-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5ea56-110">This method can return one of these values.</span></span>



| <span data-ttu-id="5ea56-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5ea56-111">Return code</span></span>                                                                            | <span data-ttu-id="5ea56-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ea56-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="5ea56-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5ea56-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="5ea56-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="5ea56-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="5ea56-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="5ea56-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="5ea56-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="5ea56-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5ea56-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ea56-117">Requirements</span></span>



| <span data-ttu-id="5ea56-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ea56-118">Requirement</span></span> | <span data-ttu-id="5ea56-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5ea56-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea56-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ea56-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5ea56-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ea56-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5ea56-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ea56-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5ea56-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5ea56-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5ea56-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5ea56-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ea56-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5ea56-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ea56-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ea56-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea56-127">**Itabletcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5ea56-127">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




