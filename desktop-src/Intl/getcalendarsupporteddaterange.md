---
description: Veraltet. Ruft den unterstützten Datumsbereich für einen angegebenen Kalender ab.
ms.assetid: fe036ac5-77c0-4e83-8d70-db3fa0f7c803
title: Getcalendarsupporteddaterange-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarSupportedDateRange
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 57b1175ef7bcf5b6b5d91af63682ca565bc0f1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960165"
---
# <a name="getcalendarsupporteddaterange-function"></a><span data-ttu-id="dbbe4-104">Getcalendarsupporteddaterange-Funktion</span><span class="sxs-lookup"><span data-stu-id="dbbe4-104">GetCalendarSupportedDateRange function</span></span>

<span data-ttu-id="dbbe4-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-105">Deprecated.</span></span> <span data-ttu-id="dbbe4-106">Ruft den unterstützten Datumsbereich für einen angegebenen Kalender ab.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-106">Gets the supported date range for a specified calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbbe4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbbe4-107">Syntax</span></span>


```C++
BOOL GetCalendarSupportedDateRange(
  _In_  CALID         Calendar,
  _Out_ LPCALDATETIME lpCalMinDateTime,
  _Out_ LPCALDATETIME lpCalMaxDateTime
);
```



## <a name="parameters"></a><span data-ttu-id="dbbe4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbbe4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbbe4-109">*Kalender* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbbe4-109">*Calendar* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbe4-110">Der [Kalender Bezeichner](calendar-identifiers.md) , für den der unterstützte Datumsbereich angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-110">[Calendar identifier](calendar-identifiers.md) for which to get the supported date range.</span></span>

</dd> <dt>

<span data-ttu-id="dbbe4-111">*lpcalmindatetime* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dbbe4-111">*lpCalMinDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbe4-112">Ein Zeiger auf eine [**caldatetime**](caldatetime.md) -Struktur, die das unterstützte minimal Datum definiert.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-112">Pointer to a [**CALDATETIME**](caldatetime.md) structure defining the minimum supported date.</span></span>

</dd> <dt>

<span data-ttu-id="dbbe4-113">*lpcalmaxdatetime* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dbbe4-113">*lpCalMaxDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbe4-114">Ein Zeiger auf eine [**caldatetime**](caldatetime.md) -Struktur, die das maximal unterstützte Datum definiert.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-114">Pointer to a [**CALDATETIME**](caldatetime.md) structure defining the maximum supported date.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbbe4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dbbe4-115">Return value</span></span>

<span data-ttu-id="dbbe4-116">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="dbbe4-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="dbbe4-117">Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:</span><span class="sxs-lookup"><span data-stu-id="dbbe4-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="dbbe4-118">Fehler \_ : Ungültiger \_ Parameter.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="dbbe4-119">Jeder Parameterwert war ungültig.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbbe4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbbe4-120">Remarks</span></span>

<span data-ttu-id="dbbe4-121">Das früheste von dieser Funktion unterstützte Datum ist der 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-121">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="dbbe4-122">Diese Funktion verfügt über keine zugeordnete Header Datei oder Bibliotheksdatei.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-122">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="dbbe4-123">Die Anwendung kann [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen (Kernel32.dll) aufzurufen, um ein Modul Handle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-123">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="dbbe4-124">Anschließend kann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit dem Modul Handle und dem Namen dieser Funktion aufgerufen werden, um die Funktions Adresse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-124">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbbe4-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbbe4-125">Requirements</span></span>



| <span data-ttu-id="dbbe4-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbbe4-126">Requirement</span></span> | <span data-ttu-id="dbbe4-127">Wert</span><span class="sxs-lookup"><span data-stu-id="dbbe4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbbe4-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbbe4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dbbe4-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbbe4-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dbbe4-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbbe4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dbbe4-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbbe4-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dbbe4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dbbe4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbbe4-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbbe4-133"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbbe4-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbbe4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbbe4-135">Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="dbbe4-135">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="dbbe4-136">Funktionen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="dbbe4-136">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="dbbe4-137">NLS: Beispiel für namensbasierte APIs</span><span class="sxs-lookup"><span data-stu-id="dbbe4-137">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
