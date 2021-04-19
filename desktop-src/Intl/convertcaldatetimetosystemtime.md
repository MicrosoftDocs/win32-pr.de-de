---
description: Veraltet. Konvertiert eine angegebene caldatetime-Struktur in eine SYSTEMTIME-Struktur.
ms.assetid: 0c3f602d-62de-4c27-95d9-d35738f3279d
title: Convertcaldatetimetsystemtime-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertCalDateTimeToSystemTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 9c317a31904e2d1b0b2110f6b2dc367ac3e2e0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373073"
---
# <a name="convertcaldatetimetosystemtime-function"></a><span data-ttu-id="2e229-104">Convertcaldatetimetsystemtime-Funktion</span><span class="sxs-lookup"><span data-stu-id="2e229-104">ConvertCalDateTimeToSystemTime function</span></span>

<span data-ttu-id="2e229-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="2e229-105">Deprecated.</span></span> <span data-ttu-id="2e229-106">Konvertiert eine angegebene [**caldatetime**](caldatetime.md) -Struktur in eine [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2e229-106">Converts a specified [**CALDATETIME**](caldatetime.md) structure to a [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e229-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e229-107">Syntax</span></span>


```C++
BOOL ConvertCalDateTimeToSystemTime(
  _In_  const LPCALDATETIME lpCalDateTime,
  _Out_       SYSTEMTIME    *lpSysTime
);
```



## <a name="parameters"></a><span data-ttu-id="2e229-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e229-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e229-109">*lpcaldatetime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e229-109">*lpCalDateTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e229-110">Zeiger auf die zu konvertierende [**caldatetime**](caldatetime.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2e229-110">Pointer to the [**CALDATETIME**](caldatetime.md) structure to convert.</span></span>

</dd> <dt>

<span data-ttu-id="2e229-111">*lpsystime* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2e229-111">*lpSysTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e229-112">Zeiger auf die entsprechende [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2e229-112">Pointer to the equivalent [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e229-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e229-113">Return value</span></span>

<span data-ttu-id="2e229-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="2e229-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="2e229-115">Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:</span><span class="sxs-lookup"><span data-stu-id="2e229-115">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="2e229-116">das Fehler \_ Datum liegt \_ außerhalb des zulässigen \_ \_ Bereichs.</span><span class="sxs-lookup"><span data-stu-id="2e229-116">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="2e229-117">Das angegebene Datum lag außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="2e229-117">The specified date was out of range.</span></span>
-   <span data-ttu-id="2e229-118">Fehler \_ : Ungültiger \_ Parameter.</span><span class="sxs-lookup"><span data-stu-id="2e229-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="2e229-119">Jeder Parameterwert war ungültig.</span><span class="sxs-lookup"><span data-stu-id="2e229-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e229-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e229-120">Remarks</span></span>

<span data-ttu-id="2e229-121">Diese Funktion verfügt über keine zugeordnete Header Datei oder Bibliotheksdatei.</span><span class="sxs-lookup"><span data-stu-id="2e229-121">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="2e229-122">Die Anwendung kann [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen (Kernel32.dll) aufzurufen, um ein Modul Handle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2e229-122">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="2e229-123">Anschließend kann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit dem Modul Handle und dem Namen dieser Funktion aufgerufen werden, um die Funktions Adresse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2e229-123">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e229-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e229-124">Requirements</span></span>



| <span data-ttu-id="2e229-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e229-125">Requirement</span></span> | <span data-ttu-id="2e229-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2e229-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e229-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e229-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2e229-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e229-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2e229-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e229-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2e229-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e229-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2e229-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2e229-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e229-132"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e229-132"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e229-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e229-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e229-134">Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="2e229-134">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="2e229-135">Funktionen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="2e229-135">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="2e229-136">Abrufen von Zeit-und Datumsinformationen</span><span class="sxs-lookup"><span data-stu-id="2e229-136">Retrieving Time and Date Information</span></span>](time-and-date.md)
</dt> </dl>

 

 
