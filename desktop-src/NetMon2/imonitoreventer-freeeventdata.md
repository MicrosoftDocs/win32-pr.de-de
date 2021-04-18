---
description: Die Methode "freeventdata" gibt den zugeordneten Speicherplatz für die nmeventdata-Struktur frei.
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: 'Imonitoreventer:: freeventdata-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.FreeEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c71b7563e00bfceb220ce1c2bf109339267fbabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343642"
---
# <a name="imonitoreventerfreeeventdata-method"></a><span data-ttu-id="0207a-103">Imonitoreventer:: freeventdata-Methode</span><span class="sxs-lookup"><span data-stu-id="0207a-103">IMonitorEventer::FreeEventData method</span></span>

<span data-ttu-id="0207a-104">Die Methode " **freeventdata** " gibt den zugeordneten Speicherplatz für die [**nmeventdata**](nmeventdata.md) -Struktur frei.</span><span class="sxs-lookup"><span data-stu-id="0207a-104">The **FreeEventData** method frees space allocated for the [**NMEVENTDATA**](nmeventdata.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0207a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0207a-105">Syntax</span></span>


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="0207a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0207a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0207a-107">*pnmeventdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0207a-107">*pNMEventData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0207a-108">Adresse der [**nmeventdata**](nmeventdata.md) -Struktur, deren Arbeitsspeicher freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0207a-108">Address of the [**NMEVENTDATA**](nmeventdata.md) structure, the memory of which is freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0207a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0207a-109">Return value</span></span>

<span data-ttu-id="0207a-110">Diese Methode gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="0207a-110">This method returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0207a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0207a-111">Remarks</span></span>

<span data-ttu-id="0207a-112">Diese Methode wird von Monitoren aufgerufen, um den Arbeitsspeicher freizugeben, den Sie für die Ereignisdaten Struktur zuordnen.</span><span class="sxs-lookup"><span data-stu-id="0207a-112">Monitors call this method to free the memory they allocate for the event data structure.</span></span> <span data-ttu-id="0207a-113">Beachten Sie, dass während des Monitors weiterhin ein Zeiger auf Zeichen folgen in einer zugeordneten [**nmeventdata**](nmeventdata.md) -Struktur vorhanden ist, muss der Arbeitsspeicher für diese Zeichen folgen freigegeben werden, bevor die Methode " **freieventdata** " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0207a-113">Be aware that while the monitor still has a pointer to strings in an allocated [**NMEVENTDATA**](nmeventdata.md) structure, the memory for these strings must be freed before the **FreeEventData** method is called.</span></span>

<span data-ttu-id="0207a-114">Weitere Informationen zum Zuordnen von Arbeitsspeicher für eine [**nmeventdata**](nmeventdata.md) -Struktur finden Sie unter [**imonitoreventer:: geteventdata**](imonitoreventer-geteventdata.md).</span><span class="sxs-lookup"><span data-stu-id="0207a-114">For more information about how to allocate memory for an [**NMEVENTDATA**](nmeventdata.md) structure, see [**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0207a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0207a-115">Requirements</span></span>



| <span data-ttu-id="0207a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0207a-116">Requirement</span></span> | <span data-ttu-id="0207a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0207a-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0207a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0207a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0207a-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0207a-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0207a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0207a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0207a-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0207a-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0207a-122">Header</span><span class="sxs-lookup"><span data-stu-id="0207a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0207a-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0207a-123"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0207a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0207a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0207a-125">**Imonitoreventer Enter**</span><span class="sxs-lookup"><span data-stu-id="0207a-125">**IMonitorEventer**</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="0207a-126">**Imonitoreventer:: geteventdata**</span><span class="sxs-lookup"><span data-stu-id="0207a-126">**IMonitorEventer::GetEventData**</span></span>](imonitoreventer-geteventdata.md)
</dt> <dt>

[<span data-ttu-id="0207a-127">**Nmeventdata**</span><span class="sxs-lookup"><span data-stu-id="0207a-127">**NMEVENTDATA**</span></span>](nmeventdata.md)
</dt> </dl>

 

 




