---
title: Tlsdisconnectfromserver-Funktion
description: Schließt ein geöffnetes Handle für einen Remotedesktop-Lizenzserver.
ms.assetid: b4b001ec-823b-4514-bbec-839a83a9a189
ms.tgt_platform: multiple
keywords:
- Tlsdisconnectfromserver-Funktion Remotedesktopdienste
topic_type:
- apiref
api_name:
- TLSDisconnectFromServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 265a6b04186bd640943cf2b348dda7afcf8f712a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342669"
---
# <a name="tlsdisconnectfromserver-function"></a><span data-ttu-id="a2ae6-104">Tlsdisconnectfromserver-Funktion</span><span class="sxs-lookup"><span data-stu-id="a2ae6-104">TLSDisconnectFromServer function</span></span>

<span data-ttu-id="a2ae6-105">Schließt ein geöffnetes Handle für einen Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="a2ae6-105">Closes an open handle to a Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="a2ae6-106">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="a2ae6-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="a2ae6-107">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mstlsapi.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="a2ae6-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a2ae6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2ae6-108">Syntax</span></span>


```C++
void WINAPI TLSDisconnectFromServer(
  _In_ TLS_HANDLE hHandle
);
```



## <a name="parameters"></a><span data-ttu-id="a2ae6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2ae6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2ae6-110">*hHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2ae6-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ae6-111">Handle für einen Remotedesktop Lizenzserver, der durch einen Rückruf der [**tlsconnecttolsserver**](tlsconnecttolsserver.md) -Funktion geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="a2ae6-111">Handle to a Remote Desktop license server that is opened by a call to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2ae6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2ae6-112">Return value</span></span>

<span data-ttu-id="a2ae6-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a2ae6-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2ae6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2ae6-114">Remarks</span></span>

<span data-ttu-id="a2ae6-115">Rufen Sie die **tlsdisconnectfromserver** -Funktion als Teil der cleanuproutine Ihres Programms auf, um alle Server Handles zu schließen, die durch Aufrufe der [**tlsconnecttolsserver**](tlsconnecttolsserver.md) -Funktion geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="a2ae6-115">Call the **TLSDisconnectFromServer** function as part of your program's clean-up routine to close all the server handles that are opened by calls to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2ae6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2ae6-116">Requirements</span></span>



| <span data-ttu-id="a2ae6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2ae6-117">Requirement</span></span> | <span data-ttu-id="a2ae6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a2ae6-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ae6-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2ae6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a2ae6-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2ae6-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2ae6-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2ae6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a2ae6-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2ae6-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2ae6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a2ae6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2ae6-124"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2ae6-124"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2ae6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2ae6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ae6-126">**TLS- \_ handle**</span><span class="sxs-lookup"><span data-stu-id="a2ae6-126">**TLS\_HANDLE**</span></span>](tls-handle.md)
</dt> <dt>

[<span data-ttu-id="a2ae6-127">**Tlsconnecttolsserver**</span><span class="sxs-lookup"><span data-stu-id="a2ae6-127">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> </dl>

 

