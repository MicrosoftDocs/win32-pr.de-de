---
title: Cleanupkredentialcache-Funktion
description: Wird von bestimmten Security Support Provider (SSP) implementiert, um den SSP-Anmelde Informations Cache zu leeren.
ms.assetid: e60870e6-22d3-4321-abca-a5b9d2b0ce2d
keywords:
- Cleanupkredentialcache-Funktion WinInet
topic_type:
- apiref
api_name:
- CleanupCredentialCache
api_location:
- MSNSSPC.dll
- MSAPSSPC.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53464073dd59837ba8026bbec03118055fba20cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102927"
---
# <a name="cleanupcredentialcache-function"></a><span data-ttu-id="39e34-104">Cleanupkredentialcache-Funktion</span><span class="sxs-lookup"><span data-stu-id="39e34-104">CleanupCredentialCache function</span></span>

<span data-ttu-id="39e34-105">Die **cleanupkredentialcache** -Funktion wird von bestimmten SSP (Security Support Providers) implementiert, um den SSP-Anmelde Informations Cache zu leeren.</span><span class="sxs-lookup"><span data-stu-id="39e34-105">The **CleanupCredentialCache** function is implemented by certain Security Support Providers (SSP) to flush the SSP credential cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="39e34-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="39e34-106">Syntax</span></span>


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a><span data-ttu-id="39e34-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="39e34-107">Parameters</span></span>

<span data-ttu-id="39e34-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="39e34-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39e34-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39e34-109">Return value</span></span>

<span data-ttu-id="39e34-110">**True** , wenn die Funktion erfolgreich ausgeführt wird. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="39e34-110">**TRUE** if the function succeeds; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="39e34-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39e34-111">Remarks</span></span>

<span data-ttu-id="39e34-112">Die **cleanupkredentialcache** -Funktion wird von den folgenden SSPs implementiert:</span><span class="sxs-lookup"><span data-stu-id="39e34-112">The **CleanupCredentialCache** function is implemented by the following SSPs:</span></span>

-   <span data-ttu-id="39e34-113">MSNSSPC.dll</span><span class="sxs-lookup"><span data-stu-id="39e34-113">MSNSSPC.dll</span></span>
-   <span data-ttu-id="39e34-114">MSAPSSPC.dll</span><span class="sxs-lookup"><span data-stu-id="39e34-114">MSAPSSPC.dll</span></span>

<span data-ttu-id="39e34-115">Die Implementierung von **cleanupkredentialcache** durch diese SSPs gibt immer **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="39e34-115">The implementation of **CleanupCredentialCache** by these SSPs always returns **TRUE**.</span></span>

<span data-ttu-id="39e34-116">Bevor Sie versuchen, ein Modul Handle zum Exportieren von **cleanupkredentialcache** abzurufen, muss die Anwendung überprüfen, ob es sich bei dem geladenen SSP um eines der bekannten SSPs handelt, die die **cleanupkredentialcache** -Funktion implementieren.</span><span class="sxs-lookup"><span data-stu-id="39e34-116">Before attempting to obtain a module handle to export **CleanupCredentialCache**, the application must verify that the SSP that has been loaded is one of the known SSPs implementing the **CleanupCredentialCache** function.</span></span>

<span data-ttu-id="39e34-117">Um den SSP-Anmelde Informations Cache zu leeren, muss die Anwendung ein Modul Handle für den SSP abrufen, indem die [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="39e34-117">In order to flush the SSP credential cache, the application must obtain a module handle for the SSP by calling the [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function.</span></span> <span data-ttu-id="39e34-118">Nachdem das Modul abgerufen wurde, sollte die Anwendung die vom SSP implementierte **cleanupcredentialcache** -Funktion exportieren, indem Sie die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufruft und das von **GetModuleHandle** und **cleanupcredentialcache** zurückgegebene Modul als Eingabeparameter übergibt.</span><span class="sxs-lookup"><span data-stu-id="39e34-118">After obtaining the module, the application should export the **CleanupCredentialCache** function implemented by the SSP by calling the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function, passing the module returned by **GetModuleHandle** and **CleanupCredentialCache** as input parameters.</span></span>

<span data-ttu-id="39e34-119">Wie alle anderen Aspekte der WinInet-API kann diese Funktion nicht sicher innerhalb von DllMain oder den Konstruktoren und Dekonstruktoren von globalen Objekten aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="39e34-119">Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.</span></span>

> [!Note]  
> <span data-ttu-id="39e34-120">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="39e34-120">WinINet does not support server implementations.</span></span> <span data-ttu-id="39e34-121">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39e34-121">In addition, it should not be used from a service.</span></span> <span data-ttu-id="39e34-122">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="39e34-122">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="39e34-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39e34-123">Requirements</span></span>



| <span data-ttu-id="39e34-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39e34-124">Requirement</span></span> | <span data-ttu-id="39e34-125">Wert</span><span class="sxs-lookup"><span data-stu-id="39e34-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39e34-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39e34-126">Minimum supported client</span></span><br/> | <span data-ttu-id="39e34-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39e34-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                 |
| <span data-ttu-id="39e34-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39e34-128">Minimum supported server</span></span><br/> | <span data-ttu-id="39e34-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39e34-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                       |
| <span data-ttu-id="39e34-130">DLL</span><span class="sxs-lookup"><span data-stu-id="39e34-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39e34-131"><dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39e34-131"><dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt></span></span> </dl> |



 

