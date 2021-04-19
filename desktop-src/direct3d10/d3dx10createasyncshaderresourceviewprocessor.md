---
description: Erstellen Sie einen Datenprozessor, der eine Ressource lädt, und erstellen Sie dann eine Shader-Ressourcen Ansicht dafür. Datenprozessoren sind eine Komponente der Funktion zum asynchronen Laden von Daten in d3dx10, die Thread-Pumpen verwendet.
ms.assetid: 6e5a6138-c218-4200-a24e-d906d34933b8
title: D3DX10CreateAsyncShaderResourceViewProcessor-Funktion (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderResourceViewProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: bd55e4191382c5abde52ce05d0a16b5533d79eac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353755"
---
# <a name="d3dx10createasyncshaderresourceviewprocessor-function"></a><span data-ttu-id="df71c-104">D3DX10CreateAsyncShaderResourceViewProcessor-Funktion</span><span class="sxs-lookup"><span data-stu-id="df71c-104">D3DX10CreateAsyncShaderResourceViewProcessor function</span></span>

<span data-ttu-id="df71c-105">Erstellen Sie einen Datenprozessor, der eine Ressource lädt, und erstellen Sie dann eine Shader-Ressourcen Ansicht dafür.</span><span class="sxs-lookup"><span data-stu-id="df71c-105">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="df71c-106">Datenprozessoren sind eine Komponente der Funktion zum asynchronen Laden von Daten in d3dx10, die [**Thread-Pumpen**](id3dx10threadpump.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="df71c-106">Data processors are a component of the asynchronous data loading feature in D3DX10 that uses [**thread pumps**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="df71c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="df71c-107">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="df71c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="df71c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df71c-109">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df71c-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df71c-110">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="df71c-110">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="df71c-111">Zeiger auf das Direct3D-Gerät (siehe [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), das verwendet wird, um eine Ressource und eine Shader-Ressourcen Ansicht für diese Ressource zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="df71c-111">Pointer to the Direct3D device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will be used to create a resource and a shader-resource view for that resource.</span></span>

</dd> <dt>

<span data-ttu-id="df71c-112">*ploadinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df71c-112">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df71c-113">Type: **[ **d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="df71c-113">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="df71c-114">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="df71c-114">Optional.</span></span> <span data-ttu-id="df71c-115">Gibt die Merkmale einer Textur an (siehe [**d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)), wenn der Datenprozessor erstellt wird. Legen Sie diese Einstellung auf **null** fest, um die Merkmale einer Textur beim Laden der Textur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="df71c-115">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="df71c-116">*ppdataprocessor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="df71c-116">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df71c-117">Typ: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="df71c-117">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="df71c-118">Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX10DataProcessor-Schnittstelle**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="df71c-118">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df71c-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df71c-119">Return value</span></span>

<span data-ttu-id="df71c-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df71c-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df71c-121">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="df71c-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df71c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df71c-122">Requirements</span></span>



| <span data-ttu-id="df71c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df71c-123">Requirement</span></span> | <span data-ttu-id="df71c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="df71c-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="df71c-125">Header</span><span class="sxs-lookup"><span data-stu-id="df71c-125">Header</span></span><br/> | <dl> <span data-ttu-id="df71c-126"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="df71c-126"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df71c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df71c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df71c-128">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="df71c-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




