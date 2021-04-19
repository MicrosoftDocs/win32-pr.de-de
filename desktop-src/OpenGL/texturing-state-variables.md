---
title: Texturierungsstatusvariablen
description: Texturierungsstatusvariablen
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- Texturing-Zustandsvariablen OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a9894e9f3723cca957fdeeb2882ede8f689ee7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106342316"
---
# <a name="texturing-state-variables"></a><span data-ttu-id="dd791-104">Texturierungsstatusvariablen</span><span class="sxs-lookup"><span data-stu-id="dd791-104">Texturing State Variables</span></span>

<dl> <span data-ttu-id="dd791-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL \_ Textur \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL\_TEXTURE\_*x*</dt> </span></span><dd> 

|                  |                                                       |
|------------------|-------------------------------------------------------|
| <span data-ttu-id="dd791-106">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-106">Description:</span></span>     | <span data-ttu-id="dd791-107">True, wenn die *x*   -D-Texturierung aktiviert ist (*x* ist 1-d oder 2D).</span><span class="sxs-lookup"><span data-stu-id="dd791-107">True if *x* - D texturing enabled (*x* is 1-D or 2-D)</span></span> |
| <span data-ttu-id="dd791-108">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-108">Attribute group:</span></span> | <span data-ttu-id="dd791-109">Textur/aktivieren</span><span class="sxs-lookup"><span data-stu-id="dd791-109">texture/enable</span></span>                                        |
| <span data-ttu-id="dd791-110">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-110">Initial value:</span></span>   | <span data-ttu-id="dd791-111">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="dd791-111">GL\_FALSE</span></span>                                             |
| <span data-ttu-id="dd791-112">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-112">Get command:</span></span>     | [<span data-ttu-id="dd791-113">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="dd791-113">**glIsEnabled**</span></span>](glisenabled.md)                    |



 

<span data-ttu-id="dd791-114"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL- \_ Textur</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-114"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL\_TEXTURE</dt> </span></span><dd> 

|                  |                                              |
|------------------|----------------------------------------------|
| <span data-ttu-id="dd791-115">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-115">Description:</span></span>     | <span data-ttu-id="dd791-116">*x*   -D Textur Bild auf Detailebene *i*</span><span class="sxs-lookup"><span data-stu-id="dd791-116">*x* - D texture image at level of detail *i*</span></span> |
| <span data-ttu-id="dd791-117">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-117">Attribute group:</span></span> |                                              |
| <span data-ttu-id="dd791-118">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-118">Initial value:</span></span>   |                                              |
| <span data-ttu-id="dd791-119">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-119">Get command:</span></span>     | [<span data-ttu-id="dd791-120">**glgetteximage**</span><span class="sxs-lookup"><span data-stu-id="dd791-120">**glGetTexImage**</span></span>](glgetteximage.md)       |



 

