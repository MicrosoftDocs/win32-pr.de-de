---
title: Beleuchtungs Zustandsvariablen
description: Beleuchtungs Zustandsvariablen
ms.assetid: a9fb1e22-5e33-4b46-9c3b-2f64de5dd646
keywords:
- Beleuchtungs Zustandsvariablen OpenGL
topic_type:
- apiref
api_name:
- Lighting State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7144e284b5be5abd5a6dc4e08fe2228b621465
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857399"
---
# <a name="lighting-state-variables"></a><span data-ttu-id="4b554-104">Beleuchtungs Zustandsvariablen</span><span class="sxs-lookup"><span data-stu-id="4b554-104">Lighting State Variables</span></span>

<dl> <span data-ttu-id="4b554-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>GL- \_ Beleuchtung</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>GL\_LIGHTING</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4b554-106">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-106">Description:</span></span>     | <span data-ttu-id="4b554-107">True, wenn Beleuchtung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4b554-107">True if lighting is enabled</span></span>        |
| <span data-ttu-id="4b554-108">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-108">Attribute group:</span></span> | <span data-ttu-id="4b554-109">Beleuchtung/Aktivierung</span><span class="sxs-lookup"><span data-stu-id="4b554-109">lighting/enable</span></span>                    |
| <span data-ttu-id="4b554-110">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-110">Initial value:</span></span>   | <span data-ttu-id="4b554-111">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="4b554-111">GL\_FALSE</span></span>                          |
| <span data-ttu-id="4b554-112">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-112">Get command:</span></span>     | [<span data-ttu-id="4b554-113">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="4b554-113">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="4b554-114"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>GL- \_ Farb \_ Material</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-114"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>GL\_COLOR\_MATERIAL</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4b554-115">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-115">Description:</span></span>     | <span data-ttu-id="4b554-116">True, wenn die Farb Verfolgung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4b554-116">True if color tracking is enabled</span></span>  |
| <span data-ttu-id="4b554-117">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-117">Attribute group:</span></span> | <span data-ttu-id="4b554-118">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-118">lighting</span></span>                           |
| <span data-ttu-id="4b554-119">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-119">Initial value:</span></span>   | <span data-ttu-id="4b554-120">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="4b554-120">GL\_FALSE</span></span>                          |
| <span data-ttu-id="4b554-121">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-121">Get command:</span></span>     | [<span data-ttu-id="4b554-122">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="4b554-122">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="4b554-123"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>GL- \_ Farb \_ Material \_ Parameter</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-123"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>GL\_COLOR\_MATERIAL\_PARAMETER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4b554-124">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-124">Description:</span></span>     | <span data-ttu-id="4b554-125">Material Eigenschaften Nachverfolgung der aktuellen Farbe</span><span class="sxs-lookup"><span data-stu-id="4b554-125">Material properties tracking current color</span></span>                                       |
| <span data-ttu-id="4b554-126">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-126">Attribute group:</span></span> | <span data-ttu-id="4b554-127">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-127">lighting</span></span>                                                                         |
| <span data-ttu-id="4b554-128">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-128">Initial value:</span></span>   | <span data-ttu-id="4b554-129">GL \_ AMBIENT \_ und \_ diffuse</span><span class="sxs-lookup"><span data-stu-id="4b554-129">GL\_AMBIENT\_AND\_DIFFUSE</span></span>                                                        |
| <span data-ttu-id="4b554-130">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-130">Get command:</span></span>     | [<span data-ttu-id="4b554-131">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="4b554-131">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="4b554-132"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL- \_ Farb \_ Material \_ Gesicht</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-132"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL\_COLOR\_MATERIAL\_FACE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4b554-133">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-133">Description:</span></span>     | <span data-ttu-id="4b554-134">Von der Farbüberwachung betroffene Gesichter</span><span class="sxs-lookup"><span data-stu-id="4b554-134">Faces affected by color tracking</span></span>                                                 |
| <span data-ttu-id="4b554-135">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-135">Attribute group:</span></span> | <span data-ttu-id="4b554-136">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-136">lighting</span></span>                                                                         |
| <span data-ttu-id="4b554-137">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-137">Initial value:</span></span>   | <span data-ttu-id="4b554-138">GL \_ vor \_ und \_ zurück</span><span class="sxs-lookup"><span data-stu-id="4b554-138">GL\_FRONT\_AND\_BACK</span></span>                                                             |
| <span data-ttu-id="4b554-139">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-139">Get command:</span></span>     | [<span data-ttu-id="4b554-140">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="4b554-140">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="4b554-141"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL- \_ AMBIENT</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-141"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="4b554-142">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-142">Description:</span></span>     | <span data-ttu-id="4b554-143">Umgebungs Material Farbe</span><span class="sxs-lookup"><span data-stu-id="4b554-143">Ambient material color</span></span>                   |
| <span data-ttu-id="4b554-144">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-144">Attribute group:</span></span> | <span data-ttu-id="4b554-145">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-145">lighting</span></span>                                 |
| <span data-ttu-id="4b554-146">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-146">Initial value:</span></span>   | <span data-ttu-id="4b554-147">(0,2, 0,2, 0,2, 1.0)</span><span class="sxs-lookup"><span data-stu-id="4b554-147">(0.2,0.2,0.2,1.0)</span></span>                        |
| <span data-ttu-id="4b554-148">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-148">Get command:</span></span>     | [<span data-ttu-id="4b554-149">**glgetmaterialfv**</span><span class="sxs-lookup"><span data-stu-id="4b554-149">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="4b554-150"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL- \_ diffuses</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-150"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="4b554-151">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-151">Description:</span></span>     | <span data-ttu-id="4b554-152">Farbe für Diffuses Material</span><span class="sxs-lookup"><span data-stu-id="4b554-152">Diffuse material color</span></span>                   |
| <span data-ttu-id="4b554-153">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-153">Attribute group:</span></span> | <span data-ttu-id="4b554-154">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-154">lighting</span></span>                                 |
| <span data-ttu-id="4b554-155">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-155">Initial value:</span></span>   | <span data-ttu-id="4b554-156">(0,8, 0.8, 0.8, 1.0)</span><span class="sxs-lookup"><span data-stu-id="4b554-156">(0.8,0.8,0.8,1.0)</span></span>                        |
| <span data-ttu-id="4b554-157">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-157">Get command:</span></span>     | [<span data-ttu-id="4b554-158">**glgetmaterialfv**</span><span class="sxs-lookup"><span data-stu-id="4b554-158">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="4b554-159"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL \_ Glanz</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-159"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="4b554-160">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-160">Description:</span></span>     | <span data-ttu-id="4b554-161">Glanz Material Farbe</span><span class="sxs-lookup"><span data-stu-id="4b554-161">Specular material color</span></span>                  |
| <span data-ttu-id="4b554-162">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-162">Attribute group:</span></span> | <span data-ttu-id="4b554-163">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-163">lighting</span></span>                                 |
| <span data-ttu-id="4b554-164">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-164">Initial value:</span></span>   | <span data-ttu-id="4b554-165">(0,0, 0,0, 0,0, 1.0)</span><span class="sxs-lookup"><span data-stu-id="4b554-165">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="4b554-166">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-166">Get command:</span></span>     | [<span data-ttu-id="4b554-167">**glgetmaterialfv**</span><span class="sxs-lookup"><span data-stu-id="4b554-167">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="4b554-168"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>GL \_ -Ausgabe</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-168"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>GL\_EMISSION</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="4b554-169">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-169">Description:</span></span>     | <span data-ttu-id="4b554-170">Emissive Material Farbe</span><span class="sxs-lookup"><span data-stu-id="4b554-170">Emissive material color</span></span>                  |
| <span data-ttu-id="4b554-171">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-171">Attribute group:</span></span> | <span data-ttu-id="4b554-172">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-172">lighting</span></span>                                 |
| <span data-ttu-id="4b554-173">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-173">Initial value:</span></span>   | <span data-ttu-id="4b554-174">(0,0, 0,0, 0,0, 1.0)</span><span class="sxs-lookup"><span data-stu-id="4b554-174">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="4b554-175">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-175">Get command:</span></span>     | [<span data-ttu-id="4b554-176">**glgetmaterialfv**</span><span class="sxs-lookup"><span data-stu-id="4b554-176">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="4b554-177"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL \_ .</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-177"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL\_SHININESS</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="4b554-178">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-178">Description:</span></span>     | <span data-ttu-id="4b554-179">Glanz Exponent von Material</span><span class="sxs-lookup"><span data-stu-id="4b554-179">Specular exponent of material</span></span>            |
| <span data-ttu-id="4b554-180">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-180">Attribute group:</span></span> | <span data-ttu-id="4b554-181">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-181">lighting</span></span>                                 |
| <span data-ttu-id="4b554-182">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-182">Initial value:</span></span>   | <span data-ttu-id="4b554-183">0,0</span><span class="sxs-lookup"><span data-stu-id="4b554-183">0.0</span></span>                                      |
| <span data-ttu-id="4b554-184">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-184">Get command:</span></span>     | [<span data-ttu-id="4b554-185">**glgetmaterialfv**</span><span class="sxs-lookup"><span data-stu-id="4b554-185">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="4b554-186"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>GL- \_ Light- \_ Modell \_ AMBIENT</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-186"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>GL\_LIGHT\_MODEL\_AMBIENT</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="4b554-187">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-187">Description:</span></span>     | <span data-ttu-id="4b554-188">Ambiente-Szene Farbe</span><span class="sxs-lookup"><span data-stu-id="4b554-188">Ambient scene color</span></span>                                                            |
| <span data-ttu-id="4b554-189">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-189">Attribute group:</span></span> | <span data-ttu-id="4b554-190">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-190">lighting</span></span>                                                                       |
| <span data-ttu-id="4b554-191">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-191">Initial value:</span></span>   | <span data-ttu-id="4b554-192">(0,2, 0,2, 0,2, 1.0)</span><span class="sxs-lookup"><span data-stu-id="4b554-192">(0.2,0.2,0.2,1.0)</span></span>                                                              |
| <span data-ttu-id="4b554-193">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-193">Get command:</span></span>     | [<span data-ttu-id="4b554-194">**glgetfloatv**</span><span class="sxs-lookup"><span data-stu-id="4b554-194">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="4b554-195"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>\_ \_ \_ lokaler \_ Viewer für GL-Light-Modell</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-195"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4b554-196">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-196">Description:</span></span>     | <span data-ttu-id="4b554-197">Viewer ist lokal</span><span class="sxs-lookup"><span data-stu-id="4b554-197">Viewer is local</span></span>                                                                  |
| <span data-ttu-id="4b554-198">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-198">Attribute group:</span></span> | <span data-ttu-id="4b554-199">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-199">lighting</span></span>                                                                         |
| <span data-ttu-id="4b554-200">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-200">Initial value:</span></span>   | <span data-ttu-id="4b554-201">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="4b554-201">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="4b554-202">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-202">Get command:</span></span>     | [<span data-ttu-id="4b554-203">**glgetbooleanv**</span><span class="sxs-lookup"><span data-stu-id="4b554-203">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="4b554-204"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL- \_ Light- \_ Modell auf \_ zwei \_ Seiten</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-204"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL\_LIGHT\_MODEL\_TWO\_SIDE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4b554-205">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-205">Description:</span></span>     | <span data-ttu-id="4b554-206">Verwenden der zweiseitigen Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="4b554-206">Use two-sided lighting</span></span>                                                           |
| <span data-ttu-id="4b554-207">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-207">Attribute group:</span></span> | <span data-ttu-id="4b554-208">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-208">lighting</span></span>                                                                         |
| <span data-ttu-id="4b554-209">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-209">Initial value:</span></span>   | <span data-ttu-id="4b554-210">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="4b554-210">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="4b554-211">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-211">Get command:</span></span>     | [<span data-ttu-id="4b554-212">**glgetbooleanv**</span><span class="sxs-lookup"><span data-stu-id="4b554-212">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="4b554-213"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL- \_ AMBIENT</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-213"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4b554-214">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-214">Description:</span></span>     | <span data-ttu-id="4b554-215">Umgebungs Intensität von Light *i*</span><span class="sxs-lookup"><span data-stu-id="4b554-215">Ambient intensity of light *i*</span></span>     |
| <span data-ttu-id="4b554-216">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-216">Attribute group:</span></span> | <span data-ttu-id="4b554-217">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-217">lighting</span></span>                           |
| <span data-ttu-id="4b554-218">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-218">Initial value:</span></span>   | <span data-ttu-id="4b554-219">(0,0, 0,0, 0,0, 1.0)</span><span class="sxs-lookup"><span data-stu-id="4b554-219">(0.0,0.0,0.0,1.0)</span></span>                  |
| <span data-ttu-id="4b554-220">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-220">Get command:</span></span>     | [<span data-ttu-id="4b554-221">**glgetlightfv**</span><span class="sxs-lookup"><span data-stu-id="4b554-221">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4b554-222"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL- \_ diffuses</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-222"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4b554-223">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-223">Description:</span></span>     | <span data-ttu-id="4b554-224">Diffuses Intensität von Light *i*</span><span class="sxs-lookup"><span data-stu-id="4b554-224">Diffuse intensity of light *i*</span></span>     |
| <span data-ttu-id="4b554-225">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-225">Attribute group:</span></span> | <span data-ttu-id="4b554-226">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-226">lighting</span></span>                           |
| <span data-ttu-id="4b554-227">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-227">Initial value:</span></span>   |                                    |
| <span data-ttu-id="4b554-228">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-228">Get command:</span></span>     | [<span data-ttu-id="4b554-229">**glgetlightfv**</span><span class="sxs-lookup"><span data-stu-id="4b554-229">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4b554-230"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL \_ Glanz</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-230"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4b554-231">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-231">Description:</span></span>     | <span data-ttu-id="4b554-232">Glanz Intensität von Light *i*</span><span class="sxs-lookup"><span data-stu-id="4b554-232">Specular intensity of light *i*</span></span>    |
| <span data-ttu-id="4b554-233">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-233">Attribute group:</span></span> | <span data-ttu-id="4b554-234">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-234">lighting</span></span>                           |
| <span data-ttu-id="4b554-235">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-235">Initial value:</span></span>   |                                    |
| <span data-ttu-id="4b554-236">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-236">Get command:</span></span>     | [<span data-ttu-id="4b554-237">**glgetlightfv**</span><span class="sxs-lookup"><span data-stu-id="4b554-237">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4b554-238"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>GL- \_ Position</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-238"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>GL\_POSITION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4b554-239">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-239">Description:</span></span>     | <span data-ttu-id="4b554-240">Position von Light *i*</span><span class="sxs-lookup"><span data-stu-id="4b554-240">Position of light *i*</span></span>              |
| <span data-ttu-id="4b554-241">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-241">Attribute group:</span></span> | <span data-ttu-id="4b554-242">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-242">lighting</span></span>                           |
| <span data-ttu-id="4b554-243">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-243">Initial value:</span></span>   | <span data-ttu-id="4b554-244">(0,0, 0,0, 1.0, 0,0)</span><span class="sxs-lookup"><span data-stu-id="4b554-244">(0.0,0.0,1.0,0.0)</span></span>                  |
| <span data-ttu-id="4b554-245">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-245">Get command:</span></span>     | [<span data-ttu-id="4b554-246">**glgetlightfv**</span><span class="sxs-lookup"><span data-stu-id="4b554-246">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4b554-247"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>GL- \_ Konstante \_ Dämpfung</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-247"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>GL\_CONSTANT\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4b554-248">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-248">Description:</span></span>     | <span data-ttu-id="4b554-249">Faktor für konstante Dämpfung</span><span class="sxs-lookup"><span data-stu-id="4b554-249">Constant attenuation factor</span></span>        |
| <span data-ttu-id="4b554-250">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-250">Attribute group:</span></span> | <span data-ttu-id="4b554-251">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-251">lighting</span></span>                           |
| <span data-ttu-id="4b554-252">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-252">Initial value:</span></span>   | <span data-ttu-id="4b554-253">1.0</span><span class="sxs-lookup"><span data-stu-id="4b554-253">1.0</span></span>                                |
| <span data-ttu-id="4b554-254">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-254">Get command:</span></span>     | [<span data-ttu-id="4b554-255">**glgetlightfv**</span><span class="sxs-lookup"><span data-stu-id="4b554-255">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4b554-256"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>\_lineare \_ Dämpfung von GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-256"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>GL\_LINEAR\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4b554-257">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-257">Description:</span></span>     | <span data-ttu-id="4b554-258">Faktor für lineare Dämpfung</span><span class="sxs-lookup"><span data-stu-id="4b554-258">Linear attenuation factor</span></span>          |
| <span data-ttu-id="4b554-259">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-259">Attribute group:</span></span> | <span data-ttu-id="4b554-260">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-260">lighting</span></span>                           |
| <span data-ttu-id="4b554-261">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-261">Initial value:</span></span>   | <span data-ttu-id="4b554-262">0,0</span><span class="sxs-lookup"><span data-stu-id="4b554-262">0.0</span></span>                                |
| <span data-ttu-id="4b554-263">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-263">Get command:</span></span>     | [<span data-ttu-id="4b554-264">**glgetlightfv**</span><span class="sxs-lookup"><span data-stu-id="4b554-264">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4b554-265"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>GL. \_ quadratische \_ Dämpfung</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-265"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>GL\_QUADRATIC\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4b554-266">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-266">Description:</span></span>     | <span data-ttu-id="4b554-267">Faktor für die quadratische Dämpfung</span><span class="sxs-lookup"><span data-stu-id="4b554-267">Quadratic attenuation factor</span></span>       |
| <span data-ttu-id="4b554-268">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-268">Attribute group:</span></span> | <span data-ttu-id="4b554-269">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-269">lighting</span></span>                           |
| <span data-ttu-id="4b554-270">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-270">Initial value:</span></span>   | <span data-ttu-id="4b554-271">0,0</span><span class="sxs-lookup"><span data-stu-id="4b554-271">0.0</span></span>                                |
| <span data-ttu-id="4b554-272">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-272">Get command:</span></span>     | [<span data-ttu-id="4b554-273">**glgetlightfv**</span><span class="sxs-lookup"><span data-stu-id="4b554-273">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4b554-274"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>GL- \_ Spot- \_ Richtung</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-274"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>GL\_SPOT\_DIRECTION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4b554-275">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-275">Description:</span></span>     | <span data-ttu-id="4b554-276">Spotlight-Richtung von Light *i*</span><span class="sxs-lookup"><span data-stu-id="4b554-276">Spotlight direction of light *i*</span></span>   |
| <span data-ttu-id="4b554-277">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-277">Attribute group:</span></span> | <span data-ttu-id="4b554-278">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-278">lighting</span></span>                           |
| <span data-ttu-id="4b554-279">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-279">Initial value:</span></span>   | <span data-ttu-id="4b554-280">(0,0, 0,0,-1,0)</span><span class="sxs-lookup"><span data-stu-id="4b554-280">(0.0,0.0,-1.0)</span></span>                     |
| <span data-ttu-id="4b554-281">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-281">Get command:</span></span>     | [<span data-ttu-id="4b554-282">**glgetlightfv**</span><span class="sxs-lookup"><span data-stu-id="4b554-282">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4b554-283"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>GL- \_ Spot- \_ Exponent</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-283"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>GL\_SPOT\_EXPONENT</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4b554-284">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-284">Description:</span></span>     | <span data-ttu-id="4b554-285">Spotlight-Exponent von Light *i*</span><span class="sxs-lookup"><span data-stu-id="4b554-285">Spotlight exponent of light *i*</span></span>    |
| <span data-ttu-id="4b554-286">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-286">Attribute group:</span></span> | <span data-ttu-id="4b554-287">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-287">lighting</span></span>                           |
| <span data-ttu-id="4b554-288">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-288">Initial value:</span></span>   | <span data-ttu-id="4b554-289">0,0</span><span class="sxs-lookup"><span data-stu-id="4b554-289">0.0</span></span>                                |
| <span data-ttu-id="4b554-290">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-290">Get command:</span></span>     | [<span data-ttu-id="4b554-291">**glgetlightfv**</span><span class="sxs-lookup"><span data-stu-id="4b554-291">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4b554-292"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL. \_ Spot- \_ cuumff</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-292"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL\_SPOT\_CUTOFF</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4b554-293">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-293">Description:</span></span>     | <span data-ttu-id="4b554-294">Spotlight-Winkel des Lichts *i*</span><span class="sxs-lookup"><span data-stu-id="4b554-294">Spotlight angle of light *i*</span></span>       |
| <span data-ttu-id="4b554-295">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-295">Attribute group:</span></span> | <span data-ttu-id="4b554-296">Belichtung</span><span class="sxs-lookup"><span data-stu-id="4b554-296">lighting</span></span>                           |
| <span data-ttu-id="4b554-297">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-297">Initial value:</span></span>   | <span data-ttu-id="4b554-298">180,0</span><span class="sxs-lookup"><span data-stu-id="4b554-298">180.0</span></span>                              |
| <span data-ttu-id="4b554-299">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-299">Get command:</span></span>     | [<span data-ttu-id="4b554-300">**glgetlightfv**</span><span class="sxs-lookup"><span data-stu-id="4b554-300">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4b554-301"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ Light *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-301"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL\_LIGHT *i*</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4b554-302">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-302">Description:</span></span>     | <span data-ttu-id="4b554-303">True, wenn Light *i* aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4b554-303">True if light *i* enabled</span></span>          |
| <span data-ttu-id="4b554-304">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-304">Attribute group:</span></span> | <span data-ttu-id="4b554-305">Beleuchtung/Aktivierung</span><span class="sxs-lookup"><span data-stu-id="4b554-305">lighting/enable</span></span>                    |
| <span data-ttu-id="4b554-306">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-306">Initial value:</span></span>   | <span data-ttu-id="4b554-307">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="4b554-307">GL\_FALSE</span></span>                          |
| <span data-ttu-id="4b554-308">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-308">Get command:</span></span>     | [<span data-ttu-id="4b554-309">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="4b554-309">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="4b554-310"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>GL- \_ Farb \_ Indizes</dt> </span><span class="sxs-lookup"><span data-stu-id="4b554-310"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>GL\_COLOR\_INDEXES</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="4b554-311">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="4b554-311">Description:</span></span>     | <span data-ttu-id="4b554-312">*C (a)*, *c (d)* und *c (s)* für die Farb Index Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="4b554-312">*C (a)*, *C (d)*, and *C (s)* for color-index lighting</span></span>                         |
| <span data-ttu-id="4b554-313">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="4b554-313">Attribute group:</span></span> | <span data-ttu-id="4b554-314">Beleuchtung/Aktivierung</span><span class="sxs-lookup"><span data-stu-id="4b554-314">lighting/enable</span></span>                                                                |
| <span data-ttu-id="4b554-315">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="4b554-315">Initial value:</span></span>   | <span data-ttu-id="4b554-316">0, 1, 1</span><span class="sxs-lookup"><span data-stu-id="4b554-316">0,1,1</span></span>                                                                          |
| <span data-ttu-id="4b554-317">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="4b554-317">Get command:</span></span>     | [<span data-ttu-id="4b554-318">**glgetfloatv**</span><span class="sxs-lookup"><span data-stu-id="4b554-318">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




