---
title: Externes. oncolorchange-Ereignis
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Externes. oncolorchange-Ereignis
ms.assetid: f2cd44b1-c813-479b-b847-96ddb9572697
keywords:
- Externe. oncolorchange-Ereignisfenster Media Player
topic_type:
- apiref
api_name:
- External.OnColorChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029c8bb860443ed026737c7413be2bed8862c6d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370126"
---
# <a name="externaloncolorchange-event"></a><span data-ttu-id="39c32-105">Externes. oncolorchange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="39c32-105">External.OnColorChange Event</span></span>

> [!Note]  
> <span data-ttu-id="39c32-106">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="39c32-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="39c32-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39c32-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="39c32-108">Das **oncolorchange** -Ereignis tritt auf, wenn sich die Farbe der Windows Media Player-Benutzeroberfläche ändert.</span><span class="sxs-lookup"><span data-stu-id="39c32-108">The **OnColorChange** event occurs when the color of the Windows Media Player user interface changes.</span></span>

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="39c32-109">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="39c32-109">Possible Values</span></span>

<span data-ttu-id="39c32-110">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die den Namen der Funktion im Skript angibt, die von Windows Media Player bei Auftreten des Ereignisses aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="39c32-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="39c32-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="39c32-111">Parameters</span></span>

<span data-ttu-id="39c32-112">Die Funktion, die dieses Ereignis behandelt, nimmt keine Parameter an.</span><span class="sxs-lookup"><span data-stu-id="39c32-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="39c32-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39c32-113">Remarks</span></span>

<span data-ttu-id="39c32-114">Benutzer können die Farbe der Windows Media Player-Benutzeroberfläche ändern.</span><span class="sxs-lookup"><span data-stu-id="39c32-114">Users can change the color of the Windows Media Player user interface.</span></span> <span data-ttu-id="39c32-115">Sie können dieses Ereignis verwenden, um die Darstellung der gehosteten Webseite so anzupassen, dass Sie dem Player entspricht.</span><span class="sxs-lookup"><span data-stu-id="39c32-115">You can use this event to customize the appearance of your hosted webpage to match the Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="39c32-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39c32-116">Requirements</span></span>



| <span data-ttu-id="39c32-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39c32-117">Requirement</span></span> | <span data-ttu-id="39c32-118">Wert</span><span class="sxs-lookup"><span data-stu-id="39c32-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39c32-119">Version</span><span class="sxs-lookup"><span data-stu-id="39c32-119">Version</span></span><br/> | <span data-ttu-id="39c32-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="39c32-120">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="39c32-121">DLL</span><span class="sxs-lookup"><span data-stu-id="39c32-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="39c32-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39c32-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c32-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39c32-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c32-124">**Externes Objekt für den Typ 2-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="39c32-124">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





