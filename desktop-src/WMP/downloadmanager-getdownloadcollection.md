---
title: Download Manager. getdownloadcollection-Methode
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Mit der getdownloadcollection-Methode wird die angegebene Download Auflistung abgerufen.
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- getdownloadcollection-Methode, Windows Media Player
- getdownloadcollection-Methode, Windows Media Player, Download Manager-Klasse
- Download Manager-Klasse, Windows Media Player, getdownloadcollection-Methode
topic_type:
- apiref
api_name:
- DownloadManager.getDownloadCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e879d82c3f49db08d75b8aec37271e8d966019e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367598"
---
# <a name="downloadmanagergetdownloadcollection-method"></a><span data-ttu-id="0f1de-108">Download Manager. getdownloadcollection-Methode</span><span class="sxs-lookup"><span data-stu-id="0f1de-108">DownloadManager.getDownloadCollection method</span></span>

> [!Note]  
> <span data-ttu-id="0f1de-109">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="0f1de-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="0f1de-110">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0f1de-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="0f1de-111">Mit der **getdownloadcollection** -Methode wird die angegebene Download Auflistung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0f1de-111">The **getDownloadCollection** method retrieves the specified download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f1de-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f1de-112">Syntax</span></span>


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a><span data-ttu-id="0f1de-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f1de-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f1de-114">*CollectionId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f1de-114">*collectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f1de-115">**Zahl** (**Long**), die die ID der abzurufenden Download Auflistung angibt.</span><span class="sxs-lookup"><span data-stu-id="0f1de-115">**Number** (**long**) specifying the ID of the download collection to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f1de-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f1de-116">Return value</span></span>

<span data-ttu-id="0f1de-117">Diese Methode gibt ein **downloadcollection** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="0f1de-117">This method returns a **DownloadCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f1de-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f1de-118">Remarks</span></span>

<span data-ttu-id="0f1de-119">Sie müssen zuerst *Download Manager* anrufen. " **kreatedownloadcollection** " zum Erstellen einer neuen Sammlung und zum Abrufen des ID-Werts.</span><span class="sxs-lookup"><span data-stu-id="0f1de-119">You must first call *DownloadManager*.**createDownloadCollection** to create a new collection and retrieve its ID value.</span></span>

<span data-ttu-id="0f1de-120">Eine vorhandene Download Sammlung kann Elemente enthalten, die als abgebrochen markiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0f1de-120">An existing download collection may contain items that have been marked as cancelled.</span></span>

<span data-ttu-id="0f1de-121">Echt Zeit Download Elemente, die nicht in einer vorherigen Sitzung abgeschlossen wurden, werden nicht als Teil der Sammlung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0f1de-121">Real-time download items not completed in a prior session are not retrieved as part of the collection.</span></span> <span data-ttu-id="0f1de-122">Hintergrund Downloads, die vor der aktuellen Sitzung abgeschlossen wurden, verbleiben bis zum Entfernen in der Download Auflistung.</span><span class="sxs-lookup"><span data-stu-id="0f1de-122">Background downloads that were completed prior to the current session remain in the download collection until removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f1de-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f1de-123">Requirements</span></span>



| <span data-ttu-id="0f1de-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f1de-124">Requirement</span></span> | <span data-ttu-id="0f1de-125">Wert</span><span class="sxs-lookup"><span data-stu-id="0f1de-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f1de-126">Version</span><span class="sxs-lookup"><span data-stu-id="0f1de-126">Version</span></span><br/> | <span data-ttu-id="0f1de-127">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="0f1de-127">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="0f1de-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0f1de-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="0f1de-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f1de-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f1de-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f1de-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f1de-131">**Download Manager-Objekt**</span><span class="sxs-lookup"><span data-stu-id="0f1de-131">**DownloadManager Object**</span></span>](downloadmanager-object.md)
</dt> <dt>

[<span data-ttu-id="0f1de-132">**Download Manager. "kreatedownloadcollection"**</span><span class="sxs-lookup"><span data-stu-id="0f1de-132">**DownloadManager. createDownloadCollection**</span></span>](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[<span data-ttu-id="0f1de-133">**Download Collection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="0f1de-133">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





