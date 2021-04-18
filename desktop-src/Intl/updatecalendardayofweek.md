---
description: Veraltet. Ruft den Wochentag ab, der einem angegebenen Tag entspricht, und füllt den DayOfWeek-Member in der angegebenen caldatetime-Struktur mit diesem Wert auf.
ms.assetid: b9ae250a-73bb-4ec2-bb0d-e1f8b25c173c
title: Updatecalendardayosweek-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateCalendarDayOfWeek
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 316af539e6ca0476f0f8d575a160fcd7c3219e90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354852"
---
# <a name="updatecalendardayofweek-function"></a><span data-ttu-id="cde0b-104">Updatecalendardayosweek-Funktion</span><span class="sxs-lookup"><span data-stu-id="cde0b-104">UpdateCalendarDayOfWeek function</span></span>

<span data-ttu-id="cde0b-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="cde0b-105">Deprecated.</span></span> <span data-ttu-id="cde0b-106">Ruft den Wochentag ab, der einem angegebenen Tag entspricht, und füllt den **DayOfWeek** -Member in der angegebenen [**caldatetime**](caldatetime.md) -Struktur mit diesem Wert auf.</span><span class="sxs-lookup"><span data-stu-id="cde0b-106">Gets the day of the week that corresponds to a specified day and populates the **DayOfWeek** member in the specified [**CALDATETIME**](caldatetime.md) structure with that value.</span></span>

## <a name="syntax"></a><span data-ttu-id="cde0b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cde0b-107">Syntax</span></span>


```C++
BOOL UpdateCalendarDayOfWeek(
  _Inout_ LPCALDATETIME lpCalDateTime
);
```



## <a name="parameters"></a><span data-ttu-id="cde0b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cde0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cde0b-109">*lpcaldatetime* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cde0b-109">*lpCalDateTime* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cde0b-110">Ein Zeiger auf die [**caldatetime**](caldatetime.md) -Struktur, die das Datum enthält, für das der Wochentag festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cde0b-110">Pointer to the [**CALDATETIME**](caldatetime.md) structure containing the date for which to set the day of the week.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cde0b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cde0b-111">Return value</span></span>

<span data-ttu-id="cde0b-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="cde0b-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="cde0b-113">Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:</span><span class="sxs-lookup"><span data-stu-id="cde0b-113">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="cde0b-114">das Fehler \_ Datum liegt \_ außerhalb des zulässigen \_ \_ Bereichs.</span><span class="sxs-lookup"><span data-stu-id="cde0b-114">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="cde0b-115">Das angegebene Datum lag außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="cde0b-115">The specified date was out of range.</span></span>
-   <span data-ttu-id="cde0b-116">Fehler \_ : Ungültiger \_ Parameter.</span><span class="sxs-lookup"><span data-stu-id="cde0b-116">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="cde0b-117">Jeder Parameterwert war ungültig.</span><span class="sxs-lookup"><span data-stu-id="cde0b-117">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="cde0b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cde0b-118">Remarks</span></span>

<span data-ttu-id="cde0b-119">Diese Funktion verfügt über keine zugeordnete Header Datei oder Bibliotheksdatei.</span><span class="sxs-lookup"><span data-stu-id="cde0b-119">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="cde0b-120">Die Anwendung kann [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen (Kernel32.dll) aufzurufen, um ein Modul Handle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cde0b-120">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="cde0b-121">Anschließend kann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modul Handle und dem Namen dieser Funktion aufgerufen werden, um die Funktions Adresse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cde0b-121">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="cde0b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cde0b-122">Requirements</span></span>



| <span data-ttu-id="cde0b-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cde0b-123">Requirement</span></span> | <span data-ttu-id="cde0b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="cde0b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cde0b-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cde0b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cde0b-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cde0b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cde0b-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cde0b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cde0b-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cde0b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cde0b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cde0b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cde0b-130"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cde0b-130"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cde0b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cde0b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde0b-132">Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="cde0b-132">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="cde0b-133">Funktionen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="cde0b-133">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="cde0b-134">**Caldatetime**</span><span class="sxs-lookup"><span data-stu-id="cde0b-134">**CALDATETIME**</span></span>](caldatetime.md)
</dt> </dl>

 

 
