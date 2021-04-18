---
description: Ruft die Anzahl der Farbkanäle ab, die im Arbeitsspeicher zum Speichern von Beispielen verwendet werden.
ms.assetid: dd1e3590-78e1-41a2-9f15-79389d9a210a
title: 'ID3DXPRTBuffer:: getnumchannels-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.GetNumChannels
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 99456c6386a822489eca6beef41f639008007778
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364401"
---
# <a name="id3dxprtbuffergetnumchannels-method"></a><span data-ttu-id="511b7-103">ID3DXPRTBuffer:: getnumchannels-Methode</span><span class="sxs-lookup"><span data-stu-id="511b7-103">ID3DXPRTBuffer::GetNumChannels method</span></span>

<span data-ttu-id="511b7-104">Ruft die Anzahl der Farbkanäle ab, die im Arbeitsspeicher zum Speichern von Beispielen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="511b7-104">Retrieves the number of color channels used in memory to store samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="511b7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="511b7-105">Syntax</span></span>


```C++
UINT GetNumChannels();
```



## <a name="parameters"></a><span data-ttu-id="511b7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="511b7-106">Parameters</span></span>

<span data-ttu-id="511b7-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="511b7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="511b7-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="511b7-108">Return value</span></span>

<span data-ttu-id="511b7-109">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="511b7-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="511b7-110">Gibt die Anzahl der Farbkanäle zurück, die im Arbeitsspeicher zum Speichern von Beispielen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="511b7-110">Returns the number of color channels used in memory to store samples.</span></span> <span data-ttu-id="511b7-111">Der Wert ist im Allgemeinen entweder 1, um die Werte für die Leuchtkraft anzugeben, oder 3, um RGB-Werte darzustellen.</span><span class="sxs-lookup"><span data-stu-id="511b7-111">The value generally will be either 1 to represent luminance values, or 3 to represent RGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="511b7-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="511b7-112">Requirements</span></span>



| <span data-ttu-id="511b7-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="511b7-113">Requirement</span></span> | <span data-ttu-id="511b7-114">Wert</span><span class="sxs-lookup"><span data-stu-id="511b7-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="511b7-115">Header</span><span class="sxs-lookup"><span data-stu-id="511b7-115">Header</span></span><br/>  | <dl> <span data-ttu-id="511b7-116"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="511b7-116"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="511b7-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="511b7-117">Library</span></span><br/> | <dl> <span data-ttu-id="511b7-118"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="511b7-118"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="511b7-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="511b7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="511b7-120">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="511b7-120">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