<span data-ttu-id="dd791-121"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL- \_ Textur \_ Breite</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-121"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL\_TEXTURE\_WIDTH</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="dd791-122">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-122">Description:</span></span>     | <span data-ttu-id="dd791-123">*x*   -D *Textur Bild*   Breite</span><span class="sxs-lookup"><span data-stu-id="dd791-123">*x* - D texture image *i* 's width</span></span>                       |
| <span data-ttu-id="dd791-124">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-124">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="dd791-125">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-125">Initial value:</span></span>   | <span data-ttu-id="dd791-126">0</span><span class="sxs-lookup"><span data-stu-id="dd791-126">0</span></span>                                                        |
| <span data-ttu-id="dd791-127">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-127">Get command:</span></span>     | [<span data-ttu-id="dd791-128">**glgettexlevelparameter**</span><span class="sxs-lookup"><span data-stu-id="dd791-128">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="dd791-129"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL- \_ Textur \_ Höhe</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-129"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL\_TEXTURE\_HEIGHT</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="dd791-130">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-130">Description:</span></span>     | <span data-ttu-id="dd791-131">*x*   -D *Textur Bild meine*   Höhe</span><span class="sxs-lookup"><span data-stu-id="dd791-131">*x* - D texture image *i* 's height</span></span>                      |
| <span data-ttu-id="dd791-132">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-132">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="dd791-133">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-133">Initial value:</span></span>   | <span data-ttu-id="dd791-134">0</span><span class="sxs-lookup"><span data-stu-id="dd791-134">0</span></span>                                                        |
| <span data-ttu-id="dd791-135">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-135">Get command:</span></span>     | [<span data-ttu-id="dd791-136">**glgettexlevelparameter**</span><span class="sxs-lookup"><span data-stu-id="dd791-136">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="dd791-137"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL- \_ Textur Rahmen \_</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-137"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL\_TEXTURE\_BORDER</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="dd791-138">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-138">Description:</span></span>     | <span data-ttu-id="dd791-139">*x*   -D Textur Bild *i* Rahmen  </span><span class="sxs-lookup"><span data-stu-id="dd791-139">*x* - D texture image *i* 's border</span></span>                      |
| <span data-ttu-id="dd791-140">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-140">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="dd791-141">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-141">Initial value:</span></span>   | <span data-ttu-id="dd791-142">0</span><span class="sxs-lookup"><span data-stu-id="dd791-142">0</span></span>                                                        |
| <span data-ttu-id="dd791-143">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-143">Get command:</span></span>     | [<span data-ttu-id="dd791-144">**glgettexlevelparameter**</span><span class="sxs-lookup"><span data-stu-id="dd791-144">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="dd791-145"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>GL- \_ Textur \_ Komponenten</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-145"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>GL\_TEXTURE\_COMPONENTS</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="dd791-146">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-146">Description:</span></span>     | <span data-ttu-id="dd791-147">Textur Bild Komponenten</span><span class="sxs-lookup"><span data-stu-id="dd791-147">Texture image components</span></span>                                 |
| <span data-ttu-id="dd791-148">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-148">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="dd791-149">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-149">Initial value:</span></span>   | <span data-ttu-id="dd791-150">1</span><span class="sxs-lookup"><span data-stu-id="dd791-150">1</span></span>                                                        |
| <span data-ttu-id="dd791-151">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-151">Get command:</span></span>     | [<span data-ttu-id="dd791-152">**glgettexlevelparameter**</span><span class="sxs-lookup"><span data-stu-id="dd791-152">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="dd791-153"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>Rahmenfarbe des GL- \_ Textur Rahmens \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-153"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>GL\_TEXTURE\_BORDER\_COLOR</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="dd791-154">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-154">Description:</span></span>     | <span data-ttu-id="dd791-155">Textur Rahmenfarbe</span><span class="sxs-lookup"><span data-stu-id="dd791-155">Texture border color</span></span>                           |
| <span data-ttu-id="dd791-156">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-156">Attribute group:</span></span> | <span data-ttu-id="dd791-157">Struktur</span><span class="sxs-lookup"><span data-stu-id="dd791-157">texture</span></span>                                        |
| <span data-ttu-id="dd791-158">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-158">Initial value:</span></span>   | <span data-ttu-id="dd791-159">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="dd791-159">0, 0, 0, 0</span></span>                                     |
| <span data-ttu-id="dd791-160">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-160">Get command:</span></span>     | [<span data-ttu-id="dd791-161">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="dd791-161">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="dd791-162"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL- \_ Textur- \_ Min- \_ Filter</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-162"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL\_TEXTURE\_MIN\_FILTER</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="dd791-163">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-163">Description:</span></span>     | <span data-ttu-id="dd791-164">Textur Minimierung-Funktion</span><span class="sxs-lookup"><span data-stu-id="dd791-164">Texture minification function</span></span>                  |
| <span data-ttu-id="dd791-165">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-165">Attribute group:</span></span> | <span data-ttu-id="dd791-166">Struktur</span><span class="sxs-lookup"><span data-stu-id="dd791-166">texture</span></span>                                        |
| <span data-ttu-id="dd791-167">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-167">Initial value:</span></span>   | <span data-ttu-id="dd791-168">\_nächste nächste \_ MipMap ( \_ linear)</span><span class="sxs-lookup"><span data-stu-id="dd791-168">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>                    |
| <span data-ttu-id="dd791-169">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-169">Get command:</span></span>     | [<span data-ttu-id="dd791-170">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="dd791-170">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="dd791-171"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL- \_ Textur- \_ mag- \_ Filter</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-171"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL\_TEXTURE\_MAG\_FILTER</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="dd791-172">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-172">Description:</span></span>     | <span data-ttu-id="dd791-173">Textur Vergrößerungsfunktion</span><span class="sxs-lookup"><span data-stu-id="dd791-173">Texture magnification function</span></span>                 |
| <span data-ttu-id="dd791-174">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-174">Attribute group:</span></span> | <span data-ttu-id="dd791-175">Struktur</span><span class="sxs-lookup"><span data-stu-id="dd791-175">texture</span></span>                                        |
| <span data-ttu-id="dd791-176">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-176">Initial value:</span></span>   | <span data-ttu-id="dd791-177">GL \_ linear</span><span class="sxs-lookup"><span data-stu-id="dd791-177">GL\_LINEAR</span></span>                                     |
| <span data-ttu-id="dd791-178">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-178">Get command:</span></span>     | [<span data-ttu-id="dd791-179">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="dd791-179">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="dd791-180"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL- \_ Textur Umbruch \_ \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-180"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL\_TEXTURE\_WRAP\_ *x*</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="dd791-181">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-181">Description:</span></span>     | <span data-ttu-id="dd791-182">Textur Umbruch Modus (*x*   ist S oder T)</span><span class="sxs-lookup"><span data-stu-id="dd791-182">Texture wrap mode (*x* is S or T)</span></span>              |
| <span data-ttu-id="dd791-183">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-183">Attribute group:</span></span> | <span data-ttu-id="dd791-184">Struktur</span><span class="sxs-lookup"><span data-stu-id="dd791-184">texture</span></span>                                        |
| <span data-ttu-id="dd791-185">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-185">Initial value:</span></span>   | <span data-ttu-id="dd791-186">GL. \_ Wiederholung</span><span class="sxs-lookup"><span data-stu-id="dd791-186">GL\_REPEAT</span></span>                                     |
| <span data-ttu-id="dd791-187">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-187">Get command:</span></span>     | [<span data-ttu-id="dd791-188">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="dd791-188">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="dd791-189"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL- \_ Textur \_ env- \_ Modus</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-189"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL\_TEXTURE\_ENV\_MODE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="dd791-190">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-190">Description:</span></span>     | <span data-ttu-id="dd791-191">Textur-Anwendungsfunktion</span><span class="sxs-lookup"><span data-stu-id="dd791-191">Texture application function</span></span>         |
| <span data-ttu-id="dd791-192">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-192">Attribute group:</span></span> | <span data-ttu-id="dd791-193">Struktur</span><span class="sxs-lookup"><span data-stu-id="dd791-193">texture</span></span>                              |
| <span data-ttu-id="dd791-194">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-194">Initial value:</span></span>   | <span data-ttu-id="dd791-195">GL \_ modulate</span><span class="sxs-lookup"><span data-stu-id="dd791-195">GL\_MODULATE</span></span>                         |
| <span data-ttu-id="dd791-196">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-196">Get command:</span></span>     | [<span data-ttu-id="dd791-197">**glgettexenviv**</span><span class="sxs-lookup"><span data-stu-id="dd791-197">**glGetTexEnviv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="dd791-198"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL- \_ Textur Gesamt \_ \_ Farbe</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-198"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL\_TEXTURE\_ENV\_COLOR</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="dd791-199">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-199">Description:</span></span>     | <span data-ttu-id="dd791-200">Textur Umgebungs Farbe</span><span class="sxs-lookup"><span data-stu-id="dd791-200">Texture environment color</span></span>            |
| <span data-ttu-id="dd791-201">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-201">Attribute group:</span></span> | <span data-ttu-id="dd791-202">Struktur</span><span class="sxs-lookup"><span data-stu-id="dd791-202">texture</span></span>                              |
| <span data-ttu-id="dd791-203">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-203">Initial value:</span></span>   | <span data-ttu-id="dd791-204">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="dd791-204">0, 0, 0, 0</span></span>                           |
| <span data-ttu-id="dd791-205">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-205">Get command:</span></span>     | [<span data-ttu-id="dd791-206">**glgettexendvfv**</span><span class="sxs-lookup"><span data-stu-id="dd791-206">**glGetTexEnvfv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="dd791-207"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL \_ Textur \_ gen \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-207"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL\_TEXTURE\_GEN\_ *x*</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="dd791-208">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-208">Description:</span></span>     | <span data-ttu-id="dd791-209">TEXGEN ist aktiviert (*x*   ist S, T, R oder Q).</span><span class="sxs-lookup"><span data-stu-id="dd791-209">Texgen is enabled (*x* is S, T, R, or Q)</span></span> |
| <span data-ttu-id="dd791-210">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-210">Attribute group:</span></span> | <span data-ttu-id="dd791-211">Textur/aktivieren</span><span class="sxs-lookup"><span data-stu-id="dd791-211">texture/enable</span></span>                           |
| <span data-ttu-id="dd791-212">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-212">Initial value:</span></span>   | <span data-ttu-id="dd791-213">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="dd791-213">GL\_FALSE</span></span>                                |
| <span data-ttu-id="dd791-214">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-214">Get command:</span></span>     | [<span data-ttu-id="dd791-215">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="dd791-215">**glIsEnabled**</span></span>](glisenabled.md)       |



 

