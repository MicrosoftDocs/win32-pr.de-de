---
description: Hebt die Zuordnung eines angefügten ID3DXTextureGutterHelper-Objekts zum ID3DXPRTBuffer-Objekt auf.
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: 'ID3DXPRTBuffer:: releasegh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ReleaseGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9fb7a68f11d21065d6b4911b9ee7f58920aeb25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394258"
---
# <a name="id3dxprtbufferreleasegh-method"></a><span data-ttu-id="26d74-103">ID3DXPRTBuffer:: releasegh-Methode</span><span class="sxs-lookup"><span data-stu-id="26d74-103">ID3DXPRTBuffer::ReleaseGH method</span></span>

<span data-ttu-id="26d74-104">Hebt die Zuordnung eines angefügten [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Objekts zum [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="26d74-104">Unassociates an attached [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="26d74-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="26d74-105">Syntax</span></span>


```C++
HRESULT ReleaseGH();
```



## <a name="parameters"></a><span data-ttu-id="26d74-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="26d74-106">Parameters</span></span>

<span data-ttu-id="26d74-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="26d74-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26d74-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26d74-108">Return value</span></span>

<span data-ttu-id="26d74-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="26d74-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="26d74-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="26d74-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="26d74-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26d74-111">Remarks</span></span>

<span data-ttu-id="26d74-112">Diese Methode gibt den Zeiger auf die [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Schnittstelle frei.</span><span class="sxs-lookup"><span data-stu-id="26d74-112">This method releases the pointer to the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) interface.</span></span>

<span data-ttu-id="26d74-113">Sie müssen sicherstellen, dass die Anzahl von [**ID3DXPRTBuffer:: attachgh**](id3dxprtbuffer--attachgh.md) -aufrufen mit der Anzahl von **ID3DXPRTBuffer:: releasegh** -aufrufen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="26d74-113">You must ensure that the number of [**ID3DXPRTBuffer::AttachGH**](id3dxprtbuffer--attachgh.md) calls matches the number of **ID3DXPRTBuffer::ReleaseGH** calls.</span></span> <span data-ttu-id="26d74-114">Nach dem Aufruf von **ID3DXPRTBuffer:: releasegh** sollte der von **ID3DXPRTBuffer:: attachgh** zurückgegebene pgh-Zeiger nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26d74-114">After calling **ID3DXPRTBuffer::ReleaseGH**, the pGH pointer returned by **ID3DXPRTBuffer::AttachGH** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="26d74-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26d74-115">Requirements</span></span>



| <span data-ttu-id="26d74-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26d74-116">Requirement</span></span> | <span data-ttu-id="26d74-117">Wert</span><span class="sxs-lookup"><span data-stu-id="26d74-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26d74-118">Header</span><span class="sxs-lookup"><span data-stu-id="26d74-118">Header</span></span><br/>  | <dl> <span data-ttu-id="26d74-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="26d74-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="26d74-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="26d74-120">Library</span></span><br/> | <dl> <span data-ttu-id="26d74-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26d74-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="26d74-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26d74-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26d74-123">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="26d74-123">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="26d74-124">**ID3DXPRTBuffer:: attachgh**</span><span class="sxs-lookup"><span data-stu-id="26d74-124">**ID3DXPRTBuffer::AttachGH**</span></span>](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 




