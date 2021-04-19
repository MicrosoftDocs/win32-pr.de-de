---
title: Rasadminservergetinfo-Funktion (rassapi. h)
description: Die rasadminservergetinfo-Funktion Ruft die Serverkonfiguration eines RAS-Servers ab.
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- Rasadminservergetinfo-Funktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminServerGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115a2421db5efbafb72d73952684ff7758c6995b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372637"
---
# <a name="rasadminservergetinfo-function"></a><span data-ttu-id="1af83-104">Rasadminservergetinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="1af83-104">RasAdminServerGetInfo function</span></span>

<span data-ttu-id="1af83-105">\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1af83-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="1af83-106">Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="1af83-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="1af83-107">Anwendungen sollten die [**mpradminservergetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) -Funktion verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="1af83-107">Applications should use the [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) function.\]</span></span>

<span data-ttu-id="1af83-108">Die **rasadminservergetinfo** -Funktion Ruft die Serverkonfiguration eines RAS-Servers ab.</span><span class="sxs-lookup"><span data-stu-id="1af83-108">The **RasAdminServerGetInfo** function gets the server configuration of a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1af83-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1af83-109">Syntax</span></span>


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a><span data-ttu-id="1af83-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1af83-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1af83-111">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1af83-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1af83-112">Zeiger auf eine mit **null** endenden Unicode-Zeichenfolge, die den Namen des Windows NT/Windows 2000-RAS-Servers angibt.</span><span class="sxs-lookup"><span data-stu-id="1af83-112">Pointer to a **null**-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="1af83-113">Wenn dieser Parameter **null** ist, gibt die Funktion Informationen über den lokalen Computer zurück.</span><span class="sxs-lookup"><span data-stu-id="1af83-113">If this parameter is **NULL**, the function returns information about the local computer.</span></span> <span data-ttu-id="1af83-114">Geben Sie den Namen mit führenden " \\ \\ " Zeichen im folgenden Format an: \\ \\ *Servername*.</span><span class="sxs-lookup"><span data-stu-id="1af83-114">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="1af83-115">*pRasServer0* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1af83-115">*pRasServer0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1af83-116">Ein Zeiger auf die [**RAS- \_ Server- \_ 0**](ras-server-0-str.md) -Struktur, die die Anzahl der auf dem Server konfigurierten Ports, die Anzahl der derzeit verwendeten Ports und die Server Versionsnummer empfängt.</span><span class="sxs-lookup"><span data-stu-id="1af83-116">Pointer to the [**RAS\_SERVER\_0**](ras-server-0-str.md) structure that receives the number of ports configured on the server, the number of ports currently in use, and the server version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1af83-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1af83-117">Return value</span></span>

<span data-ttu-id="1af83-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1af83-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="1af83-119">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1af83-119">If the function fails, the return value is an error code.</span></span> <span data-ttu-id="1af83-120">Mögliche Fehlercodes sind diejenigen, die von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) für die [**callnamedpipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1af83-120">Possible error codes include those returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) for the [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) function.</span></span> <span data-ttu-id="1af83-121">Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " **GetLastError**" nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1af83-121">There is no extended error information for this function; do not call **GetLastError**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1af83-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1af83-122">Remarks</span></span>

<span data-ttu-id="1af83-123">Um alle RAS-Server in einer Domäne aufzulisten, geben Sie die [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) -Funktion an, und geben Sie \_ \_ für den *Server Type* -Parameter den Befehl SV Type Dialin an.</span><span class="sxs-lookup"><span data-stu-id="1af83-123">To enumerate all RAS servers in a domain, call the [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) function and specify SV\_TYPE\_DIALIN for the *servertype* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="1af83-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1af83-124">Requirements</span></span>



| <span data-ttu-id="1af83-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1af83-125">Requirement</span></span> | <span data-ttu-id="1af83-126">Wert</span><span class="sxs-lookup"><span data-stu-id="1af83-126">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1af83-127">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1af83-127">End of client support</span></span><br/> | <span data-ttu-id="1af83-128">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1af83-128">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="1af83-129">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="1af83-129">End of server support</span></span><br/> | <span data-ttu-id="1af83-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1af83-130">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="1af83-131">Header</span><span class="sxs-lookup"><span data-stu-id="1af83-131">Header</span></span><br/>                | <dl> <span data-ttu-id="1af83-132"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1af83-132"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="1af83-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1af83-133">Library</span></span><br/>               | <dl> <span data-ttu-id="1af83-134"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1af83-134"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1af83-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1af83-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1af83-136"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1af83-136"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1af83-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1af83-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af83-138">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="1af83-138">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="1af83-139">RAS-Server-Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="1af83-139">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="1af83-140">**NetServerEnum**</span><span class="sxs-lookup"><span data-stu-id="1af83-140">**NetServerEnum**</span></span>](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[<span data-ttu-id="1af83-141">**RAS- \_ Server \_ 0**</span><span class="sxs-lookup"><span data-stu-id="1af83-141">**RAS\_SERVER\_0**</span></span>](ras-server-0-str.md)
</dt> </dl>

 

