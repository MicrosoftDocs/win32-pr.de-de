---
title: glblendfunc-Funktion (GL. h)
description: Die Funktion "glblendfunc" gibt Pixel Arithmetik an.
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- glblendfunc-Funktion OpenGL
topic_type:
- apiref
api_name:
- glBlendFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6300543bbf589c704da6d941bd743f693e0ed5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344476"
---
# <a name="glblendfunc-function"></a><span data-ttu-id="003c3-104">glblendfunc-Funktion</span><span class="sxs-lookup"><span data-stu-id="003c3-104">glBlendFunc function</span></span>

<span data-ttu-id="003c3-105">Die Funktion " **glblendfunc** " gibt Pixel Arithmetik an.</span><span class="sxs-lookup"><span data-stu-id="003c3-105">The **glBlendFunc** function specifies pixel arithmetic.</span></span>

## <a name="syntax"></a><span data-ttu-id="003c3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="003c3-106">Syntax</span></span>


```C++
void WINAPI glBlendFunc(
   GLenum sfactor,
   GLenum dfactor
);
```



## <a name="parameters"></a><span data-ttu-id="003c3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="003c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="003c3-108">*sfactor*</span><span class="sxs-lookup"><span data-stu-id="003c3-108">*sfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="003c3-109">Gibt an, wie die Quell Mischungs Faktoren für Rot, grün, blau und Alpha berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="003c3-109">Specifies how the red, green, blue, and alpha source-blending factors are computed.</span></span> <span data-ttu-id="003c3-110">Neun symbolische Konstanten werden akzeptiert: GL \_ zero, GL \_ One, GL \_ DST \_ Color, GL \_ One \_ minus \_ DST \_ Color, GL \_ src \_ Alpha, GL \_ One \_ minus \_ src \_ Alpha, GL \_ DST \_ Alpha, GL \_ One \_ minus \_ DST \_ Alpha und GL \_ src \_ alpha \_ inteate.</span><span class="sxs-lookup"><span data-stu-id="003c3-110">Nine symbolic constants are accepted: GL\_ZERO, GL\_ONE, GL\_DST\_COLOR, GL\_ONE\_MINUS\_DST\_COLOR, GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA, GL\_DST\_ALPHA, GL\_ONE\_MINUS\_DST\_ALPHA, and GL\_SRC\_ALPHA\_SATURATE.</span></span>

</dd> <dt>

<span data-ttu-id="003c3-111">*Dfactor*</span><span class="sxs-lookup"><span data-stu-id="003c3-111">*dfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="003c3-112">Gibt an, wie die roten, grünen, blauen und Alpha-zielmischungs Faktoren berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="003c3-112">Specifies how the red, green, blue, and alpha destination-blending factors are computed.</span></span> <span data-ttu-id="003c3-113">Acht symbolische Konstanten werden akzeptiert: GL \_ zero, GL \_ One, GL \_ src \_ Color, GL \_ One \_ minus \_ src \_ Color, GL \_ src \_ Alpha, GL \_ One \_ minus \_ src \_ Alpha, GL \_ DST \_ Alpha und GL \_ One minus \_ \_ DST \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="003c3-113">Eight symbolic constants are accepted: GL\_ZERO, GL\_ONE, GL\_SRC\_COLOR, GL\_ONE\_MINUS\_SRC\_COLOR, GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA, GL\_DST\_ALPHA, and GL\_ONE\_MINUS\_DST\_ALPHA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="003c3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="003c3-114">Return value</span></span>

<span data-ttu-id="003c3-115">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="003c3-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="003c3-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="003c3-116">Error codes</span></span>

<span data-ttu-id="003c3-117">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="003c3-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="003c3-118">Name</span><span class="sxs-lookup"><span data-stu-id="003c3-118">Name</span></span>                                                                                                  | <span data-ttu-id="003c3-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="003c3-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="003c3-120"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="003c3-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="003c3-121">*Sfactor* oder *Dfactor* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="003c3-121">Either *sfactor* or *dfactor* was not an accepted value.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="003c3-122"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="003c3-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="003c3-123">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="003c3-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="003c3-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="003c3-124">Remarks</span></span>

