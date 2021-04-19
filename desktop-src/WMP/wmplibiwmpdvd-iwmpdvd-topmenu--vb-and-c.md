---
title: Iwmpdvd-topmenu-Methode
description: Die topmenu-Methode beendet die Wiedergabe und zeigt das obere Menü (oder das Stamm Menü) für den aktuellen Titel an.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- topmenu-Methoden Fenster Media Player
- topmenu-Methode, Windows Media Player, iwmpdvd-Schnittstelle
- Iwmpdvd Interface, Windows Media Player, topmenu-Methode
topic_type:
- apiref
api_name:
- IWMPDVD.topMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d59bf126a026626cc7f1ba87ea9d0eb94bd1a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361690"
---
# <a name="iwmpdvdtopmenu-method"></a><span data-ttu-id="de79a-106">Iwmpdvd:: topmenu-Methode</span><span class="sxs-lookup"><span data-stu-id="de79a-106">IWMPDVD::topMenu method</span></span>

<span data-ttu-id="de79a-107">Die **topmenu** -Methode beendet die Wiedergabe und zeigt das obere Menü (oder das Stamm Menü) für den aktuellen Titel an.</span><span class="sxs-lookup"><span data-stu-id="de79a-107">The **topMenu** method stops playback and displays the top (or root) menu for the current title.</span></span>

## <a name="syntax"></a><span data-ttu-id="de79a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="de79a-108">Syntax</span></span>


```CSharp
public void topMenu();
```


```VB

Public Sub topMenu()
Implements IWMPDVD.topMenu
```





## <a name="parameters"></a><span data-ttu-id="de79a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="de79a-109">Parameters</span></span>

<span data-ttu-id="de79a-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="de79a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de79a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de79a-111">Return value</span></span>

<span data-ttu-id="de79a-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="de79a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de79a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de79a-113">Remarks</span></span>

<span data-ttu-id="de79a-114">Jede DVD wird unterschiedlich verfasst.</span><span class="sxs-lookup"><span data-stu-id="de79a-114">Every DVD is authored differently.</span></span> <span data-ttu-id="de79a-115">Die DVD muss ein Menü enthalten, damit diese Methode funktioniert.</span><span class="sxs-lookup"><span data-stu-id="de79a-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="de79a-116">Einige DVDs werden so erstellt, dass die **topmenu** -und **iwmpdvd. titlemenu** -Methoden dasselbe Menü öffnen.</span><span class="sxs-lookup"><span data-stu-id="de79a-116">Some DVDs are authored so that the **topMenu** and **IWMPDVD.titleMenu** methods open the same menu.</span></span> <span data-ttu-id="de79a-117">Die **topmenu** -Methode ruft normalerweise das Top-Menü (oder das Stamm Menü) auf, aber es kann das Menü Titel aufrufen, wenn kein Stamm Menü verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="de79a-117">The **topMenu** method usually invokes the top (or root) menu, but it may invoke the title menu if there is no root menu available.</span></span>

## <a name="requirements"></a><span data-ttu-id="de79a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de79a-118">Requirements</span></span>



| <span data-ttu-id="de79a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de79a-119">Requirement</span></span> | <span data-ttu-id="de79a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="de79a-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de79a-121">Version</span><span class="sxs-lookup"><span data-stu-id="de79a-121">Version</span></span><br/>   | <span data-ttu-id="de79a-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="de79a-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="de79a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="de79a-123">Namespace</span></span><br/> | <span data-ttu-id="de79a-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="de79a-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="de79a-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="de79a-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="de79a-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="de79a-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de79a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de79a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de79a-128">**Iwmpdvd-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="de79a-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="de79a-129">**Iwmpdvd. titlemenu (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="de79a-129">**IWMPDVD.titleMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





