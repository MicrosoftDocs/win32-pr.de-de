---
description: Ermöglicht dem dumpcode, die entladenen Modul Informationen aus Ntdll.dll für den Speicher im Minidump zu erhalten.
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: Rtlgetunloadeventtrace-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTrace
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9297ba0019c89c5e93961d4b36e0fe16da04d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362037"
---
# <a name="rtlgetunloadeventtrace-function"></a><span data-ttu-id="532e3-103">Rtlgetunloadeventtrace-Funktion</span><span class="sxs-lookup"><span data-stu-id="532e3-103">RtlGetUnloadEventTrace function</span></span>

<span data-ttu-id="532e3-104">\[Diese Funktion kann ohne vorherige Ankündigung geändert oder aus Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="532e3-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="532e3-105">Ermöglicht dem dumpcode, die entladenen Modul Informationen aus Ntdll.dll für den Speicher im Minidump zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="532e3-105">Enables the dump code to get the unloaded module information from Ntdll.dll for storage in the minidump.</span></span>

## <a name="syntax"></a><span data-ttu-id="532e3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="532e3-106">Syntax</span></span>


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="532e3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="532e3-107">Parameters</span></span>

<span data-ttu-id="532e3-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="532e3-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="532e3-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="532e3-109">Return value</span></span>

<span data-ttu-id="532e3-110">Diese Funktion gibt einen Zeiger auf ein Array zurück.</span><span class="sxs-lookup"><span data-stu-id="532e3-110">This function returns a pointer to an array.</span></span> <span data-ttu-id="532e3-111">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="532e3-111">For more information, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="532e3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="532e3-112">Remarks</span></span>

<span data-ttu-id="532e3-113">Das rtlpunloadeventtrace-Array wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="532e3-113">The RtlpUnloadEventTrace array is defined as follows:</span></span>

``` syntax
#define RTL_UNLOAD_EVENT_TRACE_NUMBER 64

typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;

RTL_UNLOAD_EVENT_TRACE RtlpUnloadEventTrace[RTL_UNLOAD_EVENT_TRACE_NUMBER];
```

<span data-ttu-id="532e3-114">Dieser Funktion ist keine Header Datei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="532e3-114">This function has no associated header file.</span></span> <span data-ttu-id="532e3-115">Die zugehörige Import Bibliothek ntdll. lib ist im Windows-Treiberkit (WDK) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="532e3-115">The associated import library, Ntdll.lib, is available in the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="532e3-116">Sie können diese Funktion auch mit der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="532e3-116">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="532e3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="532e3-117">Requirements</span></span>



| <span data-ttu-id="532e3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="532e3-118">Requirement</span></span> | <span data-ttu-id="532e3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="532e3-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="532e3-120">DLL</span><span class="sxs-lookup"><span data-stu-id="532e3-120">DLL</span></span><br/> | <dl> <span data-ttu-id="532e3-121"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="532e3-121"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
