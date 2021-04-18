---
title: Header Anmerkungen
description: Header Anmerkungen beschreiben, wie eine Funktion Ihre Parameter und den Rückgabewert verwendet.
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- Windows-API, Header Datei Anmerkungen
- Header Datei Anmerkungen
- Specstrings. h
- Standard Anmerkung (Language, SAL)
- _bcount
- _deref
- _deref_opt
- _ecount
- _full
- _in
- _inout
- _opt
- _out
- _part
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8535118383a97d6c48f19246ad24ce324e8bb528
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340281"
---
# <a name="header-annotations"></a><span data-ttu-id="de532-117">Header Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="de532-117">Header Annotations</span></span>

<span data-ttu-id="de532-118">\[In diesem Thema werden die Anmerkungen beschrieben, die in den Windows-Headern durch Windows 7 unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="de532-118">\[This topic describes the annotations supported in the Windows headers through Windows 7.</span></span> <span data-ttu-id="de532-119">Wenn Sie für Windows 8 entwickeln, sollten Sie die Anmerkungen verwenden, die in [SAL]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120))-Anmerkungen beschrieben werden.\]</span><span class="sxs-lookup"><span data-stu-id="de532-119">If you are developing for Windows 8, you should use the annotations described in [SAL Annotations]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]</span></span>

<span data-ttu-id="de532-120">Header Anmerkungen beschreiben, wie eine Funktion Ihre Parameter und den Rückgabewert verwendet.</span><span class="sxs-lookup"><span data-stu-id="de532-120">Header annotations describe how a function uses its parameters and return value.</span></span> <span data-ttu-id="de532-121">Diese Anmerkungen wurden vielen der Windows-Header Dateien hinzugefügt, um sicherzustellen, dass Sie die Windows-API ordnungsgemäß aufrufen.</span><span class="sxs-lookup"><span data-stu-id="de532-121">These annotations have been added to many of the Windows header files to help you ensure that you are calling the Windows API correctly.</span></span> <span data-ttu-id="de532-122">Wenn Sie die Code Analyse aktivieren, die ab Visual Studio 2005 verfügbar ist, erzeugt der Compiler Warnungen der Ebene 6000, wenn Sie diese Funktionen nicht gemäß der Verwendung aufrufen, die durch die Anmerkungen beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="de532-122">If you enable code analysis, which is available starting with the Visual Studio 2005, the compiler will produce level 6000 warnings if you are not calling these functions per the usage described through the annotations.</span></span> <span data-ttu-id="de532-123">Sie können diese Anmerkungen auch in Ihrem eigenen Code hinzufügen, um sicherzustellen, dass Sie ordnungsgemäß aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="de532-123">You can also add these annotations in your own code to ensure that it is being called correctly.</span></span> <span data-ttu-id="de532-124">Informationen zum Aktivieren der Code Analyse in Visual Studio finden Sie in der Dokumentation für Ihre Version von Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="de532-124">To enable code analysis in Visual Studio, see the documentation for your version of Visual Studio.</span></span>

<span data-ttu-id="de532-125">Diese Anmerkungen werden in specstrings. h definiert.</span><span class="sxs-lookup"><span data-stu-id="de532-125">These annotations are defined in Specstrings.h.</span></span> <span data-ttu-id="de532-126">Sie basieren auf primitiven, die Teil der Standard Annotation-Sprache (SAL) sind und mithilfe von implementiert werden `_declspec("SAL_*")` .</span><span class="sxs-lookup"><span data-stu-id="de532-126">They are built on primitives that are part of the Standard Annotation Language (SAL) and implemented using `_declspec("SAL_*")`.</span></span>

<span data-ttu-id="de532-127">Es gibt zwei Klassen von Anmerkungen: Puffer Anmerkungen und erweiterte Anmerkungen.</span><span class="sxs-lookup"><span data-stu-id="de532-127">There are two classes of annotations: buffer annotations and advanced annotations.</span></span>

## <a name="buffer-annotations"></a><span data-ttu-id="de532-128">Puffer Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="de532-128">Buffer Annotations</span></span>

<span data-ttu-id="de532-129">Puffer Anmerkungen beschreiben, wie Funktionen ihre Zeiger verwenden, und können verwendet werden, um Pufferüberläufe zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="de532-129">Buffer annotations describe how functions use their pointers and can be used to detect buffer overruns.</span></span> <span data-ttu-id="de532-130">Jeder Parameter kann NULL oder eine Puffer Anmerkung verwenden.</span><span class="sxs-lookup"><span data-stu-id="de532-130">Each parameter may use zero or one buffer annotation.</span></span> <span data-ttu-id="de532-131">Eine Puffer Anmerkung wird mit einem führenden Unterstrich und den Komponenten erstellt, die in den folgenden Abschnitten beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="de532-131">A buffer annotation is constructed with a leading underscore and the components described in the following sections.</span></span>



