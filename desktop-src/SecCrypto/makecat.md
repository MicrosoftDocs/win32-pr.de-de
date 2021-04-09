---
description: Ein CryptoAPI-Tool, mit dem eine Katalog Datei erstellt wird.
ms.assetid: 233b3644-f2a5-4166-bac0-30bf2f54e957
title: MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6c2c3cb1d7df5a9f717143465d48d4c066466d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862843"
---
# <a name="makecat"></a><span data-ttu-id="a5984-103">MakeCat</span><span class="sxs-lookup"><span data-stu-id="a5984-103">MakeCat</span></span>

<span data-ttu-id="a5984-104">Das Tool MakeCat ist ein CryptoAPI-Tool, mit dem eine Katalog Datei erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a5984-104">The MakeCat tool is a CryptoAPI tool that creates a catalog file.</span></span> <span data-ttu-id="a5984-105">MakeCat ist als Teil des Microsoft Windows Software Development Kit (SDK) für Windows 7 und .NET Framework 4,0 verfügbar und wird standardmäßig im \\ Ordner "bin" des SDK-Installations Pfads installiert.</span><span class="sxs-lookup"><span data-stu-id="a5984-105">MakeCat is available as part of the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0 and is installed, by default, in the \\Bin folder of the SDK installation path.</span></span>

<span data-ttu-id="a5984-106">Das MakeCat-Tool verwendet die folgende Befehlssyntax:</span><span class="sxs-lookup"><span data-stu-id="a5984-106">The MakeCat tool uses the following command syntax:</span></span>

<span data-ttu-id="a5984-107">**MakeCat** \[ **-n** \| **-r** \| **-v** \] *Dateiname*</span><span class="sxs-lookup"><span data-stu-id="a5984-107">**MakeCat** \[**-n**\|**-r**\|**-v**\] *FileName*</span></span>

## <a name="parameters"></a><span data-ttu-id="a5984-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5984-108">Parameters</span></span>



| <span data-ttu-id="a5984-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5984-109">Parameter</span></span>             | <span data-ttu-id="a5984-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5984-110">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5984-111">**-n**</span><span class="sxs-lookup"><span data-stu-id="a5984-111">**-n**</span></span><br/>     | <span data-ttu-id="a5984-112">Bei einem BEHEB baren Fehler nicht anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="a5984-112">Do not stop on a recoverable error.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="a5984-113">**-r**</span><span class="sxs-lookup"><span data-stu-id="a5984-113">**-r**</span></span><br/>     | <span data-ttu-id="a5984-114">Erzwingt das Beenden von MakeCat, wenn wiederherstellbare Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="a5984-114">Forces MakeCat to end if it encounters recoverable errors.</span></span> <span data-ttu-id="a5984-115">Dies gilt insbesondere, wenn die Einträge im Abschnitt Katalogdateien einer CDF-Datei verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a5984-115">Specifically, it will end when processing the entries in the catalog files section of a .cdf file.</span></span><br/> |
| <span data-ttu-id="a5984-116">**-v**</span><span class="sxs-lookup"><span data-stu-id="a5984-116">**-v**</span></span><br/>     | <span data-ttu-id="a5984-117">Ausführlich.</span><span class="sxs-lookup"><span data-stu-id="a5984-117">Verbose.</span></span> <span data-ttu-id="a5984-118">Zeigt alle Status-und Fehlermeldungen an.</span><span class="sxs-lookup"><span data-stu-id="a5984-118">Displays all progress and error messages.</span></span><br/>                                                                                                            |
| <span data-ttu-id="a5984-119">*FileName*</span><span class="sxs-lookup"><span data-stu-id="a5984-119">*FileName*</span></span><br/> | <span data-ttu-id="a5984-120">Der Name der zu analysierten CDF-Datei.</span><span class="sxs-lookup"><span data-stu-id="a5984-120">Name of the .cdf file to be parsed.</span></span> <span data-ttu-id="a5984-121">Informationen zu den erforderlichen Strukturen und Inhalten finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="a5984-121">For required structure and contents, see Remarks.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="a5984-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5984-122">Remarks</span></span>

<span data-ttu-id="a5984-123">Die CDF-Datei muss mit den folgenden Spezifikationen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a5984-123">The .cdf file must be built with the following specifications.</span></span>

