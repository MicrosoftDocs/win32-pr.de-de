---
description: Erstellen Sie ein asynchrones Datei Lade Modul.
ms.assetid: 1b79fba5-e7f0-4160-9cec-ffea94f84fde
title: D3DX10CreateAsyncFileLoader-Funktion (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncFileLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e98bccf709fa4a6d921e266148b94fd8623429ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355169"
---
# <a name="d3dx10createasyncfileloader-function"></a><span data-ttu-id="14783-103">D3DX10CreateAsyncFileLoader-Funktion</span><span class="sxs-lookup"><span data-stu-id="14783-103">D3DX10CreateAsyncFileLoader function</span></span>

<span data-ttu-id="14783-104">Erstellen Sie ein asynchrones Datei Lade Modul.</span><span class="sxs-lookup"><span data-stu-id="14783-104">Create an asynchronous-file loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="14783-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14783-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="14783-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14783-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14783-107">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14783-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14783-108">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14783-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14783-109">Der Name der zu ladenden Datei.</span><span class="sxs-lookup"><span data-stu-id="14783-109">The name of the file to load.</span></span> <span data-ttu-id="14783-110">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="14783-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="14783-111">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="14783-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="14783-112">*ppdataloader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="14783-112">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14783-113">Typ: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="14783-113">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="14783-114">Adresse eines Zeigers auf den asynchronen Daten Lader (siehe [**ID3DX10DataLoader Interface**](id3dx10dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="14783-114">Address of a pointer to the asynchronous-data loader (see [**ID3DX10DataLoader Interface**](id3dx10dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14783-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14783-115">Return value</span></span>

<span data-ttu-id="14783-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="14783-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="14783-117">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="14783-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14783-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14783-118">Requirements</span></span>



| <span data-ttu-id="14783-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14783-119">Requirement</span></span> | <span data-ttu-id="14783-120">Wert</span><span class="sxs-lookup"><span data-stu-id="14783-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="14783-121">Header</span><span class="sxs-lookup"><span data-stu-id="14783-121">Header</span></span><br/> | <dl> <span data-ttu-id="14783-122"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="14783-122"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14783-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14783-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14783-124">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="14783-124">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
