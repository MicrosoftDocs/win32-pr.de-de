---
title: Download Item. Progress
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die Status-Eigenschaft ruft den Fortschritt des Downloads in Bytes ab.
ms.assetid: 58644eac-8dd0-4e9d-8055-03833c863a6e
keywords:
- Download Element. Progress (Windows-Media Player
topic_type:
- apiref
api_name:
- DownloadItem.progress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1967c1eb3dc72c00b8b10b70da5d797343e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369617"
---
# <a name="downloaditemprogress"></a><span data-ttu-id="d9d48-106">Download Item. Progress</span><span class="sxs-lookup"><span data-stu-id="d9d48-106">DownloadItem.progress</span></span>

> [!Note]  
> <span data-ttu-id="d9d48-107">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="d9d48-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="d9d48-108">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d9d48-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="d9d48-109">Die Status **-Eigenschaft ruft den fort** Schritt des Downloads in Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="d9d48-109">The **progress** property retrieves the progress of the download in bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9d48-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9d48-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).progress
      
```

## <a name="possible-values"></a><span data-ttu-id="d9d48-111">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="d9d48-111">Possible Values</span></span>

<span data-ttu-id="d9d48-112">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="d9d48-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9d48-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9d48-113">Requirements</span></span>



| <span data-ttu-id="d9d48-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9d48-114">Requirement</span></span> | <span data-ttu-id="d9d48-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d9d48-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d9d48-116">Version</span><span class="sxs-lookup"><span data-stu-id="d9d48-116">Version</span></span><br/> | <span data-ttu-id="d9d48-117">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="d9d48-117">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="d9d48-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d9d48-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="d9d48-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9d48-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9d48-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9d48-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9d48-121">**Download Item-Objekt**</span><span class="sxs-lookup"><span data-stu-id="d9d48-121">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="d9d48-122">**Download Item. Size**</span><span class="sxs-lookup"><span data-stu-id="d9d48-122">**DownloadItem.size**</span></span>](downloaditem-size.md)
</dt> </dl>

 

 





