---
title: glugettessproperty-Funktion (glu. h)
description: Die Funktion "glugettessproperty" Ruft eine Mosaik Objekt Eigenschaft ab.
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- glugettessproperty-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluGetTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482f32b227dbcf0c2a62405e344aa719bb4b9e17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391812"
---
# <a name="glugettessproperty-function"></a><span data-ttu-id="0c049-104">glugettessproperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="0c049-104">gluGetTessProperty function</span></span>

<span data-ttu-id="0c049-105">Die Funktion " **glugettessproperty** " Ruft eine Mosaik Objekt Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="0c049-105">The **gluGetTessProperty** function gets a tessellation object property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c049-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c049-106">Syntax</span></span>


```C++
void WINAPI gluGetTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      *value
);
```



## <a name="parameters"></a><span data-ttu-id="0c049-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c049-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c049-108">*ATI*</span><span class="sxs-lookup"><span data-stu-id="0c049-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="0c049-109">Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="0c049-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0c049-110">*,*</span><span class="sxs-lookup"><span data-stu-id="0c049-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="0c049-111">Die Eigenschaft, deren Wert abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c049-111">The property whose value is to be retrieved.</span></span> <span data-ttu-id="0c049-112">Die folgenden Werte sind gültig: die \_ Regel "glu Tess" \_ , " \_ glu Tess" und " \_ \_ \_ glu- \_ Toleranz" \_ .</span><span class="sxs-lookup"><span data-stu-id="0c049-112">The following values are valid: GLU\_TESS\_WINDING\_RULE, GLU\_TESS\_BOUNDARY\_ONLY, and GLU\_TESS\_TOLERANCE.</span></span>

</dd> <dt>

<span data-ttu-id="0c049-113">*value*</span><span class="sxs-lookup"><span data-stu-id="0c049-113">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="0c049-114">Ein Zeiger auf den Speicherort, an dem der Wert der benannten Eigenschaft geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="0c049-114">A pointer to the location where the value of the named property is written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c049-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c049-115">Return value</span></span>

<span data-ttu-id="0c049-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0c049-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c049-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c049-117">Remarks</span></span>

<span data-ttu-id="0c049-118">Verwenden Sie " **glugettessproperty** ", um Eigenschaften abzurufen, die in einem Mosaik Objekt gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="0c049-118">Use **gluGetTessProperty** to retrieve properties stored in a tessellation object.</span></span> <span data-ttu-id="0c049-119">Diese Eigenschaften beeinflussen die Art und Weise, wie Mosaik Objekte interpretiert und gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="0c049-119">These properties affect the way tessellation objects are interpreted and rendered.</span></span> <span data-ttu-id="0c049-120">Informationen zu den Eigenschaften und deren Funktionsfähigkeit finden Sie unter " [**glutessproperty**](glutessproperty.md)".</span><span class="sxs-lookup"><span data-stu-id="0c049-120">For information about what the properties are and what they do, see [**gluTessProperty**](glutessproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c049-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c049-121">Requirements</span></span>



| <span data-ttu-id="0c049-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c049-122">Requirement</span></span> | <span data-ttu-id="0c049-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0c049-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0c049-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c049-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0c049-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c049-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0c049-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c049-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0c049-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c049-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0c049-128">Header</span><span class="sxs-lookup"><span data-stu-id="0c049-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c049-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c049-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="0c049-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c049-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="0c049-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c049-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0c049-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0c049-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c049-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c049-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c049-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c049-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c049-135">**glunewtess**</span><span class="sxs-lookup"><span data-stu-id="0c049-135">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="0c049-136">**glutessproperty**</span><span class="sxs-lookup"><span data-stu-id="0c049-136">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> </dl>

 

 





