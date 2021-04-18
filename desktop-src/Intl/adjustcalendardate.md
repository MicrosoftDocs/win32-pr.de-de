---
description: Veraltet. Passt ein Datum an eine angegebene Anzahl von Jahren, Monaten, Wochen oder Tagen an.
ms.assetid: be8d61fd-efa3-4386-969f-30216c282ebc
title: "\"-Funktion\""
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdjustCalendarDate
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: ce2f61fd7d7d6354130873b5b2b2376c856e3958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345691"
---
# <a name="adjustcalendardate-function"></a><span data-ttu-id="b3fd0-104">"-Funktion"</span><span class="sxs-lookup"><span data-stu-id="b3fd0-104">AdjustCalendarDate function</span></span>

<span data-ttu-id="b3fd0-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-105">Deprecated.</span></span> <span data-ttu-id="b3fd0-106">Passt ein Datum an eine angegebene Anzahl von Jahren, Monaten, Wochen oder Tagen an.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-106">Adjusts a date by a specified number of years, months, weeks, or days.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3fd0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3fd0-107">Syntax</span></span>


```C++
BOOL AdjustCalendarDate(
  _Inout_ LPCALDATETIME        lpCalDateTime,
  _In_    CALDATETIME_DATEUNIT calUnit,
  _Out_   INT                  amount
);
```



## <a name="parameters"></a><span data-ttu-id="b3fd0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3fd0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3fd0-109">*lpcaldatetime* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b3fd0-109">*lpCalDateTime* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fd0-110">Ein Zeiger auf eine [**caldatetime**](caldatetime.md) -Struktur, die die Datums-und Kalenderinformationen enthält, die angepasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-110">Pointer to a [**CALDATETIME**](caldatetime.md) structure that contains the date and calendar information to adjust.</span></span>

</dd> <dt>

<span data-ttu-id="b3fd0-111">*calunit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3fd0-111">*calUnit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fd0-112">Der [**\_ dateunit**](caldatetime-dateunit.md) -Enumerationswert caldatetime, der die Datums Einheit angibt, z. b. dayunit.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-112">The [**CALDATETIME\_DATEUNIT**](caldatetime-dateunit.md) enumeration value indicating the date unit, for example, DayUnit.</span></span>

</dd> <dt>

<span data-ttu-id="b3fd0-113">*Betrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b3fd0-113">*amount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fd0-114">Der Betrag, um den das angegebene Datum angepasst werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-114">The amount by which to adjust the specified date.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3fd0-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3fd0-115">Return value</span></span>

<span data-ttu-id="b3fd0-116">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="b3fd0-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="b3fd0-117">Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:</span><span class="sxs-lookup"><span data-stu-id="b3fd0-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="b3fd0-118">das Fehler \_ Datum liegt \_ außerhalb des zulässigen \_ \_ Bereichs.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-118">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="b3fd0-119">Das angegebene Datum lag außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-119">The specified date was out of range.</span></span>
-   <span data-ttu-id="b3fd0-120">Fehler \_ : Ungültiger \_ Parameter.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-120">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="b3fd0-121">Jeder Parameterwert war ungültig.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-121">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3fd0-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3fd0-122">Remarks</span></span>

<span data-ttu-id="b3fd0-123">Diese Funktion verfügt über keine zugeordnete Header Datei oder Bibliotheksdatei.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-123">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="b3fd0-124">Die Anwendung kann [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen (Kernel32.dll) aufzurufen, um ein Modul Handle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-124">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="b3fd0-125">Anschließend kann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit dem Modul Handle und dem Namen dieser Funktion aufgerufen werden, um die Funktions Adresse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-125">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3fd0-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3fd0-126">Requirements</span></span>



| <span data-ttu-id="b3fd0-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3fd0-127">Requirement</span></span> | <span data-ttu-id="b3fd0-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b3fd0-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3fd0-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3fd0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b3fd0-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3fd0-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b3fd0-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3fd0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b3fd0-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3fd0-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3fd0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b3fd0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3fd0-134"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3fd0-134"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3fd0-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3fd0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3fd0-136">Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="b3fd0-136">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="b3fd0-137">Funktionen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="b3fd0-137">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="b3fd0-138">NLS: Beispiel für namensbasierte APIs</span><span class="sxs-lookup"><span data-stu-id="b3fd0-138">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
