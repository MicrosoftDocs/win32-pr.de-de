---
title: Pixelvorgänge
description: Pixelvorgänge
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- Pixelvorgänge OpenGL
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d36fc22ace4ee18303ce0eb16c5a10f901510f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908878"
---
# <a name="pixel-operations"></a><span data-ttu-id="7fa81-104">Pixelvorgänge</span><span class="sxs-lookup"><span data-stu-id="7fa81-104">Pixel Operations</span></span>

<dl> <span data-ttu-id="7fa81-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL \_ SCISSOR \_ TEST</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL\_SCISSOR\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-106">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-106">Property</span></span> | <span data-ttu-id="7fa81-107">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-107">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="7fa81-108">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-108">Description:</span></span>     | <span data-ttu-id="7fa81-109">Scissoring aktiviert</span><span class="sxs-lookup"><span data-stu-id="7fa81-109">Scissoring enabled</span></span>                 |
| <span data-ttu-id="7fa81-110">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-110">Attribute group:</span></span> | <span data-ttu-id="7fa81-111">scissor/enable</span><span class="sxs-lookup"><span data-stu-id="7fa81-111">scissor/enable</span></span>                     |
| <span data-ttu-id="7fa81-112">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-112">Initial value:</span></span>   | <span data-ttu-id="7fa81-113">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="7fa81-113">GL\_FALSE</span></span>                          |
| <span data-ttu-id="7fa81-114">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-114">Get command:</span></span>     | [<span data-ttu-id="7fa81-115">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fa81-115">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="7fa81-116"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL \_ SCISSOR \_ BOX</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-116"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL\_SCISSOR\_BOX</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-117">Property</span></span> | <span data-ttu-id="7fa81-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-118">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fa81-119">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-119">Description:</span></span>     | <span data-ttu-id="7fa81-120">Scissor-Feld</span><span class="sxs-lookup"><span data-stu-id="7fa81-120">Scissor box</span></span>                                                                      |
| <span data-ttu-id="7fa81-121">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-121">Attribute group:</span></span> | <span data-ttu-id="7fa81-122">Schere</span><span class="sxs-lookup"><span data-stu-id="7fa81-122">scissor</span></span>                                                                          |
| <span data-ttu-id="7fa81-123">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-123">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="7fa81-124">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-124">Get command:</span></span>     | [<span data-ttu-id="7fa81-125">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fa81-125">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fa81-126"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>\_GL-SCHABLONENTEST \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-126"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL\_STENCIL\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-127">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-127">Property</span></span> | <span data-ttu-id="7fa81-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-128">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="7fa81-129">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-129">Description:</span></span>     | <span data-ttu-id="7fa81-130">Schablonen aktiviert</span><span class="sxs-lookup"><span data-stu-id="7fa81-130">Stenciling enabled</span></span>                 |
| <span data-ttu-id="7fa81-131">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-131">Attribute group:</span></span> | <span data-ttu-id="7fa81-132">Schablonenpuffer/Aktivieren</span><span class="sxs-lookup"><span data-stu-id="7fa81-132">stencil-buffer/enable</span></span>              |
| <span data-ttu-id="7fa81-133">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-133">Initial value:</span></span>   | <span data-ttu-id="7fa81-134">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="7fa81-134">GL\_FALSE</span></span>                          |
| <span data-ttu-id="7fa81-135">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-135">Get command:</span></span>     | [<span data-ttu-id="7fa81-136">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fa81-136">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="7fa81-137"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL \_ STENCIL \_ FUNC</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-137"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL\_STENCIL\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-138">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-138">Property</span></span> | <span data-ttu-id="7fa81-139">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-139">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fa81-140">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-140">Description:</span></span>     | <span data-ttu-id="7fa81-141">Schablonenfunktion</span><span class="sxs-lookup"><span data-stu-id="7fa81-141">Stencil function</span></span>                                                                 |
| <span data-ttu-id="7fa81-142">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-142">Attribute group:</span></span> | <span data-ttu-id="7fa81-143">Schablonenpuffer</span><span class="sxs-lookup"><span data-stu-id="7fa81-143">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="7fa81-144">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-144">Initial value:</span></span>   | <span data-ttu-id="7fa81-145">GL \_ ALWAYS</span><span class="sxs-lookup"><span data-stu-id="7fa81-145">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="7fa81-146">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-146">Get command:</span></span>     | [<span data-ttu-id="7fa81-147">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fa81-147">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fa81-148"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL \_ STENCIL \_ VALUE \_ MASK</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-148"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL\_STENCIL\_VALUE\_MASK</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-149">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-149">Property</span></span> | <span data-ttu-id="7fa81-150">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-150">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fa81-151">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-151">Description:</span></span>     | <span data-ttu-id="7fa81-152">Schablonenmaske</span><span class="sxs-lookup"><span data-stu-id="7fa81-152">Stencil mask</span></span>                                                                     |
| <span data-ttu-id="7fa81-153">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-153">Attribute group:</span></span> | <span data-ttu-id="7fa81-154">Schablonenpuffer</span><span class="sxs-lookup"><span data-stu-id="7fa81-154">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="7fa81-155">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-155">Initial value:</span></span>   | <span data-ttu-id="7fa81-156">1 s</span><span class="sxs-lookup"><span data-stu-id="7fa81-156">1's</span></span>                                                                              |
| <span data-ttu-id="7fa81-157">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-157">Get command:</span></span>     | [<span data-ttu-id="7fa81-158">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fa81-158">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fa81-159"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL \_ STENCIL \_ REF</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-159"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL\_STENCIL\_REF</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-160">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-160">Property</span></span> | <span data-ttu-id="7fa81-161">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-161">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fa81-162">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-162">Description:</span></span>     | <span data-ttu-id="7fa81-163">Schablonenverweiswert</span><span class="sxs-lookup"><span data-stu-id="7fa81-163">Stencil reference value</span></span>                                                          |
| <span data-ttu-id="7fa81-164">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-164">Attribute group:</span></span> | <span data-ttu-id="7fa81-165">Schablonenpuffer</span><span class="sxs-lookup"><span data-stu-id="7fa81-165">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="7fa81-166">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-166">Initial value:</span></span>   | <span data-ttu-id="7fa81-167">0</span><span class="sxs-lookup"><span data-stu-id="7fa81-167">0</span></span>                                                                                |
| <span data-ttu-id="7fa81-168">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-168">Get command:</span></span>     | [<span data-ttu-id="7fa81-169">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fa81-169">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fa81-170"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>FEHLER \_ BEI GL-SCHABLONE \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-170"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL\_STENCIL\_FAIL</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-171">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-171">Property</span></span> | <span data-ttu-id="7fa81-172">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-172">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fa81-173">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-173">Description:</span></span>     | <span data-ttu-id="7fa81-174">Schablonen-Fehleraktion</span><span class="sxs-lookup"><span data-stu-id="7fa81-174">Stencil fail action</span></span>                                                              |
| <span data-ttu-id="7fa81-175">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-175">Attribute group:</span></span> | <span data-ttu-id="7fa81-176">Schablonenpuffer</span><span class="sxs-lookup"><span data-stu-id="7fa81-176">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="7fa81-177">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-177">Initial value:</span></span>   | <span data-ttu-id="7fa81-178">GL \_ KEEP</span><span class="sxs-lookup"><span data-stu-id="7fa81-178">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="7fa81-179">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-179">Get command:</span></span>     | [<span data-ttu-id="7fa81-180">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fa81-180">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fa81-181"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>FEHLER \_ BEI GL-SCHABLONENPASSTIEFE \_ \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-181"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL\_STENCIL\_PASS\_DEPTH\_FAIL</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-182">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-182">Property</span></span> | <span data-ttu-id="7fa81-183">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-183">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fa81-184">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-184">Description:</span></span>     | <span data-ttu-id="7fa81-185">Fehleraktion für Schablonentiefepuffer</span><span class="sxs-lookup"><span data-stu-id="7fa81-185">Stencil depth buffer fail action</span></span>                                                 |
| <span data-ttu-id="7fa81-186">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-186">Attribute group:</span></span> | <span data-ttu-id="7fa81-187">Schablonenpuffer</span><span class="sxs-lookup"><span data-stu-id="7fa81-187">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="7fa81-188">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-188">Initial value:</span></span>   | <span data-ttu-id="7fa81-189">GL \_ KEEP</span><span class="sxs-lookup"><span data-stu-id="7fa81-189">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="7fa81-190">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-190">Get command:</span></span>     | [<span data-ttu-id="7fa81-191">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fa81-191">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fa81-192"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL \_ STENCIL \_ PASS \_ DEPTH \_ PASS</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-192"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL\_STENCIL\_PASS\_DEPTH\_PASS</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-193">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-193">Property</span></span> | <span data-ttu-id="7fa81-194">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-194">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fa81-195">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-195">Description:</span></span>     | <span data-ttu-id="7fa81-196">Pufferdurchlaufaktion für Schablonentiefe</span><span class="sxs-lookup"><span data-stu-id="7fa81-196">Stencil depth buffer pass action</span></span>                                                 |
| <span data-ttu-id="7fa81-197">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-197">Attribute group:</span></span> | <span data-ttu-id="7fa81-198">Schablonenpuffer</span><span class="sxs-lookup"><span data-stu-id="7fa81-198">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="7fa81-199">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-199">Initial value:</span></span>   | <span data-ttu-id="7fa81-200">GL \_ KEEP</span><span class="sxs-lookup"><span data-stu-id="7fa81-200">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="7fa81-201">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-201">Get command:</span></span>     | [<span data-ttu-id="7fa81-202">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fa81-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fa81-203"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL \_ ALPHA \_ TEST</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-203"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL\_ALPHA\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-204">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-204">Property</span></span> | <span data-ttu-id="7fa81-205">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-205">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="7fa81-206">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-206">Description:</span></span>     | <span data-ttu-id="7fa81-207">Alphatest aktiviert</span><span class="sxs-lookup"><span data-stu-id="7fa81-207">Alpha test enabled</span></span>                 |
| <span data-ttu-id="7fa81-208">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-208">Attribute group:</span></span> | <span data-ttu-id="7fa81-209">Farbpuffer/Aktivieren</span><span class="sxs-lookup"><span data-stu-id="7fa81-209">color-buffer/enable</span></span>                |
| <span data-ttu-id="7fa81-210">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-210">Initial value:</span></span>   | <span data-ttu-id="7fa81-211">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="7fa81-211">GL\_FALSE</span></span>                          |
| <span data-ttu-id="7fa81-212">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-212">Get command:</span></span>     | [<span data-ttu-id="7fa81-213">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fa81-213">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="7fa81-214"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL \_ ALPHA \_ TEST \_ FUNC</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-214"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL\_ALPHA\_TEST\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-215">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-215">Property</span></span> | <span data-ttu-id="7fa81-216">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-216">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fa81-217">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-217">Description:</span></span>     | <span data-ttu-id="7fa81-218">Alphatestfunktion</span><span class="sxs-lookup"><span data-stu-id="7fa81-218">Alpha test function</span></span>                                                              |
| <span data-ttu-id="7fa81-219">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-219">Attribute group:</span></span> | <span data-ttu-id="7fa81-220">Farbpuffer</span><span class="sxs-lookup"><span data-stu-id="7fa81-220">color-buffer</span></span>                                                                     |
| <span data-ttu-id="7fa81-221">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-221">Initial value:</span></span>   | <span data-ttu-id="7fa81-222">GL \_ ALWAYS</span><span class="sxs-lookup"><span data-stu-id="7fa81-222">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="7fa81-223">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-223">Get command:</span></span>     | [<span data-ttu-id="7fa81-224">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fa81-224">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fa81-225"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL \_ ALPHA \_ TEST \_ REF</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-225"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL\_ALPHA\_TEST\_REF</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-226">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-226">Property</span></span> | <span data-ttu-id="7fa81-227">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-227">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fa81-228">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-228">Description:</span></span>     | <span data-ttu-id="7fa81-229">Alphatestverweiswert</span><span class="sxs-lookup"><span data-stu-id="7fa81-229">Alpha test reference value</span></span>                                                       |
| <span data-ttu-id="7fa81-230">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-230">Attribute group:</span></span> | <span data-ttu-id="7fa81-231">Farbpuffer</span><span class="sxs-lookup"><span data-stu-id="7fa81-231">color-buffer</span></span>                                                                     |
| <span data-ttu-id="7fa81-232">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-232">Initial value:</span></span>   | <span data-ttu-id="7fa81-233">0</span><span class="sxs-lookup"><span data-stu-id="7fa81-233">0</span></span>                                                                                |
| <span data-ttu-id="7fa81-234">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-234">Get command:</span></span>     | [<span data-ttu-id="7fa81-235">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fa81-235">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fa81-236"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL \_ DEPTH \_ TEST</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-236"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL\_DEPTH\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-237">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-237">Property</span></span> | <span data-ttu-id="7fa81-238">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-238">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="7fa81-239">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-239">Description:</span></span>     | <span data-ttu-id="7fa81-240">Tiefenpuffer aktiviert</span><span class="sxs-lookup"><span data-stu-id="7fa81-240">Depth buffer enabled</span></span>               |
| <span data-ttu-id="7fa81-241">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-241">Attribute group:</span></span> | <span data-ttu-id="7fa81-242">Tiefenpuffer/Aktivieren</span><span class="sxs-lookup"><span data-stu-id="7fa81-242">depth-buffer/enable</span></span>                |
| <span data-ttu-id="7fa81-243">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-243">Initial value:</span></span>   | <span data-ttu-id="7fa81-244">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="7fa81-244">GL\_FALSE</span></span>                          |
| <span data-ttu-id="7fa81-245">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-245">Get command:</span></span>     | [<span data-ttu-id="7fa81-246">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fa81-246">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="7fa81-247"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL \_ DEPTH \_ FUNC</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-247"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL\_DEPTH\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-248">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-248">Property</span></span> | <span data-ttu-id="7fa81-249">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-249">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fa81-250">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-250">Description:</span></span>     | <span data-ttu-id="7fa81-251">Testfunktion "Tiefenpuffer"</span><span class="sxs-lookup"><span data-stu-id="7fa81-251">Depth buffer test function</span></span>                                                       |
| <span data-ttu-id="7fa81-252">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-252">Attribute group:</span></span> | <span data-ttu-id="7fa81-253">Tiefenpuffer</span><span class="sxs-lookup"><span data-stu-id="7fa81-253">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="7fa81-254">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-254">Initial value:</span></span>   | <span data-ttu-id="7fa81-255">GL \_ LESS</span><span class="sxs-lookup"><span data-stu-id="7fa81-255">GL\_LESS</span></span>                                                                         |
| <span data-ttu-id="7fa81-256">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-256">Get command:</span></span>     | [<span data-ttu-id="7fa81-257">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fa81-257">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fa81-258"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL \_ BLEND</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-258"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL\_BLEND</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-259">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-259">Property</span></span> | <span data-ttu-id="7fa81-260">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-260">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="7fa81-261">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-261">Description:</span></span>     | <span data-ttu-id="7fa81-262">Blending aktiviert</span><span class="sxs-lookup"><span data-stu-id="7fa81-262">Blending enabled</span></span>                   |
| <span data-ttu-id="7fa81-263">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-263">Attribute group:</span></span> | <span data-ttu-id="7fa81-264">Farbpuffer/Aktivieren</span><span class="sxs-lookup"><span data-stu-id="7fa81-264">color-buffer/enable</span></span>                |
| <span data-ttu-id="7fa81-265">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-265">Initial value:</span></span>   | <span data-ttu-id="7fa81-266">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="7fa81-266">GL\_FALSE</span></span>                          |
| <span data-ttu-id="7fa81-267">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-267">Get command:</span></span>     | [<span data-ttu-id="7fa81-268">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fa81-268">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="7fa81-269"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL \_ BLENC \_ SRC</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-269"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL\_BLENC\_SRC</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-270">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-270">Property</span></span> | <span data-ttu-id="7fa81-271">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-271">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fa81-272">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-272">Description:</span></span>     | <span data-ttu-id="7fa81-273">Blending-Quellfunktion</span><span class="sxs-lookup"><span data-stu-id="7fa81-273">Blending source function</span></span>                                                         |
| <span data-ttu-id="7fa81-274">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-274">Attribute group:</span></span> | <span data-ttu-id="7fa81-275">Farbpuffer</span><span class="sxs-lookup"><span data-stu-id="7fa81-275">color-buffer</span></span>                                                                     |
| <span data-ttu-id="7fa81-276">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-276">Initial value:</span></span>   | <span data-ttu-id="7fa81-277">GL \_ ONE</span><span class="sxs-lookup"><span data-stu-id="7fa81-277">GL\_ONE</span></span>                                                                          |
| <span data-ttu-id="7fa81-278">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-278">Get command:</span></span>     | [<span data-ttu-id="7fa81-279">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fa81-279">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fa81-280"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL \_ BLEND \_ DST</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-280"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL\_BLEND\_DST</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-281">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-281">Property</span></span> | <span data-ttu-id="7fa81-282">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-282">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fa81-283">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-283">Description:</span></span>     | <span data-ttu-id="7fa81-284">Blendingzielfunktion</span><span class="sxs-lookup"><span data-stu-id="7fa81-284">Blending destination function</span></span>                                                    |
| <span data-ttu-id="7fa81-285">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-285">Attribute group:</span></span> | <span data-ttu-id="7fa81-286">Farbpuffer</span><span class="sxs-lookup"><span data-stu-id="7fa81-286">color-buffer</span></span>                                                                     |
| <span data-ttu-id="7fa81-287">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-287">Initial value:</span></span>   | <span data-ttu-id="7fa81-288">GL \_ ZERO</span><span class="sxs-lookup"><span data-stu-id="7fa81-288">GL\_ZERO</span></span>                                                                         |
| <span data-ttu-id="7fa81-289">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-289">Get command:</span></span>     | [<span data-ttu-id="7fa81-290">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fa81-290">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fa81-291"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL \_ DITHER</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-291"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL\_DITHER</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-292">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-292">Property</span></span> | <span data-ttu-id="7fa81-293">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-293">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="7fa81-294">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-294">Description:</span></span>     | <span data-ttu-id="7fa81-295">Dithering aktiviert</span><span class="sxs-lookup"><span data-stu-id="7fa81-295">Dithering enabled</span></span>                  |
| <span data-ttu-id="7fa81-296">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-296">Attribute group:</span></span> | <span data-ttu-id="7fa81-297">Farbpuffer/Aktivieren</span><span class="sxs-lookup"><span data-stu-id="7fa81-297">color-buffer/enable</span></span>                |
| <span data-ttu-id="7fa81-298">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-298">Initial value:</span></span>   | <span data-ttu-id="7fa81-299">GL \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="7fa81-299">GL\_TRUE</span></span>                           |
| <span data-ttu-id="7fa81-300">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-300">Get command:</span></span>     | [<span data-ttu-id="7fa81-301">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fa81-301">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="7fa81-302"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL \_ LOGIC \_ OP</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-302"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL\_LOGIC\_OP</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-303">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-303">Property</span></span> | <span data-ttu-id="7fa81-304">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-304">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="7fa81-305">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-305">Description:</span></span>     | <span data-ttu-id="7fa81-306">Logischer Vorgang aktiviert</span><span class="sxs-lookup"><span data-stu-id="7fa81-306">Logical operation enabled</span></span>          |
| <span data-ttu-id="7fa81-307">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-307">Attribute group:</span></span> | <span data-ttu-id="7fa81-308">Farbpuffer/Aktivieren</span><span class="sxs-lookup"><span data-stu-id="7fa81-308">color-buffer/enable</span></span>                |
| <span data-ttu-id="7fa81-309">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-309">Initial value:</span></span>   | <span data-ttu-id="7fa81-310">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="7fa81-310">GL\_FALSE</span></span>                          |
| <span data-ttu-id="7fa81-311">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-311">Get command:</span></span>     | [<span data-ttu-id="7fa81-312">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fa81-312">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="7fa81-313"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL \_ LOGIC \_ OP \_ MODE</dt> </span><span class="sxs-lookup"><span data-stu-id="7fa81-313"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL\_LOGIC\_OP\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="7fa81-314">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fa81-314">Property</span></span> | <span data-ttu-id="7fa81-315">Wert</span><span class="sxs-lookup"><span data-stu-id="7fa81-315">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fa81-316">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7fa81-316">Description:</span></span>     | <span data-ttu-id="7fa81-317">Logische Vorgangsfunktion</span><span class="sxs-lookup"><span data-stu-id="7fa81-317">Logical operation function</span></span>                                                       |
| <span data-ttu-id="7fa81-318">Attributgruppe:</span><span class="sxs-lookup"><span data-stu-id="7fa81-318">Attribute group:</span></span> | <span data-ttu-id="7fa81-319">Farbpuffer</span><span class="sxs-lookup"><span data-stu-id="7fa81-319">color-buffer</span></span>                                                                     |
| <span data-ttu-id="7fa81-320">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="7fa81-320">Initial value:</span></span>   | <span data-ttu-id="7fa81-321">GL \_ COPY</span><span class="sxs-lookup"><span data-stu-id="7fa81-321">GL\_COPY</span></span>                                                                         |
| <span data-ttu-id="7fa81-322">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="7fa81-322">Get command:</span></span>     | [<span data-ttu-id="7fa81-323">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fa81-323">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