| <span data-ttu-id="de532-132">Puffergröße</span><span class="sxs-lookup"><span data-stu-id="de532-132">Buffer size</span></span>                                                                                  | <span data-ttu-id="de532-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de532-133">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de532-134"><span id="_size_"></span><span id="_SIZE_"></span>(*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-134"><span id="_size_"></span><span id="_SIZE_"></span>(*size*)</span></span><br/>                        | <span data-ttu-id="de532-135">Gibt die Gesamtgröße des Puffers an.</span><span class="sxs-lookup"><span data-stu-id="de532-135">Specifies the total size of the buffer.</span></span> <span data-ttu-id="de532-136">Verwenden \_ Sie mit BCOUNT und \_ ecount; verwenden Sie nicht mit \_ Part.</span><span class="sxs-lookup"><span data-stu-id="de532-136">Use with \_bcount and \_ecount; do not use with \_part.</span></span> <span data-ttu-id="de532-137">Dieser Wert ist der barrierefreie Speicherplatz. Er ist möglicherweise kleiner als der zugewiesene Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="de532-137">This value is the accessible space; it may be less than the allocated space.</span></span><br/> |
| <span data-ttu-id="de532-138"><span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-138"><span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*size*,*length*)</span></span><br/> | <span data-ttu-id="de532-139">Gibt die Gesamtgröße und die initialisierte Länge des Puffers an.</span><span class="sxs-lookup"><span data-stu-id="de532-139">Specifies the total size and initialized length of the buffer.</span></span> <span data-ttu-id="de532-140">Verwendung mit \_ BCOUNT \_ -Teil und \_ ecount- \_ Teil.</span><span class="sxs-lookup"><span data-stu-id="de532-140">Use with \_bcount\_part and \_ecount\_part.</span></span> <span data-ttu-id="de532-141">Die Gesamtgröße ist möglicherweise kleiner als der zugewiesene Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="de532-141">The total size may be less than the allocated space.</span></span><br/>              |



 



| <span data-ttu-id="de532-142">Puffergrößen Einheiten</span><span class="sxs-lookup"><span data-stu-id="de532-142">Buffer size units</span></span>                                                       | <span data-ttu-id="de532-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de532-143">Description</span></span>                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="de532-144"><span id="_bcount"></span><span id="_BCOUNT"></span>\_BCOUNT</span><span class="sxs-lookup"><span data-stu-id="de532-144"><span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount</span></span><br/> | <span data-ttu-id="de532-145">Die Puffergröße beträgt Byte.</span><span class="sxs-lookup"><span data-stu-id="de532-145">The buffer size is in bytes.</span></span><br/>    |
| <span data-ttu-id="de532-146"><span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount</span><span class="sxs-lookup"><span data-stu-id="de532-146"><span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount</span></span><br/> | <span data-ttu-id="de532-147">Die Puffergröße ist in-Elementen.</span><span class="sxs-lookup"><span data-stu-id="de532-147">The buffer size is in elements.</span></span><br/> |



 



