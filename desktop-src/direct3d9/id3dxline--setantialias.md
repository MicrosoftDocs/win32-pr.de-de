---
description: Schaltet das Zeilen-Antialiasing um.
ms.assetid: 9c212823-2dc6-40dd-b1aa-9fc4a2c540f4
title: 'ID3DXLine:: setantialias-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetAntialias
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893e2061beedb6d45dc86e87903613984e3d1785
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365138"
---
# <a name="id3dxlinesetantialias-method"></a><span data-ttu-id="99b58-103">ID3DXLine:: setantialias-Methode</span><span class="sxs-lookup"><span data-stu-id="99b58-103">ID3DXLine::SetAntialias method</span></span>

<span data-ttu-id="99b58-104">Schaltet das Zeilen-Antialiasing um.</span><span class="sxs-lookup"><span data-stu-id="99b58-104">Toggles line antialiasing.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b58-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="99b58-105">Syntax</span></span>


```C++
HRESULT SetAntialias(
  [in] BOOL bAntiAlias
);
```



## <a name="parameters"></a><span data-ttu-id="99b58-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="99b58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b58-107">*bantialias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99b58-107">*bAntiAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b58-108">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99b58-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99b58-109">Schaltet das Antialiasing ein und aus.</span><span class="sxs-lookup"><span data-stu-id="99b58-109">Toggles antialiasing on and off.</span></span> <span data-ttu-id="99b58-110">**True** schaltet das Antialiasing ein, und **false** deaktiviert das Antialiasing.</span><span class="sxs-lookup"><span data-stu-id="99b58-110">**TRUE** turns antialiasing on, and **FALSE** turns antialiasing off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99b58-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99b58-111">Return value</span></span>

<span data-ttu-id="99b58-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99b58-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99b58-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99b58-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="99b58-114">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="99b58-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="99b58-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99b58-115">Requirements</span></span>



| <span data-ttu-id="99b58-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99b58-116">Requirement</span></span> | <span data-ttu-id="99b58-117">Wert</span><span class="sxs-lookup"><span data-stu-id="99b58-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99b58-118">Header</span><span class="sxs-lookup"><span data-stu-id="99b58-118">Header</span></span><br/>  | <dl> <span data-ttu-id="99b58-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="99b58-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="99b58-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="99b58-120">Library</span></span><br/> | <dl> <span data-ttu-id="99b58-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99b58-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="99b58-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99b58-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b58-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="99b58-123">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="99b58-124">**ID3DXLine:: getAntialias**</span><span class="sxs-lookup"><span data-stu-id="99b58-124">**ID3DXLine::GetAntialias**</span></span>](id3dxline--getantialias.md)
</dt> </dl>

 

 
