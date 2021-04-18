---
title: glCopyTexImage1D-Funktion (GL. h)
description: Die glCopyTexImage1D-Funktion kopiert Pixel aus dem Frame Puffer in ein eindimensionales Textur Bild.
ms.assetid: 3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd
keywords:
- glCopyTexImage1D-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63180386c094f0c4e4de0f1a361bc3bcb1c6e5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340349"
---
# <a name="glcopyteximage1d-function"></a><span data-ttu-id="8e1db-104">glCopyTexImage1D-Funktion</span><span class="sxs-lookup"><span data-stu-id="8e1db-104">glCopyTexImage1D function</span></span>

<span data-ttu-id="8e1db-105">Die **glCopyTexImage1D** -Funktion kopiert Pixel aus dem Frame Puffer in ein eindimensionales Textur Bild.</span><span class="sxs-lookup"><span data-stu-id="8e1db-105">The **glCopyTexImage1D** function copies pixels from the framebuffer into a one-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e1db-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e1db-106">Syntax</span></span>


```C++
void WINAPI glCopyTexImage1D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLint   border
);
```



## <a name="parameters"></a><span data-ttu-id="8e1db-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e1db-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e1db-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="8e1db-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="8e1db-109">Das Ziel, für das die Bilddaten geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8e1db-109">The target for which the image data will be changed.</span></span> <span data-ttu-id="8e1db-110">Muss den Wert "GL \_ Texture \_ 1D" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8e1db-110">Must have the value GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="8e1db-111">*level*</span><span class="sxs-lookup"><span data-stu-id="8e1db-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="8e1db-112">Die Detailebene.</span><span class="sxs-lookup"><span data-stu-id="8e1db-112">The level-of-detail number.</span></span> <span data-ttu-id="8e1db-113">Ebene 0 ist das Basis Image.</span><span class="sxs-lookup"><span data-stu-id="8e1db-113">Level 0 is the base image.</span></span> <span data-ttu-id="8e1db-114">Ebene *n* ist das *n*-te MipMap-Reduzierungs Bild.</span><span class="sxs-lookup"><span data-stu-id="8e1db-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="8e1db-115">*internalformat*</span><span class="sxs-lookup"><span data-stu-id="8e1db-115">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="8e1db-116">Das interne Format und die Auflösung der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="8e1db-116">The internal format and resolution of the texture data.</span></span> <span data-ttu-id="8e1db-117">Dieser Parameter muss einen der folgenden symbolischen Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8e1db-117">This parameter must be one of the following symbolic values.</span></span>