| <span data-ttu-id="de532-148">Richtung</span><span class="sxs-lookup"><span data-stu-id="de532-148">Direction</span></span>                                                            | <span data-ttu-id="de532-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de532-149">Description</span></span>                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de532-150"><span id="_in"></span><span id="_IN"></span>\_in</span><span class="sxs-lookup"><span data-stu-id="de532-150"><span id="_in"></span><span id="_IN"></span>\_in</span></span><br/>          | <span data-ttu-id="de532-151">Die Funktion liest aus dem Puffer.</span><span class="sxs-lookup"><span data-stu-id="de532-151">The function reads from the buffer.</span></span> <span data-ttu-id="de532-152">Der Aufrufer stellt den Puffer bereit und initialisiert ihn.</span><span class="sxs-lookup"><span data-stu-id="de532-152">The caller provides the buffer and initializes it.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="de532-153"><span id="_inout"></span><span id="_INOUT"></span>\_INOUT</span><span class="sxs-lookup"><span data-stu-id="de532-153"><span id="_inout"></span><span id="_INOUT"></span>\_inout</span></span><br/> | <span data-ttu-id="de532-154">Die-Funktion liest aus und schreibt in den Puffer.</span><span class="sxs-lookup"><span data-stu-id="de532-154">The function both reads from and writes to buffer.</span></span> <span data-ttu-id="de532-155">Der Aufrufer stellt den Puffer bereit und initialisiert ihn.</span><span class="sxs-lookup"><span data-stu-id="de532-155">The caller provides the buffer and initializes it.</span></span> <span data-ttu-id="de532-156">Bei Verwendung mit \_ Deref kann der Puffer von der Funktion neu zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="de532-156">If used with \_deref, the buffer may be reallocated by the function.</span></span><br/>                                      |
| <span data-ttu-id="de532-157"><span id="_out"></span><span id="_OUT"></span>\_vorgenommen</span><span class="sxs-lookup"><span data-stu-id="de532-157"><span id="_out"></span><span id="_OUT"></span>\_out</span></span><br/>       | <span data-ttu-id="de532-158">Die Funktion schreibt in den Puffer.</span><span class="sxs-lookup"><span data-stu-id="de532-158">The function writes to the buffer.</span></span> <span data-ttu-id="de532-159">Wenn die Funktion für den Rückgabewert oder mit \_ Deref verwendet wird, stellt Sie den Puffer bereit und initialisiert sie.</span><span class="sxs-lookup"><span data-stu-id="de532-159">If used on the return value or with \_deref, the function provides the buffer and initializes it.</span></span> <span data-ttu-id="de532-160">Andernfalls stellt der Aufrufer den Puffer bereit, und die Funktion initialisiert ihn.</span><span class="sxs-lookup"><span data-stu-id="de532-160">Otherwise, the caller provides the buffer and the function initializes it.</span></span><br/> |



 



| <span data-ttu-id="de532-161">Dereferenzierung</span><span class="sxs-lookup"><span data-stu-id="de532-161">Indirection</span></span>                                                                       | <span data-ttu-id="de532-162">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de532-162">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de532-163"><span id="_deref"></span><span id="_DEREF"></span>\_Deref</span><span class="sxs-lookup"><span data-stu-id="de532-163"><span id="_deref"></span><span id="_DEREF"></span>\_deref</span></span><br/>              | <span data-ttu-id="de532-164">Dereferenziert den-Parameter, um den Puffer Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="de532-164">Dereference the parameter to obtain the buffer pointer.</span></span> <span data-ttu-id="de532-165">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="de532-165">This parameter may not be **NULL**.</span></span><br/> |
| <span data-ttu-id="de532-166"><span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_Deref- \_ Opt</span><span class="sxs-lookup"><span data-stu-id="de532-166"><span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_deref\_opt</span></span><br/> | <span data-ttu-id="de532-167">Dereferenziert den-Parameter, um den Puffer Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="de532-167">Dereference the parameter to obtain the buffer pointer.</span></span> <span data-ttu-id="de532-168">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="de532-168">This parameter can be **NULL**.</span></span><br/>     |



 



| <span data-ttu-id="de532-169">Initialisierung</span><span class="sxs-lookup"><span data-stu-id="de532-169">Initialization</span></span>                                                    | <span data-ttu-id="de532-170">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de532-170">Description</span></span>                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de532-171"><span id="_full"></span><span id="_FULL"></span>\_voll</span><span class="sxs-lookup"><span data-stu-id="de532-171"><span id="_full"></span><span id="_FULL"></span>\_full</span></span><br/> | <span data-ttu-id="de532-172">Die Funktion initialisiert den gesamten Puffer.</span><span class="sxs-lookup"><span data-stu-id="de532-172">The function initializes the entire buffer.</span></span> <span data-ttu-id="de532-173">Nur mit Ausgabe Puffern verwenden.</span><span class="sxs-lookup"><span data-stu-id="de532-173">Use only with output buffers.</span></span><br/>                                     |
| <span data-ttu-id="de532-174"><span id="_part"></span><span id="_PART"></span>\_Ostteil</span><span class="sxs-lookup"><span data-stu-id="de532-174"><span id="_part"></span><span id="_PART"></span>\_part</span></span><br/> | <span data-ttu-id="de532-175">Mit der-Funktion wird ein Teil des Puffers initialisiert, und es wird explizit angegeben, wie viel.</span><span class="sxs-lookup"><span data-stu-id="de532-175">The function initializes part of the buffer, and explicitly indicates how much.</span></span> <span data-ttu-id="de532-176">Nur mit Ausgabe Puffern verwenden.</span><span class="sxs-lookup"><span data-stu-id="de532-176">Use only with output buffers.</span></span><br/> |



 



