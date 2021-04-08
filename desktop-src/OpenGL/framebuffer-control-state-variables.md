---
title: Statusvariablen des Framebuffer-Steuer Elements
description: Statusvariablen des Framebuffer-Steuer Elements
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Framebuffer-Steuerelement Zustandsvariablen OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d44327858ae43212fcaa4364ed23045de5e0296f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857072"
---
# <a name="framebuffer-control-state-variables"></a><span data-ttu-id="a94e7-104">Statusvariablen des Framebuffer-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="a94e7-104">Framebuffer Control State Variables</span></span>

<dl> <span data-ttu-id="a94e7-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>GL- \_ Zeichnungs \_ Puffer</dt> </span><span class="sxs-lookup"><span data-stu-id="a94e7-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>GL\_DRAW\_BUFFER</dt> </span></span><dd> 

|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="a94e7-106">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="a94e7-106">Description:</span></span>     | <span data-ttu-id="a94e7-107">Puffer zum Zeichnen ausgewählt</span><span class="sxs-lookup"><span data-stu-id="a94e7-107">Buffers selected for drawing</span></span>           |
| <span data-ttu-id="a94e7-108">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="a94e7-108">Attribute group:</span></span> | <span data-ttu-id="a94e7-109">Farb Puffer</span><span class="sxs-lookup"><span data-stu-id="a94e7-109">color-buffer</span></span>                           |
| <span data-ttu-id="a94e7-110">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="a94e7-110">Initial value:</span></span>   |                                        |
| <span data-ttu-id="a94e7-111">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="a94e7-111">Get command:</span></span>     | [<span data-ttu-id="a94e7-112">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="a94e7-112">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="a94e7-113"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL- \_ Index- \_ Schreib Vorfrage</dt> </span><span class="sxs-lookup"><span data-stu-id="a94e7-113"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL\_INDEX\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a94e7-114">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="a94e7-114">Description:</span></span>     | <span data-ttu-id="a94e7-115">Farb Index-Schreib Vorfrage</span><span class="sxs-lookup"><span data-stu-id="a94e7-115">Color-index writemask</span></span>                                                            |
| <span data-ttu-id="a94e7-116">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="a94e7-116">Attribute group:</span></span> | <span data-ttu-id="a94e7-117">Farb Puffer</span><span class="sxs-lookup"><span data-stu-id="a94e7-117">color-buffer</span></span>                                                                     |
| <span data-ttu-id="a94e7-118">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="a94e7-118">Initial value:</span></span>   | <span data-ttu-id="a94e7-119">1</span><span class="sxs-lookup"><span data-stu-id="a94e7-119">1's</span></span>                                                                              |
| <span data-ttu-id="a94e7-120">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="a94e7-120">Get command:</span></span>     | [<span data-ttu-id="a94e7-121">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="a94e7-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a94e7-122"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL- \_ Farb \_ schreibfrage</dt> </span><span class="sxs-lookup"><span data-stu-id="a94e7-122"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL\_COLOR\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a94e7-123">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="a94e7-123">Description:</span></span>     | <span data-ttu-id="a94e7-124">Farbschreib Zugriff aktiviert; R, G, B oder a</span><span class="sxs-lookup"><span data-stu-id="a94e7-124">Color write enables; R, G, B, or A</span></span>                                               |
| <span data-ttu-id="a94e7-125">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="a94e7-125">Attribute group:</span></span> | <span data-ttu-id="a94e7-126">Farb Puffer</span><span class="sxs-lookup"><span data-stu-id="a94e7-126">color-buffer</span></span>                                                                     |
| <span data-ttu-id="a94e7-127">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="a94e7-127">Initial value:</span></span>   | <span data-ttu-id="a94e7-128">GL \_ true</span><span class="sxs-lookup"><span data-stu-id="a94e7-128">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="a94e7-129">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="a94e7-129">Get command:</span></span>     | [<span data-ttu-id="a94e7-130">**glgetbooleanv**</span><span class="sxs-lookup"><span data-stu-id="a94e7-130">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a94e7-131"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>\_ausführliche \_ Schreib vorschreibfrage</dt> </span><span class="sxs-lookup"><span data-stu-id="a94e7-131"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>GL\_DEPTH\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a94e7-132">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="a94e7-132">Description:</span></span>     | <span data-ttu-id="a94e7-133">Der für das Schreiben aktivierte tiefen Puffer</span><span class="sxs-lookup"><span data-stu-id="a94e7-133">Depth buffer enabled for writing</span></span>                                                 |
| <span data-ttu-id="a94e7-134">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="a94e7-134">Attribute group:</span></span> | <span data-ttu-id="a94e7-135">tiefen Puffer</span><span class="sxs-lookup"><span data-stu-id="a94e7-135">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="a94e7-136">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="a94e7-136">Initial value:</span></span>   | <span data-ttu-id="a94e7-137">GL \_ true</span><span class="sxs-lookup"><span data-stu-id="a94e7-137">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="a94e7-138">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="a94e7-138">Get command:</span></span>     | [<span data-ttu-id="a94e7-139">**glgetbooleanv**</span><span class="sxs-lookup"><span data-stu-id="a94e7-139">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a94e7-140"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL. \_ Schablonen \_ schreibfrage</dt> </span><span class="sxs-lookup"><span data-stu-id="a94e7-140"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL\_STENCIL\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a94e7-141">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="a94e7-141">Description:</span></span>     | <span data-ttu-id="a94e7-142">Schablone-Puffer schreibfrage</span><span class="sxs-lookup"><span data-stu-id="a94e7-142">Stencil-buffer writemask</span></span>                                                         |
| <span data-ttu-id="a94e7-143">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="a94e7-143">Attribute group:</span></span> | <span data-ttu-id="a94e7-144">Schablone-Puffer</span><span class="sxs-lookup"><span data-stu-id="a94e7-144">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="a94e7-145">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="a94e7-145">Initial value:</span></span>   | <span data-ttu-id="a94e7-146">1</span><span class="sxs-lookup"><span data-stu-id="a94e7-146">1's</span></span>                                                                              |
| <span data-ttu-id="a94e7-147">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="a94e7-147">Get command:</span></span>     | [<span data-ttu-id="a94e7-148">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="a94e7-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a94e7-149"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>Füllwert für GL- \_ Farbe \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="a94e7-149"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>GL\_COLOR\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a94e7-150">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="a94e7-150">Description:</span></span>     | <span data-ttu-id="a94e7-151">Unklarer Wert des Farb Puffers (RGBA-Modus)</span><span class="sxs-lookup"><span data-stu-id="a94e7-151">Color-buffer clear value (RGBA mode)</span></span>                                           |
| <span data-ttu-id="a94e7-152">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="a94e7-152">Attribute group:</span></span> | <span data-ttu-id="a94e7-153">Farb Puffer</span><span class="sxs-lookup"><span data-stu-id="a94e7-153">color-buffer</span></span>                                                                   |
| <span data-ttu-id="a94e7-154">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="a94e7-154">Initial value:</span></span>   | <span data-ttu-id="a94e7-155">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="a94e7-155">0, 0, 0, 0</span></span>                                                                     |
| <span data-ttu-id="a94e7-156">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="a94e7-156">Get command:</span></span>     | [<span data-ttu-id="a94e7-157">**glgetfloatv**</span><span class="sxs-lookup"><span data-stu-id="a94e7-157">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a94e7-158"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>Wert für GL- \_ Index \_ Löschen \_</dt> </span><span class="sxs-lookup"><span data-stu-id="a94e7-158"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>GL\_INDEX\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a94e7-159">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="a94e7-159">Description:</span></span>     | <span data-ttu-id="a94e7-160">Unklarer Wert des Farb Puffers (Farb Index Modus)</span><span class="sxs-lookup"><span data-stu-id="a94e7-160">Color-buffer clear value (color-index mode)</span></span>                                    |
| <span data-ttu-id="a94e7-161">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="a94e7-161">Attribute group:</span></span> | <span data-ttu-id="a94e7-162">Farb Puffer</span><span class="sxs-lookup"><span data-stu-id="a94e7-162">color-buffer</span></span>                                                                   |
| <span data-ttu-id="a94e7-163">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="a94e7-163">Initial value:</span></span>   | <span data-ttu-id="a94e7-164">0</span><span class="sxs-lookup"><span data-stu-id="a94e7-164">0</span></span>                                                                              |
| <span data-ttu-id="a94e7-165">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="a94e7-165">Get command:</span></span>     | [<span data-ttu-id="a94e7-166">**glgetfloatv**</span><span class="sxs-lookup"><span data-stu-id="a94e7-166">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a94e7-167"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL- \_ Tiefe \_ Clear- \_ Wert</dt> </span><span class="sxs-lookup"><span data-stu-id="a94e7-167"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL\_DEPTH\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a94e7-168">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="a94e7-168">Description:</span></span>     | <span data-ttu-id="a94e7-169">Tiefen Puffer-Clear-Wert</span><span class="sxs-lookup"><span data-stu-id="a94e7-169">Depth-buffer clear value</span></span>                                                         |
| <span data-ttu-id="a94e7-170">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="a94e7-170">Attribute group:</span></span> | <span data-ttu-id="a94e7-171">tiefen Puffer</span><span class="sxs-lookup"><span data-stu-id="a94e7-171">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="a94e7-172">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="a94e7-172">Initial value:</span></span>   | <span data-ttu-id="a94e7-173">1</span><span class="sxs-lookup"><span data-stu-id="a94e7-173">1</span></span>                                                                                |
| <span data-ttu-id="a94e7-174">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="a94e7-174">Get command:</span></span>     | [<span data-ttu-id="a94e7-175">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="a94e7-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a94e7-176"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>Lösch Wert für GL- \_ Schablone \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="a94e7-176"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>GL\_STENCIL\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a94e7-177">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="a94e7-177">Description:</span></span>     | <span data-ttu-id="a94e7-178">Stencil-Puffer Clear-Wert</span><span class="sxs-lookup"><span data-stu-id="a94e7-178">Stencil-buffer clear value</span></span>                                                       |
| <span data-ttu-id="a94e7-179">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="a94e7-179">Attribute group:</span></span> | <span data-ttu-id="a94e7-180">Schablone-Puffer</span><span class="sxs-lookup"><span data-stu-id="a94e7-180">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="a94e7-181">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="a94e7-181">Initial value:</span></span>   | <span data-ttu-id="a94e7-182">0</span><span class="sxs-lookup"><span data-stu-id="a94e7-182">0</span></span>                                                                                |
| <span data-ttu-id="a94e7-183">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="a94e7-183">Get command:</span></span>     | [<span data-ttu-id="a94e7-184">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="a94e7-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="a94e7-185"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>Wert für GL- \_ Accum \_ Clear \_</dt> </span><span class="sxs-lookup"><span data-stu-id="a94e7-185"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL\_ACCUM\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a94e7-186">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="a94e7-186">Description:</span></span>     | <span data-ttu-id="a94e7-187">Kumulations Puffer-Clear-Wert</span><span class="sxs-lookup"><span data-stu-id="a94e7-187">Accumulation-buffer clear value</span></span>                                                |
| <span data-ttu-id="a94e7-188">Attribut Gruppe:</span><span class="sxs-lookup"><span data-stu-id="a94e7-188">Attribute group:</span></span> | <span data-ttu-id="a94e7-189">Accum-Buffer</span><span class="sxs-lookup"><span data-stu-id="a94e7-189">accum-buffer</span></span>                                                                   |
| <span data-ttu-id="a94e7-190">Anfangswert:</span><span class="sxs-lookup"><span data-stu-id="a94e7-190">Initial value:</span></span>   | <span data-ttu-id="a94e7-191">0</span><span class="sxs-lookup"><span data-stu-id="a94e7-191">0</span></span>                                                                              |
| <span data-ttu-id="a94e7-192">Get-Befehl:</span><span class="sxs-lookup"><span data-stu-id="a94e7-192">Get command:</span></span>     | [<span data-ttu-id="a94e7-193">**glgetfloatv**</span><span class="sxs-lookup"><span data-stu-id="a94e7-193">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