``` syntax
[CatalogHeader]
Name=Name              
ResultDir=ResultDir   
PublicVersion=[|1]
CatalogVersion = [|1|2]
HashAlgorithms=[|SHA1|SHA256]
PageHashes=[true|false]
EncodingType=Encodingtype 
CATATTR1={type}:{oid}:{value} (optional)
CATATTR2={type}:{oid}:{value} (optional)

[CatalogFiles]
{reference tag}=file path and name
{reference tag}ALTSIPID={guid} (optional)
{reference tag}ATTR1={type}:{oid}:{value} (optional)
{reference tag}ATTR2={type}:{oid}:{value} (optional)
<HASH>kernel32.dll=kernel32.dll
<HASH>ntdll.dll=ntdll.dll
```

> [!Note]  
> <span data-ttu-id="a5984-124">Der letzte Eintrag in der CDF-Datei muss immer über ein explizites Zeilen Trennzeichen am Ende der Zeile verfügen.</span><span class="sxs-lookup"><span data-stu-id="a5984-124">The last entry in the .cdf file must always have an explicit newline character at the end of the line.</span></span>

 

<span data-ttu-id="a5984-125">Der \[ Abschnitt catalogheader \] definiert Informationen über die gesamte Katalog Datei.</span><span class="sxs-lookup"><span data-stu-id="a5984-125">The \[CatalogHeader\] section defines information about the entire catalog file.</span></span>



