---
description: Ruft Schriftart Eigenschaften ab, die in einer TextMetric-Struktur identifiziert werden. Diese Methode unterstützt die ANSI-und Unicode-Compilereinstellungen.
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: 'ID3DXFont:: GetTextMetrics-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetTextMetrics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ce6064804d2aac2846cbea6971f145fc07759f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354766"
---
# <a name="id3dxfontgettextmetrics-method"></a><span data-ttu-id="d9f23-104">ID3DXFont:: GetTextMetrics-Methode</span><span class="sxs-lookup"><span data-stu-id="d9f23-104">ID3DXFont::GetTextMetrics method</span></span>

<span data-ttu-id="d9f23-105">Ruft Schriftart Eigenschaften ab, die in einer [**TextMetric**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) -Struktur identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="d9f23-105">Retrieves font characteristics that are identified in a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.</span></span> <span data-ttu-id="d9f23-106">Diese Methode unterstützt die ANSI-und Unicode-Compilereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="d9f23-106">This method supports ANSI and Unicode compiler settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9f23-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9f23-107">Syntax</span></span>


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="d9f23-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9f23-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9f23-109">*ptextmetrics* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d9f23-109">*pTextMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9f23-110">Typ: **[ **TextMetric**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***</span><span class="sxs-lookup"><span data-stu-id="d9f23-110">Type: **[**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***</span></span>

<span data-ttu-id="d9f23-111">Zeiger auf eine [**textmetrikstruktur**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) , die Schriftart Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="d9f23-111">Pointer to a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure, which contains font properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9f23-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9f23-112">Return value</span></span>

<span data-ttu-id="d9f23-113">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9f23-113">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9f23-114">Ist ungleich null (0), wenn die Funktion erfolgreich ausgeführt wird, andernfalls null (0).</span><span class="sxs-lookup"><span data-stu-id="d9f23-114">Nonzero if the function is successful; otherwise 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9f23-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9f23-115">Remarks</span></span>

<span data-ttu-id="d9f23-116">Die Compilereinstellung bestimmt auch den Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="d9f23-116">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="d9f23-117">Wenn Unicode definiert ist, gibt die Funktion eine textmetricw-Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="d9f23-117">If Unicode is defined, the function returns a TEXTMETRICW structure.</span></span> <span data-ttu-id="d9f23-118">Andernfalls gibt der Funktions Aufruhe eine textmetrica-Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="d9f23-118">Otherwise, the function call returns a TEXTMETRICA structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f23-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9f23-119">Requirements</span></span>



| <span data-ttu-id="d9f23-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9f23-120">Requirement</span></span> | <span data-ttu-id="d9f23-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d9f23-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f23-122">Header</span><span class="sxs-lookup"><span data-stu-id="d9f23-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d9f23-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9f23-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d9f23-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d9f23-124">Library</span></span><br/> | <dl> <span data-ttu-id="d9f23-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9f23-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d9f23-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9f23-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f23-127">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="d9f23-127">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
