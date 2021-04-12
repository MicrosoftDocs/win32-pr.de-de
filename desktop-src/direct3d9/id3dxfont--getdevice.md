---
description: Ruft das Direct3D-Gerät ab, das dem Schriftart Objekt zugeordnet ist.
ms.assetid: c713cbe2-6e6e-476b-a995-14fa149cb088
title: 'ID3DXFont:: getdevice-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2de1b6e2c3b2c2b61576c739d96abc8b8fc8851a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355856"
---
# <a name="id3dxfontgetdevice-method"></a><span data-ttu-id="79af5-103">ID3DXFont:: getdevice-Methode</span><span class="sxs-lookup"><span data-stu-id="79af5-103">ID3DXFont::GetDevice method</span></span>

<span data-ttu-id="79af5-104">Ruft das Direct3D-Gerät ab, das dem Schriftart Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="79af5-104">Retrieves the Direct3D device associated with the font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="79af5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="79af5-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="79af5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="79af5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79af5-107">*ppdevice* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="79af5-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79af5-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="79af5-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="79af5-109">Adresse eines Zeigers auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Direct3D-Geräte Objekt darstellt, das dem Schriftart Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="79af5-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79af5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79af5-110">Return value</span></span>

<span data-ttu-id="79af5-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79af5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79af5-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="79af5-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="79af5-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="79af5-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="79af5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79af5-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="79af5-115">Durch Aufrufen dieser Methode wird der interne Verweis Zähler in der [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle vergrößert.</span><span class="sxs-lookup"><span data-stu-id="79af5-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="79af5-116">Stellen Sie sicher, dass [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) aufgerufen wird, wenn Sie die **IDirect3DDevice9** -Schnittstelle verwenden, oder wenn Sie einen Speicherplatz haben.</span><span class="sxs-lookup"><span data-stu-id="79af5-116">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="79af5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79af5-117">Requirements</span></span>



| <span data-ttu-id="79af5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79af5-118">Requirement</span></span> | <span data-ttu-id="79af5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="79af5-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79af5-120">Header</span><span class="sxs-lookup"><span data-stu-id="79af5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="79af5-121"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="79af5-121"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="79af5-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="79af5-122">Library</span></span><br/> | <dl> <span data-ttu-id="79af5-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79af5-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="79af5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79af5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79af5-125">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="79af5-125">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
