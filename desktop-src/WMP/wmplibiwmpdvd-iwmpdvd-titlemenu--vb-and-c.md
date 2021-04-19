---
title: Iwmpdvd-titlemenu-Methode
description: Die titlemenu-Methode beendet die Wiedergabe und zeigt das Titelmenü an.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- titlemenu-Methode, Windows-Media Player
- titlemenu-Methode, Windows Media Player, iwmpdvd-Schnittstelle
- Iwmpdvd Interface, Windows Media Player, titlemenu-Methode
topic_type:
- apiref
api_name:
- IWMPDVD.titleMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0889a3f65ccefe4e09bb5ff47a66867681dcc801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367791"
---
# <a name="iwmpdvdtitlemenu-method"></a><span data-ttu-id="d9f30-106">Iwmpdvd:: titlemenu-Methode</span><span class="sxs-lookup"><span data-stu-id="d9f30-106">IWMPDVD::titleMenu method</span></span>

<span data-ttu-id="d9f30-107">Die **titlemenu** -Methode beendet die Wiedergabe und zeigt das Titelmenü an.</span><span class="sxs-lookup"><span data-stu-id="d9f30-107">The **titleMenu** method stops playback and displays the title menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9f30-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9f30-108">Syntax</span></span>


```CSharp
public void titleMenu();
```


```VB

Public Sub titleMenu()
Implements IWMPDVD.titleMenu
```





## <a name="parameters"></a><span data-ttu-id="d9f30-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9f30-109">Parameters</span></span>

<span data-ttu-id="d9f30-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d9f30-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9f30-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9f30-111">Return value</span></span>

<span data-ttu-id="d9f30-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d9f30-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9f30-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9f30-113">Remarks</span></span>

<span data-ttu-id="d9f30-114">Jede DVD wird unterschiedlich verfasst.</span><span class="sxs-lookup"><span data-stu-id="d9f30-114">Every DVD is authored differently.</span></span> <span data-ttu-id="d9f30-115">Die DVD muss ein Menü enthalten, damit diese Methode funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d9f30-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="d9f30-116">Einige DVDs werden so erstellt, dass die **iwmpdvd. topmenu** -Methode und die **titlemenu** -Methode dasselbe Menü öffnen.</span><span class="sxs-lookup"><span data-stu-id="d9f30-116">Some DVDs are authored so that the **IWMPDVD.topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="d9f30-117">Die **titlemenu** -Methode ruft in der Regel das Titelmenü auf, aber Sie kann das oberste Menü aufrufen, wenn kein Titel Menü verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d9f30-117">The **titleMenu** method usually invokes the title menu, but it may invoke the top menu if there is no title menu available.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f30-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9f30-118">Requirements</span></span>



| <span data-ttu-id="d9f30-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9f30-119">Requirement</span></span> | <span data-ttu-id="d9f30-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d9f30-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f30-121">Version</span><span class="sxs-lookup"><span data-stu-id="d9f30-121">Version</span></span><br/>   | <span data-ttu-id="d9f30-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="d9f30-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d9f30-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="d9f30-123">Namespace</span></span><br/> | <span data-ttu-id="d9f30-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d9f30-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d9f30-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="d9f30-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d9f30-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d9f30-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f30-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9f30-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f30-128">**Iwmpdvd-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="d9f30-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d9f30-129">**Iwmpdvd. topmenu (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="d9f30-129">**IWMPDVD.topMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