| <span data-ttu-id="8e1db-118">Konstante</span><span class="sxs-lookup"><span data-stu-id="8e1db-118">Constant</span></span>                 | <span data-ttu-id="8e1db-119">R-Bits</span><span class="sxs-lookup"><span data-stu-id="8e1db-119">R Bits</span></span> | <span data-ttu-id="8e1db-120">G Bits</span><span class="sxs-lookup"><span data-stu-id="8e1db-120">G Bits</span></span> | <span data-ttu-id="8e1db-121">B Bits</span><span class="sxs-lookup"><span data-stu-id="8e1db-121">B Bits</span></span> | <span data-ttu-id="8e1db-122">Eine Bits</span><span class="sxs-lookup"><span data-stu-id="8e1db-122">A Bits</span></span> | <span data-ttu-id="8e1db-123">L Bits</span><span class="sxs-lookup"><span data-stu-id="8e1db-123">L Bits</span></span> | <span data-ttu-id="8e1db-124">I Bits</span><span class="sxs-lookup"><span data-stu-id="8e1db-124">I Bits</span></span> |
|--------------------------|--------|--------|--------|--------|--------|--------|
| <span data-ttu-id="8e1db-125">GL- \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="8e1db-125">GL\_ALPHA</span></span>                |        |        |        |        |        |        |
| <span data-ttu-id="8e1db-126">GL \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="8e1db-126">GL\_ALPHA4</span></span>               |        |        |        | <span data-ttu-id="8e1db-127">4</span><span class="sxs-lookup"><span data-stu-id="8e1db-127">4</span></span>      |        |        |
| <span data-ttu-id="8e1db-128">GL \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="8e1db-128">GL\_ALPHA8</span></span>               |        |        |        | <span data-ttu-id="8e1db-129">8</span><span class="sxs-lookup"><span data-stu-id="8e1db-129">8</span></span>      |        |        |
| <span data-ttu-id="8e1db-130">GL \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="8e1db-130">GL\_ALPHA12</span></span>              |        |        |        | <span data-ttu-id="8e1db-131">12</span><span class="sxs-lookup"><span data-stu-id="8e1db-131">12</span></span>     |        |        |
| <span data-ttu-id="8e1db-132">GL \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="8e1db-132">GL\_ALPHA16</span></span>              |        |        |        | <span data-ttu-id="8e1db-133">16</span><span class="sxs-lookup"><span data-stu-id="8e1db-133">16</span></span>     |        |        |
| <span data-ttu-id="8e1db-134">GL- \_ Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="8e1db-134">GL\_LUMINANCE</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="8e1db-135">GL \_ LUMINANCE4</span><span class="sxs-lookup"><span data-stu-id="8e1db-135">GL\_LUMINANCE4</span></span>           |        |        |        |        | <span data-ttu-id="8e1db-136">4</span><span class="sxs-lookup"><span data-stu-id="8e1db-136">4</span></span>      |        |
| <span data-ttu-id="8e1db-137">GL \_ LUMINANCE8</span><span class="sxs-lookup"><span data-stu-id="8e1db-137">GL\_LUMINANCE8</span></span>           |        |        |        |        | <span data-ttu-id="8e1db-138">8</span><span class="sxs-lookup"><span data-stu-id="8e1db-138">8</span></span>      |        |
| <span data-ttu-id="8e1db-139">GL \_ LUMINANCE12</span><span class="sxs-lookup"><span data-stu-id="8e1db-139">GL\_LUMINANCE12</span></span>          |        |        |        |        | <span data-ttu-id="8e1db-140">12</span><span class="sxs-lookup"><span data-stu-id="8e1db-140">12</span></span>     |        |
| <span data-ttu-id="8e1db-141">GL \_ LUMINANCE16</span><span class="sxs-lookup"><span data-stu-id="8e1db-141">GL\_LUMINANCE16</span></span>          |        |        |        |        | <span data-ttu-id="8e1db-142">16</span><span class="sxs-lookup"><span data-stu-id="8e1db-142">16</span></span>     |        |
| <span data-ttu-id="8e1db-143">GL- \_ Leuchtkraft \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="8e1db-143">GL\_LUMINANCE\_ALPHA</span></span>     |        |        |        |        |        |        |
| <span data-ttu-id="8e1db-144">GL \_ LUMINANCE4 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="8e1db-144">GL\_LUMINANCE4\_ALPHA4</span></span>   |        |        |        | <span data-ttu-id="8e1db-145">4</span><span class="sxs-lookup"><span data-stu-id="8e1db-145">4</span></span>      | <span data-ttu-id="8e1db-146">4</span><span class="sxs-lookup"><span data-stu-id="8e1db-146">4</span></span>      |        |
| <span data-ttu-id="8e1db-147">GL \_ LUMINANCE6 \_ ALPHA2</span><span class="sxs-lookup"><span data-stu-id="8e1db-147">GL\_LUMINANCE6\_ALPHA2</span></span>   |        |        |        | <span data-ttu-id="8e1db-148">2</span><span class="sxs-lookup"><span data-stu-id="8e1db-148">2</span></span>      | <span data-ttu-id="8e1db-149">6</span><span class="sxs-lookup"><span data-stu-id="8e1db-149">6</span></span>      |        |
| <span data-ttu-id="8e1db-150">GL \_ LUMINANCE8 \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="8e1db-150">GL\_LUMINANCE8\_ALPHA8</span></span>   |        |        |        | <span data-ttu-id="8e1db-151">8</span><span class="sxs-lookup"><span data-stu-id="8e1db-151">8</span></span>      | <span data-ttu-id="8e1db-152">8</span><span class="sxs-lookup"><span data-stu-id="8e1db-152">8</span></span>      |        |
| <span data-ttu-id="8e1db-153">GL \_ LUMINANCE12 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="8e1db-153">GL\_LUMINANCE12\_ALPHA4</span></span>  |        |        |        | <span data-ttu-id="8e1db-154">4</span><span class="sxs-lookup"><span data-stu-id="8e1db-154">4</span></span>      | <span data-ttu-id="8e1db-155">12</span><span class="sxs-lookup"><span data-stu-id="8e1db-155">12</span></span>     |        |
| <span data-ttu-id="8e1db-156">GL \_ LUMINANCE12 \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="8e1db-156">GL\_LUMINANCE12\_ALPHA12</span></span> |        |        |        | <span data-ttu-id="8e1db-157">12</span><span class="sxs-lookup"><span data-stu-id="8e1db-157">12</span></span>     | <span data-ttu-id="8e1db-158">12</span><span class="sxs-lookup"><span data-stu-id="8e1db-158">12</span></span>     |        |
| <span data-ttu-id="8e1db-159">GL \_ LUMINANCE16 \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="8e1db-159">GL\_LUMINANCE16\_ALPHA16</span></span> |        |        |        | <span data-ttu-id="8e1db-160">16</span><span class="sxs-lookup"><span data-stu-id="8e1db-160">16</span></span>     | <span data-ttu-id="8e1db-161">16</span><span class="sxs-lookup"><span data-stu-id="8e1db-161">16</span></span>     |        |
| <span data-ttu-id="8e1db-162">GL- \_ Intensität</span><span class="sxs-lookup"><span data-stu-id="8e1db-162">GL\_INTENSITY</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="8e1db-163">GL \_ INTENSITY4</span><span class="sxs-lookup"><span data-stu-id="8e1db-163">GL\_INTENSITY4</span></span>           |        |        |        |        |        | <span data-ttu-id="8e1db-164">4</span><span class="sxs-lookup"><span data-stu-id="8e1db-164">4</span></span>      |
| <span data-ttu-id="8e1db-165">GL \_ INTENSITY8</span><span class="sxs-lookup"><span data-stu-id="8e1db-165">GL\_INTENSITY8</span></span>           |        |        |        |        |        | <span data-ttu-id="8e1db-166">8</span><span class="sxs-lookup"><span data-stu-id="8e1db-166">8</span></span>      |
| <span data-ttu-id="8e1db-167">GL \_ INTENSITY12</span><span class="sxs-lookup"><span data-stu-id="8e1db-167">GL\_INTENSITY12</span></span>          |        |        |        |        |        | <span data-ttu-id="8e1db-168">12</span><span class="sxs-lookup"><span data-stu-id="8e1db-168">12</span></span>     |
| <span data-ttu-id="8e1db-169">GL \_ INTENSITY16</span><span class="sxs-lookup"><span data-stu-id="8e1db-169">GL\_INTENSITY16</span></span>          |        |        |        |        |        | <span data-ttu-id="8e1db-170">16</span><span class="sxs-lookup"><span data-stu-id="8e1db-170">16</span></span>     |
| <span data-ttu-id="8e1db-171">GL. \_ RGB</span><span class="sxs-lookup"><span data-stu-id="8e1db-171">GL\_RGB</span></span>                  |        |        |        |        |        |        |
| <span data-ttu-id="8e1db-172">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="8e1db-172">GL\_R3\_G3\_B2</span></span>           | <span data-ttu-id="8e1db-173">3</span><span class="sxs-lookup"><span data-stu-id="8e1db-173">3</span></span>      | <span data-ttu-id="8e1db-174">3</span><span class="sxs-lookup"><span data-stu-id="8e1db-174">3</span></span>      | <span data-ttu-id="8e1db-175">2</span><span class="sxs-lookup"><span data-stu-id="8e1db-175">2</span></span>      |        |        |        |
| <span data-ttu-id="8e1db-176">GL \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="8e1db-176">GL\_RGB4</span></span>                 | <span data-ttu-id="8e1db-177">4</span><span class="sxs-lookup"><span data-stu-id="8e1db-177">4</span></span>      | <span data-ttu-id="8e1db-178">4</span><span class="sxs-lookup"><span data-stu-id="8e1db-178">4</span></span>      | <span data-ttu-id="8e1db-179">4</span><span class="sxs-lookup"><span data-stu-id="8e1db-179">4</span></span>      |        |        |        |
| <span data-ttu-id="8e1db-180">GL \_ RGB5</span><span class="sxs-lookup"><span data-stu-id="8e1db-180">GL\_RGB5</span></span>                 | <span data-ttu-id="8e1db-181">5</span><span class="sxs-lookup"><span data-stu-id="8e1db-181">5</span></span>      | <span data-ttu-id="8e1db-182">5</span><span class="sxs-lookup"><span data-stu-id="8e1db-182">5</span></span>      | <span data-ttu-id="8e1db-183">5</span><span class="sxs-lookup"><span data-stu-id="8e1db-183">5</span></span>      |        |        |        |
| <span data-ttu-id="8e1db-184">GL \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="8e1db-184">GL\_RGB8</span></span>                 | <span data-ttu-id="8e1db-185">8</span><span class="sxs-lookup"><span data-stu-id="8e1db-185">8</span></span>      | <span data-ttu-id="8e1db-186">8</span><span class="sxs-lookup"><span data-stu-id="8e1db-186">8</span></span>      | <span data-ttu-id="8e1db-187">8</span><span class="sxs-lookup"><span data-stu-id="8e1db-187">8</span></span>      |        |        |        |
| <span data-ttu-id="8e1db-188">GL \_ RGB10</span><span class="sxs-lookup"><span data-stu-id="8e1db-188">GL\_RGB10</span></span>                | <span data-ttu-id="8e1db-189">10</span><span class="sxs-lookup"><span data-stu-id="8e1db-189">10</span></span>     | <span data-ttu-id="8e1db-190">10</span><span class="sxs-lookup"><span data-stu-id="8e1db-190">10</span></span>     | <span data-ttu-id="8e1db-191">10</span><span class="sxs-lookup"><span data-stu-id="8e1db-191">10</span></span>     |        |        |        |
| <span data-ttu-id="8e1db-192">GL \_ RGB12</span><span class="sxs-lookup"><span data-stu-id="8e1db-192">GL\_RGB12</span></span>                | <span data-ttu-id="8e1db-193">12</span><span class="sxs-lookup"><span data-stu-id="8e1db-193">12</span></span>     | <span data-ttu-id="8e1db-194">12</span><span class="sxs-lookup"><span data-stu-id="8e1db-194">12</span></span>     | <span data-ttu-id="8e1db-195">12</span><span class="sxs-lookup"><span data-stu-id="8e1db-195">12</span></span>     |        |        |        |
| <span data-ttu-id="8e1db-196">GL \_ RGB16</span><span class="sxs-lookup"><span data-stu-id="8e1db-196">GL\_RGB16</span></span>                | <span data-ttu-id="8e1db-197">16</span><span class="sxs-lookup"><span data-stu-id="8e1db-197">16</span></span>     | <span data-ttu-id="8e1db-198">16</span><span class="sxs-lookup"><span data-stu-id="8e1db-198">16</span></span>     | <span data-ttu-id="8e1db-199">16</span><span class="sxs-lookup"><span data-stu-id="8e1db-199">16</span></span>     |        |        |        |
| <span data-ttu-id="8e1db-200">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="8e1db-200">GL\_RGBA</span></span>                 |        |        |        |        |        |        |
| <span data-ttu-id="8e1db-201">GL \_ RGBA2</span><span class="sxs-lookup"><span data-stu-id="8e1db-201">GL\_RGBA2</span></span>                | <span data-ttu-id="8e1db-202">2</span><span class="sxs-lookup"><span data-stu-id="8e1db-202">2</span></span>      | <span data-ttu-id="8e1db-203">2</span><span class="sxs-lookup"><span data-stu-id="8e1db-203">2</span></span>      | <span data-ttu-id="8e1db-204">2</span><span class="sxs-lookup"><span data-stu-id="8e1db-204">2</span></span>      | <span data-ttu-id="8e1db-205">2</span><span class="sxs-lookup"><span data-stu-id="8e1db-205">2</span></span>      |        |        |
| <span data-ttu-id="8e1db-206">GL \_ RGBA4</span><span class="sxs-lookup"><span data-stu-id="8e1db-206">GL\_RGBA4</span></span>                | <span data-ttu-id="8e1db-207">4</span><span class="sxs-lookup"><span data-stu-id="8e1db-207">4</span></span>      | <span data-ttu-id="8e1db-208">4</span><span class="sxs-lookup"><span data-stu-id="8e1db-208">4</span></span>      | <span data-ttu-id="8e1db-209">4</span><span class="sxs-lookup"><span data-stu-id="8e1db-209">4</span></span>      | <span data-ttu-id="8e1db-210">4</span><span class="sxs-lookup"><span data-stu-id="8e1db-210">4</span></span>      |        |        |
| <span data-ttu-id="8e1db-211">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="8e1db-211">GL\_RGB5\_A1</span></span>             | <span data-ttu-id="8e1db-212">5</span><span class="sxs-lookup"><span data-stu-id="8e1db-212">5</span></span>      | <span data-ttu-id="8e1db-213">5</span><span class="sxs-lookup"><span data-stu-id="8e1db-213">5</span></span>      | <span data-ttu-id="8e1db-214">5</span><span class="sxs-lookup"><span data-stu-id="8e1db-214">5</span></span>      | <span data-ttu-id="8e1db-215">1</span><span class="sxs-lookup"><span data-stu-id="8e1db-215">1</span></span>      |        |        |
| <span data-ttu-id="8e1db-216">GL \_ RGBA8</span><span class="sxs-lookup"><span data-stu-id="8e1db-216">GL\_RGBA8</span></span>                | <span data-ttu-id="8e1db-217">8</span><span class="sxs-lookup"><span data-stu-id="8e1db-217">8</span></span>      | <span data-ttu-id="8e1db-218">8</span><span class="sxs-lookup"><span data-stu-id="8e1db-218">8</span></span>      | <span data-ttu-id="8e1db-219">8</span><span class="sxs-lookup"><span data-stu-id="8e1db-219">8</span></span>      | <span data-ttu-id="8e1db-220">8</span><span class="sxs-lookup"><span data-stu-id="8e1db-220">8</span></span>      |        |        |
| <span data-ttu-id="8e1db-221">GL \_ RGB10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="8e1db-221">GL\_RGB10\_A2</span></span>            | <span data-ttu-id="8e1db-222">10</span><span class="sxs-lookup"><span data-stu-id="8e1db-222">10</span></span>     | <span data-ttu-id="8e1db-223">10</span><span class="sxs-lookup"><span data-stu-id="8e1db-223">10</span></span>     | <span data-ttu-id="8e1db-224">10</span><span class="sxs-lookup"><span data-stu-id="8e1db-224">10</span></span>     | <span data-ttu-id="8e1db-225">2</span><span class="sxs-lookup"><span data-stu-id="8e1db-225">2</span></span>      |        |        |
| <span data-ttu-id="8e1db-226">GL \_ RGBA12</span><span class="sxs-lookup"><span data-stu-id="8e1db-226">GL\_RGBA12</span></span>               | <span data-ttu-id="8e1db-227">12</span><span class="sxs-lookup"><span data-stu-id="8e1db-227">12</span></span>     | <span data-ttu-id="8e1db-228">12</span><span class="sxs-lookup"><span data-stu-id="8e1db-228">12</span></span>     | <span data-ttu-id="8e1db-229">12</span><span class="sxs-lookup"><span data-stu-id="8e1db-229">12</span></span>     | <span data-ttu-id="8e1db-230">12</span><span class="sxs-lookup"><span data-stu-id="8e1db-230">12</span></span>     |        |        |
| <span data-ttu-id="8e1db-231">GL \_ RGBA16</span><span class="sxs-lookup"><span data-stu-id="8e1db-231">GL\_RGBA16</span></span>               | <span data-ttu-id="8e1db-232">16</span><span class="sxs-lookup"><span data-stu-id="8e1db-232">16</span></span>     | <span data-ttu-id="8e1db-233">16</span><span class="sxs-lookup"><span data-stu-id="8e1db-233">16</span></span>     | <span data-ttu-id="8e1db-234">16</span><span class="sxs-lookup"><span data-stu-id="8e1db-234">16</span></span>     | <span data-ttu-id="8e1db-235">16</span><span class="sxs-lookup"><span data-stu-id="8e1db-235">16</span></span>     |        |        |



 

