---
description: Rufen Sie das Gerät ab, das dem Sprite-Objekt zugeordnet ist.
ms.assetid: 9119b232-22c8-4b05-b584-ce176370ca97
title: 'ID3DX10Sprite:: getdevice-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d4e7a3c6ebfcbcb83aaaed6273ea321b33a44ce1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356116"
---
# <a name="id3dx10spritegetdevice-method"></a><span data-ttu-id="bc1a1-103">ID3DX10Sprite:: getdevice-Methode</span><span class="sxs-lookup"><span data-stu-id="bc1a1-103">ID3DX10Sprite::GetDevice method</span></span>

<span data-ttu-id="bc1a1-104">Rufen Sie das Gerät ab, das dem Sprite-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bc1a1-104">Retrieve the device associated with the sprite object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc1a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc1a1-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="bc1a1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc1a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc1a1-107">*ppdevice* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bc1a1-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc1a1-108">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="bc1a1-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="bc1a1-109">Adresse eines Zeigers auf eine ID3D10Device-Schnittstelle, die das Direct3D-Geräte Objekt darstellt, das dem Sprite-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bc1a1-109">Address of a pointer to an ID3D10Device interface, representing the Direct3D device object associated with the sprite object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc1a1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc1a1-110">Return value</span></span>

<span data-ttu-id="bc1a1-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bc1a1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bc1a1-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bc1a1-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bc1a1-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="bc1a1-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc1a1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc1a1-114">Remarks</span></span>

<span data-ttu-id="bc1a1-115">Durch Aufrufen dieser Methode wird der interne Verweis Zähler in der ID3D10Device-Schnittstelle vergrößert.</span><span class="sxs-lookup"><span data-stu-id="bc1a1-115">Calling this method will increase the internal reference count on the ID3D10Device interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc1a1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc1a1-116">Requirements</span></span>



| <span data-ttu-id="bc1a1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc1a1-117">Requirement</span></span> | <span data-ttu-id="bc1a1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="bc1a1-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc1a1-119">Header</span><span class="sxs-lookup"><span data-stu-id="bc1a1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bc1a1-120"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc1a1-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc1a1-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bc1a1-121">Library</span></span><br/> | <dl> <span data-ttu-id="bc1a1-122"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc1a1-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc1a1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc1a1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc1a1-124">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="bc1a1-124">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="bc1a1-125">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="bc1a1-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




