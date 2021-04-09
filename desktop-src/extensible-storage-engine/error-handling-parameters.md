---
description: 'Weitere Informationen: Fehler Behandlungsparameter'
title: Fehler Behandlungsparameter
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb225d7dbb67655286635320352060bcf2cb8a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868735"
---
# <a name="error-handling-parameters"></a><span data-ttu-id="6440e-103">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="6440e-103">Error Handling Parameters</span></span>


<span data-ttu-id="6440e-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6440e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="error-handling-parameters"></a><span data-ttu-id="6440e-105">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="6440e-105">Error Handling Parameters</span></span>

<span data-ttu-id="6440e-106">Dieses Thema enthält Parameter, die für die Fehlerbehandlung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6440e-106">This topic contains parameters that are used for error handling.</span></span>

<span data-ttu-id="6440e-107">*JET_paramErrorToString* 70</span><span class="sxs-lookup"><span data-stu-id="6440e-107">*JET_paramErrorToString* 70</span></span>  

<span data-ttu-id="6440e-108">Dieser Parameter kann verwendet werden, um eine [JET_ERR](./jet-err.md) in eine Zeichenfolge zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="6440e-108">This parameter can be used to convert a [JET_ERR](./jet-err.md) into a string.</span></span> <span data-ttu-id="6440e-109">Dies erfolgt mithilfe eines speziellen Aufrufens von [jetgetsystemparameter](./jetgetsystemparameter-function.md) , bei dem der ganzzahlige Ausgabepuffer den zu konvertierenden [JET_ERR](./jet-err.md) Wert enthält (als Eingabeparameter), und der Zeichen folgen-Ausgabepuffer die übereinstimmende Fehler Zeichenfolge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6440e-109">This is done using a special call to [JetGetSystemParameter](./jetgetsystemparameter-function.md) where the integer output buffer contains the [JET_ERR](./jet-err.md) value to be converted (as an input parameter) and the string output buffer returns the matching error string.</span></span> <span data-ttu-id="6440e-110">Die Zeichenfolge sieht in etwa wie folgt aus: "JET_errSuccess, erfolgreicher Vorgang".</span><span class="sxs-lookup"><span data-stu-id="6440e-110">The string will look something like this: "JET_errSuccess,Successful Operation".</span></span> <span data-ttu-id="6440e-111">Die Zeichenfolge besteht aus dem symbolischen Namen für die Zeichenfolge, einem Komma und einer einfachen Textbeschreibung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="6440e-111">The string is composed of the symbolic name for the string, then a comma, and then a simple text description of the error.</span></span> <span data-ttu-id="6440e-112">Die Beschreibungs Zeichenfolge kann selbst Kommas enthalten.</span><span class="sxs-lookup"><span data-stu-id="6440e-112">The description string may itself contain commas.</span></span> <span data-ttu-id="6440e-113">Wenn der Fehler nicht erkannt wird, lautet die Zeichenfolge "Unbekannter Fehler, unbekannter Fehler".</span><span class="sxs-lookup"><span data-stu-id="6440e-113">If the error is not recognized then the string will be "Unknown Error,Unknown Error".</span></span>

<span data-ttu-id="6440e-114">**Hinweis**  Dieser Parameter ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6440e-114">**Note**  This parameter is read only.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6440e-115">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="6440e-115">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="6440e-116">Sonderfunktionen</span><span class="sxs-lookup"><span data-stu-id="6440e-116">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6440e-117">Typ:</span><span class="sxs-lookup"><span data-stu-id="6440e-117">Type:</span></span></p></td>
<td><p><span data-ttu-id="6440e-118">Sonderfunktionen</span><span class="sxs-lookup"><span data-stu-id="6440e-118">Special</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6440e-119">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="6440e-119">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="6440e-120">Sonderfunktionen</span><span class="sxs-lookup"><span data-stu-id="6440e-120">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6440e-121">Umfang:</span><span class="sxs-lookup"><span data-stu-id="6440e-121">Scope:</span></span></p></td>
<td><p><span data-ttu-id="6440e-122">Global</span><span class="sxs-lookup"><span data-stu-id="6440e-122">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6440e-123">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="6440e-123">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="6440e-124">Nein</span><span class="sxs-lookup"><span data-stu-id="6440e-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6440e-125">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="6440e-125">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="6440e-126">Nein</span><span class="sxs-lookup"><span data-stu-id="6440e-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6440e-127">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="6440e-127">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="6440e-128">Nein</span><span class="sxs-lookup"><span data-stu-id="6440e-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6440e-129">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="6440e-129">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="6440e-130">Nein</span><span class="sxs-lookup"><span data-stu-id="6440e-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6440e-131">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="6440e-131">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="6440e-132">Nein</span><span class="sxs-lookup"><span data-stu-id="6440e-132">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6440e-133">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="6440e-133">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="6440e-134">Nein</span><span class="sxs-lookup"><span data-stu-id="6440e-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6440e-135">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="6440e-135">Availability:</span></span></p></td>
<td><p><span data-ttu-id="6440e-136">Alle</span><span class="sxs-lookup"><span data-stu-id="6440e-136">All</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6440e-137">*JET_paramExceptionAction*</span><span class="sxs-lookup"><span data-stu-id="6440e-137">*JET_paramExceptionAction*</span></span>  
<span data-ttu-id="6440e-138">98</span><span class="sxs-lookup"><span data-stu-id="6440e-138">98</span></span>  

