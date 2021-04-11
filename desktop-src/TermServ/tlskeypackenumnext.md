---
title: Tlskeypackenumnext-Funktion
description: Wird von einem vorherigen-Befehl der tlskeypackenumbegin-Funktion fortgesetzt und gibt das nächste Key Pack zurück, das auf einem Remotedesktop-Lizenzserver installiert ist, der den Suchkriterien entspricht.
ms.assetid: 2614eb7a-df57-42a6-ad34-0a3211a6b8c3
ms.tgt_platform: multiple
keywords:
- Tlskeypackenumnext-Funktion Remotedesktopdienste
topic_type:
- apiref
api_name:
- TLSKeyPackEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897874f333ed7933ea1616f7f5ba5f1686736d0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040202"
---
# <a name="tlskeypackenumnext-function"></a><span data-ttu-id="e8b98-104">Tlskeypackenumnext-Funktion</span><span class="sxs-lookup"><span data-stu-id="e8b98-104">TLSKeyPackEnumNext function</span></span>

<span data-ttu-id="e8b98-105">Wird von einem vorherigen-Befehl der [**tlskeypackenumbegin**](tlskeypackenumbegin.md) -Funktion fortgesetzt und gibt das nächste Key Pack zurück, das auf einem Remotedesktop-Lizenzserver installiert ist, der den Suchkriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="e8b98-105">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and returns the next key pack that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="e8b98-106">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="e8b98-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="e8b98-107">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mstlsapi.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="e8b98-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e8b98-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8b98-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LsKeyPack  *lpKeyPack,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="e8b98-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8b98-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8b98-110">*hHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8b98-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8b98-111">Handle für einen Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="e8b98-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="e8b98-112">Geben Sie ein Handle an, das von der [**tlsconnecttolsserver**](tlsconnecttolsserver.md) -Funktion geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="e8b98-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e8b98-113">*lpkeypack* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8b98-113">*lpKeyPack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8b98-114">Ein Zeiger auf eine [**lschräypack**](lskeypack.md) -Struktur, die das nächste Key Pack empfängt, das mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="e8b98-114">Pointer to a [**LSKeyPack**](lskeypack.md) structure that receives the next key pack that matches the search criteria.</span></span>

</dd> <dt>

<span data-ttu-id="e8b98-115">*pdwerrcode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e8b98-115">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8b98-116">Ein Zeiger auf eine Variable, die bei der Rückgabe einen der folgenden Fehlercodes empfängt.</span><span class="sxs-lookup"><span data-stu-id="e8b98-116">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="e8b98-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ S \_ erfolgreich** (0)</span><span class="sxs-lookup"><span data-stu-id="e8b98-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e8b98-118">Der-Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8b98-118">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span data-ttu-id="e8b98-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**Lserver \_ \_Keine \_ weiteren \_ Daten** (4001)</span><span class="sxs-lookup"><span data-stu-id="e8b98-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER\_I\_NO\_MORE\_DATA** (4001)</span></span>


</dt> <dd>

<span data-ttu-id="e8b98-120">Es sind keine weiteren Schlüsselpakete mit den Suchkriterien übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e8b98-120">No more key packs match the search criteria.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="e8b98-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Lserver \_ Interner E- \_ \_ Fehler** (5001)</span><span class="sxs-lookup"><span data-stu-id="e8b98-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="e8b98-122">Interner Fehler auf dem Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="e8b98-122">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="e8b98-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Lserver \_ E \_ ungültige \_ Reihenfolge** (5006)</span><span class="sxs-lookup"><span data-stu-id="e8b98-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="e8b98-124">Die Aufruf Sequenz war nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="e8b98-124">The calling sequence was not valid.</span></span> <span data-ttu-id="e8b98-125">Vor diesem muss die [**tlskeypackenumbegin ()**](tlskeypackenumbegin.md) -Funktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e8b98-125">Must call the [**TLSKeyPackEnumBegin()**](tlskeypackenumbegin.md) function before this.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="e8b98-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**Lserver \_ E- \_ Server \_ ausgelastet** (5007)</span><span class="sxs-lookup"><span data-stu-id="e8b98-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="e8b98-127">Der Lizenzserver ist zu stark ausgelastet, um die Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e8b98-127">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="e8b98-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**Lserver \_ E \_ outo-Memory** (5008)</span><span class="sxs-lookup"><span data-stu-id="e8b98-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="e8b98-129">Die Anforderung kann aufgrund von unzureichendem Arbeitsspeicher nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="e8b98-129">Cannot process the request because of insufficient memory.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8b98-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8b98-130">Return value</span></span>

<span data-ttu-id="e8b98-131">Diese Funktion gibt die folgenden möglichen Rückgabewerte zurück.</span><span class="sxs-lookup"><span data-stu-id="e8b98-131">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="e8b98-132">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="e8b98-132">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="e8b98-133">Der-Befehl wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8b98-133">The call succeeded.</span></span> <span data-ttu-id="e8b98-134">Überprüfen Sie den Wert des Parameters " *pdwerrcode* ", um den Rückgabecode für den-Befehl abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e8b98-134">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="e8b98-135">**RPC \_ S \_ ungültig \_**</span><span class="sxs-lookup"><span data-stu-id="e8b98-135">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="e8b98-136">Das Argument war ungültig.</span><span class="sxs-lookup"><span data-stu-id="e8b98-136">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8b98-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8b98-137">Requirements</span></span>



| <span data-ttu-id="e8b98-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8b98-138">Requirement</span></span> | <span data-ttu-id="e8b98-139">Wert</span><span class="sxs-lookup"><span data-stu-id="e8b98-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b98-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8b98-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e8b98-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8b98-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e8b98-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8b98-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e8b98-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8b98-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e8b98-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e8b98-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8b98-145"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8b98-145"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8b98-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8b98-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b98-147">**Lschräypack**</span><span class="sxs-lookup"><span data-stu-id="e8b98-147">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="e8b98-148">**Tlsconnecttolsserver**</span><span class="sxs-lookup"><span data-stu-id="e8b98-148">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="e8b98-149">**Tlskeypackenumbegin**</span><span class="sxs-lookup"><span data-stu-id="e8b98-149">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="e8b98-150">**Tlskeypackenumend**</span><span class="sxs-lookup"><span data-stu-id="e8b98-150">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

