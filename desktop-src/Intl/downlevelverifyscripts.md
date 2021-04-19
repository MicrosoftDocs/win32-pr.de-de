---
description: Vergleicht zwei aufgelistete Listen von Skripts.
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: Downlevelverifyscripts-Funktion (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelVerifyScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: 62e029576d53109e3c57faf4ec913472f8aea65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364190"
---
# <a name="downlevelverifyscripts-function"></a><span data-ttu-id="9de07-103">Downlevelverifyscripts-Funktion</span><span class="sxs-lookup"><span data-stu-id="9de07-103">DownlevelVerifyScripts function</span></span>

<span data-ttu-id="9de07-104">Vergleicht zwei aufgelistete Listen von Skripts.</span><span class="sxs-lookup"><span data-stu-id="9de07-104">Compares two enumerated lists of scripts.</span></span>

> [!Note]  
> <span data-ttu-id="9de07-105">Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9de07-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="9de07-106">Die Verwendung von erfordert das Downloadpaket.</span><span class="sxs-lookup"><span data-stu-id="9de07-106">Its use requires the download package.</span></span> <span data-ttu-id="9de07-107">Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**verifyscripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)aufruft.</span><span class="sxs-lookup"><span data-stu-id="9de07-107">Applications that only run on Windows Vista and later should call [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9de07-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9de07-108">Syntax</span></span>


```C++
BOOL DownlevelVerifyScripts(
  _In_ DWORD   dwFlags,
  _In_ LPCWSTR lpLocaleScripts,
  _In_ int     cchLocaleScripts,
  _In_ LPCWSTR lpTestScripts,
  _In_ int     cchTestScripts
);
```



## <a name="parameters"></a><span data-ttu-id="9de07-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9de07-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9de07-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9de07-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9de07-111">Flags, die Optionen für die Skript Überprüfung angeben.</span><span class="sxs-lookup"><span data-stu-id="9de07-111">Flags specifying script verification options.</span></span>



| <span data-ttu-id="9de07-112">Wert</span><span class="sxs-lookup"><span data-stu-id="9de07-112">Value</span></span>                                                                                                                                                             | <span data-ttu-id="9de07-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9de07-113">Meaning</span></span>                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <span data-ttu-id="9de07-114"><dt>**VS \_ Allow \_ Latin**</dt></span><span class="sxs-lookup"><span data-stu-id="9de07-114"><dt>**VS\_ALLOW\_LATIN**</dt></span></span> </dl> | <span data-ttu-id="9de07-115">Lassen Sie "Latn" (lateinische Skripts) in der Testliste zu, auch wenn Sie sich nicht in der Liste der Gebiets Schemas befinden.</span><span class="sxs-lookup"><span data-stu-id="9de07-115">Allow "Latn" (Latin script) in the test list, even if it is not in the locale list.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9de07-116">*lplocalescripts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9de07-116">*lpLocaleScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9de07-117">Zeiger auf die Liste der Gebiets Schemas, die Aufzählungs Liste der Skripts für ein bestimmtes Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="9de07-117">Pointer to the locale list, the enumerated list of scripts for a given locale.</span></span> <span data-ttu-id="9de07-118">Diese Liste wird in der Regel durch Aufrufen von [**downlevelgetlocalescripts**](downlevelgetlocalescripts.md)aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="9de07-118">This list is typically populated by calling [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).</span></span>

</dd> <dt>

<span data-ttu-id="9de07-119">*cchlocalescripts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9de07-119">*cchLocaleScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9de07-120">Die Größe (in Zeichen) der Zeichenfolge, die von *lplocalescripts* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9de07-120">Size, in characters, of the string indicated by *lpLocaleScripts*.</span></span> <span data-ttu-id="9de07-121">Die Anwendung legt diesen Parameter auf-1 fest, wenn die Zeichenfolge NULL-terminiert ist.</span><span class="sxs-lookup"><span data-stu-id="9de07-121">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="9de07-122">Wenn dieser Parameter auf 0 festgelegt ist, schlägt die Funktion fehl.</span><span class="sxs-lookup"><span data-stu-id="9de07-122">If this parameter is set to 0, the function fails.</span></span>

</dd> <dt>

<span data-ttu-id="9de07-123">*lptestscripts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9de07-123">*lpTestScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9de07-124">Zeiger auf die Testliste, eine zweite aufgelistete Liste von Skripts.</span><span class="sxs-lookup"><span data-stu-id="9de07-124">Pointer to the test list, a second enumerated list of scripts.</span></span> <span data-ttu-id="9de07-125">Diese Liste wird in der Regel durch Aufrufen von [**downlevelgetstringscripts**](downlevelgetstringscripts.md)aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="9de07-125">This list is typically populated by calling [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).</span></span>

</dd> <dt>

<span data-ttu-id="9de07-126">*cchtestscripts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9de07-126">*cchTestScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9de07-127">Die Größe (in Zeichen) der Zeichenfolge, die von *lptestscripts* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9de07-127">Size, in characters, of the string indicated by *lpTestScripts*.</span></span> <span data-ttu-id="9de07-128">Die Anwendung legt diesen Parameter auf-1 fest, wenn die Zeichenfolge NULL-terminiert ist.</span><span class="sxs-lookup"><span data-stu-id="9de07-128">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="9de07-129">Wenn dieser Parameter auf 0 festgelegt ist, schlägt die Funktion fehl.</span><span class="sxs-lookup"><span data-stu-id="9de07-129">If this parameter is set to 0, the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9de07-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9de07-130">Return value</span></span>

<span data-ttu-id="9de07-131">Gibt " **true** " zurück, wenn die Testliste nicht leer ist und alle Elemente in der Liste auch in der Liste der Gebiets Schemas enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="9de07-131">Returns **TRUE** if the test list is non-empty and all items in the list are also included in the locale list.</span></span> <span data-ttu-id="9de07-132">Andernfalls gibt die Funktion **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="9de07-132">Otherwise, the function returns **FALSE**.</span></span>

<span data-ttu-id="9de07-133">Der Rückgabewert **false** kann darauf hindeuten, dass die Testliste ein Element enthält, das nicht in der Liste der Gebiets Schemas enthalten ist, oder es kann auf einen Fehler hinweisen.</span><span class="sxs-lookup"><span data-stu-id="9de07-133">A return value of **FALSE** can indicate that the test list contains an item that is not in the locale list, or it can indicate an error.</span></span> <span data-ttu-id="9de07-134">Um zwischen diesen beiden Fällen zu unterscheiden, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9de07-134">To distinguish between these two cases, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="9de07-135">Wenn **downlevelverifyscripts** erfolgreich festgestellt hat, dass ein Element in der Testliste vorhanden ist, das nicht in der Liste der Gebiets Schemas enthalten ist, gibt **GetLastError** den Fehler \_ Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="9de07-135">If **DownlevelVerifyScripts** has successfully determined that there is an item in the test list that is not in the locale list, **GetLastError** returns ERROR\_SUCCESS.</span></span> <span data-ttu-id="9de07-136">Andernfalls kann **GetLastError** einen der folgenden Fehlercodes zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="9de07-136">Otherwise, **GetLastError** can return one of the following error codes:</span></span>

-   <span data-ttu-id="9de07-137">\_ungültige \_ Flags.</span><span class="sxs-lookup"><span data-stu-id="9de07-137">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="9de07-138">Die für Flags angegebenen Werte waren ungültig.</span><span class="sxs-lookup"><span data-stu-id="9de07-138">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="9de07-139">Fehler \_ : Ungültiger \_ Parameter.</span><span class="sxs-lookup"><span data-stu-id="9de07-139">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="9de07-140">Jeder Parameterwert war ungültig.</span><span class="sxs-lookup"><span data-stu-id="9de07-140">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="9de07-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9de07-141">Remarks</span></span>

<span data-ttu-id="9de07-142">Diese Funktion vergleicht Zeichen folgen, z. b. "Latn;". Cyrl; ", die aus einer Reihe von 4-Zeichen-Skriptnamen bestehen, wobei jeder Skript Name auf ein Semikolon folgt.</span><span class="sxs-lookup"><span data-stu-id="9de07-142">This function compares strings, such as "Latn;Cyrl;", that consist of a series of 4-character script names, with each script name followed by a semicolon.</span></span> <span data-ttu-id="9de07-143">Es gilt auch für einen besonderen Fall, dass das lateinische Skript häufig in Sprachen und Gebiets Schemas verwendet wird, für die es nicht nativ ist.</span><span class="sxs-lookup"><span data-stu-id="9de07-143">It also has a special case to account for the fact that the Latin script is often used in languages and locales for which it is not native.</span></span>

<span data-ttu-id="9de07-144">Diese Funktion ist als Teil einer Strategie zum mindern von Sicherheitsproblemen im Zusammenhang mit [internationalisierten Domänen Namen (IDNs)](handling-internationalized-domain-names--idns.md)nützlich.</span><span class="sxs-lookup"><span data-stu-id="9de07-144">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="9de07-145">Im folgenden finden Sie Beispiele für die Rückgabe dieser Funktion und einen nachfolgenden Rückruf von [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) in verschiedenen Szenarien.</span><span class="sxs-lookup"><span data-stu-id="9de07-145">The following are examples of the return of this function and a subsequent call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) in various scenarios.</span></span> <span data-ttu-id="9de07-146">In den letzten beiden Beispielen wird ein Fall veranschaulicht, in dem die Testliste ein abschließendes Semikolon (falsch formatierte Zeichenfolge) und einen Fall, in dem die Testliste leer ist, fehlt.</span><span class="sxs-lookup"><span data-stu-id="9de07-146">The last two examples illustrate, respectively, a case in which the test list lacks a terminating semicolon (malformed string) and a case in which the test list is empty.</span></span>