| <span data-ttu-id="de532-177">Erforderlicher oder optionaler Puffer</span><span class="sxs-lookup"><span data-stu-id="de532-177">Required or optional buffer</span></span>                                    | <span data-ttu-id="de532-178">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de532-178">Description</span></span>                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="de532-179"><span id="_opt"></span><span id="_OPT"></span>\_  opt</span><span class="sxs-lookup"><span data-stu-id="de532-179"><span id="_opt"></span><span id="_OPT"></span>\_opt</span></span><br/> | <span data-ttu-id="de532-180">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="de532-180">This parameter can be **NULL**.</span></span><br/> |



 

<span data-ttu-id="de532-181">Im folgenden Beispiel werden die Anmerkungen für die **GetModuleFileName** -Funktion gezeigt.</span><span class="sxs-lookup"><span data-stu-id="de532-181">The following example shows the annotations for the **GetModuleFileName** function.</span></span> <span data-ttu-id="de532-182">Der *HMODULE* -Parameter ist ein optionaler Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="de532-182">The *hModule* parameter is an optional input parameter .</span></span> <span data-ttu-id="de532-183">Der *lpFileName* -Parameter ist ein Output-Parameter. seine Größe in Zeichen wird durch den *nSize* -Parameter angegeben, und seine Länge schließt das **null**-abschließende Zeichen ein.</span><span class="sxs-lookup"><span data-stu-id="de532-183">The *lpFilename* parameter is an output parameter; its size in characters is specified by the *nSize* parameter and its length includes the **null**-terminating character.</span></span> <span data-ttu-id="de532-184">Der *nSize* -Parameter ist ein Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="de532-184">The *nSize* parameter is an input parameter.</span></span>


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



<span data-ttu-id="de532-185">Im folgenden finden Sie die Anmerkungen, die in specstrings. h definiert sind.</span><span class="sxs-lookup"><span data-stu-id="de532-185">The following are the annotations defined in Specstrings.h.</span></span> <span data-ttu-id="de532-186">Verwenden Sie die Informationen in den obigen Tabellen, um ihre Bedeutung zu interpretieren.</span><span class="sxs-lookup"><span data-stu-id="de532-186">Use the information in the tables above to interpret their meaning.</span></span>

