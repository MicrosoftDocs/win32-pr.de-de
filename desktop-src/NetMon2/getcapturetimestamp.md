---
description: Die getcapturetimestamp-Funktion gibt das Datum und die Uhrzeit zurück, zu der die Erfassung mit dem Aufzeichnen von Frames begonnen hat
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: Getcapturetimestamp-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 855aa8b5432fd06bb25571fcb48c091dcfe502f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525139"
---
# <a name="getcapturetimestamp-function"></a><span data-ttu-id="65d36-103">Getcapturetimestamp-Funktion</span><span class="sxs-lookup"><span data-stu-id="65d36-103">GetCaptureTimeStamp function</span></span>

<span data-ttu-id="65d36-104">Die **getcapturetimestamp** -Funktion gibt das Datum und die Uhrzeit zurück, zu der die Erfassung mit dem Aufzeichnen von Frames begonnen hat</span><span class="sxs-lookup"><span data-stu-id="65d36-104">The **GetCaptureTimeStamp** function returns the time and date when the capture started recording frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d36-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="65d36-105">Syntax</span></span>


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="65d36-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="65d36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65d36-107">*hcapture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65d36-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65d36-108">Handle für die Erfassung.</span><span class="sxs-lookup"><span data-stu-id="65d36-108">Handle to the capture.</span></span> <span data-ttu-id="65d36-109">Weitere Informationen zum Abrufen des Aufzeichnungs Handles finden Sie im Abschnitt "Hinweise" in diesem Thema zu **getcapturetimestamp** .</span><span class="sxs-lookup"><span data-stu-id="65d36-109">For information about obtaining the capture handle, see the Remarks section of this **GetCaptureTimeStamp** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65d36-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65d36-110">Return value</span></span>

<span data-ttu-id="65d36-111">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf eine [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="65d36-111">If the function is successful, the return value is a pointer to a [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

<span data-ttu-id="65d36-112">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="65d36-112">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="65d36-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65d36-113">Remarks</span></span>

<span data-ttu-id="65d36-114">Die **getcapturetimestamp** -Funktion gibt die Zeit zurück, zu der der Netzwerk Paketanbieter (NPP) mit dem Sammeln von Daten beginnt, nicht, wenn der Experte die Erfassung für die Analyse lädt.</span><span class="sxs-lookup"><span data-stu-id="65d36-114">The **GetCaptureTimeStamp** function returns the time when the Network Packet Provider (NPP) starts collecting data, not when the expert loads the capture for analysis.</span></span>

<span data-ttu-id="65d36-115">Überschreiben Sie die Daten in der **SYSTEMTIME** -Struktur nicht.</span><span class="sxs-lookup"><span data-stu-id="65d36-115">Do not overwrite the data in the **SYSTEMTIME** structure.</span></span> <span data-ttu-id="65d36-116">Die Daten sind Teil der Erfassung.</span><span class="sxs-lookup"><span data-stu-id="65d36-116">The data is part of the capture.</span></span> <span data-ttu-id="65d36-117">Der Versuch, die Daten zu ändern, verursacht eine Zugriffsverletzung.</span><span class="sxs-lookup"><span data-stu-id="65d36-117">Trying to modify the data causes an access violation.</span></span>

<span data-ttu-id="65d36-118">[*Experten*](e.md) und [*Parser*](p.md) können die **getcapturetimestamp** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="65d36-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureTimeStamp** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="65d36-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65d36-119">Requirements</span></span>



| <span data-ttu-id="65d36-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65d36-120">Requirement</span></span> | <span data-ttu-id="65d36-121">Wert</span><span class="sxs-lookup"><span data-stu-id="65d36-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="65d36-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="65d36-122">Minimum supported client</span></span><br/> | <span data-ttu-id="65d36-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65d36-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="65d36-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="65d36-124">Minimum supported server</span></span><br/> | <span data-ttu-id="65d36-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65d36-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="65d36-126">Header</span><span class="sxs-lookup"><span data-stu-id="65d36-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="65d36-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="65d36-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="65d36-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="65d36-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="65d36-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65d36-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="65d36-130">DLL</span><span class="sxs-lookup"><span data-stu-id="65d36-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65d36-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65d36-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65d36-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65d36-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d36-133">System Time</span><span class="sxs-lookup"><span data-stu-id="65d36-133">SYSTEMTIME</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