<span data-ttu-id="dd791-216"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL- \_ Augen \_ Ebene</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-216"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL\_EYE\_PLANE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="dd791-217">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-217">Description:</span></span>     | <span data-ttu-id="dd791-218">Formel für die Formel der TEXGEN-Ebene</span><span class="sxs-lookup"><span data-stu-id="dd791-218">Texgen plane equation coefficients</span></span>   |
| <span data-ttu-id="dd791-219">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-219">Attribute group:</span></span> | <span data-ttu-id="dd791-220">Struktur</span><span class="sxs-lookup"><span data-stu-id="dd791-220">texture</span></span>                              |
| <span data-ttu-id="dd791-221">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-221">Initial value:</span></span>   |                                      |
| <span data-ttu-id="dd791-222">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-222">Get command:</span></span>     | [<span data-ttu-id="dd791-223">**glgettexgenfv**</span><span class="sxs-lookup"><span data-stu-id="dd791-223">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="dd791-224"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>GL- \_ Objekt \_ Ebene</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-224"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>GL\_OBJECT\_PLANE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="dd791-225">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-225">Description:</span></span>     | <span data-ttu-id="dd791-226">Lineare Koeffizienten für TEXGEN-Objekte</span><span class="sxs-lookup"><span data-stu-id="dd791-226">Texgen object linear coefficients</span></span>    |
| <span data-ttu-id="dd791-227">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-227">Attribute group:</span></span> | <span data-ttu-id="dd791-228">Struktur</span><span class="sxs-lookup"><span data-stu-id="dd791-228">texture</span></span>                              |
| <span data-ttu-id="dd791-229">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-229">Initial value:</span></span>   |                                      |
| <span data-ttu-id="dd791-230">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-230">Get command:</span></span>     | [<span data-ttu-id="dd791-231">**glgettexgenfv**</span><span class="sxs-lookup"><span data-stu-id="dd791-231">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="dd791-232"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL- \_ Textur \_ gen- \_ Modus</dt> </span><span class="sxs-lookup"><span data-stu-id="dd791-232"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL\_TEXTURE\_GEN\_MODE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="dd791-233">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dd791-233">Description:</span></span>     | <span data-ttu-id="dd791-234">Für TEXGEN verwendete Funktion</span><span class="sxs-lookup"><span data-stu-id="dd791-234">Function used for texgen</span></span>             |
| <span data-ttu-id="dd791-235">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="dd791-235">Attribute group:</span></span> | <span data-ttu-id="dd791-236">Struktur</span><span class="sxs-lookup"><span data-stu-id="dd791-236">texture</span></span>                              |
| <span data-ttu-id="dd791-237">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="dd791-237">Initial value:</span></span>   | <span data-ttu-id="dd791-238">GL- \_ Eye \_ linear</span><span class="sxs-lookup"><span data-stu-id="dd791-238">GL\_EYE\_LINEAR</span></span>                      |
| <span data-ttu-id="dd791-239">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="dd791-239">Get command:</span></span>     | [<span data-ttu-id="dd791-240">**glgettexgeniv**</span><span class="sxs-lookup"><span data-stu-id="dd791-240">**glGetTexGeniv**</span></span>](glgettexgen.md) |



 

</dd> </dl>

 

 