| <span data-ttu-id="9de07-147">"Locale"-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9de07-147">"Locale" string</span></span> | <span data-ttu-id="9de07-148">"Test"-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9de07-148">"Test" string</span></span> | <span data-ttu-id="9de07-149">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="9de07-149">*dwFlags*</span></span>        | <span data-ttu-id="9de07-150">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9de07-150">Return value</span></span> | <span data-ttu-id="9de07-151">GetLastError-Rückgabe</span><span class="sxs-lookup"><span data-stu-id="9de07-151">GetLastError return</span></span>       |
|-----------------|---------------|------------------|--------------|---------------------------|
| <span data-ttu-id="9de07-152">Han Hira; Betrieben</span><span class="sxs-lookup"><span data-stu-id="9de07-152">Hani;Hira;Kana;</span></span> | <span data-ttu-id="9de07-153">Han</span><span class="sxs-lookup"><span data-stu-id="9de07-153">Hani;</span></span>         | <span data-ttu-id="9de07-154">–</span><span class="sxs-lookup"><span data-stu-id="9de07-154">N/A</span></span>              | <span data-ttu-id="9de07-155">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="9de07-155">**TRUE**</span></span>     | <span data-ttu-id="9de07-156">–</span><span class="sxs-lookup"><span data-stu-id="9de07-156">N/A</span></span>                       |
| <span data-ttu-id="9de07-157">Han Hira; Betrieben</span><span class="sxs-lookup"><span data-stu-id="9de07-157">Hani;Hira;Kana;</span></span> | <span data-ttu-id="9de07-158">Han Latn</span><span class="sxs-lookup"><span data-stu-id="9de07-158">Hani;Latn;</span></span>    | <span data-ttu-id="9de07-159">0</span><span class="sxs-lookup"><span data-stu-id="9de07-159">0</span></span>                | <span data-ttu-id="9de07-160">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="9de07-160">**FALSE**</span></span>    | <span data-ttu-id="9de07-161">Fehler \_ erfolgreich</span><span class="sxs-lookup"><span data-stu-id="9de07-161">ERROR\_SUCCESS</span></span>            |
| <span data-ttu-id="9de07-162">Han Hira; Betrieben</span><span class="sxs-lookup"><span data-stu-id="9de07-162">Hani;Hira;Kana;</span></span> | <span data-ttu-id="9de07-163">Han Latn</span><span class="sxs-lookup"><span data-stu-id="9de07-163">Hani;Latn;</span></span>    | <span data-ttu-id="9de07-164">VS \_ Allow \_ Latin</span><span class="sxs-lookup"><span data-stu-id="9de07-164">VS\_ALLOW\_LATIN</span></span> | <span data-ttu-id="9de07-165">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="9de07-165">**TRUE**</span></span>     | <span data-ttu-id="9de07-166">–</span><span class="sxs-lookup"><span data-stu-id="9de07-166">N/A</span></span>                       |
| <span data-ttu-id="9de07-167">Han Hira; Betrieben</span><span class="sxs-lookup"><span data-stu-id="9de07-167">Hani;Hira;Kana;</span></span> | <span data-ttu-id="9de07-168">Cyrl;</span><span class="sxs-lookup"><span data-stu-id="9de07-168">Cyrl;</span></span>         | <span data-ttu-id="9de07-169">–</span><span class="sxs-lookup"><span data-stu-id="9de07-169">N/A</span></span>              | <span data-ttu-id="9de07-170">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="9de07-170">**FALSE**</span></span>    | <span data-ttu-id="9de07-171">Fehler \_ erfolgreich</span><span class="sxs-lookup"><span data-stu-id="9de07-171">ERROR\_SUCCESS</span></span>            |
| <span data-ttu-id="9de07-172">Han Hira; Betrieben</span><span class="sxs-lookup"><span data-stu-id="9de07-172">Hani;Hira;Kana;</span></span> | <span data-ttu-id="9de07-173">Cyrl;</span><span class="sxs-lookup"><span data-stu-id="9de07-173">Cyrl;</span></span>         | <span data-ttu-id="9de07-174">–</span><span class="sxs-lookup"><span data-stu-id="9de07-174">N/A</span></span>              | <span data-ttu-id="9de07-175">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="9de07-175">**FALSE**</span></span>    | <span data-ttu-id="9de07-176">Fehler bei \_ ungültigem \_ Parameter</span><span class="sxs-lookup"><span data-stu-id="9de07-176">ERROR\_INVALID\_PARAMETER</span></span> |
| <span data-ttu-id="9de07-177">Han Hira; Betrieben</span><span class="sxs-lookup"><span data-stu-id="9de07-177">Hani;Hira;Kana;</span></span> |               | <span data-ttu-id="9de07-178">–</span><span class="sxs-lookup"><span data-stu-id="9de07-178">N/A</span></span>              | <span data-ttu-id="9de07-179">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="9de07-179">**FALSE**</span></span>    | <span data-ttu-id="9de07-180">Fehler \_ erfolgreich</span><span class="sxs-lookup"><span data-stu-id="9de07-180">ERROR\_SUCCESS</span></span>            |



 

