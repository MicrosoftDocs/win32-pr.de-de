---
title: glCopyTexImage2D-Funktion (GL. h)
description: Die glCopyTexImage2D-Funktion kopiert Pixel aus dem Frame Puffer in ein zweidimensionales Textur Bild.
ms.assetid: 4b9d7be6-054d-4590-b3f0-a2a670786c4b
keywords:
- glCopyTexImage2D-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d04a979e9bb026da904687506f3201d12c12c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858980"
---
# <a name="glcopyteximage2d-function"></a><span data-ttu-id="dd3c2-104">glCopyTexImage2D-Funktion</span><span class="sxs-lookup"><span data-stu-id="dd3c2-104">glCopyTexImage2D function</span></span>

<span data-ttu-id="dd3c2-105">Die **glCopyTexImage2D** -Funktion kopiert Pixel aus dem Frame Puffer in ein zweidimensionales Textur Bild.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-105">The **glCopyTexImage2D** function copies pixels from the framebuffer into a two-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd3c2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd3c2-106">Syntax</span></span>


```C++
void WINAPI glCopyTexImage2D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLint   border
);
```



## <a name="parameters"></a><span data-ttu-id="dd3c2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd3c2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd3c2-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="dd3c2-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="dd3c2-109">Das Ziel, in das die Bilddaten geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="dd3c2-110">Muss den Wert "GL \_ Texture \_ 2D" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-110">Must have the value GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="dd3c2-111">*level*</span><span class="sxs-lookup"><span data-stu-id="dd3c2-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="dd3c2-112">Die Detailebene.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-112">The level-of-detail number.</span></span> <span data-ttu-id="dd3c2-113">Ebene 0 ist das Basis Image.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-113">Level 0 is the base image.</span></span> <span data-ttu-id="dd3c2-114">Ebene *n* ist das *n*-te MipMap-Reduzierungs Bild.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="dd3c2-115">*internalformat*</span><span class="sxs-lookup"><span data-stu-id="dd3c2-115">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="dd3c2-116">Das interne Format und die Auflösung der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-116">The internal format and resolution of the texture data.</span></span> <span data-ttu-id="dd3c2-117">Die Werte 1, 2, 3 und 4 werden für *internalformat* nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-117">The values 1, 2, 3, and 4 are not accepted for *internalFormat*.</span></span> <span data-ttu-id="dd3c2-118">Der-Parameter kann einen der folgenden symbolischen Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-118">The parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="dd3c2-119">Konstante</span><span class="sxs-lookup"><span data-stu-id="dd3c2-119">Constant</span></span>                 | <span data-ttu-id="dd3c2-120">R-Bits</span><span class="sxs-lookup"><span data-stu-id="dd3c2-120">R Bits</span></span> | <span data-ttu-id="dd3c2-121">G Bits</span><span class="sxs-lookup"><span data-stu-id="dd3c2-121">G Bits</span></span> | <span data-ttu-id="dd3c2-122">B Bits</span><span class="sxs-lookup"><span data-stu-id="dd3c2-122">B Bits</span></span> | <span data-ttu-id="dd3c2-123">Eine Bits</span><span class="sxs-lookup"><span data-stu-id="dd3c2-123">A Bits</span></span> | <span data-ttu-id="dd3c2-124">L Bits</span><span class="sxs-lookup"><span data-stu-id="dd3c2-124">L Bits</span></span> | <span data-ttu-id="dd3c2-125">I Bits</span><span class="sxs-lookup"><span data-stu-id="dd3c2-125">I Bits</span></span> |
|--------------------------|--------|--------|--------|--------|--------|--------|
| <span data-ttu-id="dd3c2-126">GL- \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="dd3c2-126">GL\_ALPHA</span></span>                |        |        |        |        |        |        |
| <span data-ttu-id="dd3c2-127">GL \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-127">GL\_ALPHA4</span></span>               |        |        |        | <span data-ttu-id="dd3c2-128">4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-128">4</span></span>      |        |        |
| <span data-ttu-id="dd3c2-129">GL \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-129">GL\_ALPHA8</span></span>               |        |        |        | <span data-ttu-id="dd3c2-130">8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-130">8</span></span>      |        |        |
| <span data-ttu-id="dd3c2-131">GL \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-131">GL\_ALPHA12</span></span>              |        |        |        | <span data-ttu-id="dd3c2-132">12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-132">12</span></span>     |        |        |
| <span data-ttu-id="dd3c2-133">GL \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-133">GL\_ALPHA16</span></span>              |        |        |        | <span data-ttu-id="dd3c2-134">16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-134">16</span></span>     |        |        |
| <span data-ttu-id="dd3c2-135">GL- \_ Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="dd3c2-135">GL\_LUMINANCE</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="dd3c2-136">GL \_ LUMINANCE4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-136">GL\_LUMINANCE4</span></span>           |        |        |        |        | <span data-ttu-id="dd3c2-137">4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-137">4</span></span>      |        |
| <span data-ttu-id="dd3c2-138">GL \_ LUMINANCE8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-138">GL\_LUMINANCE8</span></span>           |        |        |        |        | <span data-ttu-id="dd3c2-139">8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-139">8</span></span>      |        |
| <span data-ttu-id="dd3c2-140">GL \_ LUMINANCE12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-140">GL\_LUMINANCE12</span></span>          |        |        |        |        | <span data-ttu-id="dd3c2-141">12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-141">12</span></span>     |        |
| <span data-ttu-id="dd3c2-142">GL \_ LUMINANCE16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-142">GL\_LUMINANCE16</span></span>          |        |        |        |        | <span data-ttu-id="dd3c2-143">16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-143">16</span></span>     |        |
| <span data-ttu-id="dd3c2-144">GL- \_ Leuchtkraft \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="dd3c2-144">GL\_LUMINANCE\_ALPHA</span></span>     |        |        |        |        |        |        |
| <span data-ttu-id="dd3c2-145">GL \_ LUMINANCE4 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-145">GL\_LUMINANCE4\_ALPHA4</span></span>   |        |        |        | <span data-ttu-id="dd3c2-146">4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-146">4</span></span>      | <span data-ttu-id="dd3c2-147">4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-147">4</span></span>      |        |
| <span data-ttu-id="dd3c2-148">GL \_ LUMINANCE6 \_ ALPHA2</span><span class="sxs-lookup"><span data-stu-id="dd3c2-148">GL\_LUMINANCE6\_ALPHA2</span></span>   |        |        |        | <span data-ttu-id="dd3c2-149">2</span><span class="sxs-lookup"><span data-stu-id="dd3c2-149">2</span></span>      | <span data-ttu-id="dd3c2-150">6</span><span class="sxs-lookup"><span data-stu-id="dd3c2-150">6</span></span>      |        |
| <span data-ttu-id="dd3c2-151">GL \_ LUMINANCE8 \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-151">GL\_LUMINANCE8\_ALPHA8</span></span>   |        |        |        | <span data-ttu-id="dd3c2-152">8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-152">8</span></span>      | <span data-ttu-id="dd3c2-153">8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-153">8</span></span>      |        |
| <span data-ttu-id="dd3c2-154">GL \_ LUMINANCE12 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-154">GL\_LUMINANCE12\_ALPHA4</span></span>  |        |        |        | <span data-ttu-id="dd3c2-155">4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-155">4</span></span>      | <span data-ttu-id="dd3c2-156">12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-156">12</span></span>     |        |
| <span data-ttu-id="dd3c2-157">GL \_ LUMINANCE12 \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-157">GL\_LUMINANCE12\_ALPHA12</span></span> |        |        |        | <span data-ttu-id="dd3c2-158">12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-158">12</span></span>     | <span data-ttu-id="dd3c2-159">12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-159">12</span></span>     |        |
| <span data-ttu-id="dd3c2-160">GL \_ LUMINANCE16 \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-160">GL\_LUMINANCE16\_ALPHA16</span></span> |        |        |        | <span data-ttu-id="dd3c2-161">16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-161">16</span></span>     | <span data-ttu-id="dd3c2-162">16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-162">16</span></span>     |        |
| <span data-ttu-id="dd3c2-163">GL- \_ Intensität</span><span class="sxs-lookup"><span data-stu-id="dd3c2-163">GL\_INTENSITY</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="dd3c2-164">GL \_ INTENSITY4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-164">GL\_INTENSITY4</span></span>           |        |        |        |        |        | <span data-ttu-id="dd3c2-165">4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-165">4</span></span>      |
| <span data-ttu-id="dd3c2-166">GL \_ INTENSITY8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-166">GL\_INTENSITY8</span></span>           |        |        |        |        |        | <span data-ttu-id="dd3c2-167">8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-167">8</span></span>      |
| <span data-ttu-id="dd3c2-168">GL \_ INTENSITY12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-168">GL\_INTENSITY12</span></span>          |        |        |        |        |        | <span data-ttu-id="dd3c2-169">12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-169">12</span></span>     |
| <span data-ttu-id="dd3c2-170">GL \_ INTENSITY16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-170">GL\_INTENSITY16</span></span>          |        |        |        |        |        | <span data-ttu-id="dd3c2-171">16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-171">16</span></span>     |
| <span data-ttu-id="dd3c2-172">GL. \_ RGB</span><span class="sxs-lookup"><span data-stu-id="dd3c2-172">GL\_RGB</span></span>                  |        |        |        |        |        |        |
| <span data-ttu-id="dd3c2-173">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="dd3c2-173">GL\_R3\_G3\_B2</span></span>           | <span data-ttu-id="dd3c2-174">3</span><span class="sxs-lookup"><span data-stu-id="dd3c2-174">3</span></span>      | <span data-ttu-id="dd3c2-175">3</span><span class="sxs-lookup"><span data-stu-id="dd3c2-175">3</span></span>      | <span data-ttu-id="dd3c2-176">2</span><span class="sxs-lookup"><span data-stu-id="dd3c2-176">2</span></span>      |        |        |        |
| <span data-ttu-id="dd3c2-177">GL \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-177">GL\_RGB4</span></span>                 | <span data-ttu-id="dd3c2-178">4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-178">4</span></span>      | <span data-ttu-id="dd3c2-179">4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-179">4</span></span>      | <span data-ttu-id="dd3c2-180">4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-180">4</span></span>      |        |        |        |
| <span data-ttu-id="dd3c2-181">GL \_ RGB5</span><span class="sxs-lookup"><span data-stu-id="dd3c2-181">GL\_RGB5</span></span>                 | <span data-ttu-id="dd3c2-182">5</span><span class="sxs-lookup"><span data-stu-id="dd3c2-182">5</span></span>      | <span data-ttu-id="dd3c2-183">5</span><span class="sxs-lookup"><span data-stu-id="dd3c2-183">5</span></span>      | <span data-ttu-id="dd3c2-184">5</span><span class="sxs-lookup"><span data-stu-id="dd3c2-184">5</span></span>      |        |        |        |
| <span data-ttu-id="dd3c2-185">GL \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-185">GL\_RGB8</span></span>                 | <span data-ttu-id="dd3c2-186">8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-186">8</span></span>      | <span data-ttu-id="dd3c2-187">8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-187">8</span></span>      | <span data-ttu-id="dd3c2-188">8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-188">8</span></span>      |        |        |        |
| <span data-ttu-id="dd3c2-189">GL \_ RGB10</span><span class="sxs-lookup"><span data-stu-id="dd3c2-189">GL\_RGB10</span></span>                | <span data-ttu-id="dd3c2-190">10</span><span class="sxs-lookup"><span data-stu-id="dd3c2-190">10</span></span>     | <span data-ttu-id="dd3c2-191">10</span><span class="sxs-lookup"><span data-stu-id="dd3c2-191">10</span></span>     | <span data-ttu-id="dd3c2-192">10</span><span class="sxs-lookup"><span data-stu-id="dd3c2-192">10</span></span>     |        |        |        |
| <span data-ttu-id="dd3c2-193">GL \_ RGB12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-193">GL\_RGB12</span></span>                | <span data-ttu-id="dd3c2-194">12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-194">12</span></span>     | <span data-ttu-id="dd3c2-195">12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-195">12</span></span>     | <span data-ttu-id="dd3c2-196">12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-196">12</span></span>     |        |        |        |
| <span data-ttu-id="dd3c2-197">GL \_ RGB16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-197">GL\_RGB16</span></span>                | <span data-ttu-id="dd3c2-198">16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-198">16</span></span>     | <span data-ttu-id="dd3c2-199">16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-199">16</span></span>     | <span data-ttu-id="dd3c2-200">16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-200">16</span></span>     |        |        |        |
| <span data-ttu-id="dd3c2-201">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="dd3c2-201">GL\_RGBA</span></span>                 |        |        |        |        |        |        |
| <span data-ttu-id="dd3c2-202">GL \_ RGBA2</span><span class="sxs-lookup"><span data-stu-id="dd3c2-202">GL\_RGBA2</span></span>                | <span data-ttu-id="dd3c2-203">2</span><span class="sxs-lookup"><span data-stu-id="dd3c2-203">2</span></span>      | <span data-ttu-id="dd3c2-204">2</span><span class="sxs-lookup"><span data-stu-id="dd3c2-204">2</span></span>      | <span data-ttu-id="dd3c2-205">2</span><span class="sxs-lookup"><span data-stu-id="dd3c2-205">2</span></span>      | <span data-ttu-id="dd3c2-206">2</span><span class="sxs-lookup"><span data-stu-id="dd3c2-206">2</span></span>      |        |        |
| <span data-ttu-id="dd3c2-207">GL \_ RGBA4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-207">GL\_RGBA4</span></span>                | <span data-ttu-id="dd3c2-208">4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-208">4</span></span>      | <span data-ttu-id="dd3c2-209">4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-209">4</span></span>      | <span data-ttu-id="dd3c2-210">4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-210">4</span></span>      | <span data-ttu-id="dd3c2-211">4</span><span class="sxs-lookup"><span data-stu-id="dd3c2-211">4</span></span>      |        |        |
| <span data-ttu-id="dd3c2-212">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="dd3c2-212">GL\_RGB5\_A1</span></span>             | <span data-ttu-id="dd3c2-213">5</span><span class="sxs-lookup"><span data-stu-id="dd3c2-213">5</span></span>      | <span data-ttu-id="dd3c2-214">5</span><span class="sxs-lookup"><span data-stu-id="dd3c2-214">5</span></span>      | <span data-ttu-id="dd3c2-215">5</span><span class="sxs-lookup"><span data-stu-id="dd3c2-215">5</span></span>      | <span data-ttu-id="dd3c2-216">1</span><span class="sxs-lookup"><span data-stu-id="dd3c2-216">1</span></span>      |        |        |
| <span data-ttu-id="dd3c2-217">GL \_ RGBA8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-217">GL\_RGBA8</span></span>                | <span data-ttu-id="dd3c2-218">8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-218">8</span></span>      | <span data-ttu-id="dd3c2-219">8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-219">8</span></span>      | <span data-ttu-id="dd3c2-220">8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-220">8</span></span>      | <span data-ttu-id="dd3c2-221">8</span><span class="sxs-lookup"><span data-stu-id="dd3c2-221">8</span></span>      |        |        |
| <span data-ttu-id="dd3c2-222">GL \_ RGB10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="dd3c2-222">GL\_RGB10\_A2</span></span>            | <span data-ttu-id="dd3c2-223">10</span><span class="sxs-lookup"><span data-stu-id="dd3c2-223">10</span></span>     | <span data-ttu-id="dd3c2-224">10</span><span class="sxs-lookup"><span data-stu-id="dd3c2-224">10</span></span>     | <span data-ttu-id="dd3c2-225">10</span><span class="sxs-lookup"><span data-stu-id="dd3c2-225">10</span></span>     | <span data-ttu-id="dd3c2-226">2</span><span class="sxs-lookup"><span data-stu-id="dd3c2-226">2</span></span>      |        |        |
| <span data-ttu-id="dd3c2-227">GL \_ RGBA12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-227">GL\_RGBA12</span></span>               | <span data-ttu-id="dd3c2-228">12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-228">12</span></span>     | <span data-ttu-id="dd3c2-229">12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-229">12</span></span>     | <span data-ttu-id="dd3c2-230">12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-230">12</span></span>     | <span data-ttu-id="dd3c2-231">12</span><span class="sxs-lookup"><span data-stu-id="dd3c2-231">12</span></span>     |        |        |
| <span data-ttu-id="dd3c2-232">GL \_ RGBA16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-232">GL\_RGBA16</span></span>               | <span data-ttu-id="dd3c2-233">16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-233">16</span></span>     | <span data-ttu-id="dd3c2-234">16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-234">16</span></span>     | <span data-ttu-id="dd3c2-235">16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-235">16</span></span>     | <span data-ttu-id="dd3c2-236">16</span><span class="sxs-lookup"><span data-stu-id="dd3c2-236">16</span></span>     |        |        |



 

