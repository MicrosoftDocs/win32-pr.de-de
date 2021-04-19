---
title: Iwmpcdromburn burnwiedergabe (Eigenschaft)
description: Die burnwiedergabe-Eigenschaft ruft die aktuelle Wiedergabeliste ab, die auf die CD brennen soll.
ms.assetid: 973032de-7249-4ccd-9909-ccc888f4490f
keywords:
- burnwiedergabe-Eigenschaften Fenster Media Player
- burnwiedergabe-Eigenschaft, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, burnwiedergabe (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnPlaylist
- IWMPCdromBurn.get_burnPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae095696b9c106926fb7f363430574b2eb87cea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369132"
---
# <a name="iwmpcdromburnburnplaylist-property"></a><span data-ttu-id="c2d27-106">Iwmpcdromburn:: burnwiedergabe (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c2d27-106">IWMPCdromBurn::burnPlaylist property</span></span>

<span data-ttu-id="c2d27-107">Die **burnwiedergabe** -Eigenschaft ruft die aktuelle Wiedergabeliste ab, die auf die CD brennen soll.</span><span class="sxs-lookup"><span data-stu-id="c2d27-107">The **burnPlaylist** property gets the current playlist to burn to the CD.</span></span>

<span data-ttu-id="c2d27-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c2d27-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2d27-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2d27-109">Syntax</span></span>


```CSharp
public IWMPPlaylist burnPlaylist {get;}
```


```VB

Public ReadOnly Property burnPlaylist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="c2d27-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c2d27-110">Property value</span></span>

<span data-ttu-id="c2d27-111">Die **WMPLib. iwmpwiedergabe** -Schnittstelle der zu brennenden Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="c2d27-111">The **WMPLib.IWMPPlaylist** interface of the playlist to burn.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2d27-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2d27-112">Requirements</span></span>



| <span data-ttu-id="c2d27-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2d27-113">Requirement</span></span> | <span data-ttu-id="c2d27-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c2d27-114">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d27-115">Version</span><span class="sxs-lookup"><span data-stu-id="c2d27-115">Version</span></span><br/>   | <span data-ttu-id="c2d27-116">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="c2d27-116">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="c2d27-117">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2d27-117">Namespace</span></span><br/> | <span data-ttu-id="c2d27-118">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c2d27-118">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c2d27-119">Assembly</span><span class="sxs-lookup"><span data-stu-id="c2d27-119">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c2d27-120"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c2d27-120"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2d27-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2d27-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2d27-122">**Iwmpcdromburn-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c2d27-122">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c2d27-123">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c2d27-123">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





