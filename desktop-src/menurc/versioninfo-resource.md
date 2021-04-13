---
title: VERSIONINFO-Ressource
description: Definiert eine Versions Informations Ressource. Die Ressource enthält Informationen über die Datei als Versionsnummer, das beabsichtigte Betriebssystem und den ursprünglichen Dateinamen. Die Ressource ist für die Verwendung mit den Versions Informationsfunktionen vorgesehen.
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- VERSIONINFO-Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9248abe18d07820ebefaa6d939f36f617f6cd07f
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "104316718"
---
# <a name="versioninfo-resource"></a><span data-ttu-id="08678-106">VERSIONINFO-Ressource</span><span class="sxs-lookup"><span data-stu-id="08678-106">VERSIONINFO resource</span></span>

<span data-ttu-id="08678-107">Definiert eine Versions Informations Ressource.</span><span class="sxs-lookup"><span data-stu-id="08678-107">Defines a version-information resource.</span></span> <span data-ttu-id="08678-108">Die Ressource enthält Informationen über die Datei als Versionsnummer, das beabsichtigte Betriebssystem und den ursprünglichen Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="08678-108">The resource contains such information about the file as its version number, its intended operating system, and its original filename.</span></span> <span data-ttu-id="08678-109">Die Ressource ist für die Verwendung mit den [Versions Informations](./version-information.md) Funktionen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="08678-109">The resource is intended to be used with the [Version Information](./version-information.md) functions.</span></span>

<span data-ttu-id="08678-110">Es gibt zwei Möglichkeiten, eine **VERSIONINFO** -Anweisung zu formatieren:</span><span class="sxs-lookup"><span data-stu-id="08678-110">There are two ways to format a **VERSIONINFO** statement:</span></span>

``` syntax
versionID VERSIONINFO fixed-info  { block-statement . . . }
```

<span data-ttu-id="08678-111">\- oder -</span><span class="sxs-lookup"><span data-stu-id="08678-111">\- or -</span></span>

``` syntax
versionID VERSIONINFO 
fixed-info
BEGIN
block-statement
. . .
END
```

## <a name="parameters"></a><span data-ttu-id="08678-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="08678-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08678-113"><span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*</span><span class="sxs-lookup"><span data-stu-id="08678-113"><span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*</span></span>
</dt> <dd>

<span data-ttu-id="08678-114">Der Versions Informationsressourcen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="08678-114">Version-information resource identifier.</span></span> <span data-ttu-id="08678-115">Dieser Wert muss 1 sein.</span><span class="sxs-lookup"><span data-stu-id="08678-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="08678-116"><span id="fixed-info"></span><span id="FIXED-INFO"></span>*Fixed-Info*</span><span class="sxs-lookup"><span data-stu-id="08678-116"><span id="fixed-info"></span><span id="FIXED-INFO"></span>*fixed-info*</span></span>
</dt> <dd>

<span data-ttu-id="08678-117">Versionsinformationen, wie z. b. die Dateiversion und das beabsichtigte Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="08678-117">Version information, such as the file version and the intended operating system.</span></span> <span data-ttu-id="08678-118">Dieser Parameter besteht aus den folgenden Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="08678-118">This parameter consists of the following statements.</span></span>



| <span data-ttu-id="08678-119">-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="08678-119">Statement</span></span>                         | <span data-ttu-id="08678-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08678-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08678-121">**File Version** - *Version*</span><span class="sxs-lookup"><span data-stu-id="08678-121">**FILEVERSION** *version*</span></span>         | <span data-ttu-id="08678-122">Binäre Versionsnummer für die Datei.</span><span class="sxs-lookup"><span data-stu-id="08678-122">Binary version number for the file.</span></span> <span data-ttu-id="08678-123">Die *Version* besteht aus 2 32-Bit-Ganzzahlen, die durch ganze Zahlen mit 4 16 Bit definiert werden.</span><span class="sxs-lookup"><span data-stu-id="08678-123">The *version* consists of two 32-bit integers, defined by four 16-bit integers.</span></span> <span data-ttu-id="08678-124">Beispielsweise wird "fileversion 3, 10, 0, 61" in zwei Double Words übersetzt: 0x0003000a und 0x0000003d in dieser Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="08678-124">For example, "FILEVERSION 3,10,0,61" is translated into two doublewords: 0x0003000a and 0x0000003d, in that order.</span></span> <span data-ttu-id="08678-125">Wenn die *Version* durch die **DWORD** -Werte *DW1* und *DW2* definiert ist, müssen Sie daher wie folgt in der **fileversion** -Anweisung angezeigt werden: `HIWORD(dw1)` , `LOWORD(dw1)` , `HIWORD(dw2)` , `LOWORD(dw2)` .</span><span class="sxs-lookup"><span data-stu-id="08678-125">Therefore, if *version* is defined by the **DWORD** values *dw1* and *dw2*, they need to appear in the **FILEVERSION** statement as follows: `HIWORD(dw1)`, `LOWORD(dw1)`, `HIWORD(dw2)`, `LOWORD(dw2)`.</span></span> |
| <span data-ttu-id="08678-126">**ProductVersion** - *Version*</span><span class="sxs-lookup"><span data-stu-id="08678-126">**PRODUCTVERSION** *version*</span></span>      | <span data-ttu-id="08678-127">Binäre Versionsnummer für das Produkt, mit dem die Datei verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="08678-127">Binary version number for the product with which the file is distributed.</span></span> <span data-ttu-id="08678-128">Der *Versions* Parameter ist 2 32-Bit-Ganzzahlen, die durch ganze Zahlen mit 4 16 Bit definiert werden.</span><span class="sxs-lookup"><span data-stu-id="08678-128">The *version* parameter is two 32-bit integers, defined by four 16-bit integers.</span></span> <span data-ttu-id="08678-129">Weitere Informationen zur- *Version* finden Sie in der Beschreibung der **Dateiversion** .</span><span class="sxs-lookup"><span data-stu-id="08678-129">For more information about *version*, see the **FILEVERSION** description.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="08678-130">**Fileflagsmask** *fileflagsmask*</span><span class="sxs-lookup"><span data-stu-id="08678-130">**FILEFLAGSMASK** *fileflagsmask*</span></span> | <span data-ttu-id="08678-131">Gibt an, welche Bits in der **FILEFLAGS** -Anweisung gültig sind.</span><span class="sxs-lookup"><span data-stu-id="08678-131">Indicates which bits in the **FILEFLAGS** statement are valid.</span></span> <span data-ttu-id="08678-132">Bei 16-Bit-Fenstern ist dieser Wert 0x3F.</span><span class="sxs-lookup"><span data-stu-id="08678-132">For 16-bit Windows, this value is 0x3f.</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="08678-133">**FILEFLAGS** - *FILEFLAGS*</span><span class="sxs-lookup"><span data-stu-id="08678-133">**FILEFLAGS** *fileflags*</span></span>         | <span data-ttu-id="08678-134">Attribute der Datei.</span><span class="sxs-lookup"><span data-stu-id="08678-134">Attributes of the file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="08678-135">**FILEOS** - *Datei* Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="08678-135">**FILEOS** *fileos*</span></span>               | <span data-ttu-id="08678-136">Das Betriebssystem, für das diese Datei entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="08678-136">Operating system for which this file was designed.</span></span> <span data-ttu-id="08678-137">Der *FILEOS* -Parameter kann einer der Betriebssystem Werte sein, die im Abschnitt "Hinweise" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="08678-137">The *fileos* parameter can be one of the operating system values given in the Remarks section.</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="08678-138">**FILETYPE** - *Dateityp*</span><span class="sxs-lookup"><span data-stu-id="08678-138">**FILETYPE** *filetype*</span></span>           | <span data-ttu-id="08678-139">Allgemeiner Dateityp.</span><span class="sxs-lookup"><span data-stu-id="08678-139">General type of file.</span></span> <span data-ttu-id="08678-140">Der *filetype* -Parameter kann einer der Dateityp Werte sein, die im Abschnitt "Hinweise" aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="08678-140">The *filetype* parameter can be one of the file type values listed in the Remarks section.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="08678-141">**Filesubtype** - *Untertyp*</span><span class="sxs-lookup"><span data-stu-id="08678-141">**FILESUBTYPE** *subtype*</span></span>         | <span data-ttu-id="08678-142">Funktion der Datei.</span><span class="sxs-lookup"><span data-stu-id="08678-142">Function of the file.</span></span> <span data-ttu-id="08678-143">Der *Untertyp* -Parameter ist 0 (null), es sei denn, der *filetype* -Parameter in der **filetype** -Anweisung ist VFT \_ drv, VFT- \_ Schriftart oder VFT \_ .</span><span class="sxs-lookup"><span data-stu-id="08678-143">The *subtype* parameter is zero unless the *filetype* parameter in the **FILETYPE** statement is VFT\_DRV, VFT\_FONT, or VFT\_VXD.</span></span> <span data-ttu-id="08678-144">Eine Liste der Werte für den Datei Untertyp finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="08678-144">For a list of file subtype values, see the Remarks section.</span></span>                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="08678-145"><span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*Block-Anweisung*</span><span class="sxs-lookup"><span data-stu-id="08678-145"><span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*block-statement*</span></span>
</dt> <dd>

