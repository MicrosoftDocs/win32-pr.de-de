---
description: Ruft das Gerät ab, das dem Effekt zugeordnet ist.
ms.assetid: acef5d0a-b185-4054-8982-0580440ab76b
title: 'ID3DXEffect:: getdevice-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fde2d9f3d9db362bf48fda66e9da10b91a864bb0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365358"
---
# <a name="id3dxeffectgetdevice-method"></a><span data-ttu-id="ca34d-103">ID3DXEffect:: getdevice-Methode</span><span class="sxs-lookup"><span data-stu-id="ca34d-103">ID3DXEffect::GetDevice method</span></span>

<span data-ttu-id="ca34d-104">Ruft das Gerät ab, das dem Effekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ca34d-104">Retrieves the device associated with the effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca34d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca34d-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="ca34d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca34d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca34d-107">*ppdevice* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ca34d-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca34d-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="ca34d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="ca34d-109">Adresse eines Zeigers auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das dem Effekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ca34d-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca34d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca34d-110">Return value</span></span>

<span data-ttu-id="ca34d-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca34d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca34d-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ca34d-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ca34d-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="ca34d-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca34d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca34d-114">Remarks</span></span>

<span data-ttu-id="ca34d-115">Durch Aufrufen dieser Methode wird der interne Verweis Zähler für die [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle vergrößert.</span><span class="sxs-lookup"><span data-stu-id="ca34d-115">Calling this method will increase the internal reference count for the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="ca34d-116">Stellen Sie sicher, dass Sie "IUnknown:: Release" anrufen, wenn Sie die **IDirect3DDevice9** -Schnittstelle verwenden oder wenn Sie einen Speicherplatz haben.</span><span class="sxs-lookup"><span data-stu-id="ca34d-116">Be sure to call IUnknown::Release when you are done using the **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca34d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca34d-117">Requirements</span></span>



| <span data-ttu-id="ca34d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca34d-118">Requirement</span></span> | <span data-ttu-id="ca34d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ca34d-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca34d-120">Header</span><span class="sxs-lookup"><span data-stu-id="ca34d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ca34d-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca34d-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="ca34d-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ca34d-122">Library</span></span><br/> | <dl> <span data-ttu-id="ca34d-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca34d-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ca34d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca34d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca34d-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="ca34d-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
