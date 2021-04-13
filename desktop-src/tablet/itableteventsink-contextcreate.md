---
description: Tritt auf, wenn ein neuer Tablet-Kontext erstellt wird.
ms.assetid: 64e1f778-90c1-417d-a80b-37aeecffd411
title: 'Itableteventsink:: contextcreate-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.ContextCreate
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e622a246c7c317cf9e3373cbd3791108ed071e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349409"
---
# <a name="itableteventsinkcontextcreate-method"></a><span data-ttu-id="7db4e-103">Itableteventsink:: contextcreate-Methode</span><span class="sxs-lookup"><span data-stu-id="7db4e-103">ITabletEventSink::ContextCreate method</span></span>

<span data-ttu-id="7db4e-104">Tritt auf, wenn ein neuer Tablet-Kontext erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7db4e-104">Occurs when a new tablet context is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="7db4e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7db4e-105">Syntax</span></span>


```C++
HRESULT ContextCreate(
  [in] TABLET_CONTEXT_ID tcid
);
```



## <a name="parameters"></a><span data-ttu-id="7db4e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7db4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7db4e-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7db4e-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7db4e-108">Der Bezeichner des zu erstellenden Tablet-Kontexts.</span><span class="sxs-lookup"><span data-stu-id="7db4e-108">The identifier of the tablet context being created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7db4e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7db4e-109">Return value</span></span>

<span data-ttu-id="7db4e-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7db4e-110">This method can return one of these values.</span></span>



| <span data-ttu-id="7db4e-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7db4e-111">Return code</span></span>                                                                            | <span data-ttu-id="7db4e-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7db4e-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="7db4e-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7db4e-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="7db4e-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="7db4e-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="7db4e-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="7db4e-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="7db4e-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7db4e-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7db4e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7db4e-117">Requirements</span></span>



| <span data-ttu-id="7db4e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7db4e-118">Requirement</span></span> | <span data-ttu-id="7db4e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7db4e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7db4e-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7db4e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7db4e-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7db4e-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7db4e-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7db4e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7db4e-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7db4e-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7db4e-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7db4e-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="7db4e-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7db4e-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7db4e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7db4e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7db4e-127">**Itableteventsink-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7db4e-127">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




