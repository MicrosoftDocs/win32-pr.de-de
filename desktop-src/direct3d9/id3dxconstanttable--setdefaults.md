---
description: Legt die Konstanten auf ihre Standardwerte fest. Die Standardwerte werden in den Variablen Deklarationen im Shader deklariert.
ms.assetid: 593a3a1b-cf96-4d46-9917-21068def0988
title: 'ID3DXConstantTable:: SetDefaults-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetDefaults
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed49e626c979f7146b42078cf1f65fdd6716efc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762072"
---
# <a name="id3dxconstanttablesetdefaults-method"></a><span data-ttu-id="3cd17-104">ID3DXConstantTable:: SetDefaults-Methode</span><span class="sxs-lookup"><span data-stu-id="3cd17-104">ID3DXConstantTable::SetDefaults method</span></span>

<span data-ttu-id="3cd17-105">Legt die Konstanten auf ihre Standardwerte fest.</span><span class="sxs-lookup"><span data-stu-id="3cd17-105">Sets the constants to their default values.</span></span> <span data-ttu-id="3cd17-106">Die Standardwerte werden in den Variablen Deklarationen im Shader deklariert.</span><span class="sxs-lookup"><span data-stu-id="3cd17-106">The default values are declared in the variable declarations in the shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cd17-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cd17-107">Syntax</span></span>


```C++
HRESULT SetDefaults(
  [in] LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="3cd17-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cd17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cd17-109">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3cd17-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cd17-110">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="3cd17-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="3cd17-111">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3cd17-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cd17-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3cd17-112">Return value</span></span>

<span data-ttu-id="3cd17-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3cd17-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3cd17-114">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3cd17-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3cd17-115">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="3cd17-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cd17-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cd17-116">Requirements</span></span>



| <span data-ttu-id="3cd17-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3cd17-117">Requirement</span></span> | <span data-ttu-id="3cd17-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3cd17-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cd17-119">Header</span><span class="sxs-lookup"><span data-stu-id="3cd17-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3cd17-120"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cd17-120"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3cd17-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3cd17-121">Library</span></span><br/> | <dl> <span data-ttu-id="3cd17-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3cd17-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3cd17-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cd17-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cd17-124">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="3cd17-124">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
