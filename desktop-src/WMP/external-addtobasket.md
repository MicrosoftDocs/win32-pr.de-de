---
title: Extern. adddebasket-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. adddebasket-Methode
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- adddebasket-Methode, Windows Media Player
- adddebasket-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, adddebasket-Methode
topic_type:
- apiref
api_name:
- External.addToBasket
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2fab549dec9e24b0c5bbe61f5511e375c4c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361997"
---
# <a name="externaladdtobasket-method"></a><span data-ttu-id="09864-107">Extern. adddebasket-Methode</span><span class="sxs-lookup"><span data-stu-id="09864-107">External.addToBasket method</span></span>

> [!Note]  
> <span data-ttu-id="09864-108">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="09864-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="09864-109">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="09864-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="09864-110">Die **adddebasket** -Methode fügt dem Listen Bereich (auch als Warenkorb bezeichnet) in Windows Media Player Medienelemente hinzu.</span><span class="sxs-lookup"><span data-stu-id="09864-110">The **addToBasket** method adds media items to the list pane (also called the basket) in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="09864-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="09864-111">Syntax</span></span>


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a><span data-ttu-id="09864-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="09864-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09864-113">*ViewType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09864-113">*ViewType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09864-114">Eine **Zeichenfolge** , die den Typ des Elements angibt, das dem Listen Bereich hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="09864-114">**String** that specifies the type of item being added to the list pane.</span></span> <span data-ttu-id="09864-115">Der Aufrufer muss diesen Parameter auf eine der folgenden [Bibliotheks Speicherort Konstanten](library-location-constants.md)festlegen:</span><span class="sxs-lookup"><span data-stu-id="09864-115">The caller must set this parameter to one of the following [library location constants](library-location-constants.md):</span></span>

<span data-ttu-id="09864-116">Cplistid</span><span class="sxs-lookup"><span data-stu-id="09864-116">CPListID</span></span>

<span data-ttu-id="09864-117">Cptrackid</span><span class="sxs-lookup"><span data-stu-id="09864-117">CPTrackID</span></span>

<span data-ttu-id="09864-118">Cpalbumid</span><span class="sxs-lookup"><span data-stu-id="09864-118">CPAlbumID</span></span>

<span data-ttu-id="09864-119">Cpartist</span><span class="sxs-lookup"><span data-stu-id="09864-119">CPArtist</span></span>

<span data-ttu-id="09864-120">Cpgenreid</span><span class="sxs-lookup"><span data-stu-id="09864-120">CPGenreID</span></span>

<span data-ttu-id="09864-121">Cpalbumsubgenreid</span><span class="sxs-lookup"><span data-stu-id="09864-121">CPAlbumSubGenreID</span></span>

<span data-ttu-id="09864-122">Cpradioid</span><span class="sxs-lookup"><span data-stu-id="09864-122">CPRadioID</span></span>

</dd> <dt>

<span data-ttu-id="09864-123">*Viewids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09864-123">*ViewIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09864-124">**Zeichenfolge** , die die durch Semikolons getrennten IDs der Elemente enthält, die dem Listen Bereich hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="09864-124">**String** containing the IDs, delimited by semicolons, of the items to be added to the list pane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09864-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09864-125">Return value</span></span>

<span data-ttu-id="09864-126">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="09864-126">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="09864-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09864-127">Requirements</span></span>



| <span data-ttu-id="09864-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09864-128">Requirement</span></span> | <span data-ttu-id="09864-129">Wert</span><span class="sxs-lookup"><span data-stu-id="09864-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09864-130">Version</span><span class="sxs-lookup"><span data-stu-id="09864-130">Version</span></span><br/> | <span data-ttu-id="09864-131">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="09864-131">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="09864-132">DLL</span><span class="sxs-lookup"><span data-stu-id="09864-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="09864-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09864-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09864-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09864-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09864-135">**Externalobject für Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="09864-135">**ExternalObject for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="09864-136">**Extern. baskettitle**</span><span class="sxs-lookup"><span data-stu-id="09864-136">**External.basketTitle**</span></span>](external-baskettitle.md)
</dt> </dl>

 

 