</dd> <dt>

<span data-ttu-id="8e1db-236">*x*</span><span class="sxs-lookup"><span data-stu-id="8e1db-236">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="8e1db-237">Die x-Ebenen-Koordinate der unteren linken Ecke der Zeile der zu kopierenden Pixel.</span><span class="sxs-lookup"><span data-stu-id="8e1db-237">The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="8e1db-238">*y*</span><span class="sxs-lookup"><span data-stu-id="8e1db-238">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="8e1db-239">Die y-ebenenkoordinate des Fensters der unteren linken Ecke der Zeile der zu kopierenden Pixel.</span><span class="sxs-lookup"><span data-stu-id="8e1db-239">The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="8e1db-240">*width*</span><span class="sxs-lookup"><span data-stu-id="8e1db-240">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="8e1db-241">Die Breite des Textur Bilds.</span><span class="sxs-lookup"><span data-stu-id="8e1db-241">The width of the texture image.</span></span> <span data-ttu-id="8e1db-242">Muss NULL oder 2N + 2 (*Border*) für eine ganze Zahl *n* sein.</span><span class="sxs-lookup"><span data-stu-id="8e1db-242">Must be zero or 2n + 2(*border*) for some integer *n*.</span></span> <span data-ttu-id="8e1db-243">Die Höhe des Textur Bilds ist 1.</span><span class="sxs-lookup"><span data-stu-id="8e1db-243">The height of the texture image is 1.</span></span>

