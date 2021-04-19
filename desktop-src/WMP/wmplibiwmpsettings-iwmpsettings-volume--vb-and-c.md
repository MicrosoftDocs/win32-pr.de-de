---
title: Iwmpsettings-volumenschaft
description: Mit der Volume-Eigenschaft wird das aktuelle Wiedergabe Volume abgerufen oder festgelegt.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- Volumeeigenschaft (Windows Media Player)
- Volumeeigenschaft Windows Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows-Media Player, Volume-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings.volume
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b21e50c9d3c52b7ce117d6c2ab681e592571c0f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370007"
---
# <a name="iwmpsettingsvolume-property"></a><span data-ttu-id="0c77c-106">Iwmpsettings:: Volume-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0c77c-106">IWMPSettings::volume property</span></span>

<span data-ttu-id="0c77c-107">Mit der **Volume** -Eigenschaft wird das aktuelle Wiedergabe Volume abgerufen oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c77c-107">The **volume** property gets or sets the current playback volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c77c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c77c-108">Syntax</span></span>


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="0c77c-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0c77c-109">Property value</span></span>

<span data-ttu-id="0c77c-110">Ein **System. Int32** -Wert, der die Volumeebene zwischen 0 und 100 ist.</span><span class="sxs-lookup"><span data-stu-id="0c77c-110">A **System.Int32** that is the volume level, ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c77c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c77c-111">Remarks</span></span>

<span data-ttu-id="0c77c-112">Der Wert 0 (null) gibt kein Volume (stumm) an.</span><span class="sxs-lookup"><span data-stu-id="0c77c-112">A value of zero specifies no volume (muted).</span></span> <span data-ttu-id="0c77c-113">Der Wert 100 gibt das vollständige Volume an.</span><span class="sxs-lookup"><span data-stu-id="0c77c-113">A value of 100 specifies full volume.</span></span> <span data-ttu-id="0c77c-114">Wenn für diese Eigenschaft kein Wert angegeben wird, wird standardmäßig die letzte für Windows Media Player festgelegte volumeeinstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c77c-114">If no value is specified for this property, it defaults to the last volume setting established for Windows Media Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c77c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c77c-115">Requirements</span></span>



| <span data-ttu-id="0c77c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c77c-116">Requirement</span></span> | <span data-ttu-id="0c77c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0c77c-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c77c-118">Version</span><span class="sxs-lookup"><span data-stu-id="0c77c-118">Version</span></span><br/>   | <span data-ttu-id="0c77c-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="0c77c-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0c77c-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c77c-120">Namespace</span></span><br/> | <span data-ttu-id="0c77c-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0c77c-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0c77c-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="0c77c-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0c77c-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0c77c-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c77c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c77c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c77c-125">**Iwmpsettings-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0c77c-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





