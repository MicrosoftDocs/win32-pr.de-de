---
title: DVD. IsAvailable
description: Die IsAvailable-Eigenschaft gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann. | DVD. IsAvailable
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- DVD. IsAvailable-Windows-Media Player
topic_type:
- apiref
api_name:
- DVD.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088b4b6365dd60d859fda8ec563cc9c8ff8a4c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366404"
---
# <a name="dvdisavailable"></a><span data-ttu-id="37662-105">DVD. IsAvailable</span><span class="sxs-lookup"><span data-stu-id="37662-105">DVD.isAvailable</span></span>

<span data-ttu-id="37662-106">Die **IsAvailable** -Eigenschaft gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="37662-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

``` syntax
player.dvd.isAvailable(
        name
        )
```

## <a name="parameters"></a><span data-ttu-id="37662-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="37662-107">Parameters</span></span>

<span data-ttu-id="37662-108">*name*</span><span class="sxs-lookup"><span data-stu-id="37662-108">*name*</span></span>

<span data-ttu-id="37662-109">Eine **Zeichenfolge** , die einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="37662-109">**String** containing one of the following values.</span></span>



| <span data-ttu-id="37662-110">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="37662-110">String</span></span>     | <span data-ttu-id="37662-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37662-111">Description</span></span>                                                                            |
|------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37662-112">back (Zurück)</span><span class="sxs-lookup"><span data-stu-id="37662-112">back</span></span>       | <span data-ttu-id="37662-113">Bestimmt, ob die **Back** -Methode verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="37662-113">Determines whether the **back** method is available.</span></span>                                   |
| <span data-ttu-id="37662-114">DVD</span><span class="sxs-lookup"><span data-stu-id="37662-114">dvd</span></span>        | <span data-ttu-id="37662-115">Bestimmt, ob die DVD geladen wird.</span><span class="sxs-lookup"><span data-stu-id="37662-115">Determines whether the DVD is loaded.</span></span>                                                  |
| <span data-ttu-id="37662-116">dvddecoder</span><span class="sxs-lookup"><span data-stu-id="37662-116">dvdDecoder</span></span> | <span data-ttu-id="37662-117">Bestimmt, ob der DVD-Decoder auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="37662-117">Determines whether the DVD decoder is installed on system.</span></span>                             |
| <span data-ttu-id="37662-118">resume</span><span class="sxs-lookup"><span data-stu-id="37662-118">resume</span></span>     | <span data-ttu-id="37662-119">Bestimmt, ob die **Resume** -Methode verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="37662-119">Determines whether the **resume** method is available.</span></span>                                 |
| <span data-ttu-id="37662-120">titlemenu</span><span class="sxs-lookup"><span data-stu-id="37662-120">titleMenu</span></span>  | <span data-ttu-id="37662-121">Bestimmt, ob die **titlemenu** -Methode verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="37662-121">Determines whether the **titleMenu** method is available.</span></span>                              |
| <span data-ttu-id="37662-122">topmenu</span><span class="sxs-lookup"><span data-stu-id="37662-122">topMenu</span></span>    | <span data-ttu-id="37662-123">Bestimmt, ob die **topmenu** -Methode verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="37662-123">Determines whether the **topMenu** method is available.</span></span> <span data-ttu-id="37662-124">Wird üblicherweise als Stamm Menü bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="37662-124">Commonly called the root menu.</span></span> |



 

## <a name="return-values"></a><span data-ttu-id="37662-125">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="37662-125">Return Values</span></span>

<span data-ttu-id="37662-126">Diese Methode gibt einen schreibgeschützten **booleschen** Wert zurück, der angibt, ob der angegebene Parameter verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="37662-126">This method returns a read-only **Boolean** indicating whether the specified parameter is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="37662-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37662-127">Remarks</span></span>

<span data-ttu-id="37662-128">Die DVD-Features von Windows Media Player können nicht auf Computern verwendet werden, auf denen keine DVD-Decoder von Drittanbietern installiert sind.</span><span class="sxs-lookup"><span data-stu-id="37662-128">The DVD features of Windows Media Player will not work on computers that do not have third-party DVD decoders installed.</span></span> <span data-ttu-id="37662-129">Sie können bestimmen, ob ein Decoder verfügbar ist, indem Sie **IsAvailable**("dvddecoder") aufrufen.</span><span class="sxs-lookup"><span data-stu-id="37662-129">You can determine whether a decoder is available by calling **isAvailable**("dvdDecoder").</span></span>

<span data-ttu-id="37662-130">Jede DVD wird unterschiedlich verfasst.</span><span class="sxs-lookup"><span data-stu-id="37662-130">Every DVD is authored differently.</span></span> <span data-ttu-id="37662-131">Die während der DVD-Wiedergabe und-Navigation verfügbaren Methoden hängen davon ab, wie die DVD erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="37662-131">The methods available during DVD playback and navigation depend on how the DVD is authored.</span></span>

<span data-ttu-id="37662-132">**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="37662-132">**Windows Media Player 10 Mobile:** This property always returns **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="37662-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37662-133">Requirements</span></span>



| <span data-ttu-id="37662-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37662-134">Requirement</span></span> | <span data-ttu-id="37662-135">Wert</span><span class="sxs-lookup"><span data-stu-id="37662-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37662-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37662-136">Minimum supported client</span></span><br/> | <span data-ttu-id="37662-137">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37662-137">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37662-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37662-138">Minimum supported server</span></span><br/> | <span data-ttu-id="37662-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37662-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="37662-140">Version</span><span class="sxs-lookup"><span data-stu-id="37662-140">Version</span></span><br/>                  | <span data-ttu-id="37662-141">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="37662-141">Windows Media Player for Windows XP or later</span></span><br/>                            |
| <span data-ttu-id="37662-142">DLL</span><span class="sxs-lookup"><span data-stu-id="37662-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37662-143"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37662-143"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37662-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37662-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37662-145">**DVD-Objekt**</span><span class="sxs-lookup"><span data-stu-id="37662-145">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





