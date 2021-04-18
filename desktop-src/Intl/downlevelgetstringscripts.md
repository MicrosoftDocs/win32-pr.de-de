---
description: Stellt eine Liste der in der angegebenen Unicode-Zeichenfolge verwendeten Skripts bereit.
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: Downlevelgetstringscripts-Funktion (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetStringScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: bc5a9fdaf3beb9e1c401943f923fa48bd9d4b44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350875"
---
# <a name="downlevelgetstringscripts-function"></a><span data-ttu-id="c5a60-103">Downlevelgetstringscripts-Funktion</span><span class="sxs-lookup"><span data-stu-id="c5a60-103">DownlevelGetStringScripts function</span></span>

<span data-ttu-id="c5a60-104">Stellt eine Liste der in der angegebenen Unicode-Zeichenfolge verwendeten Skripts bereit.</span><span class="sxs-lookup"><span data-stu-id="c5a60-104">Provides a list of scripts used in the specified Unicode string.</span></span>

> [!Note]  
> <span data-ttu-id="c5a60-105">Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c5a60-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="c5a60-106">Die Verwendung von erfordert das Downloadpaket.</span><span class="sxs-lookup"><span data-stu-id="c5a60-106">Its use requires the download package.</span></span> <span data-ttu-id="c5a60-107">Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**getstringscripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c5a60-107">Applications that only run on Windows Vista and later should call [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c5a60-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5a60-108">Syntax</span></span>


```C++
int DownlevelGetStringScripts(
  _In_  DWORD   dwFlags,
  _In_  LPCWSTR lpString,
  _In_  int     cchString,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a><span data-ttu-id="c5a60-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5a60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5a60-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5a60-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a60-111">Flags, die Optionen für das Abrufen von Skripts angeben.</span><span class="sxs-lookup"><span data-stu-id="c5a60-111">Flags specifying options for script retrieval.</span></span>



| <span data-ttu-id="c5a60-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c5a60-112">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="c5a60-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c5a60-113">Meaning</span></span>                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <span data-ttu-id="c5a60-114"><dt>**GSS \_ zulassen \_ vererbte \_ Common**</dt></span><span class="sxs-lookup"><span data-stu-id="c5a60-114"><dt>**GSS\_ALLOW\_INHERITED\_COMMON**</dt></span></span> </dl> | <span data-ttu-id="c5a60-115">Rufen Sie die Skriptinformationen "qaii" (geerbt) und "zyyy" (Common) ab.</span><span class="sxs-lookup"><span data-stu-id="c5a60-115">Retrieve "Qaii" (INHERITED) and "Zyyy" (COMMON) script information.</span></span> <span data-ttu-id="c5a60-116">Dieser Wert hat keine Auswirkung auf die Verarbeitung nicht zugewiesener Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c5a60-116">This value does not affect the processing of unassigned characters.</span></span> <span data-ttu-id="c5a60-117">Diese Zeichen in der Eingabe Zeichenfolge bewirken immer, dass ein "ZZZZ" (nicht zugewiesenes Skript) in der Skript Zeichenfolge angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c5a60-117">These characters in the input string always cause a "Zzzz" (UNASSIGNED script) to appear in the script string.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="c5a60-118">Standardmäßig ignoriert diese Funktion alle geerbten oder allgemeinen Zeichen in der Unicode-Eingabe Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c5a60-118">By default, this function ignores any inherited or common characters in the input Unicode string.</span></span> <span data-ttu-id="c5a60-119">Wenn GSS \_ Allow \_ geerbte \_ Common nicht festgelegt ist, wird weder "qaii" noch "zyyy" in der Skript Zeichenfolge angezeigt, auch wenn die Eingabe Zeichenfolge solche Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="c5a60-119">If GSS\_ALLOW\_INHERITED\_COMMON is not set, neither "Qaii" nor "Zyyy" will appear in the script string, even if the input string contains such characters.</span></span> <span data-ttu-id="c5a60-120">Wenn GSS \_ \_ die Vererbung von Vererbung zulassen \_ festgelegt ist und die Eingabe Zeichenfolge geerbte und/oder gemeinsame Zeichen enthält, werden "qaii" und/oder "zyyy" in der Skript Zeichenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c5a60-120">If GSS\_ALLOW\_INHERITED\_COMMON is set, and if the input string contains inherited and/or common characters, "Qaii" and/or "Zyyy" appear in the script string.</span></span> <span data-ttu-id="c5a60-121">Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="c5a60-121">See the Remarks section.</span></span>

 

</dd> <dt>

<span data-ttu-id="c5a60-122">*lpString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5a60-122">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a60-123">Zeiger auf die zu analysierende Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c5a60-123">Pointer to the Unicode string to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="c5a60-124">*cchString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5a60-124">*cchString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a60-125">Größe (in Zeichen) der Unicode-Zeichenfolge, die von *lpString* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c5a60-125">Size, in characters, of the Unicode string indicated by *lpString*.</span></span> <span data-ttu-id="c5a60-126">Die Anwendung legt diesen Parameter auf-1 fest, wenn die Zeichenfolge NULL-terminiert ist.</span><span class="sxs-lookup"><span data-stu-id="c5a60-126">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="c5a60-127">Wenn die Anwendung diesen Parameter auf 0 festlegt, ruft die Funktion eine NULL-Unicode-Zeichenfolge (L " \\ 0") in *lpscripts* ab und gibt 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="c5a60-127">If the application sets this parameter to 0, the function retrieves a null Unicode string (L"\\0") in *lpScripts* and returns 1.</span></span>

</dd> <dt>

<span data-ttu-id="c5a60-128">*lpscripts* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c5a60-128">*lpScripts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a60-129">Zeiger auf einen Puffer, in dem diese Funktion eine auf NULL endende Zeichenfolge abruft, die eine Liste von Skripts mit der in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html)verwendeten 4-Zeichen-Notation darstellt.</span><span class="sxs-lookup"><span data-stu-id="c5a60-129">Pointer to a buffer in which this function retrieves a null-terminated string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="c5a60-130">Jeder Skript Name besteht aus vier lateinischen Zeichen, und die Namen werden in alphabetischer Reihenfolge abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c5a60-130">Each script name consists of four Latin characters, and the names are retrieved in alphabetical order.</span></span> <span data-ttu-id="c5a60-131">Auf jeden Namen, einschließlich des letzten, folgt ein Semikolon.</span><span class="sxs-lookup"><span data-stu-id="c5a60-131">Each name, including the last, is followed by a semicolon.</span></span>

<span data-ttu-id="c5a60-132">Alternativ kann dieser Parameter **null** enthalten, wenn *cchscripts* auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c5a60-132">Alternatively, this parameter can contain **NULL** if *cchScripts* set to 0.</span></span> <span data-ttu-id="c5a60-133">In diesem Fall gibt die-Funktion die erforderliche Größe für den Skript Puffer zurück.</span><span class="sxs-lookup"><span data-stu-id="c5a60-133">In this case, the function returns the required size for the script buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c5a60-134">*cchscripts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5a60-134">*cchScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a60-135">Größe in Zeichen für den Skript Puffer, der von *lpscripts* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c5a60-135">Size, in characters, for the script buffer indicated by *lpScripts*.</span></span>

<span data-ttu-id="c5a60-136">Alternativ kann die Anwendung diesen Parameter auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="c5a60-136">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="c5a60-137">In diesem Fall ruft die Funktion **null** in *lpscripts* ab und gibt die erforderliche Größe für den Skript Puffer zurück.</span><span class="sxs-lookup"><span data-stu-id="c5a60-137">In this case, the function retrieves **NULL** in *lpScripts* and returns the required size for the script buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5a60-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5a60-138">Return value</span></span>

<span data-ttu-id="c5a60-139">Gibt die Anzahl von Zeichen zurück, die im Ausgabepuffer abgerufen wurden, einschließlich eines abschließenden NULL-Zeichens, wenn erfolgreich und *cchscripts* auf einen Wert ungleich 0 (null) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c5a60-139">Returns the number of characters retrieved in the output buffer, including a terminating null character, if successful and *cchScripts* is set to a nonzero value.</span></span> <span data-ttu-id="c5a60-140">Die-Funktion gibt 1 zurück, um anzugeben, dass kein Skript gefunden wurde, z. b. wenn die Eingabe Zeichenfolge nur gängige oder geerbte Zeichen enthält und GSS zulassen, dass \_ \_ geerbte \_ Common nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c5a60-140">The function returns 1 to indicate that no script has been found, for example, when the input string only contains COMMON or INHERITED characters and GSS\_ALLOW\_INHERITED\_COMMON is not set.</span></span> <span data-ttu-id="c5a60-141">Da jedes gefundene Skript fünf Zeichen (vier Zeichen + Trennzeichen) hinzufügt, stellt eine einfache mathematische Operation die Skript Anzahl als (Rückgabe \_ Code-1)/5 bereit.</span><span class="sxs-lookup"><span data-stu-id="c5a60-141">Given that each found script adds five characters (four characters + delimiter), a simple mathematical operation provides the script count as (return\_code - 1) / 5.</span></span>

<span data-ttu-id="c5a60-142">Wenn die Funktion erfolgreich ist und der Wert von *cchscripts* 0 ist, ist der Rückgabewert die erforderliche Größe (in Zeichen einschließlich eines abschließenden NULL-Zeichens) für den Skript Puffer.</span><span class="sxs-lookup"><span data-stu-id="c5a60-142">If the function succeeds and the value of *cchScripts* is 0, the return value is the required size, in characters including a terminating null character, for the script buffer.</span></span> <span data-ttu-id="c5a60-143">Die Skript Anzahl ist wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c5a60-143">The script count is as described above.</span></span>

<span data-ttu-id="c5a60-144">Die Funktion gibt 0 zurück, wenn Sie nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="c5a60-144">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="c5a60-145">Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:</span><span class="sxs-lookup"><span data-stu-id="c5a60-145">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="c5a60-146">Fehler \_ baddb.</span><span class="sxs-lookup"><span data-stu-id="c5a60-146">ERROR\_BADDB.</span></span> <span data-ttu-id="c5a60-147">Die Funktion konnte nicht auf die Daten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c5a60-147">The function could not access the data.</span></span> <span data-ttu-id="c5a60-148">Diese Situation sollte normalerweise nicht eintreten, und weist in der Regel auf eine fehlerhafte Installation, ein Datenträger Problem oder das like hin.</span><span class="sxs-lookup"><span data-stu-id="c5a60-148">This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</span></span>
-   <span data-ttu-id="c5a60-149">Fehler \_ beim \_ Puffer.</span><span class="sxs-lookup"><span data-stu-id="c5a60-149">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="c5a60-150">Eine angegebene Puffergröße war nicht groß genug, oder Sie wurde falsch auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c5a60-150">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="c5a60-151">\_ungültige \_ Flags.</span><span class="sxs-lookup"><span data-stu-id="c5a60-151">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="c5a60-152">Die für Flags angegebenen Werte waren ungültig.</span><span class="sxs-lookup"><span data-stu-id="c5a60-152">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="c5a60-153">Fehler \_ : Ungültiger \_ Parameter.</span><span class="sxs-lookup"><span data-stu-id="c5a60-153">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="c5a60-154">Jeder Parameterwert war ungültig.</span><span class="sxs-lookup"><span data-stu-id="c5a60-154">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5a60-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5a60-155">Remarks</span></span>

<span data-ttu-id="c5a60-156">Diese Funktion ist als Teil einer Strategie zum mindern von Sicherheitsproblemen im Zusammenhang mit [internationalisierten Domänen Namen (IDNs)](handling-internationalized-domain-names--idns.md)nützlich.</span><span class="sxs-lookup"><span data-stu-id="c5a60-156">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="c5a60-157">Die Skript Bestimmung basiert auf den vom Unicode-Konsortium in veröffentlichten Skript Werten <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> , mit dem Unterschied, dass die nicht zugewiesenen Zeichen den Wert "ZZZZ" (nicht zugewiesen) anstelle von "zyyy" (Common) aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c5a60-157">The script determination is based on the script values published by the Unicode Consortium in <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt>, except that the unassigned characters have the value "Zzzz" (UNASSIGNED) instead of "Zyyy" (COMMON).</span></span>

<span data-ttu-id="c5a60-158">Im folgenden finden Sie einige Beispiele für das Verhalten dieser Funktion:</span><span class="sxs-lookup"><span data-stu-id="c5a60-158">Here are some examples of the behavior of this function:</span></span>



<span data-ttu-id="c5a60-159">Eingabezeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c5a60-159">Input string</span></span>

<span data-ttu-id="c5a60-160">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c5a60-160">*dwFlags*</span></span>

<span data-ttu-id="c5a60-161">*lpscripts*</span><span class="sxs-lookup"><span data-stu-id="c5a60-161">*lpScripts*</span></span>

<span data-ttu-id="c5a60-162">Skripts</span><span class="sxs-lookup"><span data-stu-id="c5a60-162">Scripts</span></span>

<span data-ttu-id="c5a60-163">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c5a60-163">Microsoft.com</span></span>

<span data-ttu-id="c5a60-164">0</span><span class="sxs-lookup"><span data-stu-id="c5a60-164">0</span></span>

<span data-ttu-id="c5a60-165">Latn</span><span class="sxs-lookup"><span data-stu-id="c5a60-165">Latn;</span></span>

<span data-ttu-id="c5a60-166">Lateinisch</span><span class="sxs-lookup"><span data-stu-id="c5a60-166">Latin</span></span>

<span data-ttu-id="c5a60-167">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c5a60-167">Microsoft.com</span></span>

<span data-ttu-id="c5a60-168">GSS \_ zulassen \_ vererbte \_ Common</span><span class="sxs-lookup"><span data-stu-id="c5a60-168">GSS\_ALLOW\_INHERITED\_COMMON</span></span>

<span data-ttu-id="c5a60-169">Latn Zyyy;</span><span class="sxs-lookup"><span data-stu-id="c5a60-169">Latn;Zyyy;</span></span>

<span data-ttu-id="c5a60-170">Lateinisch und allgemein</span><span class="sxs-lookup"><span data-stu-id="c5a60-170">Latin + Common</span></span>

<span data-ttu-id="c5a60-171">$ {ROWSPAN2} $NI ño $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c5a60-171">${ROWSPAN2}$Niño${REMOVE}$</span></span>  

<span data-ttu-id="c5a60-172">004e 0069 0241 006f</span><span class="sxs-lookup"><span data-stu-id="c5a60-172">004E 0069 0241 006F</span></span>

<span data-ttu-id="c5a60-173">$ {ROWSPAN2} $GSS \_ \_ vererbte \_ Allgemeine $ {Remove} $ zulassen</span><span class="sxs-lookup"><span data-stu-id="c5a60-173">${ROWSPAN2}$GSS\_ALLOW\_INHERITED\_COMMON${REMOVE}$</span></span>  

<span data-ttu-id="c5a60-174">$ {ROWSPAN2} $Latn; $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c5a60-174">${ROWSPAN2}$Latn;${REMOVE}$</span></span>  

<span data-ttu-id="c5a60-175">$ {ROWSPAN2} $Latin $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c5a60-175">${ROWSPAN2}$Latin${REMOVE}$</span></span>  

<span data-ttu-id="c5a60-176">Verwendet lateinischen kleinen Buchstaben N mit Tilde</span><span class="sxs-lookup"><span data-stu-id="c5a60-176">Uses LATIN SMALL LETTER N WITH TILDE</span></span>

<span data-ttu-id="c5a60-177">$ {ROWSPAN2} $NI ño $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c5a60-177">${ROWSPAN2}$Niño${REMOVE}$</span></span>  

<span data-ttu-id="c5a60-178">004e 0069 006e 0303 006f</span><span class="sxs-lookup"><span data-stu-id="c5a60-178">004E 0069 006E 0303 006F</span></span>

<span data-ttu-id="c5a60-179">$ {ROWSPAN2} $GSS \_ \_ vererbte \_ Allgemeine $ {Remove} $ zulassen</span><span class="sxs-lookup"><span data-stu-id="c5a60-179">${ROWSPAN2}$GSS\_ALLOW\_INHERITED\_COMMON${REMOVE}$</span></span>  

<span data-ttu-id="c5a60-180">$ {ROWSPAN2} $Latn; Qaii; $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c5a60-180">${ROWSPAN2}$Latn;Qaii;${REMOVE}$</span></span>  

<span data-ttu-id="c5a60-181">$ {ROWSPAN2} $Latin + geerbt $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c5a60-181">${ROWSPAN2}$Latin + Inherited${REMOVE}$</span></span>  

<span data-ttu-id="c5a60-182">Verwendet das Kombinieren von Tilde</span><span class="sxs-lookup"><span data-stu-id="c5a60-182">Uses COMBINING TILDE</span></span>

<span data-ttu-id="c5a60-183">$ {ROWSPAN2} $SP ůf $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c5a60-183">${ROWSPAN2}$Spооf${REMOVE}$</span></span>  

<span data-ttu-id="c5a60-184">0053 0070 043e 043e 0066</span><span class="sxs-lookup"><span data-stu-id="c5a60-184">0053 0070 043e 043e 0066</span></span>

<span data-ttu-id="c5a60-185">$ {ROWSPAN2} $0 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c5a60-185">${ROWSPAN2}$0${REMOVE}$</span></span>  

<span data-ttu-id="c5a60-186">$ {ROWSPAN2} $Latn; Cyrl; $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c5a60-186">${ROWSPAN2}$Latn;Cyrl;${REMOVE}$</span></span>  

<span data-ttu-id="c5a60-187">$ {ROWSPAN2} $Latin + Cyrillic $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c5a60-187">${ROWSPAN2}$Latin + Cyrillic${REMOVE}$</span></span>  

<span data-ttu-id="c5a60-188">Verwendet den kyrillischen kleinen Buchstaben O</span><span class="sxs-lookup"><span data-stu-id="c5a60-188">Uses CYRILLIC SMALL LETTER O</span></span>

<span data-ttu-id="c5a60-189"></span><span class="sxs-lookup"><span data-stu-id="c5a60-189"></span></span>

<span data-ttu-id="c5a60-190">U + F000</span><span class="sxs-lookup"><span data-stu-id="c5a60-190">U+f000</span></span>

<span data-ttu-id="c5a60-191">0</span><span class="sxs-lookup"><span data-stu-id="c5a60-191">0</span></span>

<span data-ttu-id="c5a60-192">Zzzz</span><span class="sxs-lookup"><span data-stu-id="c5a60-192">Zzzz;</span></span>

<span data-ttu-id="c5a60-193">Nicht zugewiesen</span><span class="sxs-lookup"><span data-stu-id="c5a60-193">Unassigned</span></span>

<span data-ttu-id="c5a60-194"></span><span class="sxs-lookup"><span data-stu-id="c5a60-194"></span></span>

<span data-ttu-id="c5a60-195">U + F000</span><span class="sxs-lookup"><span data-stu-id="c5a60-195">U+f000</span></span>

<span data-ttu-id="c5a60-196">GSS \_ zulassen \_ vererbte \_ Common</span><span class="sxs-lookup"><span data-stu-id="c5a60-196">GSS\_ALLOW\_INHERITED\_COMMON</span></span>

<span data-ttu-id="c5a60-197">Zzzz</span><span class="sxs-lookup"><span data-stu-id="c5a60-197">Zzzz;</span></span>

<span data-ttu-id="c5a60-198">Nicht zugewiesen</span><span class="sxs-lookup"><span data-stu-id="c5a60-198">Unassigned</span></span>



 

<span data-ttu-id="c5a60-199">Die erforderliche Header Datei und dll sind Teil des Downloads ["Microsoft Internationalized Domain Name (IDN) Entschärfungs-APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) , der im [MSDN Download Center](https://www.microsoft.com/?ref=go)verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c5a60-199">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5a60-200">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5a60-200">Requirements</span></span>



| <span data-ttu-id="c5a60-201">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5a60-201">Requirement</span></span> | <span data-ttu-id="c5a60-202">Wert</span><span class="sxs-lookup"><span data-stu-id="c5a60-202">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a60-203">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5a60-203">Minimum supported client</span></span><br/> | <span data-ttu-id="c5a60-204">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5a60-204">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                 |
| <span data-ttu-id="c5a60-205">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5a60-205">Minimum supported server</span></span><br/> | <span data-ttu-id="c5a60-206">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5a60-206">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                        |
| <span data-ttu-id="c5a60-207">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c5a60-207">Redistributable</span></span><br/>          | <span data-ttu-id="c5a60-208">Microsoft Internationalized Domain Name (IDN) Entschärfungs-APIs unter Windows XP (SP2 oder höher), Windows Server 2003 (SP1 oder höher) oder Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5a60-208">Microsoft Internationalized Domain Name (IDN) Mitigation APIs on Windows XP (SP2 or later), Windows Server 2003 (SP1 or later), or Windows Vista</span></span><br/> |
| <span data-ttu-id="c5a60-209">Header</span><span class="sxs-lookup"><span data-stu-id="c5a60-209">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5a60-210"><dt>Idndl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5a60-210"><dt>Idndl.h</dt></span></span> </dl>                                                                          |
| <span data-ttu-id="c5a60-211">DLL</span><span class="sxs-lookup"><span data-stu-id="c5a60-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5a60-212"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5a60-212"><dt>Idndl.dll</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="c5a60-213">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5a60-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5a60-214">Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="c5a60-214">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="c5a60-215">Funktionen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="c5a60-215">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="c5a60-216">Umgang mit internationalisierten Domänen Namen (IDNs)</span><span class="sxs-lookup"><span data-stu-id="c5a60-216">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="c5a60-217">**Downlevelgetlocalescripts**</span><span class="sxs-lookup"><span data-stu-id="c5a60-217">**DownlevelGetLocaleScripts**</span></span>](downlevelgetlocalescripts.md)
</dt> <dt>

[<span data-ttu-id="c5a60-218">**Downlevelverifyscripts**</span><span class="sxs-lookup"><span data-stu-id="c5a60-218">**DownlevelVerifyScripts**</span></span>](downlevelverifyscripts.md)
</dt> <dt>

[<span data-ttu-id="c5a60-219">**Getstringscripts**</span><span class="sxs-lookup"><span data-stu-id="c5a60-219">**GetStringScripts**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 
