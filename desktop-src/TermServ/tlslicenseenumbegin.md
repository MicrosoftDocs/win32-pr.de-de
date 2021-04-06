---
title: Tlslicenseenumbegin-Funktion
description: Beginnt die Enumeration von Lizenzen, die vom Remotedesktop Lizenzserver basierend auf Suchkriterien ausgestellt werden.
ms.assetid: ec575632-b828-49c0-b326-1ab420381875
ms.tgt_platform: multiple
keywords:
- Tlslicenseenumbegin-Funktion Remotedesktopdienste
topic_type:
- apiref
api_name:
- TLSLicenseEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95913337de968d0b30780b5898b7f204d947dd4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743608"
---
# <a name="tlslicenseenumbegin-function"></a><span data-ttu-id="884e0-104">Tlslicenseenumbegin-Funktion</span><span class="sxs-lookup"><span data-stu-id="884e0-104">TLSLicenseEnumBegin function</span></span>

<span data-ttu-id="884e0-105">Beginnt die Enumeration von Lizenzen, die vom Remotedesktop Lizenzserver basierend auf Suchkriterien ausgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="884e0-105">Begins enumeration of licenses that are issued by the Remote Desktop license server based on search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="884e0-106">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="884e0-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="884e0-107">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mstlsapi.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="884e0-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="884e0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="884e0-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSLicense  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="884e0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="884e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="884e0-110">*hHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="884e0-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="884e0-111">Handle für einen Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="884e0-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="884e0-112">Geben Sie ein Handle an, das von der [**tlsconnecttolsserver**](tlsconnecttolsserver.md) -Funktion geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="884e0-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="884e0-113">*dwsearchparser* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="884e0-113">*dwSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="884e0-114">Gibt die Suchkriterien an.</span><span class="sxs-lookup"><span data-stu-id="884e0-114">Specifies the search criteria.</span></span> <span data-ttu-id="884e0-115">Der-Parameter kann eine oder eine Kombination der Werte sein, die in der folgenden Liste beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="884e0-115">The parameter can be one or a combination of the values that are described in the following list.</span></span> <span data-ttu-id="884e0-116">Der-Parameter gibt den Typ des Schlüssel Pakets und das zu durchsuchende Key Pack an.</span><span class="sxs-lookup"><span data-stu-id="884e0-116">The parameter specifies the type of key pack and which key pack to search.</span></span>

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span data-ttu-id="884e0-117"><span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**Lslicense \_ Durchsuchen von \_ licenseid** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="884e0-117"><span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE\_SEARCH\_LICENSEID** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-118">Suchen Sie nach Lizenz-ID.</span><span class="sxs-lookup"><span data-stu-id="884e0-118">Search by license ID.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span data-ttu-id="884e0-119"><span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**Lslicense \_ \_Keypackid suchen** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="884e0-119"><span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE\_SEARCH\_KEYPACKID** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-120">Suchen Sie nach Key Pack-ID.</span><span class="sxs-lookup"><span data-stu-id="884e0-120">Search by key pack ID.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span data-ttu-id="884e0-121"><span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**Lslicense \_ \_MachineName suchen** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="884e0-121"><span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE\_SEARCH\_MACHINENAME** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-122">Nach Computernamen suchen.</span><span class="sxs-lookup"><span data-stu-id="884e0-122">Search by machine name.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span data-ttu-id="884e0-123"><span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**Lslicense \_ \_Benutzername suchen** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="884e0-123"><span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE\_SEARCH\_USERNAME** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-124">Suchen Sie nach Benutzername.</span><span class="sxs-lookup"><span data-stu-id="884e0-124">Search by user name.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span data-ttu-id="884e0-125"><span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**Lslicense \_ Suche \_ IssueDate** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="884e0-125"><span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE\_SEARCH\_ISSUEDATE** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-126">Nach Ausgabedatum suchen.</span><span class="sxs-lookup"><span data-stu-id="884e0-126">Search by issue date.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span data-ttu-id="884e0-127"><span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**Lslicense \_ Durchsuchen von \_ ExpireDate** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="884e0-127"><span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE\_SEARCH\_EXPIREDATE** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-128">Nach Ablaufdatum suchen.</span><span class="sxs-lookup"><span data-stu-id="884e0-128">Search by expiration date.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span data-ttu-id="884e0-129"><span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**Lslicense \_ \_ Numlicenses suchen** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="884e0-129"><span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE\_SEARCH\_ NUMLICENSES** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-130">Suchen Sie nach Anzahl der Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="884e0-130">Search by number of licenses.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span data-ttu-id="884e0-131"><span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**Lslicense \_ Such \_ Eintrags \_ Status** (0x20000000)</span><span class="sxs-lookup"><span data-stu-id="884e0-131"><span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE\_SEARCH\_ ENTRY\_STATUS** (0x20000000)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-132">Nach Eintrags Status suchen.</span><span class="sxs-lookup"><span data-stu-id="884e0-132">Search by entry status.</span></span>

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span data-ttu-id="884e0-133"><span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**Lslicense \_ ExSearch \_ licenstatusstatus** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="884e0-133"><span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE\_EXSEARCH\_LICENSESTATUS** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-134">Suchen Sie nach Lizenzstatus.</span><span class="sxs-lookup"><span data-stu-id="884e0-134">Search by license status.</span></span>

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span data-ttu-id="884e0-135"><span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**Lschräypack \_ \_Alle suchen** (0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="884e0-135"><span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK\_SEARCH\_ALL** (0xFFFFFFFF)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-136">Alle Lizenzen suchen.</span><span class="sxs-lookup"><span data-stu-id="884e0-136">Search all licenses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="884e0-137">*bmatchall* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="884e0-137">*bMatchAll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="884e0-138">Gibt an, ob alle Suchwerte abgeglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="884e0-138">Specifies whether to match all search values.</span></span>

</dd> <dt>

<span data-ttu-id="884e0-139">*lpsearchparameminm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="884e0-139">*lpSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="884e0-140">Ein Zeiger auf eine [**lslicense**](lslicense.md) -Struktur, die die Suchparameter angibt, nach denen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="884e0-140">Pointer to a [**LSLicense**](lslicense.md) structure that specifies the search parameters to look for.</span></span>

</dd> <dt>

<span data-ttu-id="884e0-141">*pdwerrcode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="884e0-141">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="884e0-142">Ein Zeiger auf eine Variable, die bei der Rückgabe einen der folgenden Fehlercodes empfängt.</span><span class="sxs-lookup"><span data-stu-id="884e0-142">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="884e0-143"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ S \_ erfolgreich** (0)</span><span class="sxs-lookup"><span data-stu-id="884e0-143"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-144">Der-Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="884e0-144">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="884e0-145"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Lserver \_ Interner E- \_ \_ Fehler** (5001)</span><span class="sxs-lookup"><span data-stu-id="884e0-145"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-146">Interner Fehler auf dem Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="884e0-146">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="884e0-147"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Lserver \_ E \_ ungültige \_ Reihenfolge** (5006)</span><span class="sxs-lookup"><span data-stu-id="884e0-147"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-148">Die Aufruf Sequenz war nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="884e0-148">The calling sequence was not valid.</span></span> <span data-ttu-id="884e0-149">Höchstwahrscheinlich wurde eine vorherige Enumeration nicht beendet.</span><span class="sxs-lookup"><span data-stu-id="884e0-149">Most likely, a previous enumeration has not ended.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="884e0-150"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**Lserver \_ E- \_ Server \_ ausgelastet** (5007)</span><span class="sxs-lookup"><span data-stu-id="884e0-150"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-151">Der Lizenzserver ist zu stark ausgelastet, um die Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="884e0-151">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="884e0-152"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**Lserver \_ E \_ outo-Memory** (5008)</span><span class="sxs-lookup"><span data-stu-id="884e0-152"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-153">Die Anforderung kann aufgrund von unzureichendem Arbeitsspeicher nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="884e0-153">Cannot process the request because of insufficient memory.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span data-ttu-id="884e0-154"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**Lserver \_ E \_ ungültige \_ Daten** (5009)</span><span class="sxs-lookup"><span data-stu-id="884e0-154"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER\_E\_INVALID\_DATA** (5009)</span></span>


</dt> <dd>

<span data-ttu-id="884e0-155">Die Daten im Suchparameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="884e0-155">Data in the search parameter is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="884e0-156">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="884e0-156">Return value</span></span>

<span data-ttu-id="884e0-157">Diese Funktion gibt die folgenden möglichen Rückgabewerte zurück.</span><span class="sxs-lookup"><span data-stu-id="884e0-157">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="884e0-158">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="884e0-158">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="884e0-159">Der-Befehl wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="884e0-159">The call succeeded.</span></span> <span data-ttu-id="884e0-160">Überprüfen Sie den Wert des Parameters " *pdwerrcode* ", um den Rückgabecode für den-Befehl abzurufen.</span><span class="sxs-lookup"><span data-stu-id="884e0-160">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="884e0-161">**RPC \_ S \_ ungültig \_**</span><span class="sxs-lookup"><span data-stu-id="884e0-161">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="884e0-162">Das Argument war ungültig.</span><span class="sxs-lookup"><span data-stu-id="884e0-162">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="884e0-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="884e0-163">Requirements</span></span>



| <span data-ttu-id="884e0-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="884e0-164">Requirement</span></span> | <span data-ttu-id="884e0-165">Wert</span><span class="sxs-lookup"><span data-stu-id="884e0-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="884e0-166">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="884e0-166">Minimum supported client</span></span><br/> | <span data-ttu-id="884e0-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="884e0-167">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="884e0-168">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="884e0-168">Minimum supported server</span></span><br/> | <span data-ttu-id="884e0-169">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="884e0-169">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="884e0-170">DLL</span><span class="sxs-lookup"><span data-stu-id="884e0-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="884e0-171"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="884e0-171"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="884e0-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="884e0-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="884e0-173">**Lslicense**</span><span class="sxs-lookup"><span data-stu-id="884e0-173">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="884e0-174">**Tlsconnecttolsserver**</span><span class="sxs-lookup"><span data-stu-id="884e0-174">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="884e0-175">**Tlslicensitztenenumnext**</span><span class="sxs-lookup"><span data-stu-id="884e0-175">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dt>

[<span data-ttu-id="884e0-176">**Tlslicenabenumend**</span><span class="sxs-lookup"><span data-stu-id="884e0-176">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

