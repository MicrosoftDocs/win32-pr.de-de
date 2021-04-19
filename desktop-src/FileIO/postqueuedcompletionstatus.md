---
description: Stellt ein e/a-abschlusspaket an einen e/a-Abschlussport.
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: PostQueuedCompletionStatus-Funktion (ioapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostQueuedCompletionStatus
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: f12de10032df7fec32dd9a577353dd20c0f4eaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356961"
---
# <a name="postqueuedcompletionstatus-function"></a><span data-ttu-id="2c5b9-103">PostQueuedCompletionStatus-Funktion</span><span class="sxs-lookup"><span data-stu-id="2c5b9-103">PostQueuedCompletionStatus function</span></span>

<span data-ttu-id="2c5b9-104">Stellt ein e/a-abschlusspaket an einen e/a-Abschlussport.</span><span class="sxs-lookup"><span data-stu-id="2c5b9-104">Posts an I/O completion packet to an I/O completion port.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c5b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c5b9-105">Syntax</span></span>


```C++
BOOL WINAPI PostQueuedCompletionStatus(
  _In_     HANDLE       CompletionPort,
  _In_     DWORD        dwNumberOfBytesTransferred,
  _In_     ULONG_PTR    dwCompletionKey,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a><span data-ttu-id="2c5b9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c5b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c5b9-107">*Completionport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c5b9-107">*CompletionPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c5b9-108">Ein Handle für einen e/a-Abschlussport, an den das e/a-abschlusspaket gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c5b9-108">A handle to an I/O completion port to which the I/O completion packet is to be posted.</span></span>

</dd> <dt>

<span data-ttu-id="2c5b9-109">*dwnumofbytestransferred* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c5b9-109">*dwNumberOfBytesTransferred* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c5b9-110">Der Wert, der durch den *lpnumofbytestransferred* -Parameter der [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c5b9-110">The value to be returned through the *lpNumberOfBytesTransferred* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="2c5b9-111">*dwcompletionkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c5b9-111">*dwCompletionKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c5b9-112">Der Wert, der durch den *lpcompletionkey* -Parameter der [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c5b9-112">The value to be returned through the *lpCompletionKey* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="2c5b9-113">*lpoverlgetauscht* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2c5b9-113">*lpOverlapped* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2c5b9-114">Der Wert, der durch den *lpoverllapp* -Parameter der [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c5b9-114">The value to be returned through the *lpOverlapped* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c5b9-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c5b9-115">Return value</span></span>

<span data-ttu-id="2c5b9-116">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.</span><span class="sxs-lookup"><span data-stu-id="2c5b9-116">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="2c5b9-117">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="2c5b9-117">If the function fails, the return value is zero.</span></span> <span data-ttu-id="2c5b9-118">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="2c5b9-118">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span></span>

## <a name="remarks"></a><span data-ttu-id="2c5b9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c5b9-119">Remarks</span></span>

<span data-ttu-id="2c5b9-120">Das e/a-abschlusspaket erfüllt einen ausstehenden aufrufungs [**Vorgang der GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2c5b9-120">The I/O completion packet will satisfy an outstanding call to the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span> <span data-ttu-id="2c5b9-121">Diese Funktion gibt mit den drei Werten zurück, die als zweite, dritte und vierte Parameter des Aufrufes **PostQueuedCompletionStatus** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2c5b9-121">This function returns with the three values passed as the second, third, and fourth parameters of the call to **PostQueuedCompletionStatus**.</span></span> <span data-ttu-id="2c5b9-122">Diese Werte werden vom System nicht verwendet oder überprüft.</span><span class="sxs-lookup"><span data-stu-id="2c5b9-122">The system does not use or validate these values.</span></span> <span data-ttu-id="2c5b9-123">Insbesondere muss der Parameter " *lpoverlgetauscht* " nicht auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="2c5b9-123">In particular, the *lpOverlapped* parameter need not point to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="2c5b9-124">In Windows 8 und Windows Server 2012 wird diese Funktion von den folgenden Technologien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2c5b9-124">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="2c5b9-125">Technologie</span><span class="sxs-lookup"><span data-stu-id="2c5b9-125">Technology</span></span>                                           | <span data-ttu-id="2c5b9-126">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="2c5b9-126">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="2c5b9-127">Server Message Block-Protokoll (SMB) 3,0</span><span class="sxs-lookup"><span data-stu-id="2c5b9-127">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="2c5b9-128">Ja</span><span class="sxs-lookup"><span data-stu-id="2c5b9-128">Yes</span></span><br/> |
| <span data-ttu-id="2c5b9-129">SMB 3,0 transparent Failover (TFO)</span><span class="sxs-lookup"><span data-stu-id="2c5b9-129">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="2c5b9-130">Ja</span><span class="sxs-lookup"><span data-stu-id="2c5b9-130">Yes</span></span><br/> |
| <span data-ttu-id="2c5b9-131">SMB 3,0 mit Dateifreigaben mit horizontaler Skalierung (also)</span><span class="sxs-lookup"><span data-stu-id="2c5b9-131">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="2c5b9-132">Ja</span><span class="sxs-lookup"><span data-stu-id="2c5b9-132">Yes</span></span><br/> |
| <span data-ttu-id="2c5b9-133">Freigegebenes Clustervolume Datei System (csvfs)</span><span class="sxs-lookup"><span data-stu-id="2c5b9-133">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="2c5b9-134">Ja</span><span class="sxs-lookup"><span data-stu-id="2c5b9-134">Yes</span></span><br/> |
| <span data-ttu-id="2c5b9-135">Robustes Dateisystem (Resilient File System, ReFS)</span><span class="sxs-lookup"><span data-stu-id="2c5b9-135">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="2c5b9-136">Ja</span><span class="sxs-lookup"><span data-stu-id="2c5b9-136">Yes</span></span><br/> |



 

<span data-ttu-id="2c5b9-137">Csvfs führt umgeleitete e/a für komprimierte Dateien aus.</span><span class="sxs-lookup"><span data-stu-id="2c5b9-137">CsvFs will do redirected IO for compressed files.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c5b9-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c5b9-138">Requirements</span></span>



| <span data-ttu-id="2c5b9-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c5b9-139">Requirement</span></span> | <span data-ttu-id="2c5b9-140">Wert</span><span class="sxs-lookup"><span data-stu-id="2c5b9-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c5b9-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c5b9-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2c5b9-142">\[UWP-Apps für Windows XP-Desktop-Apps \|\]</span><span class="sxs-lookup"><span data-stu-id="2c5b9-142">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2c5b9-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c5b9-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2c5b9-144">Windows Server 2003 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2c5b9-144">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="2c5b9-145">Header</span><span class="sxs-lookup"><span data-stu-id="2c5b9-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c5b9-146"><dt>Ioapi. h (Include Windows. h); </dt> <dt>Winbase. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c5b9-146"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2c5b9-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2c5b9-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="2c5b9-148"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c5b9-148"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="2c5b9-149">DLL</span><span class="sxs-lookup"><span data-stu-id="2c5b9-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c5b9-150"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c5b9-150"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="2c5b9-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c5b9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c5b9-152">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="2c5b9-152">**CreateIoCompletionPort**</span></span>](createiocompletionport.md)
</dt> <dt>

[<span data-ttu-id="2c5b9-153">Dateiverwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="2c5b9-153">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="2c5b9-154">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="2c5b9-154">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="2c5b9-155">**Überlappende**</span><span class="sxs-lookup"><span data-stu-id="2c5b9-155">**OVERLAPPED**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

