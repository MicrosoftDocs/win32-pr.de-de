---
description: 'D3DX10CheckVersion-Funktion: Stellen Sie sicher, dass die Version von D3DX, mit der Sie kompiliert haben, die Version ist, die Sie ausführen.'
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: D3DX10CheckVersion-Funktion (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CheckVersion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4fc8befa88fb706965a30224843745b033ea205b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105348"
---
# <a name="d3dx10checkversion-function"></a><span data-ttu-id="83849-103">D3DX10CheckVersion-Funktion</span><span class="sxs-lookup"><span data-stu-id="83849-103">D3DX10CheckVersion function</span></span>

<span data-ttu-id="83849-104">Stellen Sie sicher, dass die Version von D3DX, mit der Sie kompiliert haben, die Version ist, die Sie ausführen.</span><span class="sxs-lookup"><span data-stu-id="83849-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="83849-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="83849-105">Syntax</span></span>


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a><span data-ttu-id="83849-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="83849-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83849-107">*D3DSdkVersion* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="83849-107">*D3DSdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83849-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83849-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83849-109">Verwenden Sie die D3D10 \_ \_ SDK-VERSION.</span><span class="sxs-lookup"><span data-stu-id="83849-109">Use D3D10\_SDK\_VERSION.</span></span> <span data-ttu-id="83849-110">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="83849-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="83849-111">*D3DX10SdkVersion* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="83849-111">*D3DX10SdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83849-112">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83849-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83849-113">Verwenden Sie die D3DX10 \_ \_ SDK-VERSION.</span><span class="sxs-lookup"><span data-stu-id="83849-113">Use D3DX10\_SDK\_VERSION.</span></span> <span data-ttu-id="83849-114">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="83849-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83849-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83849-115">Return value</span></span>

<span data-ttu-id="83849-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83849-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83849-117">Wenn die Version nicht entspricht, gibt die Funktion FALSE zurück (eine Zahl kleiner oder gleich 0, die Zahl selbst hat keine Bedeutung).</span><span class="sxs-lookup"><span data-stu-id="83849-117">If the version doesn't match, the function will return FALSE (a number less than or equal to 0, the number itself has no meaning).</span></span>

## <a name="remarks"></a><span data-ttu-id="83849-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83849-118">Remarks</span></span>

<span data-ttu-id="83849-119">Verwenden Sie diese Funktion während der Initialisierung Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="83849-119">Use this function during the initialization of your application.</span></span>


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a><span data-ttu-id="83849-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83849-120">Requirements</span></span>



| <span data-ttu-id="83849-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83849-121">Requirement</span></span> | <span data-ttu-id="83849-122">Wert</span><span class="sxs-lookup"><span data-stu-id="83849-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83849-123">Header</span><span class="sxs-lookup"><span data-stu-id="83849-123">Header</span></span><br/>  | <dl> <span data-ttu-id="83849-124"><dt>D3DX10Core.h</dt></span><span class="sxs-lookup"><span data-stu-id="83849-124"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="83849-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="83849-125">Library</span></span><br/> | <dl> <span data-ttu-id="83849-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="83849-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="83849-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="83849-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83849-128">Universell Functions</span><span class="sxs-lookup"><span data-stu-id="83849-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
