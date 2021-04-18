---
description: Rufen Sie Schriftart Eigenschaften ab.
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: 'ID3DX10Font:: GetTextMetrics-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetTextMetrics
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72decdcf0a9573f7ad8ba0f4e363df6df3599477
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530938"
---
# <a name="id3dx10fontgettextmetrics-method"></a><span data-ttu-id="11580-103">ID3DX10Font:: GetTextMetrics-Methode</span><span class="sxs-lookup"><span data-stu-id="11580-103">ID3DX10Font::GetTextMetrics method</span></span>

<span data-ttu-id="11580-104">Rufen Sie Schriftart Eigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="11580-104">Retrieve font characteristics.</span></span>

## <a name="syntax"></a><span data-ttu-id="11580-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="11580-105">Syntax</span></span>


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="11580-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11580-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11580-107">*ptextmetrics* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11580-107">*pTextMetrics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11580-108">Typ: **TextMetric \***</span><span class="sxs-lookup"><span data-stu-id="11580-108">Type: **TEXTMETRIC\***</span></span>

<span data-ttu-id="11580-109">Zeiger auf eine [textmetrikstruktur](/previous-versions//ms534202(v=vs.85)) , die Schriftart Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="11580-109">Pointer to a [TEXTMETRIC](/previous-versions//ms534202(v=vs.85)) structure, which contains font properties.</span></span> <span data-ttu-id="11580-110">Wenn Unicode definiert ist, gibt die Funktion eine textmetricw-Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="11580-110">If Unicode is defined, the function returns a TEXTMETRICW structure.</span></span> <span data-ttu-id="11580-111">Andernfalls gibt die Funktion eine textmetrica-Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="11580-111">Otherwise, the function returns a TEXTMETRICA structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11580-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11580-112">Return value</span></span>

<span data-ttu-id="11580-113">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11580-113">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11580-114">Ist ungleich null (0), wenn die Funktion erfolgreich ausgeführt wird, andernfalls null (0).</span><span class="sxs-lookup"><span data-stu-id="11580-114">Nonzero if the function is successful; otherwise 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="11580-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11580-115">Requirements</span></span>



| <span data-ttu-id="11580-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11580-116">Requirement</span></span> | <span data-ttu-id="11580-117">Wert</span><span class="sxs-lookup"><span data-stu-id="11580-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11580-118">Header</span><span class="sxs-lookup"><span data-stu-id="11580-118">Header</span></span><br/>  | <dl> <span data-ttu-id="11580-119"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="11580-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="11580-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11580-120">Library</span></span><br/> | <dl> <span data-ttu-id="11580-121"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11580-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11580-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11580-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11580-123">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="11580-123">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="11580-124">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="11580-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
