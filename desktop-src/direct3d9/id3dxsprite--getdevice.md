---
description: Ruft das Gerät ab, das dem Sprite-Objekt zugeordnet ist.
ms.assetid: 9ce18623-893e-4395-bdf7-8d16a641a557
title: 'ID3DXSprite:: getdevice-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf98eb932971a22232a5dbc8f0d5449f8639db97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394193"
---
# <a name="id3dxspritegetdevice-method"></a><span data-ttu-id="26229-103">ID3DXSprite:: getdevice-Methode</span><span class="sxs-lookup"><span data-stu-id="26229-103">ID3DXSprite::GetDevice method</span></span>

<span data-ttu-id="26229-104">Ruft das Gerät ab, das dem Sprite-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="26229-104">Retrieves the device associated with the sprite object.</span></span>

## <a name="syntax"></a><span data-ttu-id="26229-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="26229-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="26229-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="26229-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26229-107">*ppdevice* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="26229-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="26229-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="26229-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="26229-109">Adresse eines Zeigers auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Direct3D-Geräte Objekt darstellt, das dem Sprite-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="26229-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the sprite object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26229-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26229-110">Return value</span></span>

<span data-ttu-id="26229-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="26229-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="26229-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="26229-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="26229-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="26229-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="26229-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26229-114">Remarks</span></span>

<span data-ttu-id="26229-115">Durch Aufrufen dieser Methode wird der interne Verweis Zähler in der [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle vergrößert.</span><span class="sxs-lookup"><span data-stu-id="26229-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="26229-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26229-116">Requirements</span></span>



| <span data-ttu-id="26229-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26229-117">Requirement</span></span> | <span data-ttu-id="26229-118">Wert</span><span class="sxs-lookup"><span data-stu-id="26229-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26229-119">Header</span><span class="sxs-lookup"><span data-stu-id="26229-119">Header</span></span><br/>  | <dl> <span data-ttu-id="26229-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="26229-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="26229-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="26229-121">Library</span></span><br/> | <dl> <span data-ttu-id="26229-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26229-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="26229-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26229-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26229-124">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="26229-124">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 
