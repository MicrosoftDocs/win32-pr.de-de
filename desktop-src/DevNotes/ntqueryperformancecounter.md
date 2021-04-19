---
description: Gibt den aktuellen Wert eines Leistungs Zählers und optional die Häufigkeit des Leistungs Zählers zurück.
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: Ntqueryperformancecounter-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryPerformanceCounter
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 5bf0aad74f6992212fb3b2238b3030c68cda2fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369453"
---
# <a name="ntqueryperformancecounter-function"></a><span data-ttu-id="7f423-103">Ntqueryperformancecounter-Funktion</span><span class="sxs-lookup"><span data-stu-id="7f423-103">NtQueryPerformanceCounter function</span></span>

<span data-ttu-id="7f423-104">\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f423-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="7f423-105">Verwenden Sie stattdessen die Funktionen **QueryPerformanceCounter** und **QueryPerformanceFrequency** .\]</span><span class="sxs-lookup"><span data-stu-id="7f423-105">Use the **QueryPerformanceCounter** and **QueryPerformanceFrequency** functions instead.\]</span></span>

<span data-ttu-id="7f423-106">Gibt den aktuellen Wert eines Leistungs Zählers und optional die Häufigkeit des Leistungs Zählers zurück.</span><span class="sxs-lookup"><span data-stu-id="7f423-106">Returns the current value of a performance counter and, optionally, the frequency of the performance counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f423-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f423-107">Syntax</span></span>


```C++
NTSTATUS NtQueryPerformanceCounter(
  _Out_     PLARGE_INTEGER PerformanceCounter,
  _Out_opt_ PLARGE_INTEGER PerformanceFrequency
);
```



## <a name="parameters"></a><span data-ttu-id="7f423-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f423-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f423-109">*Performance Counter* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7f423-109">*PerformanceCounter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f423-110">Die Adresse einer Variablen, die den aktuellen Leistungs Zählers Wert empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="7f423-110">The address of a variable to receive the current performance counter value.</span></span>

</dd> <dt>

<span data-ttu-id="7f423-111">*Performance Frequency* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="7f423-111">*PerformanceFrequency* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7f423-112">Die Adresse einer Variablen, die die Häufigkeit des Leistungs Zählers empfängt.</span><span class="sxs-lookup"><span data-stu-id="7f423-112">The address of a variable to receive the performance counter frequency.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f423-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f423-113">Return value</span></span>

<span data-ttu-id="7f423-114">Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie den **NTSTATUS** -Code **Status \_ Erfolg** zurück. andernfalls wird ein Fehlercode zurückgegeben, z. b. eine **Status \_ Zugriffs \_ Verletzung**.</span><span class="sxs-lookup"><span data-stu-id="7f423-114">If the function succeeds, it returns the **NTSTATUS** code **STATUS\_SUCCESS**; otherwise, it returns an error code such as **STATUS\_ACCESS\_VIOLATION**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f423-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f423-115">Remarks</span></span>

<span data-ttu-id="7f423-116">Für **ntqueryperformancecounter** ist keine Header Datei verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7f423-116">No header file is available for **NtQueryPerformanceCounter**.</span></span> <span data-ttu-id="7f423-117">Sie sollten die oben genannten alternativen Funktionen verwenden, obwohl Sie auch die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden können, um dynamisch mit Ntdll.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="7f423-117">You should use the alternative functions named above, although you can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

<span data-ttu-id="7f423-118">Die Leistungs Häufigkeit ist die Häufigkeit des Leistungs Zählers in Hertz, insbesondere in Zählungen pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="7f423-118">Performance frequency is the frequency of the performance counter in hertz, specifically in counts per second.</span></span> <span data-ttu-id="7f423-119">Dieser Wert ist implementierungsabhängig.</span><span class="sxs-lookup"><span data-stu-id="7f423-119">This value is implementation dependent.</span></span> <span data-ttu-id="7f423-120">Wenn die Implementierung nicht über Hardware zur Unterstützung der Leistungszeit verfügt, wird der zurückgegebene Wert 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7f423-120">If the implementation does not have hardware to support performance timing, the value returned is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f423-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f423-121">Requirements</span></span>



| <span data-ttu-id="7f423-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f423-122">Requirement</span></span> | <span data-ttu-id="7f423-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7f423-123">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7f423-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7f423-124">DLL</span></span><br/> | <dl> <span data-ttu-id="7f423-125"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f423-125"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f423-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f423-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f423-127">**QueryPerformanceCounter**</span><span class="sxs-lookup"><span data-stu-id="7f423-127">**QueryPerformanceCounter**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[<span data-ttu-id="7f423-128">**QueryPerformanceFrequency**</span><span class="sxs-lookup"><span data-stu-id="7f423-128">**QueryPerformanceFrequency**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