</dd> <dt>

<span data-ttu-id="dd3c2-237">*x*</span><span class="sxs-lookup"><span data-stu-id="dd3c2-237">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="dd3c2-238">Die x-Ebenen-Koordinate der unteren linken Ecke des rechteckigen Bereichs, der kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-238">The window x-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="dd3c2-239">*y*</span><span class="sxs-lookup"><span data-stu-id="dd3c2-239">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="dd3c2-240">Die y-ebenenkoordinate des Fensters der unteren linken Ecke des rechteckigen Bereichs von Pixeln, die kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-240">The window y-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="dd3c2-241">*width*</span><span class="sxs-lookup"><span data-stu-id="dd3c2-241">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="dd3c2-242">Die Breite des Textur Bilds.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-242">The width of the texture image.</span></span> <span data-ttu-id="dd3c2-243">Muss \* für eine Ganzzahl *n* den 2N *+ 2-* Rahmen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-243">Must be 2n + 2 \* *border* for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="dd3c2-244">*height*</span><span class="sxs-lookup"><span data-stu-id="dd3c2-244">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="dd3c2-245">Die Höhe des Textur Bilds.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-245">The height of the texture image.</span></span> <span data-ttu-id="dd3c2-246">Muss \* für eine Ganzzahl *n* den 2N *+ 2-* Rahmen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-246">Must be 2n + 2 \* *border* for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="dd3c2-247">*Aun*</span><span class="sxs-lookup"><span data-stu-id="dd3c2-247">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="dd3c2-248">Die Breite des Rahmens.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-248">The width of the border.</span></span> <span data-ttu-id="dd3c2-249">Muss entweder NULL oder 1 sein.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-249">Must be either zero or 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd3c2-250">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd3c2-250">Return value</span></span>

