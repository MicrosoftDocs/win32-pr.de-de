---
title: Count. scalefactor (Eigenschaft)
description: Ruft den Skalierungsfaktor ab, mit dem der indikatorenwert dargestellt wird, oder legt ihn fest
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- Scalefactor-Eigenschaft (Sysmon)
- Scalefactor-Eigenschaft "sysmon", "ratteritem"-Klasse
- Namteritem Class sysmon, scalefactor-Eigenschaft
topic_type:
- apiref
api_name:
- CounterItem.ScaleFactor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9a04df634fe54c82230ade679afb3259519173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340797"
---
# <a name="counteritemscalefactor-property"></a><span data-ttu-id="b52df-106">Count. scalefactor (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b52df-106">CounterItem.ScaleFactor property</span></span>

<span data-ttu-id="b52df-107">Ruft den Skalierungsfaktor ab, mit dem der indikatorenwert dargestellt wird, oder legt ihn fest</span><span class="sxs-lookup"><span data-stu-id="b52df-107">Retrieves or sets the scale factor used to graph the counter value.</span></span>

<span data-ttu-id="b52df-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b52df-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b52df-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b52df-109">Syntax</span></span>


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a><span data-ttu-id="b52df-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b52df-110">Property value</span></span>

<span data-ttu-id="b52df-111">Der Skalierungsfaktor, der beim Anzeigen der dargestellten Werte für Werte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b52df-111">Scale factor used in displaying the graphed counter values.</span></span> <span data-ttu-id="b52df-112">Gültige Werte liegen im Bereich von-9 bis 9 (die Werte entsprechen 0,000000001-100000000,0).</span><span class="sxs-lookup"><span data-stu-id="b52df-112">Valid values range from -9 to 9 (the values correspond to 0.000000001 - 100000000.0).</span></span>

<span data-ttu-id="b52df-113">**Vor Windows Vista:** Gültige Werte reichen von-7 bis 7 (die Werte entsprechen 0,0000001-1000000,0).</span><span class="sxs-lookup"><span data-stu-id="b52df-113">**Prior to Windows Vista:** Valid values range from -7 to 7 (the values correspond to 0.0000001 - 1000000.0).</span></span>

## <a name="remarks"></a><span data-ttu-id="b52df-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b52df-114">Remarks</span></span>

<span data-ttu-id="b52df-115">Legen Sie diese Eigenschaft nur fest, wenn Sie den standardmäßigen Skalierungsfaktor des Zählers ändern möchten (jeder Counter definiert seinen eigenen Skalierungsfaktor).</span><span class="sxs-lookup"><span data-stu-id="b52df-115">Only set this property if you want to change the counter's default scale factor (each counter defines its own scale factor).</span></span> <span data-ttu-id="b52df-116">Der Wert dieser Eigenschaft wird auf "Integer. MaxValue" festgelegt, wenn der Leistungs Besatz den Standard Skalierungsfaktor verwendet, um die Werte zu Graphen.</span><span class="sxs-lookup"><span data-stu-id="b52df-116">The value of this property is set to Integer.MaxValue if the counter is using its default scale factor to graph the values.</span></span>

## <a name="requirements"></a><span data-ttu-id="b52df-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b52df-117">Requirements</span></span>



| <span data-ttu-id="b52df-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b52df-118">Requirement</span></span> | <span data-ttu-id="b52df-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b52df-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b52df-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b52df-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b52df-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b52df-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b52df-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b52df-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b52df-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b52df-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b52df-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b52df-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b52df-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b52df-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b52df-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b52df-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b52df-127">**Ratteritem**</span><span class="sxs-lookup"><span data-stu-id="b52df-127">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="b52df-128">**Systemmonitor. scaledefit**</span><span class="sxs-lookup"><span data-stu-id="b52df-128">**SystemMonitor.ScaleToFit**</span></span>](systemmonitor-scaletofit.md)
</dt> </dl>

 

 





