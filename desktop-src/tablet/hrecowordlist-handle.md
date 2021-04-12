---
description: Ein hrecowordlist-Handle wird verwendet, um eine Wort Liste zu verwalten, die Sie an einen Erkennungs Kontext anfügen. Sie verwenden eine Wort Liste, um die Erkennungsergebnisse zu verbessern.
ms.assetid: 7333307b-1857-48a7-bb9f-bdbd8530f093
title: Hrecowordlist-handle ("recapis. h")
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e5d33862cacb7040a26edc23d7db04c57206c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526573"
---
# <a name="hrecowordlist-handle"></a><span data-ttu-id="71146-104">Hrecowordlist-handle</span><span class="sxs-lookup"><span data-stu-id="71146-104">HRECOWORDLIST Handle</span></span>

<span data-ttu-id="71146-105">Ein **hrecowordlist** -Handle wird verwendet, um eine Wort Liste zu verwalten, die Sie an einen Erkennungs Kontext anfügen.</span><span class="sxs-lookup"><span data-stu-id="71146-105">An **HRECOWORDLIST** handle is used to manage a word list you attach to a recognizer context.</span></span> <span data-ttu-id="71146-106">Sie verwenden eine Wort Liste, um die Erkennungsergebnisse zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="71146-106">You use a word list to improve recognition results.</span></span>


```C++
typedef HANDLE HRECOWORDLIST;
```



## <a name="remarks"></a><span data-ttu-id="71146-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71146-107">Remarks</span></span>

<span data-ttu-id="71146-108">Die folgende Funktion verwendet eine **hrecowordlist**.</span><span class="sxs-lookup"><span data-stu-id="71146-108">The following function use an **HRECOWORDLIST**.</span></span>



| <span data-ttu-id="71146-109">Funktion</span><span class="sxs-lookup"><span data-stu-id="71146-109">Function</span></span>                                         | <span data-ttu-id="71146-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71146-110">Description</span></span>                                         |
|--------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="71146-111">**Addwordstowordlist**</span><span class="sxs-lookup"><span data-stu-id="71146-111">**AddWordsToWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-addwordstowordlist) | <span data-ttu-id="71146-112">Fügt der Word-Liste mindestens ein Wort hinzu.</span><span class="sxs-lookup"><span data-stu-id="71146-112">Adds one or more words to the word list.</span></span><br/> |
| [<span data-ttu-id="71146-113">**Destroywordlist**</span><span class="sxs-lookup"><span data-stu-id="71146-113">**DestroyWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroywordlist)       | <span data-ttu-id="71146-114">Zerstört die aktuelle Wort Liste.</span><span class="sxs-lookup"><span data-stu-id="71146-114">Destroys the current word list.</span></span><br/>          |
| [<span data-ttu-id="71146-115">**Makewordlist**</span><span class="sxs-lookup"><span data-stu-id="71146-115">**MakeWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-makewordlist)             | <span data-ttu-id="71146-116">Erstellt eine Wort Liste.</span><span class="sxs-lookup"><span data-stu-id="71146-116">Creates a word list.</span></span><br/>                     |



 

## <a name="requirements"></a><span data-ttu-id="71146-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71146-117">Requirements</span></span>



| <span data-ttu-id="71146-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71146-118">Requirement</span></span> | <span data-ttu-id="71146-119">Wert</span><span class="sxs-lookup"><span data-stu-id="71146-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="71146-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71146-120">Minimum supported client</span></span><br/> | <span data-ttu-id="71146-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71146-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="71146-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71146-122">Minimum supported server</span></span><br/> | <span data-ttu-id="71146-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="71146-123">None supported</span></span><br/>                                                            |
| <span data-ttu-id="71146-124">Header</span><span class="sxs-lookup"><span data-stu-id="71146-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="71146-125"><dt>"Recapis. h"</dt></span><span class="sxs-lookup"><span data-stu-id="71146-125"><dt>Recapis.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71146-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71146-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71146-127">**Setwordlist-Funktion**</span><span class="sxs-lookup"><span data-stu-id="71146-127">**SetWordList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 




