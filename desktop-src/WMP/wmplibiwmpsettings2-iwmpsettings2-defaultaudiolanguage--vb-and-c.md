---
title: IWMPSettings2 defaultaudiolanguage (Eigenschaft)
description: Die defaultaudiolanguage-Eigenschaft ruft den Gebiets Schema Bezeichner (Locale Identifier, LCID) der in Windows Media Player angegebenen Standard Audiosprache ab.
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- defaultaudiolanguage-Eigenschaft, Windows Media Player
- defaultaudiolanguage-Eigenschaft, Windows Media Player, IWMPSettings2-Schnittstelle
- IWMPSettings2 Interface Windows Media Player, defaultaudiolanguage-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings2.defaultAudioLanguage
- IWMPSettings2.get_defaultAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7ac9120437005d9f32388e4d639d2d5893675e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356451"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a><span data-ttu-id="0ed7d-106">IWMPSettings2::d efaultaudiolanguage-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0ed7d-106">IWMPSettings2::defaultAudioLanguage property</span></span>

<span data-ttu-id="0ed7d-107">Die **defaultaudiolanguage** -Eigenschaft ruft den Gebiets Schema Bezeichner (Locale Identifier, LCID) der in Windows Media Player angegebenen Standard Audiosprache ab.</span><span class="sxs-lookup"><span data-stu-id="0ed7d-107">The **defaultAudioLanguage** property gets the locale identifier (LCID) of the default audio language specified in Windows Media Player.</span></span>

<span data-ttu-id="0ed7d-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0ed7d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ed7d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ed7d-109">Syntax</span></span>


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="0ed7d-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0ed7d-110">Property value</span></span>

<span data-ttu-id="0ed7d-111">Ein **System. Int32** -Wert, der die LCID ist.</span><span class="sxs-lookup"><span data-stu-id="0ed7d-111">A **System.Int32** that is the LCID.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ed7d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ed7d-112">Remarks</span></span>

<span data-ttu-id="0ed7d-113">Eine LCID identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="0ed7d-113">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ed7d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ed7d-114">Requirements</span></span>



| <span data-ttu-id="0ed7d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ed7d-115">Requirement</span></span> | <span data-ttu-id="0ed7d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0ed7d-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed7d-117">Version</span><span class="sxs-lookup"><span data-stu-id="0ed7d-117">Version</span></span><br/>   | <span data-ttu-id="0ed7d-118">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="0ed7d-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0ed7d-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ed7d-119">Namespace</span></span><br/> | <span data-ttu-id="0ed7d-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0ed7d-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0ed7d-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="0ed7d-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0ed7d-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0ed7d-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ed7d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ed7d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ed7d-124">**IWMPControls3. currentaudiolanguage (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0ed7d-124">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0ed7d-125">**Iwmpsettings-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0ed7d-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0ed7d-126">**IWMPSettings2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0ed7d-126">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





