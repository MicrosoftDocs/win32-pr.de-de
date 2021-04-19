---
title: ColorType-Enumeration (Software-BDC. h)
description: Elemente der ColorType-Enumeration werden verwendet, um Typen von Farben anzugeben, die für eine weiche Tastatur verfügbar sind.
ms.assetid: 63a51f67-d85c-4017-a569-03df164198db
keywords:
- Color Type-Enumeration Text Services-Framework
topic_type:
- apiref
api_name:
- COLORTYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28f3b4111973e9676a34c548db566b1c95ac43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342860"
---
# <a name="colortype-enumeration"></a><span data-ttu-id="ea44e-104">ColorType-Enumeration</span><span class="sxs-lookup"><span data-stu-id="ea44e-104">COLORTYPE enumeration</span></span>

<span data-ttu-id="ea44e-105">Elemente der **ColorType** -Enumeration werden verwendet, um Typen von Farben anzugeben, die für eine weiche Tastatur verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ea44e-105">Elements of the **COLORTYPE** enumeration are used to specify types of colors that are available for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea44e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea44e-106">Syntax</span></span>


```C++
typedef enum tagCOLORTYPE { 
  bkcolor         = 0,
  UnSelForeColor  = 1,
  UnSelTextColor  = 2,
  SelForeColor    = 3,
  SelTextColor    = 4,
  Max_color_Type  = 5
} COLORTYPE;
```



## <a name="constants"></a><span data-ttu-id="ea44e-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ea44e-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ea44e-108"><span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**</span><span class="sxs-lookup"><span data-stu-id="ea44e-108"><span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**</span></span>
</dt> <dd>

<span data-ttu-id="ea44e-109">Hintergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="ea44e-109">Background color.</span></span>

</dd> <dt>

<span data-ttu-id="ea44e-110"><span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**Unselforecolor**</span><span class="sxs-lookup"><span data-stu-id="ea44e-110"><span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**UnSelForeColor**</span></span>
</dt> <dd>

<span data-ttu-id="ea44e-111">Nicht ausgewählte Vordergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="ea44e-111">Unselected foreground color.</span></span>

</dd> <dt>

<span data-ttu-id="ea44e-112"><span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**Unseltextcolor**</span><span class="sxs-lookup"><span data-stu-id="ea44e-112"><span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**UnSelTextColor**</span></span>
</dt> <dd>

<span data-ttu-id="ea44e-113">Nicht ausgewählte Textfarbe.</span><span class="sxs-lookup"><span data-stu-id="ea44e-113">Unselected text color.</span></span>

</dd> <dt>

<span data-ttu-id="ea44e-114"><span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**Selforecolor**</span><span class="sxs-lookup"><span data-stu-id="ea44e-114"><span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**SelForeColor**</span></span>
</dt> <dd>

<span data-ttu-id="ea44e-115">Ausgewählte Vordergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="ea44e-115">Selected foreground color.</span></span>

</dd> <dt>

<span data-ttu-id="ea44e-116"><span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**Seltextcolor**</span><span class="sxs-lookup"><span data-stu-id="ea44e-116"><span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**SelTextColor**</span></span>
</dt> <dd>

<span data-ttu-id="ea44e-117">Ausgewählte Textfarbe.</span><span class="sxs-lookup"><span data-stu-id="ea44e-117">Selected text color.</span></span>

</dd> <dt>

<span data-ttu-id="ea44e-118"><span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**Max \_ - \_ Farbtyp**</span><span class="sxs-lookup"><span data-stu-id="ea44e-118"><span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**Max\_color\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="ea44e-119">Der maximale Farbtyp.</span><span class="sxs-lookup"><span data-stu-id="ea44e-119">Maximum color type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea44e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea44e-120">Requirements</span></span>



| <span data-ttu-id="ea44e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea44e-121">Requirement</span></span> | <span data-ttu-id="ea44e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ea44e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea44e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea44e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ea44e-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea44e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ea44e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea44e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ea44e-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea44e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ea44e-127">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ea44e-127">Redistributable</span></span><br/>          | <span data-ttu-id="ea44e-128">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ea44e-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="ea44e-129">Header</span><span class="sxs-lookup"><span data-stu-id="ea44e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea44e-130"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea44e-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="ea44e-131">IDL</span><span class="sxs-lookup"><span data-stu-id="ea44e-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ea44e-132"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ea44e-132"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





