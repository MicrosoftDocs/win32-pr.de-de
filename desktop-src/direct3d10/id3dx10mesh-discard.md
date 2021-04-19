---
description: 'Entfernt Mesh-Daten von dem Gerät, für das ein Commit an das Gerät ausgeführt wurde (mit ID3DX10Mesh:: commitcomdevice).'
ms.assetid: 60eee1f8-f04b-4f33-8f86-0564d0334f97
title: ID3DX10Mesh::D iscard-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Discard
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f861de8eefff603954e896a1b6684afc8806764f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367372"
---
# <a name="id3dx10meshdiscard-method"></a><span data-ttu-id="5adbf-103">ID3DX10Mesh::D iscard-Methode</span><span class="sxs-lookup"><span data-stu-id="5adbf-103">ID3DX10Mesh::Discard method</span></span>

<span data-ttu-id="5adbf-104">Entfernt Mesh-Daten von dem Gerät, für das ein Commit an das Gerät ausgeführt wurde (mit [**ID3DX10Mesh:: commitcomdevice**](id3dx10mesh-committodevice.md)).</span><span class="sxs-lookup"><span data-stu-id="5adbf-104">Removes mesh data from the device that has been committed to the device (with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="5adbf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5adbf-105">Syntax</span></span>


```C++
HRESULT Discard(
  [in] D3DX10_MESH_DISCARD_FLAGS dwDiscard
);
```



## <a name="parameters"></a><span data-ttu-id="5adbf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5adbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5adbf-107">*dwdiscard* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5adbf-107">*dwDiscard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5adbf-108">Type: **[ **d3dx10 \_ Mesh- \_ Verwerfungs \_ Flags**](d3dx10-mesh-discard-flags.md)**</span><span class="sxs-lookup"><span data-stu-id="5adbf-108">Type: **[**D3DX10\_MESH\_DISCARD\_FLAGS**](d3dx10-mesh-discard-flags.md)**</span></span>

<span data-ttu-id="5adbf-109">Gibt an, welche Teile von Mesh-Daten vom Gerät verworfen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5adbf-109">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="5adbf-110">Siehe [**d3dx10 \_ Mesh- \_ Verwerfungs \_ Flags**](d3dx10-mesh-discard-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5adbf-110">See [**D3DX10\_MESH\_DISCARD\_FLAGS**](d3dx10-mesh-discard-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5adbf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5adbf-111">Return value</span></span>

<span data-ttu-id="5adbf-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5adbf-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5adbf-113">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="5adbf-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5adbf-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5adbf-114">Requirements</span></span>



| <span data-ttu-id="5adbf-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5adbf-115">Requirement</span></span> | <span data-ttu-id="5adbf-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5adbf-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5adbf-117">Header</span><span class="sxs-lookup"><span data-stu-id="5adbf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5adbf-118"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5adbf-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5adbf-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5adbf-119">Library</span></span><br/> | <dl> <span data-ttu-id="5adbf-120"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5adbf-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5adbf-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5adbf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5adbf-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="5adbf-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="5adbf-123">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5adbf-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




