---
description: Stellt eine Liste von Wörtern dar, die verwendet werden können, um das Erkennungs Ergebnis zu verbessern.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: Inkwordlist-Klasse (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkWordList
- InkWordList.IInkWordList
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 7f3bbf077758bfd0449f5bca1ba3739342fa3658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359522"
---
# <a name="inkwordlist-class"></a><span data-ttu-id="616c1-103">Inkwordlist-Klasse</span><span class="sxs-lookup"><span data-stu-id="616c1-103">InkWordList class</span></span>

<span data-ttu-id="616c1-104">Stellt eine Liste von Wörtern dar, die verwendet werden können, um das Erkennungs Ergebnis zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="616c1-104">Represents a list of words that can be used to improve the recognition result.</span></span>

<span data-ttu-id="616c1-105">**Inkwordlist** enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="616c1-105">**InkWordList** has these types of members:</span></span>

-   [<span data-ttu-id="616c1-106">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="616c1-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="616c1-107">Methoden</span><span class="sxs-lookup"><span data-stu-id="616c1-107">Methods</span></span>](#methods)

### <a name="interfaces"></a><span data-ttu-id="616c1-108">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="616c1-108">Interfaces</span></span>

<span data-ttu-id="616c1-109">Diese Schnittstellen werden von der **inkwordlist** -Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="616c1-109">The **InkWordList** class defines these interfaces.</span></span>



| <span data-ttu-id="616c1-110">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="616c1-110">Interface</span></span>        | <span data-ttu-id="616c1-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="616c1-111">Description</span></span>                                                           |
|:-----------------|:----------------------------------------------------------------------|
| <span data-ttu-id="616c1-112">**Iinkwordlist**</span><span class="sxs-lookup"><span data-stu-id="616c1-112">**IInkWordList**</span></span> | <span data-ttu-id="616c1-113">Dieses Objekt implementiert die **iinkwordlist** -com-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="616c1-113">This object implements the **IInkWordList** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="616c1-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="616c1-114">Methods</span></span>

<span data-ttu-id="616c1-115">Die **inkwordlist** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="616c1-115">The **InkWordList** class has these methods.</span></span>



| <span data-ttu-id="616c1-116">Methode</span><span class="sxs-lookup"><span data-stu-id="616c1-116">Method</span></span>                                       | <span data-ttu-id="616c1-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="616c1-117">Description</span></span>                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="616c1-118">**AddWord**</span><span class="sxs-lookup"><span data-stu-id="616c1-118">**AddWord**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | <span data-ttu-id="616c1-119">Fügt der **inkwordlist** ein einzelnes Wort hinzu.</span><span class="sxs-lookup"><span data-stu-id="616c1-119">Adds a single word to the **InkWordList**.</span></span><br/>                   |
| [<span data-ttu-id="616c1-120">**Merge**</span><span class="sxs-lookup"><span data-stu-id="616c1-120">**Merge**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | <span data-ttu-id="616c1-121">Führt eine weitere **inkwordlist** mit in diese **inkwordlist** zusammen.</span><span class="sxs-lookup"><span data-stu-id="616c1-121">Merges another **InkWordList** to into this **InkWordList**.</span></span><br/> |
| [<span data-ttu-id="616c1-122">**Removeword**</span><span class="sxs-lookup"><span data-stu-id="616c1-122">**RemoveWord**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | <span data-ttu-id="616c1-123">Entfernt ein einzelnes Wort aus einer " **inkwordlist**".</span><span class="sxs-lookup"><span data-stu-id="616c1-123">Removes a single word from a **InkWordList**.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="616c1-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="616c1-124">Remarks</span></span>

<span data-ttu-id="616c1-125">Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="616c1-125">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="616c1-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="616c1-126">Requirements</span></span>



| <span data-ttu-id="616c1-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="616c1-127">Requirement</span></span> | <span data-ttu-id="616c1-128">Wert</span><span class="sxs-lookup"><span data-stu-id="616c1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="616c1-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="616c1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="616c1-130">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="616c1-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="616c1-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="616c1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="616c1-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="616c1-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="616c1-133">Header</span><span class="sxs-lookup"><span data-stu-id="616c1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="616c1-134"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="616c1-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="616c1-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="616c1-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="616c1-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="616c1-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="616c1-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="616c1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="616c1-138">**WordList-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="616c1-138">**WordList Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[<span data-ttu-id="616c1-139">Faktoid-Konstanten</span><span class="sxs-lookup"><span data-stu-id="616c1-139">Factoid Constants</span></span>](factoid-constants.md)
</dt> <dt>

[<span data-ttu-id="616c1-140">**Inkrecognizercontext-Klasse**</span><span class="sxs-lookup"><span data-stu-id="616c1-140">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> </dl>

 

