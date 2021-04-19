---
title: Tlslicenabenumend-Funktion
description: Wird von einem vorherigen-Befehl der tlslicenseenumbegin-Funktion fortgesetzt und beendet die-Enumeration.
ms.assetid: b9cba03c-0f5a-41e8-ae13-bcdd0ac6dd99
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der tlslicenabenumend-Funktion
topic_type:
- apiref
api_name:
- TLSLicenseEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bbd494ec539ee78008fa3df274282da1e9db6c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344710"
---
# <a name="tlslicenseenumend-function"></a><span data-ttu-id="47c97-104">Tlslicenabenumend-Funktion</span><span class="sxs-lookup"><span data-stu-id="47c97-104">TLSLicenseEnumEnd function</span></span>

<span data-ttu-id="47c97-105">Wird von einem vorherigen-Befehl der [**tlslicenseenumbegin**](tlslicenseenumbegin.md) -Funktion fortgesetzt und beendet die-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="47c97-105">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and terminates the enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="47c97-106">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="47c97-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="47c97-107">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mstlsapi.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="47c97-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="47c97-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="47c97-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumEnd(
  _In_  TLS_HANDLE hHandle,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="47c97-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="47c97-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47c97-110">*hHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47c97-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c97-111">Handle für einen Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="47c97-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="47c97-112">Geben Sie ein Handle an, das von der [**tlsconnecttolsserver**](tlsconnecttolsserver.md) -Funktion geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="47c97-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="47c97-113">*pdwerrcode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="47c97-113">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47c97-114">Ein Zeiger auf eine Variable, die bei der Rückgabe einen der folgenden Fehlercodes empfängt.</span><span class="sxs-lookup"><span data-stu-id="47c97-114">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="47c97-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ S \_ erfolgreich** (0)</span><span class="sxs-lookup"><span data-stu-id="47c97-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="47c97-116">Der-Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47c97-116">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>

<span data-ttu-id="47c97-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**Lserver \_ E \_ ungültiges \_ handle** (5005)</span><span class="sxs-lookup"><span data-stu-id="47c97-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER\_E\_INVALID\_HANDLE** (5005)</span></span>


</dt> <dd>

<span data-ttu-id="47c97-118">Das Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="47c97-118">The handle is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47c97-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47c97-119">Return value</span></span>

<span data-ttu-id="47c97-120">Diese Funktion gibt die folgenden möglichen Rückgabewerte zurück.</span><span class="sxs-lookup"><span data-stu-id="47c97-120">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="47c97-121">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="47c97-121">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="47c97-122">Der-Befehl wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47c97-122">The call succeeded.</span></span> <span data-ttu-id="47c97-123">Überprüfen Sie den Wert des Parameters " *pdwerrcode* ", um den Rückgabecode für den-Befehl abzurufen.</span><span class="sxs-lookup"><span data-stu-id="47c97-123">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="47c97-124">**RPC \_ S \_ ungültig \_**</span><span class="sxs-lookup"><span data-stu-id="47c97-124">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="47c97-125">Das Argument war ungültig.</span><span class="sxs-lookup"><span data-stu-id="47c97-125">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47c97-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47c97-126">Requirements</span></span>



| <span data-ttu-id="47c97-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47c97-127">Requirement</span></span> | <span data-ttu-id="47c97-128">Wert</span><span class="sxs-lookup"><span data-stu-id="47c97-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47c97-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47c97-129">Minimum supported client</span></span><br/> | <span data-ttu-id="47c97-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47c97-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="47c97-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47c97-131">Minimum supported server</span></span><br/> | <span data-ttu-id="47c97-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47c97-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="47c97-133">DLL</span><span class="sxs-lookup"><span data-stu-id="47c97-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47c97-134"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47c97-134"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47c97-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47c97-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c97-136">**Lslicense**</span><span class="sxs-lookup"><span data-stu-id="47c97-136">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="47c97-137">**Tlsconnecttolsserver**</span><span class="sxs-lookup"><span data-stu-id="47c97-137">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="47c97-138">**Tlslicenseenumbegin**</span><span class="sxs-lookup"><span data-stu-id="47c97-138">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="47c97-139">**Tlslicensitztenenumnext**</span><span class="sxs-lookup"><span data-stu-id="47c97-139">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> </dl>

 

