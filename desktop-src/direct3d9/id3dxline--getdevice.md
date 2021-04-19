---
description: Ruft das Direct3D-Gerät ab, das dem-Zeilen Objekt zugeordnet ist.
ms.assetid: 42459668-aa18-478d-82d9-b8b25dc4a898
title: 'ID3DXLine:: getdevice-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a97edf37d14edce4982d62d76f9429091ad491ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367503"
---
# <a name="id3dxlinegetdevice-method"></a><span data-ttu-id="b280e-103">ID3DXLine:: getdevice-Methode</span><span class="sxs-lookup"><span data-stu-id="b280e-103">ID3DXLine::GetDevice method</span></span>

<span data-ttu-id="b280e-104">Ruft das Direct3D-Gerät ab, das dem-Zeilen Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b280e-104">Retrieves the Direct3D device associated with the line object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b280e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b280e-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="b280e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b280e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b280e-107">*ppdevice* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b280e-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b280e-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="b280e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="b280e-109">Adresse eines Zeigers auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Direct3D-Geräte Objekt darstellt, das dem-Zeilen Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b280e-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the line object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b280e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b280e-110">Return value</span></span>

<span data-ttu-id="b280e-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b280e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b280e-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b280e-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b280e-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="b280e-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="b280e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b280e-114">Requirements</span></span>



| <span data-ttu-id="b280e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b280e-115">Requirement</span></span> | <span data-ttu-id="b280e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b280e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b280e-117">Header</span><span class="sxs-lookup"><span data-stu-id="b280e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b280e-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b280e-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="b280e-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b280e-119">Library</span></span><br/> | <dl> <span data-ttu-id="b280e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b280e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b280e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b280e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b280e-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="b280e-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
