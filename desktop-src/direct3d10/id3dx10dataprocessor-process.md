---
description: Verarbeiten einiger Daten.
ms.assetid: c64f6a2d-4512-4028-8ed9-bfc5e9e86758
title: ID3DX10DataProcessor::P rocess-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.Process
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2ddad2f6350f48f65bc82e094eccb92b1b8bf390
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219725"
---
# <a name="id3dx10dataprocessorprocess-method"></a><span data-ttu-id="f3ac6-103">ID3DX10DataProcessor::P rocess-Methode</span><span class="sxs-lookup"><span data-stu-id="f3ac6-103">ID3DX10DataProcessor::Process method</span></span>

<span data-ttu-id="f3ac6-104">Verarbeiten einiger Daten.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-104">Process some data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3ac6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3ac6-105">Syntax</span></span>


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="f3ac6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3ac6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3ac6-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3ac6-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3ac6-108">Typ: **void \***</span><span class="sxs-lookup"><span data-stu-id="f3ac6-108">Type: **void\***</span></span>

<span data-ttu-id="f3ac6-109">Zeiger auf die zu verarbeitenden Daten.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-109">Pointer to the data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="f3ac6-110">*cbytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3ac6-110">*cBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3ac6-111">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3ac6-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3ac6-112">Die Größe der zu verarbeitenden Daten.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-112">Size of the data to be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3ac6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3ac6-113">Return value</span></span>

<span data-ttu-id="f3ac6-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f3ac6-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f3ac6-115">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3ac6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3ac6-116">Requirements</span></span>



| <span data-ttu-id="f3ac6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3ac6-117">Requirement</span></span> | <span data-ttu-id="f3ac6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f3ac6-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3ac6-119">Header</span><span class="sxs-lookup"><span data-stu-id="f3ac6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f3ac6-120"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3ac6-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f3ac6-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f3ac6-121">Library</span></span><br/> | <dl> <span data-ttu-id="f3ac6-122"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3ac6-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3ac6-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3ac6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3ac6-124">ID3DX10DataProcessor</span><span class="sxs-lookup"><span data-stu-id="f3ac6-124">ID3DX10DataProcessor</span></span>](id3dx10dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="f3ac6-125">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f3ac6-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