</dd> <dt>

<span data-ttu-id="8e1db-244">*Aun*</span><span class="sxs-lookup"><span data-stu-id="8e1db-244">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="8e1db-245">Die Breite des Rahmens.</span><span class="sxs-lookup"><span data-stu-id="8e1db-245">The width of the border.</span></span> <span data-ttu-id="8e1db-246">Muss entweder NULL oder 1 sein.</span><span class="sxs-lookup"><span data-stu-id="8e1db-246">Must be either zero or 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e1db-247">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e1db-247">Return value</span></span>

<span data-ttu-id="8e1db-248">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8e1db-248">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8e1db-249">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="8e1db-249">Error codes</span></span>

<span data-ttu-id="8e1db-250">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8e1db-250">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8e1db-251">Name</span><span class="sxs-lookup"><span data-stu-id="8e1db-251">Name</span></span>                                                                                                  | <span data-ttu-id="8e1db-252">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8e1db-252">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8e1db-253"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8e1db-253"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8e1db-254">Das *Ziel* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="8e1db-254">*target* was not an accepted value.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="8e1db-255"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="8e1db-255"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="8e1db-256">die *Ebene* war kleiner als 0 (null) oder größer als log2 *Max*, wobei *Max* der zurückgegebene Wert von GL \_ Max \_ Texture \_ size ist.</span><span class="sxs-lookup"><span data-stu-id="8e1db-256">*level* was less than zero or greater than log2 *max*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                           |
| <dl> <span data-ttu-id="8e1db-257"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="8e1db-257"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="8e1db-258">der *Rahmen war nicht* 0 (null) oder 1.</span><span class="sxs-lookup"><span data-stu-id="8e1db-258">*border* was not zero or 1.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="8e1db-259"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="8e1db-259"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="8e1db-260">*Breite* war kleiner als 0 (null), größer als 2 + gl \_ Maximale \_ Textur \_ Größe, oder *Breite* kann nicht als 2n + (*Border*) für eine Ganzzahl *n* dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8e1db-260">*width* was less than zero, greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or *width* cannot be represented as 2n +(*border*) for some integer *n*.</span></span><br/> |
| <dl> <span data-ttu-id="8e1db-261"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="8e1db-261"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8e1db-262">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8e1db-262">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                    |



