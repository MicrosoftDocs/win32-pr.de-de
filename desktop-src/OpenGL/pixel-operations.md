---
title: Pixel Vorgänge
description: Pixel Vorgänge
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- Pixel Vorgänge OpenGL
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda15342b246ba979bdbe60184eeb632368f36b4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857275"
---
# <a name="pixel-operations"></a><span data-ttu-id="ef0fa-104">Pixel Vorgänge</span><span class="sxs-lookup"><span data-stu-id="ef0fa-104">Pixel Operations</span></span>

<dl> <span data-ttu-id="ef0fa-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL- \_ Scissor- \_ Test</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL\_SCISSOR\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="ef0fa-106">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-106">Description:</span></span>     | <span data-ttu-id="ef0fa-107">Scissoring aktiviert</span><span class="sxs-lookup"><span data-stu-id="ef0fa-107">Scissoring enabled</span></span>                 |
| <span data-ttu-id="ef0fa-108">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-108">Attribute group:</span></span> | <span data-ttu-id="ef0fa-109">Scissor/enable</span><span class="sxs-lookup"><span data-stu-id="ef0fa-109">scissor/enable</span></span>                     |
| <span data-ttu-id="ef0fa-110">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-110">Initial value:</span></span>   | <span data-ttu-id="ef0fa-111">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="ef0fa-111">GL\_FALSE</span></span>                          |
| <span data-ttu-id="ef0fa-112">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-112">Get command:</span></span>     | [<span data-ttu-id="ef0fa-113">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-113">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="ef0fa-114"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>Feld "GL \_ Scissor" \_</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-114"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL\_SCISSOR\_BOX</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef0fa-115">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-115">Description:</span></span>     | <span data-ttu-id="ef0fa-116">Scissor-Feld</span><span class="sxs-lookup"><span data-stu-id="ef0fa-116">Scissor box</span></span>                                                                      |
| <span data-ttu-id="ef0fa-117">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-117">Attribute group:</span></span> | <span data-ttu-id="ef0fa-118">Scheren</span><span class="sxs-lookup"><span data-stu-id="ef0fa-118">scissor</span></span>                                                                          |
| <span data-ttu-id="ef0fa-119">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-119">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="ef0fa-120">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-120">Get command:</span></span>     | [<span data-ttu-id="ef0fa-121">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ef0fa-122"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL- \_ Schablonen \_ Test</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-122"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL\_STENCIL\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="ef0fa-123">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-123">Description:</span></span>     | <span data-ttu-id="ef0fa-124">Aktivierte Schablone</span><span class="sxs-lookup"><span data-stu-id="ef0fa-124">Stenciling enabled</span></span>                 |
| <span data-ttu-id="ef0fa-125">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-125">Attribute group:</span></span> | <span data-ttu-id="ef0fa-126">Schablone-Puffer/aktivieren</span><span class="sxs-lookup"><span data-stu-id="ef0fa-126">stencil-buffer/enable</span></span>              |
| <span data-ttu-id="ef0fa-127">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-127">Initial value:</span></span>   | <span data-ttu-id="ef0fa-128">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="ef0fa-128">GL\_FALSE</span></span>                          |
| <span data-ttu-id="ef0fa-129">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-129">Get command:</span></span>     | [<span data-ttu-id="ef0fa-130">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-130">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="ef0fa-131"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL- \_ Schablone \_ Func</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-131"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL\_STENCIL\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef0fa-132">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-132">Description:</span></span>     | <span data-ttu-id="ef0fa-133">Schablone-Funktion</span><span class="sxs-lookup"><span data-stu-id="ef0fa-133">Stencil function</span></span>                                                                 |
| <span data-ttu-id="ef0fa-134">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-134">Attribute group:</span></span> | <span data-ttu-id="ef0fa-135">Schablone-Puffer</span><span class="sxs-lookup"><span data-stu-id="ef0fa-135">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="ef0fa-136">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-136">Initial value:</span></span>   | <span data-ttu-id="ef0fa-137">immer GL. \_</span><span class="sxs-lookup"><span data-stu-id="ef0fa-137">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="ef0fa-138">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-138">Get command:</span></span>     | [<span data-ttu-id="ef0fa-139">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-139">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ef0fa-140"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL- \_ Schablonen \_ Wert \_ Maske</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-140"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL\_STENCIL\_VALUE\_MASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef0fa-141">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-141">Description:</span></span>     | <span data-ttu-id="ef0fa-142">Schablonen Maske</span><span class="sxs-lookup"><span data-stu-id="ef0fa-142">Stencil mask</span></span>                                                                     |
| <span data-ttu-id="ef0fa-143">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-143">Attribute group:</span></span> | <span data-ttu-id="ef0fa-144">Schablone-Puffer</span><span class="sxs-lookup"><span data-stu-id="ef0fa-144">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="ef0fa-145">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-145">Initial value:</span></span>   | <span data-ttu-id="ef0fa-146">1</span><span class="sxs-lookup"><span data-stu-id="ef0fa-146">1's</span></span>                                                                              |
| <span data-ttu-id="ef0fa-147">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-147">Get command:</span></span>     | [<span data-ttu-id="ef0fa-148">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ef0fa-149"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL- \_ Schablone \_ Ref</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-149"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL\_STENCIL\_REF</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef0fa-150">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-150">Description:</span></span>     | <span data-ttu-id="ef0fa-151">Schablonen Referenzwert</span><span class="sxs-lookup"><span data-stu-id="ef0fa-151">Stencil reference value</span></span>                                                          |
| <span data-ttu-id="ef0fa-152">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-152">Attribute group:</span></span> | <span data-ttu-id="ef0fa-153">Schablone-Puffer</span><span class="sxs-lookup"><span data-stu-id="ef0fa-153">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="ef0fa-154">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-154">Initial value:</span></span>   | <span data-ttu-id="ef0fa-155">0</span><span class="sxs-lookup"><span data-stu-id="ef0fa-155">0</span></span>                                                                                |
| <span data-ttu-id="ef0fa-156">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-156">Get command:</span></span>     | [<span data-ttu-id="ef0fa-157">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-157">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ef0fa-158"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL- \_ Schablone \_ schlägt fehl</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-158"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL\_STENCIL\_FAIL</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef0fa-159">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-159">Description:</span></span>     | <span data-ttu-id="ef0fa-160">Schablone-Fehler Aktion</span><span class="sxs-lookup"><span data-stu-id="ef0fa-160">Stencil fail action</span></span>                                                              |
| <span data-ttu-id="ef0fa-161">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-161">Attribute group:</span></span> | <span data-ttu-id="ef0fa-162">Schablone-Puffer</span><span class="sxs-lookup"><span data-stu-id="ef0fa-162">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="ef0fa-163">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-163">Initial value:</span></span>   | <span data-ttu-id="ef0fa-164">GL \_ beibehalten</span><span class="sxs-lookup"><span data-stu-id="ef0fa-164">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="ef0fa-165">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-165">Get command:</span></span>     | [<span data-ttu-id="ef0fa-166">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-166">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ef0fa-167"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>Fehler beim Übergeben der GL- \_ Schablone \_ \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-167"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL\_STENCIL\_PASS\_DEPTH\_FAIL</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef0fa-168">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-168">Description:</span></span>     | <span data-ttu-id="ef0fa-169">Aktion für Schablone-tiefen Puffer Fehler</span><span class="sxs-lookup"><span data-stu-id="ef0fa-169">Stencil depth buffer fail action</span></span>                                                 |
| <span data-ttu-id="ef0fa-170">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-170">Attribute group:</span></span> | <span data-ttu-id="ef0fa-171">Schablone-Puffer</span><span class="sxs-lookup"><span data-stu-id="ef0fa-171">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="ef0fa-172">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-172">Initial value:</span></span>   | <span data-ttu-id="ef0fa-173">GL \_ beibehalten</span><span class="sxs-lookup"><span data-stu-id="ef0fa-173">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="ef0fa-174">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-174">Get command:</span></span>     | [<span data-ttu-id="ef0fa-175">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ef0fa-176"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>bestandungs Tiefe für GL- \_ Schablone \_ \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-176"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL\_STENCIL\_PASS\_DEPTH\_PASS</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef0fa-177">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-177">Description:</span></span>     | <span data-ttu-id="ef0fa-178">Aktion für Schablone-tiefen Puffer Durchlauf</span><span class="sxs-lookup"><span data-stu-id="ef0fa-178">Stencil depth buffer pass action</span></span>                                                 |
| <span data-ttu-id="ef0fa-179">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-179">Attribute group:</span></span> | <span data-ttu-id="ef0fa-180">Schablone-Puffer</span><span class="sxs-lookup"><span data-stu-id="ef0fa-180">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="ef0fa-181">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-181">Initial value:</span></span>   | <span data-ttu-id="ef0fa-182">GL \_ beibehalten</span><span class="sxs-lookup"><span data-stu-id="ef0fa-182">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="ef0fa-183">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-183">Get command:</span></span>     | [<span data-ttu-id="ef0fa-184">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ef0fa-185"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL- \_ alpha \_ Test</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-185"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL\_ALPHA\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="ef0fa-186">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-186">Description:</span></span>     | <span data-ttu-id="ef0fa-187">Alpha Test aktiviert</span><span class="sxs-lookup"><span data-stu-id="ef0fa-187">Alpha test enabled</span></span>                 |
| <span data-ttu-id="ef0fa-188">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-188">Attribute group:</span></span> | <span data-ttu-id="ef0fa-189">Farb Puffer/-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="ef0fa-189">color-buffer/enable</span></span>                |
| <span data-ttu-id="ef0fa-190">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-190">Initial value:</span></span>   | <span data-ttu-id="ef0fa-191">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="ef0fa-191">GL\_FALSE</span></span>                          |
| <span data-ttu-id="ef0fa-192">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-192">Get command:</span></span>     | [<span data-ttu-id="ef0fa-193">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-193">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="ef0fa-194"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL- \_ alpha \_ Test- \_ Func</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-194"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL\_ALPHA\_TEST\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef0fa-195">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-195">Description:</span></span>     | <span data-ttu-id="ef0fa-196">Alpha-Testfunktion</span><span class="sxs-lookup"><span data-stu-id="ef0fa-196">Alpha test function</span></span>                                                              |
| <span data-ttu-id="ef0fa-197">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-197">Attribute group:</span></span> | <span data-ttu-id="ef0fa-198">Farb Puffer</span><span class="sxs-lookup"><span data-stu-id="ef0fa-198">color-buffer</span></span>                                                                     |
| <span data-ttu-id="ef0fa-199">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-199">Initial value:</span></span>   | <span data-ttu-id="ef0fa-200">immer GL. \_</span><span class="sxs-lookup"><span data-stu-id="ef0fa-200">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="ef0fa-201">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-201">Get command:</span></span>     | [<span data-ttu-id="ef0fa-202">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ef0fa-203"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL- \_ alpha- \_ Test \_ Ref</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-203"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL\_ALPHA\_TEST\_REF</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef0fa-204">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-204">Description:</span></span>     | <span data-ttu-id="ef0fa-205">Alpha-Test Verweis Wert</span><span class="sxs-lookup"><span data-stu-id="ef0fa-205">Alpha test reference value</span></span>                                                       |
| <span data-ttu-id="ef0fa-206">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-206">Attribute group:</span></span> | <span data-ttu-id="ef0fa-207">Farb Puffer</span><span class="sxs-lookup"><span data-stu-id="ef0fa-207">color-buffer</span></span>                                                                     |
| <span data-ttu-id="ef0fa-208">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-208">Initial value:</span></span>   | <span data-ttu-id="ef0fa-209">0</span><span class="sxs-lookup"><span data-stu-id="ef0fa-209">0</span></span>                                                                                |
| <span data-ttu-id="ef0fa-210">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-210">Get command:</span></span>     | [<span data-ttu-id="ef0fa-211">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-211">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ef0fa-212"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL- \_ tiefen \_ Test</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-212"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL\_DEPTH\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="ef0fa-213">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-213">Description:</span></span>     | <span data-ttu-id="ef0fa-214">Tiefen Puffer aktiviert</span><span class="sxs-lookup"><span data-stu-id="ef0fa-214">Depth buffer enabled</span></span>               |
| <span data-ttu-id="ef0fa-215">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-215">Attribute group:</span></span> | <span data-ttu-id="ef0fa-216">tiefen Puffer/aktivieren</span><span class="sxs-lookup"><span data-stu-id="ef0fa-216">depth-buffer/enable</span></span>                |
| <span data-ttu-id="ef0fa-217">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-217">Initial value:</span></span>   | <span data-ttu-id="ef0fa-218">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="ef0fa-218">GL\_FALSE</span></span>                          |
| <span data-ttu-id="ef0fa-219">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-219">Get command:</span></span>     | [<span data-ttu-id="ef0fa-220">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-220">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="ef0fa-221"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL- \_ Tiefe \_ Func</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-221"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL\_DEPTH\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef0fa-222">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-222">Description:</span></span>     | <span data-ttu-id="ef0fa-223">Tiefen Puffer-Testfunktion</span><span class="sxs-lookup"><span data-stu-id="ef0fa-223">Depth buffer test function</span></span>                                                       |
| <span data-ttu-id="ef0fa-224">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-224">Attribute group:</span></span> | <span data-ttu-id="ef0fa-225">tiefen Puffer</span><span class="sxs-lookup"><span data-stu-id="ef0fa-225">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="ef0fa-226">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-226">Initial value:</span></span>   | <span data-ttu-id="ef0fa-227">GL \_ weniger</span><span class="sxs-lookup"><span data-stu-id="ef0fa-227">GL\_LESS</span></span>                                                                         |
| <span data-ttu-id="ef0fa-228">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-228">Get command:</span></span>     | [<span data-ttu-id="ef0fa-229">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-229">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ef0fa-230"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL \_ Blend</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-230"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL\_BLEND</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="ef0fa-231">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-231">Description:</span></span>     | <span data-ttu-id="ef0fa-232">Blending aktiviert</span><span class="sxs-lookup"><span data-stu-id="ef0fa-232">Blending enabled</span></span>                   |
| <span data-ttu-id="ef0fa-233">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-233">Attribute group:</span></span> | <span data-ttu-id="ef0fa-234">Farb Puffer/-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="ef0fa-234">color-buffer/enable</span></span>                |
| <span data-ttu-id="ef0fa-235">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-235">Initial value:</span></span>   | <span data-ttu-id="ef0fa-236">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="ef0fa-236">GL\_FALSE</span></span>                          |
| <span data-ttu-id="ef0fa-237">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-237">Get command:</span></span>     | [<span data-ttu-id="ef0fa-238">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-238">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="ef0fa-239"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL \_ blenc \_ src</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-239"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL\_BLENC\_SRC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef0fa-240">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-240">Description:</span></span>     | <span data-ttu-id="ef0fa-241">Blending der Quell Funktion</span><span class="sxs-lookup"><span data-stu-id="ef0fa-241">Blending source function</span></span>                                                         |
| <span data-ttu-id="ef0fa-242">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-242">Attribute group:</span></span> | <span data-ttu-id="ef0fa-243">Farb Puffer</span><span class="sxs-lookup"><span data-stu-id="ef0fa-243">color-buffer</span></span>                                                                     |
| <span data-ttu-id="ef0fa-244">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-244">Initial value:</span></span>   | <span data-ttu-id="ef0fa-245">GL \_ 1</span><span class="sxs-lookup"><span data-stu-id="ef0fa-245">GL\_ONE</span></span>                                                                          |
| <span data-ttu-id="ef0fa-246">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-246">Get command:</span></span>     | [<span data-ttu-id="ef0fa-247">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-247">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ef0fa-248"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL \_ Blend \_ DST</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-248"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL\_BLEND\_DST</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef0fa-249">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-249">Description:</span></span>     | <span data-ttu-id="ef0fa-250">Zielfunktion wird gemischt</span><span class="sxs-lookup"><span data-stu-id="ef0fa-250">Blending destination function</span></span>                                                    |
| <span data-ttu-id="ef0fa-251">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-251">Attribute group:</span></span> | <span data-ttu-id="ef0fa-252">Farb Puffer</span><span class="sxs-lookup"><span data-stu-id="ef0fa-252">color-buffer</span></span>                                                                     |
| <span data-ttu-id="ef0fa-253">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-253">Initial value:</span></span>   | <span data-ttu-id="ef0fa-254">GL \_ null</span><span class="sxs-lookup"><span data-stu-id="ef0fa-254">GL\_ZERO</span></span>                                                                         |
| <span data-ttu-id="ef0fa-255">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-255">Get command:</span></span>     | [<span data-ttu-id="ef0fa-256">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-256">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ef0fa-257"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL \_ .</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-257"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL\_DITHER</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="ef0fa-258">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-258">Description:</span></span>     | <span data-ttu-id="ef0fa-259">Dithering aktiviert</span><span class="sxs-lookup"><span data-stu-id="ef0fa-259">Dithering enabled</span></span>                  |
| <span data-ttu-id="ef0fa-260">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-260">Attribute group:</span></span> | <span data-ttu-id="ef0fa-261">Farb Puffer/-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="ef0fa-261">color-buffer/enable</span></span>                |
| <span data-ttu-id="ef0fa-262">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-262">Initial value:</span></span>   | <span data-ttu-id="ef0fa-263">GL \_ true</span><span class="sxs-lookup"><span data-stu-id="ef0fa-263">GL\_TRUE</span></span>                           |
| <span data-ttu-id="ef0fa-264">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-264">Get command:</span></span>     | [<span data-ttu-id="ef0fa-265">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-265">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="ef0fa-266"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL- \_ Logik- \_ op</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-266"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL\_LOGIC\_OP</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="ef0fa-267">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-267">Description:</span></span>     | <span data-ttu-id="ef0fa-268">Logischer Vorgang aktiviert</span><span class="sxs-lookup"><span data-stu-id="ef0fa-268">Logical operation enabled</span></span>          |
| <span data-ttu-id="ef0fa-269">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-269">Attribute group:</span></span> | <span data-ttu-id="ef0fa-270">Farb Puffer/-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="ef0fa-270">color-buffer/enable</span></span>                |
| <span data-ttu-id="ef0fa-271">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-271">Initial value:</span></span>   | <span data-ttu-id="ef0fa-272">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="ef0fa-272">GL\_FALSE</span></span>                          |
| <span data-ttu-id="ef0fa-273">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-273">Get command:</span></span>     | [<span data-ttu-id="ef0fa-274">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-274">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="ef0fa-275"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL- \_ Logik- \_ op- \_ Modus</dt> </span><span class="sxs-lookup"><span data-stu-id="ef0fa-275"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL\_LOGIC\_OP\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef0fa-276">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-276">Description:</span></span>     | <span data-ttu-id="ef0fa-277">Logische Vorgangs Funktion</span><span class="sxs-lookup"><span data-stu-id="ef0fa-277">Logical operation function</span></span>                                                       |
| <span data-ttu-id="ef0fa-278">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-278">Attribute group:</span></span> | <span data-ttu-id="ef0fa-279">Farb Puffer</span><span class="sxs-lookup"><span data-stu-id="ef0fa-279">color-buffer</span></span>                                                                     |
| <span data-ttu-id="ef0fa-280">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-280">Initial value:</span></span>   | <span data-ttu-id="ef0fa-281">GL- \_ Kopie</span><span class="sxs-lookup"><span data-stu-id="ef0fa-281">GL\_COPY</span></span>                                                                         |
| <span data-ttu-id="ef0fa-282">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="ef0fa-282">Get command:</span></span>     | [<span data-ttu-id="ef0fa-283">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="ef0fa-283">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




