---
title: ErrorItem. Condition
description: Die Condition-Eigenschaft ruft einen Wert ab, der die Bedingung für den Fehler angibt.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- ErrorItem. Condition-Windows-Media Player
topic_type:
- apiref
api_name:
- ErrorItem.condition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c498e7479a7a3e067dea2d8a562800351effd672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373938"
---
# <a name="erroritemcondition"></a><span data-ttu-id="709a1-104">ErrorItem. Condition</span><span class="sxs-lookup"><span data-stu-id="709a1-104">ErrorItem.condition</span></span>

<span data-ttu-id="709a1-105">Die **Condition** -Eigenschaft ruft einen Wert ab, der die Bedingung für den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="709a1-105">The **condition** property retrieves a value indicating the condition for the error.</span></span>

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a><span data-ttu-id="709a1-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="709a1-106">Possible Values</span></span>

<span data-ttu-id="709a1-107">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**), die den Bedingungs Code darstellt.</span><span class="sxs-lookup"><span data-stu-id="709a1-107">This property is a read-only **Number** (**long**) that represents the condition code.</span></span>

## <a name="remarks"></a><span data-ttu-id="709a1-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="709a1-108">Remarks</span></span>

<span data-ttu-id="709a1-109">Der Bedingungs Code ist ein Wert, der von Microsoft verwendet wird, um zusätzliche Informationen für die Mitarbeiter des technischen Supports bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="709a1-109">The condition code is a value that is used by Microsoft to provide additional information for technical support personnel.</span></span>

<span data-ttu-id="709a1-110">**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="709a1-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="709a1-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="709a1-111">Requirements</span></span>



| <span data-ttu-id="709a1-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="709a1-112">Requirement</span></span> | <span data-ttu-id="709a1-113">Wert</span><span class="sxs-lookup"><span data-stu-id="709a1-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="709a1-114">Version</span><span class="sxs-lookup"><span data-stu-id="709a1-114">Version</span></span><br/> | <span data-ttu-id="709a1-115">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="709a1-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="709a1-116">DLL</span><span class="sxs-lookup"><span data-stu-id="709a1-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="709a1-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="709a1-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="709a1-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="709a1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="709a1-119">**ErrorItem-Objekt**</span><span class="sxs-lookup"><span data-stu-id="709a1-119">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