## <a name="remarks"></a><span data-ttu-id="8e1db-263">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e1db-263">Remarks</span></span>

<span data-ttu-id="8e1db-264">Die **glCopyTexImage1D** -Funktion definiert ein eindimensionales Textur Bild mithilfe von Pixel aus dem aktuellen Framebuffer, nicht aus dem Hauptspeicher, wie es bei [**glTexImage1D**](glteximage1d.md)der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="8e1db-264">The **glCopyTexImage1D** function defines a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexImage1D**](glteximage1d.md).</span></span>

<span data-ttu-id="8e1db-265">Mithilfe der mit *Level* angegebenen MipMap-Ebene werden Textur Arrays als Pixel Zeile definiert, die an der unteren linken Ecke des Fensters an den durch *x* und *y* angegebenen Koordinaten ausgerichtet ist, wobei die Länge gleich dem Rahmen der *Breite* + 2 ist \* .</span><span class="sxs-lookup"><span data-stu-id="8e1db-265">Using the mipmap level specified with *level*, texture arrays are defined as a pixel row aligned with the lower-left corner of the window at the coordinates specified by *x* and *y*, with a length equal to *width* + 2 \* *border*.</span></span> <span data-ttu-id="8e1db-266">Das interne Format des Textur Arrays wird mit dem *internalformat* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="8e1db-266">The internal format of the texture array is specified with the *internalFormat* parameter.</span></span>

