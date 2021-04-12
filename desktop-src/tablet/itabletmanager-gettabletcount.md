---
description: Ruft die Anzahl der Tablets ab, die an das System angefügt sind.
ms.assetid: b2027336-611b-4d17-8943-f16770effaf8
title: 'Itabletmanager:: gettabletcount-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager.GetTabletCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fbdd485c44bc67b3ecaec5aa279d4bc20e18d167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218366"
---
# <a name="itabletmanagergettabletcount-method"></a><span data-ttu-id="bb43f-103">Itabletmanager:: gettabletcount-Methode</span><span class="sxs-lookup"><span data-stu-id="bb43f-103">ITabletManager::GetTabletCount method</span></span>

<span data-ttu-id="bb43f-104">Ruft die Anzahl der Tablets ab, die an das System angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="bb43f-104">Retrieves the number of tablets attached to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb43f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb43f-105">Syntax</span></span>


```C++
HRESULT GetTabletCount(
  [out] ULONG *pcTablets
);
```



## <a name="parameters"></a><span data-ttu-id="bb43f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb43f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb43f-107">*pctablets* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bb43f-107">*pcTablets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb43f-108">Die Anzahl der Tablets, die an das System angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="bb43f-108">The number of tablets attached to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb43f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb43f-109">Return value</span></span>

<span data-ttu-id="bb43f-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bb43f-110">This method can return one of these values.</span></span>



| <span data-ttu-id="bb43f-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bb43f-111">Return code</span></span>                                                                            | <span data-ttu-id="bb43f-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb43f-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="bb43f-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bb43f-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="bb43f-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="bb43f-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="bb43f-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="bb43f-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="bb43f-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="bb43f-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bb43f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb43f-117">Requirements</span></span>



| <span data-ttu-id="bb43f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb43f-118">Requirement</span></span> | <span data-ttu-id="bb43f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bb43f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb43f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb43f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bb43f-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb43f-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bb43f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb43f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bb43f-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bb43f-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="bb43f-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bb43f-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb43f-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb43f-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb43f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb43f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb43f-127">**Itabletmanager-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="bb43f-127">**ITabletManager Interface**</span></span>](itabletmanager.md)
</dt> </dl>

 

 




