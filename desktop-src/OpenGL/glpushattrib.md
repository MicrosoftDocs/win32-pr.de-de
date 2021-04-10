---
title: glpushatpub-Funktion (GL. h)
description: Überträgt den Attribut Stapel.
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
keywords:
- glpushatpub-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPushAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bc15b85ddca3bdbe5f6774b5368c6f0cde8dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040291"
---
# <a name="glpushattrib-function"></a><span data-ttu-id="6bb71-104">glpushatpub-Funktion</span><span class="sxs-lookup"><span data-stu-id="6bb71-104">glPushAttrib function</span></span>

<span data-ttu-id="6bb71-105">Überträgt den Attribut Stapel.</span><span class="sxs-lookup"><span data-stu-id="6bb71-105">Pushes the attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb71-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bb71-106">Syntax</span></span>


```C++
void WINAPI glPushAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="6bb71-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bb71-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bb71-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="6bb71-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="6bb71-109">Eine Maske, die angibt, welche Attribute gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6bb71-109">A mask that indicates which attributes to save.</span></span> <span data-ttu-id="6bb71-110">Die symbolischen Masken Konstanten und Ihr zugeordneter OpenGL-Zustand lauten wie folgt (in den eingerückt ten Absätzen wird aufgelistet, welche Attribute gespeichert werden):</span><span class="sxs-lookup"><span data-stu-id="6bb71-110">The symbolic mask constants and their associated OpenGL state are as follows (the indented paragraphs list which attributes are saved):</span></span>

<dl> <dt>

<span data-ttu-id="6bb71-111"><span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>GL- \_ Accum- \_ Puffer \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-111"><span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>GL\_ACCUM\_BUFFER\_BIT</span></span> 
</dt> <dd>

<span data-ttu-id="6bb71-112">Wert für Kumulations Puffer Clear</span><span class="sxs-lookup"><span data-stu-id="6bb71-112">Accumulation buffer clear value</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-113"><span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>GL- \_ Farb \_ Puffer \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-113"><span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>GL\_COLOR\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-114">GL \_ alpha \_ Test Enable Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-114">GL\_ALPHA\_TEST enable bit</span></span>

<span data-ttu-id="6bb71-115">Alpha-Testfunktion und Verweis Wert</span><span class="sxs-lookup"><span data-stu-id="6bb71-115">Alpha test function and reference value</span></span>

<span data-ttu-id="6bb71-116">GL \_ Blend-Bit aktivieren</span><span class="sxs-lookup"><span data-stu-id="6bb71-116">GL\_BLEND enable bit</span></span>

<span data-ttu-id="6bb71-117">Mischen von Quell-und Zielfunktionen</span><span class="sxs-lookup"><span data-stu-id="6bb71-117">Blending source and destination functions</span></span>

<span data-ttu-id="6bb71-118">GL \_ Dither Enable Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-118">GL\_DITHER enable bit</span></span>

<span data-ttu-id="6bb71-119">GL- \_ Zeichnen- \_ Puffereinstellung</span><span class="sxs-lookup"><span data-stu-id="6bb71-119">GL\_DRAW\_BUFFER setting</span></span>

<span data-ttu-id="6bb71-120">GL \_ Logic \_ op Enable Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-120">GL\_LOGIC\_OP enable bit</span></span>

<span data-ttu-id="6bb71-121">Logik-op-Funktion</span><span class="sxs-lookup"><span data-stu-id="6bb71-121">Logic op function</span></span>

<span data-ttu-id="6bb71-122">Werte für den Farbmodus und den indexmodusmodus</span><span class="sxs-lookup"><span data-stu-id="6bb71-122">Color-mode and index-mode clear values</span></span>

<span data-ttu-id="6bb71-123">Beschreibe-und indexmodusschreibmodus</span><span class="sxs-lookup"><span data-stu-id="6bb71-123">Color-mode and index-mode writemasks</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-124"><span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>GL \_ Aktuelles \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-124"><span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>GL\_CURRENT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-125">Aktuelle RGBA-Farbe</span><span class="sxs-lookup"><span data-stu-id="6bb71-125">Current RGBA color</span></span>

<span data-ttu-id="6bb71-126">Aktueller Farbindex</span><span class="sxs-lookup"><span data-stu-id="6bb71-126">Current color index</span></span>

<span data-ttu-id="6bb71-127">Aktueller normaler Vektor</span><span class="sxs-lookup"><span data-stu-id="6bb71-127">Current normal vector</span></span>

<span data-ttu-id="6bb71-128">Aktuelle Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="6bb71-128">Current texture coordinates</span></span>

<span data-ttu-id="6bb71-129">Aktuelle Raster Position GL \_ aktuelle \_ Raster \_ Position \_ gültiges Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-129">Current raster position GL\_CURRENT\_RASTER\_POSITION\_VALID flag</span></span>

<span data-ttu-id="6bb71-130">RGBA-Farbe, die der aktuellen Raster Position zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="6bb71-130">RGBA color associated with current raster position</span></span>

<span data-ttu-id="6bb71-131">Der aktuellen Raster Position zugeordneter Farb Index.</span><span class="sxs-lookup"><span data-stu-id="6bb71-131">Color index associated with current raster position</span></span>

<span data-ttu-id="6bb71-132">Der aktuellen Raster Position zugeordnete Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="6bb71-132">Texture coordinates associated with current raster position</span></span>

<span data-ttu-id="6bb71-133">GL \_ Edge-Flag-Flag \_</span><span class="sxs-lookup"><span data-stu-id="6bb71-133">GL\_EDGE\_FLAG flag</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-134"><span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>GL- \_ Tiefe- \_ Puffer \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-134"><span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>GL\_DEPTH\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-135">GL- \_ tiefen \_ Test-Enable-Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-135">GL\_DEPTH\_TEST enable bit</span></span>

<span data-ttu-id="6bb71-136">Tiefen Puffer-Testfunktion</span><span class="sxs-lookup"><span data-stu-id="6bb71-136">Depth buffer test function</span></span>

<span data-ttu-id="6bb71-137">Tiefen Puffer-Clear-Wert</span><span class="sxs-lookup"><span data-stu-id="6bb71-137">Depth buffer clear value</span></span>

<span data-ttu-id="6bb71-138">GL- \_ tiefen \_ Schreibweise für das Aktivieren des Bits</span><span class="sxs-lookup"><span data-stu-id="6bb71-138">GL\_DEPTH\_WRITEMASK enable bit</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-139"><span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>GL \_ enable \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-139"><span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>GL\_ENABLE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-140">GL- \_ alpha- \_ TESTFLAG</span><span class="sxs-lookup"><span data-stu-id="6bb71-140">GL\_ALPHA\_TEST flag</span></span>

<span data-ttu-id="6bb71-141">GL \_ Auto \_ Normal Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-141">GL\_AUTO\_NORMAL flag</span></span>

<span data-ttu-id="6bb71-142">GL- \_ Blend-Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-142">GL\_BLEND flag</span></span>

<span data-ttu-id="6bb71-143">Bits für die benutzerdefinierbaren Clippingebenen aktivieren</span><span class="sxs-lookup"><span data-stu-id="6bb71-143">Enable bits for the user-definable clipping planes</span></span>

<span data-ttu-id="6bb71-144">GL- \_ Farb \_ Material</span><span class="sxs-lookup"><span data-stu-id="6bb71-144">GL\_COLOR\_MATERIAL</span></span>

<span data-ttu-id="6bb71-145">GL- \_ \_ cullface-Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-145">GL\_CULL\_FACE flag</span></span>

<span data-ttu-id="6bb71-146">GL- \_ tiefen \_ TESTFLAG</span><span class="sxs-lookup"><span data-stu-id="6bb71-146">GL\_DEPTH\_TEST flag</span></span>

<span data-ttu-id="6bb71-147">GL \_ Dither-Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-147">GL\_DITHER flag</span></span>

<span data-ttu-id="6bb71-148">GL- \_ nebelflag</span><span class="sxs-lookup"><span data-stu-id="6bb71-148">GL\_FOG flag</span></span>

<span data-ttu-id="6bb71-149">GL \_ Light *i* WHERE 0 <= *i* < GL \_ Max \_ Lights</span><span class="sxs-lookup"><span data-stu-id="6bb71-149">GL\_LIGHT *i* where 0 <= *i* < GL\_MAX\_LIGHTS</span></span>

<span data-ttu-id="6bb71-150">GL- \_ Beleuchtungs Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-150">GL\_LIGHTING flag</span></span>

<span data-ttu-id="6bb71-151">Glättung für GL- \_ Linie \_</span><span class="sxs-lookup"><span data-stu-id="6bb71-151">GL\_LINE\_SMOOTH flag</span></span>

<span data-ttu-id="6bb71-152">GL-Zeilen Kennzeichen- \_ \_ Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-152">GL\_LINE\_STIPPLE flag</span></span>

<span data-ttu-id="6bb71-153">GL \_ Color \_ Logic \_ op-Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-153">GL\_COLOR\_LOGIC\_OP flag</span></span>

<span data-ttu-id="6bb71-154">GL- \_ Index \_ Logik-op- \_ Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-154">GL\_INDEX\_LOGIC\_OP flag</span></span>

<span data-ttu-id="6bb71-155">GL \_ zuordnung1 \_ x, wobei x ein Kartentyp ist</span><span class="sxs-lookup"><span data-stu-id="6bb71-155">GL\_MAP1\_x where x is a map type</span></span>

<span data-ttu-id="6bb71-156">GL \_ map2 \_ x, wobei x ein Kartentyp ist</span><span class="sxs-lookup"><span data-stu-id="6bb71-156">GL\_MAP2\_x where x is a map type</span></span>

<span data-ttu-id="6bb71-157">GL \_ normalize-Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-157">GL\_NORMALIZE flag</span></span>

<span data-ttu-id="6bb71-158">GL- \_ Punkt- \_ Smooth-Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-158">GL\_POINT\_SMOOTH flag</span></span>

<span data-ttu-id="6bb71-159">GL- \_ Polygon- \_ offsesettyp \_</span><span class="sxs-lookup"><span data-stu-id="6bb71-159">GL\_POLYGON\_OFFSET\_LINE flag</span></span>

<span data-ttu-id="6bb71-160">Füllflag für GL- \_ Polygon- \_ Offset \_</span><span class="sxs-lookup"><span data-stu-id="6bb71-160">GL\_POLYGON\_OFFSET\_FILL flag</span></span>

<span data-ttu-id="6bb71-161">GL- \_ Polygon- \_ \_ offpunktflag</span><span class="sxs-lookup"><span data-stu-id="6bb71-161">GL\_POLYGON\_OFFSET\_POINT flag</span></span>

<span data-ttu-id="6bb71-162">GL- \_ Polygon- \_ Smooth-Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-162">GL\_POLYGON\_SMOOTH flag</span></span>

<span data-ttu-id="6bb71-163">GL- \_ Polygon- \_ stippflag</span><span class="sxs-lookup"><span data-stu-id="6bb71-163">GL\_POLYGON\_STIPPLE flag</span></span>

<span data-ttu-id="6bb71-164">TESTFLAG für GL- \_ Scissor \_</span><span class="sxs-lookup"><span data-stu-id="6bb71-164">GL\_SCISSOR\_TEST flag</span></span>

<span data-ttu-id="6bb71-165">GL- \_ Schablone- \_ TESTFLAG</span><span class="sxs-lookup"><span data-stu-id="6bb71-165">GL\_STENCIL\_TEST flag</span></span>

<span data-ttu-id="6bb71-166">GL \_ Texture \_ 1D-Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-166">GL\_TEXTURE\_1D flag</span></span>

<span data-ttu-id="6bb71-167">GL \_ Texture \_ 2D-Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-167">GL\_TEXTURE\_2D flag</span></span>

<span data-ttu-id="6bb71-168">Flags GL \_ Textur \_ gen \_ x, wobei x S, T, R oder Q ist</span><span class="sxs-lookup"><span data-stu-id="6bb71-168">Flags GL\_TEXTURE\_GEN\_x where x is S, T, R, or Q</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-169"><span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>GL- \_ eval- \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-169"><span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>GL\_EVAL\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-170">GL \_ zuordnung1 \_ x enable Bits, wobei x ein Kartentyp ist</span><span class="sxs-lookup"><span data-stu-id="6bb71-170">GL\_MAP1\_x enable bits, where x is a map type</span></span>

<span data-ttu-id="6bb71-171">GL \_ map2 \_ x enable Bits, wobei x ein Kartentyp ist</span><span class="sxs-lookup"><span data-stu-id="6bb71-171">GL\_MAP2\_x enable bits, where x is a map type</span></span>

<span data-ttu-id="6bb71-172">1D-Raster Endpunkte und-Abteilungen</span><span class="sxs-lookup"><span data-stu-id="6bb71-172">1-D grid endpoints and divisions</span></span>

<span data-ttu-id="6bb71-173">2D-Raster Endpunkte und-Abteilungen</span><span class="sxs-lookup"><span data-stu-id="6bb71-173">2-D grid endpoints and divisions</span></span>

<span data-ttu-id="6bb71-174">GL \_ Auto \_ Normal Enable-Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-174">GL\_AUTO\_NORMAL enable bit</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-175"><span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>GL \_ - \_ nebelbit</span><span class="sxs-lookup"><span data-stu-id="6bb71-175"><span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>GL\_FOG\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-176">GL- \_ Nebel-Aktivierungsflag</span><span class="sxs-lookup"><span data-stu-id="6bb71-176">GL\_FOG enable flag</span></span>

<span data-ttu-id="6bb71-177">Nebelfarbe</span><span class="sxs-lookup"><span data-stu-id="6bb71-177">Fog color</span></span>

<span data-ttu-id="6bb71-178">Nebeldichte</span><span class="sxs-lookup"><span data-stu-id="6bb71-178">Fog density</span></span>

<span data-ttu-id="6bb71-179">Linearer Nebel Anfang</span><span class="sxs-lookup"><span data-stu-id="6bb71-179">Linear fog start</span></span>

<span data-ttu-id="6bb71-180">Lineare Nebel Ende</span><span class="sxs-lookup"><span data-stu-id="6bb71-180">Linear fog end</span></span>

<span data-ttu-id="6bb71-181">Nebelindex</span><span class="sxs-lookup"><span data-stu-id="6bb71-181">Fog index</span></span>

<span data-ttu-id="6bb71-182">GL \_ - \_ nebelmoduswert</span><span class="sxs-lookup"><span data-stu-id="6bb71-182">GL\_FOG\_MODE value</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-183"><span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>GL- \_ Hinweis \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-183"><span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>GL\_HINT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-184">GL- \_ Perspektiven \_ Korrektur- \_ Hinweis Einstellung</span><span class="sxs-lookup"><span data-stu-id="6bb71-184">GL\_PERSPECTIVE\_CORRECTION\_HINT setting</span></span>

<span data-ttu-id="6bb71-185">GL- \_ Punkt- \_ Smooth Hint- \_ Einstellung</span><span class="sxs-lookup"><span data-stu-id="6bb71-185">GL\_POINT\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="6bb71-186">\_ \_ Smooth Hint- \_ Einstellung für GL-Linie</span><span class="sxs-lookup"><span data-stu-id="6bb71-186">GL\_LINE\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="6bb71-187">GL- \_ Polygon- \_ Smooth Hint- \_ Einstellung</span><span class="sxs-lookup"><span data-stu-id="6bb71-187">GL\_POLYGON\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="6bb71-188">GL- \_ Nebel- \_ Hinweis Einstellung</span><span class="sxs-lookup"><span data-stu-id="6bb71-188">GL\_FOG\_HINT setting</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-189"><span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>GL- \_ Beleuchtungs \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-189"><span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>GL\_LIGHTING\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-190">GL- \_ Farb \_ Material, Enable Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-190">GL\_COLOR\_MATERIAL enable bit</span></span>

<span data-ttu-id="6bb71-191">Wert für GL- \_ Farb \_ Material \_ Gesicht</span><span class="sxs-lookup"><span data-stu-id="6bb71-191">GL\_COLOR\_MATERIAL\_FACE value</span></span>

<span data-ttu-id="6bb71-192">Farb Materialparameter zum Nachverfolgen der aktuellen Farbe</span><span class="sxs-lookup"><span data-stu-id="6bb71-192">Color material parameters that are tracking the current color</span></span>

<span data-ttu-id="6bb71-193">Ambiente-Szene Farbe</span><span class="sxs-lookup"><span data-stu-id="6bb71-193">Ambient scene color</span></span>

<span data-ttu-id="6bb71-194">\_Wert des \_ \_ Werts für den lokalen GL-lichtmodell \_</span><span class="sxs-lookup"><span data-stu-id="6bb71-194">GL\_LIGHT\_MODEL\_LOCAL\_VIEWER value</span></span>

<span data-ttu-id="6bb71-195">Das GL- \_ Light- \_ Modell mit \_ zwei \_ seitigen Einstellungen</span><span class="sxs-lookup"><span data-stu-id="6bb71-195">GL\_LIGHT\_MODEL\_TWO\_SIDE setting</span></span>

<span data-ttu-id="6bb71-196">GL- \_ Beleuchtung-Bit aktivieren</span><span class="sxs-lookup"><span data-stu-id="6bb71-196">GL\_LIGHTING enable bit</span></span>

<span data-ttu-id="6bb71-197">Bits für jedes Licht aktivieren</span><span class="sxs-lookup"><span data-stu-id="6bb71-197">Enable bit for each light</span></span>

<span data-ttu-id="6bb71-198">Ambient, diffuses und Glanz Intensität für jedes Licht</span><span class="sxs-lookup"><span data-stu-id="6bb71-198">Ambient, diffuse, and specular intensity for each light</span></span>

<span data-ttu-id="6bb71-199">Richtung, Position, Exponent und Umdrehungs Winkel für jede Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="6bb71-199">Direction, position, exponent, and cutoff angle for each light</span></span>

<span data-ttu-id="6bb71-200">Konstante, lineare und quadratische Dämpfungsfaktoren für jede Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="6bb71-200">Constant, linear, and quadratic attenuation factors for each light</span></span>

<span data-ttu-id="6bb71-201">Ambient, diffuse, Glanz und selbst leuchtendes Farbe für jedes Material</span><span class="sxs-lookup"><span data-stu-id="6bb71-201">Ambient, diffuse, specular, and emissive color for each material</span></span>

<span data-ttu-id="6bb71-202">Ambient-, diffuse und Glanz Farben Indizes für jedes Material</span><span class="sxs-lookup"><span data-stu-id="6bb71-202">Ambient, diffuse, and specular color indexes for each material</span></span>

<span data-ttu-id="6bb71-203">Glanz Exponent für jede Material- \_ Schattierung- \_ Modell Einstellung</span><span class="sxs-lookup"><span data-stu-id="6bb71-203">Specular exponent for each material GL\_SHADE\_MODEL setting</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-204"><span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>GL \_ - \_ linienbit</span><span class="sxs-lookup"><span data-stu-id="6bb71-204"><span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>GL\_LINE\_BIT</span></span> 
</dt> <dd>

<span data-ttu-id="6bb71-205">Glättung für GL- \_ Linie \_</span><span class="sxs-lookup"><span data-stu-id="6bb71-205">GL\_LINE\_SMOOTH flag</span></span>

<span data-ttu-id="6bb71-206">Bereich für GL- \_ Zeilen- \_ Stippel aktivieren</span><span class="sxs-lookup"><span data-stu-id="6bb71-206">GL\_LINE\_STIPPLE enable bit</span></span>

<span data-ttu-id="6bb71-207">Zeilen stippingmuster und Wiederholungs Counter</span><span class="sxs-lookup"><span data-stu-id="6bb71-207">Line stipple pattern and repeat counter</span></span>

<span data-ttu-id="6bb71-208">Linienstärke</span><span class="sxs-lookup"><span data-stu-id="6bb71-208">Line width</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-209"><span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>GL- \_ Listen \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-209"><span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>GL\_LIST\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-210">\_ \_ Basis Einstellung der GL-Liste</span><span class="sxs-lookup"><span data-stu-id="6bb71-210">GL\_LIST\_BASE setting</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-211"><span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>GL- \_ Pixel \_ Modus- \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-211"><span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>GL\_PIXEL\_MODE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-212">GL. \_ Rote \_ Bias und GL-Einstellungen für die \_ Rote \_ Skala</span><span class="sxs-lookup"><span data-stu-id="6bb71-212">GL\_RED\_BIAS and GL\_RED\_SCALE settings</span></span>

<span data-ttu-id="6bb71-213">GL \_ \_ -grüner Bias und GL- \_ grün \_ Skalierungs Werte</span><span class="sxs-lookup"><span data-stu-id="6bb71-213">GL\_GREEN\_BIAS and GL\_GREEN\_SCALE values</span></span>

<span data-ttu-id="6bb71-214">GL \_ Blue \_ Bias und GL \_ Blue \_ Scale</span><span class="sxs-lookup"><span data-stu-id="6bb71-214">GL\_BLUE\_BIAS and GL\_BLUE\_SCALE</span></span>

<span data-ttu-id="6bb71-215">GL \_ \_ -Alpha-Bias und GL- \_ alpha \_ Skala</span><span class="sxs-lookup"><span data-stu-id="6bb71-215">GL\_ALPHA\_BIAS and GL\_ALPHA\_SCALE</span></span>

<span data-ttu-id="6bb71-216">GL \_ \_ -Tiefe und GL- \_ tiefen \_ Skala</span><span class="sxs-lookup"><span data-stu-id="6bb71-216">GL\_DEPTH\_BIAS and GL\_DEPTH\_SCALE</span></span>

<span data-ttu-id="6bb71-217">Werte für GL \_ \_ -Index Offset und GL- \_ Index \_ Verschiebung</span><span class="sxs-lookup"><span data-stu-id="6bb71-217">GL\_INDEX\_OFFSET and GL\_INDEX\_SHIFT values</span></span>

<span data-ttu-id="6bb71-218">GL \_ \_ -Kartenfarbe und GL- \_ Karten- \_ Stencil-Flags</span><span class="sxs-lookup"><span data-stu-id="6bb71-218">GL\_MAP\_COLOR and GL\_MAP\_STENCIL flags</span></span>

<span data-ttu-id="6bb71-219">\_Y Zoom \_ X-und GL \_ Zoom-Y- \_ Faktoren</span><span class="sxs-lookup"><span data-stu-id="6bb71-219">GL\_ZOOM\_X and GL\_ZOOM\_Y factors</span></span>

<span data-ttu-id="6bb71-220">GL- \_ Lese \_ Puffereinstellung</span><span class="sxs-lookup"><span data-stu-id="6bb71-220">GL\_READ\_BUFFER setting</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-221"><span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>GL \_ - \_ punktbit</span><span class="sxs-lookup"><span data-stu-id="6bb71-221"><span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>GL\_POINT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-222">GL- \_ Punkt- \_ Smooth-Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-222">GL\_POINT\_SMOOTH flag</span></span>

<span data-ttu-id="6bb71-223">Punktgröße</span><span class="sxs-lookup"><span data-stu-id="6bb71-223">Point size</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-224"><span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>GL- \_ Polygon- \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-224"><span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>GL\_POLYGON\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-225">GL. \_ \_ gesichtbit aktivieren</span><span class="sxs-lookup"><span data-stu-id="6bb71-225">GL\_CULL\_FACE enable bit</span></span>

<span data-ttu-id="6bb71-226">Wert des GL- \_ cull- \_ Gesichts \_ Modus</span><span class="sxs-lookup"><span data-stu-id="6bb71-226">GL\_CULL\_FACE\_MODE value</span></span>

<span data-ttu-id="6bb71-227">GL- \_ Front- \_ Face-Indikator</span><span class="sxs-lookup"><span data-stu-id="6bb71-227">GL\_FRONT\_FACE indicator</span></span>

<span data-ttu-id="6bb71-228">Einstellung des GL- \_ Polygon \_ Modus</span><span class="sxs-lookup"><span data-stu-id="6bb71-228">GL\_POLYGON\_MODE setting</span></span>

<span data-ttu-id="6bb71-229">GL- \_ Polygon- \_ Smooth-Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-229">GL\_POLYGON\_SMOOTH flag</span></span>

<span data-ttu-id="6bb71-230">GL- \_ Polygon- \_ Stippel aktivieren (Bit)</span><span class="sxs-lookup"><span data-stu-id="6bb71-230">GL\_POLYGON\_STIPPLE enable bit</span></span>

<span data-ttu-id="6bb71-231">Füllflag für GL- \_ Polygon- \_ Offset \_</span><span class="sxs-lookup"><span data-stu-id="6bb71-231">GL\_POLYGON\_OFFSET\_FILL flag</span></span>

<span data-ttu-id="6bb71-232">GL- \_ Polygon- \_ offsesettyp \_</span><span class="sxs-lookup"><span data-stu-id="6bb71-232">GL\_POLYGON\_OFFSET\_LINE flag</span></span>

<span data-ttu-id="6bb71-233">GL- \_ Polygon- \_ \_ offpunktflag</span><span class="sxs-lookup"><span data-stu-id="6bb71-233">GL\_POLYGON\_OFFSET\_POINT flag</span></span>

<span data-ttu-id="6bb71-234">GL- \_ Polygon- \_ Offset \_ Faktor</span><span class="sxs-lookup"><span data-stu-id="6bb71-234">GL\_POLYGON\_OFFSET\_FACTOR</span></span>

<span data-ttu-id="6bb71-235">GL- \_ Polygon- \_ Offset \_ Einheiten</span><span class="sxs-lookup"><span data-stu-id="6bb71-235">GL\_POLYGON\_OFFSET\_UNITS</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-236"><span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>GL- \_ Polygon- \_ Stippel \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-236"><span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>GL\_POLYGON\_STIPPLE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-237">Polygon-Stippel Bild</span><span class="sxs-lookup"><span data-stu-id="6bb71-237">Polygon stipple image</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-238"><span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>GL- \_ Scheren- \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-238"><span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>GL\_SCISSOR\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-239">TESTFLAG für GL- \_ Scissor \_</span><span class="sxs-lookup"><span data-stu-id="6bb71-239">GL\_SCISSOR\_TEST flag</span></span>

<span data-ttu-id="6bb71-240">Scissor-Feld</span><span class="sxs-lookup"><span data-stu-id="6bb71-240">Scissor box</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-241"><span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>GL- \_ Schablone- \_ Puffer \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-241"><span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>GL\_STENCIL\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-242">GL- \_ Schablone-Test-enable- \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-242">GL\_STENCIL\_TEST enable bit</span></span>

<span data-ttu-id="6bb71-243">Schablonen Funktion und Verweis Wert</span><span class="sxs-lookup"><span data-stu-id="6bb71-243">Stencil function and reference value</span></span>

<span data-ttu-id="6bb71-244">Schablone-Wert Maske</span><span class="sxs-lookup"><span data-stu-id="6bb71-244">Stencil value mask</span></span>

<span data-ttu-id="6bb71-245">Fehler-, Pass-und Tiefe Puffer Pass Aktionen der Schablone</span><span class="sxs-lookup"><span data-stu-id="6bb71-245">Stencil fail, pass, and depth buffer pass actions</span></span>

<span data-ttu-id="6bb71-246">Unklarer Wert für Schablonen Puffer</span><span class="sxs-lookup"><span data-stu-id="6bb71-246">Stencil buffer clear value</span></span>

<span data-ttu-id="6bb71-247">Beschreibe-pufferfrage</span><span class="sxs-lookup"><span data-stu-id="6bb71-247">Stencil buffer writemask</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-248"><span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>GL- \_ Textur \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-248"><span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>GL\_TEXTURE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-249">Bits für die vier Texturkoordinaten aktivieren</span><span class="sxs-lookup"><span data-stu-id="6bb71-249">Enable bits for the four texture coordinates</span></span>

<span data-ttu-id="6bb71-250">Rahmenfarbe für jedes Textur Bild</span><span class="sxs-lookup"><span data-stu-id="6bb71-250">Border color for each texture image</span></span>

<span data-ttu-id="6bb71-251">Minification-Funktion für jedes Textur Bild</span><span class="sxs-lookup"><span data-stu-id="6bb71-251">Minification function for each texture image</span></span>

<span data-ttu-id="6bb71-252">Vergrößerungsfunktion für jedes Textur Bild</span><span class="sxs-lookup"><span data-stu-id="6bb71-252">Magnification function for each texture image</span></span>

<span data-ttu-id="6bb71-253">Texturkoordinaten und Umbruch Modus für jedes Textur Bild</span><span class="sxs-lookup"><span data-stu-id="6bb71-253">Texture coordinates and wrap mode for each texture image</span></span>

<span data-ttu-id="6bb71-254">Farbe und Modus für jede Textur Umgebung</span><span class="sxs-lookup"><span data-stu-id="6bb71-254">Color and mode for each texture environment</span></span>

<span data-ttu-id="6bb71-255">Bits GL- \_ Textur \_ gen \_ *x* aktivieren; *x* ist S, T, R und Q</span><span class="sxs-lookup"><span data-stu-id="6bb71-255">Enable bits GL\_TEXTURE\_GEN\_*x*; *x* is S, T, R, and Q</span></span>

<span data-ttu-id="6bb71-256">GL \_ \_ -Textur gen \_ -Modus-Einstellung für S, T, R und Q</span><span class="sxs-lookup"><span data-stu-id="6bb71-256">GL\_TEXTURE\_GEN\_MODE setting for S, T, R, and Q</span></span>

<span data-ttu-id="6bb71-257">auf gltexgen-Ebenen Gleichungen für S, T, R und Q</span><span class="sxs-lookup"><span data-stu-id="6bb71-257">glTexGen plane equations for S, T, R, and Q</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-258"><span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>GL- \_ Transform- \_ Bit</span><span class="sxs-lookup"><span data-stu-id="6bb71-258"><span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>GL\_TRANSFORM\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-259">Koeffizienten der sechs Clipping-Ebenen</span><span class="sxs-lookup"><span data-stu-id="6bb71-259">Coefficients of the six clipping planes</span></span>

<span data-ttu-id="6bb71-260">Bits für die benutzerdefinierbaren Clippingebenen aktivieren</span><span class="sxs-lookup"><span data-stu-id="6bb71-260">Enable bits for the user-definable clipping planes</span></span>

<span data-ttu-id="6bb71-261">Wert des GL- \_ Matrix \_ Modus</span><span class="sxs-lookup"><span data-stu-id="6bb71-261">GL\_MATRIX\_MODE value</span></span>

<span data-ttu-id="6bb71-262">GL \_ normalize-Flag</span><span class="sxs-lookup"><span data-stu-id="6bb71-262">GL\_NORMALIZE flag</span></span>

</dd> <dt>

<span data-ttu-id="6bb71-263"><span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>GL- \_ \_ viewportbit</span><span class="sxs-lookup"><span data-stu-id="6bb71-263"><span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>GL\_VIEWPORT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="6bb71-264">Tiefenbereich (nah und weit)</span><span class="sxs-lookup"><span data-stu-id="6bb71-264">Depth range (near and far)</span></span>

<span data-ttu-id="6bb71-265">Ursprung und Block des Viewports</span><span class="sxs-lookup"><span data-stu-id="6bb71-265">Viewport origin and extent</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bb71-266">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6bb71-266">Return value</span></span>

<span data-ttu-id="6bb71-267">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6bb71-267">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6bb71-268">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="6bb71-268">Error codes</span></span>

<span data-ttu-id="6bb71-269">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6bb71-269">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6bb71-270">Name</span><span class="sxs-lookup"><span data-stu-id="6bb71-270">Name</span></span>                                                                                                  | <span data-ttu-id="6bb71-271">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6bb71-271">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6bb71-272"><dt>**GL- \_ Stapel \_ Überlauf**</dt></span><span class="sxs-lookup"><span data-stu-id="6bb71-272"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="6bb71-273">Die Funktion wurde aufgerufen, während der Attribut Stapel voll war.</span><span class="sxs-lookup"><span data-stu-id="6bb71-273">The function was called while the attribute stack was full.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="6bb71-274"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="6bb71-274"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6bb71-275">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6bb71-275">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6bb71-276">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6bb71-276">Remarks</span></span>

<span data-ttu-id="6bb71-277">Die Funktion " **glpushatpub** " erfordert ein Argument, eine Maske, die angibt, welche Gruppen von Zustandsvariablen im Attribut Stapel gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6bb71-277">The **glPushAttrib** function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack.</span></span> <span data-ttu-id="6bb71-278">Symbolische Konstanten werden verwendet, um Bits in der Maske festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6bb71-278">Symbolic constants are used to set bits in the mask.</span></span> <span data-ttu-id="6bb71-279">Der mask-Parameter wird in der Regel erstellt, indem der logische **or** -Vorgang auf mehrere dieser Konstanten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bb71-279">The mask parameter is typically constructed by applying the logical **OR** operation to several of these constants.</span></span> <span data-ttu-id="6bb71-280">Sie können den Wert "Special Mask GL \_ All \_ atzb" verwenden \_ , um alle Stackable-Zustände zu speichern.</span><span class="sxs-lookup"><span data-stu-id="6bb71-280">You can use the special mask GL\_ALL\_ATTRIB\_BITS to save all stackable states.</span></span>

<span data-ttu-id="6bb71-281">Die Funktion " [**glpopatpub**](glpopattrib.md) " stellt die Werte der Zustandsvariablen wieder her, die mit dem letzten Befehl " **glpushatpub** " gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="6bb71-281">The [**glPopAttrib**](glpopattrib.md) function restores the values of the state variables saved with the last **glPushAttrib** command.</span></span> <span data-ttu-id="6bb71-282">Die nicht gespeicherten Änderungen bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="6bb71-282">Those not saved are left unchanged.</span></span>

<span data-ttu-id="6bb71-283">Es ist ein Fehler, Attribute auf einen vollständigen Stapel zu übersetzen oder Attribute aus einem leeren Stapel zu Pop.</span><span class="sxs-lookup"><span data-stu-id="6bb71-283">It is an error to push attributes onto a full stack, or to pop attributes off an empty stack.</span></span> <span data-ttu-id="6bb71-284">In beiden Fällen wird das Fehlerflag festgelegt, und es wird keine andere Änderung am OpenGL-Zustand vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="6bb71-284">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="6bb71-285">Der Attribut Stapel ist zunächst leer.</span><span class="sxs-lookup"><span data-stu-id="6bb71-285">Initially, the attribute stack is empty.</span></span>

<span data-ttu-id="6bb71-286">Nicht alle Werte für den OpenGL-Zustand können im Attribut Stapel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="6bb71-286">Not all values for the OpenGL state can be saved on the attribute stack.</span></span> <span data-ttu-id="6bb71-287">Sie können z. b. das Pixel Paket nicht speichern und den Zustand des rendermoduszustands sowie den Zustand "Status" und "Feedback" auswählen.</span><span class="sxs-lookup"><span data-stu-id="6bb71-287">For example, you cannot save pixel pack and unpack state, render mode state, and select and feedback state.</span></span>

<span data-ttu-id="6bb71-288">Die Tiefe des Attribut Stapels hängt von der Implementierung ab, muss jedoch mindestens 16 sein.</span><span class="sxs-lookup"><span data-stu-id="6bb71-288">The depth of the attribute stack depends on the implementation, but it must be at least 16.</span></span>

<span data-ttu-id="6bb71-289">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glpushatpub** und [**glpopatpub**](glpopattrib.md)ab:</span><span class="sxs-lookup"><span data-stu-id="6bb71-289">The following functions retrieve information related to **glPushAttrib** and [**glPopAttrib**](glpopattrib.md):</span></span>

<span data-ttu-id="6bb71-290">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit der \_ \_ Stapel \_ Tiefe des Argument-GL</span><span class="sxs-lookup"><span data-stu-id="6bb71-290">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="6bb71-291">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit der \_ maximalen \_ attrb- \_ Stapel \_ Tiefe des Arguments</span><span class="sxs-lookup"><span data-stu-id="6bb71-291">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb71-292">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bb71-292">Requirements</span></span>



| <span data-ttu-id="6bb71-293">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6bb71-293">Requirement</span></span> | <span data-ttu-id="6bb71-294">Wert</span><span class="sxs-lookup"><span data-stu-id="6bb71-294">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb71-295">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6bb71-295">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb71-296">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bb71-296">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6bb71-297">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6bb71-297">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb71-298">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bb71-298">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6bb71-299">Header</span><span class="sxs-lookup"><span data-stu-id="6bb71-299">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bb71-300"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bb71-300"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6bb71-301">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6bb71-301">Library</span></span><br/>                  | <dl> <span data-ttu-id="6bb71-302"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bb71-302"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6bb71-303">DLL</span><span class="sxs-lookup"><span data-stu-id="6bb71-303">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bb71-304"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bb71-304"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb71-305">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6bb71-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb71-306">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6bb71-306">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6bb71-307">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6bb71-307">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6bb71-308">**glget**</span><span class="sxs-lookup"><span data-stu-id="6bb71-308">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="6bb71-309">**glgetclipplane**</span><span class="sxs-lookup"><span data-stu-id="6bb71-309">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="6bb71-310">**glgeterror**</span><span class="sxs-lookup"><span data-stu-id="6bb71-310">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="6bb71-311">**glgetlight**</span><span class="sxs-lookup"><span data-stu-id="6bb71-311">**glGetLight**</span></span>](glgetlight.md)
</dt> <dt>

[<span data-ttu-id="6bb71-312">**glgetmap**</span><span class="sxs-lookup"><span data-stu-id="6bb71-312">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="6bb71-313">**glgetmaterial**</span><span class="sxs-lookup"><span data-stu-id="6bb71-313">**glGetMaterial**</span></span>](glgetmaterial.md)
</dt> <dt>

[<span data-ttu-id="6bb71-314">**glgetpixelmap**</span><span class="sxs-lookup"><span data-stu-id="6bb71-314">**glGetPixelMap**</span></span>](glgetpixelmap.md)
</dt> <dt>

[<span data-ttu-id="6bb71-315">**glgetpolygonstippel**</span><span class="sxs-lookup"><span data-stu-id="6bb71-315">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="6bb71-316">**glgetstring**</span><span class="sxs-lookup"><span data-stu-id="6bb71-316">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="6bb71-317">**glgettex-v**</span><span class="sxs-lookup"><span data-stu-id="6bb71-317">**glGetTexEnv**</span></span>](glgettexenv.md)
</dt> <dt>

[<span data-ttu-id="6bb71-318">**glgettexgen**</span><span class="sxs-lookup"><span data-stu-id="6bb71-318">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="6bb71-319">**glgetteximage**</span><span class="sxs-lookup"><span data-stu-id="6bb71-319">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="6bb71-320">**glgettexlevelparameter**</span><span class="sxs-lookup"><span data-stu-id="6bb71-320">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="6bb71-321">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="6bb71-321">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="6bb71-322">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="6bb71-322">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





