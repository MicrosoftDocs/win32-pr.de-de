---
title: Facteritem. getdataat-Methode
description: Ruft den angegebenen Leistungs Zählers von einem bestimmten Punkt im Diagramm ab.
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
keywords:
- Getdataat-Methode (Sysmon)
- Getdataat-Methode "sysmon", "ratteritem"-Objekt
- Inititeritem-Objekt (Sysmon), getdataat-Methode
topic_type:
- apiref
api_name:
- CounterItem.GetDataAt
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354d8242e6cb765980878a7783805416bb1a1009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517921"
---
# <a name="counteritemgetdataat-method"></a><span data-ttu-id="bc4a8-106">Facteritem. getdataat-Methode</span><span class="sxs-lookup"><span data-stu-id="bc4a8-106">CounterItem.GetDataAt method</span></span>

<span data-ttu-id="bc4a8-107">Ruft den angegebenen Leistungs Zählers von einem bestimmten Punkt im Diagramm ab.</span><span class="sxs-lookup"><span data-stu-id="bc4a8-107">Retrieves the specified counter value from a specific point in the graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc4a8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc4a8-108">Syntax</span></span>


```VB
CounterItem.GetDataAt( _
  ByVal index As Long, _
  ByVal which As SysmonDataType, _
  ByRef variant As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="bc4a8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc4a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc4a8-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc4a8-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc4a8-111">NULL basierter Index des Diagramm Punkts, dessen Wert abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc4a8-111">Zero-based index of the graph point whose value you want to retrieve.</span></span> <span data-ttu-id="bc4a8-112">Gültige Werte liegen im Bereich von 0 bis ([**Systemmonitor. datapointcount**](systemmonitor-datapointcount.md) -1).</span><span class="sxs-lookup"><span data-stu-id="bc4a8-112">Valid values range from 0 to ([**SystemMonitor.DataPointCount**](systemmonitor-datapointcount.md) - 1).</span></span>

</dd> <dt>

<span data-ttu-id="bc4a8-113">*welches* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc4a8-113">*which* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc4a8-114">Der Typ des abzurufenden Leistungs Zählers, z. b. der durchschnittliche Wert des Zählers, der im Diagramm Fenster angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bc4a8-114">Type of counter value to retrieve, for example, the average value of the counter as displayed in the graph window.</span></span> <span data-ttu-id="bc4a8-115">Mögliche Werte finden Sie unter [**sysmondatatype**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).</span><span class="sxs-lookup"><span data-stu-id="bc4a8-115">For possible values, see [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).</span></span>

</dd> <dt>

<span data-ttu-id="bc4a8-116">*Variant* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bc4a8-116">*variant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc4a8-117">Der abgerufene Wert des Leistungs Zählers.</span><span class="sxs-lookup"><span data-stu-id="bc4a8-117">Counter value that was retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc4a8-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc4a8-118">Return value</span></span>

<span data-ttu-id="bc4a8-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bc4a8-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc4a8-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc4a8-120">Remarks</span></span>

<span data-ttu-id="bc4a8-121">Verwenden Sie diese Methode nur, wenn</span><span class="sxs-lookup"><span data-stu-id="bc4a8-121">Use this method only if</span></span>

-   <span data-ttu-id="bc4a8-122">[**Systemmonitor. Display Type**](systemmonitor-displaytype.md) ist auf sysmonlinegraph festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bc4a8-122">[**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is set to sysmonLineGraph</span></span>
-   <span data-ttu-id="bc4a8-123">[**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) ist auf sysmonlogfiles oder sysmonsqllog festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bc4a8-123">[**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonLogFiles or sysmonSqlLog</span></span>

## <a name="requirements"></a><span data-ttu-id="bc4a8-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc4a8-124">Requirements</span></span>



| <span data-ttu-id="bc4a8-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc4a8-125">Requirement</span></span> | <span data-ttu-id="bc4a8-126">Wert</span><span class="sxs-lookup"><span data-stu-id="bc4a8-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc4a8-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc4a8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bc4a8-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc4a8-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc4a8-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc4a8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bc4a8-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc4a8-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc4a8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bc4a8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc4a8-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="bc4a8-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc4a8-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc4a8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc4a8-134">**Ratteritem**</span><span class="sxs-lookup"><span data-stu-id="bc4a8-134">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="bc4a8-135">**"Count. getstatistics"**</span><span class="sxs-lookup"><span data-stu-id="bc4a8-135">**CounterItem.GetStatistics**</span></span>](counteritem-getstatistics.md)
</dt> <dt>

[<span data-ttu-id="bc4a8-136">**"Count. GetValue"**</span><span class="sxs-lookup"><span data-stu-id="bc4a8-136">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





