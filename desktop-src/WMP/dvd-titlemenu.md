---
title: DVD. titlemenu-Methode
description: Die titlemenu-Methode beendet die Titel Wiedergabe und zeigt das Menü Titel an.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- titlemenu-Methode, Windows-Media Player
- titlemenu-Methode, Windows Media Player, DVD-Klasse
- DVD-Klasse, Windows Media Player, titlemenu-Methode
topic_type:
- apiref
api_name:
- DVD.titleMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9351603d5307415f57610422a83d3586067bdcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340588"
---
# <a name="dvdtitlemenu-method"></a><span data-ttu-id="433ab-106">DVD. titlemenu-Methode</span><span class="sxs-lookup"><span data-stu-id="433ab-106">DVD.titleMenu method</span></span>

<span data-ttu-id="433ab-107">Die **titlemenu** -Methode beendet die Titel Wiedergabe und zeigt das Menü Titel an.</span><span class="sxs-lookup"><span data-stu-id="433ab-107">The **titleMenu** method stops title playback and displays the title menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="433ab-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="433ab-108">Syntax</span></span>


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a><span data-ttu-id="433ab-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="433ab-109">Parameters</span></span>

<span data-ttu-id="433ab-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="433ab-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="433ab-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="433ab-111">Return value</span></span>

<span data-ttu-id="433ab-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="433ab-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="433ab-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="433ab-113">Remarks</span></span>

<span data-ttu-id="433ab-114">Jede DVD wird unterschiedlich verfasst.</span><span class="sxs-lookup"><span data-stu-id="433ab-114">Every DVD is authored differently.</span></span> <span data-ttu-id="433ab-115">Die DVD muss ein Menü enthalten, damit diese Methode funktioniert.</span><span class="sxs-lookup"><span data-stu-id="433ab-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="433ab-116">Einige DVDs werden so erstellt, dass die **topmenu** -und **titlemenu** -Methoden dasselbe Menü öffnen.</span><span class="sxs-lookup"><span data-stu-id="433ab-116">Some DVDs are authored so that the **topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="433ab-117">Die **titlemenu** -Methode ruft in der Regel das Titelmenü auf, aber es kann stattdessen das oberste Menü aufrufen, wenn kein Titel Menü verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="433ab-117">The **titleMenu** method usually invokes the title menu but it may invoke the top menu instead, if there is no title menu available.</span></span>

<span data-ttu-id="433ab-118">**Windows Media Player 10 Mobile:** Diese Methode ist immer erfolgreich, führt jedoch nicht den beabsichtigten Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="433ab-118">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="433ab-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="433ab-119">Requirements</span></span>



| <span data-ttu-id="433ab-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="433ab-120">Requirement</span></span> | <span data-ttu-id="433ab-121">Wert</span><span class="sxs-lookup"><span data-stu-id="433ab-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="433ab-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="433ab-122">Minimum supported client</span></span><br/> | <span data-ttu-id="433ab-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="433ab-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="433ab-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="433ab-124">Minimum supported server</span></span><br/> | <span data-ttu-id="433ab-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="433ab-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="433ab-126">Version</span><span class="sxs-lookup"><span data-stu-id="433ab-126">Version</span></span><br/>                  | <span data-ttu-id="433ab-127">Windows Media Player für Windows XP oder höher.</span><span class="sxs-lookup"><span data-stu-id="433ab-127">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="433ab-128">DLL</span><span class="sxs-lookup"><span data-stu-id="433ab-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="433ab-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="433ab-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="433ab-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="433ab-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="433ab-131">**DVD-Objekt**</span><span class="sxs-lookup"><span data-stu-id="433ab-131">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="433ab-132">**DVD. topmenu**</span><span class="sxs-lookup"><span data-stu-id="433ab-132">**DVD.topMenu**</span></span>](dvd-topmenu.md)
</dt> </dl>

 

 





