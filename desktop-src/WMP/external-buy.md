---
title: Extern. Buy-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die Methode kaufen initiiert den Kauf eines Satzes von Medien Elementen.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- Windows-Media Player "Methode kaufen"
- Kaufmethode Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, Methode kaufen
topic_type:
- apiref
api_name:
- External.buy
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5ffee188372e33ed4ceadf1bb1ee2ea0f986207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354212"
---
# <a name="externalbuy-method"></a><span data-ttu-id="f2cfa-108">Extern. Buy-Methode</span><span class="sxs-lookup"><span data-stu-id="f2cfa-108">External.buy method</span></span>

> [!Note]  
> <span data-ttu-id="f2cfa-109">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="f2cfa-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f2cfa-110">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f2cfa-111">Die Methode **kaufen** initiiert den Kauf eines Satzes von Medien Elementen.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-111">The **buy** method initiates the purchase of a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2cfa-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2cfa-112">Syntax</span></span>


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a><span data-ttu-id="f2cfa-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2cfa-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2cfa-114">*ViewType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2cfa-114">*ViewType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2cfa-115">Eine **Zeichenfolge** , die den Typ des zu erstellenden Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-115">**String** that specifies the type of item to be purchased.</span></span> <span data-ttu-id="f2cfa-116">Der Aufrufer muss diesen Parameter auf eine der folgenden [Bibliotheks Speicherort Konstanten](library-location-constants.md)festlegen:</span><span class="sxs-lookup"><span data-stu-id="f2cfa-116">The caller must set this parameter to one of the following [library location constants](library-location-constants.md):</span></span>

<span data-ttu-id="f2cfa-117">Cplistid</span><span class="sxs-lookup"><span data-stu-id="f2cfa-117">CPListID</span></span>

<span data-ttu-id="f2cfa-118">Cptrackid</span><span class="sxs-lookup"><span data-stu-id="f2cfa-118">CPTrackID</span></span>

<span data-ttu-id="f2cfa-119">Cpalbumid</span><span class="sxs-lookup"><span data-stu-id="f2cfa-119">CPAlbumID</span></span>

</dd> <dt>

<span data-ttu-id="f2cfa-120">*Viewids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2cfa-120">*ViewIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2cfa-121">**Zeichenfolge** , die die durch Semikolons getrennten IDs der zu erwerbenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-121">**String** containing the IDs, delimited by semicolons, of the items to be purchased.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2cfa-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2cfa-122">Return value</span></span>

<span data-ttu-id="f2cfa-123">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2cfa-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2cfa-124">Requirements</span></span>



| <span data-ttu-id="f2cfa-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2cfa-125">Requirement</span></span> | <span data-ttu-id="f2cfa-126">Wert</span><span class="sxs-lookup"><span data-stu-id="f2cfa-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f2cfa-127">Version</span><span class="sxs-lookup"><span data-stu-id="f2cfa-127">Version</span></span><br/> | <span data-ttu-id="f2cfa-128">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-128">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="f2cfa-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f2cfa-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="f2cfa-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2cfa-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2cfa-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2cfa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2cfa-132">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="f2cfa-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="f2cfa-133">**Extern. Download**</span><span class="sxs-lookup"><span data-stu-id="f2cfa-133">**External.download**</span></span>](external-download.md)
</dt> <dt>

[<span data-ttu-id="f2cfa-134">**Iwmpcontentpartner:: kaufen**</span><span class="sxs-lookup"><span data-stu-id="f2cfa-134">**IWMPContentPartner::Buy**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[<span data-ttu-id="f2cfa-135">**Erwerben von Medieninhalten**</span><span class="sxs-lookup"><span data-stu-id="f2cfa-135">**Purchasing Media Content**</span></span>](purchasing-media-content.md)
</dt> </dl>

 

 





