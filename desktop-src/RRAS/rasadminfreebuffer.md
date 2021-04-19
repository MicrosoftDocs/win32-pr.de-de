---
title: Rasadminfrebuffer-Funktion (rassapi. h)
description: Die rasadminfrebuffer-Funktion gibt Arbeitsspeicher frei, der von RAS im Auftrag des Aufrufers zugeordnet wurde.
ms.assetid: 6dfbba22-3af1-4771-8c22-506996f30c6b
keywords:
- Rasadminfrebuffer-Funktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminFreeBuffer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf86a3005a2b865b2096eddc5ffa9c0c33f848a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370956"
---
# <a name="rasadminfreebuffer-function"></a><span data-ttu-id="22564-104">Rasadminfrebuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="22564-104">RasAdminFreeBuffer function</span></span>

<span data-ttu-id="22564-105">\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="22564-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="22564-106">Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="22564-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="22564-107">Anwendungen sollten die [**mpradminbufferfree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) -Funktion verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="22564-107">Applications should use the [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) function.\]</span></span>

<span data-ttu-id="22564-108">Die **rasadminfrebuffer** -Funktion gibt Arbeitsspeicher frei, der von RAS im Auftrag des Aufrufers zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="22564-108">The **RasAdminFreeBuffer** function frees memory that was allocated by RAS on behalf of the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="22564-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="22564-109">Syntax</span></span>


```C++
DWORD RasAdminFreeBuffer(
  _In_ PVOID Pointer
);
```



## <a name="parameters"></a><span data-ttu-id="22564-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="22564-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22564-111">*Zeiger* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22564-111">*Pointer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22564-112">Zeiger auf den Puffer, der freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="22564-112">Pointer to the buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22564-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22564-113">Return value</span></span>

<span data-ttu-id="22564-114">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="22564-114">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="22564-115">Wenn die Funktion fehlschlägt, kann der folgende Fehlercode als Rückgabewert zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="22564-115">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="22564-116">Wert</span><span class="sxs-lookup"><span data-stu-id="22564-116">Value</span></span>                                                                                                    | <span data-ttu-id="22564-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="22564-117">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="22564-118"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="22564-118"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="22564-119">Der *Zeiger* Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="22564-119">The *Pointer* parameter is invalid.</span></span><br/> |



 

<span data-ttu-id="22564-120">Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="22564-120">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="22564-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22564-121">Remarks</span></span>

<span data-ttu-id="22564-122">Verwenden Sie die **rasadminfreebuffer** -Funktion, um die Puffer freizugeben, die von den Funktionen [**rasadminportenum**](rasadminportenum.md) und [**rasadminportgetinfo**](rasadminportgetinfo.md) belegt werden.</span><span class="sxs-lookup"><span data-stu-id="22564-122">Use the **RasAdminFreeBuffer** function to free the buffers allocated by the [**RasAdminPortEnum**](rasadminportenum.md) and [**RasAdminPortGetInfo**](rasadminportgetinfo.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="22564-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22564-123">Requirements</span></span>



| <span data-ttu-id="22564-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22564-124">Requirement</span></span> | <span data-ttu-id="22564-125">Wert</span><span class="sxs-lookup"><span data-stu-id="22564-125">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22564-126">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="22564-126">End of client support</span></span><br/> | <span data-ttu-id="22564-127">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="22564-127">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="22564-128">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="22564-128">End of server support</span></span><br/> | <span data-ttu-id="22564-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="22564-129">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="22564-130">Header</span><span class="sxs-lookup"><span data-stu-id="22564-130">Header</span></span><br/>                | <dl> <span data-ttu-id="22564-131"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="22564-131"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="22564-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22564-132">Library</span></span><br/>               | <dl> <span data-ttu-id="22564-133"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22564-133"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="22564-134">DLL</span><span class="sxs-lookup"><span data-stu-id="22564-134">DLL</span></span><br/>                   | <dl> <span data-ttu-id="22564-135"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22564-135"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22564-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22564-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22564-137">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="22564-137">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="22564-138">RAS-Server-Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="22564-138">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="22564-139">**Rasadminportenum**</span><span class="sxs-lookup"><span data-stu-id="22564-139">**RasAdminPortEnum**</span></span>](rasadminportenum.md)
</dt> <dt>

[<span data-ttu-id="22564-140">**Rasadminportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="22564-140">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

