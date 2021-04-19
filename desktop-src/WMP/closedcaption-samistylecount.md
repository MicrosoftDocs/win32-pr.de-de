---
title: Closedcaption. samistylecount
description: Die samistylecount-Eigenschaft ruft die Anzahl der Stile ab, die von der aktuellen Sami-Datei unterstützt werden.
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- Closedcaption. samistylecount-Fenster Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyleCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab48fc6660065da1635b58b67784f2ab0ff91b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367548"
---
# <a name="closedcaptionsamistylecount"></a><span data-ttu-id="321c2-104">Closedcaption. samistylecount</span><span class="sxs-lookup"><span data-stu-id="321c2-104">ClosedCaption.SAMIStyleCount</span></span>

<span data-ttu-id="321c2-105">Die **samistylecount** -Eigenschaft ruft die Anzahl der Stile ab, die von der aktuellen Sami-Datei unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="321c2-105">The **SAMIStyleCount** property retrieves the number of styles supported by the current SAMI file.</span></span>

``` syntax
player.closedCaption.SAMIStyleCount
```

## <a name="possible-values"></a><span data-ttu-id="321c2-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="321c2-106">Possible Values</span></span>

<span data-ttu-id="321c2-107">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="321c2-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="321c2-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="321c2-108">Remarks</span></span>

<span data-ttu-id="321c2-109">Diese Methode kann erst verwendet werden, wenn eine digitale Mediendatei (*Player*) geöffnet ist.**openstate** ist gleich 13).</span><span class="sxs-lookup"><span data-stu-id="321c2-109">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="321c2-110">**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="321c2-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="321c2-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="321c2-111">Requirements</span></span>



| <span data-ttu-id="321c2-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="321c2-112">Requirement</span></span> | <span data-ttu-id="321c2-113">Wert</span><span class="sxs-lookup"><span data-stu-id="321c2-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="321c2-114">Version</span><span class="sxs-lookup"><span data-stu-id="321c2-114">Version</span></span><br/> | <span data-ttu-id="321c2-115">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="321c2-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="321c2-116">DLL</span><span class="sxs-lookup"><span data-stu-id="321c2-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="321c2-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="321c2-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="321c2-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="321c2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321c2-119">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="321c2-119">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="321c2-120">**Closedcaption-Objekt**</span><span class="sxs-lookup"><span data-stu-id="321c2-120">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="321c2-121">**Closedcaption. getsamistylename**</span><span class="sxs-lookup"><span data-stu-id="321c2-121">**ClosedCaption.getSAMIStyleName**</span></span>](closedcaption-getsamistylename.md)
</dt> <dt>

[<span data-ttu-id="321c2-122">**Closedcaption. samistyle**</span><span class="sxs-lookup"><span data-stu-id="321c2-122">**ClosedCaption.SAMIStyle**</span></span>](closedcaption-samistyle.md)
</dt> </dl>

 

 





