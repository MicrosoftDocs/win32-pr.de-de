---
title: Iwmpcdromburn burnformat (Eigenschaft)
description: Die burnformat-Eigenschaft ruft einen Wert ab, der den Typ der zu brennenden CD angibt.
ms.assetid: f60fcbd2-5d34-46f3-a2e2-29dac2ecf689
keywords:
- burnformat-Eigenschaften Fenster Media Player
- burnformat-Eigenschaft, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, burnformat (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnFormat
- IWMPCdromBurn.get_burnFormat
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17e379727376b1ce272a95cd77c688fa611b291a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361327"
---
# <a name="iwmpcdromburnburnformat-property"></a><span data-ttu-id="3434e-106">Iwmpcdromburn:: burnformat (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3434e-106">IWMPCdromBurn::burnFormat property</span></span>

<span data-ttu-id="3434e-107">Die **burnformat** -Eigenschaft ruft einen Wert ab, der den Typ der zu brennenden CD angibt.</span><span class="sxs-lookup"><span data-stu-id="3434e-107">The **burnFormat** property gets a value that indicates the type of CD to burn.</span></span>

<span data-ttu-id="3434e-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3434e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3434e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3434e-109">Syntax</span></span>


```CSharp
public WMPBurnFormat burnFormat {get;}
```


```VB

Public ReadOnly Property burnFormat As WMPBurnFormat
```





## <a name="property-value"></a><span data-ttu-id="3434e-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3434e-110">Property value</span></span>

<span data-ttu-id="3434e-111">Ein **WMPLib. wmpburnformat** , bei dem es sich um einen Wert aus der **wmpburnformat** -Enumeration handelt, der den Typ der zu brennenden CD angibt.</span><span class="sxs-lookup"><span data-stu-id="3434e-111">A **WMPLib.WMPBurnFormat** that is a value from the **WMPBurnFormat** enumeration that indicates the type of CD to burn.</span></span>

## <a name="requirements"></a><span data-ttu-id="3434e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3434e-112">Requirements</span></span>



| <span data-ttu-id="3434e-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3434e-113">Requirement</span></span> | <span data-ttu-id="3434e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="3434e-114">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3434e-115">Version</span><span class="sxs-lookup"><span data-stu-id="3434e-115">Version</span></span><br/>   | <span data-ttu-id="3434e-116">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="3434e-116">Windows Media Player 11</span></span><br/>                                                                             |
| <span data-ttu-id="3434e-117">Namespace</span><span class="sxs-lookup"><span data-stu-id="3434e-117">Namespace</span></span><br/> | <span data-ttu-id="3434e-118">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3434e-118">**WMPLib**</span></span><br/>                                                                                          |
| <span data-ttu-id="3434e-119">Assembly</span><span class="sxs-lookup"><span data-stu-id="3434e-119">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3434e-120"><dt>Interop. WMPLib (Interop.WMPLib.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3434e-120"><dt>Interop.WMPLib (Interop.WMPLib.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3434e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3434e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3434e-122">**Iwmpcdromburn-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="3434e-122">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3434e-123">**Wmpburnformat**</span><span class="sxs-lookup"><span data-stu-id="3434e-123">**WMPBurnFormat**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
</dt> </dl>

 

 





