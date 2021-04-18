---
title: Download Item. SourceUrl
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die SourceUrl-Eigenschaft ruft die Quell-URL des Downloads ab.
ms.assetid: 87af20a5-5721-498d-8417-3e7dbbec38a2
keywords:
- Download Element. SourceURL (Windows Media Player)
topic_type:
- apiref
api_name:
- DownloadItem.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1670fb4fec0ff4adb68269cf6fe6bb39be248e01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364676"
---
# <a name="downloaditemsourceurl"></a><span data-ttu-id="41856-106">Download Item. SourceUrl</span><span class="sxs-lookup"><span data-stu-id="41856-106">DownloadItem.sourceURL</span></span>

> [!Note]  
> <span data-ttu-id="41856-107">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="41856-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="41856-108">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41856-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="41856-109">Die **SourceUrl** -Eigenschaft ruft die Quell-URL des Downloads ab.</span><span class="sxs-lookup"><span data-stu-id="41856-109">The **sourceURL** property retrieves the source URL of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="41856-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="41856-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).sourceURL
      
```

## <a name="possible-values"></a><span data-ttu-id="41856-111">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="41856-111">Possible Values</span></span>

<span data-ttu-id="41856-112">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="41856-112">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="41856-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41856-113">Remarks</span></span>

<span data-ttu-id="41856-114">Es können nur die folgenden Digital Media-Formate heruntergeladen werden:</span><span class="sxs-lookup"><span data-stu-id="41856-114">Only the following digital media formats can be downloaded:</span></span>

-   <span data-ttu-id="41856-115">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="41856-115">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="41856-116">MP3</span><span class="sxs-lookup"><span data-stu-id="41856-116">MP3</span></span>
-   <span data-ttu-id="41856-117">Windows Media Audio (WMA)</span><span class="sxs-lookup"><span data-stu-id="41856-117">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="41856-118">Windows Media Video (WMV)</span><span class="sxs-lookup"><span data-stu-id="41856-118">Windows Media Video (WMV)</span></span>

## <a name="requirements"></a><span data-ttu-id="41856-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41856-119">Requirements</span></span>



| <span data-ttu-id="41856-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41856-120">Requirement</span></span> | <span data-ttu-id="41856-121">Wert</span><span class="sxs-lookup"><span data-stu-id="41856-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="41856-122">Version</span><span class="sxs-lookup"><span data-stu-id="41856-122">Version</span></span><br/> | <span data-ttu-id="41856-123">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="41856-123">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="41856-124">DLL</span><span class="sxs-lookup"><span data-stu-id="41856-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="41856-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41856-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41856-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41856-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41856-127">**Download Item-Objekt**</span><span class="sxs-lookup"><span data-stu-id="41856-127">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





