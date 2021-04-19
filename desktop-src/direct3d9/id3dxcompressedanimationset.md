---
description: Eine Anwendung verwendet die Methoden dieser Schnittstelle zum Implementieren eines Keyframe-Animations Satzes, der in einem komprimierten Datenformat gespeichert ist.
ms.assetid: 858f09b7-c3b6-4e22-8017-ce2d6188ba80
title: ID3DXCompressedAnimationSet-Schnittstelle (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33dd1017859be14924d8d40265696cfb552754ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363980"
---
# <a name="id3dxcompressedanimationset-interface"></a><span data-ttu-id="b27f1-103">ID3DXCompressedAnimationSet-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b27f1-103">ID3DXCompressedAnimationSet interface</span></span>

<span data-ttu-id="b27f1-104">Eine Anwendung verwendet die Methoden dieser Schnittstelle zum Implementieren eines Keyframe-Animations Satzes, der in einem komprimierten Datenformat gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="b27f1-104">An application uses the methods of this interface to implement a key frame animation set stored in a compressed data format.</span></span>

## <a name="members"></a><span data-ttu-id="b27f1-105">Member</span><span class="sxs-lookup"><span data-stu-id="b27f1-105">Members</span></span>

<span data-ttu-id="b27f1-106">Die **ID3DXCompressedAnimationSet** -Schnittstelle erbt von [**ID3DXAnimationSet**](id3dxanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="b27f1-106">The **ID3DXCompressedAnimationSet** interface inherits from [**ID3DXAnimationSet**](id3dxanimationset.md).</span></span> <span data-ttu-id="b27f1-107">**ID3DXCompressedAnimationSet** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b27f1-107">**ID3DXCompressedAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="b27f1-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="b27f1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b27f1-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="b27f1-109">Methods</span></span>

<span data-ttu-id="b27f1-110">Die **ID3DXCompressedAnimationSet** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b27f1-110">The **ID3DXCompressedAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="b27f1-111">Methode</span><span class="sxs-lookup"><span data-stu-id="b27f1-111">Method</span></span>                                                                                  | <span data-ttu-id="b27f1-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b27f1-112">Description</span></span>                                                                      |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="b27f1-113">**Getcallbackkeys**</span><span class="sxs-lookup"><span data-stu-id="b27f1-113">**GetCallbackKeys**</span></span>](id3dxcompressedanimationset--getcallbackkeys.md)                 | <span data-ttu-id="b27f1-114">Füllt ein Array mit Rückruf Schlüsseldaten, die für die Keyframe-Animation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b27f1-114">Fills an array with callback key data used for key frame animation.</span></span><br/>   |
| [<span data-ttu-id="b27f1-115">**Getcompresseddata**</span><span class="sxs-lookup"><span data-stu-id="b27f1-115">**GetCompressedData**</span></span>](id3dxcompressedanimationset--getcompresseddata.md)             | <span data-ttu-id="b27f1-116">Ruft den Datenpuffer ab, in dem komprimierte Keyframe-Animationsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b27f1-116">Gets the data buffer that stores compressed key frame animation data.</span></span><br/> |
| [<span data-ttu-id="b27f1-117">**Getnumcallbackkeys**</span><span class="sxs-lookup"><span data-stu-id="b27f1-117">**GetNumCallbackKeys**</span></span>](id3dxcompressedanimationset--getnumcallbackkeys.md)           | <span data-ttu-id="b27f1-118">Ruft die Anzahl der Rückruf Schlüssel im Animations Satz ab.</span><span class="sxs-lookup"><span data-stu-id="b27f1-118">Gets the number of callback keys in the animation set.</span></span><br/>                |
| [<span data-ttu-id="b27f1-119">**Getplaybacktype**</span><span class="sxs-lookup"><span data-stu-id="b27f1-119">**GetPlaybackType**</span></span>](id3dxcompressedanimationset--getplaybacktype.md)                 | <span data-ttu-id="b27f1-120">Ruft den Typ der Wiedergabe Schleife für Animations Sätze ab.</span><span class="sxs-lookup"><span data-stu-id="b27f1-120">Gets the type of the animation set playback loop.</span></span><br/>                     |
| [<span data-ttu-id="b27f1-121">**Getsourcetickspersecond**</span><span class="sxs-lookup"><span data-stu-id="b27f1-121">**GetSourceTicksPerSecond**</span></span>](id3dxcompressedanimationset--getsourcetickspersecond.md) | <span data-ttu-id="b27f1-122">Ruft die Anzahl der pro Sekunde auftretenden Animations Tastatur-Frame Ticks ab.</span><span class="sxs-lookup"><span data-stu-id="b27f1-122">Gets the number of animation key frame ticks that occur per second.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="b27f1-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b27f1-123">Remarks</span></span>

<span data-ttu-id="b27f1-124">Erstellen Sie mit [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md)einen Keyframe-Animations Satz mit komprimiertem Format.</span><span class="sxs-lookup"><span data-stu-id="b27f1-124">Create a compressed-format key frame animation set with [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).</span></span>

<span data-ttu-id="b27f1-125">Der LPD3DXCOMPRESSEDANIMATIONSET-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="b27f1-125">The LPD3DXCOMPRESSEDANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXCompressedAnimationSet ID3DXCompressedAnimationSet;
typedef interface ID3DXCompressedAnimationSet *LPD3DXCOMPRESSEDANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="b27f1-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b27f1-126">Requirements</span></span>



| <span data-ttu-id="b27f1-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b27f1-127">Requirement</span></span> | <span data-ttu-id="b27f1-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b27f1-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b27f1-129">Header</span><span class="sxs-lookup"><span data-stu-id="b27f1-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b27f1-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b27f1-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b27f1-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b27f1-131">Library</span></span><br/> | <dl> <span data-ttu-id="b27f1-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b27f1-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b27f1-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b27f1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b27f1-134">**ID3DXAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="b27f1-134">**ID3DXAnimationSet**</span></span>](id3dxanimationset.md)
</dt> <dt>

[<span data-ttu-id="b27f1-135">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b27f1-135">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




