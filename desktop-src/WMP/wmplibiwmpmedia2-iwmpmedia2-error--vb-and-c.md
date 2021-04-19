---
title: IWMPMedia2 Error (Eigenschaft)
description: Die Error-Eigenschaft ruft eine iwmperroritem-Schnittstelle ab, wenn das Medien Element einen Fehlerzustand aufweist.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Fehler Eigenschaften Fenster Media Player
- Fehler Eigenschaft, Windows Media Player, IWMPMedia2-Schnittstelle
- IWMPMedia2 Interface, Windows Media Player, Fehler Eigenschaft
topic_type:
- apiref
api_name:
- IWMPMedia2.Error
- IWMPMedia2.get_Error
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2179b4604efd03574c78261575ce02311cd18a0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355266"
---
# <a name="iwmpmedia2error-property"></a><span data-ttu-id="320ca-106">IWMPMedia2:: Error (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="320ca-106">IWMPMedia2::Error property</span></span>

<span data-ttu-id="320ca-107">Die **Error** -Eigenschaft ruft eine **iwmperroritem** -Schnittstelle ab, wenn das Medien Element einen Fehlerzustand aufweist.</span><span class="sxs-lookup"><span data-stu-id="320ca-107">The **Error** property gets an **IWMPErrorItem** interface if the media item has an error condition.</span></span>

<span data-ttu-id="320ca-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="320ca-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="320ca-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="320ca-109">Syntax</span></span>


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a><span data-ttu-id="320ca-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="320ca-110">Property value</span></span>

<span data-ttu-id="320ca-111">Eine **WMPLib. iwmperroritem** -Schnittstelle, die Zugriff auf Informationen über den Fehlerzustand bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="320ca-111">A **WMPLib.IWMPErrorItem** interface that provides access to information about the error condition.</span></span>

## <a name="remarks"></a><span data-ttu-id="320ca-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="320ca-112">Remarks</span></span>

<span data-ttu-id="320ca-113">Wenn das Medien Element nicht wiedergegeben werden kann, ruft diese Eigenschaft eine **iwmperroritem** -Schnittstelle ab, die Informationen über das aufgetretene Problem enthält.</span><span class="sxs-lookup"><span data-stu-id="320ca-113">If the media item cannot be played, this property gets an **IWMPErrorItem** interface that contains information about the problem encountered.</span></span>

## <a name="requirements"></a><span data-ttu-id="320ca-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="320ca-114">Requirements</span></span>



| <span data-ttu-id="320ca-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="320ca-115">Requirement</span></span> | <span data-ttu-id="320ca-116">Wert</span><span class="sxs-lookup"><span data-stu-id="320ca-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="320ca-117">Version</span><span class="sxs-lookup"><span data-stu-id="320ca-117">Version</span></span><br/>   | <span data-ttu-id="320ca-118">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="320ca-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="320ca-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="320ca-119">Namespace</span></span><br/> | <span data-ttu-id="320ca-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="320ca-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="320ca-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="320ca-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="320ca-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="320ca-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="320ca-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="320ca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="320ca-124">**Iwmperroritem (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="320ca-124">**IWMPErrorItem (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="320ca-125">**IWMPMedia2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="320ca-125">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





