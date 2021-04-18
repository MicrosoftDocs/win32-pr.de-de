---
title: Downloadcollection. Item-Methode
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die Item-Methode ruft ein ausstehendes Download Objekt ab.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, downloadcollection-Klasse
- Download Collection-Klasse, Windows Media Player, Element-Methode
topic_type:
- apiref
api_name:
- DownloadCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57db60a776c71d9ff16eceb1584c79a125bbf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354721"
---
# <a name="downloadcollectionitem-method"></a><span data-ttu-id="2b9d0-108">Downloadcollection. Item-Methode</span><span class="sxs-lookup"><span data-stu-id="2b9d0-108">DownloadCollection.item method</span></span>

> [!Note]  
> <span data-ttu-id="2b9d0-109">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="2b9d0-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="2b9d0-110">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b9d0-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="2b9d0-111">Die **Item** -Methode ruft ein ausstehendes Download Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="2b9d0-111">The **item** method retrieves a pending download object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b9d0-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b9d0-112">Syntax</span></span>


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a><span data-ttu-id="2b9d0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b9d0-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b9d0-114">*ItemID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b9d0-114">*itemId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b9d0-115">**Zahl** (**Long**), die den Index des abzurufenden **Download** Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="2b9d0-115">**Number** (**long**) specifying the index of the **DownloadItem** to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b9d0-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b9d0-116">Return value</span></span>

<span data-ttu-id="2b9d0-117">Diese Methode gibt ein-Objekt vom Typ " **Downloader** " zurück.</span><span class="sxs-lookup"><span data-stu-id="2b9d0-117">This method returns a **DownloadItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b9d0-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b9d0-118">Remarks</span></span>

<span data-ttu-id="2b9d0-119">Der *ItemID* -Wert ist NULL basiert.</span><span class="sxs-lookup"><span data-stu-id="2b9d0-119">The *itemID* value is zero-based.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b9d0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b9d0-120">Requirements</span></span>



| <span data-ttu-id="2b9d0-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b9d0-121">Requirement</span></span> | <span data-ttu-id="2b9d0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="2b9d0-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2b9d0-123">Version</span><span class="sxs-lookup"><span data-stu-id="2b9d0-123">Version</span></span><br/> | <span data-ttu-id="2b9d0-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="2b9d0-124">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="2b9d0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2b9d0-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="2b9d0-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b9d0-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b9d0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b9d0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b9d0-128">**Download Collection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="2b9d0-128">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> <dt>

[<span data-ttu-id="2b9d0-129">**Download Item-Objekt**</span><span class="sxs-lookup"><span data-stu-id="2b9d0-129">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





