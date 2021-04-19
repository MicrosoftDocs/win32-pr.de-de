---
description: Erstellen Sie ein Lade Modul für asynchrone Speicher.
ms.assetid: 92177390-cb09-445e-9828-806a23ef91b5
title: D3DX10CreateAsyncMemoryLoader-Funktion (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncMemoryLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 0219026eabfcff6dfcec0df4721716302f09f5e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353374"
---
# <a name="d3dx10createasyncmemoryloader-function"></a><span data-ttu-id="b1f72-103">D3DX10CreateAsyncMemoryLoader-Funktion</span><span class="sxs-lookup"><span data-stu-id="b1f72-103">D3DX10CreateAsyncMemoryLoader function</span></span>

<span data-ttu-id="b1f72-104">Erstellen Sie ein Lade Modul für asynchrone Speicher.</span><span class="sxs-lookup"><span data-stu-id="b1f72-104">Create an asynchronous-memory loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1f72-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1f72-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="b1f72-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1f72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1f72-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1f72-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1f72-108">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1f72-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1f72-109">Zeiger auf die Daten.</span><span class="sxs-lookup"><span data-stu-id="b1f72-109">Pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="b1f72-110">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1f72-110">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1f72-111">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1f72-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1f72-112">Größe der Daten.</span><span class="sxs-lookup"><span data-stu-id="b1f72-112">Size of the data.</span></span>

</dd> <dt>

<span data-ttu-id="b1f72-113">*ppdataloader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b1f72-113">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1f72-114">Typ: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b1f72-114">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="b1f72-115">Die Adresse eines Zeigers auf den asynchronen Datenprozessor (siehe [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="b1f72-115">The address of a pointer to the asynchronous-data processor (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1f72-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1f72-116">Return value</span></span>

<span data-ttu-id="b1f72-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1f72-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1f72-118">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="b1f72-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1f72-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1f72-119">Requirements</span></span>



| <span data-ttu-id="b1f72-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1f72-120">Requirement</span></span> | <span data-ttu-id="b1f72-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b1f72-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1f72-122">Header</span><span class="sxs-lookup"><span data-stu-id="b1f72-122">Header</span></span><br/> | <dl> <span data-ttu-id="b1f72-123"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1f72-123"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1f72-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1f72-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1f72-125">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="b1f72-125">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