<span data-ttu-id="8e1db-267">Die **glCopyTexImage1D** -Funktion verarbeitet die Pixel in einer Zeile auf die gleiche Weise wie [**glcopypixels**](glcopypixels.md), mit dem Unterschied, dass vor der abschließenden Konvertierung der Pixel alle Pixel Komponenten Werte an den Bereich \[ 0, 1 gebunden und in das \] interne Format der Textur für die Speicherung im Textur Array konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="8e1db-267">The **glCopyTexImage1D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md), except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="8e1db-268">Die Pixel Reihenfolge wird mit niedrigeren *x* -Koordinaten bestimmt, die den unteren Texturkoordinaten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8e1db-268">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="8e1db-269">Wenn eine der Pixel innerhalb einer angegebenen Zeile des aktuellen Frame Puffer außerhalb des Fensters liegt, das dem aktuellen renderingkontext zugeordnet ist, sind ihre Werte nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="8e1db-269">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="8e1db-270">Sie können **glCopyTexImage1D** -Aufrufe nicht in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="8e1db-270">You cannot include calls to **glCopyTexImage1D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="8e1db-271">Die **glCopyTexImage1D** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8e1db-271">The **glCopyTexImage1D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="8e1db-272">Die Texturierung hat keine Auswirkung auf den Farb Index Modus.</span><span class="sxs-lookup"><span data-stu-id="8e1db-272">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="8e1db-273">Die Funktionen " [**glpixelstore**](glpixelstore-functions.md) " und " [**glpixeltransfer**](glpixeltransfer.md) " wirken sich auf Textur Bilder genau so aus, wie Sie sich auf [**gldrawpixels**](gldrawpixels.md)auswirken</span><span class="sxs-lookup"><span data-stu-id="8e1db-273">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="8e1db-274">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glCopyTexImage1D** ab:</span><span class="sxs-lookup"><span data-stu-id="8e1db-274">The following function retrieves information related to **glCopyTexImage1D**:</span></span>

