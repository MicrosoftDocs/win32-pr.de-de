---
description: Ruft den Index der Gitterfläche ab, zu der jeder textexgehört.
ms.assetid: 3eb3461c-4e16-4c89-9ca9-fc9c6b5638c7
title: 'ID3DXTextureGutterHelper:: getfacemap-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8164ec35c3b3596914577287ecc6b9285142fca8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367455"
---
# <a name="id3dxtexturegutterhelpergetfacemap-method"></a><span data-ttu-id="3de41-103">ID3DXTextureGutterHelper:: getfacemap-Methode</span><span class="sxs-lookup"><span data-stu-id="3de41-103">ID3DXTextureGutterHelper::GetFaceMap method</span></span>

<span data-ttu-id="3de41-104">Ruft den Index der Gitterfläche ab, zu der jeder textexgehört.</span><span class="sxs-lookup"><span data-stu-id="3de41-104">Retrieves the index of the mesh face to which each texel belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de41-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3de41-105">Syntax</span></span>


```C++
HRESULT GetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a><span data-ttu-id="3de41-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3de41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3de41-107">*pfacedata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3de41-107">*pFaceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3de41-108">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3de41-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3de41-109">Zeiger auf den Index der Mesh-Seite, zu der jeder textexgehört.</span><span class="sxs-lookup"><span data-stu-id="3de41-109">Pointer to the index of the mesh face to which each texel belongs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3de41-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3de41-110">Return value</span></span>

<span data-ttu-id="3de41-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3de41-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3de41-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3de41-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3de41-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="3de41-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="3de41-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3de41-114">Remarks</span></span>

<span data-ttu-id="3de41-115">Die von dieser Methode zurückgegebenen mesface-Daten sind nur für gültige Texels (Non-Class 0) gültig.</span><span class="sxs-lookup"><span data-stu-id="3de41-115">The mesh face data returned by this method is valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="3de41-116">[**ID3DXTextureGutterHelper:: getguttermap**](id3dxtexturegutterhelper--getguttermap.md) gibt Werte ungleich 0 (null) für gültige Texels (nicht Klassen 0) zurück.</span><span class="sxs-lookup"><span data-stu-id="3de41-116">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return nonzero values for valid (non-class 0) texels.</span></span>

<span data-ttu-id="3de41-117">Bei [**Klasse 2 texeln**](id3dxtexturegutterhelper.md)ruft diese Methode das nächste Gesicht ab.</span><span class="sxs-lookup"><span data-stu-id="3de41-117">For [**class 2 texels**](id3dxtexturegutterhelper.md), this method retrieves the closest face.</span></span>

<span data-ttu-id="3de41-118">Die Anwendung muss pfacedata zuordnen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="3de41-118">The application must allocate and manage pFaceData.</span></span>

## <a name="requirements"></a><span data-ttu-id="3de41-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3de41-119">Requirements</span></span>



| <span data-ttu-id="3de41-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3de41-120">Requirement</span></span> | <span data-ttu-id="3de41-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3de41-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3de41-122">Header</span><span class="sxs-lookup"><span data-stu-id="3de41-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3de41-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3de41-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3de41-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3de41-124">Library</span></span><br/> | <dl> <span data-ttu-id="3de41-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3de41-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3de41-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3de41-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de41-127">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="3de41-127">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
