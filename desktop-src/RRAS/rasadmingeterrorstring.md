---
title: Rasadmingeterrorstring-Funktion (rassapi. h)
description: Die rasadmingeterrorstring-Funktion Ruft eine Meldungs Zeichenfolge ab, die einem RAS-Fehlercode entspricht, der von einer der RAS-Server Verwaltungsfunktionen (rasadmin) zurückgegeben wurde.
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- Rasadmingeterrorstring-Funktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminGetErrorString
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc239c5f26061b5234631079ba21ce0d24ad570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372037"
---
# <a name="rasadmingeterrorstring-function"></a><span data-ttu-id="e5caf-104">Rasadmingeterrorstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="e5caf-104">RasAdminGetErrorString function</span></span>

<span data-ttu-id="e5caf-105">\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e5caf-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="e5caf-106">Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="e5caf-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="e5caf-107">Anwendungen sollten die [**mpradmingeterrorstring**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) -Funktion verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="e5caf-107">Applications should use the [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) function.\]</span></span>

<span data-ttu-id="e5caf-108">Die **rasadmingeterrorstring** -Funktion Ruft eine Meldungs Zeichenfolge ab, die einem RAS-Fehlercode entspricht, der von einer der RAS-Server Verwaltungsfunktionen (rasadmin) zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e5caf-108">The **RasAdminGetErrorString** function retrieves a message string that corresponds to a RAS error code returned by one of the RAS server administration (RasAdmin) functions.</span></span> <span data-ttu-id="e5caf-109">Diese Nachrichten Zeichenfolgen werden aus dem Rasmsg.dll abgerufen, der als Teil von RAS installiert wird.</span><span class="sxs-lookup"><span data-stu-id="e5caf-109">These message strings are retrieved from the Rasmsg.dll that is installed as part of RAS.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5caf-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5caf-110">Syntax</span></span>


