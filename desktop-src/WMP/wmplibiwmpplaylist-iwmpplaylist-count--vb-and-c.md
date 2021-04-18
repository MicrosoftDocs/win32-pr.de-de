---
title: Iwmpwiedergabe count (Eigenschaft)
description: Die Count-Eigenschaft ruft die Anzahl der Medienelemente in einer Wiedergabeliste ab.
ms.assetid: dbff3c86-2d42-4d47-a5cb-b8199efac728
keywords:
- Anzahl der Eigenschaften Fenster Media Player
- Count-Eigenschaft, Windows Media Player, iwmpwiedergabe-Schnittstelle
- Iwmpwiedergabe Interface, Windows Media Player, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPPlaylist.count
- IWMPPlaylist.get_count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d988fefc436b65652d2b0765320ca289417c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354703"
---
# <a name="iwmpplaylistcount-property"></a><span data-ttu-id="4c91b-106">Iwmpwiedergabe:: count (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4c91b-106">IWMPPlaylist::count property</span></span>

<span data-ttu-id="4c91b-107">Die **count** -Eigenschaft ruft die Anzahl der Medienelemente in einer Wiedergabeliste ab.</span><span class="sxs-lookup"><span data-stu-id="4c91b-107">The **count** property gets the number of media items in a playlist.</span></span>

<span data-ttu-id="4c91b-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4c91b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c91b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c91b-109">Syntax</span></span>


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="4c91b-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4c91b-110">Property value</span></span>

<span data-ttu-id="4c91b-111">Ein **System. Int32** -Wert, der die Anzahl der Medienelemente in der Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="4c91b-111">A **System.Int32** that is the number of media items in the playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c91b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c91b-112">Remarks</span></span>

<span data-ttu-id="4c91b-113">Vor der Verwendung dieser Eigenschaft müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="4c91b-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="4c91b-114">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="4c91b-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="4c91b-115">Einen Beispielcode, der diese Eigenschaft verwendet, finden Sie unter der [AttributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4c91b-115">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c91b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c91b-116">Requirements</span></span>



| <span data-ttu-id="4c91b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c91b-117">Requirement</span></span> | <span data-ttu-id="4c91b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4c91b-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c91b-119">Version</span><span class="sxs-lookup"><span data-stu-id="4c91b-119">Version</span></span><br/>   | <span data-ttu-id="4c91b-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="4c91b-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4c91b-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c91b-121">Namespace</span></span><br/> | <span data-ttu-id="4c91b-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4c91b-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4c91b-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="4c91b-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4c91b-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4c91b-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c91b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c91b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c91b-126">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="4c91b-126">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





