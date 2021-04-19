---
description: Rufen Sie das Direct3D-Gerät ab, das dem Schriftart Objekt zugeordnet ist.
ms.assetid: aad2406e-9461-4a84-9875-74b53d68ef40
title: 'ID3DX10Font:: getdevice-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72719e07c62b681579162fda56000d2d6238bd52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373517"
---
# <a name="id3dx10fontgetdevice-method"></a><span data-ttu-id="3d5a8-103">ID3DX10Font:: getdevice-Methode</span><span class="sxs-lookup"><span data-stu-id="3d5a8-103">ID3DX10Font::GetDevice method</span></span>

<span data-ttu-id="3d5a8-104">Rufen Sie das Direct3D-Gerät ab, das dem Schriftart Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3d5a8-104">Retrieve the Direct3D device associated with the font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d5a8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d5a8-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="3d5a8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d5a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d5a8-107">*ppdevice* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3d5a8-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d5a8-108">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="3d5a8-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="3d5a8-109">Adresse eines Zeigers auf eine ID3D10Device-Schnittstelle, die das Direct3D-Geräte Objekt darstellt, das dem Schriftart Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3d5a8-109">Address of a pointer to an ID3D10Device interface, representing the Direct3D device object associated with the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d5a8-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d5a8-110">Return value</span></span>

<span data-ttu-id="3d5a8-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3d5a8-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3d5a8-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3d5a8-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3d5a8-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="3d5a8-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d5a8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d5a8-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3d5a8-115">Durch Aufrufen dieser Methode wird der interne Verweis Zähler in der ID3D10Device-Schnittstelle vergrößert.</span><span class="sxs-lookup"><span data-stu-id="3d5a8-115">Calling this method will increase the internal reference count on the ID3D10Device interface.</span></span> <span data-ttu-id="3d5a8-116">Stellen Sie sicher, dass IUnknown aufgerufen wird, wenn Sie die ID3D10Device-Schnittstelle verwenden, oder wenn Sie einen Speicherplatz haben.</span><span class="sxs-lookup"><span data-stu-id="3d5a8-116">Be sure to call IUnknown when you are done using this ID3D10Device interface or you will have a memory leak.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3d5a8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d5a8-117">Requirements</span></span>



| <span data-ttu-id="3d5a8-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d5a8-118">Requirement</span></span> | <span data-ttu-id="3d5a8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3d5a8-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5a8-120">Header</span><span class="sxs-lookup"><span data-stu-id="3d5a8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3d5a8-121"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d5a8-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3d5a8-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3d5a8-122">Library</span></span><br/> | <dl> <span data-ttu-id="3d5a8-123"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d5a8-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d5a8-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d5a8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d5a8-125">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="3d5a8-125">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="3d5a8-126">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="3d5a8-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




