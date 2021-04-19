---
title: ErrorItem. errorcontext
description: Die errorcontext-Eigenschaft ruft einen Wert ab, der den Kontext des Fehlers angibt.
ms.assetid: 700d2bf0-dd3b-4211-99ea-58f952cf24b0
keywords:
- ErrorItem. errorcontext-Windows-Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorContext
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b9ed91d34645f08e7d3d28860ced9ca51420dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360289"
---
# <a name="erroritemerrorcontext"></a><span data-ttu-id="daffe-104">ErrorItem. errorcontext</span><span class="sxs-lookup"><span data-stu-id="daffe-104">ErrorItem.errorContext</span></span>

<span data-ttu-id="daffe-105">Die **errorcontext** -Eigenschaft ruft einen Wert ab, der den Kontext des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="daffe-105">The **errorContext** property retrieves a value indicating the context of the error.</span></span>

``` syntax
player.error.item(
        index
        ).errorContext
```

## <a name="possible-values"></a><span data-ttu-id="daffe-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="daffe-106">Possible Values</span></span>

<span data-ttu-id="daffe-107">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge** , die den Fehler Kontext Code darstellt.</span><span class="sxs-lookup"><span data-stu-id="daffe-107">This property is a read-only **String** that represents the error context code.</span></span>

## <a name="remarks"></a><span data-ttu-id="daffe-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="daffe-108">Remarks</span></span>

<span data-ttu-id="daffe-109">Der Fehler Kontext sind Informationen, die von Microsoft verwendet werden, um zusätzliche Informationen für den technischen Support zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="daffe-109">The error context is information that is used by Microsoft to provide additional information for technical support personnel.</span></span>

<span data-ttu-id="daffe-110">**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer eine leere Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="daffe-110">**Windows Media Player 10 Mobile:** This property always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="daffe-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="daffe-111">Requirements</span></span>



| <span data-ttu-id="daffe-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="daffe-112">Requirement</span></span> | <span data-ttu-id="daffe-113">Wert</span><span class="sxs-lookup"><span data-stu-id="daffe-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="daffe-114">Version</span><span class="sxs-lookup"><span data-stu-id="daffe-114">Version</span></span><br/> | <span data-ttu-id="daffe-115">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="daffe-115">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="daffe-116">DLL</span><span class="sxs-lookup"><span data-stu-id="daffe-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="daffe-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="daffe-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daffe-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="daffe-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daffe-119">**ErrorItem-Objekt**</span><span class="sxs-lookup"><span data-stu-id="daffe-119">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





