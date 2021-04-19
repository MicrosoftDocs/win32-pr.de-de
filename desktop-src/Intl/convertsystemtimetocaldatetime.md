---
description: Veraltet. Konvertiert eine angegebene SYSTEMTIME-Struktur in eine caldatetime-Struktur.
ms.assetid: d21f75bc-1a93-4cb9-8b9b-6fa0e81886bf
title: Convertsystemtimeumcaldatetime-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertSystemTimeToCalDateTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 738899c7307797f0edeade93f7e4e706919be900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106367975"
---
# <a name="convertsystemtimetocaldatetime-function"></a><span data-ttu-id="4700e-104">Convertsystemtimeumcaldatetime-Funktion</span><span class="sxs-lookup"><span data-stu-id="4700e-104">ConvertSystemTimeToCalDateTime function</span></span>

<span data-ttu-id="4700e-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="4700e-105">Deprecated.</span></span> <span data-ttu-id="4700e-106">Konvertiert eine angegebene [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) -Struktur in eine [**caldatetime**](caldatetime.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4700e-106">Converts a specified [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure to a [**CALDATETIME**](caldatetime.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4700e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4700e-107">Syntax</span></span>


```C++
BOOL ConvertSystemTimeToCalDateTime(
  _In_  const SYSTEMTIME   *lpSysTime,
  _In_        CALID         calId,
  _Out_       LPCALDATETIME lpCalDateTime

);
```



## <a name="parameters"></a><span data-ttu-id="4700e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4700e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4700e-109">*lpsystime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4700e-109">*lpSysTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4700e-110">Zeiger auf die zu konvertierende [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4700e-110">Pointer to the [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure to convert.</span></span>

</dd> <dt>

<span data-ttu-id="4700e-111">*Calid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4700e-111">*calId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4700e-112">Der für die Konvertierung zu verwendende System [Kalender Bezeichner](calendar-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="4700e-112">The system [calendar identifier](calendar-identifiers.md) to use in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="4700e-113">*lpcaldatetime* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4700e-113">*lpCalDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4700e-114">Ein Zeiger auf die entsprechende [**caldatetime**](caldatetime.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4700e-114">Pointer to the equivalent [**CALDATETIME**](caldatetime.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4700e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4700e-115">Return value</span></span>

<span data-ttu-id="4700e-116">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="4700e-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="4700e-117">Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:</span><span class="sxs-lookup"><span data-stu-id="4700e-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="4700e-118">Fehler \_ : Ungültiger \_ Parameter.</span><span class="sxs-lookup"><span data-stu-id="4700e-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="4700e-119">Jeder Parameterwert war ungültig.</span><span class="sxs-lookup"><span data-stu-id="4700e-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="4700e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4700e-120">Remarks</span></span>

<span data-ttu-id="4700e-121">Das früheste von dieser Funktion unterstützte Datum ist der 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="4700e-121">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="4700e-122">Diese Funktion verfügt über keine zugeordnete Header Datei oder Bibliotheksdatei.</span><span class="sxs-lookup"><span data-stu-id="4700e-122">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="4700e-123">Die Anwendung kann [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen (Kernel32.dll) aufzurufen, um ein Modul Handle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4700e-123">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="4700e-124">Anschließend kann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit dem Modul Handle und dem Namen dieser Funktion aufgerufen werden, um die Funktions Adresse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4700e-124">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="4700e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4700e-125">Requirements</span></span>



| <span data-ttu-id="4700e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4700e-126">Requirement</span></span> | <span data-ttu-id="4700e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="4700e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4700e-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4700e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4700e-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4700e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4700e-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4700e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4700e-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4700e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4700e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4700e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4700e-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4700e-133"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4700e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4700e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4700e-135">Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="4700e-135">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="4700e-136">Funktionen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="4700e-136">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="4700e-137">Abrufen von Zeit-und Datumsinformationen</span><span class="sxs-lookup"><span data-stu-id="4700e-137">Retrieving Time and Date Information</span></span>](time-and-date.md)
</dt> </dl>

 

 