```C++
DWORD RasAdminGetErrorString(
  _In_  UINT  ResourceId,
  _Out_ WCHAR *lpszString,
  _In_  DWORD InBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="e5caf-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5caf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5caf-112">*ResourceId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5caf-112">*ResourceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5caf-113">Gibt einen Fehlercode an, der von einer der rasadmin-Funktionen zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e5caf-113">Specifies an error code returned by one of the RasAdmin functions.</span></span> <span data-ttu-id="e5caf-114">Dieser Wert muss im Bereich der Fehlercodes von "rasbase" zu "rasbaseend" liegen.</span><span class="sxs-lookup"><span data-stu-id="e5caf-114">This value must be in the range of error codes from RASBASE to RASBASEEND.</span></span> <span data-ttu-id="e5caf-115">Diese werden in "raserror. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="e5caf-115">These are defined in Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="e5caf-116">*lpszstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e5caf-116">*lpszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5caf-117">Ein Zeiger auf einen Puffer, der die Fehlermeldung empfängt, die dem angegebenen Fehlercode entspricht.</span><span class="sxs-lookup"><span data-stu-id="e5caf-117">Pointer to a buffer that receives the error message that corresponds to the specified error code.</span></span>

</dd> <dt>

<span data-ttu-id="e5caf-118">*Inbubsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5caf-118">*InBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5caf-119">Gibt die Größe des *lpszstring* -Puffers in Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="e5caf-119">Specifies the size, in characters, of the *lpszString* buffer.</span></span> <span data-ttu-id="e5caf-120">Fehlermeldungen sind in der Regel 80 Zeichen oder weniger. eine Puffergröße von 512 Zeichen ist immer ausreichend.</span><span class="sxs-lookup"><span data-stu-id="e5caf-120">Error messages are typically 80 characters or less; a buffer size of 512 characters is always adequate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5caf-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5caf-121">Return value</span></span>

<span data-ttu-id="e5caf-122">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e5caf-122">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="e5caf-123">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e5caf-123">If the function fails, the return value is an error code.</span></span> <span data-ttu-id="e5caf-124">Dieser Wert kann ein letzter Fehlerwert sein, der von den Funktionen [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**globalzuordc**](/windows/win32/api/winbase/nf-winbase-globalalloc)oder [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) festgelegt wird. oder Sie können einen der folgenden Fehlercodes aufweisen:</span><span class="sxs-lookup"><span data-stu-id="e5caf-124">This value can be a last error value set by the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc), or [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) functions; or it can be one of the following error codes.</span></span>



| <span data-ttu-id="e5caf-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e5caf-125">Value</span></span>                                                                                                      | <span data-ttu-id="e5caf-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e5caf-126">Meaning</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e5caf-127"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="e5caf-127"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>   | <span data-ttu-id="e5caf-128">Die Parameter " *ResourceId* " oder " *lpszstring* " sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="e5caf-128">The *ResourceId* or *lpszString* parameters are invalid.</span></span><br/>      |
| <dl> <span data-ttu-id="e5caf-129"><dt>**Fehler \_ beim \_ Puffer.**</dt></span><span class="sxs-lookup"><span data-stu-id="e5caf-129"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="e5caf-130">Die vom *inbubsize* -Parameter angegebene Größe ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="e5caf-130">The size specified by the *InBufSize* parameter is too small.</span></span><br/> |



 

<span data-ttu-id="e5caf-131">Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e5caf-131">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="e5caf-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5caf-132">Remarks</span></span>

<span data-ttu-id="e5caf-133">Die rasadmin-Funktionen können Fehlercodes zurückgeben, die nicht im von der **rasadmingeterrorstring** -Funktion unterstützten Bereich liegen.</span><span class="sxs-lookup"><span data-stu-id="e5caf-133">The RasAdmin functions can return error codes that are not in the range supported by the **RasAdminGetErrorString** function.</span></span> <span data-ttu-id="e5caf-134">Die rasadmin-Funktionen können z. b. Fehlercodes zurückgeben, die in "lmerr. h" und "Winerror. h" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e5caf-134">For example, the RasAdmin functions can return error codes that are defined in Lmerr.h and Winerror.h.</span></span> <span data-ttu-id="e5caf-135">Vergewissern Sie sich vor dem Aufrufen von **rasadmingeterrorstring**, dass sich der Fehlercode im Bereich "rasbase" zu "rasbaseend" befindet, wie in "raserror. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="e5caf-135">Before calling **RasAdminGetErrorString**, verify that the error code is in the range RASBASE to RASBASEEND, as defined in Raserror.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5caf-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5caf-136">Requirements</span></span>



| <span data-ttu-id="e5caf-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5caf-137">Requirement</span></span> | <span data-ttu-id="e5caf-138">Wert</span><span class="sxs-lookup"><span data-stu-id="e5caf-138">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5caf-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e5caf-139">End of client support</span></span><br/> | <span data-ttu-id="e5caf-140">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e5caf-140">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="e5caf-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="e5caf-141">End of server support</span></span><br/> | <span data-ttu-id="e5caf-142">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e5caf-142">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="e5caf-143">Header</span><span class="sxs-lookup"><span data-stu-id="e5caf-143">Header</span></span><br/>                | <dl> <span data-ttu-id="e5caf-144"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5caf-144"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5caf-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e5caf-145">Library</span></span><br/>               | <dl> <span data-ttu-id="e5caf-146"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5caf-146"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e5caf-147">DLL</span><span class="sxs-lookup"><span data-stu-id="e5caf-147">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e5caf-148"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5caf-148"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5caf-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5caf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5caf-150">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="e5caf-150">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="e5caf-151">RAS-Server-Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="e5caf-151">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="e5caf-152">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="e5caf-152">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="e5caf-153">**GlobalAlloc**</span><span class="sxs-lookup"><span data-stu-id="e5caf-153">**GlobalAlloc**</span></span>](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[<span data-ttu-id="e5caf-154">**LoadString**</span><span class="sxs-lookup"><span data-stu-id="e5caf-154">**LoadString**</span></span>](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

