---
title: IWMPClosedCaption2 samistylecount (Eigenschaft)
description: Die samistylecount-Eigenschaft ruft die Anzahl der Stile ab, die von der aktuellen Sami-Datei unterstützt werden.
ms.assetid: e2a0d194-6fa2-48c9-9fc7-0b60029d2e5d
keywords:
- Samistylecount-Eigenschaften Fenster Media Player
- Samistylecount-Eigenschaft, Windows Media Player, IWMPClosedCaption2-Schnittstelle
- IWMPClosedCaption2 Interface, Windows Media Player, samistylecount (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMIStyleCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff361b4c6d34f63e86e3d8458bff4d3308cae29f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372460"
---
# <a name="iwmpclosedcaption2samistylecount-property"></a><span data-ttu-id="00e62-106">IWMPClosedCaption2:: samistylecount (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="00e62-106">IWMPClosedCaption2::SAMIStyleCount property</span></span>

<span data-ttu-id="00e62-107">Die **samistylecount** -Eigenschaft ruft die Anzahl der Stile ab, die von der aktuellen Sami-Datei unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="00e62-107">The **SAMIStyleCount** property gets the number of styles supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="00e62-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="00e62-108">Syntax</span></span>


```CSharp
public System.Int32 SAMIStyleCount {get; set;}
```


```VB

Public ReadOnly Property SAMIStyleCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="00e62-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="00e62-109">Property value</span></span>

<span data-ttu-id="00e62-110">Ein **System. Int32** -Wert, der die Anzahl der Stile ist.</span><span class="sxs-lookup"><span data-stu-id="00e62-110">A **System.Int32** that is the number of styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="00e62-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00e62-111">Remarks</span></span>

<span data-ttu-id="00e62-112">Diese Eigenschaft gibt 0 (null) zurück, es sei denn, eine digitale Mediendatei ist geöffnet (AxWindowsMediaPlayer. openstate ist gleich 13).</span><span class="sxs-lookup"><span data-stu-id="00e62-112">This property returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="00e62-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00e62-113">Requirements</span></span>



| <span data-ttu-id="00e62-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00e62-114">Requirement</span></span> | <span data-ttu-id="00e62-115">Wert</span><span class="sxs-lookup"><span data-stu-id="00e62-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00e62-116">Version</span><span class="sxs-lookup"><span data-stu-id="00e62-116">Version</span></span><br/>   | <span data-ttu-id="00e62-117">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="00e62-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="00e62-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="00e62-118">Namespace</span></span><br/> | <span data-ttu-id="00e62-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="00e62-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="00e62-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="00e62-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="00e62-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="00e62-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00e62-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00e62-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00e62-123">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="00e62-123">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="00e62-124">**Iwmpclosedcaption-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="00e62-124">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="00e62-125">**Iwmpclosedcaption. samistyle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="00e62-125">**IWMPClosedCaption.SAMIStyle (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="00e62-126">**IWMPClosedCaption2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="00e62-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="00e62-127">**IWMPClosedCaption2. getsamistylename (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="00e62-127">**IWMPClosedCaption2.getSAMIStyleName (VB and C#)**</span></span>](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md)
</dt> </dl>

 

 





