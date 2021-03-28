---
title: D3DX11CreateEffectFromMemory-Funktion (D3dx11effect. h)
description: Erstellt einen Effekt aus einem binären Effekt oder einer Datei.
ms.assetid: 4aa65efb-4c6b-4faf-b48f-01329bdff6cd
keywords:
- D3DX11CreateEffectFromMemory-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateEffectFromMemory
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467d2094a7124b96a08c7bab6d7a4209deee9996
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996010"
---
# <a name="d3dx11createeffectfrommemory-function"></a><span data-ttu-id="99b57-104">D3DX11CreateEffectFromMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="99b57-104">D3DX11CreateEffectFromMemory function</span></span>

<span data-ttu-id="99b57-105">Erstellt einen Effekt aus einem binären Effekt oder einer Datei.</span><span class="sxs-lookup"><span data-stu-id="99b57-105">Creates an effect from a binary effect or file.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b57-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="99b57-106">Syntax</span></span>


```C++
HRESULT D3DX11CreateEffectFromMemory(
   void          *pData,
   SIZE_T        DataLength,
   UINT          FXFlags,
   ID3D11Device  *pDevice,
   ID3DX11Effect **ppEffect
);
```



## <a name="parameters"></a><span data-ttu-id="99b57-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="99b57-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b57-108">*pData*</span><span class="sxs-lookup"><span data-stu-id="99b57-108">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="99b57-109">Typ: **void \***</span><span class="sxs-lookup"><span data-stu-id="99b57-109">Type: **void\***</span></span>

<span data-ttu-id="99b57-110">BLOB der kompilierten Effekt Daten.</span><span class="sxs-lookup"><span data-stu-id="99b57-110">Blob of compiled effect data.</span></span>

</dd> <dt>

<span data-ttu-id="99b57-111">*DATALENGTH*</span><span class="sxs-lookup"><span data-stu-id="99b57-111">*DataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="99b57-112">Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="99b57-112">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="99b57-113">Länge des Daten-BLOBs.</span><span class="sxs-lookup"><span data-stu-id="99b57-113">Length of the data blob.</span></span>

</dd> <dt>

<span data-ttu-id="99b57-114">*Fxflags*</span><span class="sxs-lookup"><span data-stu-id="99b57-114">*FXFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="99b57-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="99b57-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="99b57-116">Es sind keine Auswirkungs Flags vorhanden.</span><span class="sxs-lookup"><span data-stu-id="99b57-116">No effect flags exist.</span></span> <span data-ttu-id="99b57-117">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="99b57-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="99b57-118">*pdevice*</span><span class="sxs-lookup"><span data-stu-id="99b57-118">*pDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="99b57-119">Typ: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="99b57-119">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="99b57-120">Zeiger auf den [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) , auf dem die Effekt Ressourcen erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="99b57-120">Pointer to the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) on which to create Effect resources.</span></span>

</dd> <dt>

<span data-ttu-id="99b57-121">*ppeer-ect*</span><span class="sxs-lookup"><span data-stu-id="99b57-121">*ppEffect*</span></span> 
</dt> <dd>

<span data-ttu-id="99b57-122">Typ: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="99b57-122">Type: **[**ID3DX11Effect**](id3dx11effect.md)\*\***</span></span>

<span data-ttu-id="99b57-123">Adresse der neu erstellten [**ID3DX11Effect**](id3dx11effect.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="99b57-123">Address of the newly created [**ID3DX11Effect**](id3dx11effect.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99b57-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99b57-124">Return value</span></span>

<span data-ttu-id="99b57-125">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99b57-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99b57-126">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="99b57-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="99b57-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99b57-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="99b57-128">Sie müssen die [Effekte 11-Quelle](https://github.com/Microsoft/FX11) verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="99b57-128">You must use [Effects 11 source](https://github.com/Microsoft/FX11) to build your effects-type application.</span></span> <span data-ttu-id="99b57-129">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="99b57-129">For more info about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="99b57-130">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="99b57-130">Requirements</span></span>



| <span data-ttu-id="99b57-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99b57-131">Requirement</span></span> | <span data-ttu-id="99b57-132">Wert</span><span class="sxs-lookup"><span data-stu-id="99b57-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="99b57-133">Header</span><span class="sxs-lookup"><span data-stu-id="99b57-133">Header</span></span><br/> | <dl> <span data-ttu-id="99b57-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="99b57-134"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99b57-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="99b57-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b57-136">Effekte 11-Funktionen</span><span class="sxs-lookup"><span data-stu-id="99b57-136">Effects 11 Functions</span></span>](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

