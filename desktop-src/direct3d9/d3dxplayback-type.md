---
description: Definiert den Typ der Animations Satz-Schleifen Modi, die für die Wiedergabe verwendet werden.
ms.assetid: 2ce26bf0-2b33-4193-a58f-03493a051351
title: D3DXPLAYBACK_TYPE-Enumeration (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLAYBACK_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ce95b4765ec678c43c8e0ed92008deeb9927298
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870099"
---
# <a name="d3dxplayback_type-enumeration"></a><span data-ttu-id="12e83-103">D3DXPLAYBACK- \_ Typenumeration</span><span class="sxs-lookup"><span data-stu-id="12e83-103">D3DXPLAYBACK\_TYPE enumeration</span></span>

<span data-ttu-id="12e83-104">Definiert den Typ der Animations Satz-Schleifen Modi, die für die Wiedergabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12e83-104">Defines the type of animation set looping modes used for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="12e83-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="12e83-105">Syntax</span></span>


```C++
typedef enum D3DXPLAYBACK_TYPE { 
  D3DXPLAY_LOOP         = 0,
  D3DXPLAY_ONCE         = 1,
  D3DXPLAY_PINGPONG     = 2,
  D3DXPLAY_FORCE_DWORD  = 0x7fffffff
} D3DXPLAYBACK_TYPE, *LPD3DXPLAYBACK_TYPE;
```



## <a name="constants"></a><span data-ttu-id="12e83-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="12e83-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="12e83-107"><span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**D3DXPLAY- \_ Schleife**</span><span class="sxs-lookup"><span data-stu-id="12e83-107"><span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**D3DXPLAY\_LOOP**</span></span>
</dt> <dd>

<span data-ttu-id="12e83-108">Die Animation wird endlos wiederholt.</span><span class="sxs-lookup"><span data-stu-id="12e83-108">The animation repeats endlessly.</span></span>

</dd> <dt>

<span data-ttu-id="12e83-109"><span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY \_ einmal**</span><span class="sxs-lookup"><span data-stu-id="12e83-109"><span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY\_ONCE**</span></span>
</dt> <dd>

<span data-ttu-id="12e83-110">Die Animation wird einmal abgespielt und dann im letzten Frame angehalten.</span><span class="sxs-lookup"><span data-stu-id="12e83-110">The animation plays once, and then it stops on the last frame.</span></span>

</dd> <dt>

<span data-ttu-id="12e83-111"><span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY \_ Pingpong**</span><span class="sxs-lookup"><span data-stu-id="12e83-111"><span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY\_PINGPONG**</span></span>
</dt> <dd>

<span data-ttu-id="12e83-112">Die Animation wechselt endlos zwischen dem Abspielen und der Wiedergabe von rückwärts.</span><span class="sxs-lookup"><span data-stu-id="12e83-112">The animation alternates endlessly between playing forward and playing backward.</span></span>

</dd> <dt>

<span data-ttu-id="12e83-113"><span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="12e83-113"><span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="12e83-114">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="12e83-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="12e83-115">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="12e83-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="12e83-116">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="12e83-116">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12e83-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12e83-117">Requirements</span></span>



| <span data-ttu-id="12e83-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12e83-118">Requirement</span></span> | <span data-ttu-id="12e83-119">Wert</span><span class="sxs-lookup"><span data-stu-id="12e83-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12e83-120">Header</span><span class="sxs-lookup"><span data-stu-id="12e83-120">Header</span></span><br/> | <dl> <span data-ttu-id="12e83-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="12e83-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12e83-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12e83-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e83-123">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="12e83-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