<span data-ttu-id="dd3c2-251">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-251">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dd3c2-252">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="dd3c2-252">Error codes</span></span>

<span data-ttu-id="dd3c2-253">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-253">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="dd3c2-254">Name</span><span class="sxs-lookup"><span data-stu-id="dd3c2-254">Name</span></span>                                                                                                  | <span data-ttu-id="dd3c2-255">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dd3c2-255">Meaning</span></span>                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dd3c2-256"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd3c2-256"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="dd3c2-257">Das *Ziel* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-257">*target* was not an accepted value.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="dd3c2-258"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="dd3c2-258"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="dd3c2-259">die *Ebene* war kleiner als 0 (null) oder größer als log2 *Max*, wobei *Max* der zurückgegebene Wert von GL \_ Max \_ Texture \_ size ist.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-259">*level* was less than zero or greater than log2 *max*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                               |
| <dl> <span data-ttu-id="dd3c2-260"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="dd3c2-260"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="dd3c2-261">der *Rahmen war nicht* 0 (null) oder 1.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-261">*border* was not zero or 1.</span></span><br/>                                                                                                                       |
| <dl> <span data-ttu-id="dd3c2-262"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="dd3c2-262"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="dd3c2-263">*Breite* war kleiner als 0 (null), größer als 2 + gl \_ Maximale \_ Textur \_ Größe, oder *Breite* kann nicht als 2N + 2-Rahmen \*  für eine Ganzzahl *n* dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-263">*width* was less than zero, greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or *width* cannot be represented as 2n + 2 \* *border* for some integer *n*.</span></span><br/> |
| <dl> <span data-ttu-id="dd3c2-264"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="dd3c2-264"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="dd3c2-265">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-265">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="dd3c2-266">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd3c2-266">Remarks</span></span>

