---
title: gluvierccallback-Funktion (glu. h)
description: Die Funktion "gluvierccallback" definiert einen Rückruf für ein Quadric-Objekt.
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- gluvierccallback-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluQuadricCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c0c92e3cd4e723b59ee9060c5e2f33b710e7f69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518413"
---
# <a name="gluquadriccallback-function"></a><span data-ttu-id="9b49c-104">gluvierccallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="9b49c-104">gluQuadricCallback function</span></span>

<span data-ttu-id="9b49c-105">Die Funktion " **gluvierccallback** " definiert einen Rückruf für ein Quadric-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9b49c-105">The **gluQuadricCallback** function defines a callback for a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b49c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b49c-106">Syntax</span></span>


```C++
void WINAPI gluQuadricCallback(
   GLUquadric *qobj,
   GLenum     which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="9b49c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b49c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b49c-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="9b49c-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="9b49c-109">Das Quadric-Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="9b49c-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9b49c-110">*,*</span><span class="sxs-lookup"><span data-stu-id="9b49c-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="9b49c-111">Der Rückruf, der definiert wird.</span><span class="sxs-lookup"><span data-stu-id="9b49c-111">The callback being defined.</span></span> <span data-ttu-id="9b49c-112">Der einzige gültige Wert ist "glu \_ Error".</span><span class="sxs-lookup"><span data-stu-id="9b49c-112">The only valid value is GLU\_ERROR.</span></span>



| <span data-ttu-id="9b49c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="9b49c-113">Value</span></span>                                                                                                                                             | <span data-ttu-id="9b49c-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9b49c-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <span data-ttu-id="9b49c-115"><dt>**Glu- \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="9b49c-115"><dt>**GLU\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="9b49c-116">Die Funktion " **gluvierccallback** " wird aufgerufen, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="9b49c-116">The **gluQuadricCallback** function is called when an error is encountered.</span></span> <span data-ttu-id="9b49c-117">Das einzige Argument ist vom Typ " **GLenum**" und gibt den spezifischen Fehler an, der aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9b49c-117">Its single argument is of type **GLenum**, and it indicates the specific error that occurred.</span></span> <span data-ttu-id="9b49c-118">Zeichen folgen, die diese Fehler beschreiben, können mit dem " [**gluerrorstring**](gluerrorstring.md) "-Befehl abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9b49c-118">Character strings describing these errors can be retrieved with the [**gluErrorString**](gluerrorstring.md) call.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9b49c-119">*fn*</span><span class="sxs-lookup"><span data-stu-id="9b49c-119">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="9b49c-120">Die aufzurufende Funktion.</span><span class="sxs-lookup"><span data-stu-id="9b49c-120">The function to be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b49c-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b49c-121">Return value</span></span>

<span data-ttu-id="9b49c-122">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9b49c-122">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b49c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b49c-123">Remarks</span></span>

<span data-ttu-id="9b49c-124">Verwenden Sie " **gluvierccallback** ", um einen neuen Rückruf zu definieren, der von einem Quadric-Objekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b49c-124">Use **gluQuadricCallback** to define a new callback to be used by a quadric object.</span></span> <span data-ttu-id="9b49c-125">Wenn der angegebene Rückruf bereits definiert ist, wird er ersetzt.</span><span class="sxs-lookup"><span data-stu-id="9b49c-125">If the specified callback is already defined, it is replaced.</span></span> <span data-ttu-id="9b49c-126">Wenn *FN* den Wert **null** hat, wird ein beliebiger vorhandener Rückruf gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9b49c-126">If *fn* is **NULL**, any existing callback is erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b49c-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b49c-127">Requirements</span></span>



| <span data-ttu-id="9b49c-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b49c-128">Requirement</span></span> | <span data-ttu-id="9b49c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9b49c-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9b49c-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b49c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9b49c-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b49c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9b49c-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b49c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9b49c-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b49c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9b49c-134">Header</span><span class="sxs-lookup"><span data-stu-id="9b49c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b49c-135"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b49c-135"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9b49c-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9b49c-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b49c-137"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b49c-137"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9b49c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9b49c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b49c-139"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b49c-139"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b49c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b49c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b49c-141">**gluerrorstring**</span><span class="sxs-lookup"><span data-stu-id="9b49c-141">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="9b49c-142">**glunewquadric**</span><span class="sxs-lookup"><span data-stu-id="9b49c-142">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> </dl>

 

 