| <span data-ttu-id="a5984-126">Option</span><span class="sxs-lookup"><span data-stu-id="a5984-126">Option</span></span>                    | <span data-ttu-id="a5984-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5984-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5984-128">Name</span><span class="sxs-lookup"><span data-stu-id="a5984-128">Name</span></span><br/>           | <span data-ttu-id="a5984-129">Name der Katalog Datei, einschließlich der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="a5984-129">Name of the catalog file, including its extension.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a5984-130">Resultdir</span><span class="sxs-lookup"><span data-stu-id="a5984-130">ResultDir</span></span><br/>      | <span data-ttu-id="a5984-131">Verzeichnis, in dem die erstellte. cat-Datei platziert wird.</span><span class="sxs-lookup"><span data-stu-id="a5984-131">Directory where the created .cat file will be placed.</span></span> <span data-ttu-id="a5984-132">Wenn dies nicht angegeben ist, wird das aktuelle Standardverzeichnis verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5984-132">If not indicated, the default current directory is used.</span></span> <span data-ttu-id="a5984-133">Wenn das Verzeichnis nicht vorhanden ist, wird es erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5984-133">If the directory does not exist, it is created.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="a5984-134">Veröffentlichversion</span><span class="sxs-lookup"><span data-stu-id="a5984-134">PublicVersion</span></span><br/>  | <span data-ttu-id="a5984-135">Diese Option wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a5984-135">This option is not supported.</span></span> <br/> <span data-ttu-id="a5984-136">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Katalogversion.</span><span class="sxs-lookup"><span data-stu-id="a5984-136">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** Catalog version.</span></span> <span data-ttu-id="a5984-137">Wenn das Feld leer gelassen wird, wird der Standardwert 1 verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5984-137">If left blank, the default value, 1, is used.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a5984-138">CatalogVersion</span><span class="sxs-lookup"><span data-stu-id="a5984-138">CatalogVersion</span></span><br/> | <span data-ttu-id="a5984-139">Katalogversion.</span><span class="sxs-lookup"><span data-stu-id="a5984-139">Catalog version.</span></span> <span data-ttu-id="a5984-140">Wenn die Version nicht vorhanden ist oder auf 1 festgelegt ist, wird "0x100" an den *dwpublicversion* -Parameter der [**cryptgatopen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) -Funktion übergeben, und es wird eine Katalog Datei der Version 1 erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5984-140">If the version is not present or is set to 1, then "0x100" is passed to the *dwPublicVersion* parameter of the [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) function, and a version 1 catalog file is created.</span></span> <span data-ttu-id="a5984-141">Die hashalgorithms-Option muss leer sein oder SHA1 enthalten.</span><span class="sxs-lookup"><span data-stu-id="a5984-141">The HashAlgorithms option must be empty or contain SHA1.</span></span><br/> <span data-ttu-id="a5984-142">Wenn die Version auf 2 festgelegt ist, wird "0x200" an den *dwpublicversion* -Parameter der [**cryptgatopen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) -Funktion übergeben, und es wird eine Katalog Datei der Version 2 erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5984-142">If the version is set to 2, then "0x200" is passed to the *dwPublicVersion* parameter of the [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) function, and a version 2 catalog file is created.</span></span> <span data-ttu-id="a5984-143">Die hashalgorithms-Option muss SHA256 enthalten.</span><span class="sxs-lookup"><span data-stu-id="a5984-143">The HashAlgorithms option must contain SHA256.</span></span><br/> <span data-ttu-id="a5984-144">Wenn diese Option vorhanden ist, aber einen anderen Wert als 1 oder 2 enthält, führt das MakeCat-Tool zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="a5984-144">If this option is present but contains any value other than 1 or 2, the MakeCat tool will error out.</span></span><br/> <span data-ttu-id="a5984-145">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Diese Option wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a5984-145">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/> |
| <span data-ttu-id="a5984-146">Hashalgorithms</span><span class="sxs-lookup"><span data-stu-id="a5984-146">HashAlgorithms</span></span><br/> | <span data-ttu-id="a5984-147">Der Name des verwendeten Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="a5984-147">Name of the hashing algorithm used.</span></span> <span data-ttu-id="a5984-148">Weitere Informationen finden Sie unter der CatalogVersion-Option.</span><span class="sxs-lookup"><span data-stu-id="a5984-148">For more information, see the CatalogVersion option.</span></span><br/> <span data-ttu-id="a5984-149">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Diese Option wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a5984-149">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a5984-150">Einschleusen</span><span class="sxs-lookup"><span data-stu-id="a5984-150">PageHashes</span></span><br/>     | <span data-ttu-id="a5984-151">Gibt an, ob die Dateien, die in der <HASH> Option im \[ Abschnitt catalogfiles aufgeführt sind, mit Hash Hash \]</span><span class="sxs-lookup"><span data-stu-id="a5984-151">Specifies whether to hash the files listed in the <HASH> option in the \[CatalogFiles\] section</span></span><br/> <span data-ttu-id="a5984-152">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Diese Option wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a5984-152">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a5984-153">EncodingType</span><span class="sxs-lookup"><span data-stu-id="a5984-153">EncodingType</span></span><br/>   | <span data-ttu-id="a5984-154">Der Typ der verwendeten Nachrichten Codierung.</span><span class="sxs-lookup"><span data-stu-id="a5984-154">Type of message encoding used.</span></span> <span data-ttu-id="a5984-155">Wenn das Feld leer gelassen wird, ist der Standard Codierungstyp PKCS \_ 7 \_ ASN \_ Encoding \| X509 \_ ASN \_ Encoding, 0x00010001.</span><span class="sxs-lookup"><span data-stu-id="a5984-155">If left blank, the default EncodingType is PKCS\_7\_ASN\_ENCODING \| X509\_ASN\_ENCODING, 0x00010001.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="a5984-156">Der \[ Abschnitt catalogfiles \] definiert jeden Member der Katalog Datei mit Dateien verschiedener Typen und Attribute verschiedener Typen in separaten Gruppen.</span><span class="sxs-lookup"><span data-stu-id="a5984-156">The \[CatalogFiles\] section defines each member of the catalog file with files of various types and attributes of various types in separate groups.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5984-157">Option</span><span class="sxs-lookup"><span data-stu-id="a5984-157">Option</span></span></th>
<th><span data-ttu-id="a5984-158">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5984-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a5984-159">Verweistag</span><span class="sxs-lookup"><span data-stu-id="a5984-159">reference tag</span></span><br/></td>
<td><span data-ttu-id="a5984-160">Text Verweis auf die Datei.</span><span class="sxs-lookup"><span data-stu-id="a5984-160">Text reference to the file.</span></span> <span data-ttu-id="a5984-161">Dies kann beliebige ASCII-Textzeichen außer dem Gleichheitszeichen (=) enthalten.</span><span class="sxs-lookup"><span data-stu-id="a5984-161">This can include any ASCII text characters except the equal sign (=).</span></span> <span data-ttu-id="a5984-162">Das System muss dieses Tag nach der Installation reproduzieren können.</span><span class="sxs-lookup"><span data-stu-id="a5984-162">The system must be able to reproduce this tag after installation.</span></span> <br/> <span data-ttu-id="a5984-163">Verwenden Sie <HASH> als Präfix des Datei namens.</span><span class="sxs-lookup"><span data-stu-id="a5984-163">Use <HASH> as a prefix of the file name.</span></span> <span data-ttu-id="a5984-164">Dies führt dazu, dass das-Tag der Datei Hash in ASCII-Zeichen folgen Form ist.</span><span class="sxs-lookup"><span data-stu-id="a5984-164">This results in the tag being the file's hash in ASCII string form.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5984-165">Dateipfad und-Name</span><span class="sxs-lookup"><span data-stu-id="a5984-165">file path and name</span></span><br/></td>
<td><span data-ttu-id="a5984-166">Der Dateiname, einschließlich der zu erteilenden Erweiterung und des relativen Pfads zur Datei.</span><span class="sxs-lookup"><span data-stu-id="a5984-166">The file name, including the extension to be parsed and the relative path to the file.</span></span> <span data-ttu-id="a5984-167">Jeder Dateityp, der mit SignTool signiert werden kann, kann einem Katalog hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a5984-167">Any type of file that can be signed with SignTool can be added to a catalog.</span></span> <span data-ttu-id="a5984-168">Dateinamen mit den folgenden Erweiterungen können z. b. zu einem Katalog hinzugefügt werden:. exe,. cab,. cat,. ocx,. dll und. STL.</span><span class="sxs-lookup"><span data-stu-id="a5984-168">For example, file names with the following extensions, among others, can be added to a catalog: .exe, .cab, .cat, .ocx, .dll, and .stl.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a5984-169">Altsipid</span><span class="sxs-lookup"><span data-stu-id="a5984-169">ALTSIPID</span></span><br/></td>
<td><span data-ttu-id="a5984-170">SIP-GUID, die für Hashwerte anstelle des Standard-SIP basierend auf dem Dateityp verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5984-170">SIP GUID that is to be used for hashing instead of the standard SIP based on file type.</span></span> <span data-ttu-id="a5984-171">Dieser Eintrag ist optional.</span><span class="sxs-lookup"><span data-stu-id="a5984-171">This entry is optional.</span></span> <span data-ttu-id="a5984-172">Wenn dieser Eintrag weggelassen wird, wird der Member mithilfe des standardsip Hashwert.</span><span class="sxs-lookup"><span data-stu-id="a5984-172">If this entry is omitted, the member will be hashed using the default SIP.</span></span> <span data-ttu-id="a5984-173">Wenn kein installiertes Standard-SIP gefunden wird, wird der flatsip verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5984-173">If no default installed SIP is found, the Flat SIP will be used.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5984-174">guid</span><span class="sxs-lookup"><span data-stu-id="a5984-174">guid</span></span><br/></td>
<td><span data-ttu-id="a5984-175">Text Darstellung einer GUID.</span><span class="sxs-lookup"><span data-stu-id="a5984-175">Text representation of a GUID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a5984-176">Attrx</span><span class="sxs-lookup"><span data-stu-id="a5984-176">ATTRx</span></span><br/></td>
<td><span data-ttu-id="a5984-177">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a5984-177">Optional.</span></span> <span data-ttu-id="a5984-178">Attribut oder Anweisung über die Datei oder den Inhalt.</span><span class="sxs-lookup"><span data-stu-id="a5984-178">Attribute or statement about the file or content.</span></span> <span data-ttu-id="a5984-179">Es kann eine beliebige Anzahl von Attributen, einschließlich None, vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="a5984-179">There can be any number of attributes, including none.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5984-180">type</span><span class="sxs-lookup"><span data-stu-id="a5984-180">type</span></span><br/></td>
<td><span data-ttu-id="a5984-181">Definiert, welcher Attributtyp im Format 0x00000000 (Text) hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a5984-181">Defines what type of attribute is being added in the format 0x00000000 (text).</span></span> <span data-ttu-id="a5984-182">Diese Option kann eine bitweise<strong>or</strong> -Kombination von 0 (null) oder mehreren der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="a5984-182">This option can be a bitwise-<strong>OR</strong> combination of zero or more of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="a5984-183">0x10000000 Authenticated-Attribut (signiert, in den Hash eingeschlossen).</span><span class="sxs-lookup"><span data-stu-id="a5984-183">0x10000000 Authenticated attribute (signed, included in the hash).</span></span></li>
<li><span data-ttu-id="a5984-184">0x20000000 nicht authentifiziertes Attribut (ohne Vorzeichen, nicht in den Hash eingeschlossen, nicht überprüfbar).</span><span class="sxs-lookup"><span data-stu-id="a5984-184">0x20000000 Unauthenticated attribute (unsigned, not included in the hash, not verifiable).</span></span></li>
<li><span data-ttu-id="a5984-185">Das 0x01000000-Attribut wird nicht in SHA1-Einträge in einem CatalogVersion 2-Katalog repliziert.</span><span class="sxs-lookup"><span data-stu-id="a5984-185">0x01000000 Attribute will not be replicated to SHA1 entries in a CatalogVersion 2 catalog.</span></span></li>
<li><span data-ttu-id="a5984-186">Das 0x00010000 bis-Attribut wird als Klartext dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a5984-186">0x00010000 Attribute is represented in plaintext.</span></span> <span data-ttu-id="a5984-187">Es wird keine Konvertierung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5984-187">No conversion will be done.</span></span></li>
<li><span data-ttu-id="a5984-188">Das 0x00020000-Attribut wird in der Base-64-Codierung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a5984-188">0x00020000 Attribute is represented in base-64 encoding.</span></span> <span data-ttu-id="a5984-189">Diese wird verwendet, um Binärdaten darzustellen.</span><span class="sxs-lookup"><span data-stu-id="a5984-189">This is used to represent binary data.</span></span></li>
<li><span data-ttu-id="a5984-190">Das 0x00000001-Attribut ist ein Name-Wert-Paar.</span><span class="sxs-lookup"><span data-stu-id="a5984-190">0x00000001 Attribute is a name-value pair.</span></span> <span data-ttu-id="a5984-191">Verwenden Sie die OID-Option für den Namen.</span><span class="sxs-lookup"><span data-stu-id="a5984-191">Use the oid option for the name.</span></span> <span data-ttu-id="a5984-192">Dieses Attribut ist langsam. Verwenden Sie daher diese Option sparsam.</span><span class="sxs-lookup"><span data-stu-id="a5984-192">This attribute is slow; therefore, use this option sparingly.</span></span></li>
<li><span data-ttu-id="a5984-193">auf das 0x00000002-Attribut wird von einem <a href="/windows/desktop/SecGloss/o-gly"><em>Objekt Bezeichner</em></a> (OID) verwiesen.</span><span class="sxs-lookup"><span data-stu-id="a5984-193">0x00000002 Attribute is referenced by an <a href="/windows/desktop/SecGloss/o-gly"><em>object identifier</em></a> (OID).</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a5984-194">oid</span><span class="sxs-lookup"><span data-stu-id="a5984-194">oid</span></span><br/></td>
<td><span data-ttu-id="a5984-195">Die Textdarstellung des Verweis Schlüssels des Attributs.</span><span class="sxs-lookup"><span data-stu-id="a5984-195">The text representation of the attribute's reference key.</span></span> <span data-ttu-id="a5984-196">Dies ist eine OID in Form einer Text Zeichenfolge in gepunkteter Quad-Notation (z. b. a. b. c. d) oder eines textnamens.</span><span class="sxs-lookup"><span data-stu-id="a5984-196">It is an OID in the form of a text string in dotted quad notation (for example, a.b.c.d) or a text Name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5984-197">value</span><span class="sxs-lookup"><span data-stu-id="a5984-197">value</span></span><br/></td>
<td><span data-ttu-id="a5984-198">Die Textdarstellung des Werts des Attributs.</span><span class="sxs-lookup"><span data-stu-id="a5984-198">The text representation of the value of the attribute.</span></span> <span data-ttu-id="a5984-199">Der Typ der verwendeten Textdarstellung hängt vom Wert der Type-Option ab.</span><span class="sxs-lookup"><span data-stu-id="a5984-199">The type of text representation used depends on the value of the type option.</span></span> <span data-ttu-id="a5984-200">Die EOL-Zeichen bestimmen die Länge.</span><span class="sxs-lookup"><span data-stu-id="a5984-200">The EOL characters determine the length.</span></span><br/></td>
</tr>
<tr class="odd">
<td><HASH><br/></td>
<td><span data-ttu-id="a5984-201">Hashes der angegebenen Datei.</span><span class="sxs-lookup"><span data-stu-id="a5984-201">Hashes the specified file.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a5984-202">Die generierte Katalog Datei ist nicht signiert.</span><span class="sxs-lookup"><span data-stu-id="a5984-202">The generated catalog file is unsigned.</span></span> <span data-ttu-id="a5984-203">Wenn Sie vor der Übertragung signiert werden soll, wird Sie mithilfe von [SignTool](signtool.md)signiert.</span><span class="sxs-lookup"><span data-stu-id="a5984-203">If it is to be signed prior to transmittal, it is signed by using [SignTool](signtool.md).</span></span>

 

 