<span data-ttu-id="003c3-125">Im RGB-Modus können Pixel mithilfe einer Funktion gezeichnet werden, die die eingehenden (Quell-) RGBA-Werte mit den RGBA-Werten kombiniert, die bereits im Frame Puffer (den Zielwerten) vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="003c3-125">In RGB mode, pixels can be drawn using a function that blends the incoming (source) RGBA values with the RGBA values that are already in the framebuffer (the destination values).</span></span> <span data-ttu-id="003c3-126">Standardmäßig ist Blending deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="003c3-126">By default, blending is disabled.</span></span> <span data-ttu-id="003c3-127">Verwenden Sie [**glEnable**](glenable.md) und [**glEnable**](gldisable.md) mit dem GL- \_ Argument GL, um das Mischen zu aktivieren und zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="003c3-127">Use [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the GL\_BLEND argument to enable and disable blending.</span></span>

<span data-ttu-id="003c3-128">Wenn diese Option aktiviert ist, definiert **glblendfunc** den Mischungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="003c3-128">When enabled, **glBlendFunc** defines the operation of blending.</span></span> <span data-ttu-id="003c3-129">Der *sfactor* -Parameter gibt an, welche von neun Methoden zum Skalieren der Quell Farbkomponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="003c3-129">The *sfactor* parameter specifies which of nine methods is used to scale the source color components.</span></span> <span data-ttu-id="003c3-130">Der *Dfactor* -Parameter gibt an, welche von acht Methoden zum Skalieren der Ziel Farbkomponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="003c3-130">The *dfactor* parameter specifies which of eight methods is used to scale the destination color components.</span></span> <span data-ttu-id="003c3-131">Die elf möglichen Methoden werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="003c3-131">The eleven possible methods are described in the following table.</span></span> <span data-ttu-id="003c3-132">Jede Methode definiert vier Skalierungsfaktoren für Rot, grün, blau und alpha.</span><span class="sxs-lookup"><span data-stu-id="003c3-132">Each method defines four scale factors one each for red, green, blue, and alpha.</span></span>

<span data-ttu-id="003c3-133">In der Tabelle und in nachfolgenden Gleichungen werden Quell-und Ziel Farbkomponenten als (*R*?</span><span class="sxs-lookup"><span data-stu-id="003c3-133">In the table and in subsequent equations, source and destination color components are referred to as (*R*?</span></span> <span data-ttu-id="003c3-134">, *G*?</span><span class="sxs-lookup"><span data-stu-id="003c3-134">, *G*?</span></span> <span data-ttu-id="003c3-135">, *B*?</span><span class="sxs-lookup"><span data-stu-id="003c3-135">, *B*?</span></span> <span data-ttu-id="003c3-136">, *A*?</span><span class="sxs-lookup"><span data-stu-id="003c3-136">, *A*?</span></span> <span data-ttu-id="003c3-137">) und (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *a*<sub>d</sub> ).</span><span class="sxs-lookup"><span data-stu-id="003c3-137">) and (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ).</span></span> <span data-ttu-id="003c3-138">Sie haben einen ganzzahligen Wert zwischen 0 (null) und (*k*<sub>r</sub> , *k*<sub>G</sub> , *k*<sub>r</sub> , *k*<sub>A</sub> ), wobei</span><span class="sxs-lookup"><span data-stu-id="003c3-138">They are understood to have integer values between zero and (*k*<sub>R</sub> , *k*<sub>G</sub> , *k*<sub>R</sub> , *k*<sub>A</sub> ), where</span></span>

<span data-ttu-id="003c3-139">*k*<sub>r</sub> = 2 <sup>m</sup>*r* -1</span><span class="sxs-lookup"><span data-stu-id="003c3-139">*k*<sub>R</sub> = 2 <sup>m</sup>*R* - 1</span></span>

<span data-ttu-id="003c3-140">*k*<sub>g</sub> = 2 <sup>m</sup>*g* -1</span><span class="sxs-lookup"><span data-stu-id="003c3-140">*k*<sub>G</sub> = 2 <sup>m</sup>*G* - 1</span></span>

<span data-ttu-id="003c3-141">*k*<sub>b</sub> = 2 <sup>Mio</sup>.*b* -1</span><span class="sxs-lookup"><span data-stu-id="003c3-141">*k*<sub>B</sub> = 2 <sup>m</sup>*B* - 1</span></span>

<span data-ttu-id="003c3-142">*k*<sub>a</sub> = 2 <sup>m</sup>*a* -1</span><span class="sxs-lookup"><span data-stu-id="003c3-142">*k*<sub>A</sub> = 2 <sup>m</sup>*A* - 1</span></span>

<span data-ttu-id="003c3-143">und (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>a</sub> ) ist die Anzahl von roten, grünen, blauen und Alpha-bitflächen.</span><span class="sxs-lookup"><span data-stu-id="003c3-143">and (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>A</sub> ) is the number of red, green, blue, and alpha bitplanes.</span></span>

<span data-ttu-id="003c3-144">Quell-und zielskalierungs Faktoren werden als (*s*<sub>r</sub> , *s*<sub>g</sub> , *s*<sub>B</sub> , *s*<sub>a</sub> ) und (*d*<sub>r</sub> , *d*<sub>G</sub> , *d*<sub>b</sub> , *d*<sub>a</sub> ) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="003c3-144">Source and destination scale factors are referred to as (*s*<sub>R</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>A</sub> ) and (*d*<sub>R</sub> , *d*<sub>G</sub> , *d*<sub>B</sub> , *d*<sub>A</sub> ).</span></span> <span data-ttu-id="003c3-145">Die in der Tabelle beschriebenen Skalierungsfaktoren (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ) stellen entweder den Quell-oder den Ziel Faktor dar.</span><span class="sxs-lookup"><span data-stu-id="003c3-145">The scale factors described in the table, denoted (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), represent either source or destination factors.</span></span> <span data-ttu-id="003c3-146">Alle Skalierungsfaktoren haben den Bereich \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="003c3-146">All scale factors have range \[0,1\].</span></span>



| <span data-ttu-id="003c3-147">Parameter</span><span class="sxs-lookup"><span data-stu-id="003c3-147">Parameter</span></span>                  | <span data-ttu-id="003c3-148">(*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>a</sub>  )</span><span class="sxs-lookup"><span data-stu-id="003c3-148">(*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )</span></span>                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="003c3-149">GL \_ null</span><span class="sxs-lookup"><span data-stu-id="003c3-149">GL\_ZERO</span></span>                   | <span data-ttu-id="003c3-150">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="003c3-150">(0,0,0,0)</span></span>                                                                                                                                                    |
| <span data-ttu-id="003c3-151">GL \_ 1</span><span class="sxs-lookup"><span data-stu-id="003c3-151">GL\_ONE</span></span>                    | <span data-ttu-id="003c3-152">(1, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="003c3-152">(1,1,1,1)</span></span>                                                                                                                                                    |
| <span data-ttu-id="003c3-153">GL- \_ src- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="003c3-153">GL\_SRC\_COLOR</span></span>             | <span data-ttu-id="003c3-154">(*R*?</span><span class="sxs-lookup"><span data-stu-id="003c3-154">(*R*?</span></span><span data-ttu-id="003c3-155"> / *k*<sub>R</sub> , *G*?</span><span class="sxs-lookup"><span data-stu-id="003c3-155"> / *k*<sub>R</sub> , *G*?</span></span><span data-ttu-id="003c3-156"> / *k*<sub>G</sub> , *B*?</span><span class="sxs-lookup"><span data-stu-id="003c3-156"> / *k*<sub>G</sub> , *B*?</span></span><span data-ttu-id="003c3-157"> / *k*<sub>B</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="003c3-157"> / *k*<sub>B</sub> , *A*?</span></span><span data-ttu-id="003c3-158"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="003c3-158"> / *k*<sub>A</sub> )</span></span>                                                         |
| <span data-ttu-id="003c3-159">GL \_ 1 \_ minus \_ src- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="003c3-159">GL\_ONE\_MINUS\_SRC\_COLOR</span></span> | <span data-ttu-id="003c3-160">(1, 1, 1, 1)-(*R*?</span><span class="sxs-lookup"><span data-stu-id="003c3-160">(1,1,1,1) - (*R*?</span></span><span data-ttu-id="003c3-161"> / *k*<sub>R</sub> , *G*?</span><span class="sxs-lookup"><span data-stu-id="003c3-161"> / *k*<sub>R</sub> , *G*?</span></span><span data-ttu-id="003c3-162"> / *k*<sub>G</sub> , *B*?</span><span class="sxs-lookup"><span data-stu-id="003c3-162"> / *k*<sub>G</sub> , *B*?</span></span><span data-ttu-id="003c3-163"> / *k*<sub>B</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="003c3-163"> / *k*<sub>B</sub> , *A*?</span></span><span data-ttu-id="003c3-164"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="003c3-164"> / *k*<sub>A</sub> )</span></span>                                             |
| <span data-ttu-id="003c3-165">GL- \_ DST- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="003c3-165">GL\_DST\_COLOR</span></span>             | <span data-ttu-id="003c3-166">(*R*<sub>d</sub>  /  *k*<sub>R</sub> , *G*<sub>d</sub>  /  *k*<sub>G</sub> , *B*<sub>d</sub>  /  *k*<sub>B</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="003c3-166">(*R*<sub>d</sub> / *k*<sub>R</sub> , *G*<sub>d</sub> / *k*<sub>G</sub> , *B*<sub>d</sub> / *k*<sub>B</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span>             |
| <span data-ttu-id="003c3-167">GL \_ 1 \_ minus \_ DST- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="003c3-167">GL\_ONE\_MINUS\_DST\_COLOR</span></span> | <span data-ttu-id="003c3-168">(1, 1, 1, 1)-(*R*<sub>d</sub>  /  *k*<sub>R</sub> , *G*<sub>d</sub>  /  *k*<sub>G</sub> , *B*<sub>d</sub>  /  *k*<sub>B</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="003c3-168">(1,1,1,1) - (*R*<sub>d</sub> / *k*<sub>R</sub> , *G*<sub>d</sub> / *k*<sub>G</sub> , *B*<sub>d</sub> / *k*<sub>B</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span> |
| <span data-ttu-id="003c3-169">GL \_ src \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="003c3-169">GL\_SRC\_ALPHA</span></span>             | <span data-ttu-id="003c3-170">(*A*?</span><span class="sxs-lookup"><span data-stu-id="003c3-170">(*A*?</span></span><span data-ttu-id="003c3-171"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="003c3-171"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="003c3-172"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="003c3-172"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="003c3-173"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="003c3-173"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="003c3-174"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="003c3-174"> / *k*<sub>A</sub> )</span></span>                                                         |
| <span data-ttu-id="003c3-175">GL \_ One \_ minus \_ src \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="003c3-175">GL\_ONE\_MINUS\_SRC\_ALPHA</span></span> | <span data-ttu-id="003c3-176">(1, 1, 1, 1)-(*A*?</span><span class="sxs-lookup"><span data-stu-id="003c3-176">(1,1,1,1) - (*A*?</span></span><span data-ttu-id="003c3-177"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="003c3-177"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="003c3-178"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="003c3-178"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="003c3-179"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="003c3-179"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="003c3-180"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="003c3-180"> / *k*<sub>A</sub> )</span></span>                                             |
| <span data-ttu-id="003c3-181">GL- \_ DST- \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="003c3-181">GL\_DST\_ALPHA</span></span>             | <span data-ttu-id="003c3-182">(*A*<sub>d</sub>  /  *k*<sub>A</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , <sub>d</sub>  /  *k*<sub>a</sub> , <sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="003c3-182">(*A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span>             |
| <span data-ttu-id="003c3-183">GL \_ 1 \_ minus \_ DST- \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="003c3-183">GL\_ONE\_MINUS\_DST\_ALPHA</span></span> | <span data-ttu-id="003c3-184">(1, 1, 1, 1)-(*a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , <sub>d</sub>  /  *k*<sub>a</sub> , <sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="003c3-184">(1,1,1,1) - (*A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span> |
| <span data-ttu-id="003c3-185">GL \_ src \_ alpha- \_ vollständig</span><span class="sxs-lookup"><span data-stu-id="003c3-185">GL\_SRC\_ALPHA\_SATURATE</span></span>   | <span data-ttu-id="003c3-186">(*i, i, i* , 1)</span><span class="sxs-lookup"><span data-stu-id="003c3-186">(*i,i,i,* 1)</span></span>                                                                                                                                                 |



 

<span data-ttu-id="003c3-187">In der Tabelle</span><span class="sxs-lookup"><span data-stu-id="003c3-187">In the table,</span></span>

<span data-ttu-id="003c3-188">*i* = min (*A*?</span><span class="sxs-lookup"><span data-stu-id="003c3-188">*i* = min (*A*?</span></span> <span data-ttu-id="003c3-189">, *k*<sub>a</sub>   -  <sub>d</sub> )/ *k*<sub>a</sub></span><span class="sxs-lookup"><span data-stu-id="003c3-189">, *k*<sub>A</sub>  - *A*<sub>d</sub> ) / *k*<sub>A</sub></span></span>

<span data-ttu-id="003c3-190">Zum Ermitteln der gemischten RGBA-Werte eines Pixels beim Zeichnen im RGBA-Modus verwendet das System die folgenden Gleichungen:</span><span class="sxs-lookup"><span data-stu-id="003c3-190">To determine the blended RGBA values of a pixel when drawing in RGBA mode, the system uses the following equations:</span></span>

<span data-ttu-id="003c3-191">*R* (*d*) = min ( *k*<sub>r</sub> , *r*? *s*<sub>r</sub>  +  *r*<sub>d</sub> <sub>r</sub> )</span><span class="sxs-lookup"><span data-stu-id="003c3-191">*R* (*d*) = min( *k*<sub>R</sub> , *R*? *s*<sub>R</sub> + *R*<sub>d</sub> *d*<sub>R</sub> )</span></span>

<span data-ttu-id="003c3-192">*G* (*d*) = min ( *k*<sub>g</sub> , *g*? *s*<sub>g</sub>  +  *g*<sub>d</sub> *d*<sub>g</sub> )</span><span class="sxs-lookup"><span data-stu-id="003c3-192">*G* (*d*) = min( *k*<sub>G</sub> , *G*? *s*<sub>G</sub> + *G*<sub>d</sub> *d*<sub>G</sub>  )</span></span>

<span data-ttu-id="003c3-193">*B* (*d*) = min ( *k*<sub>B</sub> *, b*? *s*<sub>b</sub>  +  *b*<sub>d</sub> *b*<sub></sub> )</span><span class="sxs-lookup"><span data-stu-id="003c3-193">*B* (*d*) = min( *k*<sub>B</sub> *, B*? *s*<sub>B</sub> + *B*<sub>d</sub> *d*<sub>B</sub>  )</span></span>

<span data-ttu-id="003c3-194">*A* (*d*) = min ( *k*<sub>A</sub> , *a*? *s*<sub>a</sub>  +  <sub>d</sub> <sub></sub> a)</span><span class="sxs-lookup"><span data-stu-id="003c3-194">*A* (*d*) = min( *k*<sub>A</sub> , *A*? *s*<sub>A</sub> + *A*<sub>d</sub> *d*<sub>A</sub>  )</span></span>

<span data-ttu-id="003c3-195">Trotz der offensichtlichen Genauigkeit der obigen Gleichungen ist das Mischen von Arithmetik nicht genau angegeben, da die Mischung mit unpräzisen ganzzahligen Farbwerten arbeitet.</span><span class="sxs-lookup"><span data-stu-id="003c3-195">Despite the apparent precision of the above equations, blending arithmetic is not exactly specified, because blending operates with imprecise integer color values.</span></span> <span data-ttu-id="003c3-196">Ein Blend-Faktor, der gleich 1 sein sollte, ist jedoch garantiert, dass seine multipktivität nicht geändert wird, und ein Blend-Faktor, der gleich 0 (null) ist, reduziert seinen Multiplikand auf NULL.</span><span class="sxs-lookup"><span data-stu-id="003c3-196">However, a blend factor that should be equal to one is guaranteed not to modify its multiplicand, and a blend factor equal to zero reduces its multiplicand to zero.</span></span> <span data-ttu-id="003c3-197">Wenn *sfactor* z. b. "GL \_ src Alpha" ist \_ , ist " *Dfactor* " GL \_ One \_ minus \_ src \_ Alpha und "?" gleich *k*<sub>A</sub>. die Gleichungen verringern die einfache Ersetzung: </span><span class="sxs-lookup"><span data-stu-id="003c3-197">Thus, for example, when *sfactor* is GL\_SRC\_ALPHA, *dfactor* is GL\_ONE\_MINUS\_SRC\_ALPHA, and *A*? is equal to *k*<sub>A</sub>, the equations reduce to simple replacement:</span></span>

<span data-ttu-id="003c3-198">*R*<sub>d</sub>  =  *r*?</span><span class="sxs-lookup"><span data-stu-id="003c3-198">*R*<sub>d</sub> = *R*?</span></span>

<span data-ttu-id="003c3-199">*G*<sub>d</sub>  =  *g*?</span><span class="sxs-lookup"><span data-stu-id="003c3-199">*G*<sub>d</sub> = *G*?</span></span>

<span data-ttu-id="003c3-200">B <sub>d</sub>  =  *b*?</span><span class="sxs-lookup"><span data-stu-id="003c3-200">B <sub>d</sub> = *B*?</span></span>

<span data-ttu-id="003c3-201">*A*<sub>d</sub>  =  *a*?</span><span class="sxs-lookup"><span data-stu-id="003c3-201">*A*<sub>d</sub> = *A*?</span></span>

## <a name="examples"></a><span data-ttu-id="003c3-202">Beispiele</span><span class="sxs-lookup"><span data-stu-id="003c3-202">Examples</span></span>

<span data-ttu-id="003c3-203">Transparenz wird am besten mithilfe von **glblendfunc**(GL \_ src \_ Alpha, GL \_ One \_ minus \_ src \_ Alpha) implementiert, wobei primitive vom weitesten zum nächsten sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="003c3-203">Transparency is best implemented using **glBlendFunc**(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) with primitives sorted from farthest to nearest.</span></span> <span data-ttu-id="003c3-204">Beachten Sie, dass diese Transparenz Berechnung nicht erfordert, dass Alpha-bitflächen im Framebuffer vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="003c3-204">Note that this transparency calculation does not require the presence of alpha bitplanes in the framebuffer.</span></span>

<span data-ttu-id="003c3-205">Sie können auch **glblendfunc**(GL \_ src \_ Alpha, GL \_ One \_ minus \_ src \_ Alpha) zum Rendern von Antialiasing Punkten und Zeilen in beliebiger Reihenfolge verwenden.</span><span class="sxs-lookup"><span data-stu-id="003c3-205">You can also use **glBlendFunc**(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) for rendering antialiased points and lines in arbitrary order.</span></span>

<span data-ttu-id="003c3-206">Um das Polygon-Antialiasing zu optimieren, verwenden Sie **glblendfunc**(GL \_ src \_ alpha \_ sätate, GL \_ One) mit Polygonen, die von der nächstgelegenen zu weit entfernten sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="003c3-206">To optimize polygon antialiasing, use **glBlendFunc**(GL\_SRC\_ALPHA\_SATURATE, GL\_ONE) with polygons sorted from nearest to farthest.</span></span> <span data-ttu-id="003c3-207">(Siehe GL \_ . Polygon- \_ Smooth-Argument in [**glEnable**](glenable.md) für Informationen zum Polygon-Antialiasing.) Ziel-Alpha bitflächen, die vorhanden sein müssen, damit diese Blend-Funktion ordnungsgemäß funktioniert, speichern die akkumulierte Abdeckung.</span><span class="sxs-lookup"><span data-stu-id="003c3-207">(See the GL\_POLYGON\_SMOOTH argument in [**glEnable**](glenable.md) for information on polygon antialiasing.) Destination alpha bitplanes, which must be present for this blend function to operate correctly, store the accumulated coverage.</span></span>

<span data-ttu-id="003c3-208">Ein eingehender (Quelle) Alpha ist eine Material Deckkraft im Bereich von 1,0 (*K*<sub>a</sub> ), die eine komplette Deckkraft darstellt, bis 0,0 (0), die eine umfassende Transparenz darstellt.</span><span class="sxs-lookup"><span data-stu-id="003c3-208">Incoming (source) alpha is a material opacity, ranging from 1.0 (*K*<sub>A</sub> ), representing complete opacity, to 0.0 (0), representing complete transparency.</span></span>

<span data-ttu-id="003c3-209">Wenn Sie mehr als einen Farb Puffer für das Zeichnen aktivieren, wird jeder aktivierte Puffer separat gemischt, und der Inhalt des Puffers wird für die Zielfarbe verwendet.</span><span class="sxs-lookup"><span data-stu-id="003c3-209">When you enable more than one color buffer for drawing, each enabled buffer is blended separately, and the contents of the buffer is used for destination color.</span></span> <span data-ttu-id="003c3-210">(Siehe [**gldrawbuffer**](gldrawbuffer.md).)</span><span class="sxs-lookup"><span data-stu-id="003c3-210">(See [**glDrawBuffer**](gldrawbuffer.md).)</span></span>

<span data-ttu-id="003c3-211">Blending wirkt sich nur auf das RGBA-Rendering aus.</span><span class="sxs-lookup"><span data-stu-id="003c3-211">Blending affects only RGBA rendering.</span></span> <span data-ttu-id="003c3-212">Sie wird von farbindexrenderatoren ignoriert.</span><span class="sxs-lookup"><span data-stu-id="003c3-212">It is ignored by color-index renderers.</span></span>

<span data-ttu-id="003c3-213">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glblendfunc** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="003c3-213">The following functions retrieve information related to **glBlendFunc**:</span></span>

<span data-ttu-id="003c3-214">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Blend \_ src</span><span class="sxs-lookup"><span data-stu-id="003c3-214">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_BLEND\_SRC</span></span>

<span data-ttu-id="003c3-215">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Blend \_ DST</span><span class="sxs-lookup"><span data-stu-id="003c3-215">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_BLEND\_DST</span></span>

<span data-ttu-id="003c3-216">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Blend</span><span class="sxs-lookup"><span data-stu-id="003c3-216">[**glIsEnabled**](glisenabled.md) with argument GL\_BLEND</span></span>

## <a name="requirements"></a><span data-ttu-id="003c3-217">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="003c3-217">Requirements</span></span>



| <span data-ttu-id="003c3-218">Anforderung</span><span class="sxs-lookup"><span data-stu-id="003c3-218">Requirement</span></span> | <span data-ttu-id="003c3-219">Wert</span><span class="sxs-lookup"><span data-stu-id="003c3-219">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="003c3-220">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="003c3-220">Minimum supported client</span></span><br/> | <span data-ttu-id="003c3-221">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="003c3-221">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="003c3-222">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="003c3-222">Minimum supported server</span></span><br/> | <span data-ttu-id="003c3-223">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="003c3-223">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="003c3-224">Header</span><span class="sxs-lookup"><span data-stu-id="003c3-224">Header</span></span><br/>                   | <dl> <span data-ttu-id="003c3-225"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="003c3-225"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="003c3-226">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="003c3-226">Library</span></span><br/>                  | <dl> <span data-ttu-id="003c3-227"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="003c3-227"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="003c3-228">DLL</span><span class="sxs-lookup"><span data-stu-id="003c3-228">DLL</span></span><br/>                      | <dl> <span data-ttu-id="003c3-229"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="003c3-229"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="003c3-230">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="003c3-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="003c3-231">**glalphafunc**</span><span class="sxs-lookup"><span data-stu-id="003c3-231">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="003c3-232">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="003c3-232">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="003c3-233">**glClear**</span><span class="sxs-lookup"><span data-stu-id="003c3-233">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="003c3-234">**gldeaktivieren**</span><span class="sxs-lookup"><span data-stu-id="003c3-234">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="003c3-235">**gldrawbuffer**</span><span class="sxs-lookup"><span data-stu-id="003c3-235">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="003c3-236">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="003c3-236">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="003c3-237">**glget**</span><span class="sxs-lookup"><span data-stu-id="003c3-237">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="003c3-238">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="003c3-238">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="003c3-239">**gllogicop**</span><span class="sxs-lookup"><span data-stu-id="003c3-239">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="003c3-240">**glstencilfunc**</span><span class="sxs-lookup"><span data-stu-id="003c3-240">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





