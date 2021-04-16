---
title: glColor4ui-Funktion (GL. h)
description: Legt die aktuelle Farbe fest. | glColor4ui-Funktion (GL. h)
ms.assetid: 8bcf7c6f-ed40-44eb-91d3-b82cb13c8445
keywords:
- glColor4ui-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColor4ui
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7ff1ef42cc5e8255f787d52a990d97573515dd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530761"
---
# <a name="glcolor4ui-function"></a><span data-ttu-id="c2227-105">glColor4ui-Funktion</span><span class="sxs-lookup"><span data-stu-id="c2227-105">glColor4ui function</span></span>

<span data-ttu-id="c2227-106">Legt die aktuelle Farbe fest.</span><span class="sxs-lookup"><span data-stu-id="c2227-106">Sets the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2227-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2227-107">Syntax</span></span>


```C++
void WINAPI glColor4ui(
   GLuint red,
   GLuint green,
   GLuint blue,
   GLuint alpha
);
```



## <a name="parameters"></a><span data-ttu-id="c2227-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2227-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2227-109">*Red*</span><span class="sxs-lookup"><span data-stu-id="c2227-109">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="c2227-110">Der neue rote Wert für die aktuelle Farbe.</span><span class="sxs-lookup"><span data-stu-id="c2227-110">The new red value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="c2227-111">*Grünbuchs*</span><span class="sxs-lookup"><span data-stu-id="c2227-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="c2227-112">Der neue grüne Wert für die aktuelle Farbe.</span><span class="sxs-lookup"><span data-stu-id="c2227-112">The new green value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="c2227-113">*blauen*</span><span class="sxs-lookup"><span data-stu-id="c2227-113">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="c2227-114">Der neue blaue Wert für die aktuelle Farbe.</span><span class="sxs-lookup"><span data-stu-id="c2227-114">The new blue value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="c2227-115">*alpha*</span><span class="sxs-lookup"><span data-stu-id="c2227-115">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="c2227-116">Der neue Alpha-Wert für die aktuelle Farbe.</span><span class="sxs-lookup"><span data-stu-id="c2227-116">The new alpha value for the current color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2227-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2227-117">Return value</span></span>

<span data-ttu-id="c2227-118">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c2227-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2227-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2227-119">Remarks</span></span>

<span data-ttu-id="c2227-120">Der GL speichert sowohl einen aktuellen einwertigen Farbindex als auch eine aktuelle vier wertige RGBA-Farbe.</span><span class="sxs-lookup"><span data-stu-id="c2227-120">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="c2227-121">mit **glcolor** wird eine neue vier wertige RGBA-Farbe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c2227-121">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="c2227-122">**glcolor** hat zwei Hauptvarianten: **glcolor3** und **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="c2227-122">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="c2227-123">**glcolor3** -Varianten geben die neuen roten, grünen und blauen Werte explizit an und legen den aktuellen Alpha-Wert implizit auf 1,0 (volle Intensität) fest.</span><span class="sxs-lookup"><span data-stu-id="c2227-123">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="c2227-124">**glcolor4** Varianten geben alle vier Farbkomponenten explizit an.</span><span class="sxs-lookup"><span data-stu-id="c2227-124">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="c2227-125">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** und **glcolor4i** nehmen drei oder vier signierte Byte-, kurzoder lange ganze Zahlen als Argumente an.</span><span class="sxs-lookup"><span data-stu-id="c2227-125">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="c2227-126">Wenn v an den Namen angefügt wird, können die Farb Befehle einen Zeiger auf ein Array solcher Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="c2227-126">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="c2227-127">Aktuelle Farbwerte werden im Gleit Komma Format mit nicht spezifizierten Mantisse-und Exponent-Größen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c2227-127">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="c2227-128">Ganzzahlige Farbkomponenten ohne Vorzeichen werden bei Angabe von Gleit Komma Werten linear zugeordnet, sodass der größte darstellbare Wert 1,0 (volle Intensität) und 0 dem Wert 0,0 (keine Intensität) zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="c2227-128">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="c2227-129">Ganzzahlige Farbkomponenten mit Vorzeichen werden bei Angabe von Gleit Komma Werten linear zugeordnet, sodass der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert-1,0 zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="c2227-129">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="c2227-130">(Beachten Sie, dass diese Zuordnung nicht 0 genau in 0,0 konvertiert.) Gleit Komma Werte werden direkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c2227-130">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="c2227-131">Weder Gleit Komma Werte noch ganzzahlige ganzzahlige Werte werden an den Bereich \[ 0, 1, \] vor dem Aktualisieren der aktuellen Farbe gebunden.</span><span class="sxs-lookup"><span data-stu-id="c2227-131">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="c2227-132">Farbkomponenten werden jedoch an diesen Bereich gebunden, bevor Sie interpoliert oder in einen Farb Puffer geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c2227-132">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2227-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2227-133">Requirements</span></span>



| <span data-ttu-id="c2227-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2227-134">Requirement</span></span> | <span data-ttu-id="c2227-135">Wert</span><span class="sxs-lookup"><span data-stu-id="c2227-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2227-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2227-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c2227-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2227-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c2227-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2227-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c2227-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2227-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c2227-140">Header</span><span class="sxs-lookup"><span data-stu-id="c2227-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2227-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2227-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c2227-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c2227-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2227-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2227-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c2227-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c2227-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2227-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2227-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2227-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2227-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2227-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c2227-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c2227-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c2227-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c2227-149">**glgetbooleanv, glgetdoublev, glgetfloatv, glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="c2227-149">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="c2227-150">**glindex**</span><span class="sxs-lookup"><span data-stu-id="c2227-150">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





