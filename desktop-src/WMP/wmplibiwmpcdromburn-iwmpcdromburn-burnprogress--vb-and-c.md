---
title: Iwmpcdromburn-burnprogress (Eigenschaft)
description: Die burnprogress-Eigenschaft ruft den Fortschritt der CD-brennen als Prozentsatz ab.
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- burnprogress-Eigenschaften Fenster Media Player
- burnprogress-Eigenschaft, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, burnprogress (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnProgress
- IWMPCdromBurn.get_burnProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 835c8c1091941437c226427ddb3ef53e8c577b5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372580"
---
# <a name="iwmpcdromburnburnprogress-property"></a><span data-ttu-id="60fd5-106">Iwmpcdromburn:: burnprogress (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="60fd5-106">IWMPCdromBurn::burnProgress property</span></span>

<span data-ttu-id="60fd5-107">Die **burnprogress** -Eigenschaft ruft den Fortschritt der CD-brennen als Prozentsatz ab.</span><span class="sxs-lookup"><span data-stu-id="60fd5-107">The **burnProgress** property gets the CD burning progress as percent complete.</span></span>

<span data-ttu-id="60fd5-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="60fd5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="60fd5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="60fd5-109">Syntax</span></span>


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="60fd5-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="60fd5-110">Property value</span></span>

<span data-ttu-id="60fd5-111">Ein **System. Int32** -Wert, der der Fortschritts Wert ist.</span><span class="sxs-lookup"><span data-stu-id="60fd5-111">A **System.Int32** that is the progress value.</span></span> <span data-ttu-id="60fd5-112">Die Statuswerte liegen im Bereich von 0 bis 100.</span><span class="sxs-lookup"><span data-stu-id="60fd5-112">Progress values range from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="60fd5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60fd5-113">Remarks</span></span>

<span data-ttu-id="60fd5-114">Der Statuswert stellt den abgeschlossenen Prozentsatz des gesamten Brennvorgangs dar, einschließlich aller stagingvorgänge.</span><span class="sxs-lookup"><span data-stu-id="60fd5-114">The progress value represents the completed percentage of the entire burning process, including any staging operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="60fd5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60fd5-115">Requirements</span></span>



| <span data-ttu-id="60fd5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60fd5-116">Requirement</span></span> | <span data-ttu-id="60fd5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="60fd5-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60fd5-118">Version</span><span class="sxs-lookup"><span data-stu-id="60fd5-118">Version</span></span><br/>   | <span data-ttu-id="60fd5-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="60fd5-119">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="60fd5-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="60fd5-120">Namespace</span></span><br/> | <span data-ttu-id="60fd5-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="60fd5-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="60fd5-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="60fd5-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="60fd5-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="60fd5-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60fd5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60fd5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60fd5-125">**Iwmpcdromburn-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="60fd5-125">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





