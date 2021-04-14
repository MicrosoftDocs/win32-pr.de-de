---
title: Tlslicensenumnext-Funktion
description: Wird von einem vorherigen aufrufsvorgang der tlslicenseenumbegin-Funktion fortgesetzt und gibt die nächste Lizenz zurück, die auf einem Remotedesktop Lizenzserver installiert ist, der den Suchkriterien entspricht.
ms.assetid: 6932289b-b59c-493c-8dbc-03c0662e921e
ms.tgt_platform: multiple
keywords:
- Tlslicensenumnext-Funktion Remotedesktopdienste
topic_type:
- apiref
api_name:
- TLSLicenseEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c13b0a3137258015fe311c49b2cc9b999e3a13f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392210"
---
# <a name="tlslicenseenumnext-function"></a><span data-ttu-id="1d46c-104">Tlslicensenumnext-Funktion</span><span class="sxs-lookup"><span data-stu-id="1d46c-104">TLSLicenseEnumNext function</span></span>

<span data-ttu-id="1d46c-105">Wird von einem vorherigen aufrufsvorgang der [**tlslicenseenumbegin**](tlslicenseenumbegin.md) -Funktion fortgesetzt und gibt die nächste Lizenz zurück, die auf einem Remotedesktop Lizenzserver installiert ist, der den Suchkriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="1d46c-105">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and returns the next license that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="1d46c-106">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="1d46c-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="1d46c-107">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mstlsapi.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="1d46c-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1d46c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d46c-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LSLicense  *lpLicense,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="1d46c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d46c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d46c-110">*hHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d46c-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d46c-111">Handle für einen Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="1d46c-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="1d46c-112">Geben Sie ein Handle an, das von der [**tlsconnecttolsserver**](tlsconnecttolsserver.md) -Funktion geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="1d46c-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="1d46c-113">*lplicense* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d46c-113">*lpLicense* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d46c-114">Ein Zeiger auf eine [**lslicense**](lslicense.md) -Struktur, die die nächste Lizenz empfängt, die den Suchkriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="1d46c-114">Pointer to a [**LSLicense**](lslicense.md) structure that receives the next license that matches the search criteria.</span></span>

</dd> <dt>

<span data-ttu-id="1d46c-115">*pdwerrcode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1d46c-115">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d46c-116">Ein Zeiger auf eine Variable, die bei der Rückgabe einen der folgenden Fehlercodes empfängt.</span><span class="sxs-lookup"><span data-stu-id="1d46c-116">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="1d46c-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ S \_ erfolgreich** (0)</span><span class="sxs-lookup"><span data-stu-id="1d46c-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1d46c-118">Der-Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d46c-118">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span data-ttu-id="1d46c-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**Lserver \_ \_Keine \_ weiteren \_ Daten** (4001)</span><span class="sxs-lookup"><span data-stu-id="1d46c-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER\_I\_NO\_MORE\_DATA** (4001)</span></span>


</dt> <dd>

<span data-ttu-id="1d46c-120">Keine weiteren Lizenzen stimmen mit den Suchkriterien überein.</span><span class="sxs-lookup"><span data-stu-id="1d46c-120">No more licenses match the search criteria.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="1d46c-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Lserver \_ Interner E- \_ \_ Fehler** (5001)</span><span class="sxs-lookup"><span data-stu-id="1d46c-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="1d46c-122">Interner Fehler auf dem Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="1d46c-122">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="1d46c-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Lserver \_ E \_ ungültige \_ Reihenfolge** (5006)</span><span class="sxs-lookup"><span data-stu-id="1d46c-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="1d46c-124">Die Aufruf Sequenz war nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="1d46c-124">The calling sequence was not valid.</span></span> <span data-ttu-id="1d46c-125">Vor diesem muss die [**tlslicenseenumbegin ()**](tlslicenseenumbegin.md) -Funktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1d46c-125">Must call the [**TLSLicenseEnumBegin()**](tlslicenseenumbegin.md) function before this.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="1d46c-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**Lserver \_ E- \_ Server \_ ausgelastet** (5007)</span><span class="sxs-lookup"><span data-stu-id="1d46c-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="1d46c-127">Der Lizenzserver ist zu stark ausgelastet, um die Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1d46c-127">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="1d46c-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**Lserver \_ E \_ outo-Memory** (5008)</span><span class="sxs-lookup"><span data-stu-id="1d46c-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="1d46c-129">Die Anforderung kann aufgrund von unzureichendem Arbeitsspeicher nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1d46c-129">Cannot process the request because of insufficient memory.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d46c-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d46c-130">Return value</span></span>

<span data-ttu-id="1d46c-131">Diese Funktion gibt die folgenden möglichen Rückgabewerte zurück.</span><span class="sxs-lookup"><span data-stu-id="1d46c-131">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="1d46c-132">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="1d46c-132">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="1d46c-133">Der-Befehl wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d46c-133">The call succeeded.</span></span> <span data-ttu-id="1d46c-134">Überprüfen Sie den Wert des Parameters " *pdwerrcode* ", um den Rückgabecode für den-Befehl abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1d46c-134">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="1d46c-135">**RPC \_ S \_ ungültig \_**</span><span class="sxs-lookup"><span data-stu-id="1d46c-135">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="1d46c-136">Das Argument war ungültig.</span><span class="sxs-lookup"><span data-stu-id="1d46c-136">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d46c-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d46c-137">Requirements</span></span>



| <span data-ttu-id="1d46c-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d46c-138">Requirement</span></span> | <span data-ttu-id="1d46c-139">Wert</span><span class="sxs-lookup"><span data-stu-id="1d46c-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d46c-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d46c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1d46c-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d46c-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d46c-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d46c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1d46c-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d46c-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d46c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1d46c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d46c-145"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d46c-145"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d46c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d46c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d46c-147">**Lslicense**</span><span class="sxs-lookup"><span data-stu-id="1d46c-147">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="1d46c-148">**Tlsconnecttolsserver**</span><span class="sxs-lookup"><span data-stu-id="1d46c-148">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="1d46c-149">**Tlslicenseenumbegin**</span><span class="sxs-lookup"><span data-stu-id="1d46c-149">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="1d46c-150">**Tlslicenabenumend**</span><span class="sxs-lookup"><span data-stu-id="1d46c-150">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

