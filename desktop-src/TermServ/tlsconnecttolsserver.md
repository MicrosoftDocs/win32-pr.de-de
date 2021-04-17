---
title: Tlsconnecttolsserver-Funktion
description: Öffnet ein Handle für die angegebene Remotedesktop Lizenzservers.
ms.assetid: 9e90a8e8-9319-42ee-b541-a1d028b6ed4d
ms.tgt_platform: multiple
keywords:
- Tlsconnecttolsserver-Funktion Remotedesktopdienste
topic_type:
- apiref
api_name:
- TLSConnectToLsServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7f36b519399f0a8c1627fad7c7768f36ece57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392015"
---
# <a name="tlsconnecttolsserver-function"></a><span data-ttu-id="c603e-104">Tlsconnecttolsserver-Funktion</span><span class="sxs-lookup"><span data-stu-id="c603e-104">TLSConnectToLsServer function</span></span>

<span data-ttu-id="c603e-105">Öffnet ein Handle für die angegebene Remotedesktop Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="c603e-105">Opens a handle to the specified Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="c603e-106">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="c603e-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="c603e-107">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mstlsapi.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="c603e-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c603e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c603e-108">Syntax</span></span>


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a><span data-ttu-id="c603e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c603e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c603e-110">*pszlsserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c603e-110">*pszLsServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c603e-111">Zeiger auf eine mit **null** endenden Zeichenfolge, die den NetBIOS-Namen des Remotedesktop Lizenzservers angibt.</span><span class="sxs-lookup"><span data-stu-id="c603e-111">Pointer to a **null**-terminated string that specifies the NetBIOS name of the Remote Desktop license server.</span></span> <span data-ttu-id="c603e-112">Wenn der Wert dieses Parameters **null** ist, ist der angegebene Server der lokale Computer.</span><span class="sxs-lookup"><span data-stu-id="c603e-112">If the value of this parameter is **NULL**, the specified server is the local computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c603e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c603e-113">Return value</span></span>

<span data-ttu-id="c603e-114">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Handle für den angegebenen Server.</span><span class="sxs-lookup"><span data-stu-id="c603e-114">If the function succeeds, the return value is a handle to the specified server.</span></span>

<span data-ttu-id="c603e-115">Wenn die Funktion fehlschlägt, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="c603e-115">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="c603e-116">Um erweiterte Fehlerinformationen abzurufen, müssen Sie die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c603e-116">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="c603e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c603e-117">Remarks</span></span>

<span data-ttu-id="c603e-118">Wenn Sie mit der Verwendung des Handles, das von der **tlsconnecttolsserver** -Funktion zurückgegeben wird, fertig sind, geben Sie es durch Aufrufen der [**tlsdisconnectfromserver**](tlsdisconnectfromserver.md) -Funktion frei.</span><span class="sxs-lookup"><span data-stu-id="c603e-118">When you have finished using the handle that is returned by the **TLSConnectToLsServer** function, release it by calling the [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c603e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c603e-119">Requirements</span></span>



| <span data-ttu-id="c603e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c603e-120">Requirement</span></span> | <span data-ttu-id="c603e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c603e-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c603e-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c603e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c603e-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c603e-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c603e-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c603e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c603e-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c603e-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c603e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c603e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c603e-127"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c603e-127"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c603e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c603e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c603e-129">**TLS- \_ handle**</span><span class="sxs-lookup"><span data-stu-id="c603e-129">**TLS\_HANDLE**</span></span>](tls-handle.md)
</dt> <dt>

[<span data-ttu-id="c603e-130">**Tlsdisconnectfromserver**</span><span class="sxs-lookup"><span data-stu-id="c603e-130">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> </dl>

 

