---
title: Rasadminportdisconnect-Funktion (rassapi. h)
description: Die rasadminportdisconnect-Funktion trennt einen Port, der zurzeit verwendet wird.
ms.assetid: 7ed3bc46-2d56-44c8-afd5-fcbdad0f7f3a
keywords:
- Rasadminportdisconnect-Funktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminPortDisconnect
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee05e7927bd6c9adb086a09f76b9022affd74792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361384"
---
# <a name="rasadminportdisconnect-function"></a><span data-ttu-id="53785-104">Rasadminportdisconnect-Funktion</span><span class="sxs-lookup"><span data-stu-id="53785-104">RasAdminPortDisconnect function</span></span>

<span data-ttu-id="53785-105">\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="53785-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="53785-106">Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="53785-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="53785-107">Anwendungen sollten die [**mpradminportdisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) -Funktion verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="53785-107">Applications should use the [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) function.\]</span></span>

<span data-ttu-id="53785-108">Die **rasadminportdisconnect** -Funktion trennt einen Port, der zurzeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="53785-108">The **RasAdminPortDisconnect** function disconnects a port that is currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="53785-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="53785-109">Syntax</span></span>


```C++
DWORD RasAdminPortDisconnect(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a><span data-ttu-id="53785-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="53785-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53785-111">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53785-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53785-112">Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des Windows NT/Windows 2000-RAS-Servers angibt.</span><span class="sxs-lookup"><span data-stu-id="53785-112">Pointer to a null-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="53785-113">Geben Sie den Namen mit führenden " \\ \\ " Zeichen im folgenden Format an: \\ \\ *Servername*.</span><span class="sxs-lookup"><span data-stu-id="53785-113">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="53785-114">*lpszport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53785-114">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53785-115">Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des Ports auf dem Server angibt.</span><span class="sxs-lookup"><span data-stu-id="53785-115">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53785-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53785-116">Return value</span></span>

<span data-ttu-id="53785-117">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="53785-117">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="53785-118">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Fehlercodes sein.</span><span class="sxs-lookup"><span data-stu-id="53785-118">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="53785-119">Wert</span><span class="sxs-lookup"><span data-stu-id="53785-119">Value</span></span>                                                                                               | <span data-ttu-id="53785-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="53785-120">Meaning</span></span>                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="53785-121"><dt>**\_ungültiger \_ Port.**</dt></span><span class="sxs-lookup"><span data-stu-id="53785-121"><dt>**ERROR\_INVALID\_PORT**</dt></span></span> </dl> | <span data-ttu-id="53785-122">Der angegebene Port ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="53785-122">The specified port is invalid.</span></span><br/>    |
| <dl> <span data-ttu-id="53785-123"><dt>**NERR \_ usernotfound**</dt></span><span class="sxs-lookup"><span data-stu-id="53785-123"><dt>**NERR\_UserNotFound**</dt></span></span> </dl>   | <span data-ttu-id="53785-124">Der Port wird derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="53785-124">The port is not currently in use.</span></span><br/> |



 

<span data-ttu-id="53785-125">Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="53785-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="53785-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53785-126">Requirements</span></span>



| <span data-ttu-id="53785-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53785-127">Requirement</span></span> | <span data-ttu-id="53785-128">Wert</span><span class="sxs-lookup"><span data-stu-id="53785-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53785-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="53785-129">End of client support</span></span><br/> | <span data-ttu-id="53785-130">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="53785-130">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="53785-131">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="53785-131">End of server support</span></span><br/> | <span data-ttu-id="53785-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="53785-132">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="53785-133">Header</span><span class="sxs-lookup"><span data-stu-id="53785-133">Header</span></span><br/>                | <dl> <span data-ttu-id="53785-134"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="53785-134"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="53785-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="53785-135">Library</span></span><br/>               | <dl> <span data-ttu-id="53785-136"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53785-136"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="53785-137">DLL</span><span class="sxs-lookup"><span data-stu-id="53785-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="53785-138"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53785-138"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53785-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53785-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53785-140">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="53785-140">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="53785-141">RAS-Server-Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="53785-141">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> </dl>

 

