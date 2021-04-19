---
description: Verknüpft ein ID3DXTextureGutterHelper-Objekt mit dem ID3DXPRTBuffer-Objekt.
ms.assetid: 095fea82-ac7a-42fa-990a-084715c73823
title: 'ID3DXPRTBuffer:: attachgh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AttachGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba5afa238107d60620291b50b8f184eb4e5d361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353744"
---
# <a name="id3dxprtbufferattachgh-method"></a><span data-ttu-id="0eadb-103">ID3DXPRTBuffer:: attachgh-Methode</span><span class="sxs-lookup"><span data-stu-id="0eadb-103">ID3DXPRTBuffer::AttachGH method</span></span>

<span data-ttu-id="0eadb-104">Verknüpft ein [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Objekt mit dem [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="0eadb-104">Associates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eadb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0eadb-105">Syntax</span></span>


```C++
HRESULT AttachGH(
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a><span data-ttu-id="0eadb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0eadb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eadb-107">*pgh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0eadb-107">*pGH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0eadb-108">Typ: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span><span class="sxs-lookup"><span data-stu-id="0eadb-108">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span></span>

<span data-ttu-id="0eadb-109">Ein Zeiger auf die [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Schnittstelle eines Objekts, das Textur Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="0eadb-109">Pointer to the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) interface of an object that contains texture gutter data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0eadb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0eadb-110">Return value</span></span>

<span data-ttu-id="0eadb-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0eadb-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0eadb-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0eadb-112">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0eadb-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0eadb-113">Remarks</span></span>

<span data-ttu-id="0eadb-114">Der Verweis Zähler des [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Objekts wird automatisch um 1 erhöht.</span><span class="sxs-lookup"><span data-stu-id="0eadb-114">The reference count of the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object will automatically be incremented by one.</span></span> <span data-ttu-id="0eadb-115">Vorhandene **ID3DXTextureGutterHelper** -Zeiger werden freigegeben.</span><span class="sxs-lookup"><span data-stu-id="0eadb-115">Any existing **ID3DXTextureGutterHelper** pointers will be released.</span></span>

<span data-ttu-id="0eadb-116">Sie müssen sicherstellen, dass die Anzahl von **ID3DXPRTBuffer:: attachgh** -aufrufen mit der Anzahl von [**ID3DXPRTBuffer:: releasegh**](id3dxprtbuffer--releasegh.md) -aufrufen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="0eadb-116">You must ensure that the number of **ID3DXPRTBuffer::AttachGH** calls matches the number of [**ID3DXPRTBuffer::ReleaseGH**](id3dxprtbuffer--releasegh.md) calls.</span></span> <span data-ttu-id="0eadb-117">Nach dem Aufruf von **ID3DXPRTBuffer:: releasegh** sollte der von **ID3DXPRTBuffer:: attachgh** zurückgegebene pgh-Zeiger nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0eadb-117">After calling **ID3DXPRTBuffer::ReleaseGH**, the pGH pointer returned by **ID3DXPRTBuffer::AttachGH** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eadb-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0eadb-118">Requirements</span></span>



| <span data-ttu-id="0eadb-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0eadb-119">Requirement</span></span> | <span data-ttu-id="0eadb-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0eadb-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0eadb-121">Header</span><span class="sxs-lookup"><span data-stu-id="0eadb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0eadb-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0eadb-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0eadb-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0eadb-123">Library</span></span><br/> | <dl> <span data-ttu-id="0eadb-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0eadb-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0eadb-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0eadb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eadb-126">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="0eadb-126">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="0eadb-127">**ID3DXPRTBuffer:: releasegh**</span><span class="sxs-lookup"><span data-stu-id="0eadb-127">**ID3DXPRTBuffer::ReleaseGH**</span></span>](id3dxprtbuffer--releasegh.md)
</dt> </dl>

 

 




