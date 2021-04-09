---
title: glColor3uiv-Funktion (GL. h)
description: Legt die aktuelle Farbe von einem bereits vorhandenen Array von Farbwerten fest. | glColor3uiv-Funktion (GL. h)
ms.assetid: f63a165c-57a0-425d-874f-551761af5fe7
keywords:
- glColor3uiv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColor3uiv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b7b7981dd84c6d8fd4211e08a3358ad6e6c357f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869891"
---
# <a name="glcolor3uiv-function"></a><span data-ttu-id="2a92b-105">glColor3uiv-Funktion</span><span class="sxs-lookup"><span data-stu-id="2a92b-105">glColor3uiv function</span></span>

<span data-ttu-id="2a92b-106">Legt die aktuelle Farbe von einem bereits vorhandenen Array von Farbwerten fest.</span><span class="sxs-lookup"><span data-stu-id="2a92b-106">Sets the current color from an already existing array of color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a92b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a92b-107">Syntax</span></span>


```C++
void WINAPI glColor3uiv(
   const GLuint *v
);
```



## <a name="parameters"></a><span data-ttu-id="2a92b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a92b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a92b-109">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="2a92b-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="2a92b-110">Ein Zeiger auf ein Array, das rote, grüne und blaue Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="2a92b-110">A pointer to an array that contains red, green, and blue values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a92b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a92b-111">Return value</span></span>

<span data-ttu-id="2a92b-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2a92b-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a92b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a92b-113">Remarks</span></span>

<span data-ttu-id="2a92b-114">Der GL speichert sowohl einen aktuellen einwertigen Farbindex als auch eine aktuelle vier wertige RGBA-Farbe.</span><span class="sxs-lookup"><span data-stu-id="2a92b-114">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="2a92b-115">mit **glcolor** wird eine neue vier wertige RGBA-Farbe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2a92b-115">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="2a92b-116">**glcolor** hat zwei Hauptvarianten: **glcolor3** und **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="2a92b-116">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="2a92b-117">**glcolor3** -Varianten geben die neuen roten, grünen und blauen Werte explizit an und legen den aktuellen Alpha-Wert implizit auf 1,0 (volle Intensität) fest.</span><span class="sxs-lookup"><span data-stu-id="2a92b-117">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="2a92b-118">**glcolor4** Varianten geben alle vier Farbkomponenten explizit an.</span><span class="sxs-lookup"><span data-stu-id="2a92b-118">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="2a92b-119">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** und **glcolor4i** nehmen drei oder vier signierte Byte-, kurzoder lange ganze Zahlen als Argumente an.</span><span class="sxs-lookup"><span data-stu-id="2a92b-119">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="2a92b-120">Wenn v an den Namen angefügt wird, können die Farb Befehle einen Zeiger auf ein Array solcher Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="2a92b-120">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="2a92b-121">Aktuelle Farbwerte werden im Gleit Komma Format mit nicht spezifizierten Mantisse-und Exponent-Größen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2a92b-121">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="2a92b-122">Ganzzahlige Farbkomponenten ohne Vorzeichen werden bei Angabe von Gleit Komma Werten linear zugeordnet, sodass der größte darstellbare Wert 1,0 (volle Intensität) und 0 dem Wert 0,0 (keine Intensität) zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="2a92b-122">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="2a92b-123">Ganzzahlige Farbkomponenten mit Vorzeichen werden bei Angabe von Gleit Komma Werten linear zugeordnet, sodass der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert-1,0 zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="2a92b-123">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="2a92b-124">(Beachten Sie, dass diese Zuordnung nicht 0 genau in 0,0 konvertiert.) Gleit Komma Werte werden direkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2a92b-124">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="2a92b-125">Weder Gleit Komma Werte noch ganzzahlige ganzzahlige Werte werden an den Bereich \[ 0, 1, \] vor dem Aktualisieren der aktuellen Farbe gebunden.</span><span class="sxs-lookup"><span data-stu-id="2a92b-125">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="2a92b-126">Farbkomponenten werden jedoch an diesen Bereich gebunden, bevor Sie interpoliert oder in einen Farb Puffer geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2a92b-126">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a92b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a92b-127">Requirements</span></span>



| <span data-ttu-id="2a92b-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a92b-128">Requirement</span></span> | <span data-ttu-id="2a92b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2a92b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a92b-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a92b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2a92b-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a92b-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2a92b-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a92b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2a92b-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a92b-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2a92b-134">Header</span><span class="sxs-lookup"><span data-stu-id="2a92b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a92b-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a92b-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2a92b-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2a92b-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="2a92b-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a92b-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2a92b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2a92b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a92b-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a92b-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a92b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a92b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a92b-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2a92b-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2a92b-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="2a92b-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2a92b-143">**glgetbooleanv, glgetdoublev, glgetfloatv, glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="2a92b-143">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="2a92b-144">**glindex**</span><span class="sxs-lookup"><span data-stu-id="2a92b-144">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