<span data-ttu-id="08678-146">Gibt mindestens einen Versions Informationsblock an.</span><span class="sxs-lookup"><span data-stu-id="08678-146">Specifies one or more version-information blocks.</span></span> <span data-ttu-id="08678-147">Ein-Block kann Zeichen folgen Informationen oder Variablen Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="08678-147">A block can contain string information or variable information.</span></span> <span data-ttu-id="08678-148">Weitere Informationen finden Sie unter [**stringfileinfo-Block**](stringfileinfo-block.md) oder [**varfileinfo-Block**](varfileinfo-block.md).</span><span class="sxs-lookup"><span data-stu-id="08678-148">For more information, see [**StringFileInfo Block**](stringfileinfo-block.md) or [**VarFileInfo Block**](varfileinfo-block.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08678-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08678-149">Remarks</span></span>

<span data-ttu-id="08678-150">Wenn Sie die mit der **VERSIONINFO** -Anweisung angegebenen Konstanten verwenden möchten, müssen Sie die Header Datei "winver. h" oder "Windows. h" in die Ressourcen Definitionsdatei einschließen.</span><span class="sxs-lookup"><span data-stu-id="08678-150">To use the constants specified with the **VERSIONINFO** statement, you must include the Winver.h or Windows.h header file in the resource-definition file.</span></span>

<span data-ttu-id="08678-151">In der folgenden Liste werden die Parameter beschrieben, die in der **VERSIONINFO** -Anweisung verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="08678-151">The following list describes the parameters used in the **VERSIONINFO** statement:</span></span>

<dl> <dt>

<span data-ttu-id="08678-152"><span id="fileflags"></span><span id="FILEFLAGS"></span>*FILEFLAGS*</span><span class="sxs-lookup"><span data-stu-id="08678-152"><span id="fileflags"></span><span id="FILEFLAGS"></span>*fileflags*</span></span>
</dt> <dd>

<span data-ttu-id="08678-153">Eine Kombination der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="08678-153">A combination of the following values.</span></span>



| <span data-ttu-id="08678-154">Wert</span><span class="sxs-lookup"><span data-stu-id="08678-154">Value</span></span>                      | <span data-ttu-id="08678-155">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08678-155">Description</span></span>                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08678-156">**VS \_ FF- \_ Debug**</span><span class="sxs-lookup"><span data-stu-id="08678-156">**VS\_FF\_DEBUG**</span></span>          | <span data-ttu-id="08678-157">Die Datei enthält Debuginformationen oder wird mit aktivierten Debuggingfunktionen kompiliert.</span><span class="sxs-lookup"><span data-stu-id="08678-157">File contains debugging information or is compiled with debugging features enabled.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="08678-158">**VS \_ FF \_ gepatcht**</span><span class="sxs-lookup"><span data-stu-id="08678-158">**VS\_FF\_PATCHED**</span></span>        | <span data-ttu-id="08678-159">Die Datei wurde geändert und ist nicht identisch mit der ursprünglichen Versand Datei derselben Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="08678-159">File has been modified and is not identical to the original shipping file of the same version number.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="08678-160">**VS \_ FF- \_ Vorabversion**</span><span class="sxs-lookup"><span data-stu-id="08678-160">**VS\_FF\_PRERELEASE**</span></span>     | <span data-ttu-id="08678-161">Die Datei ist eine Entwicklungsversion und kein kommerziell veröffentlichtes Produkt.</span><span class="sxs-lookup"><span data-stu-id="08678-161">File is a development version, not a commercially released product.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="08678-162">**VS \_ FF \_ PrivateBuild**</span><span class="sxs-lookup"><span data-stu-id="08678-162">**VS\_FF\_PRIVATEBUILD**</span></span>   | <span data-ttu-id="08678-163">Die Datei wurde nicht mit standardmäßigen releaseprozeduren erstellt.</span><span class="sxs-lookup"><span data-stu-id="08678-163">File was not built using standard release procedures.</span></span> <span data-ttu-id="08678-164">Wenn dieser Wert angegeben wird, muss der [**stringfilinput FO-Block**](stringfileinfo-block.md) eine **PrivateBuild** -Zeichenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="08678-164">If this value is given, the [**StringFileInfo block**](stringfileinfo-block.md) must contain a **PrivateBuild** string.</span></span>                                                                                              |
| <span data-ttu-id="08678-165">**VS \_ FF \_ SpecialBuild**</span><span class="sxs-lookup"><span data-stu-id="08678-165">**VS\_FF\_SPECIALBUILD**</span></span>   | <span data-ttu-id="08678-166">Die Datei wurde vom ursprünglichen Unternehmen mithilfe von standardmäßigen releaseprozeduren erstellt, ist jedoch eine Variation der Standarddatei derselben Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="08678-166">File was built by the original company using standard release procedures but is a variation of the standard file of the same version number.</span></span> <span data-ttu-id="08678-167">Wenn dieser Wert angegeben wird, muss der [ **stringfilinput FO** -Block](stringfileinfo-block.md) Block eine **SpecialBuild** -Zeichenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="08678-167">If this value is given, the [**StringFileInfo** block](stringfileinfo-block.md) block must contain a **SpecialBuild** string.</span></span> |
| <span data-ttu-id="08678-168">**VS \_ FFI \_ fileflagsmask**</span><span class="sxs-lookup"><span data-stu-id="08678-168">**VS\_FFI\_FILEFLAGSMASK**</span></span> | <span data-ttu-id="08678-169">Eine Kombination aus allen vorangehenden Werten.</span><span class="sxs-lookup"><span data-stu-id="08678-169">A combination of all the preceding values.</span></span>                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="08678-170"><span id="fileos"></span><span id="FILEOS"></span>*FILEOS*</span><span class="sxs-lookup"><span data-stu-id="08678-170"><span id="fileos"></span><span id="FILEOS"></span>*fileos*</span></span>
</dt> <dd>

<span data-ttu-id="08678-171">Einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="08678-171">One of the following values.</span></span>



| <span data-ttu-id="08678-172">Wert</span><span class="sxs-lookup"><span data-stu-id="08678-172">Value</span></span>                   | <span data-ttu-id="08678-173">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08678-173">Description</span></span>                                                      |
|-------------------------|------------------------------------------------------------------|
| <span data-ttu-id="08678-174">**Vos \_ Unknown**</span><span class="sxs-lookup"><span data-stu-id="08678-174">**VOS\_UNKNOWN**</span></span>        | <span data-ttu-id="08678-175">Das Betriebssystem, für das die Datei entworfen wurde, ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="08678-175">The operating system for which the file was designed is unknown.</span></span> |
| <span data-ttu-id="08678-176">**Vos \_ DOS**</span><span class="sxs-lookup"><span data-stu-id="08678-176">**VOS\_DOS**</span></span>            | <span data-ttu-id="08678-177">Die Datei wurde für MS-DOS konzipiert.</span><span class="sxs-lookup"><span data-stu-id="08678-177">File was designed for MS-DOS.</span></span>                                    |
| <span data-ttu-id="08678-178">**Vos \_ NT**</span><span class="sxs-lookup"><span data-stu-id="08678-178">**VOS\_NT**</span></span>             | <span data-ttu-id="08678-179">Die Datei wurde für 32-Bit-Windows entwickelt.</span><span class="sxs-lookup"><span data-stu-id="08678-179">File was designed for 32-bit Windows.</span></span>                            |
| <span data-ttu-id="08678-180">**Vos \_ \_ WINDOWS16**</span><span class="sxs-lookup"><span data-stu-id="08678-180">**VOS\_\_WINDOWS16**</span></span>    | <span data-ttu-id="08678-181">Die Datei wurde für 16-Bit-Windows entwickelt.</span><span class="sxs-lookup"><span data-stu-id="08678-181">File was designed for 16-bit Windows.</span></span>                            |
| <span data-ttu-id="08678-182">**Vos \_ \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="08678-182">**VOS\_\_WINDOWS32**</span></span>    | <span data-ttu-id="08678-183">Die Datei wurde für 32-Bit-Windows entwickelt.</span><span class="sxs-lookup"><span data-stu-id="08678-183">File was designed for 32-bit Windows.</span></span>                            |
| <span data-ttu-id="08678-184">**Vos \_ DOS \_ WINDOWS16**</span><span class="sxs-lookup"><span data-stu-id="08678-184">**VOS\_DOS\_WINDOWS16**</span></span> | <span data-ttu-id="08678-185">Die Datei wurde für 16-Bit-Windows entwickelt, die mit MS-DOS ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08678-185">File was designed for 16-bit Windows running with MS-DOS.</span></span>        |
| <span data-ttu-id="08678-186">**Vos \_ DOS \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="08678-186">**VOS\_DOS\_WINDOWS32**</span></span> | <span data-ttu-id="08678-187">Die Datei wurde für 32-Bit-Windows entwickelt, die mit MS-DOS ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08678-187">File was designed for 32-bit Windows running with MS-DOS.</span></span>        |
| <span data-ttu-id="08678-188">**Vos \_ NT \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="08678-188">**VOS\_NT\_WINDOWS32**</span></span>  | <span data-ttu-id="08678-189">Die Datei wurde für 32-Bit-Windows entwickelt.</span><span class="sxs-lookup"><span data-stu-id="08678-189">File was designed for 32-bit Windows.</span></span>                            |



 

<span data-ttu-id="08678-190">Die Werte 0x00002l, 0x00003l, 0x20000l und 0x30000l sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="08678-190">The values 0x00002L, 0x00003L, 0x20000L and 0x30000L are reserved.</span></span>

</dd> <dt>

<span data-ttu-id="08678-191"><span id="filetype"></span><span id="FILETYPE"></span>*filetype*</span><span class="sxs-lookup"><span data-stu-id="08678-191"><span id="filetype"></span><span id="FILETYPE"></span>*filetype*</span></span>
</dt> <dd>

<span data-ttu-id="08678-192">Einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="08678-192">One of the following values.</span></span>



| <span data-ttu-id="08678-193">Wert</span><span class="sxs-lookup"><span data-stu-id="08678-193">Value</span></span>                | <span data-ttu-id="08678-194">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08678-194">Description</span></span>                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08678-195">**VFT \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="08678-195">**VFT\_UNKNOWN**</span></span>     | <span data-ttu-id="08678-196">Der Dateityp ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="08678-196">File type is unknown.</span></span>                                                                                                       |
| <span data-ttu-id="08678-197">**VFT- \_ App**</span><span class="sxs-lookup"><span data-stu-id="08678-197">**VFT\_APP**</span></span>         | <span data-ttu-id="08678-198">Die Datei enthält eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="08678-198">File contains an application.</span></span>                                                                                               |
| <span data-ttu-id="08678-199">**VFT- \_ dll**</span><span class="sxs-lookup"><span data-stu-id="08678-199">**VFT\_DLL**</span></span>         | <span data-ttu-id="08678-200">Die Datei enthält eine Dynamic Link Library (dll).</span><span class="sxs-lookup"><span data-stu-id="08678-200">File contains a dynamic-link library (DLL).</span></span>                                                                                 |
| <span data-ttu-id="08678-201">**VFT \_ drv**</span><span class="sxs-lookup"><span data-stu-id="08678-201">**VFT\_DRV**</span></span>         | <span data-ttu-id="08678-202">Die Datei enthält einen Gerätetreiber.</span><span class="sxs-lookup"><span data-stu-id="08678-202">File contains a device driver.</span></span> <span data-ttu-id="08678-203">Wenn *filetype* der **VFT \_ drv** ist, enthält der *Untertyp* eine spezifischere Beschreibung des Treibers.</span><span class="sxs-lookup"><span data-stu-id="08678-203">If *filetype* is **VFT\_DRV**, *subtype* contains a more specific description of the driver.</span></span> |
| <span data-ttu-id="08678-204">**VFT- \_ Schriftart**</span><span class="sxs-lookup"><span data-stu-id="08678-204">**VFT\_FONT**</span></span>        | <span data-ttu-id="08678-205">Die Datei enthält eine Schriftart.</span><span class="sxs-lookup"><span data-stu-id="08678-205">File contains a font.</span></span> <span data-ttu-id="08678-206">Wenn *filetype* die VFT- \_ Schriftart ist, enthält der *Untertyp* eine spezifischere Beschreibung der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="08678-206">If *filetype* is VFT\_FONT, *subtype* contains a more specific description of the font.</span></span>               |
| <span data-ttu-id="08678-207">**VFT \_ VxD**</span><span class="sxs-lookup"><span data-stu-id="08678-207">**VFT\_VXD**</span></span>         | <span data-ttu-id="08678-208">Die Datei enthält ein virtuelles Gerät.</span><span class="sxs-lookup"><span data-stu-id="08678-208">File contains a virtual device.</span></span>                                                                                             |
| <span data-ttu-id="08678-209">**statische VFT- \_ \_ lib**</span><span class="sxs-lookup"><span data-stu-id="08678-209">**VFT\_STATIC\_LIB**</span></span> | <span data-ttu-id="08678-210">Die Datei enthält eine Bibliothek mit statischem Link.</span><span class="sxs-lookup"><span data-stu-id="08678-210">File contains a static-link library.</span></span>                                                                                        |



 

<span data-ttu-id="08678-211">Alle anderen Werte sind für die Verwendung durch Microsoft reserviert.</span><span class="sxs-lookup"><span data-stu-id="08678-211">All other values are reserved for use by Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="08678-212"><span id="subtype"></span><span id="SUBTYPE"></span>*Untertyp*</span><span class="sxs-lookup"><span data-stu-id="08678-212"><span id="subtype"></span><span id="SUBTYPE"></span>*subtype*</span></span>
</dt> <dd>

<span data-ttu-id="08678-213">Weitere Informationen zum Dateityp.</span><span class="sxs-lookup"><span data-stu-id="08678-213">Additional information about the file type.</span></span>

<span data-ttu-id="08678-214">Wenn *filetype* den **VFT- \_ drv** angibt, kann dieser Parameter einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="08678-214">If *filetype* specifies **VFT\_DRV**, this parameter can be one of the following values.</span></span>



| <span data-ttu-id="08678-215">Wert</span><span class="sxs-lookup"><span data-stu-id="08678-215">Value</span></span>                             | <span data-ttu-id="08678-216">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08678-216">Description</span></span>                               |
|-----------------------------------|-------------------------------------------|
| <span data-ttu-id="08678-217">**VFT2 \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="08678-217">**VFT2\_UNKNOWN**</span></span>                 | <span data-ttu-id="08678-218">Der Treibertyp ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="08678-218">Driver type is unknown.</span></span>                   |
| <span data-ttu-id="08678-219">**VFT2 \_ drv- \_ comm**</span><span class="sxs-lookup"><span data-stu-id="08678-219">**VFT2\_DRV\_COMM**</span></span>               | <span data-ttu-id="08678-220">Die Datei enthält einen Kommunikationstreiber.</span><span class="sxs-lookup"><span data-stu-id="08678-220">File contains a communications driver.</span></span>    |
| <span data-ttu-id="08678-221">**VFT2 \_ drv- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="08678-221">**VFT2\_DRV\_PRINTER**</span></span>            | <span data-ttu-id="08678-222">Die Datei enthält einen Druckertreiber.</span><span class="sxs-lookup"><span data-stu-id="08678-222">File contains a printer driver.</span></span>           |
| <span data-ttu-id="08678-223">**VFT2 \_ drv- \_ Tastatur**</span><span class="sxs-lookup"><span data-stu-id="08678-223">**VFT2\_DRV\_KEYBOARD**</span></span>           | <span data-ttu-id="08678-224">Die Datei enthält einen Tastaturtreiber.</span><span class="sxs-lookup"><span data-stu-id="08678-224">File contains a keyboard driver.</span></span>          |
| <span data-ttu-id="08678-225">**VFT2 \_ drv- \_ Sprache**</span><span class="sxs-lookup"><span data-stu-id="08678-225">**VFT2\_DRV\_LANGUAGE**</span></span>           | <span data-ttu-id="08678-226">Die Datei enthält einen Sprachtreiber.</span><span class="sxs-lookup"><span data-stu-id="08678-226">File contains a language driver.</span></span>          |
| <span data-ttu-id="08678-227">**VFT2 \_ drv \_ anzeigen**</span><span class="sxs-lookup"><span data-stu-id="08678-227">**VFT2\_DRV\_DISPLAY**</span></span>            | <span data-ttu-id="08678-228">Die Datei enthält einen Anzeigetreiber.</span><span class="sxs-lookup"><span data-stu-id="08678-228">File contains a display driver.</span></span>           |
| <span data-ttu-id="08678-229">**VFT2 \_ drv- \_ Maus**</span><span class="sxs-lookup"><span data-stu-id="08678-229">**VFT2\_DRV\_MOUSE**</span></span>              | <span data-ttu-id="08678-230">Die Datei enthält einen Maustreiber.</span><span class="sxs-lookup"><span data-stu-id="08678-230">File contains a mouse driver.</span></span>             |
| <span data-ttu-id="08678-231">**VFT2 \_ drv- \_ Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="08678-231">**VFT2\_DRV\_NETWORK**</span></span>            | <span data-ttu-id="08678-232">Die Datei enthält einen Netzwerktreiber.</span><span class="sxs-lookup"><span data-stu-id="08678-232">File contains a network driver.</span></span>           |
| <span data-ttu-id="08678-233">**VFT2 \_ drv- \_ System**</span><span class="sxs-lookup"><span data-stu-id="08678-233">**VFT2\_DRV\_SYSTEM**</span></span>             | <span data-ttu-id="08678-234">Die Datei enthält einen System Treiber.</span><span class="sxs-lookup"><span data-stu-id="08678-234">File contains a system driver.</span></span>            |
| <span data-ttu-id="08678-235">**VFT2 \_ drv \_ installier Bar**</span><span class="sxs-lookup"><span data-stu-id="08678-235">**VFT2\_DRV\_INSTALLABLE**</span></span>        | <span data-ttu-id="08678-236">Die Datei enthält einen installierbaren Treiber.</span><span class="sxs-lookup"><span data-stu-id="08678-236">File contains an installable driver.</span></span>      |
| <span data-ttu-id="08678-237">**VFT2 \_ drv- \_ Sound**</span><span class="sxs-lookup"><span data-stu-id="08678-237">**VFT2\_DRV\_SOUND**</span></span>              | <span data-ttu-id="08678-238">Die Datei enthält einen Soundtreiber.</span><span class="sxs-lookup"><span data-stu-id="08678-238">File contains a sound driver.</span></span>             |
| <span data-ttu-id="08678-239">**VFT2 mit \_ drv \_ versionierter \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="08678-239">**VFT2\_DRV\_VERSIONED\_PRINTER**</span></span> | <span data-ttu-id="08678-240">Die Datei enthält einen Druckertreiber mit Versions Angabe.</span><span class="sxs-lookup"><span data-stu-id="08678-240">File contains a versioned printer driver.</span></span> |



 

<span data-ttu-id="08678-241">Wenn *filetype* die **VFT- \_ Schriftart** angibt, kann dieser Parameter einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="08678-241">If *filetype* specifies **VFT\_FONT**, this parameter can be one of the following values.</span></span>



| <span data-ttu-id="08678-242">Wert</span><span class="sxs-lookup"><span data-stu-id="08678-242">Value</span></span>                    | <span data-ttu-id="08678-243">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08678-243">Description</span></span>                    |
|--------------------------|--------------------------------|
| <span data-ttu-id="08678-244">**VFT2 \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="08678-244">**VFT2\_UNKNOWN**</span></span>        | <span data-ttu-id="08678-245">Der Schriftart ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="08678-245">Font type is unknown.</span></span>          |
| <span data-ttu-id="08678-246">**VFT2 \_ Schriftart \_ Raster**</span><span class="sxs-lookup"><span data-stu-id="08678-246">**VFT2\_FONT\_RASTER**</span></span>   | <span data-ttu-id="08678-247">Die Datei enthält eine Raster Schriftart.</span><span class="sxs-lookup"><span data-stu-id="08678-247">File contains a raster font.</span></span>   |
| <span data-ttu-id="08678-248">**VFT2- \_ Schriftart \_ Vektor**</span><span class="sxs-lookup"><span data-stu-id="08678-248">**VFT2\_FONT\_VECTOR**</span></span>   | <span data-ttu-id="08678-249">Die Datei enthält eine Vektor Schriftart.</span><span class="sxs-lookup"><span data-stu-id="08678-249">File contains a vector font.</span></span>   |
| <span data-ttu-id="08678-250">**VFT2 \_ Schriftart \_ TrueType**</span><span class="sxs-lookup"><span data-stu-id="08678-250">**VFT2\_FONT\_TRUETYPE**</span></span> | <span data-ttu-id="08678-251">Die Datei enthält eine TrueType-Schriftart.</span><span class="sxs-lookup"><span data-stu-id="08678-251">File contains a TrueType font.</span></span> |



 

<span data-ttu-id="08678-252">Wenn *filetype* VFT \_ VxD angibt, muss dieser Parameter der im Virtual Device-Kontroll Block enthaltene Bezeichner für virtuelle Geräte sein.</span><span class="sxs-lookup"><span data-stu-id="08678-252">If *filetype* specifies VFT\_VXD, this parameter must be the virtual-device identifier included in the virtual-device control block.</span></span>

<span data-ttu-id="08678-253">Alle *unter Typwerte* , die hier nicht aufgelistet sind, sind für die Verwendung durch Microsoft reserviert.</span><span class="sxs-lookup"><span data-stu-id="08678-253">All *subtype* values not listed here are reserved for use by Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="08678-254"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="08678-254"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="08678-255">Einer der folgenden Sprachcodes.</span><span class="sxs-lookup"><span data-stu-id="08678-255">One of the following language codes.</span></span>



| <span data-ttu-id="08678-256">Code</span><span class="sxs-lookup"><span data-stu-id="08678-256">Code</span></span>   | <span data-ttu-id="08678-257">Sprache</span><span class="sxs-lookup"><span data-stu-id="08678-257">Language</span></span>            | <span data-ttu-id="08678-258">Code</span><span class="sxs-lookup"><span data-stu-id="08678-258">Code</span></span>   | <span data-ttu-id="08678-259">Sprache</span><span class="sxs-lookup"><span data-stu-id="08678-259">Language</span></span>                  |
|--------|---------------------|--------|---------------------------|
| <span data-ttu-id="08678-260">0x0401</span><span class="sxs-lookup"><span data-stu-id="08678-260">0x0401</span></span> | <span data-ttu-id="08678-261">Arabisch</span><span class="sxs-lookup"><span data-stu-id="08678-261">Arabic</span></span>              | <span data-ttu-id="08678-262">0x0415</span><span class="sxs-lookup"><span data-stu-id="08678-262">0x0415</span></span> | <span data-ttu-id="08678-263">Polnisch</span><span class="sxs-lookup"><span data-stu-id="08678-263">Polish</span></span>                    |
| <span data-ttu-id="08678-264">0x0402</span><span class="sxs-lookup"><span data-stu-id="08678-264">0x0402</span></span> | <span data-ttu-id="08678-265">Bulgarisch</span><span class="sxs-lookup"><span data-stu-id="08678-265">Bulgarian</span></span>           | <span data-ttu-id="08678-266">0x0416</span><span class="sxs-lookup"><span data-stu-id="08678-266">0x0416</span></span> | <span data-ttu-id="08678-267">Portugiesisch (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="08678-267">Portuguese (Brazil)</span></span>       |
| <span data-ttu-id="08678-268">0x0403</span><span class="sxs-lookup"><span data-stu-id="08678-268">0x0403</span></span> | <span data-ttu-id="08678-269">Katalanisch</span><span class="sxs-lookup"><span data-stu-id="08678-269">Catalan</span></span>             | <span data-ttu-id="08678-270">0x0417</span><span class="sxs-lookup"><span data-stu-id="08678-270">0x0417</span></span> | <span data-ttu-id="08678-271">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="08678-271">Rhaeto-Romanic</span></span>            |
| <span data-ttu-id="08678-272">0x0404</span><span class="sxs-lookup"><span data-stu-id="08678-272">0x0404</span></span> | <span data-ttu-id="08678-273">Chinesisch (traditionell)</span><span class="sxs-lookup"><span data-stu-id="08678-273">Traditional Chinese</span></span> | <span data-ttu-id="08678-274">0x0418</span><span class="sxs-lookup"><span data-stu-id="08678-274">0x0418</span></span> | <span data-ttu-id="08678-275">Rumänisch</span><span class="sxs-lookup"><span data-stu-id="08678-275">Romanian</span></span>                  |
| <span data-ttu-id="08678-276">0x0405</span><span class="sxs-lookup"><span data-stu-id="08678-276">0x0405</span></span> | <span data-ttu-id="08678-277">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="08678-277">Czech</span></span>               | <span data-ttu-id="08678-278">0x0419</span><span class="sxs-lookup"><span data-stu-id="08678-278">0x0419</span></span> | <span data-ttu-id="08678-279">Russisch</span><span class="sxs-lookup"><span data-stu-id="08678-279">Russian</span></span>                   |
| <span data-ttu-id="08678-280">0x0406</span><span class="sxs-lookup"><span data-stu-id="08678-280">0x0406</span></span> | <span data-ttu-id="08678-281">Dänisch</span><span class="sxs-lookup"><span data-stu-id="08678-281">Danish</span></span>              | <span data-ttu-id="08678-282">0x041a</span><span class="sxs-lookup"><span data-stu-id="08678-282">0x041A</span></span> | <span data-ttu-id="08678-283">Croato-Serbian (lateinisch)</span><span class="sxs-lookup"><span data-stu-id="08678-283">Croato-Serbian (Latin)</span></span>    |
| <span data-ttu-id="08678-284">0x0407</span><span class="sxs-lookup"><span data-stu-id="08678-284">0x0407</span></span> | <span data-ttu-id="08678-285">Deutsch</span><span class="sxs-lookup"><span data-stu-id="08678-285">German</span></span>              | <span data-ttu-id="08678-286">0x041b</span><span class="sxs-lookup"><span data-stu-id="08678-286">0x041B</span></span> | <span data-ttu-id="08678-287">Slowakisch</span><span class="sxs-lookup"><span data-stu-id="08678-287">Slovak</span></span>                    |
| <span data-ttu-id="08678-288">0x0408</span><span class="sxs-lookup"><span data-stu-id="08678-288">0x0408</span></span> | <span data-ttu-id="08678-289">Griechisch</span><span class="sxs-lookup"><span data-stu-id="08678-289">Greek</span></span>               | <span data-ttu-id="08678-290">0x041c</span><span class="sxs-lookup"><span data-stu-id="08678-290">0x041C</span></span> | <span data-ttu-id="08678-291">Albanisch</span><span class="sxs-lookup"><span data-stu-id="08678-291">Albanian</span></span>                  |
| <span data-ttu-id="08678-292">0x0409</span><span class="sxs-lookup"><span data-stu-id="08678-292">0x0409</span></span> | <span data-ttu-id="08678-293">US-Englisch</span><span class="sxs-lookup"><span data-stu-id="08678-293">U.S. English</span></span>        | <span data-ttu-id="08678-294">0x041d</span><span class="sxs-lookup"><span data-stu-id="08678-294">0x041D</span></span> | <span data-ttu-id="08678-295">Schwedisch</span><span class="sxs-lookup"><span data-stu-id="08678-295">Swedish</span></span>                   |
| <span data-ttu-id="08678-296">0x040A</span><span class="sxs-lookup"><span data-stu-id="08678-296">0x040A</span></span> | <span data-ttu-id="08678-297">Castilisch Spanisch</span><span class="sxs-lookup"><span data-stu-id="08678-297">Castilian Spanish</span></span>   | <span data-ttu-id="08678-298">0x041E</span><span class="sxs-lookup"><span data-stu-id="08678-298">0x041E</span></span> | <span data-ttu-id="08678-299">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="08678-299">Thai</span></span>                      |
| <span data-ttu-id="08678-300">0x040b</span><span class="sxs-lookup"><span data-stu-id="08678-300">0x040B</span></span> | <span data-ttu-id="08678-301">Finnisch</span><span class="sxs-lookup"><span data-stu-id="08678-301">Finnish</span></span>             | <span data-ttu-id="08678-302">0x041f</span><span class="sxs-lookup"><span data-stu-id="08678-302">0x041F</span></span> | <span data-ttu-id="08678-303">Türkisch</span><span class="sxs-lookup"><span data-stu-id="08678-303">Turkish</span></span>                   |
| <span data-ttu-id="08678-304">0x040c</span><span class="sxs-lookup"><span data-stu-id="08678-304">0x040C</span></span> | <span data-ttu-id="08678-305">Französisch</span><span class="sxs-lookup"><span data-stu-id="08678-305">French</span></span>              | <span data-ttu-id="08678-306">0x0420</span><span class="sxs-lookup"><span data-stu-id="08678-306">0x0420</span></span> | <span data-ttu-id="08678-307">Urdu</span><span class="sxs-lookup"><span data-stu-id="08678-307">Urdu</span></span>                      |
| <span data-ttu-id="08678-308">0x040d</span><span class="sxs-lookup"><span data-stu-id="08678-308">0x040D</span></span> | <span data-ttu-id="08678-309">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="08678-309">Hebrew</span></span>              | <span data-ttu-id="08678-310">0x0421</span><span class="sxs-lookup"><span data-stu-id="08678-310">0x0421</span></span> | <span data-ttu-id="08678-311">Bahasa</span><span class="sxs-lookup"><span data-stu-id="08678-311">Bahasa</span></span>                    |
| <span data-ttu-id="08678-312">0x040e</span><span class="sxs-lookup"><span data-stu-id="08678-312">0x040E</span></span> | <span data-ttu-id="08678-313">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="08678-313">Hungarian</span></span>           | <span data-ttu-id="08678-314">0x0804</span><span class="sxs-lookup"><span data-stu-id="08678-314">0x0804</span></span> | <span data-ttu-id="08678-315">Chinesisch (vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="08678-315">Simplified Chinese</span></span>        |
| <span data-ttu-id="08678-316">0x040f</span><span class="sxs-lookup"><span data-stu-id="08678-316">0x040F</span></span> | <span data-ttu-id="08678-317">Isländisch</span><span class="sxs-lookup"><span data-stu-id="08678-317">Icelandic</span></span>           | <span data-ttu-id="08678-318">0x0807</span><span class="sxs-lookup"><span data-stu-id="08678-318">0x0807</span></span> | <span data-ttu-id="08678-319">Deutsch (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="08678-319">Swiss German</span></span>              |
| <span data-ttu-id="08678-320">0x0410</span><span class="sxs-lookup"><span data-stu-id="08678-320">0x0410</span></span> | <span data-ttu-id="08678-321">Italienisch</span><span class="sxs-lookup"><span data-stu-id="08678-321">Italian</span></span>             | <span data-ttu-id="08678-322">0x0809</span><span class="sxs-lookup"><span data-stu-id="08678-322">0x0809</span></span> | <span data-ttu-id="08678-323">Vereinigtes Königreich:</span><span class="sxs-lookup"><span data-stu-id="08678-323">U.K.</span></span> <span data-ttu-id="08678-324">Englisch</span><span class="sxs-lookup"><span data-stu-id="08678-324">English</span></span>              |
| <span data-ttu-id="08678-325">0x0411</span><span class="sxs-lookup"><span data-stu-id="08678-325">0x0411</span></span> | <span data-ttu-id="08678-326">Japanisch</span><span class="sxs-lookup"><span data-stu-id="08678-326">Japanese</span></span>            | <span data-ttu-id="08678-327">0x080a</span><span class="sxs-lookup"><span data-stu-id="08678-327">0x080A</span></span> | <span data-ttu-id="08678-328">Spanisch (Mexiko)</span><span class="sxs-lookup"><span data-stu-id="08678-328">Spanish (Mexico)</span></span>          |
| <span data-ttu-id="08678-329">0x0412</span><span class="sxs-lookup"><span data-stu-id="08678-329">0x0412</span></span> | <span data-ttu-id="08678-330">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="08678-330">Korean</span></span>              | <span data-ttu-id="08678-331">0x080c</span><span class="sxs-lookup"><span data-stu-id="08678-331">0x080C</span></span> | <span data-ttu-id="08678-332">Französisch (Belgien)</span><span class="sxs-lookup"><span data-stu-id="08678-332">Belgian French</span></span>            |
| <span data-ttu-id="08678-333">0x0413</span><span class="sxs-lookup"><span data-stu-id="08678-333">0x0413</span></span> | <span data-ttu-id="08678-334">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="08678-334">Dutch</span></span>               | <span data-ttu-id="08678-335">0x0c0c</span><span class="sxs-lookup"><span data-stu-id="08678-335">0x0C0C</span></span> | <span data-ttu-id="08678-336">Französisch (Kanada)</span><span class="sxs-lookup"><span data-stu-id="08678-336">Canadian French</span></span>           |
| <span data-ttu-id="08678-337">0x0414</span><span class="sxs-lookup"><span data-stu-id="08678-337">0x0414</span></span> | <span data-ttu-id="08678-338">Norwegisch?</span><span class="sxs-lookup"><span data-stu-id="08678-338">Norwegian ?</span></span> <span data-ttu-id="08678-339">Bokmal</span><span class="sxs-lookup"><span data-stu-id="08678-339">Bokmal</span></span>  | <span data-ttu-id="08678-340">0x100c</span><span class="sxs-lookup"><span data-stu-id="08678-340">0x100C</span></span> | <span data-ttu-id="08678-341">Schweiz Französisch</span><span class="sxs-lookup"><span data-stu-id="08678-341">Swiss French</span></span>              |
| <span data-ttu-id="08678-342">0x0810</span><span class="sxs-lookup"><span data-stu-id="08678-342">0x0810</span></span> | <span data-ttu-id="08678-343">Schweizer Italienisch</span><span class="sxs-lookup"><span data-stu-id="08678-343">Swiss Italian</span></span>       | <span data-ttu-id="08678-344">0x0816</span><span class="sxs-lookup"><span data-stu-id="08678-344">0x0816</span></span> | <span data-ttu-id="08678-345">Portugiesisch (Portugal)</span><span class="sxs-lookup"><span data-stu-id="08678-345">Portuguese (Portugal)</span></span>     |
| <span data-ttu-id="08678-346">0x0813</span><span class="sxs-lookup"><span data-stu-id="08678-346">0x0813</span></span> | <span data-ttu-id="08678-347">Belgisch Niederländisch</span><span class="sxs-lookup"><span data-stu-id="08678-347">Belgian Dutch</span></span>       | <span data-ttu-id="08678-348">0x081a</span><span class="sxs-lookup"><span data-stu-id="08678-348">0x081A</span></span> | <span data-ttu-id="08678-349">Serbo-Croatian (Kyrillisch)</span><span class="sxs-lookup"><span data-stu-id="08678-349">Serbo-Croatian (Cyrillic)</span></span> |
| <span data-ttu-id="08678-350">0x0814</span><span class="sxs-lookup"><span data-stu-id="08678-350">0x0814</span></span> | <span data-ttu-id="08678-351">Norwegisch?</span><span class="sxs-lookup"><span data-stu-id="08678-351">Norwegian ?</span></span> <span data-ttu-id="08678-352">Nynorsk</span><span class="sxs-lookup"><span data-stu-id="08678-352">Nynorsk</span></span> |        |                           |



 

</dd> <dt>

<span data-ttu-id="08678-353"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charder TID*</span><span class="sxs-lookup"><span data-stu-id="08678-353"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span></span>
</dt> <dd>

<span data-ttu-id="08678-354">Einer der folgenden Zeichensatz Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="08678-354">One of the following character-set identifiers.</span></span>



| <span data-ttu-id="08678-355">Decimal</span><span class="sxs-lookup"><span data-stu-id="08678-355">Decimal</span></span> | <span data-ttu-id="08678-356">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="08678-356">Hexadecimal</span></span> | <span data-ttu-id="08678-357">Zeichensatz</span><span class="sxs-lookup"><span data-stu-id="08678-357">Character Set</span></span>              |
|---------|-------------|----------------------------|
| <span data-ttu-id="08678-358">0</span><span class="sxs-lookup"><span data-stu-id="08678-358">0</span></span>       | <span data-ttu-id="08678-359">0000</span><span class="sxs-lookup"><span data-stu-id="08678-359">0000</span></span>        | <span data-ttu-id="08678-360">7-Bit-ASCII</span><span class="sxs-lookup"><span data-stu-id="08678-360">7-bit ASCII</span></span>                |
| <span data-ttu-id="08678-361">932</span><span class="sxs-lookup"><span data-stu-id="08678-361">932</span></span>     | <span data-ttu-id="08678-362">03a4</span><span class="sxs-lookup"><span data-stu-id="08678-362">03A4</span></span>        | <span data-ttu-id="08678-363">Japan (Schicht?</span><span class="sxs-lookup"><span data-stu-id="08678-363">Japan (Shift ?</span></span> <span data-ttu-id="08678-364">JIS X-0208)</span><span class="sxs-lookup"><span data-stu-id="08678-364">JIS X-0208)</span></span> |
| <span data-ttu-id="08678-365">949</span><span class="sxs-lookup"><span data-stu-id="08678-365">949</span></span>     | <span data-ttu-id="08678-366">03b5</span><span class="sxs-lookup"><span data-stu-id="08678-366">03B5</span></span>        | <span data-ttu-id="08678-367">Korea (Schicht?</span><span class="sxs-lookup"><span data-stu-id="08678-367">Korea (Shift ?</span></span> <span data-ttu-id="08678-368">KSC 5601)</span><span class="sxs-lookup"><span data-stu-id="08678-368">KSC 5601)</span></span>   |
| <span data-ttu-id="08678-369">950</span><span class="sxs-lookup"><span data-stu-id="08678-369">950</span></span>     | <span data-ttu-id="08678-370">03b6</span><span class="sxs-lookup"><span data-stu-id="08678-370">03B6</span></span>        | <span data-ttu-id="08678-371">Taiwan (Big5)</span><span class="sxs-lookup"><span data-stu-id="08678-371">Taiwan (Big5)</span></span>              |
| <span data-ttu-id="08678-372">1200</span><span class="sxs-lookup"><span data-stu-id="08678-372">1200</span></span>    | <span data-ttu-id="08678-373">04b0</span><span class="sxs-lookup"><span data-stu-id="08678-373">04B0</span></span>        | <span data-ttu-id="08678-374">Unicode</span><span class="sxs-lookup"><span data-stu-id="08678-374">Unicode</span></span>                    |
| <span data-ttu-id="08678-375">1250</span><span class="sxs-lookup"><span data-stu-id="08678-375">1250</span></span>    | <span data-ttu-id="08678-376">04e2</span><span class="sxs-lookup"><span data-stu-id="08678-376">04E2</span></span>        | <span data-ttu-id="08678-377">Lateinisch-2 (Osteuropäisch)</span><span class="sxs-lookup"><span data-stu-id="08678-377">Latin-2 (Eastern European)</span></span> |
| <span data-ttu-id="08678-378">1251</span><span class="sxs-lookup"><span data-stu-id="08678-378">1251</span></span>    | <span data-ttu-id="08678-379">04e3</span><span class="sxs-lookup"><span data-stu-id="08678-379">04E3</span></span>        | <span data-ttu-id="08678-380">Kyrillisch</span><span class="sxs-lookup"><span data-stu-id="08678-380">Cyrillic</span></span>                   |
| <span data-ttu-id="08678-381">1252</span><span class="sxs-lookup"><span data-stu-id="08678-381">1252</span></span>    | <span data-ttu-id="08678-382">04e4</span><span class="sxs-lookup"><span data-stu-id="08678-382">04E4</span></span>        | <span data-ttu-id="08678-383">Mehrsprachige</span><span class="sxs-lookup"><span data-stu-id="08678-383">Multilingual</span></span>               |
| <span data-ttu-id="08678-384">1253</span><span class="sxs-lookup"><span data-stu-id="08678-384">1253</span></span>    | <span data-ttu-id="08678-385">04e5</span><span class="sxs-lookup"><span data-stu-id="08678-385">04E5</span></span>        | <span data-ttu-id="08678-386">Griechisch</span><span class="sxs-lookup"><span data-stu-id="08678-386">Greek</span></span>                      |
| <span data-ttu-id="08678-387">1254</span><span class="sxs-lookup"><span data-stu-id="08678-387">1254</span></span>    | <span data-ttu-id="08678-388">04e6</span><span class="sxs-lookup"><span data-stu-id="08678-388">04E6</span></span>        | <span data-ttu-id="08678-389">Türkisch</span><span class="sxs-lookup"><span data-stu-id="08678-389">Turkish</span></span>                    |
| <span data-ttu-id="08678-390">1255</span><span class="sxs-lookup"><span data-stu-id="08678-390">1255</span></span>    | <span data-ttu-id="08678-391">04e7</span><span class="sxs-lookup"><span data-stu-id="08678-391">04E7</span></span>        | <span data-ttu-id="08678-392">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="08678-392">Hebrew</span></span>                     |
| <span data-ttu-id="08678-393">1256</span><span class="sxs-lookup"><span data-stu-id="08678-393">1256</span></span>    | <span data-ttu-id="08678-394">04e8</span><span class="sxs-lookup"><span data-stu-id="08678-394">04E8</span></span>        | <span data-ttu-id="08678-395">Arabisch</span><span class="sxs-lookup"><span data-stu-id="08678-395">Arabic</span></span>                     |



 

</dd> <dt>

<span data-ttu-id="08678-396"><span id="string-name"></span><span id="STRING-NAME"></span>*Zeichen folgen Name*</span><span class="sxs-lookup"><span data-stu-id="08678-396"><span id="string-name"></span><span id="STRING-NAME"></span>*string-name*</span></span>
</dt> <dd>

<span data-ttu-id="08678-397">Einer der folgenden vordefinierten Namen.</span><span class="sxs-lookup"><span data-stu-id="08678-397">One of the following predefined names.</span></span>



| <span data-ttu-id="08678-398">Name</span><span class="sxs-lookup"><span data-stu-id="08678-398">Name</span></span>                 | <span data-ttu-id="08678-399">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08678-399">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08678-400">**Kommentare**</span><span class="sxs-lookup"><span data-stu-id="08678-400">**Comments**</span></span>         | <span data-ttu-id="08678-401">Zusätzliche Informationen, die zu Diagnose Zwecken angezeigt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="08678-401">Additional information that should be displayed for diagnostic purposes.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="08678-402">**CompanyName**</span><span class="sxs-lookup"><span data-stu-id="08678-402">**CompanyName**</span></span>      | <span data-ttu-id="08678-403">Das Unternehmen, das die Datei erstellt hat, z. b. "Microsoft Corporation" oder "Standard Microsystems Corporation, Inc."</span><span class="sxs-lookup"><span data-stu-id="08678-403">Company that produced the file?for example, "Microsoft Corporation" or "Standard Microsystems Corporation, Inc."</span></span> <span data-ttu-id="08678-404">Diese Zeichenfolge ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="08678-404">This string is required.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="08678-405">**FileDescription**</span><span class="sxs-lookup"><span data-stu-id="08678-405">**FileDescription**</span></span>  | <span data-ttu-id="08678-406">Die Dateibeschreibung, die Benutzern angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="08678-406">File description to be presented to users.</span></span> <span data-ttu-id="08678-407">Diese Zeichenfolge wird möglicherweise in einem Listenfeld angezeigt, wenn der Benutzer die zu installierenden Dateien auswählt, z. b. "Tastaturtreiber für AT-Style-Tastaturen".</span><span class="sxs-lookup"><span data-stu-id="08678-407">This string may be displayed in a list box when the user is choosing files to install?for example, "Keyboard Driver for AT-Style Keyboards".</span></span> <span data-ttu-id="08678-408">Diese Zeichenfolge ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="08678-408">This string is required.</span></span>                                                                                            |
| <span data-ttu-id="08678-409">**FileVersion**</span><span class="sxs-lookup"><span data-stu-id="08678-409">**FileVersion**</span></span>      | <span data-ttu-id="08678-410">Versionsnummer der Datei, z. b. "3,10" oder "5.00. RC2".</span><span class="sxs-lookup"><span data-stu-id="08678-410">Version number of the file?for example, "3.10" or "5.00.RC2".</span></span> <span data-ttu-id="08678-411">Diese Zeichenfolge ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="08678-411">This string is required.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="08678-412">**InternalName**</span><span class="sxs-lookup"><span data-stu-id="08678-412">**InternalName**</span></span>     | <span data-ttu-id="08678-413">Interner Name der Datei (sofern vorhanden), z. b. ein Modulname, wenn es sich bei der Datei um eine Dynamic Link Library handelt.</span><span class="sxs-lookup"><span data-stu-id="08678-413">Internal name of the file, if one exists?for example, a module name if the file is a dynamic-link library.</span></span> <span data-ttu-id="08678-414">Wenn die Datei keinen internen Namen hat, sollte diese Zeichenfolge der ursprüngliche Dateiname ohne Erweiterung sein.</span><span class="sxs-lookup"><span data-stu-id="08678-414">If the file has no internal name, this string should be the original filename, without extension.</span></span> <span data-ttu-id="08678-415">Diese Zeichenfolge ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="08678-415">This string is required.</span></span>                                                                       |
| <span data-ttu-id="08678-416">**LegalCopyright**</span><span class="sxs-lookup"><span data-stu-id="08678-416">**LegalCopyright**</span></span>   | <span data-ttu-id="08678-417">Copyright Hinweise, die für die Datei gelten.</span><span class="sxs-lookup"><span data-stu-id="08678-417">Copyright notices that apply to the file.</span></span> <span data-ttu-id="08678-418">Dies sollte den vollständigen Text aller Hinweise, rechtliche Symbole, Copyright Daten usw. enthalten.</span><span class="sxs-lookup"><span data-stu-id="08678-418">This should include the full text of all notices, legal symbols, copyright dates, and so on.</span></span> <span data-ttu-id="08678-419">Diese Zeichenfolge ist optional.</span><span class="sxs-lookup"><span data-stu-id="08678-419">This string is optional.</span></span>                                                                                                                                             |
| <span data-ttu-id="08678-420">**LegalTrademarks**</span><span class="sxs-lookup"><span data-stu-id="08678-420">**LegalTrademarks**</span></span>  | <span data-ttu-id="08678-421">Marken und eingetragene Marken, die auf die Datei angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="08678-421">Trademarks and registered trademarks that apply to the file.</span></span> <span data-ttu-id="08678-422">Dies sollte den vollständigen Text aller Hinweise, rechtliche Symbole, Markennummern usw. umfassen.</span><span class="sxs-lookup"><span data-stu-id="08678-422">This should include the full text of all notices, legal symbols, trademark numbers, and so on.</span></span> <span data-ttu-id="08678-423">Diese Zeichenfolge ist optional.</span><span class="sxs-lookup"><span data-stu-id="08678-423">This string is optional.</span></span>                                                                                                                        |
| <span data-ttu-id="08678-424">**OriginalFilename**</span><span class="sxs-lookup"><span data-stu-id="08678-424">**OriginalFilename**</span></span> | <span data-ttu-id="08678-425">Ursprünglicher Name der Datei ohne Pfad.</span><span class="sxs-lookup"><span data-stu-id="08678-425">Original name of the file, not including a path.</span></span> <span data-ttu-id="08678-426">Mithilfe dieser Informationen kann eine Anwendung ermitteln, ob eine Datei von einem Benutzer umbenannt wurde.</span><span class="sxs-lookup"><span data-stu-id="08678-426">This information enables an application to determine whether a file has been renamed by a user.</span></span> <span data-ttu-id="08678-427">Das Format des Namens hängt vom Dateisystem ab, für das die Datei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="08678-427">The format of the name depends on the file system for which the file was created.</span></span> <span data-ttu-id="08678-428">Diese Zeichenfolge ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="08678-428">This string is required.</span></span>                                                 |
| <span data-ttu-id="08678-429">**PrivateBuild**</span><span class="sxs-lookup"><span data-stu-id="08678-429">**PrivateBuild**</span></span>     | <span data-ttu-id="08678-430">Informationen über eine private Version der Datei, z. b. "erstellt von TESTER1 auf \\ Testbed".</span><span class="sxs-lookup"><span data-stu-id="08678-430">Information about a private version of the file?for example, "Built by TESTER1 on \\TESTBED".</span></span> <span data-ttu-id="08678-431">Diese Zeichenfolge sollte nur vorhanden sein, wenn **vs \_ FF \_ PrivateBuild** im *FILEFLAGS* -Parameter des root-Blocks angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="08678-431">This string should be present only if **VS\_FF\_PRIVATEBUILD** is specified in the *fileflags* parameter of the root block.</span></span>                                                                                   |
| <span data-ttu-id="08678-432">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="08678-432">**ProductName**</span></span>      | <span data-ttu-id="08678-433">Der Name des Produkts, mit dem die Datei verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="08678-433">Name of the product with which the file is distributed.</span></span> <span data-ttu-id="08678-434">Diese Zeichenfolge ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="08678-434">This string is required.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="08678-435">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="08678-435">**ProductVersion**</span></span>   | <span data-ttu-id="08678-436">Version des Produkts, mit dem die Datei verteilt wird, z. b. "3,10" oder "5.00. RC2".</span><span class="sxs-lookup"><span data-stu-id="08678-436">Version of the product with which the file is distributed?for example, "3.10" or "5.00.RC2".</span></span> <span data-ttu-id="08678-437">Diese Zeichenfolge ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="08678-437">This string is required.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="08678-438">**SpecialBuild**</span><span class="sxs-lookup"><span data-stu-id="08678-438">**SpecialBuild**</span></span>     | <span data-ttu-id="08678-439">Text, der angibt, wie diese Version der Datei von der Standardversion abweicht, z. b. "privater Build für TESTER1 lösen von Maus Problemen auf M250-und M250E-Computern".</span><span class="sxs-lookup"><span data-stu-id="08678-439">Text that indicates how this version of the file differs from the standard version?for example, "Private build for TESTER1 solving mouse problems on M250 and M250E computers".</span></span> <span data-ttu-id="08678-440">Diese Zeichenfolge sollte nur vorhanden sein, wenn **vs \_ FF \_ SpecialBuild** im *FILEFLAGS* -Parameter des root-Blocks angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="08678-440">This string should be present only if **VS\_FF\_SPECIALBUILD** is specified in the *fileflags* parameter of the root block.</span></span> |



 

</dd> </dl>

<span data-ttu-id="08678-441">Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08678-441">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="08678-442">Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="08678-442">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="08678-443">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08678-443">Examples</span></span>

<span data-ttu-id="08678-444">Im folgenden Beispiel wird eine **VERSIONINFO** -Ressource definiert:</span><span class="sxs-lookup"><span data-stu-id="08678-444">The following example defines a **VERSIONINFO** resource:</span></span>

``` syntax
#define VER_FILEVERSION             3,10,349,0
#define VER_FILEVERSION_STR         "3.10.349.0\0"

#define VER_PRODUCTVERSION          3,10,0,0
#define VER_PRODUCTVERSION_STR      "3.10\0"

#ifndef DEBUG
#define VER_DEBUG                   0
#else
#define VER_DEBUG                   VS_FF_DEBUG
#endif

VS_VERSION_INFO VERSIONINFO
FILEVERSION     VER_FILEVERSION
PRODUCTVERSION  VER_PRODUCTVERSION
FILEFLAGSMASK   VS_FFI_FILEFLAGSMASK
FILEFLAGS       (VER_PRIVATEBUILD|VER_PRERELEASE|VER_DEBUG)
FILEOS          VOS__WINDOWS32
FILETYPE        VFT_DLL
FILESUBTYPE     VFT2_UNKNOWN
BEGIN
    BLOCK "StringFileInfo"
    BEGIN
        BLOCK "040904E4"
        BEGIN
            VALUE "CompanyName",      VER_COMPANYNAME_STR
            VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
            VALUE "FileVersion",      VER_FILEVERSION_STR
            VALUE "InternalName",     VER_INTERNALNAME_STR
            VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
            VALUE "LegalTrademarks1", VER_LEGALTRADEMARKS1_STR
            VALUE "LegalTrademarks2", VER_LEGALTRADEMARKS2_STR
            VALUE "OriginalFilename", VER_ORIGINALFILENAME_STR
            VALUE "ProductName",      VER_PRODUCTNAME_STR
            VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
        END
    END

    BLOCK "VarFileInfo"
    BEGIN
        /* The following line should only be modified for localized versions.     */
        /* It consists of any number of WORD,WORD pairs, with each pair           */
        /* describing a language,codepage combination supported by the file.      */
        /*                                                                        */
        /* For example, a file might have values "0x409,1252" indicating that it  */
        /* supports English language (0x409) in the Windows ANSI codepage (1252). */

        VALUE "Translation", 0x409, 1252

    END
END
```

## <a name="see-also"></a><span data-ttu-id="08678-445">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08678-445">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08678-446">Verwenden von Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="08678-446">Using Version Information</span></span>](./using-version-information.md)
</dt> <dt>

[<span data-ttu-id="08678-447">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="08678-447">Version Information</span></span>](./version-information.md)
</dt> </dl>

 

 