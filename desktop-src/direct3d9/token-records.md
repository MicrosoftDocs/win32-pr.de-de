---
description: In diesem Abschnitt wird das Format der Datensätze für die einzelnen Datensatz-Token-Token beschrieben. Die Informationen sind in die folgenden Abschnitte unterteilt.
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: Tokendatensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae7e1dcdd36d538ed44205fa51b8e2094d1ff14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344800"
---
# <a name="token-records"></a><span data-ttu-id="1bc08-104">Tokendatensätze</span><span class="sxs-lookup"><span data-stu-id="1bc08-104">Token Records</span></span>

<span data-ttu-id="1bc08-105">In diesem Abschnitt wird das Format der Datensätze für die einzelnen Datensatz-Token-Token beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1bc08-105">This section describes the format of the records for each of the record-bearing tokens.</span></span> <span data-ttu-id="1bc08-106">Die Informationen sind in die folgenden Abschnitte unterteilt.</span><span class="sxs-lookup"><span data-stu-id="1bc08-106">Information is divided into the following sections.</span></span>

-   [<span data-ttu-id="1bc08-107">\_Tokenname</span><span class="sxs-lookup"><span data-stu-id="1bc08-107">TOKEN\_NAME</span></span>](/windows)
-   [<span data-ttu-id="1bc08-108">Token- \_ Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1bc08-108">TOKEN\_STRING</span></span>](/windows)
-   [<span data-ttu-id="1bc08-109">Token- \_ Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="1bc08-109">TOKEN\_INTEGER</span></span>](/windows)
-   [<span data-ttu-id="1bc08-110">\_tokenguid</span><span class="sxs-lookup"><span data-stu-id="1bc08-110">TOKEN\_GUID</span></span>](/windows)
-   [<span data-ttu-id="1bc08-111">\_Liste der tokeninteger \_</span><span class="sxs-lookup"><span data-stu-id="1bc08-111">TOKEN\_INTEGER\_LIST</span></span>](/windows)
-   [<span data-ttu-id="1bc08-112">Liste der Token- \_ float \_</span><span class="sxs-lookup"><span data-stu-id="1bc08-112">TOKEN\_FLOAT\_LIST</span></span>](/windows)

## <a name="token_name"></a><span data-ttu-id="1bc08-113">\_Tokenname</span><span class="sxs-lookup"><span data-stu-id="1bc08-113">TOKEN\_NAME</span></span>

<span data-ttu-id="1bc08-114">Ein Datensatz variabler Länge.</span><span class="sxs-lookup"><span data-stu-id="1bc08-114">A variable-length record.</span></span> <span data-ttu-id="1bc08-115">Auf das Token folgt ein count-Wert, der die Anzahl von Bytes angibt, die im Feld Name befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="1bc08-115">The token is followed by a count value that specifies the number of bytes that follow in the name field.</span></span> <span data-ttu-id="1bc08-116">Ein ASCII-Name der Längen Anzahl schließt den Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="1bc08-116">An ASCII name of length count completes the record.</span></span>



| <span data-ttu-id="1bc08-117">Feld</span><span class="sxs-lookup"><span data-stu-id="1bc08-117">Field</span></span> | <span data-ttu-id="1bc08-118">type</span><span class="sxs-lookup"><span data-stu-id="1bc08-118">Type</span></span>       | <span data-ttu-id="1bc08-119">Größe (Byte)</span><span class="sxs-lookup"><span data-stu-id="1bc08-119">Size (bytes)</span></span> | <span data-ttu-id="1bc08-120">Inhalte</span><span class="sxs-lookup"><span data-stu-id="1bc08-120">Contents</span></span>                       |
|-------|------------|--------------|--------------------------------|
| <span data-ttu-id="1bc08-121">token</span><span class="sxs-lookup"><span data-stu-id="1bc08-121">token</span></span> | <span data-ttu-id="1bc08-122">WORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-122">WORD</span></span>       | <span data-ttu-id="1bc08-123">2</span><span class="sxs-lookup"><span data-stu-id="1bc08-123">2</span></span>            | <span data-ttu-id="1bc08-124">\_Tokenname</span><span class="sxs-lookup"><span data-stu-id="1bc08-124">token\_name</span></span>                    |
| <span data-ttu-id="1bc08-125">count</span><span class="sxs-lookup"><span data-stu-id="1bc08-125">count</span></span> | <span data-ttu-id="1bc08-126">DWORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-126">DWORD</span></span>      | <span data-ttu-id="1bc08-127">4</span><span class="sxs-lookup"><span data-stu-id="1bc08-127">4</span></span>            | <span data-ttu-id="1bc08-128">Länge des Namens Felds in Bytes</span><span class="sxs-lookup"><span data-stu-id="1bc08-128">Length of name field, in bytes</span></span> |
| <span data-ttu-id="1bc08-129">name</span><span class="sxs-lookup"><span data-stu-id="1bc08-129">name</span></span>  | <span data-ttu-id="1bc08-130">Bytearray</span><span class="sxs-lookup"><span data-stu-id="1bc08-130">BYTE array</span></span> | <span data-ttu-id="1bc08-131">count</span><span class="sxs-lookup"><span data-stu-id="1bc08-131">count</span></span>        | <span data-ttu-id="1bc08-132">ASCII-Name</span><span class="sxs-lookup"><span data-stu-id="1bc08-132">ASCII name</span></span>                     |



 

## <a name="token_string"></a><span data-ttu-id="1bc08-133">Token- \_ Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1bc08-133">TOKEN\_STRING</span></span>

<span data-ttu-id="1bc08-134">Ein Datensatz variabler Länge.</span><span class="sxs-lookup"><span data-stu-id="1bc08-134">A variable-length record.</span></span> <span data-ttu-id="1bc08-135">Auf das Token folgt ein count-Wert, der die Anzahl der Bytes angibt, die im Feld "Zeichenfolge" befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="1bc08-135">The token is followed by a count value that specifies the number of bytes that follow in the string field.</span></span> <span data-ttu-id="1bc08-136">Eine ASCII-Zeichenfolge der Längen Anzahl setzt den Datensatz fort, der durch ein abschließendes Token abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="1bc08-136">An ASCII string of length count continues the record, which is completed by a terminating token.</span></span> <span data-ttu-id="1bc08-137">Die Auswahl des Abschluss Zeichens wird durch Syntax Probleme bestimmt, die an anderer Stelle erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="1bc08-137">The choice of terminator is determined by syntax issues discussed elsewhere.</span></span>



| <span data-ttu-id="1bc08-138">Feld</span><span class="sxs-lookup"><span data-stu-id="1bc08-138">Field</span></span>      | <span data-ttu-id="1bc08-139">type</span><span class="sxs-lookup"><span data-stu-id="1bc08-139">Type</span></span>       | <span data-ttu-id="1bc08-140">Größe (Byte)</span><span class="sxs-lookup"><span data-stu-id="1bc08-140">Size (bytes)</span></span> | <span data-ttu-id="1bc08-141">Inhalte</span><span class="sxs-lookup"><span data-stu-id="1bc08-141">Contents</span></span>                         |
|------------|------------|--------------|----------------------------------|
| <span data-ttu-id="1bc08-142">token</span><span class="sxs-lookup"><span data-stu-id="1bc08-142">token</span></span>      | <span data-ttu-id="1bc08-143">WORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-143">WORD</span></span>       | <span data-ttu-id="1bc08-144">2</span><span class="sxs-lookup"><span data-stu-id="1bc08-144">2</span></span>            | <span data-ttu-id="1bc08-145">Token- \_ Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1bc08-145">token\_string</span></span>                    |
| <span data-ttu-id="1bc08-146">count</span><span class="sxs-lookup"><span data-stu-id="1bc08-146">count</span></span>      | <span data-ttu-id="1bc08-147">DWORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-147">DWORD</span></span>      | <span data-ttu-id="1bc08-148">4</span><span class="sxs-lookup"><span data-stu-id="1bc08-148">4</span></span>            | <span data-ttu-id="1bc08-149">Länge des Zeichen folgen Felds in Bytes</span><span class="sxs-lookup"><span data-stu-id="1bc08-149">Length of string field in bytes</span></span>  |
| <span data-ttu-id="1bc08-150">Schnür</span><span class="sxs-lookup"><span data-stu-id="1bc08-150">strinG</span></span>     | <span data-ttu-id="1bc08-151">Bytearray</span><span class="sxs-lookup"><span data-stu-id="1bc08-151">BYTE array</span></span> | <span data-ttu-id="1bc08-152">count</span><span class="sxs-lookup"><span data-stu-id="1bc08-152">count</span></span>        | <span data-ttu-id="1bc08-153">ASCII-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1bc08-153">ASCII string</span></span>                     |
| <span data-ttu-id="1bc08-154">chter</span><span class="sxs-lookup"><span data-stu-id="1bc08-154">terminator</span></span> | <span data-ttu-id="1bc08-155">DWORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-155">DWORD</span></span>      | <span data-ttu-id="1bc08-156">4</span><span class="sxs-lookup"><span data-stu-id="1bc08-156">4</span></span>            | <span data-ttu-id="1bc08-157">\_tokensemikolon oder \_ tokenkomma</span><span class="sxs-lookup"><span data-stu-id="1bc08-157">tOKEN\_SEMICOLON or TOKEN\_COMMA</span></span> |



 

## <a name="token_integer"></a><span data-ttu-id="1bc08-158">Token- \_ Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="1bc08-158">TOKEN\_INTEGER</span></span>

<span data-ttu-id="1bc08-159">Ein Datensatz mit fester Länge.</span><span class="sxs-lookup"><span data-stu-id="1bc08-159">A fixed length record.</span></span> <span data-ttu-id="1bc08-160">Auf das Token folgt der ganzzahlige Wert.</span><span class="sxs-lookup"><span data-stu-id="1bc08-160">The token is followed by the integer value required.</span></span>



| <span data-ttu-id="1bc08-161">Feld</span><span class="sxs-lookup"><span data-stu-id="1bc08-161">Field</span></span> | <span data-ttu-id="1bc08-162">type</span><span class="sxs-lookup"><span data-stu-id="1bc08-162">Type</span></span>  | <span data-ttu-id="1bc08-163">Größe (Byte)</span><span class="sxs-lookup"><span data-stu-id="1bc08-163">Size (bytes)</span></span> | <span data-ttu-id="1bc08-164">Inhalte</span><span class="sxs-lookup"><span data-stu-id="1bc08-164">Contents</span></span>       |
|-------|-------|--------------|----------------|
| <span data-ttu-id="1bc08-165">token</span><span class="sxs-lookup"><span data-stu-id="1bc08-165">token</span></span> | <span data-ttu-id="1bc08-166">WORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-166">WORD</span></span>  | <span data-ttu-id="1bc08-167">2</span><span class="sxs-lookup"><span data-stu-id="1bc08-167">2</span></span>            | <span data-ttu-id="1bc08-168">tOKEN- \_ Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="1bc08-168">tOKEN\_INTEGER</span></span> |
| <span data-ttu-id="1bc08-169">Wert</span><span class="sxs-lookup"><span data-stu-id="1bc08-169">valuE</span></span> | <span data-ttu-id="1bc08-170">DWORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-170">DWORD</span></span> | <span data-ttu-id="1bc08-171">4</span><span class="sxs-lookup"><span data-stu-id="1bc08-171">4</span></span>            | <span data-ttu-id="1bc08-172">Einzelne Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="1bc08-172">Single integer</span></span> |



 

## <a name="token_guid"></a><span data-ttu-id="1bc08-173">\_tokenguid</span><span class="sxs-lookup"><span data-stu-id="1bc08-173">TOKEN\_GUID</span></span>

<span data-ttu-id="1bc08-174">Ein Datensatz mit fester Länge.</span><span class="sxs-lookup"><span data-stu-id="1bc08-174">A fixed-length record.</span></span> <span data-ttu-id="1bc08-175">Auf das Token folgen die vier Datenfelder, die vom OSF-DCE-Standard definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1bc08-175">The token is followed by the four data fields as defined by the OSF DCE standard.</span></span>



| <span data-ttu-id="1bc08-176">Feld</span><span class="sxs-lookup"><span data-stu-id="1bc08-176">Field</span></span> | <span data-ttu-id="1bc08-177">type</span><span class="sxs-lookup"><span data-stu-id="1bc08-177">Type</span></span>       | <span data-ttu-id="1bc08-178">Größe (Byte)</span><span class="sxs-lookup"><span data-stu-id="1bc08-178">Size (bytes)</span></span> | <span data-ttu-id="1bc08-179">Inhalte</span><span class="sxs-lookup"><span data-stu-id="1bc08-179">Contents</span></span>          |
|-------|------------|--------------|-------------------|
| <span data-ttu-id="1bc08-180">token</span><span class="sxs-lookup"><span data-stu-id="1bc08-180">token</span></span> | <span data-ttu-id="1bc08-181">WORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-181">WORD</span></span>       | <span data-ttu-id="1bc08-182">2</span><span class="sxs-lookup"><span data-stu-id="1bc08-182">2</span></span>            | <span data-ttu-id="1bc08-183">\_tokenguid</span><span class="sxs-lookup"><span data-stu-id="1bc08-183">tOKEN\_GUID</span></span>       |
| <span data-ttu-id="1bc08-184">Data1</span><span class="sxs-lookup"><span data-stu-id="1bc08-184">Data1</span></span> | <span data-ttu-id="1bc08-185">DWORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-185">DWORD</span></span>      | <span data-ttu-id="1bc08-186">4</span><span class="sxs-lookup"><span data-stu-id="1bc08-186">4</span></span>            | <span data-ttu-id="1bc08-187">UUID-Datenfeld 1</span><span class="sxs-lookup"><span data-stu-id="1bc08-187">UUID data field 1</span></span> |
| <span data-ttu-id="1bc08-188">Data2</span><span class="sxs-lookup"><span data-stu-id="1bc08-188">Data2</span></span> | <span data-ttu-id="1bc08-189">WORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-189">WORD</span></span>       | <span data-ttu-id="1bc08-190">2</span><span class="sxs-lookup"><span data-stu-id="1bc08-190">2</span></span>            | <span data-ttu-id="1bc08-191">UUID-Datenfeld 2</span><span class="sxs-lookup"><span data-stu-id="1bc08-191">UUID data field 2</span></span> |
| <span data-ttu-id="1bc08-192">Data3</span><span class="sxs-lookup"><span data-stu-id="1bc08-192">Data3</span></span> | <span data-ttu-id="1bc08-193">WORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-193">WORD</span></span>       | <span data-ttu-id="1bc08-194">2</span><span class="sxs-lookup"><span data-stu-id="1bc08-194">2</span></span>            | <span data-ttu-id="1bc08-195">UUID-Datenfeld 3</span><span class="sxs-lookup"><span data-stu-id="1bc08-195">UUID data field 3</span></span> |
| <span data-ttu-id="1bc08-196">Data4</span><span class="sxs-lookup"><span data-stu-id="1bc08-196">Data4</span></span> | <span data-ttu-id="1bc08-197">Bytearray</span><span class="sxs-lookup"><span data-stu-id="1bc08-197">BYTE array</span></span> | <span data-ttu-id="1bc08-198">8</span><span class="sxs-lookup"><span data-stu-id="1bc08-198">8</span></span>            | <span data-ttu-id="1bc08-199">UUID-Datenfeld 4</span><span class="sxs-lookup"><span data-stu-id="1bc08-199">UUID data field 4</span></span> |



 

## <a name="token_integer_list"></a><span data-ttu-id="1bc08-200">\_Liste der tokeninteger \_</span><span class="sxs-lookup"><span data-stu-id="1bc08-200">TOKEN\_INTEGER\_LIST</span></span>

<span data-ttu-id="1bc08-201">Ein Datensatz variabler Länge.</span><span class="sxs-lookup"><span data-stu-id="1bc08-201">A variable-length record.</span></span> <span data-ttu-id="1bc08-202">Auf das Token folgt ein count-Wert, der die Anzahl von ganzen Zahlen angibt, die im Listenfeld befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="1bc08-202">The token is followed by a count value that specifies the number of integers that follow in the list field.</span></span> <span data-ttu-id="1bc08-203">Aus Effizienzgründen sollten aufeinanderfolgende ganzzahlige Listen in einer einzigen Liste zusammengefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1bc08-203">For efficiency, consecutive integer lists should be compounded into a single list.</span></span>



| <span data-ttu-id="1bc08-204">Feld</span><span class="sxs-lookup"><span data-stu-id="1bc08-204">Field</span></span> | <span data-ttu-id="1bc08-205">type</span><span class="sxs-lookup"><span data-stu-id="1bc08-205">Type</span></span>  | <span data-ttu-id="1bc08-206">Größe (Byte)</span><span class="sxs-lookup"><span data-stu-id="1bc08-206">Size (bytes)</span></span> | <span data-ttu-id="1bc08-207">Inhalte</span><span class="sxs-lookup"><span data-stu-id="1bc08-207">Contents</span></span>                         |
|-------|-------|--------------|----------------------------------|
| <span data-ttu-id="1bc08-208">token</span><span class="sxs-lookup"><span data-stu-id="1bc08-208">token</span></span> | <span data-ttu-id="1bc08-209">WORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-209">WORD</span></span>  | <span data-ttu-id="1bc08-210">2</span><span class="sxs-lookup"><span data-stu-id="1bc08-210">2</span></span>            | <span data-ttu-id="1bc08-211">\_Liste der tokeninteger \_</span><span class="sxs-lookup"><span data-stu-id="1bc08-211">tOKEN\_INTEGER\_LISt</span></span>             |
| <span data-ttu-id="1bc08-212">count</span><span class="sxs-lookup"><span data-stu-id="1bc08-212">count</span></span> | <span data-ttu-id="1bc08-213">DWORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-213">DWORD</span></span> | <span data-ttu-id="1bc08-214">4</span><span class="sxs-lookup"><span data-stu-id="1bc08-214">4</span></span>            | <span data-ttu-id="1bc08-215">Anzahl von ganzen Zahlen im Listenfeld</span><span class="sxs-lookup"><span data-stu-id="1bc08-215">Number of integers in list field</span></span> |
| <span data-ttu-id="1bc08-216">list</span><span class="sxs-lookup"><span data-stu-id="1bc08-216">list</span></span>  | <span data-ttu-id="1bc08-217">DWORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-217">DWORD</span></span> | <span data-ttu-id="1bc08-218">4 x-Anzahl</span><span class="sxs-lookup"><span data-stu-id="1bc08-218">4 x count</span></span>    | <span data-ttu-id="1bc08-219">Ganzzahlige Liste</span><span class="sxs-lookup"><span data-stu-id="1bc08-219">Integer list</span></span>                     |



 

## <a name="token_float_list"></a><span data-ttu-id="1bc08-220">Liste der Token- \_ float \_</span><span class="sxs-lookup"><span data-stu-id="1bc08-220">TOKEN\_FLOAT\_LIST</span></span>

<span data-ttu-id="1bc08-221">Ein Datensatz variabler Länge.</span><span class="sxs-lookup"><span data-stu-id="1bc08-221">A variable-length record.</span></span> <span data-ttu-id="1bc08-222">Auf das Token folgt ein count-Wert, der die Anzahl der Gleit Komma Zahlen oder Double-Werte angibt, die im Listenfeld nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="1bc08-222">The token is followed by a count value that specifies the number of floats or doubles that follow in the list field.</span></span> <span data-ttu-id="1bc08-223">Die Größe des Gleit Komma Werts (float oder Double) wird durch den Wert von float sizespecified im Dateiheader bestimmt.</span><span class="sxs-lookup"><span data-stu-id="1bc08-223">The size of the floating point value (float or double) is determined by the value of float sizespecified in the file header.</span></span> <span data-ttu-id="1bc08-224">Aus Effizienzgründen sollten aufeinander folgende tokenzugriffslisten \_ \_ in einer einzigen Liste zusammengefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1bc08-224">For efficiency, consecutive TOKEN\_FLOAT\_LISTs should be compounded into a single list.</span></span>



| <span data-ttu-id="1bc08-225">Feld</span><span class="sxs-lookup"><span data-stu-id="1bc08-225">Field</span></span> | <span data-ttu-id="1bc08-226">type</span><span class="sxs-lookup"><span data-stu-id="1bc08-226">Type</span></span>               | <span data-ttu-id="1bc08-227">Größe (Byte)</span><span class="sxs-lookup"><span data-stu-id="1bc08-227">Size (bytes)</span></span>   | <span data-ttu-id="1bc08-228">Inhalte</span><span class="sxs-lookup"><span data-stu-id="1bc08-228">Contents</span></span>                                  |
|-------|--------------------|----------------|-------------------------------------------|
| <span data-ttu-id="1bc08-229">token</span><span class="sxs-lookup"><span data-stu-id="1bc08-229">token</span></span> | <span data-ttu-id="1bc08-230">WORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-230">WORD</span></span>               | <span data-ttu-id="1bc08-231">2</span><span class="sxs-lookup"><span data-stu-id="1bc08-231">2</span></span>              | <span data-ttu-id="1bc08-232">Liste der tOKEN- \_ float \_</span><span class="sxs-lookup"><span data-stu-id="1bc08-232">tOKEN\_FLOAT\_LISt</span></span>                        |
| <span data-ttu-id="1bc08-233">count</span><span class="sxs-lookup"><span data-stu-id="1bc08-233">count</span></span> | <span data-ttu-id="1bc08-234">DWORD</span><span class="sxs-lookup"><span data-stu-id="1bc08-234">DWORD</span></span>              | <span data-ttu-id="1bc08-235">4</span><span class="sxs-lookup"><span data-stu-id="1bc08-235">4</span></span>              | <span data-ttu-id="1bc08-236">Anzahl von Gleit Komma-oder Double-Werte im Listenfeld</span><span class="sxs-lookup"><span data-stu-id="1bc08-236">Number of floats or doubles in list field</span></span> |
| <span data-ttu-id="1bc08-237">list</span><span class="sxs-lookup"><span data-stu-id="1bc08-237">list</span></span>  | <span data-ttu-id="1bc08-238">float/double-Array</span><span class="sxs-lookup"><span data-stu-id="1bc08-238">float/double array</span></span> | <span data-ttu-id="1bc08-239">4 oder 8 x Anzahl</span><span class="sxs-lookup"><span data-stu-id="1bc08-239">4 or 8 x count</span></span> | <span data-ttu-id="1bc08-240">Float-oder Double-Liste</span><span class="sxs-lookup"><span data-stu-id="1bc08-240">Float or double list</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="1bc08-241">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1bc08-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bc08-242">Binärcodierung</span><span class="sxs-lookup"><span data-stu-id="1bc08-242">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 
