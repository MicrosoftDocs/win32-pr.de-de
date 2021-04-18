---
title: Rasadminportgetinfo-Funktion (rassapi. h)
description: Die rasadminportgetinfo-Funktion Ruft Informationen zu einem angegebenen Port auf einem angegebenen Server ab.
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- Rasadminportgetinfo-Funktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminPortGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d80c55b3182ec930732344cb7857f99c0dc411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360952"
---
# <a name="rasadminportgetinfo-function"></a><span data-ttu-id="39d19-104">Rasadminportgetinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="39d19-104">RasAdminPortGetInfo function</span></span>

<span data-ttu-id="39d19-105">\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="39d19-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="39d19-106">Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="39d19-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="39d19-107">Anwendungen sollten die [**mpradminportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) -Funktion verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="39d19-107">Applications should use the [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) function.\]</span></span>

<span data-ttu-id="39d19-108">Die **rasadminportgetinfo** -Funktion Ruft Informationen zu einem angegebenen Port auf einem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="39d19-108">The **RasAdminPortGetInfo** function retrieves information about a specified port on a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="39d19-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="39d19-109">Syntax</span></span>


```C++
DWORD RasAdminPortGetInfo(
  _In_  const WCHAR               *lpszServer,
  _In_  const WCHAR               *lpszPort,
  _Out_       RAS_PORT_1          *pRasPort1,
  _Out_       RAS_PORT_STATISTICS *pRasStats,
  _Out_       RAS_PARAMETERS      **ppRasParams
);
```



## <a name="parameters"></a><span data-ttu-id="39d19-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="39d19-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39d19-111">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39d19-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d19-112">Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des RAS-Servers angibt.</span><span class="sxs-lookup"><span data-stu-id="39d19-112">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="39d19-113">Geben Sie den Namen mit führenden " \\ \\ " Zeichen im folgenden Format an: \\ \\ *Servername*.</span><span class="sxs-lookup"><span data-stu-id="39d19-113">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="39d19-114">*lpszport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39d19-114">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d19-115">Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des Ports auf dem Server angibt.</span><span class="sxs-lookup"><span data-stu-id="39d19-115">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> <dt>

<span data-ttu-id="39d19-116">*pRasPort1* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="39d19-116">*pRasPort1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39d19-117">Ein Zeiger auf die [**RAS- \_ Port- \_ 1**](ras-port-1-str.md) -Struktur, die die Funktion mit Informationen über den Status des Ports füllt.</span><span class="sxs-lookup"><span data-stu-id="39d19-117">Pointer to the [**RAS\_PORT\_1**](ras-port-1-str.md) structure that the function fills in with information about the state of the port.</span></span>

</dd> <dt>

<span data-ttu-id="39d19-118">" *prasstats* \[ " vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="39d19-118">*pRasStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39d19-119">Ein Zeiger auf die Struktur der [**RAS- \_ Port \_ Statistik**](ras-port-statistics-str.md) , die die Funktion mit Statistiken zum Port füllt.</span><span class="sxs-lookup"><span data-stu-id="39d19-119">Pointer to the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure that the function fills in with statistics about the port.</span></span>

</dd> <dt>

<span data-ttu-id="39d19-120">*pprasparams* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="39d19-120">*ppRasParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39d19-121">Zeiger auf eine Zeiger Variable, die die Adresse eines Arrays von [**RAS- \_ Parameter**](ras-parameters-str.md) Strukturen empfängt.</span><span class="sxs-lookup"><span data-stu-id="39d19-121">Pointer to a pointer variable that receives the address of an array of [**RAS\_PARAMETERS**](ras-parameters-str.md) structures.</span></span> <span data-ttu-id="39d19-122">Jede Struktur enthält den Namen eines medienspezifischen Schlüssels (z. b. maxconnectbit/s) und den zugehörigen Wert.</span><span class="sxs-lookup"><span data-stu-id="39d19-122">Each structure contains the name of a media-specific key, such as MAXCONNECTBPS, and its associated value.</span></span> <span data-ttu-id="39d19-123">Wenn die Anwendung mit diesem Arbeitsspeicher fertig ist, können Sie Sie freigeben, indem Sie die [**rasadminfreebuffer**](rasadminfreebuffer.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="39d19-123">When the application is finished with this memory, free it by calling the [**RasAdminFreeBuffer**](rasadminfreebuffer.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39d19-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39d19-124">Return value</span></span>

<span data-ttu-id="39d19-125">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="39d19-125">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="39d19-126">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Fehlercodes sein.</span><span class="sxs-lookup"><span data-stu-id="39d19-126">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="39d19-127">Wert</span><span class="sxs-lookup"><span data-stu-id="39d19-127">Value</span></span>                                                                                                     | <span data-ttu-id="39d19-128">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="39d19-128">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="39d19-129"><dt>**Fehler \_ dev ist \_ nicht \_ vorhanden.**</dt></span><span class="sxs-lookup"><span data-stu-id="39d19-129"><dt>**ERROR\_DEV\_NOT\_EXIST**</dt></span></span> </dl>     | <span data-ttu-id="39d19-130">Der angegebene Port ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="39d19-130">The specified port is invalid.</span></span><br/>                                        |
| <dl> <span data-ttu-id="39d19-131"><dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="39d19-131"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="39d19-132">Nicht genügend Arbeitsspeicher, um einen Puffer für das *pprasparams* -Array zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="39d19-132">Insufficient memory to allocate a buffer for the *ppRasParams* array.</span></span><br/> |



 

<span data-ttu-id="39d19-133">Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="39d19-133">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="39d19-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39d19-134">Requirements</span></span>



| <span data-ttu-id="39d19-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39d19-135">Requirement</span></span> | <span data-ttu-id="39d19-136">Wert</span><span class="sxs-lookup"><span data-stu-id="39d19-136">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39d19-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="39d19-137">End of client support</span></span><br/> | <span data-ttu-id="39d19-138">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="39d19-138">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="39d19-139">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="39d19-139">End of server support</span></span><br/> | <span data-ttu-id="39d19-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39d19-140">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="39d19-141">Header</span><span class="sxs-lookup"><span data-stu-id="39d19-141">Header</span></span><br/>                | <dl> <span data-ttu-id="39d19-142"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="39d19-142"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="39d19-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="39d19-143">Library</span></span><br/>               | <dl> <span data-ttu-id="39d19-144"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39d19-144"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="39d19-145">DLL</span><span class="sxs-lookup"><span data-stu-id="39d19-145">DLL</span></span><br/>                   | <dl> <span data-ttu-id="39d19-146"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39d19-146"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39d19-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39d19-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39d19-148">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="39d19-148">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="39d19-149">RAS-Server-Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="39d19-149">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="39d19-150">**RAS- \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="39d19-150">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="39d19-151">**RAS- \_ Port \_ 1**</span><span class="sxs-lookup"><span data-stu-id="39d19-151">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="39d19-152">**RAS- \_ Port \_ Statistik**</span><span class="sxs-lookup"><span data-stu-id="39d19-152">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="39d19-153">**Rasadminfrebuffer**</span><span class="sxs-lookup"><span data-stu-id="39d19-153">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)
</dt> </dl>

 

