---
title: Downloadcollection. RemoveItem-Methode
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Mit der RemoveItem-Methode wird ein Download Element aus einer Download Sammlung entfernt.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- RemoveItem-Methode, Windows-Media Player
- RemoveItem-Methode, Windows Media Player, downloadcollection-Klasse
- Download Collection-Klasse, Windows Media Player, RemoveItem-Methode
topic_type:
- apiref
api_name:
- DownloadCollection.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1798665b79327b7956c1b78509b55cc6e6dd70c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370843"
---
# <a name="downloadcollectionremoveitem-method"></a><span data-ttu-id="a9bd8-108">Downloadcollection. RemoveItem-Methode</span><span class="sxs-lookup"><span data-stu-id="a9bd8-108">DownloadCollection.removeItem method</span></span>

> [!Note]  
> <span data-ttu-id="a9bd8-109">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="a9bd8-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a9bd8-110">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a9bd8-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a9bd8-111">Mit der **RemoveItem** -Methode wird ein Download Element aus einer Download Sammlung entfernt.</span><span class="sxs-lookup"><span data-stu-id="a9bd8-111">The **removeItem** method removes a download item from a download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9bd8-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9bd8-112">Syntax</span></span>


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a><span data-ttu-id="a9bd8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9bd8-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9bd8-114">*ItemID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9bd8-114">*itemID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bd8-115">**Number** (**Long**), der den Index des zu entfernenden **Download** Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="a9bd8-115">**Number** (**long**) specifying the index of the **DownloadItem** to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9bd8-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9bd8-116">Return value</span></span>

<span data-ttu-id="a9bd8-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a9bd8-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9bd8-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9bd8-118">Remarks</span></span>

<span data-ttu-id="a9bd8-119">Wenn der von der *ItemID* dargestellte Download ausgeführt wird, wird der Download durch diese Methode abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a9bd8-119">If the download represented by *itemID* is in progress, this method cancels the download.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9bd8-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9bd8-120">Requirements</span></span>



| <span data-ttu-id="a9bd8-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9bd8-121">Requirement</span></span> | <span data-ttu-id="a9bd8-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a9bd8-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a9bd8-123">Version</span><span class="sxs-lookup"><span data-stu-id="a9bd8-123">Version</span></span><br/> | <span data-ttu-id="a9bd8-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="a9bd8-124">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="a9bd8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a9bd8-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="a9bd8-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9bd8-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9bd8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9bd8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9bd8-128">**Download Collection. Item**</span><span class="sxs-lookup"><span data-stu-id="a9bd8-128">**DownloadCollection.item**</span></span>](downloadcollection-item.md)
</dt> <dt>

[<span data-ttu-id="a9bd8-129">**Download Collection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="a9bd8-129">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





