---
description: Erstellen Sie ein Geräte Objekt.
ms.assetid: 5b9b00de-c744-43c7-b383-1d3358c80741
title: 'ID3DX10DataProcessor:: kreatedeviceobject-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.CreateDeviceObject
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1ed362f992ca2b9d3ce6e561e08e5fe7fd0bdbe3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219537"
---
# <a name="id3dx10dataprocessorcreatedeviceobject-method"></a><span data-ttu-id="f41d5-103">ID3DX10DataProcessor:: kreatedeviceobject-Methode</span><span class="sxs-lookup"><span data-stu-id="f41d5-103">ID3DX10DataProcessor::CreateDeviceObject method</span></span>

<span data-ttu-id="f41d5-104">Erstellen Sie ein Geräte Objekt.</span><span class="sxs-lookup"><span data-stu-id="f41d5-104">Create a device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f41d5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f41d5-105">Syntax</span></span>


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a><span data-ttu-id="f41d5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f41d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f41d5-107">*ppdataobject* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f41d5-107">*ppDataObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f41d5-108">Typ: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="f41d5-108">Type: **void\*\***</span></span>

<span data-ttu-id="f41d5-109">Adresse eines Zeigers auf das erstellte Geräte Objekt.</span><span class="sxs-lookup"><span data-stu-id="f41d5-109">Address of a pointer to the created device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f41d5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f41d5-110">Return value</span></span>

<span data-ttu-id="f41d5-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f41d5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f41d5-112">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="f41d5-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f41d5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f41d5-113">Requirements</span></span>



| <span data-ttu-id="f41d5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f41d5-114">Requirement</span></span> | <span data-ttu-id="f41d5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f41d5-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f41d5-116">Header</span><span class="sxs-lookup"><span data-stu-id="f41d5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f41d5-117"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f41d5-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f41d5-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f41d5-118">Library</span></span><br/> | <dl> <span data-ttu-id="f41d5-119"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f41d5-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f41d5-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f41d5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f41d5-121">ID3DX10DataProcessor</span><span class="sxs-lookup"><span data-stu-id="f41d5-121">ID3DX10DataProcessor</span></span>](id3dx10dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="f41d5-122">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f41d5-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