<span data-ttu-id="9de07-181">Die erforderliche Header Datei und dll sind Teil des Downloads ["Microsoft Internationalized Domain Name (IDN) Entschärfungs-APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , der im [MSDN Download Center](https://www.microsoft.com/?ref=go)verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9de07-181">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="9de07-182">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9de07-182">Requirements</span></span>



| <span data-ttu-id="9de07-183">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9de07-183">Requirement</span></span> | <span data-ttu-id="9de07-184">Wert</span><span class="sxs-lookup"><span data-stu-id="9de07-184">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9de07-185">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9de07-185">Minimum supported client</span></span><br/> | <span data-ttu-id="9de07-186">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9de07-186">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                  |
| <span data-ttu-id="9de07-187">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9de07-187">Minimum supported server</span></span><br/> | <span data-ttu-id="9de07-188">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9de07-188">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                         |
| <span data-ttu-id="9de07-189">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="9de07-189">Redistributable</span></span><br/>          | <span data-ttu-id="9de07-190">Microsoft Internationalized Domain Name (IDN) Entschärfungs-APIs onwindows XP mit SP2, Windows Server 2003 mit SP1, orwindows Vista</span><span class="sxs-lookup"><span data-stu-id="9de07-190">Microsoft Internationalized Domain Name (IDN) Mitigation APIs onWindows XP with SP2,Windows Server 2003 with SP1, orWindows Vista</span></span><br/> |
| <span data-ttu-id="9de07-191">Header</span><span class="sxs-lookup"><span data-stu-id="9de07-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="9de07-192"><dt>Idndl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9de07-192"><dt>Idndl.h</dt></span></span> </dl>                                                           |
| <span data-ttu-id="9de07-193">DLL</span><span class="sxs-lookup"><span data-stu-id="9de07-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9de07-194"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9de07-194"><dt>Idndl.dll</dt></span></span> </dl>                                                         |



## <a name="see-also"></a><span data-ttu-id="9de07-195">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9de07-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9de07-196">Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="9de07-196">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="9de07-197">Funktionen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="9de07-197">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="9de07-198">Umgang mit internationalisierten Domänen Namen (IDNs)</span><span class="sxs-lookup"><span data-stu-id="9de07-198">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="9de07-199">**Downlevelgetlocalescripts**</span><span class="sxs-lookup"><span data-stu-id="9de07-199">**DownlevelGetLocaleScripts**</span></span>](downlevelgetlocalescripts.md)
</dt> <dt>

[<span data-ttu-id="9de07-200">**Downlevelgetstringscripts**</span><span class="sxs-lookup"><span data-stu-id="9de07-200">**DownlevelGetStringScripts**</span></span>](downlevelgetstringscripts.md)
</dt> <dt>

[<span data-ttu-id="9de07-201">**Verifyscripts**</span><span class="sxs-lookup"><span data-stu-id="9de07-201">**VerifyScripts**</span></span>](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 
