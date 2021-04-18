---
title: Rasadminportenum-Funktion (rassapi. h)
description: Die rasadminportenum-Funktion Listet alle Ports auf dem angegebenen RAS-Server auf. Für jeden Port auf dem Server gibt die-Funktion die RAS- \_ Port \_ 0-Struktur zurück, die Informationen über den Port enthält.
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- Rasadminportenum-Funktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminPortEnum
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e4841627ce5df3feee3f885b399a070388ed55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352982"
---
# <a name="rasadminportenum-function"></a><span data-ttu-id="56821-105">Rasadminportenum-Funktion</span><span class="sxs-lookup"><span data-stu-id="56821-105">RasAdminPortEnum function</span></span>

<span data-ttu-id="56821-106">\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="56821-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="56821-107">Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="56821-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="56821-108">Anwendungen sollten die [**mpradminportenum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) -Funktion verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="56821-108">Applications should use the [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) function.\]</span></span>

<span data-ttu-id="56821-109">Die **rasadminportenum** -Funktion Listet alle Ports auf dem angegebenen RAS-Server auf.</span><span class="sxs-lookup"><span data-stu-id="56821-109">The **RasAdminPortEnum** function enumerates all ports on the specified RAS server.</span></span> <span data-ttu-id="56821-110">Für jeden Port auf dem Server gibt die-Funktion die [**RAS- \_ Port \_ 0**](ras-port-0-str.md) -Struktur zurück, die Informationen über den Port enthält.</span><span class="sxs-lookup"><span data-stu-id="56821-110">For each port on the server, the function returns the [**RAS\_PORT\_0**](ras-port-0-str.md) structure that contains information about the port.</span></span>

## <a name="syntax"></a><span data-ttu-id="56821-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="56821-111">Syntax</span></span>


```C++
DWORD RasAdminPortEnum(
  _In_  const WCHAR       *lpszServer,
  _Out_       PRAS_PORT_0 *ppRasPort0,
  _Out_       WORD        *pcEntriesRead
);
```



## <a name="parameters"></a><span data-ttu-id="56821-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="56821-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56821-113">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56821-113">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56821-114">Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des RAS-Servers angibt.</span><span class="sxs-lookup"><span data-stu-id="56821-114">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="56821-115">Geben Sie den Namen mit führenden " \\ \\ " Zeichen im folgenden Format an: \\ \\ *Servername*.</span><span class="sxs-lookup"><span data-stu-id="56821-115">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="56821-116">*ppRasPort0* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="56821-116">*ppRasPort0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56821-117">Ein Zeiger auf eine Variable, die einen Zeiger auf einen Puffer empfängt, der ein Array von [**RAS- \_ Port \_ 0**](ras-port-0-str.md) -Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="56821-117">Pointer to a variable that receives a pointer to a buffer that contains an array of [**RAS\_PORT\_0**](ras-port-0-str.md) structures.</span></span> <span data-ttu-id="56821-118">Wenn die Anwendung mit dem Arbeitsspeicher fertig ist, können Sie Sie freigeben, indem Sie die [**rasadminfreebuffer**](rasadminfreebuffer.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="56821-118">When the application has finished with the memory, free it by calling the [**RasAdminFreeBuffer**](rasadminfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="56821-119">*pcentriesread* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="56821-119">*pcEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56821-120">Ein Zeiger auf eine 16-Bit-Variable, die die Gesamtzahl der [**RAS- \_ Port \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) -Strukturen empfängt, die im *ppRasPort0* -Array zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="56821-120">Pointer to a 16-bit variable that receives the total number of [**RAS\_PORT\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) structures returned in the *ppRasPort0* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56821-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56821-121">Return value</span></span>

<span data-ttu-id="56821-122">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="56821-122">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="56821-123">Wenn die Funktion fehlschlägt, kann der folgende Fehlercode als Rückgabewert zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="56821-123">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="56821-124">Wert</span><span class="sxs-lookup"><span data-stu-id="56821-124">Value</span></span>                                                                                             | <span data-ttu-id="56821-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="56821-125">Meaning</span></span>                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="56821-126"><dt>**NERR \_ ItemNotFound**</dt></span><span class="sxs-lookup"><span data-stu-id="56821-126"><dt>**NERR\_ItemNotFound**</dt></span></span> </dl> | <span data-ttu-id="56821-127">Es konnten keine Ports aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="56821-127">No ports could be enumerated.</span></span> <span data-ttu-id="56821-128">Dies liegt möglicherweise daran, dass alle konfigurierten Ports auf dem Server zurzeit für die Abwahl verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56821-128">This could be because all configured ports on the server are currently being used for dialing out.</span></span><br/> |



 

<span data-ttu-id="56821-129">Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="56821-129">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="56821-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56821-130">Requirements</span></span>



| <span data-ttu-id="56821-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56821-131">Requirement</span></span> | <span data-ttu-id="56821-132">Wert</span><span class="sxs-lookup"><span data-stu-id="56821-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56821-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="56821-133">End of client support</span></span><br/> | <span data-ttu-id="56821-134">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="56821-134">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="56821-135">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="56821-135">End of server support</span></span><br/> | <span data-ttu-id="56821-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="56821-136">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="56821-137">Header</span><span class="sxs-lookup"><span data-stu-id="56821-137">Header</span></span><br/>                | <dl> <span data-ttu-id="56821-138"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="56821-138"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="56821-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="56821-139">Library</span></span><br/>               | <dl> <span data-ttu-id="56821-140"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56821-140"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="56821-141">DLL</span><span class="sxs-lookup"><span data-stu-id="56821-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="56821-142"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56821-142"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56821-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56821-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56821-144">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="56821-144">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="56821-145">RAS-Server-Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="56821-145">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="56821-146">**RAS- \_ Port \_ 0**</span><span class="sxs-lookup"><span data-stu-id="56821-146">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="56821-147">**Rasadminfrebuffer**</span><span class="sxs-lookup"><span data-stu-id="56821-147">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)
</dt> </dl>

 

