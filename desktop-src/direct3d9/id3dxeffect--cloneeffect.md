---
description: Erstellt eine Kopie eines Effekts.
ms.assetid: 6272bce0-b712-4a61-afe2-8f572993b03e
title: 'ID3DXEffect:: cloneeffect-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CloneEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: eba2f6248bd1373ebf0aae55cf94103e2c269be7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373519"
---
# <a name="id3dxeffectcloneeffect-method"></a><span data-ttu-id="83c74-103">ID3DXEffect:: cloneeffect-Methode</span><span class="sxs-lookup"><span data-stu-id="83c74-103">ID3DXEffect::CloneEffect method</span></span>

<span data-ttu-id="83c74-104">Erstellt eine Kopie eines Effekts.</span><span class="sxs-lookup"><span data-stu-id="83c74-104">Creates a copy of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="83c74-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="83c74-105">Syntax</span></span>


```C++
HRESULT CloneEffect(
  [in]  LPDIRECT3DDEVICE9 pDevice,
  [out] LPD3DXEFFECT      *ppEffect
);
```



## <a name="parameters"></a><span data-ttu-id="83c74-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="83c74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83c74-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83c74-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83c74-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="83c74-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="83c74-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das dem Effekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="83c74-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the effect.</span></span>

</dd> <dt>

<span data-ttu-id="83c74-110">*ppeer-ect* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="83c74-110">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83c74-111">Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="83c74-111">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="83c74-112">Zeiger auf eine [**ID3DXEffect**](id3dxeffect.md) -Schnittstelle, die den geklonten Effekt enthält.</span><span class="sxs-lookup"><span data-stu-id="83c74-112">Pointer to an [**ID3DXEffect**](id3dxeffect.md) interface, containing the cloned effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83c74-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83c74-113">Return value</span></span>

<span data-ttu-id="83c74-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83c74-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83c74-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="83c74-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="83c74-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="83c74-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="83c74-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83c74-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="83c74-118">Diese Funktion Klonen Sie keinen Effekt, wenn der Benutzer während der Erstellung des Effekts [D3DXFX \_ Not \_ cloneable](d3dxfx.md) angibt.</span><span class="sxs-lookup"><span data-stu-id="83c74-118">This function will not clone an effect if the user specifies [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md) during effect creation.</span></span>

 

<span data-ttu-id="83c74-119">Informationen zum Aktualisieren von freigegebenen und nicht freigegebenen Parametern in einer aktiven Technik eines geklonten Effekts finden Sie unter [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md).</span><span class="sxs-lookup"><span data-stu-id="83c74-119">To update shared and non-shared parameters in an active technique of a cloned effect, see [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83c74-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83c74-120">Requirements</span></span>



| <span data-ttu-id="83c74-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83c74-121">Requirement</span></span> | <span data-ttu-id="83c74-122">Wert</span><span class="sxs-lookup"><span data-stu-id="83c74-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="83c74-123">Header</span><span class="sxs-lookup"><span data-stu-id="83c74-123">Header</span></span><br/>  | <dl> <span data-ttu-id="83c74-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="83c74-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="83c74-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="83c74-125">Library</span></span><br/> | <dl> <span data-ttu-id="83c74-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83c74-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="83c74-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83c74-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83c74-128">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="83c74-128">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
