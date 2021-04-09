---
description: Gibt an, ob sich ein XPS-Druckauftrag in der spoolingphase oder der Renderingphase befindet.
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: Eprintxpsjoboperation-Enumeration (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobOperation
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 917993be2af6e7a78afaec1ad4749dadcaebecba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756391"
---
# <a name="eprintxpsjoboperation-enumeration"></a><span data-ttu-id="f1258-103">Eprintxpsjoboperation-Enumeration</span><span class="sxs-lookup"><span data-stu-id="f1258-103">EPrintXPSJobOperation enumeration</span></span>

<span data-ttu-id="f1258-104">Gibt an, ob sich ein XPS-Druckauftrag in der spoolingphase oder der Renderingphase befindet.</span><span class="sxs-lookup"><span data-stu-id="f1258-104">Specifies whether an XPS print job is in the spooling or the rendering phase.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1258-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1258-105">Syntax</span></span>


```C++
typedef enum tagEPrintXPSJobOperation { 
  kJobProduction,
  kJobConsumption
} EPrintXPSJobOperation;
```



## <a name="constants"></a><span data-ttu-id="f1258-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="f1258-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f1258-107"><span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kjobproduction**</span><span class="sxs-lookup"><span data-stu-id="f1258-107"><span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**</span></span>
</dt> <dd>

<span data-ttu-id="f1258-108">Der XPS-Auftrag ist Spoolvorgang.</span><span class="sxs-lookup"><span data-stu-id="f1258-108">The XPS job is spooling.</span></span>

</dd> <dt>

<span data-ttu-id="f1258-109"><span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kjobverbrauch**</span><span class="sxs-lookup"><span data-stu-id="f1258-109"><span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**</span></span>
</dt> <dd>

<span data-ttu-id="f1258-110">Der XPS-Auftrag ist Rendering.</span><span class="sxs-lookup"><span data-stu-id="f1258-110">The XPS job is rendering.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1258-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1258-111">Remarks</span></span>

<span data-ttu-id="f1258-112">Diese Enumeration wird primär als Parameter für die [**reportjobprocessingprogress**](reportjobprocessingprogress.md) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1258-112">This enumeration is primarily used as a parameter for the [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1258-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1258-113">Requirements</span></span>



| <span data-ttu-id="f1258-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1258-114">Requirement</span></span> | <span data-ttu-id="f1258-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f1258-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1258-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1258-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f1258-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1258-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f1258-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1258-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f1258-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1258-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f1258-120">Header</span><span class="sxs-lookup"><span data-stu-id="f1258-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1258-121"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1258-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




