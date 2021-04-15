---
title: DVD. topmenu-Methode
description: Die topmenu-Methode beendet die Titel Wiedergabe und zeigt das obere Menü (oder das Stamm Menü) für den aktuellen Titel an.
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- topmenu-Methoden Fenster Media Player
- topmenu-Methode, Windows Media Player, DVD-Klasse
- DVD-Klasse, Windows Media Player, topmenu-Methode
topic_type:
- apiref
api_name:
- DVD.topMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be2b0fdafb10039b24f1d77e65f4b105889da85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477379"
---
# <a name="dvdtopmenu-method"></a><span data-ttu-id="04ec1-106">DVD. topmenu-Methode</span><span class="sxs-lookup"><span data-stu-id="04ec1-106">DVD.topMenu method</span></span>

<span data-ttu-id="04ec1-107">Die **topmenu** -Methode beendet die Titel Wiedergabe und zeigt das obere Menü (oder das Stamm Menü) für den aktuellen Titel an.</span><span class="sxs-lookup"><span data-stu-id="04ec1-107">The **topMenu** method stops title playback and displays the top (or root) menu for the current title.</span></span>

## <a name="syntax"></a><span data-ttu-id="04ec1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="04ec1-108">Syntax</span></span>


```JScript
DVD.topMenu()
```



## <a name="parameters"></a><span data-ttu-id="04ec1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="04ec1-109">Parameters</span></span>

<span data-ttu-id="04ec1-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="04ec1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="04ec1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04ec1-111">Return value</span></span>

<span data-ttu-id="04ec1-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="04ec1-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04ec1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04ec1-113">Remarks</span></span>

<span data-ttu-id="04ec1-114">Jede DVD wird unterschiedlich verfasst.</span><span class="sxs-lookup"><span data-stu-id="04ec1-114">Every DVD is authored differently.</span></span> <span data-ttu-id="04ec1-115">Die DVD muss ein Menü enthalten, damit diese Methode funktioniert.</span><span class="sxs-lookup"><span data-stu-id="04ec1-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="04ec1-116">Einige DVDs werden so erstellt, dass die **topmenu** -und **titlemenu** -Methoden dasselbe Menü öffnen.</span><span class="sxs-lookup"><span data-stu-id="04ec1-116">Some DVDs are authored so that the **topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="04ec1-117">Die **topmenu** -Methode ruft normalerweise das Top-Menü (oder das Stamm Menü) auf, aber es kann stattdessen das Titelmenü aufrufen, wenn kein Stamm Menü verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="04ec1-117">The **topMenu** method usually invokes the top (or root) menu but it may invoke the title menu instead, if there is no root menu available.</span></span>

<span data-ttu-id="04ec1-118">**Windows Media Player 10 Mobile:** Diese Methode ist immer erfolgreich, führt jedoch nicht den beabsichtigten Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="04ec1-118">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="04ec1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04ec1-119">Requirements</span></span>



| <span data-ttu-id="04ec1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04ec1-120">Requirement</span></span> | <span data-ttu-id="04ec1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="04ec1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04ec1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04ec1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="04ec1-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04ec1-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="04ec1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04ec1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="04ec1-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04ec1-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="04ec1-126">Version</span><span class="sxs-lookup"><span data-stu-id="04ec1-126">Version</span></span><br/>                  | <span data-ttu-id="04ec1-127">Windows Media Player für Windows XP oder höher.</span><span class="sxs-lookup"><span data-stu-id="04ec1-127">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="04ec1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="04ec1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04ec1-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04ec1-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04ec1-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04ec1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ec1-131">**DVD-Objekt**</span><span class="sxs-lookup"><span data-stu-id="04ec1-131">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="04ec1-132">**DVD. titlemenu**</span><span class="sxs-lookup"><span data-stu-id="04ec1-132">**DVD.titleMenu**</span></span>](dvd-titlemenu.md)
</dt> </dl>

 

 





