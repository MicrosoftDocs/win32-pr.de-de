---
description: Formatiert ein Datum als Datums Zeichenfolge für ein angegebenes Gebiets Schema.
ms.assetid: e45f6d1c-2890-44f6-8406-022c99c59e02
title: Getdateformatwrapw-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDateFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: c9c369584fd15a27d5e684452b2277104b5b1da4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215948"
---
# <a name="getdateformatwrapw-function"></a><span data-ttu-id="d7189-103">Getdateformatwrapw-Funktion</span><span class="sxs-lookup"><span data-stu-id="d7189-103">GetDateFormatWrapW function</span></span>

<span data-ttu-id="d7189-104">\[**Getdateformatwrapw** ist für die Verwendung in Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d7189-104">\[**GetDateFormatWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="d7189-105">Sie wird in nachfolgenden Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="d7189-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="d7189-106">Sie sollten [**getdateformatw**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) an seiner Stelle verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="d7189-106">You should use [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in its place.\]</span></span>

<span data-ttu-id="d7189-107">Formatiert ein Datum als Datums Zeichenfolge für ein angegebenes Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="d7189-107">Formats a date as a date string for a specified locale.</span></span> <span data-ttu-id="d7189-108">Die-Funktion formatiert entweder ein bestimmtes Datum oder das lokale Systemdatum.</span><span class="sxs-lookup"><span data-stu-id="d7189-108">The function formats either a specified date or the local system date.</span></span>

> [!Note]  
> <span data-ttu-id="d7189-109">**Getdateformatwrapw** ist ein Wrapper für die **getdateformatw** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d7189-109">**GetDateFormatWrapW** is a wrapper for the **GetDateFormatW** function.</span></span> <span data-ttu-id="d7189-110">Weitere Hinweise zur Verwendung finden Sie auf der Seite " [**getDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) ".</span><span class="sxs-lookup"><span data-stu-id="d7189-110">See the [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d7189-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7189-111">Syntax</span></span>


```C++
int GetDateFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpDate,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzDateStr,
  _In_        int        cchDate
);
```



## <a name="parameters"></a><span data-ttu-id="d7189-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7189-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7189-113">Gebiets Schema  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7189-113">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7189-114">Typ: **LCID**</span><span class="sxs-lookup"><span data-stu-id="d7189-114">Type: **LCID**</span></span>

<span data-ttu-id="d7189-115">Das Gebiets Schema, für das die Datums Zeichenfolge formatiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7189-115">The locale for which the date string is to be formatted.</span></span> <span data-ttu-id="d7189-116">Wenn *pwzformat* den Wert **null** hat, formatiert die Funktion die Zeichenfolge gemäß dem Datumsformat für dieses Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="d7189-116">If *pwzFormat* is **NULL**, the function formats the string according to the date format for this locale.</span></span> <span data-ttu-id="d7189-117">Wenn *pwzformat* nicht **null** ist, verwendet die Funktion das Gebiets Schema nur für Informationen, die nicht in der Format Bild Zeichenfolge angegeben sind (z. b. die Tages-und Monatsnamen des Gebiets Schemas).</span><span class="sxs-lookup"><span data-stu-id="d7189-117">If *pwzFormat* is not **NULL**, the function uses the locale only for information not specified in the format picture string (for example, the locale's day and month names).</span></span>

<span data-ttu-id="d7189-118">Bei diesem Parameter kann es sich um einen vom [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) -Makro erstellten Gebiets Schema Bezeichner oder einen der folgenden vordefinierten Werte handeln.</span><span class="sxs-lookup"><span data-stu-id="d7189-118">This parameter can be a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro, or one of the following predefined values.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="d7189-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**Standard für Gebiets Schema \_ System \_**</span><span class="sxs-lookup"><span data-stu-id="d7189-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="d7189-120">Standardsystem Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="d7189-120">Default system locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="d7189-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_Standardbenutzer Name für locale \_**</span><span class="sxs-lookup"><span data-stu-id="d7189-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="d7189-122">Standardbenutzer Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="d7189-122">Default user locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d7189-123">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7189-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7189-124">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d7189-124">Type: **DWORD**</span></span>

<span data-ttu-id="d7189-125">Gibt verschiedene Funktions Optionen an.</span><span class="sxs-lookup"><span data-stu-id="d7189-125">Specifies various function options.</span></span> <span data-ttu-id="d7189-126">Wenn *pwzformat* nicht **null** ist, muss dieser Parameter NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d7189-126">If *pwzFormat* is not **NULL**, this parameter must be zero.</span></span> <span data-ttu-id="d7189-127">Wenn *pwzformat* **null** ist, können Sie eine Kombination der folgenden Werte angeben.</span><span class="sxs-lookup"><span data-stu-id="d7189-127">If *pwzFormat* is **NULL**, you can specify a combination of the following values.</span></span> <span data-ttu-id="d7189-128">Wenn Sie weder Date \_ yearMonth, Date \_ SHORTDATE noch Date \_ longDate angeben und *pwzformat* den Wert **null** hat, \_ wird Date SHORTDATE als Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7189-128">If you do not specify either DATE\_YEARMONTH, DATE\_SHORTDATE, or DATE\_LONGDATE, and *pwzFormat* is **NULL**, then DATE\_SHORTDATE is used as the default.</span></span>

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span data-ttu-id="d7189-129"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**Gebiets Schema \_ nouseroverride**</span><span class="sxs-lookup"><span data-stu-id="d7189-129"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE\_NOUSEROVERRIDE**</span></span>


</dt> <dd>

<span data-ttu-id="d7189-130">Wenn festgelegt, formatiert die Funktion die Zeichenfolge unter Verwendung des Standard Datums Formats des Systems für das angegebene Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="d7189-130">If set, the function formats the string using the system default date format for the specified locale.</span></span> <span data-ttu-id="d7189-131">Wenn nicht festgelegt, formatiert die Funktion die Zeichenfolge mithilfe von Benutzer Überschreibungen für das Standard Datumsformat des Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="d7189-131">If not set, the function formats the string using any user overrides to the locale's default date format.</span></span>

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span data-ttu-id="d7189-132"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**Gebiets Schema \_ verwenden \_ CP \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="d7189-132"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALE\_USE\_CP\_ACP**</span></span>


</dt> <dd>

<span data-ttu-id="d7189-133">Verwendet die ANSI-Codepage des Systems für die Zeichen folgen Übersetzung anstelle der Codepage des Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="d7189-133">Uses the system ANSI code page for string translation instead of the locale's code page.</span></span>

</dd> <dt>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>

<span data-ttu-id="d7189-134"><span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**Datum/ \_ kurzdatum**</span><span class="sxs-lookup"><span data-stu-id="d7189-134"><span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**DATE\_SHORTDATE**</span></span>


</dt> <dd>

<span data-ttu-id="d7189-135">Verwendet das kurze Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="d7189-135">Uses the short date format.</span></span> <span data-ttu-id="d7189-136">Dieser Wert kann nicht mit Date \_ longDate oder Date \_ yearMonth verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7189-136">This value cannot be used with DATE\_LONGDATE or DATE\_YEARMONTH.</span></span>

</dd> <dt>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>

<span data-ttu-id="d7189-137"><span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**Datum \_ longDate**</span><span class="sxs-lookup"><span data-stu-id="d7189-137"><span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**DATE\_LONGDATE**</span></span>


</dt> <dd>

<span data-ttu-id="d7189-138">Verwendet das lange Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="d7189-138">Uses the long date format.</span></span> <span data-ttu-id="d7189-139">Dieser Wert kann nicht mit Date \_ SHORTDATE oder Date \_ yearMonth verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7189-139">This value cannot be used with DATE\_SHORTDATE or DATE\_YEARMONTH.</span></span>

</dd> <dt>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>

<span data-ttu-id="d7189-140"><span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**Datum des \_ Monats**</span><span class="sxs-lookup"><span data-stu-id="d7189-140"><span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**DATE\_YEARMONTH**</span></span>


</dt> <dd>

<span data-ttu-id="d7189-141">Verwendet das Format Jahr/Monat.</span><span class="sxs-lookup"><span data-stu-id="d7189-141">Uses the year/month format.</span></span> <span data-ttu-id="d7189-142">Dieser Wert kann nicht mit Date \_ SHORTDATE oder Date \_ longDate verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7189-142">This value cannot be used with DATE\_SHORTDATE or DATE\_LONGDATE.</span></span>

</dd> <dt>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>

<span data-ttu-id="d7189-143"><span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**Datum der \_ Verwendung des \_ alt- \_ Kalenders**</span><span class="sxs-lookup"><span data-stu-id="d7189-143"><span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**DATE\_USE\_ALT\_CALENDAR**</span></span>


</dt> <dd>

<span data-ttu-id="d7189-144">Verwendet den alternativen Kalender, falls vorhanden, um die Datums Zeichenfolge zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="d7189-144">Uses the alternate calendar, if one exists, to format the date string.</span></span> <span data-ttu-id="d7189-145">Wenn dieses Flag festgelegt ist, verwendet die Funktion das Standardformat für diesen alternativen Kalender anstelle von Benutzer Überschreibungen.</span><span class="sxs-lookup"><span data-stu-id="d7189-145">If this flag is set, the function uses the default format for that alternate calendar, rather than using any user overrides.</span></span> <span data-ttu-id="d7189-146">Die Benutzer Überschreibungen werden nur in dem Fall verwendet, dass kein Standardformat für den angegebenen alternativen Kalender vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d7189-146">The user overrides will be used only in the event that there is no default format for the specified alternate calendar.</span></span>

</dd> <dt>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>

<span data-ttu-id="d7189-147"><span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**Datums- \_ ltrreading**</span><span class="sxs-lookup"><span data-stu-id="d7189-147"><span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**DATE\_LTRREADING**</span></span>


</dt> <dd>

<span data-ttu-id="d7189-148">Fügt Markierungen für das Lese Layout von links nach rechts hinzu.</span><span class="sxs-lookup"><span data-stu-id="d7189-148">Adds marks for left-to-right reading layout.</span></span> <span data-ttu-id="d7189-149">Dieser Wert kann nicht mit Date \_ RtlReading verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7189-149">This value cannot be used with DATE\_RTLREADING.</span></span>

</dd> <dt>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>

<span data-ttu-id="d7189-150"><span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**Datum \_ RtlReading**</span><span class="sxs-lookup"><span data-stu-id="d7189-150"><span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**DATE\_RTLREADING**</span></span>


</dt> <dd>

<span data-ttu-id="d7189-151">Fügt Markierungen für das Lese Layout von rechts nach Links hinzu.</span><span class="sxs-lookup"><span data-stu-id="d7189-151">Adds marks for right-to-left reading layout.</span></span> <span data-ttu-id="d7189-152">Dieser Wert kann nicht mit dem Datum \_ ltrreading verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7189-152">This value cannot be used with DATE\_LTRREADING.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d7189-153">*lpdate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7189-153">*lpDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7189-154">Typ: \* Konstante *[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _</span><span class="sxs-lookup"><span data-stu-id="d7189-154">Type: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)\** _</span></span>

<span data-ttu-id="d7189-155">Ein Zeiger auf eine [_ *SYSTEMTIME* \*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die Datumsinformationen enthält, die formatiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d7189-155">A pointer to a [_ *SYSTEMTIME*\*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date information to be formatted.</span></span> <span data-ttu-id="d7189-156">Wenn dieser Zeiger **null** ist, verwendet die Funktion das aktuelle lokale Systemdatum.</span><span class="sxs-lookup"><span data-stu-id="d7189-156">If this pointer is **NULL**, the function uses the current local system date.</span></span>

</dd> <dt>

<span data-ttu-id="d7189-157">*pwzformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7189-157">*pwzFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7189-158">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="d7189-158">Type: **LPCWSTR**</span></span>

<span data-ttu-id="d7189-159">Ein Zeiger auf ein Format Bild, das zum bilden der Datums Zeichenfolge verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7189-159">A pointer to a format picture to use to form the date string.</span></span> <span data-ttu-id="d7189-160">Wenn *pwzformat* den Wert **null** hat, verwendet die Funktion das Datumsformat des angegebenen Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="d7189-160">If *pwzFormat* is **NULL**, the function uses the date format of the specified locale.</span></span> <span data-ttu-id="d7189-161">Weitere Informationen finden Sie unter " [**getDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) ".</span><span class="sxs-lookup"><span data-stu-id="d7189-161">See [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) for more details.</span></span>

</dd> <dt>

<span data-ttu-id="d7189-162">*pwzdatestr* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d7189-162">*pwzDateStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7189-163">Typ: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="d7189-163">Type: **LPWSTR**</span></span>

<span data-ttu-id="d7189-164">Ein Zeiger auf einen Puffer, der die formatierte Datums Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="d7189-164">A pointer to a buffer that receives the formatted date string.</span></span>

</dd> <dt>

<span data-ttu-id="d7189-165">*cchdate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7189-165">*cchDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7189-166">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="d7189-166">Type: **int**</span></span>

<span data-ttu-id="d7189-167">Gibt die Größe des *pwzdatestr* -Puffers in Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="d7189-167">Specifies the size, in characters, of the *pwzDateStr* buffer.</span></span> <span data-ttu-id="d7189-168">Wenn *cchdate* NULL ist, gibt die Funktion die Anzahl von Zeichen zurück, die für die formatierte Datums Zeichenfolge erforderlich ist, und der Puffer, auf den *pwzdatestr* zeigt, wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7189-168">If *cchDate* is zero, the function returns the number of characters required to hold the formatted date string, and the buffer pointed to by *pwzDateStr* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7189-169">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7189-169">Return value</span></span>

<span data-ttu-id="d7189-170">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="d7189-170">Type: **int**</span></span>

<span data-ttu-id="d7189-171">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert die Anzahl der Zeichen, die in den Puffer geschrieben werden, auf den *pwzdatestr* zeigt.</span><span class="sxs-lookup"><span data-stu-id="d7189-171">If the function succeeds, the return value is the number of characters written to the buffer pointed to by *pwzDateStr*.</span></span> <span data-ttu-id="d7189-172">Wenn der *cchdate* -Parameter 0 (null) ist, ist der Rückgabewert die Anzahl von Zeichen, die für die formatierte Datums Zeichenfolge erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d7189-172">If the *cchDate* parameter is zero, the return value is the number of characters required to hold the formatted date string.</span></span> <span data-ttu-id="d7189-173">Die Anzahl schließt das abschließende Null Zeichen ein.</span><span class="sxs-lookup"><span data-stu-id="d7189-173">The count includes the terminating null character.</span></span>

<span data-ttu-id="d7189-174">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="d7189-174">If the function fails, the return value is zero.</span></span> <span data-ttu-id="d7189-175">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="d7189-175">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="d7189-176">" **GetLastError** " kann einen der folgenden Fehlercodes zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d7189-176">**GetLastError** may return one of the following error codes.</span></span>

<dl> <dt>

<span data-ttu-id="d7189-177">**Fehler \_ beim \_ Puffer.**</span><span class="sxs-lookup"><span data-stu-id="d7189-177">**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dt>

<span data-ttu-id="d7189-178">**\_ungültige \_ Flags.**</span><span class="sxs-lookup"><span data-stu-id="d7189-178">**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dt>

<span data-ttu-id="d7189-179">**Fehler bei \_ ungültigem \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="d7189-179">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d7189-180">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7189-180">Remarks</span></span>

<span data-ttu-id="d7189-181">**Getdateformatwrapw** bietet die Möglichkeit, Unicode-Zeichen folgen in älteren Betriebssystemen als Windows XP zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7189-181">**GetDateFormatWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="d7189-182">Die bevorzugte Methode ist die Verwendung von [**getdateformatw**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="d7189-182">The preferred method is to use [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="d7189-183">**Getdateformatwrapw** muss direkt aus Shlwapi.dll aufgerufen werden, und zwar mithilfe von Ordnungszahl 311.</span><span class="sxs-lookup"><span data-stu-id="d7189-183">**GetDateFormatWrapW** must be called directly from Shlwapi.dll, using ordinal 311.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7189-184">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d7189-184">Requirements</span></span>



| <span data-ttu-id="d7189-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7189-185">Requirement</span></span> | <span data-ttu-id="d7189-186">Wert</span><span class="sxs-lookup"><span data-stu-id="d7189-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7189-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7189-187">Minimum supported client</span></span><br/> | <span data-ttu-id="d7189-188">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7189-188">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7189-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7189-189">Minimum supported server</span></span><br/> | <span data-ttu-id="d7189-190">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7189-190">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d7189-191">DLL</span><span class="sxs-lookup"><span data-stu-id="d7189-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7189-192"><dt>Shlwapi.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="d7189-192"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7189-193">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d7189-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7189-194">**GetDateFormat**</span><span class="sxs-lookup"><span data-stu-id="d7189-194">**GetDateFormat**</span></span>](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> </dl>

 

 
