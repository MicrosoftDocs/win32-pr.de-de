---
title: glColor4usv-Funktion (GL. h)
description: Legt die aktuelle Farbe von einem bereits vorhandenen Array von Farbwerten fest. | glColor4usv-Funktion (GL. h)
ms.assetid: 93a02461-4c8c-4b57-bedd-7d3be078e4c4
keywords:
- glColor4usv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColor4usv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b4cb1d502eeee16c710ac721500b109e5c3ac32
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961312"
---
# <a name="glcolor4usv-function"></a><span data-ttu-id="7c051-105">glColor4usv-Funktion</span><span class="sxs-lookup"><span data-stu-id="7c051-105">glColor4usv function</span></span>

<span data-ttu-id="7c051-106">Legt die aktuelle Farbe von einem bereits vorhandenen Array von Farbwerten fest.</span><span class="sxs-lookup"><span data-stu-id="7c051-106">Sets the current color from an already existing array of color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c051-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c051-107">Syntax</span></span>


```C++
void WINAPI glColor4usv(
   const GLushort *v
);
```



## <a name="parameters"></a><span data-ttu-id="7c051-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c051-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c051-109">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="7c051-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="7c051-110">Ein Zeiger auf ein Array, das die Werte rot, grün, blau und Alpha enthält.</span><span class="sxs-lookup"><span data-stu-id="7c051-110">A pointer to an array that contains red, green, blue, and alpha values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c051-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c051-111">Return value</span></span>

<span data-ttu-id="7c051-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7c051-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c051-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c051-113">Remarks</span></span>

<span data-ttu-id="7c051-114">Der GL speichert sowohl einen aktuellen einwertigen Farbindex als auch eine aktuelle vier wertige RGBA-Farbe.</span><span class="sxs-lookup"><span data-stu-id="7c051-114">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="7c051-115">mit **glcolor** wird eine neue vier wertige RGBA-Farbe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7c051-115">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="7c051-116">**glcolor** hat zwei Hauptvarianten: **glcolor3** und **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="7c051-116">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="7c051-117">**glcolor3** -Varianten geben die neuen roten, grünen und blauen Werte explizit an und legen den aktuellen Alpha-Wert implizit auf 1,0 (volle Intensität) fest.</span><span class="sxs-lookup"><span data-stu-id="7c051-117">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="7c051-118">**glcolor4** Varianten geben alle vier Farbkomponenten explizit an.</span><span class="sxs-lookup"><span data-stu-id="7c051-118">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="7c051-119">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** und **glcolor4i** nehmen drei oder vier signierte Byte-, kurzoder lange ganze Zahlen als Argumente an.</span><span class="sxs-lookup"><span data-stu-id="7c051-119">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="7c051-120">Wenn v an den Namen angefügt wird, können die Farb Befehle einen Zeiger auf ein Array solcher Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="7c051-120">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="7c051-121">Aktuelle Farbwerte werden im Gleit Komma Format mit nicht spezifizierten Mantisse-und Exponent-Größen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7c051-121">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="7c051-122">Ganzzahlige Farbkomponenten ohne Vorzeichen werden bei Angabe von Gleit Komma Werten linear zugeordnet, sodass der größte darstellbare Wert 1,0 (volle Intensität) und 0 dem Wert 0,0 (keine Intensität) zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="7c051-122">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="7c051-123">Ganzzahlige Farbkomponenten mit Vorzeichen werden bei Angabe von Gleit Komma Werten linear zugeordnet, sodass der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert-1,0 zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="7c051-123">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="7c051-124">(Beachten Sie, dass diese Zuordnung nicht 0 genau in 0,0 konvertiert.) Gleit Komma Werte werden direkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7c051-124">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="7c051-125">Weder Gleit Komma Werte noch ganzzahlige ganzzahlige Werte werden an den Bereich \[ 0, 1, \] vor dem Aktualisieren der aktuellen Farbe gebunden.</span><span class="sxs-lookup"><span data-stu-id="7c051-125">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="7c051-126">Farbkomponenten werden jedoch an diesen Bereich gebunden, bevor Sie interpoliert oder in einen Farb Puffer geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7c051-126">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c051-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c051-127">Requirements</span></span>



| <span data-ttu-id="7c051-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c051-128">Requirement</span></span> | <span data-ttu-id="7c051-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7c051-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c051-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c051-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7c051-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c051-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7c051-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c051-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7c051-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c051-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c051-134">Header</span><span class="sxs-lookup"><span data-stu-id="7c051-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c051-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c051-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7c051-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7c051-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c051-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c051-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7c051-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7c051-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c051-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c051-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c051-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c051-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c051-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7c051-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7c051-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7c051-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7c051-143">**glgetbooleanv, glgetdoublev, glgetfloatv, glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="7c051-143">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="7c051-144">**glindex**</span><span class="sxs-lookup"><span data-stu-id="7c051-144">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