<span data-ttu-id="dd3c2-267">Die **glCopyTexImage2D** -Funktion definiert ein zweidimensionales Textur Bild mithilfe von Pixeln aus dem aktuellen Framebuffer, nicht aus dem Hauptspeicher, wie es bei [**glTexImage2D**](glteximage2d.md)der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-267">The **glCopyTexImage2D** function defines a two-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexImage2D**](glteximage2d.md).</span></span>

<span data-ttu-id="dd3c2-268">Mithilfe der mit der- *Ebene* angegebenen MipMap-Ebene werden Textur Arrays als Rechteck von Pixeln definiert, wobei sich die untere linke Ecke an den Koordinaten *x* und *y*, Width gleich *Width* + (2 \* *Border*) und Height gleich *height* + (2 \* *Border*) befindet.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-268">Using the mipmap level specified with *level*, texture arrays are defined as a rectangle of pixels with the lower-left corner located at the coordinates *x* and *y*, width equal to *width* + (2 \* *border*), and a height equal to *height* + (2 \* *border*).</span></span> <span data-ttu-id="dd3c2-269">Das interne Format des Textur Arrays wird mit dem *internalformat* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-269">The internal format of the texture array is specified with the *internalFormat* parameter.</span></span>

<span data-ttu-id="dd3c2-270">Die **glCopyTexImage2D** -Funktion verarbeitet die Pixel in einer Zeile auf die gleiche Weise wie [**glcopypixels**](glcopypixels.md) , mit dem Unterschied, dass vor der abschließenden Konvertierung der Pixel alle Pixel Komponenten Werte an den Bereich \[ 0, 1 gebunden \] und in das interne Format der Textur für die Speicherung im Textur Array konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-270">The **glCopyTexImage2D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md) except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="dd3c2-271">Die Pixel Reihenfolge wird mit niedrigeren *x* -und *y* -Koordinaten bestimmt, die den unteren *s* -und *t* -Texturkoordinaten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-271">Pixel ordering is determined with lower *x* and *y* coordinates corresponding to lower *s* and *t* texture coordinates.</span></span> <span data-ttu-id="dd3c2-272">Wenn eine der Pixel innerhalb einer angegebenen Zeile des aktuellen Frame Puffer außerhalb des Fensters liegt, das dem aktuellen renderingkontext zugeordnet ist, sind ihre Werte nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-272">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="dd3c2-273">Sie können **glCopyTexImage2D** -Aufrufe nicht in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-273">You cannot include calls to **glCopyTexImage2D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="dd3c2-274">Die **glCopyTexImage2D** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-274">The **glCopyTexImage2D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="dd3c2-275">Die Texturierung hat keine Auswirkung auf den Farb Index Modus.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-275">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="dd3c2-276">Die Funktionen " [**glpixelstore**](glpixelstore-functions.md) " und " [**glpixeltransfer**](glpixeltransfer.md) " wirken sich auf Textur Bilder genau so aus, wie Sie sich auf [**gldrawpixels**](gldrawpixels.md)auswirken</span><span class="sxs-lookup"><span data-stu-id="dd3c2-276">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="dd3c2-277">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glCopyTexImage2D** ab:</span><span class="sxs-lookup"><span data-stu-id="dd3c2-277">The following function retrieves information related to **glCopyTexImage2D**:</span></span>