<span data-ttu-id="de532-187">__bcount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-187">__bcount(*size*)</span></span>  
<span data-ttu-id="de532-188">__bcount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-188">__bcount_opt(*size*)</span></span>  
<span data-ttu-id="de532-189">__deref_bcount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-189">__deref_bcount(*size*)</span></span>  
<span data-ttu-id="de532-190">__deref_bcount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-190">__deref_bcount_opt(*size*)</span></span>  
<span data-ttu-id="de532-191">__deref_ecount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-191">__deref_ecount(*size*)</span></span>  
<span data-ttu-id="de532-192">__deref_ecount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-192">__deref_ecount_opt(*size*)</span></span>  
<span data-ttu-id="de532-193">__deref_in</span><span class="sxs-lookup"><span data-stu-id="de532-193">__deref_in</span></span>  
<span data-ttu-id="de532-194">__deref_in_bcount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-194">__deref_in_bcount(*size*)</span></span>  
<span data-ttu-id="de532-195">__deref_in_bcount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-195">__deref_in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="de532-196">__deref_in_ecount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-196">__deref_in_ecount(*size*)</span></span>  
<span data-ttu-id="de532-197">__deref_in_ecount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-197">__deref_in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="de532-198">__deref_in_opt</span><span class="sxs-lookup"><span data-stu-id="de532-198">__deref_in_opt</span></span>  
<span data-ttu-id="de532-199">__deref_inout</span><span class="sxs-lookup"><span data-stu-id="de532-199">__deref_inout</span></span>  
<span data-ttu-id="de532-200">__deref_inout_bcount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-200">__deref_inout_bcount(*size*)</span></span>  
<span data-ttu-id="de532-201">__deref_inout_bcount_full (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-201">__deref_inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="de532-202">__deref_inout_bcount_full_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-202">__deref_inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="de532-203">__deref_inout_bcount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-203">__deref_inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="de532-204">__deref_inout_bcount_part (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-204">__deref_inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="de532-205">__deref_inout_bcount_part_opt (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-205">__deref_inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="de532-206">__deref_inout_ecount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-206">__deref_inout_ecount(*size*)</span></span>  
<span data-ttu-id="de532-207">__deref_inout_ecount_full (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-207">__deref_inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="de532-208">__deref_inout_ecount_full_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-208">__deref_inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="de532-209">__deref_inout_ecount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-209">__deref_inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="de532-210">__deref_inout_ecount_part (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-210">__deref_inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="de532-211">__deref_inout_ecount_part_opt (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-211">__deref_inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="de532-212">__deref_inout_opt</span><span class="sxs-lookup"><span data-stu-id="de532-212">__deref_inout_opt</span></span>  
<span data-ttu-id="de532-213">__deref_opt_bcount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-213">__deref_opt_bcount(*size*)</span></span>  
<span data-ttu-id="de532-214">__deref_opt_bcount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-214">__deref_opt_bcount_opt(*size*)</span></span>  
<span data-ttu-id="de532-215">__deref_opt_ecount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-215">__deref_opt_ecount(*size*)</span></span>  
<span data-ttu-id="de532-216">__deref_opt_ecount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-216">__deref_opt_ecount_opt(*size*)</span></span>  
<span data-ttu-id="de532-217">__deref_opt_in</span><span class="sxs-lookup"><span data-stu-id="de532-217">__deref_opt_in</span></span>  
<span data-ttu-id="de532-218">__deref_opt_in_bcount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-218">__deref_opt_in_bcount(*size*)</span></span>  
<span data-ttu-id="de532-219">__deref_opt_in_bcount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-219">__deref_opt_in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="de532-220">__deref_opt_in_ecount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-220">__deref_opt_in_ecount(*size*)</span></span>  
<span data-ttu-id="de532-221">__deref_opt_in_ecount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-221">__deref_opt_in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="de532-222">__deref_opt_in_opt</span><span class="sxs-lookup"><span data-stu-id="de532-222">__deref_opt_in_opt</span></span>  
<span data-ttu-id="de532-223">__deref_opt_inout</span><span class="sxs-lookup"><span data-stu-id="de532-223">__deref_opt_inout</span></span>  
<span data-ttu-id="de532-224">__deref_opt_inout_bcount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-224">__deref_opt_inout_bcount(*size*)</span></span>  
<span data-ttu-id="de532-225">__deref_opt_inout_bcount_full (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-225">__deref_opt_inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="de532-226">__deref_opt_inout_bcount_full_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-226">__deref_opt_inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="de532-227">__deref_opt_inout_bcount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-227">__deref_opt_inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="de532-228">__deref_opt_inout_bcount_part (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-228">__deref_opt_inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="de532-229">__deref_opt_inout_bcount_part_opt (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-229">__deref_opt_inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="de532-230">__deref_opt_inout_ecount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-230">__deref_opt_inout_ecount(*size*)</span></span>  
<span data-ttu-id="de532-231">__deref_opt_inout_ecount_full (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-231">__deref_opt_inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="de532-232">__deref_opt_inout_ecount_full_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-232">__deref_opt_inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="de532-233">__deref_opt_inout_ecount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-233">__deref_opt_inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="de532-234">__deref_opt_inout_ecount_part (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-234">__deref_opt_inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="de532-235">__deref_opt_inout_ecount_part_opt (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-235">__deref_opt_inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="de532-236">__deref_opt_inout_opt</span><span class="sxs-lookup"><span data-stu-id="de532-236">__deref_opt_inout_opt</span></span>  
<span data-ttu-id="de532-237">__deref_opt_out</span><span class="sxs-lookup"><span data-stu-id="de532-237">__deref_opt_out</span></span>  
<span data-ttu-id="de532-238">__deref_opt_out_bcount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-238">__deref_opt_out_bcount(*size*)</span></span>  
<span data-ttu-id="de532-239">__deref_opt_out_bcount_full (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-239">__deref_opt_out_bcount_full(*size*)</span></span>  
<span data-ttu-id="de532-240">__deref_opt_out_bcount_full_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-240">__deref_opt_out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="de532-241">__deref_opt_out_bcount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-241">__deref_opt_out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="de532-242">__deref_opt_out_bcount_part (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-242">__deref_opt_out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="de532-243">__deref_opt_out_bcount_part_opt (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-243">__deref_opt_out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="de532-244">__deref_opt_out_ecount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-244">__deref_opt_out_ecount(*size*)</span></span>  
<span data-ttu-id="de532-245">__deref_opt_out_ecount_full (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-245">__deref_opt_out_ecount_full(*size*)</span></span>  
<span data-ttu-id="de532-246">__deref_opt_out_ecount_full_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-246">__deref_opt_out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="de532-247">__deref_opt_out_ecount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-247">__deref_opt_out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="de532-248">__deref_opt_out_ecount_part (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-248">__deref_opt_out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="de532-249">__deref_opt_out_ecount_part_opt (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-249">__deref_opt_out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="de532-250">__deref_opt_out_opt</span><span class="sxs-lookup"><span data-stu-id="de532-250">__deref_opt_out_opt</span></span>  
<span data-ttu-id="de532-251">__deref_out</span><span class="sxs-lookup"><span data-stu-id="de532-251">__deref_out</span></span>  
<span data-ttu-id="de532-252">__deref_out_bcount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-252">__deref_out_bcount(*size*)</span></span>  
<span data-ttu-id="de532-253">__deref_out_bcount_full (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-253">__deref_out_bcount_full(*size*)</span></span>  
<span data-ttu-id="de532-254">__deref_out_bcount_full_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-254">__deref_out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="de532-255">__deref_out_bcount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-255">__deref_out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="de532-256">__deref_out_bcount_part (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-256">__deref_out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="de532-257">__deref_out_bcount_part_opt (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-257">__deref_out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="de532-258">__deref_out_ecount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-258">__deref_out_ecount(*size*)</span></span>  
<span data-ttu-id="de532-259">__deref_out_ecount_full (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-259">__deref_out_ecount_full(*size*)</span></span>  
<span data-ttu-id="de532-260">__deref_out_ecount_full_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-260">__deref_out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="de532-261">__deref_out_ecount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-261">__deref_out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="de532-262">__deref_out_ecount_part (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-262">__deref_out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="de532-263">__deref_out_ecount_part_opt (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-263">__deref_out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="de532-264">__deref_out_opt</span><span class="sxs-lookup"><span data-stu-id="de532-264">__deref_out_opt</span></span>  
<span data-ttu-id="de532-265">__ecount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-265">__ecount(*size*)</span></span>  
<span data-ttu-id="de532-266">__ecount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-266">__ecount_opt(*size*)</span></span>  
<span data-ttu-id="de532-267">__in</span><span class="sxs-lookup"><span data-stu-id="de532-267">__in</span></span>  
<span data-ttu-id="de532-268">__in_bcount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-268">__in_bcount(*size*)</span></span>  
<span data-ttu-id="de532-269">__in_bcount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-269">__in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="de532-270">__in_ecount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-270">__in_ecount(*size*)</span></span>  
<span data-ttu-id="de532-271">__in_ecount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-271">__in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="de532-272">__in_opt</span><span class="sxs-lookup"><span data-stu-id="de532-272">__in_opt</span></span>  
<span data-ttu-id="de532-273">__inout</span><span class="sxs-lookup"><span data-stu-id="de532-273">__inout</span></span>  
<span data-ttu-id="de532-274">__inout_bcount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-274">__inout_bcount(*size*)</span></span>  
<span data-ttu-id="de532-275">__inout_bcount_full (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-275">__inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="de532-276">__inout_bcount_full_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-276">__inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="de532-277">__inout_bcount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-277">__inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="de532-278">__inout_bcount_part (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-278">__inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="de532-279">__inout_bcount_part_opt (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-279">__inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="de532-280">__inout_ecount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-280">__inout_ecount(*size*)</span></span>  
<span data-ttu-id="de532-281">__inout_ecount_full (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-281">__inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="de532-282">__inout_ecount_full_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-282">__inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="de532-283">__inout_ecount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-283">__inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="de532-284">__inout_ecount_part (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-284">__inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="de532-285">__inout_ecount_part_opt (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-285">__inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="de532-286">__inout_opt</span><span class="sxs-lookup"><span data-stu-id="de532-286">__inout_opt</span></span>  
<span data-ttu-id="de532-287">__out</span><span class="sxs-lookup"><span data-stu-id="de532-287">__out</span></span>  
<span data-ttu-id="de532-288">__out_bcount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-288">__out_bcount(*size*)</span></span>  
<span data-ttu-id="de532-289">__out_bcount_full (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-289">__out_bcount_full(*size*)</span></span>  
<span data-ttu-id="de532-290">__out_bcount_full_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-290">__out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="de532-291">__out_bcount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-291">__out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="de532-292">__out_bcount_part (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-292">__out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="de532-293">__out_bcount_part_opt (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-293">__out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="de532-294">__out_ecount (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-294">__out_ecount(*size*)</span></span>  
<span data-ttu-id="de532-295">__out_ecount_full (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-295">__out_ecount_full(*size*)</span></span>  
<span data-ttu-id="de532-296">__out_ecount_full_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-296">__out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="de532-297">__out_ecount_opt (*Größe*)</span><span class="sxs-lookup"><span data-stu-id="de532-297">__out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="de532-298">__out_ecount_part (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-298">__out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="de532-299">__out_ecount_part_opt (*Größe*,*Länge*)</span><span class="sxs-lookup"><span data-stu-id="de532-299">__out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="de532-300">__out_opt</span><span class="sxs-lookup"><span data-stu-id="de532-300">__out_opt</span></span>  

## <a name="advanced-annotations"></a><span data-ttu-id="de532-301">Erweiterte Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="de532-301">Advanced Annotations</span></span>

<span data-ttu-id="de532-302">Erweiterte Anmerkungen stellen zusätzliche Informationen zum Parameter oder Rückgabewert bereit.</span><span class="sxs-lookup"><span data-stu-id="de532-302">Advanced annotations provide additional information about the parameter or return value.</span></span> <span data-ttu-id="de532-303">Jeder Parameter oder Rückgabewert kann NULL oder eine erweiterte Anmerkung verwenden.</span><span class="sxs-lookup"><span data-stu-id="de532-303">Each parameter or return value may use zero or one advanced annotation.</span></span>



| <span data-ttu-id="de532-304">Anmerkung</span><span class="sxs-lookup"><span data-stu-id="de532-304">Annotation</span></span>                                                                                                                                               | <span data-ttu-id="de532-305">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de532-305">Description</span></span>                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de532-306"><span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blockson (*Ressource*)</span><span class="sxs-lookup"><span data-stu-id="de532-306"><span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocksOn(*resource*)</span></span><br/> | <span data-ttu-id="de532-307">Die Functions-Blöcke für die angegebene Ressource.</span><span class="sxs-lookup"><span data-stu-id="de532-307">The functions blocks on the specified resource.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="de532-308"><span id="__callback"></span><span id="__CALLBACK"></span>\_\_Rück</span><span class="sxs-lookup"><span data-stu-id="de532-308"><span id="__callback"></span><span id="__CALLBACK"></span>\_\_callback</span></span><br/>                                                                        | <span data-ttu-id="de532-309">Die-Funktion kann als Funktionszeiger verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de532-309">The function can be used as a function pointer.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="de532-310"><span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_Check Return</span><span class="sxs-lookup"><span data-stu-id="de532-310"><span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn</span></span><br/>                               | <span data-ttu-id="de532-311">Aufrufer müssen den Rückgabewert überprüfen.</span><span class="sxs-lookup"><span data-stu-id="de532-311">Callers must check the return value.</span></span><br/>                                                                                                                                                                                                                                 |
| <span data-ttu-id="de532-312"><span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_Format \_ Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="de532-312"><span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_format\_string</span></span><br/>                                                        | <span data-ttu-id="de532-313">Der-Parameter ist eine Zeichenfolge, die den printf-Stil% Markers enthält.</span><span class="sxs-lookup"><span data-stu-id="de532-313">The parameter is a string that contains printf-style % markers.</span></span><br/>                                                                                                                                                                                                      |
| <span data-ttu-id="de532-314"><span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_in \_ awcount (*expr*,*size*)</span><span class="sxs-lookup"><span data-stu-id="de532-314"><span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_in\_awcount(*expr*,*size*)</span></span><br/>                            | <span data-ttu-id="de532-315">Wenn der Ausdruck beim Beenden true ist, wird die Größe des Eingabe Puffers in Bytes angegeben.</span><span class="sxs-lookup"><span data-stu-id="de532-315">If the expression is true at exit, the size of the input buffer is specified in bytes.</span></span> <span data-ttu-id="de532-316">Wenn der Ausdruck false ist, wird die Größe in-Elementen angegeben.</span><span class="sxs-lookup"><span data-stu-id="de532-316">If the expression is false, the size is specified in elements.</span></span><br/>                                                                                                                |
| <span data-ttu-id="de532-317"><span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminiert</span><span class="sxs-lookup"><span data-stu-id="de532-317"><span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated</span></span><br/>                                          | <span data-ttu-id="de532-318">Auf den Puffer kann bis einschließlich der ersten Sequenz von zwei **null** -Zeichen oder Zeigern zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="de532-318">The buffer may be accessed up to and including the first sequence of two **null** characters or pointers.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="de532-319"><span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_NullTerminated</span><span class="sxs-lookup"><span data-stu-id="de532-319"><span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_nullterminated</span></span><br/>                                                      | <span data-ttu-id="de532-320">Auf den Puffer kann bis einschließlich des ersten **null** -Zeichens oder-Zeigers zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="de532-320">The buffer may be accessed up to and including the first **null** character or pointer.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="de532-321"><span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_Out \_ awcount (*expr*,*size*)</span><span class="sxs-lookup"><span data-stu-id="de532-321"><span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out\_awcount(*expr*,*size*)</span></span><br/>                         | <span data-ttu-id="de532-322">Wenn der Ausdruck beim Beenden true ist, wird die Größe des Ausgabepuffers in Bytes angegeben.</span><span class="sxs-lookup"><span data-stu-id="de532-322">If the expression is true at exit, the size of the output buffer is specified in bytes.</span></span> <span data-ttu-id="de532-323">Wenn der Ausdruck false ist, wird die Größe in-Elementen angegeben.</span><span class="sxs-lookup"><span data-stu-id="de532-323">If the expression is false, the size is specified in elements.</span></span> <br/>                                                                                                              |
| <span data-ttu-id="de532-324"><span id="__override"></span><span id="__OVERRIDE"></span>\_\_Dire</span><span class="sxs-lookup"><span data-stu-id="de532-324"><span id="__override"></span><span id="__OVERRIDE"></span>\_\_override</span></span><br/>                                                                        | <span data-ttu-id="de532-325">Gibt das c#-Stil Überschreibungs Verhalten für virtuelle Methoden an.</span><span class="sxs-lookup"><span data-stu-id="de532-325">Specifies C#-style override behavior for virtual methods.</span></span><br/>                                                                                                                                                                                                           |
| <span data-ttu-id="de532-326"><span id="__reserved"></span><span id="__RESERVED"></span>\_\_bleiben</span><span class="sxs-lookup"><span data-stu-id="de532-326"><span id="__reserved"></span><span id="__RESERVED"></span>\_\_reserved</span></span><br/>                                                                        | <span data-ttu-id="de532-327">Der-Parameter ist für die zukünftige Verwendung reserviert und muss NULL **oder NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="de532-327">The parameter is reserved for future use and must be zero or **NULL**.</span></span><br/>                                                                                                                                                                                               |
| <span data-ttu-id="de532-328"><span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_Erfolg (*expr*)</span><span class="sxs-lookup"><span data-stu-id="de532-328"><span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_success(*expr*)</span></span><br/>                                                       | <span data-ttu-id="de532-329">Wenn der Ausdruck beim Beenden true ist, kann der Aufrufer auf alle Garantien Vertrauen, die durch andere Anmerkungen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="de532-329">If the expression is true at exit, the caller can rely on all guarantees specified by other annotations.</span></span> <span data-ttu-id="de532-330">Wenn der Ausdruck false ist, kann der Aufrufer nicht auf die Garantien Vertrauen.</span><span class="sxs-lookup"><span data-stu-id="de532-330">If the expression is false, the caller cannot rely on the guarantees.</span></span> <span data-ttu-id="de532-331">Diese Anmerkung wird automatisch Funktionen hinzugefügt, die einen **HRESULT** -Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="de532-331">This annotation is automatically added to functions that return an **HRESULT** value.</span></span><br/> |
| <span data-ttu-id="de532-332"><span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix (*CType*)</span><span class="sxs-lookup"><span data-stu-id="de532-332"><span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix(*ctype*)</span></span><br/>                                                    | <span data-ttu-id="de532-333">Behandeln Sie den Parameter anstelle des deklarierten Typs als den angegebenen Typ.</span><span class="sxs-lookup"><span data-stu-id="de532-333">Treat the parameter as the specified type rather than its declared type.</span></span><br/>                                                                                                                                                                                             |



 

<span data-ttu-id="de532-334">In den folgenden Beispielen werden der Puffer und die erweiterten Anmerkungen für die Funktionen [**deletetimerqueuetimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**freumgebungs Strings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)und [**unlenker dexceptionfilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) gezeigt.</span><span class="sxs-lookup"><span data-stu-id="de532-334">The following examples show the buffer and advanced annotations for the [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa), and [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) functions.</span></span>


```C++
__checkReturn
BOOL
WINAPI
DeleteTimerQueueTimer(
    __in_opt HANDLE TimerQueue,
    __in     HANDLE Timer,
    __in_opt HANDLE CompletionEvent
    );

BOOL
WINAPI
FreeEnvironmentStrings(
    __in __nullnullterminated LPTCH
    );

__callback
LONG
WINAPI
UnhandledExceptionFilter(
    __in struct _EXCEPTION_POINTERS *ExceptionInfo
    );

```



## <a name="related-topics"></a><span data-ttu-id="de532-335">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="de532-335">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de532-336">SAL-Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="de532-336">SAL Annotations</span></span>](/cpp/c-runtime-library/sal-annotations?view=vs-2019)
</dt> <dt>

[<span data-ttu-id="de532-337">Exemplarische Vorgehensweise: Analysieren von C/C++-Code auf Fehler</span><span class="sxs-lookup"><span data-stu-id="de532-337">Walkthrough: Analyzing C/C++ Code for Defects</span></span>](/visualstudio/code-quality/walkthrough-analyzing-c-cpp-code-for-defects?view=vs-2015)
</dt> </dl>

 

