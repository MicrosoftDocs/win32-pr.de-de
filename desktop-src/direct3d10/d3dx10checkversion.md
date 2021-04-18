---
description: Vergewissern Sie sich, dass die Version von D3DX, die Sie mit kompiliert haben, die Version ist, die Sie ausführen.
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: D3DX10CheckVersion-Funktion (D3DX10Core. h)
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
ms.openlocfilehash: 3b41996f16cb97d91dc59f8d368f13b905992388
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371939"
---
# <a name="d3dx10checkversion-function"></a><span data-ttu-id="b7bfc-103">D3DX10CheckVersion-Funktion</span><span class="sxs-lookup"><span data-stu-id="b7bfc-103">D3DX10CheckVersion function</span></span>

<span data-ttu-id="b7bfc-104">Vergewissern Sie sich, dass die Version von D3DX, die Sie mit kompiliert haben, die Version ist, die Sie ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7bfc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7bfc-105">Syntax</span></span>


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a><span data-ttu-id="b7bfc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7bfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7bfc-107">*D3DSdkVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7bfc-107">*D3DSdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7bfc-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7bfc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7bfc-109">Verwenden Sie die d3d10 \_ SDK- \_ Version.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-109">Use D3D10\_SDK\_VERSION.</span></span> <span data-ttu-id="b7bfc-110">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b7bfc-111">*D3DX10SdkVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7bfc-111">*D3DX10SdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7bfc-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7bfc-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7bfc-113">Verwenden Sie die d3dx10 \_ SDK- \_ Version.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-113">Use D3DX10\_SDK\_VERSION.</span></span> <span data-ttu-id="b7bfc-114">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7bfc-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7bfc-115">Return value</span></span>

<span data-ttu-id="b7bfc-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7bfc-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7bfc-117">Wenn die Version nicht übereinstimmt, gibt die Funktion false zurück (eine Zahl kleiner oder gleich 0, die Zahl selbst hat keine Bedeutung).</span><span class="sxs-lookup"><span data-stu-id="b7bfc-117">If the version doesn't match, the function will return FALSE (a number less than or equal to 0, the number itself has no meaning).</span></span>

## <a name="remarks"></a><span data-ttu-id="b7bfc-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7bfc-118">Remarks</span></span>

<span data-ttu-id="b7bfc-119">Verwenden Sie diese Funktion während der Initialisierung Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-119">Use this function during the initialization of your application.</span></span>


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a><span data-ttu-id="b7bfc-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7bfc-120">Requirements</span></span>



| <span data-ttu-id="b7bfc-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7bfc-121">Requirement</span></span> | <span data-ttu-id="b7bfc-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b7bfc-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7bfc-123">Header</span><span class="sxs-lookup"><span data-stu-id="b7bfc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b7bfc-124"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7bfc-124"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="b7bfc-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b7bfc-125">Library</span></span><br/> | <dl> <span data-ttu-id="b7bfc-126"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7bfc-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b7bfc-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7bfc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7bfc-128">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="b7bfc-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
