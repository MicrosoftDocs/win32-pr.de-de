---
description: Veraltet.
ms.assetid: eb2622bc-a98d-42bd-ab59-7a849000d79d
title: Getcalendardateformatex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarDateFormatEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: b0130bf62c742d0565b1c98c138ac8c71ddf7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356192"
---
# <a name="getcalendardateformatex-function"></a><span data-ttu-id="187d4-103">Getcalendardateformatex-Funktion</span><span class="sxs-lookup"><span data-stu-id="187d4-103">GetCalendarDateFormatEx function</span></span>

<span data-ttu-id="187d4-104">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="187d4-104">Deprecated.</span></span> <span data-ttu-id="187d4-105">Ruft mit dem angegebenen Datum und Kalender eine ordnungsgemäß formatierte Datums Zeichenfolge für das angegebene Gebiets Schema ab.</span><span class="sxs-lookup"><span data-stu-id="187d4-105">Retrieves a properly formatted date string for the specified locale using the specified date and calendar.</span></span> <span data-ttu-id="187d4-106">Der Benutzer kann das kurze Datumsformat, das lange Datumsformat, das Format des Jahres Monats oder ein benutzerdefiniertes Format Muster angeben.</span><span class="sxs-lookup"><span data-stu-id="187d4-106">The user can specify the short date format, the long date format, the year month format, or a custom format pattern.</span></span>

