---
description: Stellt eine Liste von Skripts für das angegebene Gebiets Schema bereit.
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: Downlevelgetlocalescripts-Funktion (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetLocaleScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: f636ab426cd4d50878df93e3e30d69de54d60ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217806"
---
# <a name="downlevelgetlocalescripts-function"></a><span data-ttu-id="eb0db-103">Downlevelgetlocalescripts-Funktion</span><span class="sxs-lookup"><span data-stu-id="eb0db-103">DownlevelGetLocaleScripts function</span></span>

<span data-ttu-id="eb0db-104">Stellt eine Liste von Skripts für das angegebene Gebiets Schema bereit.</span><span class="sxs-lookup"><span data-stu-id="eb0db-104">Provides a list of scripts for the specified locale.</span></span>

> [!Note]  
> <span data-ttu-id="eb0db-105">Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="eb0db-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="eb0db-106">Die Verwendung von erfordert das Downloadpaket.</span><span class="sxs-lookup"><span data-stu-id="eb0db-106">Its use requires the download package.</span></span> <span data-ttu-id="eb0db-107">Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) mit *LCTYPE* aufrufen, der auf [locale \_ sscripts](locale-sscripts.md)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="eb0db-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SSCRIPTS](locale-sscripts.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="eb0db-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb0db-108">Syntax</span></span>


```C++
int DownlevelGetLocaleScripts(
  _In_  LPCWSTR lpLocaleName,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a><span data-ttu-id="eb0db-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb0db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb0db-110">*lplocalename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb0db-110">*lpLocaleName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb0db-111">Zeiger auf einen mit NULL endenden Gebiets Schema [Namen](locale-names.md).</span><span class="sxs-lookup"><span data-stu-id="eb0db-111">Pointer to a null-terminated [locale name](locale-names.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb0db-112">*lpscripts* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="eb0db-112">*lpScripts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb0db-113">Zeiger auf einen Puffer, in dem diese Funktion eine auf NULL endende Zeichenfolge abruft, die eine Liste von Skripts mit der in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html)verwendeten 4-Zeichen-Notation darstellt.</span><span class="sxs-lookup"><span data-stu-id="eb0db-113">Pointer to a buffer in which this function retrieves a null-terminated string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="eb0db-114">Jeder Skript Name besteht aus vier lateinischen Zeichen, und die Namen werden in alphabetischer Reihenfolge abgerufen.</span><span class="sxs-lookup"><span data-stu-id="eb0db-114">Each script name consists of four Latin characters, and the names are retrieved in alphabetical order.</span></span> <span data-ttu-id="eb0db-115">Auf jede dieser, einschließlich der letzten, folgt ein Semikolon.</span><span class="sxs-lookup"><span data-stu-id="eb0db-115">Each of them, including the last, is followed by a semicolon.</span></span>

<span data-ttu-id="eb0db-116">Alternativ kann dieser Parameter **null** enthalten, wenn *cchscripts* auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="eb0db-116">Alternatively, this parameter can contain **NULL** if *cchScripts* is set to 0.</span></span> <span data-ttu-id="eb0db-117">In diesem Fall gibt die-Funktion die erforderliche Größe für den Skript Puffer zurück.</span><span class="sxs-lookup"><span data-stu-id="eb0db-117">In this case, the function returns the required size for the script buffer.</span></span>

</dd> <dt>

<span data-ttu-id="eb0db-118">*cchscripts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb0db-118">*cchScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb0db-119">Größe in Zeichen für den Skript Puffer, der von *lpscripts* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eb0db-119">Size, in characters, for the script buffer indicated by *lpScripts*.</span></span>

<span data-ttu-id="eb0db-120">Alternativ kann die Anwendung diesen Parameter auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="eb0db-120">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="eb0db-121">In diesem Fall ruft die Funktion **null** in *lpscripts* ab und gibt die erforderliche Größe für den Skript Puffer zurück.</span><span class="sxs-lookup"><span data-stu-id="eb0db-121">In this case, the function retrieves **NULL** in *lpScripts* and returns the required size for the script buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb0db-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb0db-122">Return value</span></span>

<span data-ttu-id="eb0db-123">Gibt die Anzahl von Zeichen zurück, die im Skript Puffer abgerufen wurden, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="eb0db-123">Returns the number of characters retrieved in the script buffer, including the terminating null character.</span></span> <span data-ttu-id="eb0db-124">Wenn die Funktion erfolgreich ist und der Wert von *cchscripts* 0 ist, ist der Rückgabewert die erforderliche Größe (in Zeichen einschließlich eines abschließenden NULL-Zeichens) für den Skript Puffer.</span><span class="sxs-lookup"><span data-stu-id="eb0db-124">If the function succeeds and the value of *cchScripts* is 0, the return value is the required size, in characters including a terminating null character, for the script buffer.</span></span>

<span data-ttu-id="eb0db-125">Diese Funktion gibt 0 (null) zurück, wenn Sie nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="eb0db-125">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="eb0db-126">Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:</span><span class="sxs-lookup"><span data-stu-id="eb0db-126">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="eb0db-127">Fehler \_ baddb.</span><span class="sxs-lookup"><span data-stu-id="eb0db-127">ERROR\_BADDB.</span></span> <span data-ttu-id="eb0db-128">Die Funktion konnte nicht auf die Daten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="eb0db-128">The function could not access the data.</span></span> <span data-ttu-id="eb0db-129">Diese Situation sollte normalerweise nicht eintreten, und weist in der Regel auf eine fehlerhafte Installation, ein Datenträger Problem oder das like hin.</span><span class="sxs-lookup"><span data-stu-id="eb0db-129">This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</span></span>
-   <span data-ttu-id="eb0db-130">Fehler \_ beim \_ Puffer.</span><span class="sxs-lookup"><span data-stu-id="eb0db-130">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="eb0db-131">Eine angegebene Puffergröße war nicht groß genug, oder Sie wurde falsch auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eb0db-131">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="eb0db-132">Fehler \_ : Ungültiger \_ Parameter.</span><span class="sxs-lookup"><span data-stu-id="eb0db-132">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="eb0db-133">Jeder Parameterwert war ungültig.</span><span class="sxs-lookup"><span data-stu-id="eb0db-133">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb0db-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb0db-134">Remarks</span></span>

<span data-ttu-id="eb0db-135">Diese Funktion ist als Teil einer Strategie zum mindern von Sicherheitsproblemen im Zusammenhang mit [internationalisierten Domänen Namen (IDNs)](handling-internationalized-domain-names--idns.md)nützlich.</span><span class="sxs-lookup"><span data-stu-id="eb0db-135">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="eb0db-136">Im folgenden finden Sie einige Beispiele für Eingaben und Ausgaben für diese Funktion mit einer ausreichenden Puffergröße:</span><span class="sxs-lookup"><span data-stu-id="eb0db-136">Here are some examples of inputs and outputs for this function, assuming a sufficient buffer size:</span></span>



| <span data-ttu-id="eb0db-137">Gebietsschema</span><span class="sxs-lookup"><span data-stu-id="eb0db-137">Locale</span></span>                  | <span data-ttu-id="eb0db-138">*lplocalename*</span><span class="sxs-lookup"><span data-stu-id="eb0db-138">*lpLocaleName*</span></span> | <span data-ttu-id="eb0db-139">*lpscripts*</span><span class="sxs-lookup"><span data-stu-id="eb0db-139">*lpScripts*</span></span>     |
|-------------------------|----------------|-----------------|
| <span data-ttu-id="eb0db-140">Englisch (USA)</span><span class="sxs-lookup"><span data-stu-id="eb0db-140">English (United States)</span></span> | <span data-ttu-id="eb0db-141">de-DE</span><span class="sxs-lookup"><span data-stu-id="eb0db-141">en-US</span></span>          | <span data-ttu-id="eb0db-142">Latn</span><span class="sxs-lookup"><span data-stu-id="eb0db-142">Latn;</span></span>           |
| <span data-ttu-id="eb0db-143">Hindi (Indien)</span><span class="sxs-lookup"><span data-stu-id="eb0db-143">Hindi (India)</span></span>           | <span data-ttu-id="eb0db-144">hi-IN</span><span class="sxs-lookup"><span data-stu-id="eb0db-144">hi-IN</span></span>          | <span data-ttu-id="eb0db-145">Vas</span><span class="sxs-lookup"><span data-stu-id="eb0db-145">Deva;</span></span>           |
| <span data-ttu-id="eb0db-146">Japanisch (Japan)</span><span class="sxs-lookup"><span data-stu-id="eb0db-146">Japanese (Japan)</span></span>        | <span data-ttu-id="eb0db-147">ja-JP</span><span class="sxs-lookup"><span data-stu-id="eb0db-147">ja-JP</span></span>          | <span data-ttu-id="eb0db-148">Han Hira; Betrieben</span><span class="sxs-lookup"><span data-stu-id="eb0db-148">Hani;Hira;Kana;</span></span> |



 

<span data-ttu-id="eb0db-149">Die Liste enthält nicht das lateinische Skript, es sei denn, es ist ein wesentlicher Bestandteil des Schreibsystems, das für ein Gebiets Schema verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eb0db-149">The list does not contain the Latin script unless it is an essential part of the writing system used for a locale.</span></span> <span data-ttu-id="eb0db-150">Lateinische Zeichen werden jedoch häufig im Kontext von Gebiets Schemas verwendet, für die Sie nicht nativ sind, wie bei einem fremden Geschäftsnamen.</span><span class="sxs-lookup"><span data-stu-id="eb0db-150">However, Latin characters are often used in the context of locales for which they are not native, as for a foreign business name.</span></span> <span data-ttu-id="eb0db-151">Im obigen Beispiel für Hindi in Indien ist das einzige abgerufene Skript "Deva" (für "Devanagari"), obwohl auch lateinische Zeichen in Hindi-Text vorkommen können.</span><span class="sxs-lookup"><span data-stu-id="eb0db-151">In the example above for Hindi in India, the only script retrieved is "Deva" (for Devanagari), although Latin characters can also appear in Hindi text.</span></span> <span data-ttu-id="eb0db-152">Die [**downlevelverifyscripts**](downlevelverifyscripts.md) -Funktion verfügt über ein spezielles Flag, um diesen Fall zu beheben.</span><span class="sxs-lookup"><span data-stu-id="eb0db-152">The [**DownlevelVerifyScripts**](downlevelverifyscripts.md) function has a special flag to address that case.</span></span>

<span data-ttu-id="eb0db-153">Die erforderliche Header Datei und dll sind Teil des Downloads ["Microsoft Internationalized Domain Name (IDN) Entschärfungs-APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , der im [MSDN Download Center](https://www.microsoft.com/?ref=go)verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="eb0db-153">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb0db-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb0db-154">Requirements</span></span>



| <span data-ttu-id="eb0db-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb0db-155">Requirement</span></span> | <span data-ttu-id="eb0db-156">Wert</span><span class="sxs-lookup"><span data-stu-id="eb0db-156">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb0db-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb0db-157">Minimum supported client</span></span><br/> | <span data-ttu-id="eb0db-158">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb0db-158">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                 |
| <span data-ttu-id="eb0db-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb0db-159">Minimum supported server</span></span><br/> | <span data-ttu-id="eb0db-160">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb0db-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                        |
| <span data-ttu-id="eb0db-161">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="eb0db-161">Redistributable</span></span><br/>          | <span data-ttu-id="eb0db-162">Microsoft Internationalized Domain Name (IDN) Entschärfungs-APIs unter Windows XP (SP2 oder höher), Windows Server 2003 (SP1 oder höher) oder Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb0db-162">Microsoft Internationalized Domain Name (IDN) Mitigation APIs on Windows XP (SP2 or later), Windows Server 2003 (SP1 or later), or Windows Vista</span></span><br/> |
| <span data-ttu-id="eb0db-163">Header</span><span class="sxs-lookup"><span data-stu-id="eb0db-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb0db-164"><dt>Idndl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb0db-164"><dt>Idndl.h</dt></span></span> </dl>                                                                          |
| <span data-ttu-id="eb0db-165">DLL</span><span class="sxs-lookup"><span data-stu-id="eb0db-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb0db-166"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb0db-166"><dt>Idndl.dll</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="eb0db-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb0db-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb0db-168">Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="eb0db-168">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="eb0db-169">Funktionen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="eb0db-169">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="eb0db-170">Umgang mit internationalisierten Domänen Namen (IDNs)</span><span class="sxs-lookup"><span data-stu-id="eb0db-170">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="eb0db-171">**Downlevelgetstringscripts**</span><span class="sxs-lookup"><span data-stu-id="eb0db-171">**DownlevelGetStringScripts**</span></span>](downlevelgetstringscripts.md)
</dt> <dt>

[<span data-ttu-id="eb0db-172">**Downlevelverifyscripts**</span><span class="sxs-lookup"><span data-stu-id="eb0db-172">**DownlevelVerifyScripts**</span></span>](downlevelverifyscripts.md)
</dt> <dt>

[<span data-ttu-id="eb0db-173">**Getlocaleingefo**</span><span class="sxs-lookup"><span data-stu-id="eb0db-173">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
