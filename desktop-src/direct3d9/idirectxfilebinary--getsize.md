---
description: Ruft die Größe der Binärdaten ab. Veraltet.
ms.assetid: 99a74043-ce87-4545-961f-dade54e77735
title: 'Idirectxfilebinary:: GetSize-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetSize
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 664e2bf026df6d9e4b5bc07067ce1ce7fe7669db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531004"
---
# <a name="idirectxfilebinarygetsize-method"></a><span data-ttu-id="52d4d-104">Idirectxfilebinary:: GetSize-Methode</span><span class="sxs-lookup"><span data-stu-id="52d4d-104">IDirectXFileBinary::GetSize method</span></span>

<span data-ttu-id="52d4d-105">Ruft die Größe der Binärdaten ab.</span><span class="sxs-lookup"><span data-stu-id="52d4d-105">Retrieves the size of the binary data.</span></span> <span data-ttu-id="52d4d-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="52d4d-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="52d4d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="52d4d-107">Syntax</span></span>


```C++
HRESULT GetSize(
  [out] DWORD *pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="52d4d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="52d4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52d4d-109">*pcbSize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="52d4d-109">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52d4d-110">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="52d4d-110">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="52d4d-111">Ein Zeiger auf die zurückgegebene Größe der Binärdaten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="52d4d-111">Pointer to the returned size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52d4d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52d4d-112">Return value</span></span>

<span data-ttu-id="52d4d-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52d4d-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52d4d-114">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="52d4d-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="52d4d-115">Wenn die Methode fehlschlägt, kann der Rückgabewert dxfileerr \_ badvalue lauten.</span><span class="sxs-lookup"><span data-stu-id="52d4d-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="52d4d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52d4d-116">Requirements</span></span>



| <span data-ttu-id="52d4d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52d4d-117">Requirement</span></span> | <span data-ttu-id="52d4d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="52d4d-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52d4d-119">Header</span><span class="sxs-lookup"><span data-stu-id="52d4d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="52d4d-120"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="52d4d-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="52d4d-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="52d4d-121">Library</span></span><br/> | <dl> <span data-ttu-id="52d4d-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52d4d-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52d4d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52d4d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d4d-124">Idirectxfilebinary</span><span class="sxs-lookup"><span data-stu-id="52d4d-124">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
