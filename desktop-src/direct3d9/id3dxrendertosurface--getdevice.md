---
description: Ruft das Direct3D-Gerät ab, das der Renderoberfläche zugeordnet ist.
ms.assetid: 579cf7da-b8e0-4d9f-93b8-b1f47c3d5654
title: 'ID3DXRenderToSurface:: getdevice-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac01744887412349c71daa34194fc3a0b03b19a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355836"
---
# <a name="id3dxrendertosurfacegetdevice-method"></a><span data-ttu-id="cdc0d-103">ID3DXRenderToSurface:: getdevice-Methode</span><span class="sxs-lookup"><span data-stu-id="cdc0d-103">ID3DXRenderToSurface::GetDevice method</span></span>

<span data-ttu-id="cdc0d-104">Ruft das Direct3D-Gerät ab, das der Renderoberfläche zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-104">Retrieves the Direct3D device associated with the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc0d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdc0d-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="cdc0d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdc0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdc0d-107">*ppdevice* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cdc0d-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cdc0d-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="cdc0d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="cdc0d-109">Adresse eines Zeigers auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Direct3D-Geräte Objekt darstellt, das der Renderoberfläche zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdc0d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdc0d-110">Return value</span></span>

<span data-ttu-id="cdc0d-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cdc0d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cdc0d-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cdc0d-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="cdc0d-114">Durch Aufrufen dieser Methode wird der interne Verweis Zähler in der [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle vergrößert.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-114">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="cdc0d-115">Stellen Sie sicher, dass [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) aufgerufen wird, wenn Sie die **IDirect3DDevice9** -Schnittstelle verwenden, oder wenn Sie einen Speicherplatz haben.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-115">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc0d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdc0d-116">Requirements</span></span>



| <span data-ttu-id="cdc0d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdc0d-117">Requirement</span></span> | <span data-ttu-id="cdc0d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cdc0d-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc0d-119">Header</span><span class="sxs-lookup"><span data-stu-id="cdc0d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cdc0d-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdc0d-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="cdc0d-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cdc0d-121">Library</span></span><br/> | <dl> <span data-ttu-id="cdc0d-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdc0d-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cdc0d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdc0d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdc0d-124">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="cdc0d-124">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 
