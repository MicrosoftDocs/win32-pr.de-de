---
description: Ruft das dem Mesh zugeordnete Gerät ab.
ms.assetid: 16ff5267-0c64-4c3d-925d-6fc10f54c9c4
title: 'ID3DXBaseMesh:: getdevice-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2b866c86bf759305a4626f0ff5ecaa8e35bfd75d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050880"
---
# <a name="id3dxbasemeshgetdevice-method"></a><span data-ttu-id="15f79-103">ID3DXBaseMesh:: getdevice-Methode</span><span class="sxs-lookup"><span data-stu-id="15f79-103">ID3DXBaseMesh::GetDevice method</span></span>

<span data-ttu-id="15f79-104">Ruft das dem Mesh zugeordnete Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="15f79-104">Retrieves the device associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="15f79-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15f79-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="15f79-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="15f79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15f79-107">*ppdevice* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="15f79-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="15f79-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="15f79-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="15f79-109">Adresse eines Zeigers auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das dem Mesh zugeordnete Direct3D-Geräte Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="15f79-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15f79-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15f79-110">Return value</span></span>

<span data-ttu-id="15f79-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="15f79-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="15f79-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="15f79-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="15f79-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="15f79-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="15f79-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15f79-114">Remarks</span></span>

<span data-ttu-id="15f79-115">Durch Aufrufen dieser Methode wird der interne Verweis Zähler in der [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle vergrößert.</span><span class="sxs-lookup"><span data-stu-id="15f79-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="15f79-116">Stellen Sie sicher, dass [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) aufgerufen wird, wenn Sie die **IDirect3DDevice9** -Schnittstelle verwenden, oder wenn Sie einen Speicherplatz haben.</span><span class="sxs-lookup"><span data-stu-id="15f79-116">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="15f79-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15f79-117">Requirements</span></span>



| <span data-ttu-id="15f79-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15f79-118">Requirement</span></span> | <span data-ttu-id="15f79-119">Wert</span><span class="sxs-lookup"><span data-stu-id="15f79-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15f79-120">Header</span><span class="sxs-lookup"><span data-stu-id="15f79-120">Header</span></span><br/>  | <dl> <span data-ttu-id="15f79-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="15f79-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="15f79-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="15f79-122">Library</span></span><br/> | <dl> <span data-ttu-id="15f79-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15f79-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="15f79-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15f79-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15f79-125">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="15f79-125">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