<span data-ttu-id="dd3c2-278">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Textur \_ 2D</span><span class="sxs-lookup"><span data-stu-id="dd3c2-278">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="dd3c2-279">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd3c2-279">Requirements</span></span>



| <span data-ttu-id="dd3c2-280">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd3c2-280">Requirement</span></span> | <span data-ttu-id="dd3c2-281">Wert</span><span class="sxs-lookup"><span data-stu-id="dd3c2-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd3c2-282">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd3c2-282">Minimum supported client</span></span><br/> | <span data-ttu-id="dd3c2-283">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd3c2-283">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dd3c2-284">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd3c2-284">Minimum supported server</span></span><br/> | <span data-ttu-id="dd3c2-285">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd3c2-285">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dd3c2-286">Header</span><span class="sxs-lookup"><span data-stu-id="dd3c2-286">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd3c2-287"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd3c2-287"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="dd3c2-288">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dd3c2-288">Library</span></span><br/>                  | <dl> <span data-ttu-id="dd3c2-289"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd3c2-289"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dd3c2-290">DLL</span><span class="sxs-lookup"><span data-stu-id="dd3c2-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd3c2-291"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd3c2-291"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd3c2-292">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd3c2-292">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd3c2-293">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-293">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="dd3c2-294">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-294">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="dd3c2-295">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-295">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="dd3c2-296">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-296">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="dd3c2-297">**glnebel**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-297">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="dd3c2-298">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-298">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="dd3c2-299">**glpixeltransfer**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-299">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="dd3c2-300">**gltexd**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-300">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="dd3c2-301">**gltexgen**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-301">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="dd3c2-302">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-302">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="dd3c2-303">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-303">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="dd3c2-304">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-304">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





