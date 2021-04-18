---
title: Iwmpcdromburn burnstate (Eigenschaft)
description: Die burnstate-Eigenschaft ruft einen Enumerationswert ab, der den aktuellen Brenn Zustand angibt.
ms.assetid: 2bb543f9-9e4c-4425-99d6-ac89ef7f5807
keywords:
- burnstate-Eigenschaften Fenster Media Player
- burnstate-Eigenschaft, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, burnstate (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnState
- IWMPCdromBurn.get_burnState
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b1aa8ec39f032e8f130a75370131bd2894c64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360897"
---
# <a name="iwmpcdromburnburnstate-property"></a><span data-ttu-id="0b72f-106">Iwmpcdromburn:: burnstate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0b72f-106">IWMPCdromBurn::burnState property</span></span>

<span data-ttu-id="0b72f-107">Die **burnstate** -Eigenschaft ruft einen Enumerationswert ab, der den aktuellen Brenn Zustand angibt.</span><span class="sxs-lookup"><span data-stu-id="0b72f-107">The **burnState** property gets an enumeration value that indicates the current burn state.</span></span>

<span data-ttu-id="0b72f-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0b72f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b72f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b72f-109">Syntax</span></span>


```CSharp
public WMPBurnState burnState {get;}
```


```VB

Public ReadOnly Property burnState As WMPBurnState
```





## <a name="property-value"></a><span data-ttu-id="0b72f-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0b72f-110">Property value</span></span>

<span data-ttu-id="0b72f-111">Ein **WMPLib. wmpburnstate** , bei dem es sich um einen Wert aus der **wmpburnstate** -Enumeration handelt, der den aktuellen Zustand angibt.</span><span class="sxs-lookup"><span data-stu-id="0b72f-111">A **WMPLib.WMPBurnState** that is a value from the **WMPBurnState** enumeration that indicates the current state.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b72f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b72f-112">Requirements</span></span>



| <span data-ttu-id="0b72f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b72f-113">Requirement</span></span> | <span data-ttu-id="0b72f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="0b72f-114">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b72f-115">Version</span><span class="sxs-lookup"><span data-stu-id="0b72f-115">Version</span></span><br/>   | <span data-ttu-id="0b72f-116">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="0b72f-116">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="0b72f-117">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b72f-117">Namespace</span></span><br/> | <span data-ttu-id="0b72f-118">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0b72f-118">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0b72f-119">Assembly</span><span class="sxs-lookup"><span data-stu-id="0b72f-119">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0b72f-120"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0b72f-120"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b72f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b72f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b72f-122">**Iwmpcdromburn-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0b72f-122">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0b72f-123">**Wmpburnstate**</span><span class="sxs-lookup"><span data-stu-id="0b72f-123">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





