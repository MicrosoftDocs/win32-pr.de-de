---
title: IWMPControls2 (VB und C )-Schnittstelle (Wmp.h)
description: Stellt eine Methode bereit, die die iwmpcontrols-Schnittstelle ergänzt.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- IWMPControls2 (VB und C) Interface Windows Media Player
- IWMPControls2 (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPControls2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955ee2a8b18f1629427dfe45da802759901ab00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351323"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a><span data-ttu-id="aff0c-105">IWMPControls2-Schnittstelle (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="aff0c-105">IWMPControls2 (VB and C#) interface</span></span>

<span data-ttu-id="aff0c-106">Stellt eine Methode bereit, die die [**iwmpcontrols**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) -Schnittstelle ergänzt.</span><span class="sxs-lookup"><span data-stu-id="aff0c-106">Provides a method that supplements the [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) interface.</span></span>

## <a name="members"></a><span data-ttu-id="aff0c-107">Member</span><span class="sxs-lookup"><span data-stu-id="aff0c-107">Members</span></span>

<span data-ttu-id="aff0c-108">Die IWMPControls2-Schnittstelle **(VB und c#)** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="aff0c-108">The **IWMPControls2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="aff0c-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="aff0c-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="aff0c-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="aff0c-110">Methods</span></span>

<span data-ttu-id="aff0c-111">Die IWMPControls2-Schnittstelle **(VB und c#)** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="aff0c-111">The **IWMPControls2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="aff0c-112">Methode</span><span class="sxs-lookup"><span data-stu-id="aff0c-112">Method</span></span>                                                           | <span data-ttu-id="aff0c-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aff0c-113">Description</span></span>                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aff0c-114">**Schritt**</span><span class="sxs-lookup"><span data-stu-id="aff0c-114">**step**</span></span>](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | <span data-ttu-id="aff0c-115">Verschiebt das aktuelle Video Medien Element in den nächsten Frame oder den vorherigen Frame und friert die Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="aff0c-115">Moves the current video media item to the next frame or the previous frame and freezes playback.</span></span><br/> |



 

<span data-ttu-id="aff0c-116">Der folgende Beispielcode zeigt, wie auf eine [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) -Schnittstelle zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="aff0c-116">The following example code shows how to access an [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) interface.</span></span> <span data-ttu-id="aff0c-117">Im Beispielcode wird der [**iwmpcontrols**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) -Wert umgewandelt, der von der [**AxWindowsMediaPlayer. ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) -Eigenschaft an einen **IWMPControls2** -Wert zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aff0c-117">The example code casts the [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) value that the [**AxWindowsMediaPlayer.Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) property returns to a **IWMPControls2** value.</span></span>

<span data-ttu-id="aff0c-118">Für **c#**:</span><span class="sxs-lookup"><span data-stu-id="aff0c-118">For **C#**:</span></span>


```CSharp
IWMPControls2 Ctlcontrols2 = (IWMPControls2)AxWindowsMediaPlayer.Ctlcontrols;
```



<span data-ttu-id="aff0c-119">Für **VB**:</span><span class="sxs-lookup"><span data-stu-id="aff0c-119">For **VB**:</span></span>


```VB
Dim Ctlcontrols As WMPLib.IWMPControls = Me.AxWindowsMediaPlayer1.Ctlcontrols
Dim Ctlcontrols2 As WMPLib.IWMPControls2 = DirectCast(Ctlcontrols, WMPLib.IWMPControls2)
```



## <a name="requirements"></a><span data-ttu-id="aff0c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aff0c-120">Requirements</span></span>



| <span data-ttu-id="aff0c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aff0c-121">Requirement</span></span> | <span data-ttu-id="aff0c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="aff0c-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="aff0c-123">Header</span><span class="sxs-lookup"><span data-stu-id="aff0c-123">Header</span></span><br/> | <dl> <span data-ttu-id="aff0c-124"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="aff0c-124"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff0c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aff0c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff0c-126">**Iwmpcontrols**</span><span class="sxs-lookup"><span data-stu-id="aff0c-126">**IWMPControls**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[<span data-ttu-id="aff0c-127">**Schnittstellen für Visual Basic .net und C #**</span><span class="sxs-lookup"><span data-stu-id="aff0c-127">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="aff0c-128">**Iwmpcontrols-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="aff0c-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="aff0c-129">**IWMPControls3-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="aff0c-129">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





