---
description: Tritt auf, wenn ein Tablet-Kontext zerstört wird.
ms.assetid: 805289d8-267e-488b-8092-6b07b37dd6d4
title: 'Itableteventsink:: contextdestroy-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.ContextDestroy
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c9b5d78d4ce4032c1a7a2082fb749afc5a39949a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530032"
---
# <a name="itableteventsinkcontextdestroy-method"></a><span data-ttu-id="68fe0-103">Itableteventsink:: contextdestroy-Methode</span><span class="sxs-lookup"><span data-stu-id="68fe0-103">ITabletEventSink::ContextDestroy method</span></span>

<span data-ttu-id="68fe0-104">Tritt auf, wenn ein Tablet-Kontext zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="68fe0-104">Occurs when a tablet context is being destroyed.</span></span>

## <a name="syntax"></a><span data-ttu-id="68fe0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="68fe0-105">Syntax</span></span>


```C++
HRESULT ContextDestroy(
  [in] TABLET_CONTEXT_ID tcid
);
```



## <a name="parameters"></a><span data-ttu-id="68fe0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="68fe0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68fe0-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68fe0-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68fe0-108">Der Bezeichner des zu zerstörenden Tablet-Kontexts.</span><span class="sxs-lookup"><span data-stu-id="68fe0-108">The identifier of the tablet context being destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68fe0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68fe0-109">Return value</span></span>

<span data-ttu-id="68fe0-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="68fe0-110">This method can return one of these values.</span></span>



| <span data-ttu-id="68fe0-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="68fe0-111">Return code</span></span>                                                                            | <span data-ttu-id="68fe0-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68fe0-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="68fe0-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="68fe0-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="68fe0-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="68fe0-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="68fe0-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="68fe0-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="68fe0-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="68fe0-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="68fe0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68fe0-117">Requirements</span></span>



| <span data-ttu-id="68fe0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68fe0-118">Requirement</span></span> | <span data-ttu-id="68fe0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="68fe0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68fe0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68fe0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="68fe0-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68fe0-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="68fe0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68fe0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="68fe0-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="68fe0-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="68fe0-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="68fe0-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="68fe0-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="68fe0-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68fe0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68fe0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68fe0-127">**Itableteventsink-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="68fe0-127">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




