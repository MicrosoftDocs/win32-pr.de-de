---
title: Tlsgetservercertificate-Funktion
description: Gibt das Zertifikat des Remotedesktop Lizenzservers zurück.
ms.assetid: 7a31e7f9-f6d6-4030-b7db-43be118bb158
ms.tgt_platform: multiple
keywords:
- Tlsgetservercertificate-Funktion Remotedesktopdienste
topic_type:
- apiref
api_name:
- TLSGetServerCertificate
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3144245863ee4a4316bbce8333f03ca3901cb499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338130"
---
# <a name="tlsgetservercertificate-function"></a><span data-ttu-id="f130d-104">Tlsgetservercertificate-Funktion</span><span class="sxs-lookup"><span data-stu-id="f130d-104">TLSGetServerCertificate function</span></span>

<span data-ttu-id="f130d-105">Gibt das Zertifikat des Remotedesktop Lizenzservers zurück.</span><span class="sxs-lookup"><span data-stu-id="f130d-105">Returns the certificate of the Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="f130d-106">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="f130d-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="f130d-107">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mstlsapi.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="f130d-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f130d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f130d-108">Syntax</span></span>


```C++
DWORD WINAPI TLSGetServerCertificate(
  _In_  TLS_HANDLE hHandle,
  _In_  BOOL       bSignCert,
  _Out_ LPBYTE     *ppbCertBlob,
  _Out_ LPDWORD    lpdwCertBlobLen,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="f130d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f130d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f130d-110">*hHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f130d-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f130d-111">Handle für einen Remotedesktop Lizenzserver, der durch einen Rückruf der [**tlsconnecttolsserver**](tlsconnecttolsserver.md) -Funktion geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="f130d-111">Handle to a Remote Desktop license server that is opened by a call to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f130d-112">*bsigncert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f130d-112">*bSignCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f130d-113">**True** , wenn das Signaturzertifikat **false** ist, wenn Exchange-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="f130d-113">**TRUE** if signature certificate, **FALSE** if exchange certificate.</span></span>

</dd> <dt>

<span data-ttu-id="f130d-114">*ppbcertblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f130d-114">*ppbCertBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f130d-115">Ein Zeiger auf eine Variable, die einen Zeiger auf einen Puffer empfängt, der das Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="f130d-115">Pointer to a variable that receives a pointer to a buffer that contains the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="f130d-116">*lpdwcertbloblen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f130d-116">*lpdwCertBlobLen* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f130d-117">Ein Zeiger auf eine Variable, die die Größe des Zertifikats erhält, das zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f130d-117">Pointer to a variable that receives the size of the certificate that is returned.</span></span>

</dd> <dt>

<span data-ttu-id="f130d-118">*pdwerrcode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f130d-118">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f130d-119">Ein Zeiger auf eine Variable, die den Fehlercode empfängt.</span><span class="sxs-lookup"><span data-stu-id="f130d-119">Pointer to a variable that receives the error code.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="f130d-120"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ S \_ erfolgreich** (0)</span><span class="sxs-lookup"><span data-stu-id="f130d-120"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f130d-121">Der-Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f130d-121">Call is successful.</span></span>

</dd> <dt>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>

<span data-ttu-id="f130d-122"><span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS \_ W- \_ selfsign- \_ Zertifikat** (4007)</span><span class="sxs-lookup"><span data-stu-id="f130d-122"><span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS\_W\_SELFSIGN\_CERTIFICATE** (4007)</span></span>


</dt> <dd>

<span data-ttu-id="f130d-123">Das zurückgegebene Zertifikat ist ein selbst signiertes Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="f130d-123">Certificate returned is a self-signed certificate.</span></span>

</dd> <dt>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>

<span data-ttu-id="f130d-124"><span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS \_ W \_ Temp \_ selfsign- \_ Zertifikat** (4009)</span><span class="sxs-lookup"><span data-stu-id="f130d-124"><span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS\_W\_TEMP\_SELFSIGN\_CERT** (4009)</span></span>


</dt> <dd>

<span data-ttu-id="f130d-125">Das zurückgegebene Zertifikat ist temporär.</span><span class="sxs-lookup"><span data-stu-id="f130d-125">Certificate returned is temporary.</span></span>

</dd> <dt>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>

<span data-ttu-id="f130d-126"><span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS \_ E- \_ Zugriff \_ verweigert** (5003)</span><span class="sxs-lookup"><span data-stu-id="f130d-126"><span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS\_E\_ACCESS\_DENIED** (5003)</span></span>


</dt> <dd>

<span data-ttu-id="f130d-127">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="f130d-127">Access denied.</span></span>

</dd> <dt>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>

<span data-ttu-id="f130d-128"><span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS \_ E Zuordnungs \_ \_ handle** (5007)</span><span class="sxs-lookup"><span data-stu-id="f130d-128"><span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS\_E\_ALLOCATE\_HANDLE** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="f130d-129">Der Server ist zu stark ausgelastet, um die Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f130d-129">Server is too busy to process the request.</span></span>

</dd> <dt>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>

<span data-ttu-id="f130d-130"><span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS \_ E \_ kein \_ Zertifikat** (5022)</span><span class="sxs-lookup"><span data-stu-id="f130d-130"><span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS\_E\_NO\_CERTIFICATE** (5022)</span></span>


</dt> <dd>

<span data-ttu-id="f130d-131">Ein Zertifikat kann nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f130d-131">Cannot retrieve a certificate.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f130d-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f130d-132">Return value</span></span>

<span data-ttu-id="f130d-133">Diese Funktion gibt die folgenden möglichen Rückgabewerte zurück.</span><span class="sxs-lookup"><span data-stu-id="f130d-133">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="f130d-134">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="f130d-134">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="f130d-135">Der-Befehl wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f130d-135">The call succeeded.</span></span> <span data-ttu-id="f130d-136">Überprüfen Sie den Wert des Parameters " *pdwerrcode* ", um den Rückgabecode für den-Befehl abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f130d-136">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="f130d-137">**RPC \_ S \_ ungültig \_**</span><span class="sxs-lookup"><span data-stu-id="f130d-137">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="f130d-138">Das Argument war ungültig.</span><span class="sxs-lookup"><span data-stu-id="f130d-138">The argument was invalid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f130d-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f130d-139">Requirements</span></span>



| <span data-ttu-id="f130d-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f130d-140">Requirement</span></span> | <span data-ttu-id="f130d-141">Wert</span><span class="sxs-lookup"><span data-stu-id="f130d-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f130d-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f130d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f130d-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f130d-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f130d-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f130d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f130d-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f130d-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f130d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="f130d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f130d-147"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f130d-147"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f130d-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f130d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f130d-149">**Tlsconnecttolsserver**</span><span class="sxs-lookup"><span data-stu-id="f130d-149">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> </dl>

 

