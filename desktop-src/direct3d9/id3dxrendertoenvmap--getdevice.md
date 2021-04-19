---
description: Ruft das Direct3D-Gerät ab, das der Umgebungs Zuordnung zugeordnet ist.
ms.assetid: 15f342c5-7665-443a-b7b8-32cc67034c41
title: 'ID3DXRenderToEnvMap:: getdevice-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b5adc045beeefa220a849a6da752a8d3efc82ff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371901"
---
# <a name="id3dxrendertoenvmapgetdevice-method"></a><span data-ttu-id="ec71b-103">ID3DXRenderToEnvMap:: getdevice-Methode</span><span class="sxs-lookup"><span data-stu-id="ec71b-103">ID3DXRenderToEnvMap::GetDevice method</span></span>

<span data-ttu-id="ec71b-104">Ruft das Direct3D-Gerät ab, das der Umgebungs Zuordnung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ec71b-104">Retrieves the Direct3D device associated with the environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec71b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec71b-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="ec71b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec71b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec71b-107">*ppdevice* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ec71b-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ec71b-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="ec71b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="ec71b-109">Adresse eines Zeigers auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Direct3D-Geräte Objekt darstellt, das der Umgebungs Zuordnung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ec71b-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface that represents the Direct3D device object associated with the environment map.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec71b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec71b-110">Return value</span></span>

<span data-ttu-id="ec71b-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ec71b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ec71b-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ec71b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ec71b-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="ec71b-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="ec71b-114">Das Aufrufen dieser Methode erhöht den internen Verweis Zähler in der [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ec71b-114">Calling this method increases the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="ec71b-115">Stellen Sie sicher, dass [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) aufgerufen wird, wenn Sie die **IDirect3DDevice9** -Schnittstelle verwenden, oder wenn Sie einen Speicherplatz haben.</span><span class="sxs-lookup"><span data-stu-id="ec71b-115">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec71b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec71b-116">Requirements</span></span>



| <span data-ttu-id="ec71b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec71b-117">Requirement</span></span> | <span data-ttu-id="ec71b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ec71b-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec71b-119">Header</span><span class="sxs-lookup"><span data-stu-id="ec71b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ec71b-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec71b-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="ec71b-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ec71b-121">Library</span></span><br/> | <dl> <span data-ttu-id="ec71b-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec71b-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ec71b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec71b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec71b-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="ec71b-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
