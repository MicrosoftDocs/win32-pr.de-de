---
description: Ruft die Größe und den Speicherort der Liste der dynamisch entladenen Module für den aktuellen Prozess ab.
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: Rtlgetunloadeventtraceex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTraceEx
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 05b9e076041d0cd2298799970670478e9d358d32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367730"
---
# <a name="rtlgetunloadeventtraceex-function"></a><span data-ttu-id="5d53e-103">Rtlgetunloadeventtraceex-Funktion</span><span class="sxs-lookup"><span data-stu-id="5d53e-103">RtlGetUnloadEventTraceEx function</span></span>

<span data-ttu-id="5d53e-104">Ruft die Größe und den Speicherort der Liste der dynamisch entladenen Module für den aktuellen Prozess ab.</span><span class="sxs-lookup"><span data-stu-id="5d53e-104">Retrieves the size and location of the dynamically unloaded module list for the current process.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d53e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d53e-105">Syntax</span></span>


```C++
VOID WINAPI RtlGetUnloadEventTraceEx(
  _Out_ PULONG *ElementSize,
  _Out_ PULONG *ElementCount,
  _Out_ PVOID  *EventTrace
);
```



## <a name="parameters"></a><span data-ttu-id="5d53e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d53e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d53e-107">*Element Size* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5d53e-107">*ElementSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d53e-108">Ein Zeiger auf eine Variable, die die Größe eines Elements in der Liste enthält.</span><span class="sxs-lookup"><span data-stu-id="5d53e-108">A pointer to a variable that contains the size of an element in the list.</span></span>

</dd> <dt>

<span data-ttu-id="5d53e-109">*Element count* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5d53e-109">*ElementCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d53e-110">Ein Zeiger auf eine Variable, die die Anzahl der Elemente in der Liste enthält.</span><span class="sxs-lookup"><span data-stu-id="5d53e-110">A pointer to a variable that contains the number of elements in the list.</span></span>

</dd> <dt>

<span data-ttu-id="5d53e-111">*EventTrace* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5d53e-111">*EventTrace* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d53e-112">Ein Zeiger auf ein Array von **RTL- \_ Entlade \_ Ereignis \_** -Ablauf Verfolgungs Strukturen.</span><span class="sxs-lookup"><span data-stu-id="5d53e-112">A pointer to an array of **RTL\_UNLOAD\_EVENT\_TRACE** structures.</span></span> <span data-ttu-id="5d53e-113">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="5d53e-113">For more information, see Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d53e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d53e-114">Return value</span></span>

<span data-ttu-id="5d53e-115">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5d53e-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d53e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d53e-116">Remarks</span></span>

<span data-ttu-id="5d53e-117">Das Lade Modul speichert Informationen zu entladenen Ereignissen an Standorten, die über Prozesse hinweg gelesen werden können, indem die Tatsache genutzt wird, dass Ntdll.dll an derselben Basisadresse in allen Prozessen geladen wird.</span><span class="sxs-lookup"><span data-stu-id="5d53e-117">The loader stores unloaded event information in locations that can be read across processes by taking advantage of the fact that Ntdll.dll is loaded at the same base address in all processes.</span></span> <span data-ttu-id="5d53e-118">Wenn ein Debugger Informationen zu entladenen Modulen Abfragen muss, wird diese Funktion aufgerufen, um die Adresse zu bestimmen, in der sich die Variablen befinden. Anschließend wird der virtuelle Arbeitsspeicher im Ziel Prozess an diesen Adressen abgefragt, um die tatsächlichen Werte zu lesen.</span><span class="sxs-lookup"><span data-stu-id="5d53e-118">When a debugger needs to query unloaded module information, it calls this function to determine the address at which the variables reside, then queries the virtual memory in the target process at those addresses to read the actual values.</span></span>

<span data-ttu-id="5d53e-119">Jedes Element in der Liste wird wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="5d53e-119">Each element in the list is defined as follows.</span></span>

``` syntax
typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;
```

<span data-ttu-id="5d53e-120">Dieser Funktion ist keine Header Datei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5d53e-120">This function has no associated header file.</span></span> <span data-ttu-id="5d53e-121">Die zugehörige Import Bibliothek ntdll. lib ist im Windows-Treiberkit (WDK) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5d53e-121">The associated import library, Ntdll.lib, is available in the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="5d53e-122">Sie können diese Funktion auch mit der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5d53e-122">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d53e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d53e-123">Requirements</span></span>



| <span data-ttu-id="5d53e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d53e-124">Requirement</span></span> | <span data-ttu-id="5d53e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5d53e-125">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5d53e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5d53e-126">DLL</span></span><br/> | <dl> <span data-ttu-id="5d53e-127"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d53e-127"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