<span data-ttu-id="6440e-139">Dieser Parameter steuert, was geschieht, wenn eine Ausnahme von der Datenbank-Engine oder vom Code ausgelöst wird, der von der Datenbank-Engine aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6440e-139">This parameter controls what happens when an exception is thrown by the database engine or code that is called by the database engine.</span></span> <span data-ttu-id="6440e-140">Wenn JET_ExceptionMsgBox festgelegt ist, wird eine Ausnahme für den Filter für nicht behandelte Windows-Ausnahmen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6440e-140">When set to JET_ExceptionMsgBox, any exception will be thrown to the Windows unhandled exception filter.</span></span> <span data-ttu-id="6440e-141">Dies führt dazu, dass die Ausnahme als Anwendungsfehler behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="6440e-141">This will result in the exception being handled as an application failure.</span></span> <span data-ttu-id="6440e-142">Der Zweck besteht darin, dass der Anwendungscode fälschlicherweise versucht, eine Ausnahme abzufangen und zu ignorieren, die von der Datenbank-Engine generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6440e-142">The intent is to prevent application code from erroneously trying to catch and ignore an exception generated by the database engine.</span></span> <span data-ttu-id="6440e-143">Dies ist nicht zulässig, da eine Daten Bank Beschädigung auftreten könnte.</span><span class="sxs-lookup"><span data-stu-id="6440e-143">This cannot be allowed because database corruption could occur.</span></span> <span data-ttu-id="6440e-144">Wenn die Anwendung diese Ausnahmen ordnungsgemäß verarbeiten möchte, kann der Schutz deaktiviert werden, indem dieser Parameter auf JET_ExceptionNone festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="6440e-144">If the application wishes to properly handle these exceptions then the protection can be disabled by setting this parameter to JET_ExceptionNone.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6440e-145">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="6440e-145">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="6440e-146">JET_ExceptionMsgBox</span><span class="sxs-lookup"><span data-stu-id="6440e-146">JET_ExceptionMsgBox</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6440e-147">Typ:</span><span class="sxs-lookup"><span data-stu-id="6440e-147">Type:</span></span></p></td>
<td><p><span data-ttu-id="6440e-148">Integer</span><span class="sxs-lookup"><span data-stu-id="6440e-148">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6440e-149">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="6440e-149">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="6440e-150">JET_ExceptionMsgBox JET_ExceptionNone</span><span class="sxs-lookup"><span data-stu-id="6440e-150">JET_ExceptionMsgBox, JET_ExceptionNone</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6440e-151">Umfang:</span><span class="sxs-lookup"><span data-stu-id="6440e-151">Scope:</span></span></p></td>
<td><p><span data-ttu-id="6440e-152">Global</span><span class="sxs-lookup"><span data-stu-id="6440e-152">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6440e-153">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="6440e-153">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="6440e-154"><strong>Windows 2000, Windows XP und Windows Server 2003:  </strong>  Nein</span><span class="sxs-lookup"><span data-stu-id="6440e-154"><strong>Windows 2000, Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="6440e-155"><strong>Windows Vista:</strong>  Zwar</span><span class="sxs-lookup"><span data-stu-id="6440e-155"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6440e-156">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="6440e-156">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="6440e-157"><strong>Windows 2000, Windows XP und Windows Server 2003:  </strong>  Nein</span><span class="sxs-lookup"><span data-stu-id="6440e-157"><strong>Windows 2000, Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="6440e-158"><strong>Windows Vista:</strong>  Zwar</span><span class="sxs-lookup"><span data-stu-id="6440e-158"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6440e-159">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="6440e-159">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="6440e-160">Nein</span><span class="sxs-lookup"><span data-stu-id="6440e-160">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6440e-161">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="6440e-161">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="6440e-162">Ja</span><span class="sxs-lookup"><span data-stu-id="6440e-162">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6440e-163">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="6440e-163">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="6440e-164">Nein</span><span class="sxs-lookup"><span data-stu-id="6440e-164">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6440e-165">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="6440e-165">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="6440e-166">Nein</span><span class="sxs-lookup"><span data-stu-id="6440e-166">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6440e-167">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="6440e-167">Availability:</span></span></p></td>
<td><p><span data-ttu-id="6440e-168">Alle</span><span class="sxs-lookup"><span data-stu-id="6440e-168">All</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="requirements"></a><span data-ttu-id="6440e-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6440e-169">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6440e-170"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6440e-170"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6440e-171">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6440e-171">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6440e-172"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6440e-172"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6440e-173">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6440e-173">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6440e-174"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6440e-174"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6440e-175">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="6440e-175">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="see-also"></a><span data-ttu-id="6440e-176">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6440e-176">See Also</span></span>

[<span data-ttu-id="6440e-177">Fehler Behandlungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="6440e-177">Error Handling Constants</span></span>](./error-handling-constants.md)  
[<span data-ttu-id="6440e-178">Fehler Codes für erweiterbare Speicher-Engine</span><span class="sxs-lookup"><span data-stu-id="6440e-178">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="6440e-179">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="6440e-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="6440e-180">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6440e-180">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6440e-181">JetInit</span><span class="sxs-lookup"><span data-stu-id="6440e-181">JetInit</span></span>](./jetinit-function.md)
