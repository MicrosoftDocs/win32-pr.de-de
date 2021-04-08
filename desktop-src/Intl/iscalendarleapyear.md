---
description: Veraltet. Gibt an, ob das angegebene Jahr ein Schaltjahr innerhalb des angegebenen Zeitraums für den jeweiligen Kalender ist.
ms.assetid: 91f58915-f0c6-4c7a-9d9a-96e255d799fd
title: Iscalendarleapyear-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCalendarLeapYear
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 484531f8107bacb70f9e24ba2537090317825e26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865491"
---
# <a name="iscalendarleapyear-function"></a><span data-ttu-id="97212-104">Iscalendarleapyear-Funktion</span><span class="sxs-lookup"><span data-stu-id="97212-104">IsCalendarLeapYear function</span></span>

<span data-ttu-id="97212-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="97212-105">Deprecated.</span></span> <span data-ttu-id="97212-106">Gibt an, ob das angegebene Jahr ein Schaltjahr innerhalb des angegebenen Zeitraums für den jeweiligen Kalender ist.</span><span class="sxs-lookup"><span data-stu-id="97212-106">Identifies whether the specified year is a leap year within the given era for the specific calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="97212-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="97212-107">Syntax</span></span>


```C++
BOOL IsCalendarLeapYear(
  _In_ CALID calId,
  _In_ UINT  year,
  _In_ UINT  era
);
```



## <a name="parameters"></a><span data-ttu-id="97212-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="97212-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97212-109">*Calid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97212-109">*calId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97212-110">Der für die Überprüfung des Schalt Jahrs zu verwendende [Kalender Bezeichner](calendar-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="97212-110">The [calendar identifier](calendar-identifiers.md) to use for checking leap year.</span></span>

</dd> <dt>

<span data-ttu-id="97212-111">*Jahr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97212-111">*year* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97212-112">Das zu überprüfen Jahr.</span><span class="sxs-lookup"><span data-stu-id="97212-112">The year to check.</span></span>

</dd> <dt>

<span data-ttu-id="97212-113"> Zeitraum \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97212-113">*era* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97212-114">Der Zeitraum, der überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="97212-114">The era to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97212-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97212-115">Return value</span></span>

<span data-ttu-id="97212-116">Gibt **true** zurück, wenn das angegebene Jahr ein Schaltjahr ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="97212-116">Returns **TRUE** if the specified year is a leap year, or **FALSE** otherwise.</span></span> <span data-ttu-id="97212-117">Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:</span><span class="sxs-lookup"><span data-stu-id="97212-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="97212-118">Fehler \_ : Ungültiger \_ Parameter.</span><span class="sxs-lookup"><span data-stu-id="97212-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="97212-119">Jeder Parameterwert war ungültig.</span><span class="sxs-lookup"><span data-stu-id="97212-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="97212-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97212-120">Remarks</span></span>

<span data-ttu-id="97212-121">Diese Funktion verfügt über keine zugeordnete Header Datei oder Bibliotheksdatei.</span><span class="sxs-lookup"><span data-stu-id="97212-121">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="97212-122">Die Anwendung kann [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen (Kernel32.dll) aufzurufen, um ein Modul Handle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="97212-122">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="97212-123">Anschließend kann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modul Handle und dem Namen dieser Funktion aufgerufen werden, um die Funktions Adresse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="97212-123">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="97212-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97212-124">Requirements</span></span>



| <span data-ttu-id="97212-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97212-125">Requirement</span></span> | <span data-ttu-id="97212-126">Wert</span><span class="sxs-lookup"><span data-stu-id="97212-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97212-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97212-127">Minimum supported client</span></span><br/> | <span data-ttu-id="97212-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97212-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="97212-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97212-129">Minimum supported server</span></span><br/> | <span data-ttu-id="97212-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97212-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="97212-131">DLL</span><span class="sxs-lookup"><span data-stu-id="97212-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97212-132"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97212-132"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97212-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97212-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97212-134">Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="97212-134">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="97212-135">Funktionen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="97212-135">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> </dl>

 

 
