---
title: Downloadaditem. DownloadState
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die DownloadState-Eigenschaft ruft den Status des Downloads ab.
ms.assetid: dde27f43-40ee-4eb9-b316-42312ee937d0
keywords:
- Download Status-Windows-Media Player
topic_type:
- apiref
api_name:
- DownloadItem.downloadState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd2af2fab2ecb69df5b4695b227631b5be2dd96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358142"
---
# <a name="downloaditemdownloadstate"></a><span data-ttu-id="a80fb-106">Downloadaditem. DownloadState</span><span class="sxs-lookup"><span data-stu-id="a80fb-106">DownloadItem.downloadState</span></span>

> [!Note]  
> <span data-ttu-id="a80fb-107">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="a80fb-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a80fb-108">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a80fb-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a80fb-109">Die **DownloadState** -Eigenschaft ruft den Status des Downloads ab.</span><span class="sxs-lookup"><span data-stu-id="a80fb-109">The **downloadState** property retrieves the state of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="a80fb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a80fb-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).downloadState
      
```

## <a name="possible-values"></a><span data-ttu-id="a80fb-111">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="a80fb-111">Possible Values</span></span>

<span data-ttu-id="a80fb-112">Diese Eigenschaft ist eine schreibgeschützte **Zahl** , die einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="a80fb-112">This property is a read-only **Number** containing one of the following values.</span></span>



| <span data-ttu-id="a80fb-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a80fb-113">Value</span></span> | <span data-ttu-id="a80fb-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a80fb-114">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="a80fb-115">0</span><span class="sxs-lookup"><span data-stu-id="a80fb-115">0</span></span>     | <span data-ttu-id="a80fb-116">Herunterladen</span><span class="sxs-lookup"><span data-stu-id="a80fb-116">Downloading</span></span> |
| <span data-ttu-id="a80fb-117">1</span><span class="sxs-lookup"><span data-stu-id="a80fb-117">1</span></span>     | <span data-ttu-id="a80fb-118">Angehalten</span><span class="sxs-lookup"><span data-stu-id="a80fb-118">Paused</span></span>      |
| <span data-ttu-id="a80fb-119">2</span><span class="sxs-lookup"><span data-stu-id="a80fb-119">2</span></span>     | <span data-ttu-id="a80fb-120">Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="a80fb-120">Processing</span></span>  |
| <span data-ttu-id="a80fb-121">3</span><span class="sxs-lookup"><span data-stu-id="a80fb-121">3</span></span>     | <span data-ttu-id="a80fb-122">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="a80fb-122">Completed</span></span>   |
| <span data-ttu-id="a80fb-123">4</span><span class="sxs-lookup"><span data-stu-id="a80fb-123">4</span></span>     | <span data-ttu-id="a80fb-124">Canceled</span><span class="sxs-lookup"><span data-stu-id="a80fb-124">Canceled</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="a80fb-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a80fb-125">Remarks</span></span>

<span data-ttu-id="a80fb-126">Download Zustände können in beliebiger Reihenfolge auftreten.</span><span class="sxs-lookup"><span data-stu-id="a80fb-126">Download states can occur in any order.</span></span> <span data-ttu-id="a80fb-127">Schreiben Sie keinen Code, der von dem Vorkommen eines bestimmten Download Status abhängt.</span><span class="sxs-lookup"><span data-stu-id="a80fb-127">Do not write code that depends on the occurrence of any particular download state.</span></span>

## <a name="requirements"></a><span data-ttu-id="a80fb-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a80fb-128">Requirements</span></span>



| <span data-ttu-id="a80fb-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a80fb-129">Requirement</span></span> | <span data-ttu-id="a80fb-130">Wert</span><span class="sxs-lookup"><span data-stu-id="a80fb-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a80fb-131">Version</span><span class="sxs-lookup"><span data-stu-id="a80fb-131">Version</span></span><br/> | <span data-ttu-id="a80fb-132">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="a80fb-132">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="a80fb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a80fb-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="a80fb-134"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a80fb-134"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a80fb-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a80fb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a80fb-136">**Download Item-Objekt**</span><span class="sxs-lookup"><span data-stu-id="a80fb-136">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





