---
title: Rasadminportclearstatistics-Funktion (rassapi. h)
description: Die rasadminportclearstatistics-Funktion setzt die Zähler zurück, die die verschiedenen Statistiken darstellen, die von der rasadminportgetinfo-Funktion in der Struktur der RAS- \_ Port Statistik gemeldet werden \_ . Die Zähler werden auf 0 (null) zurückgesetzt und beginnen mit der Anhäufung
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- Rasadminportclearstatistics-Funktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminPortClearStatistics
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57943fbefcba1625c7badff25827c62eaca8a8c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370082"
---
# <a name="rasadminportclearstatistics-function"></a><span data-ttu-id="d4698-105">Rasadminportclearstatistics-Funktion</span><span class="sxs-lookup"><span data-stu-id="d4698-105">RasAdminPortClearStatistics function</span></span>

<span data-ttu-id="d4698-106">\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d4698-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="d4698-107">Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="d4698-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="d4698-108">Anwendungen sollten die [**mpradminportclearstats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) -Funktion verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="d4698-108">Applications should use the [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) function.\]</span></span>

<span data-ttu-id="d4698-109">Die **rasadminportclearstatistics** -Funktion setzt die Zähler zurück, die die verschiedenen Statistiken darstellen, die von der [**rasadminportgetinfo**](rasadminportgetinfo.md) -Funktion in der Struktur der [**RAS- \_ Port \_ Statistik**](ras-port-statistics-str.md) gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="d4698-109">The **RasAdminPortClearStatistics** function resets the counters representing the various statistics reported by the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function in the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure.</span></span> <span data-ttu-id="d4698-110">Die Zähler werden auf 0 (null) zurückgesetzt und beginnen mit der Anhäufung</span><span class="sxs-lookup"><span data-stu-id="d4698-110">The counters are reset to zero and start accumulating.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4698-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4698-111">Syntax</span></span>


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a><span data-ttu-id="d4698-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4698-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4698-113">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4698-113">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4698-114">Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des RAS-Servers angibt.</span><span class="sxs-lookup"><span data-stu-id="d4698-114">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="d4698-115">Geben Sie den Namen mit führenden " \\ \\ " Zeichen im folgenden Format an: \\ \\ *Servername*.</span><span class="sxs-lookup"><span data-stu-id="d4698-115">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="d4698-116">*lpszport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4698-116">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4698-117">Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des Ports auf dem Server angibt.</span><span class="sxs-lookup"><span data-stu-id="d4698-117">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4698-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4698-118">Return value</span></span>

<span data-ttu-id="d4698-119">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d4698-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="d4698-120">Wenn die Funktion fehlschlägt, kann der folgende Fehlercode als Rückgabewert zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d4698-120">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="d4698-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d4698-121">Value</span></span>                                                                                                 | <span data-ttu-id="d4698-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d4698-122">Meaning</span></span>                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d4698-123"><dt>**Fehler \_ dev ist \_ nicht \_ vorhanden.**</dt></span><span class="sxs-lookup"><span data-stu-id="d4698-123"><dt>**ERROR\_DEV\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="d4698-124">Der angegebene Port ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d4698-124">The specified port is invalid.</span></span><br/> |



 

<span data-ttu-id="d4698-125">Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d4698-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4698-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4698-126">Remarks</span></span>

<span data-ttu-id="d4698-127">Die **rasadminportclearstatistics** -Funktion löscht die Statistiken auf dem Server, nicht lokal innerhalb der Anwendung, die den-Befehl ausführt.</span><span class="sxs-lookup"><span data-stu-id="d4698-127">The **RasAdminPortClearStatistics** function clears the statistics on the server, not locally within the application that makes the call.</span></span> <span data-ttu-id="d4698-128">Dies bedeutet, dass die Statistiken auch für alle anderen Anwendungen zurückgesetzt werden, die den angegebenen Port überwachen.</span><span class="sxs-lookup"><span data-stu-id="d4698-128">This means that the statistics are also reset for any other application that is monitoring the specified port.</span></span>

<span data-ttu-id="d4698-129">Wenn der *lpszport* -Port Teil einer Multilinkverbindung ist, setzt **rasadminportclearstatistics** die Statistiken für den angegebenen Port zurück, die-Funktion setzt auch die kumulativen Statistiken für die mehrfach-Verbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="d4698-129">If the *lpszPort* port is part of a multilink connection, **RasAdminPortClearStatistics** resets the statistics for the specified port, The function also resets the cumulative statistics for the multilink connection.</span></span> <span data-ttu-id="d4698-130">Die Funktion wirkt sich jedoch nicht auf die einzelnen Statistiken für andere Ports aus, die Teil der mehrfach-Verbindung sind.</span><span class="sxs-lookup"><span data-stu-id="d4698-130">However, the function does not effect the individual statistics for other ports that are part of the multilink connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4698-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4698-131">Requirements</span></span>



| <span data-ttu-id="d4698-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4698-132">Requirement</span></span> | <span data-ttu-id="d4698-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d4698-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4698-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d4698-134">End of client support</span></span><br/> | <span data-ttu-id="d4698-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d4698-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="d4698-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="d4698-136">End of server support</span></span><br/> | <span data-ttu-id="d4698-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d4698-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="d4698-138">Header</span><span class="sxs-lookup"><span data-stu-id="d4698-138">Header</span></span><br/>                | <dl> <span data-ttu-id="d4698-139"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4698-139"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4698-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d4698-140">Library</span></span><br/>               | <dl> <span data-ttu-id="d4698-141"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4698-141"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d4698-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d4698-142">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d4698-143"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4698-143"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4698-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4698-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4698-145">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="d4698-145">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="d4698-146">RAS-Server-Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="d4698-146">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="d4698-147">**RAS- \_ Port \_ Statistik**</span><span class="sxs-lookup"><span data-stu-id="d4698-147">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="d4698-148">**Rasadminportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="d4698-148">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

