---
description: Vergleicht zwei Unicode-Zeichen folgen unter Verwendung eines angegebenen Gebiets Schemas.
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: Comparestringwrapw-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 0731182f5c01ad56db722972628d2cbe39373835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977384"
---
# <a name="comparestringwrapw-function"></a><span data-ttu-id="937eb-103">Comparestringwrapw-Funktion</span><span class="sxs-lookup"><span data-stu-id="937eb-103">CompareStringWrapW function</span></span>

<span data-ttu-id="937eb-104">\[**Comparestringwrapw** ist für die Verwendung in Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="937eb-104">\[**CompareStringWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="937eb-105">Sie wird in nachfolgenden Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="937eb-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="937eb-106">Sie sollten [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) an seiner Stelle verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="937eb-106">You should use [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in its place.\]</span></span>

<span data-ttu-id="937eb-107">Vergleicht zwei Unicode-Zeichen folgen unter Verwendung eines angegebenen Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="937eb-107">Compares two Unicode character strings, using a specified locale.</span></span>

> [!Note]  
> <span data-ttu-id="937eb-108">**Comparestringwrapw** ist ein Wrapper für die **CompareStringW** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="937eb-108">**CompareStringWrapW** is a wrapper for the **CompareStringW** function.</span></span> <span data-ttu-id="937eb-109">Weitere Hinweise zur Verwendung finden Sie auf der Seite " [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) ".</span><span class="sxs-lookup"><span data-stu-id="937eb-109">See the [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="937eb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="937eb-110">Syntax</span></span>


```C++
int CompareStringWrapW(
  _In_ LCID    Locale,
  _In_ DWORD   dwCmpFlags,
  _In_ LPCWSTR lpString1,
  _In_ int     cchCount1,
  _In_ LPCWSTR lpString2,
  _In_ int     cchCount2
);
```



## <a name="parameters"></a><span data-ttu-id="937eb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="937eb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="937eb-112">Gebiets Schema  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="937eb-112">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="937eb-113">Typ: **LCID**</span><span class="sxs-lookup"><span data-stu-id="937eb-113">Type: **LCID**</span></span>

<span data-ttu-id="937eb-114">Ein für den Vergleich verwendeter Gebiets Schema Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="937eb-114">A locale identifier used for the comparison.</span></span> <span data-ttu-id="937eb-115">Dieser Parameter kann einer der folgenden vordefinierten Gebiets Schema Bezeichner oder ein Gebiets Schema Bezeichner sein, der vom [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) -Makro erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="937eb-115">This parameter can be one of the following predefined locale identifiers or a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="937eb-116"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**Standard für Gebiets Schema \_ System \_**</span><span class="sxs-lookup"><span data-stu-id="937eb-116"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="937eb-117">Das Standard Gebiets Schema des Systems.</span><span class="sxs-lookup"><span data-stu-id="937eb-117">The system's default locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="937eb-118"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_Standardbenutzer Name für locale \_**</span><span class="sxs-lookup"><span data-stu-id="937eb-118"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="937eb-119">Das Standard Gebiets Schema des aktuellen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="937eb-119">The current user's default locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="937eb-120">*dwcmpflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="937eb-120">*dwCmpFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="937eb-121">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="937eb-121">Type: **DWORD**</span></span>

<span data-ttu-id="937eb-122">Die Flags, die angeben, wie die Funktion die beiden Zeichen folgen vergleicht.</span><span class="sxs-lookup"><span data-stu-id="937eb-122">The flags that indicate how the function compares the two strings.</span></span> <span data-ttu-id="937eb-123">Standardmäßig sind diese Flags nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="937eb-123">By default, these flags are not set.</span></span> <span data-ttu-id="937eb-124">Legen Sie den Wert auf NULL fest, um das Standardverhalten oder eine beliebige Kombination der folgenden Werte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="937eb-124">Set to zero to get the default behavior or to any combination of the following values.</span></span>

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span data-ttu-id="937eb-125"><span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**Norm \_ ignoreCase**</span><span class="sxs-lookup"><span data-stu-id="937eb-125"><span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**NORM\_IGNORECASE**</span></span>


</dt> <dd>

<span data-ttu-id="937eb-126">Fall ignorieren.</span><span class="sxs-lookup"><span data-stu-id="937eb-126">Ignore case.</span></span>

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span data-ttu-id="937eb-127"><span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**Norm \_ IgnoreKanaType**</span><span class="sxs-lookup"><span data-stu-id="937eb-127"><span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**NORM\_IGNOREKANATYPE**</span></span>


</dt> <dd>

<span data-ttu-id="937eb-128">Unterscheiden Sie nicht zwischen Hiragana-und Katakana-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="937eb-128">Do not differentiate between Hiragana and Katakana characters.</span></span> <span data-ttu-id="937eb-129">Die entsprechenden Hiragana-und Katakana-Zeichen vergleichen als gleich.</span><span class="sxs-lookup"><span data-stu-id="937eb-129">Corresponding Hiragana and Katakana characters compare as equal.</span></span>

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span data-ttu-id="937eb-130"><span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**Norm \_ ignoronspace**</span><span class="sxs-lookup"><span data-stu-id="937eb-130"><span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**NORM\_IGNORENONSPACE**</span></span>


</dt> <dd>

<span data-ttu-id="937eb-131">Zeichen ohne zwischen Raum ignorieren.</span><span class="sxs-lookup"><span data-stu-id="937eb-131">Ignore nonspacing characters.</span></span>

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span data-ttu-id="937eb-132"><span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**Norm \_ IgnoreSymbols**</span><span class="sxs-lookup"><span data-stu-id="937eb-132"><span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**NORM\_IGNORESYMBOLS**</span></span>


</dt> <dd>

<span data-ttu-id="937eb-133">Symbole ignorieren.</span><span class="sxs-lookup"><span data-stu-id="937eb-133">Ignore symbols.</span></span>

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span data-ttu-id="937eb-134"><span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**Norm \_ IgnoreWidth**</span><span class="sxs-lookup"><span data-stu-id="937eb-134"><span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**NORM\_IGNOREWIDTH**</span></span>


</dt> <dd>

<span data-ttu-id="937eb-135">Unterscheiden Sie nicht zwischen einem Einzel Byte Zeichen und demselben Zeichen als Doppelbyte Zeichen.</span><span class="sxs-lookup"><span data-stu-id="937eb-135">Do not differentiate between a single-byte character and the same character as a double-byte character.</span></span>

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span data-ttu-id="937eb-136"><span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**\_StringSort sortieren**</span><span class="sxs-lookup"><span data-stu-id="937eb-136"><span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**SORT\_STRINGSORT**</span></span>


</dt> <dd>

<span data-ttu-id="937eb-137">Interpunktions Zeichen werden wie Symbole behandelt.</span><span class="sxs-lookup"><span data-stu-id="937eb-137">Treat punctuation the same as symbols.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="937eb-138">*lpString1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="937eb-138">*lpString1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="937eb-139">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="937eb-139">Type: **LPCWSTR**</span></span>

<span data-ttu-id="937eb-140">Ein Zeiger auf die erste zu vergleichende Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="937eb-140">A pointer to the first Unicode string to be compared.</span></span>

</dd> <dt>

<span data-ttu-id="937eb-141">*cchCount1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="937eb-141">*cchCount1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="937eb-142">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="937eb-142">Type: **int**</span></span>

<span data-ttu-id="937eb-143">Die Anzahl der Zeichen in der Zeichenfolge, auf die durch den *lpString1* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="937eb-143">The number of characters in the string pointed to by the *lpString1* parameter.</span></span> <span data-ttu-id="937eb-144">Der Zähler umfasst nicht das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="937eb-144">The count does not include the terminating null character.</span></span> <span data-ttu-id="937eb-145">Wenn dieser Parameter ein negativer Wert ist, wird angenommen, dass die Zeichenfolge mit NULL endet, und die Länge wird automatisch berechnet.</span><span class="sxs-lookup"><span data-stu-id="937eb-145">If this parameter is a negative value, the string is assumed to be null-terminated and the length is calculated automatically.</span></span>

</dd> <dt>

<span data-ttu-id="937eb-146">*lpString2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="937eb-146">*lpString2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="937eb-147">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="937eb-147">Type: **LPCWSTR**</span></span>

<span data-ttu-id="937eb-148">Ein Zeiger auf die zweite zu vergleichende Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="937eb-148">A pointer to the second Unicode string to be compared.</span></span>

</dd> <dt>

<span data-ttu-id="937eb-149">*cchCount2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="937eb-149">*cchCount2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="937eb-150">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="937eb-150">Type: **int**</span></span>

<span data-ttu-id="937eb-151">Die Anzahl der Zeichen in der Zeichenfolge, auf die durch den *lpString2* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="937eb-151">The number of characters in the string pointed to by the *lpString2* parameter.</span></span> <span data-ttu-id="937eb-152">Der Zähler umfasst nicht das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="937eb-152">The count does not include the terminating null character.</span></span> <span data-ttu-id="937eb-153">Wenn dieser Parameter ein negativer Wert ist, wird angenommen, dass die Zeichenfolge mit NULL endet, und die Länge wird automatisch berechnet.</span><span class="sxs-lookup"><span data-stu-id="937eb-153">If this parameter is a negative value, the string is assumed to be null-terminated and the length is calculated automatically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="937eb-154">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="937eb-154">Return value</span></span>

<span data-ttu-id="937eb-155">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="937eb-155">Type: **int**</span></span>

<span data-ttu-id="937eb-156">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="937eb-156">If the function fails, the return value is zero.</span></span> <span data-ttu-id="937eb-157">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="937eb-157">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="937eb-158">" **GetLastError** " kann einen der folgenden Fehlercodes zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="937eb-158">**GetLastError** may return one of the following error codes.</span></span>

-   <span data-ttu-id="937eb-159">\_ungültige \_ Flags.</span><span class="sxs-lookup"><span data-stu-id="937eb-159">ERROR\_INVALID\_FLAGS</span></span>
-   <span data-ttu-id="937eb-160">Fehler bei \_ ungültigem \_ Parameter</span><span class="sxs-lookup"><span data-stu-id="937eb-160">ERROR\_INVALID\_PARAMETER</span></span>

<span data-ttu-id="937eb-161">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="937eb-161">If the function succeeds, the return value is one of the following values.</span></span> 

| <span data-ttu-id="937eb-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="937eb-162">Requirement</span></span> | <span data-ttu-id="937eb-163">Wert</span><span class="sxs-lookup"><span data-stu-id="937eb-163">Value</span></span> |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="937eb-164">CStr \_ kleiner \_ als</span><span class="sxs-lookup"><span data-stu-id="937eb-164">CSTR\_LESS\_THAN</span></span>    | <span data-ttu-id="937eb-165">Die Zeichenfolge, auf die der *lpString1* -Parameter verweist, ist weniger lexikalischer Wert als die Zeichenfolge, auf die der *lpString2* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="937eb-165">The string pointed to by the *lpString1* parameter is less in lexical value than the string pointed to by the *lpString2* parameter.</span></span> |
| <span data-ttu-id="937eb-166">CStr \_ gleich</span><span class="sxs-lookup"><span data-stu-id="937eb-166">CSTR\_EQUAL</span></span>         | <span data-ttu-id="937eb-167">Die Zeichenfolge, auf die von *lpString1* verwiesen wird, ist gleich dem lexikalischen Wert der Zeichenfolge, auf die von *lpString2* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="937eb-167">The string pointed to by *lpString1* is equal in lexical value to the string pointed to by *lpString2*.</span></span>                              |
| <span data-ttu-id="937eb-168">CStr \_ größer \_ als</span><span class="sxs-lookup"><span data-stu-id="937eb-168">CSTR\_GREATER\_THAN</span></span> | <span data-ttu-id="937eb-169">Die Zeichenfolge, auf die von *lpString1* verwiesen wird, ist im lexikalischen Wert größer als die Zeichenfolge, auf die *lpString2*</span><span class="sxs-lookup"><span data-stu-id="937eb-169">The string pointed to by *lpString1* is greater in lexical value than the string pointed to by *lpString2*</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="937eb-170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="937eb-170">Remarks</span></span>

<span data-ttu-id="937eb-171">**Sicherheitswarnung:** Wenn Sie diese Funktion falsch verwenden, kann die Sicherheit Ihrer Anwendung beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="937eb-171">**Security Warning:** Using this function incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="937eb-172">Zeichen folgen, die nicht ordnungsgemäß verglichen werden, können ungültige Eingaben verursachen.</span><span class="sxs-lookup"><span data-stu-id="937eb-172">Strings that are not compared correctly can produce invalid input.</span></span> <span data-ttu-id="937eb-173">Testen Sie Zeichen folgen, um sicherzustellen, dass Sie gültig sind, bevor Sie Sie verwenden und Fehlerhandler bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="937eb-173">Test strings to make sure they are valid before using them and provide error handlers.</span></span> <span data-ttu-id="937eb-174">Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](../intl/security-considerations--international-features.md)</span><span class="sxs-lookup"><span data-stu-id="937eb-174">For more information, see [Security Considerations: International Features](../intl/security-considerations--international-features.md)</span></span>

<span data-ttu-id="937eb-175">Die bevorzugte Methode ist die Verwendung von [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="937eb-175">The preferred method is to use [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="937eb-176">**Comparestringwrapw** muss direkt aus Shlwapi.dll aufgerufen werden. dabei wird die Ordnungszahl 45 verwendet.</span><span class="sxs-lookup"><span data-stu-id="937eb-176">**CompareStringWrapW** must be called directly from Shlwapi.dll, using ordinal 45.</span></span>

## <a name="requirements"></a><span data-ttu-id="937eb-177">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="937eb-177">Requirements</span></span>



| <span data-ttu-id="937eb-178">Anforderung</span><span class="sxs-lookup"><span data-stu-id="937eb-178">Requirement</span></span> | <span data-ttu-id="937eb-179">Wert</span><span class="sxs-lookup"><span data-stu-id="937eb-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="937eb-180">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="937eb-180">Minimum supported client</span></span><br/> | <span data-ttu-id="937eb-181">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="937eb-181">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="937eb-182">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="937eb-182">Minimum supported server</span></span><br/> | <span data-ttu-id="937eb-183">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="937eb-183">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="937eb-184">Header</span><span class="sxs-lookup"><span data-stu-id="937eb-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="937eb-185"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="937eb-185"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="937eb-186">DLL</span><span class="sxs-lookup"><span data-stu-id="937eb-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="937eb-187"><dt>Shlwapi.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="937eb-187"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="937eb-188">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="937eb-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="937eb-189">**CompareString**</span><span class="sxs-lookup"><span data-stu-id="937eb-189">**CompareString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 
