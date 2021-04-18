---
title: Extern. viewparameters
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. viewparameters
ms.assetid: 0afabe35-2857-413a-a662-1a76d3fb75fe
keywords:
- Externe. viewparameters-Fenster Media Player
topic_type:
- apiref
api_name:
- External.viewParameters
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0adec580a68bd3f6b92beef1de814729848179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364724"
---
# <a name="externalviewparameters"></a><span data-ttu-id="b4002-105">Extern. viewparameters</span><span class="sxs-lookup"><span data-stu-id="b4002-105">External.viewParameters</span></span>

> [!Note]  
> <span data-ttu-id="b4002-106">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="b4002-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b4002-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b4002-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b4002-108">Die **viewparameters** -Eigenschaft ruft Parameter ab, die der aktuellen Ansicht in Windows Media Player zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b4002-108">The **viewParameters** property retrieves parameters associated with the current view in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4002-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4002-109">Syntax</span></span>

<span data-ttu-id="b4002-110">**Window. extern. viewparameters**</span><span class="sxs-lookup"><span data-stu-id="b4002-110">**window.external.viewParameters**</span></span>

## <a name="possible-values"></a><span data-ttu-id="b4002-111">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="b4002-111">Possible Values</span></span>

<span data-ttu-id="b4002-112">Diese Eigenschaft gibt eine schreibgeschützte **Zeichenfolge** zurück.</span><span class="sxs-lookup"><span data-stu-id="b4002-112">This property returns a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4002-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4002-113">Remarks</span></span>

<span data-ttu-id="b4002-114">Diese Eigenschaft ruft Parameter ab, die zuvor vom Onlinespeicher festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="b4002-114">This property retrieves parameters that were previously set by the online store.</span></span> <span data-ttu-id="b4002-115">Der Online Shop kann z. b. Ansichts Parameter im *viewparameame-* Parameter der [changeView](external-changeview.md) -Methode oder im Parameter *para* meters der [changeviewonlinelist](external-changeviewonlinelist.md) -Methode angeben.</span><span class="sxs-lookup"><span data-stu-id="b4002-115">For example, the online store can specify view parameters in the *ViewParams* parameter of the [changeView](external-changeview.md) method or the *Params* parameter of the [changeViewOnlineList](external-changeviewonlinelist.md) method.</span></span>

<span data-ttu-id="b4002-116">Sicht Parameter werden von Windows Media Player nicht interpretiert.</span><span class="sxs-lookup"><span data-stu-id="b4002-116">View parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="b4002-117">Sie werden vom Online Shop erstellt und sind nur für den Online Shop von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="b4002-117">They are created by the online store and have meaning only to the online store.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4002-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4002-118">Requirements</span></span>



| <span data-ttu-id="b4002-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4002-119">Requirement</span></span> | <span data-ttu-id="b4002-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b4002-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4002-121">Version</span><span class="sxs-lookup"><span data-stu-id="b4002-121">Version</span></span><br/> | <span data-ttu-id="b4002-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="b4002-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="b4002-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b4002-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="b4002-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4002-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4002-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4002-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4002-126">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="b4002-126">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