> [!Note]  
> <span data-ttu-id="187d4-107">Diese Funktion kann z. b. aufgrund eines benutzerdefinierten Gebiets Schemas Daten abrufen, die sich zwischen Releases ändern.</span><span class="sxs-lookup"><span data-stu-id="187d4-107">This function can retrieve data that changes between releases, for example, due to a custom locale.</span></span> <span data-ttu-id="187d4-108">Wenn Ihre Anwendung Daten beibehalten oder übertragen muss, finden Sie weitere Informationen unter [Verwenden von permanenten](using-persistent-locale-data.md)Gebiets Schema Daten.</span><span class="sxs-lookup"><span data-stu-id="187d4-108">If your application must persist or transmit data, see [Using Persistent Locale Data](using-persistent-locale-data.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="187d4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="187d4-109">Syntax</span></span>


```C++
BOOL GetCalendarDateFormatEx(
  _In_        LPCWSTR       lpszLocale,
  _In_        DWORD         dwFlags,
  _In_  const LPCALDATETIME lpCalDateTime,
  _In_        LPCWSTR       lpFormat,
  _Out_       LPWSTR        lpDateStr,
  _In_        int           cchDate
);
```



## <a name="parameters"></a><span data-ttu-id="187d4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="187d4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="187d4-111">*lpszlocale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="187d4-111">*lpszLocale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="187d4-112">Zeiger auf einen Gebiets Schema Namen oder einen der folgenden vordefinierten Werte.</span><span class="sxs-lookup"><span data-stu-id="187d4-112">Pointer to a locale name, or one of the following predefined values.</span></span>

-   [<span data-ttu-id="187d4-113">Gebiets Schema \_ Name \_ invariant</span><span class="sxs-lookup"><span data-stu-id="187d4-113">LOCALE\_NAME\_INVARIANT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="187d4-114">Standardwert des Gebiets Schema \_ namens \_ Systems \_</span><span class="sxs-lookup"><span data-stu-id="187d4-114">LOCALE\_NAME\_SYSTEM\_DEFAULT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="187d4-115">\_Standard Name \_ des Gebiets Schemas \_</span><span class="sxs-lookup"><span data-stu-id="187d4-115">LOCALE\_NAME\_USER\_DEFAULT</span></span>](locale-name-constants.md)

</dd> <dt>

<span data-ttu-id="187d4-116">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="187d4-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="187d4-117">Flags, die Datumsformat Optionen angeben.</span><span class="sxs-lookup"><span data-stu-id="187d4-117">Flags specifying date format options.</span></span> <span data-ttu-id="187d4-118">Wenn *lpformat* nicht auf **null** festgelegt ist, muss dieser Parameter auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="187d4-118">If *lpFormat* is not set to **NULL**, this parameter must be set to 0.</span></span> <span data-ttu-id="187d4-119">Wenn *lpformat* auf **null** festgelegt ist, kann die Anwendung eine Kombination der folgenden Werte und [locale \_ nouseroverride](locale-nouseroverride.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="187d4-119">If *lpFormat* is set to **NULL**, the application can specify a combination of the following values and [LOCALE\_NOUSEROVERRIDE](locale-nouseroverride.md).</span></span>



| <span data-ttu-id="187d4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="187d4-120">Value</span></span>                                                                                                                                                               | <span data-ttu-id="187d4-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="187d4-121">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <span data-ttu-id="187d4-122"><dt>**Datum/ \_ kurzdatum**</dt></span><span class="sxs-lookup"><span data-stu-id="187d4-122"><dt>**DATE\_SHORTDATE**</dt></span></span> </dl>    | <span data-ttu-id="187d4-123">Verwenden Sie das kurze Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="187d4-123">Use the short date format.</span></span> <span data-ttu-id="187d4-124">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="187d4-124">This is the default.</span></span> <span data-ttu-id="187d4-125">Dieser Wert kann nicht mit Date \_ longDate oder Date \_ yearMonth verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="187d4-125">This value cannot be used with DATE\_LONGDATE or DATE\_YEARMONTH.</span></span> <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <span data-ttu-id="187d4-126"><dt>**Datum \_ longDate**</dt></span><span class="sxs-lookup"><span data-stu-id="187d4-126"><dt>**DATE\_LONGDATE**</dt></span></span> </dl>       | <span data-ttu-id="187d4-127">Verwenden Sie das lange Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="187d4-127">Use the long date format.</span></span> <span data-ttu-id="187d4-128">Dieser Wert kann nicht mit Date \_ SHORTDATE oder Date \_ yearMonth verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="187d4-128">This value cannot be used with DATE\_SHORTDATE or DATE\_YEARMONTH.</span></span> <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <span data-ttu-id="187d4-129"><dt>**Datum des \_ Monats**</dt></span><span class="sxs-lookup"><span data-stu-id="187d4-129"><dt>**DATE\_YEARMONTH**</dt></span></span> </dl>    | <span data-ttu-id="187d4-130">Verwenden Sie das Format Jahr/Monat.</span><span class="sxs-lookup"><span data-stu-id="187d4-130">Use the year/month format.</span></span> <span data-ttu-id="187d4-131">Dieser Wert kann nicht mit Date \_ SHORTDATE oder Date \_ longDate verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="187d4-131">This value cannot be used with DATE\_SHORTDATE or DATE\_LONGDATE.</span></span><br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <span data-ttu-id="187d4-132"><dt>**Datums- \_ ltrreading**</dt></span><span class="sxs-lookup"><span data-stu-id="187d4-132"><dt>**DATE\_LTRREADING**</dt></span></span> </dl> | <span data-ttu-id="187d4-133">Fügen Sie Markierungen für das Lese Layout von links nach rechts hinzu.</span><span class="sxs-lookup"><span data-stu-id="187d4-133">Add marks for left-to-right reading layout.</span></span> <span data-ttu-id="187d4-134">Dieser Wert kann nicht mit Date \_ RtlReading verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="187d4-134">This value cannot be used with DATE\_RTLREADING.</span></span><br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <span data-ttu-id="187d4-135"><dt>**Datum \_ RtlReading**</dt></span><span class="sxs-lookup"><span data-stu-id="187d4-135"><dt>**DATE\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="187d4-136">Fügen Sie Markierungen für das Lese Layout von rechts nach Links hinzu.</span><span class="sxs-lookup"><span data-stu-id="187d4-136">Add marks for right-to-left reading layout.</span></span> <span data-ttu-id="187d4-137">Dieser Wert kann nicht mit dem Datum \_ ltrreading verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="187d4-137">This value cannot be used with DATE\_LTRREADING</span></span><br/>                        |



 

</dd> <dt>

<span data-ttu-id="187d4-138">*lpcaldatetime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="187d4-138">*lpCalDateTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="187d4-139">Zeiger auf eine [**caldatetime**](caldatetime.md) -Struktur, die die Datums-und Kalenderinformationen enthält, die formatiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="187d4-139">Pointer to a [**CALDATETIME**](caldatetime.md) structure that contains the date and calendar information to format.</span></span>

</dd> <dt>

<span data-ttu-id="187d4-140">*lpformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="187d4-140">*lpFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="187d4-141">Zeiger auf eine Format Bild Zeichenfolge, die verwendet wird, um die Datums Zeichenfolge zu bilden.</span><span class="sxs-lookup"><span data-stu-id="187d4-141">Pointer to a format picture string that is used to form the date string.</span></span> <span data-ttu-id="187d4-142">Mögliche Werte für die Format Bild Zeichenfolge werden im [Format "Tag", "Month", "Year" und "ERA](day--month--year--and-era-format-pictures.md)" definiert.</span><span class="sxs-lookup"><span data-stu-id="187d4-142">Possible values for the format picture string are defined in [Day, Month, Year, and Era Format Pictures](day--month--year--and-era-format-pictures.md).</span></span>

<span data-ttu-id="187d4-143">Die Format Bild Zeichenfolge muss auf Null enden.</span><span class="sxs-lookup"><span data-stu-id="187d4-143">The format picture string must be null-terminated.</span></span> <span data-ttu-id="187d4-144">Die-Funktion verwendet das Gebiets Schema nur für Informationen, die nicht in der Format Bild Zeichenfolge angegeben sind, z. b. die Namen des Tags und Monats für das Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="187d4-144">The function uses the locale only for information not specified in the format picture string, for example, the day and month names for the locale.</span></span> <span data-ttu-id="187d4-145">Die Anwendung legt diesen Parameter auf **null** fest, wenn die Funktion das Datumsformat des angegebenen Gebiets Schemas verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="187d4-145">The application sets this parameter to **NULL** if the function is to use the date format of the specified locale.</span></span>

</dd> <dt>

<span data-ttu-id="187d4-146">*lpdatestr* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="187d4-146">*lpDateStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="187d4-147">Zeiger auf einen Puffer, in dem diese Funktion die formatierte Datums Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="187d4-147">Pointer to a buffer in which this function receives the formatted date string.</span></span>

</dd> <dt>

<span data-ttu-id="187d4-148">*cchdate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="187d4-148">*cchDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="187d4-149">Größe des *lpdatestr* -Puffers in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="187d4-149">Size, in characters, of the *lpDateStr* buffer.</span></span> <span data-ttu-id="187d4-150">Alternativ kann die Anwendung diesen Parameter auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="187d4-150">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="187d4-151">In diesem Fall gibt die Funktion die Anzahl der Zeichen zurück, die zum Speichern der formatierten Datums Zeichenfolge erforderlich sind, und der *lpdatestr* -Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="187d4-151">In this case, the function returns the number of characters required to hold the formatted date string, and the *lpDateStr* parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="187d4-152">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="187d4-152">Return value</span></span>

<span data-ttu-id="187d4-153">Gibt die Anzahl der Zeichen zurück, die bei erfolgreicher Ausführung in den *lpdatestr* -Puffer geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="187d4-153">Returns the number of characters written to the *lpDateStr* buffer if successful.</span></span> <span data-ttu-id="187d4-154">Wenn der *cchdate* -Parameter auf 0 festgelegt ist, gibt die Funktion die Anzahl der Zeichen zurück, die zum Speichern der formatierten Datums Zeichenfolge erforderlich sind, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="187d4-154">If the *cchDate* parameter is set to 0, the function returns the number of characters required to hold the formatted date string, including the terminating null character.</span></span>

<span data-ttu-id="187d4-155">Diese Funktion gibt 0 (null) zurück, wenn Sie nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="187d4-155">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="187d4-156">Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:</span><span class="sxs-lookup"><span data-stu-id="187d4-156">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="187d4-157">das Fehler \_ Datum liegt \_ außerhalb des zulässigen \_ \_ Bereichs.</span><span class="sxs-lookup"><span data-stu-id="187d4-157">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="187d4-158">Das angegebene Datum lag außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="187d4-158">The specified date was out of range.</span></span>
-   <span data-ttu-id="187d4-159">Fehler \_ beim \_ Puffer.</span><span class="sxs-lookup"><span data-stu-id="187d4-159">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="187d4-160">Eine angegebene Puffergröße war nicht groß genug, oder Sie wurde falsch auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="187d4-160">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="187d4-161">\_ungültige \_ Flags.</span><span class="sxs-lookup"><span data-stu-id="187d4-161">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="187d4-162">Die für Flags angegebenen Werte waren ungültig.</span><span class="sxs-lookup"><span data-stu-id="187d4-162">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="187d4-163">Fehler \_ : Ungültiger \_ Parameter.</span><span class="sxs-lookup"><span data-stu-id="187d4-163">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="187d4-164">Jeder Parameterwert war ungültig.</span><span class="sxs-lookup"><span data-stu-id="187d4-164">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="187d4-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="187d4-165">Remarks</span></span>

<span data-ttu-id="187d4-166">Das früheste von dieser Funktion unterstützte Datum ist der 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="187d4-166">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="187d4-167">Diese Funktion verfügt über keine zugeordnete Header Datei oder Bibliotheksdatei.</span><span class="sxs-lookup"><span data-stu-id="187d4-167">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="187d4-168">Die Anwendung kann [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen (Kernel32.dll) aufzurufen, um ein Modul Handle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="187d4-168">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="187d4-169">Anschließend kann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modul Handle und dem Namen dieser Funktion aufgerufen werden, um die Funktions Adresse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="187d4-169">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="187d4-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="187d4-170">Requirements</span></span>



| <span data-ttu-id="187d4-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="187d4-171">Requirement</span></span> | <span data-ttu-id="187d4-172">Wert</span><span class="sxs-lookup"><span data-stu-id="187d4-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="187d4-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="187d4-173">Minimum supported client</span></span><br/> | <span data-ttu-id="187d4-174">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="187d4-174">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="187d4-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="187d4-175">Minimum supported server</span></span><br/> | <span data-ttu-id="187d4-176">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="187d4-176">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="187d4-177">DLL</span><span class="sxs-lookup"><span data-stu-id="187d4-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="187d4-178"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="187d4-178"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="187d4-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="187d4-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="187d4-180">Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="187d4-180">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="187d4-181">Funktionen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="187d4-181">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="187d4-182">Format Abbildungen für Tag, Monat, Jahr und ERA</span><span class="sxs-lookup"><span data-stu-id="187d4-182">Day, Month, Year, and Era Format Pictures</span></span>](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[<span data-ttu-id="187d4-183">NLS: Beispiel für namensbasierte APIs</span><span class="sxs-lookup"><span data-stu-id="187d4-183">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> <dt>

[<span data-ttu-id="187d4-184">**Enumdateformatsexex**</span><span class="sxs-lookup"><span data-stu-id="187d4-184">**EnumDateFormatsExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[<span data-ttu-id="187d4-185">**GetDateFormat**</span><span class="sxs-lookup"><span data-stu-id="187d4-185">**GetDateFormat**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[<span data-ttu-id="187d4-186">**GetDateFormatEx**</span><span class="sxs-lookup"><span data-stu-id="187d4-186">**GetDateFormatEx**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[<span data-ttu-id="187d4-187">**Caldatetime**</span><span class="sxs-lookup"><span data-stu-id="187d4-187">**CALDATETIME**</span></span>](caldatetime.md)
</dt> </dl>

 

 
