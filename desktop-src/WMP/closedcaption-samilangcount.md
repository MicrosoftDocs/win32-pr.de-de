---
title: Closedcaption. samilangcount
description: Die samilangcount-Eigenschaft ruft die Anzahl der Sprachen ab, die von der aktuellen Sami-Datei unterstützt werden.
ms.assetid: ad2e776a-b430-46ee-9705-18d279e8715e
keywords:
- Closedcaption. samilangcount-Fenster Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILangCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d202ecc8bc18261ac4569f2251201e15911f91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359310"
---
# <a name="closedcaptionsamilangcount"></a><span data-ttu-id="41864-104">Closedcaption. samilangcount</span><span class="sxs-lookup"><span data-stu-id="41864-104">ClosedCaption.SAMILangCount</span></span>

<span data-ttu-id="41864-105">Die **samilangcount** -Eigenschaft ruft die Anzahl der Sprachen ab, die von der aktuellen Sami-Datei unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="41864-105">The **SAMILangCount** property retrieves the number of languages supported by the current SAMI file.</span></span>

``` syntax
player.closedCaption.SAMILangCount
```

## <a name="possible-values"></a><span data-ttu-id="41864-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="41864-106">Possible Values</span></span>

<span data-ttu-id="41864-107">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="41864-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="41864-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41864-108">Remarks</span></span>

<span data-ttu-id="41864-109">Diese Methode kann erst verwendet werden, wenn eine digitale Mediendatei (*Player*) geöffnet ist.**openstate** ist gleich 13).</span><span class="sxs-lookup"><span data-stu-id="41864-109">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="41864-110">**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="41864-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="41864-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41864-111">Requirements</span></span>



| <span data-ttu-id="41864-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41864-112">Requirement</span></span> | <span data-ttu-id="41864-113">Wert</span><span class="sxs-lookup"><span data-stu-id="41864-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="41864-114">Version</span><span class="sxs-lookup"><span data-stu-id="41864-114">Version</span></span><br/> | <span data-ttu-id="41864-115">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="41864-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="41864-116">DLL</span><span class="sxs-lookup"><span data-stu-id="41864-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="41864-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41864-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41864-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41864-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41864-119">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="41864-119">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="41864-120">**Closedcaption-Objekt**</span><span class="sxs-lookup"><span data-stu-id="41864-120">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="41864-121">**Closedcaption. getsamilangname**</span><span class="sxs-lookup"><span data-stu-id="41864-121">**ClosedCaption.getSAMILangName**</span></span>](closedcaption-getsamilangname.md)
</dt> <dt>

[<span data-ttu-id="41864-122">**Closedcaption. samilang**</span><span class="sxs-lookup"><span data-stu-id="41864-122">**ClosedCaption.SAMILang**</span></span>](closedcaption-samilang.md)
</dt> </dl>

 

 





