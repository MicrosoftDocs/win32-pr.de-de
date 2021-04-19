---
description: Tritt auf, wenn ein Tablettstift in den Bereich der Erkennung des Digitalisierungsprogramms kommt.
ms.assetid: 22be233a-fc33-4a8f-91b6-28b2f2910b69
title: 'Itableteventsink:: Cursor Input Range-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorInRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eec2b4f309480ecaecd50de2120d701c916b6fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350143"
---
# <a name="itableteventsinkcursorinrange-method"></a><span data-ttu-id="2926a-103">Itableteventsink:: Cursor Input Range-Methode</span><span class="sxs-lookup"><span data-stu-id="2926a-103">ITabletEventSink::CursorInRange method</span></span>

<span data-ttu-id="2926a-104">Tritt auf, wenn ein Tablettstift in den Bereich der Erkennung des Digitalisierungsprogramms kommt.</span><span class="sxs-lookup"><span data-stu-id="2926a-104">Occurs when a stylus comes within the digitizer's range of detection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2926a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2926a-105">Syntax</span></span>


```C++
HRESULT CursorInRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="2926a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2926a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2926a-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2926a-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2926a-108">Der Bezeichner des tablettobjekts, das den Tablettstift erkannt hat.</span><span class="sxs-lookup"><span data-stu-id="2926a-108">The identifier of the tablet object that detected the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="2926a-109">*zid*</span><span class="sxs-lookup"><span data-stu-id="2926a-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="2926a-110">Der Bezeichner des tablettstiftobjekts, das im Bereich des Digitalisierungsprogramms liegt.</span><span class="sxs-lookup"><span data-stu-id="2926a-110">The identifier of the stylus object that has come in range of the digitizer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2926a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2926a-111">Return value</span></span>

<span data-ttu-id="2926a-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2926a-112">This method can return one of these values.</span></span>



| <span data-ttu-id="2926a-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2926a-113">Return code</span></span>                                                                            | <span data-ttu-id="2926a-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2926a-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="2926a-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2926a-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="2926a-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="2926a-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="2926a-117"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="2926a-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="2926a-118">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2926a-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2926a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2926a-119">Requirements</span></span>



| <span data-ttu-id="2926a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2926a-120">Requirement</span></span> | <span data-ttu-id="2926a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2926a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2926a-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2926a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2926a-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2926a-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2926a-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2926a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2926a-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2926a-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2926a-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2926a-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="2926a-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2926a-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2926a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2926a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2926a-129">**Itableteventsink-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2926a-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