<span data-ttu-id="8e1db-275">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Texture \_ 1D</span><span class="sxs-lookup"><span data-stu-id="8e1db-275">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="8e1db-276">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e1db-276">Requirements</span></span>



| <span data-ttu-id="8e1db-277">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e1db-277">Requirement</span></span> | <span data-ttu-id="8e1db-278">Wert</span><span class="sxs-lookup"><span data-stu-id="8e1db-278">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e1db-279">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e1db-279">Minimum supported client</span></span><br/> | <span data-ttu-id="8e1db-280">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e1db-280">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8e1db-281">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e1db-281">Minimum supported server</span></span><br/> | <span data-ttu-id="8e1db-282">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e1db-282">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8e1db-283">Header</span><span class="sxs-lookup"><span data-stu-id="8e1db-283">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e1db-284"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e1db-284"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8e1db-285">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8e1db-285">Library</span></span><br/>                  | <dl> <span data-ttu-id="8e1db-286"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e1db-286"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8e1db-287">DLL</span><span class="sxs-lookup"><span data-stu-id="8e1db-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e1db-288"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e1db-288"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e1db-289">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e1db-289">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e1db-290">**glcopypixels**</span><span class="sxs-lookup"><span data-stu-id="8e1db-290">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="8e1db-291">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="8e1db-291">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="8e1db-292">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="8e1db-292">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="8e1db-293">**glnebel**</span><span class="sxs-lookup"><span data-stu-id="8e1db-293">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="8e1db-294">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="8e1db-294">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="8e1db-295">**glpixeltransfer**</span><span class="sxs-lookup"><span data-stu-id="8e1db-295">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="8e1db-296">**gltexd**</span><span class="sxs-lookup"><span data-stu-id="8e1db-296">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="8e1db-297">**gltexgen**</span><span class="sxs-lookup"><span data-stu-id="8e1db-297">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="8e1db-298">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="8e1db-298">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="8e1db-299">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="8e1db-299">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="8e1db-300">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="8e1db-300">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





