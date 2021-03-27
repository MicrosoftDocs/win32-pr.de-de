---
description: Formatiert die Zeit als Zeit Zeichenfolge für ein bestimmtes Gebiets Schema.
ms.assetid: 048b209c-f757-4b65-9ce7-282a5c21021f
title: Gettimeformatwrapw-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTimeFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 53f1bb88c2b3a79b58f3025daec31a7b1340b642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979648"
---
# <a name="gettimeformatwrapw-function"></a><span data-ttu-id="91a3c-103">Gettimeformatwrapw-Funktion</span><span class="sxs-lookup"><span data-stu-id="91a3c-103">GetTimeFormatWrapW function</span></span>

<span data-ttu-id="91a3c-104">\[**Gettimeformatwrapw** ist für die Verwendung in Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="91a3c-104">\[**GetTimeFormatWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="91a3c-105">Sie ist möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="91a3c-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="91a3c-106">Sie sollten [**gettimeformatw**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) an seiner Stelle verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="91a3c-106">You should use [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in its place.\]</span></span>

<span data-ttu-id="91a3c-107">Formatiert die Zeit als Zeit Zeichenfolge für ein bestimmtes Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="91a3c-107">Formats time as a time string for a specified locale.</span></span> <span data-ttu-id="91a3c-108">Die-Funktion formatiert entweder eine angegebene Zeit oder eine lokale Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="91a3c-108">The function formats either a specified time or the local system time.</span></span>

> [!Note]  
> <span data-ttu-id="91a3c-109">**Gettimeformatwrapw** ist ein Wrapper für die **gettimeformatw** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="91a3c-109">**GetTimeFormatWrapW** is a wrapper for the **GetTimeFormatW** function.</span></span> <span data-ttu-id="91a3c-110">Weitere Hinweise zur Verwendung finden Sie auf der Seite [**getTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .</span><span class="sxs-lookup"><span data-stu-id="91a3c-110">See the [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="91a3c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="91a3c-111">Syntax</span></span>


```C++
int GetTimeFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpTime,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzTimeStr,
  _In_        int        cchTime
);
```



## <a name="parameters"></a><span data-ttu-id="91a3c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="91a3c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91a3c-113">Gebiets Schema  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91a3c-113">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a3c-114">Typ: **LCID**</span><span class="sxs-lookup"><span data-stu-id="91a3c-114">Type: **LCID**</span></span>

<span data-ttu-id="91a3c-115">Gibt das Gebiets Schema an, für das die Zeit Zeichenfolge formatiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="91a3c-115">Specifies the locale for which the time string is to be formatted.</span></span> <span data-ttu-id="91a3c-116">Wenn *pwzformat* den Wert **null** hat, formatiert die Funktion die Zeichenfolge gemäß dem Zeitformat für dieses Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="91a3c-116">If *pwzFormat* is **NULL**, the function formats the string according to the time format for this locale.</span></span> <span data-ttu-id="91a3c-117">Wenn *pwzformat* nicht **null** ist, verwendet die Funktion das Gebiets Schema nur für Informationen, die nicht in der Format Bild Zeichenfolge angegeben sind (z. b. die Zeit Marker des Gebiets Schemas).</span><span class="sxs-lookup"><span data-stu-id="91a3c-117">If *pwzFormat* is not **NULL**, the function uses the locale only for information not specified in the format picture string (for example, the locale's time markers).</span></span>

<span data-ttu-id="91a3c-118">Bei diesem Parameter kann es sich um einen vom [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) -Makro erstellten Gebiets Schema Bezeichner oder einen der folgenden vordefinierten Werte handeln.</span><span class="sxs-lookup"><span data-stu-id="91a3c-118">This parameter can be a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro, or one of the following predefined values.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="91a3c-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**Standard für Gebiets Schema \_ System \_**</span><span class="sxs-lookup"><span data-stu-id="91a3c-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="91a3c-120">Standardsystem Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="91a3c-120">Default system locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="91a3c-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_Standardbenutzer Name für locale \_**</span><span class="sxs-lookup"><span data-stu-id="91a3c-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="91a3c-122">Standardbenutzer Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="91a3c-122">Default user locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="91a3c-123">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91a3c-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a3c-124">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="91a3c-124">Type: **DWORD**</span></span>

<span data-ttu-id="91a3c-125">Gibt verschiedene Funktions Optionen an.</span><span class="sxs-lookup"><span data-stu-id="91a3c-125">Specifies various function options.</span></span> <span data-ttu-id="91a3c-126">Sie können eine Kombination der folgenden Werte angeben.</span><span class="sxs-lookup"><span data-stu-id="91a3c-126">You can specify a combination of the following values.</span></span>

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span data-ttu-id="91a3c-127"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**Gebiets Schema \_ nouseroverride**</span><span class="sxs-lookup"><span data-stu-id="91a3c-127"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE\_NOUSEROVERRIDE**</span></span>


</dt> <dd>

<span data-ttu-id="91a3c-128">Wenn festgelegt, formatiert die Funktion die Zeichenfolge mit dem System Standard-Zeitformat für das angegebene Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="91a3c-128">If set, the function formats the string using the system default time format for the specified locale.</span></span> <span data-ttu-id="91a3c-129">Wenn nicht festgelegt, formatiert die Funktion die Zeichenfolge mithilfe von Benutzer Überschreibungen für das Standardzeit Format des Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="91a3c-129">If not set, the function formats the string using any user overrides to the locale's default time format.</span></span> <span data-ttu-id="91a3c-130">Dieses Flag kann nur festgelegt werden, wenn *pwzformat* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="91a3c-130">This flag can only be set if *pwzFormat* is **NULL**.</span></span>

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span data-ttu-id="91a3c-131"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**Gebiets Schema \_ verwenden \_ CP \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="91a3c-131"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALE\_USE\_CP\_ACP**</span></span>


</dt> <dd>

<span data-ttu-id="91a3c-132">Verwendet die ANSI-Codepage des Systems für die Zeichen folgen Übersetzung anstelle der Gebiets Schema-Codepage.</span><span class="sxs-lookup"><span data-stu-id="91a3c-132">Uses the system ANSI code page for string translation instead of the locale code page.</span></span>

</dd> <dt>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>

<span data-ttu-id="91a3c-133"><span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**Zeit ( \_ nominutesorseconds)**</span><span class="sxs-lookup"><span data-stu-id="91a3c-133"><span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**TIME\_NOMINUTESORSECONDS**</span></span>


</dt> <dd>

<span data-ttu-id="91a3c-134">Verwendet keine Minuten oder Sekunden.</span><span class="sxs-lookup"><span data-stu-id="91a3c-134">Does not use minutes or seconds.</span></span>

</dd> <dt>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>

<span data-ttu-id="91a3c-135"><span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**Zeit (in \_ Sekunden)**</span><span class="sxs-lookup"><span data-stu-id="91a3c-135"><span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**TIME\_NOSECONDS**</span></span>


</dt> <dd>

<span data-ttu-id="91a3c-136">Verwendet keine Sekunden.</span><span class="sxs-lookup"><span data-stu-id="91a3c-136">Does not use seconds.</span></span>

</dd> <dt>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>

<span data-ttu-id="91a3c-137"><span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**Zeit \_ notimemarker**</span><span class="sxs-lookup"><span data-stu-id="91a3c-137"><span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**TIME\_NOTIMEMARKER**</span></span>


</dt> <dd>

<span data-ttu-id="91a3c-138">Verwendet keinen Zeit Marker.</span><span class="sxs-lookup"><span data-stu-id="91a3c-138">Does not use a time marker.</span></span>

</dd> <dt>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>

<span data-ttu-id="91a3c-139"><span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**Zeit \_ FORCE24HOURFORMAT**</span><span class="sxs-lookup"><span data-stu-id="91a3c-139"><span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**TIME\_FORCE24HOURFORMAT**</span></span>


</dt> <dd>

<span data-ttu-id="91a3c-140">Verwendet immer ein 24-Stunden-Zeitformat.</span><span class="sxs-lookup"><span data-stu-id="91a3c-140">Always uses a 24-hour time format.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="91a3c-141">*lptime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91a3c-141">*lpTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a3c-142">Typ: \* Konstante *[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _</span><span class="sxs-lookup"><span data-stu-id="91a3c-142">Type: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)\** _</span></span>

<span data-ttu-id="91a3c-143">Ein Zeiger auf eine [_ *SYSTEMTIME* \*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die zu formatierenden Zeit Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="91a3c-143">A pointer to a [_ *SYSTEMTIME*\*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure that contains the time information to be formatted.</span></span> <span data-ttu-id="91a3c-144">Wenn dieser Zeiger **null** ist, verwendet die Funktion die aktuelle lokale Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="91a3c-144">If this pointer is **NULL**, the function uses the current local system time.</span></span>

</dd> <dt>

<span data-ttu-id="91a3c-145">*pwzformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91a3c-145">*pwzFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a3c-146">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="91a3c-146">Type: **LPCWSTR**</span></span>

<span data-ttu-id="91a3c-147">Ein Zeiger auf ein Format, das zum bilden der Zeit Zeichenfolge verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="91a3c-147">A pointer to a format to use to form the time string.</span></span> <span data-ttu-id="91a3c-148">Wenn *pwzformat* den Wert **null** hat, verwendet die Funktion das Zeitformat des angegebenen Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="91a3c-148">If *pwzFormat* is **NULL**, the function uses the time format of the specified locale.</span></span> <span data-ttu-id="91a3c-149">Weitere Informationen finden Sie unter [**getTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .</span><span class="sxs-lookup"><span data-stu-id="91a3c-149">See [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) for more details.</span></span>

</dd> <dt>

<span data-ttu-id="91a3c-150">*pwztimestr* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="91a3c-150">*pwzTimeStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91a3c-151">Typ: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="91a3c-151">Type: **LPWSTR**</span></span>

<span data-ttu-id="91a3c-152">Ein Zeiger auf einen Puffer, der die formatierte Zeit Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="91a3c-152">A pointer to a buffer that receives the formatted time string.</span></span>

</dd> <dt>

<span data-ttu-id="91a3c-153">*cchtime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91a3c-153">*cchTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a3c-154">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="91a3c-154">Type: **int**</span></span>

<span data-ttu-id="91a3c-155">Die Größe des *pwztimestr* -Puffers in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="91a3c-155">The size, in characters, of the *pwzTimeStr* buffer.</span></span> <span data-ttu-id="91a3c-156">Wenn *cchtime* NULL ist, gibt die Funktion die Anzahl der Zeichen zurück, die zum Speichern der formatierten Zeit Zeichenfolge erforderlich sind, und der Puffer, auf den *pwztimestr* zeigt, wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="91a3c-156">If *cchTime* is zero, the function returns the number of characters required to hold the formatted time string, and the buffer pointed to by *pwzTimeStr* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91a3c-157">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91a3c-157">Return value</span></span>

<span data-ttu-id="91a3c-158">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="91a3c-158">Type: **int**</span></span>

<span data-ttu-id="91a3c-159">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert die Anzahl der Zeichen, die in den Puffer geschrieben werden, auf den *pwztimestr* zeigt.</span><span class="sxs-lookup"><span data-stu-id="91a3c-159">If the function succeeds, the return value is the number of characters written to the buffer pointed to by *pwzTimeStr*.</span></span> <span data-ttu-id="91a3c-160">Wenn der *cchtime* -Parameter 0 (null) ist, ist der Rückgabewert die Anzahl von Zeichen, die für die formatierte Zeit Zeichenfolge erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="91a3c-160">If the *cchTime* parameter is zero, the return value is the number of characters required to hold the formatted time string.</span></span> <span data-ttu-id="91a3c-161">Die Anzahl schließt das abschließende Null Zeichen ein.</span><span class="sxs-lookup"><span data-stu-id="91a3c-161">The count includes the terminating null character.</span></span>

<span data-ttu-id="91a3c-162">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="91a3c-162">If the function fails, the return value is zero.</span></span> <span data-ttu-id="91a3c-163">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="91a3c-163">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="91a3c-164">" **GetLastError** " kann einen der folgenden Fehlercodes zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="91a3c-164">**GetLastError** may return one of the following error codes.</span></span>

<dl> <dt>

<span data-ttu-id="91a3c-165">**Fehler \_ beim \_ Puffer.**</span><span class="sxs-lookup"><span data-stu-id="91a3c-165">**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dt>

<span data-ttu-id="91a3c-166">**\_ungültige \_ Flags.**</span><span class="sxs-lookup"><span data-stu-id="91a3c-166">**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dt>

<span data-ttu-id="91a3c-167">**Fehler bei \_ ungültigem \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="91a3c-167">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="91a3c-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91a3c-168">Remarks</span></span>

<span data-ttu-id="91a3c-169">**Gettimeformatwrapw** bietet die Möglichkeit, Unicode-Zeichen folgen in älteren Betriebssystemen als Windows XP zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="91a3c-169">**GetTimeFormatWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="91a3c-170">Die bevorzugte Methode ist die Verwendung von [**gettimeformatw**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="91a3c-170">The preferred method is to use [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="91a3c-171">**Gettimeformatwrapw** muss direkt aus Shlwapi.dll aufgerufen werden, und zwar mithilfe von Ordnungszahl 310.</span><span class="sxs-lookup"><span data-stu-id="91a3c-171">**GetTimeFormatWrapW** must be called directly from Shlwapi.dll, using ordinal 310.</span></span>

## <a name="requirements"></a><span data-ttu-id="91a3c-172">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="91a3c-172">Requirements</span></span>



| <span data-ttu-id="91a3c-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91a3c-173">Requirement</span></span> | <span data-ttu-id="91a3c-174">Wert</span><span class="sxs-lookup"><span data-stu-id="91a3c-174">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91a3c-175">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91a3c-175">Minimum supported client</span></span><br/> | <span data-ttu-id="91a3c-176">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91a3c-176">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91a3c-177">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91a3c-177">Minimum supported server</span></span><br/> | <span data-ttu-id="91a3c-178">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91a3c-178">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="91a3c-179">DLL</span><span class="sxs-lookup"><span data-stu-id="91a3c-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91a3c-180"><dt>Shlwapi.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="91a3c-180"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91a3c-181">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="91a3c-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91a3c-182">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="91a3c-182">**GetTimeFormat**</span></span>](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)
</dt> </dl>

 

 
