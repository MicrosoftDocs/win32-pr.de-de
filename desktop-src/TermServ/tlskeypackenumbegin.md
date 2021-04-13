---
title: Tlskeypackenumbegin-Funktion
description: Beginnt die Enumeration über alle auf einem Remotedesktop Lizenzserver installierten Schlüsselpakete auf der Grundlage von Suchkriterien.
ms.assetid: 2d847fe4-66ab-42df-8213-651e14257590
ms.tgt_platform: multiple
keywords:
- Tlskeypackenumbegin-Funktion Remotedesktopdienste
topic_type:
- apiref
api_name:
- TLSKeyPackEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db8f61197e3c08f5608be954a9288ea54cad5586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341257"
---
# <a name="tlskeypackenumbegin-function"></a><span data-ttu-id="bfffb-104">Tlskeypackenumbegin-Funktion</span><span class="sxs-lookup"><span data-stu-id="bfffb-104">TLSKeyPackEnumBegin function</span></span>

<span data-ttu-id="bfffb-105">Beginnt die Enumeration über alle auf einem Remotedesktop Lizenzserver installierten Schlüsselpakete auf der Grundlage von Suchkriterien.</span><span class="sxs-lookup"><span data-stu-id="bfffb-105">Begins enumeration through all key packs that are installed on a Remote Desktop license server based on search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="bfffb-106">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="bfffb-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="bfffb-107">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mstlsapi.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="bfffb-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bfffb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfffb-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSKeyPack  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="bfffb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfffb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfffb-110">*hHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfffb-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfffb-111">Handle für einen Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="bfffb-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="bfffb-112">Geben Sie ein Handle an, das von der [**tlsconnecttolsserver**](tlsconnecttolsserver.md) -Funktion geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="bfffb-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="bfffb-113">*dwsearchparser* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfffb-113">*dwSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfffb-114">Gibt die Suchkriterien an.</span><span class="sxs-lookup"><span data-stu-id="bfffb-114">Specifies the search criteria.</span></span> <span data-ttu-id="bfffb-115">Dieser Parameter ist für die zukünftige Verwendung reserviert und muss 0xFFFFFFFF enthalten.</span><span class="sxs-lookup"><span data-stu-id="bfffb-115">This parameter is reserved for future use and must contain 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="bfffb-116">*bmatchall* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfffb-116">*bMatchAll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfffb-117">Gibt an, ob alle Suchwerte abgeglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bfffb-117">Specifies whether to match all search values.</span></span>

</dd> <dt>

<span data-ttu-id="bfffb-118">*lpsearchparameminm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfffb-118">*lpSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfffb-119">Ein Zeiger auf eine [**lschräypack**](lskeypack.md) -Struktur, die die Suchparameter angibt, nach denen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="bfffb-119">Pointer to a [**LSKeyPack**](lskeypack.md) structure that specifies the search parameters to look for.</span></span>

</dd> <dt>

<span data-ttu-id="bfffb-120">*pdwerrcode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bfffb-120">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfffb-121">Ein Zeiger auf eine Variable, die bei der Rückgabe einen der folgenden Fehlercodes empfängt.</span><span class="sxs-lookup"><span data-stu-id="bfffb-121">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="bfffb-122"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ S \_ erfolgreich** (0)</span><span class="sxs-lookup"><span data-stu-id="bfffb-122"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bfffb-123">Der-Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bfffb-123">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="bfffb-124"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Lserver \_ Interner E- \_ \_ Fehler** (5001)</span><span class="sxs-lookup"><span data-stu-id="bfffb-124"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="bfffb-125">Interner Fehler auf dem Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="bfffb-125">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="bfffb-126"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Lserver \_ E \_ ungültige \_ Reihenfolge** (5006)</span><span class="sxs-lookup"><span data-stu-id="bfffb-126"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="bfffb-127">Die Aufruf Sequenz war nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="bfffb-127">The calling sequence was not valid.</span></span> <span data-ttu-id="bfffb-128">Höchstwahrscheinlich wurde eine vorherige Enumeration nicht beendet.</span><span class="sxs-lookup"><span data-stu-id="bfffb-128">Most likely, a previous enumeration has not ended.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="bfffb-129"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**Lserver \_ E- \_ Server \_ ausgelastet** (5007)</span><span class="sxs-lookup"><span data-stu-id="bfffb-129"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="bfffb-130">Der Lizenzserver ist zu stark ausgelastet, um die Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="bfffb-130">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="bfffb-131"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**Lserver \_ E \_ outo-Memory** (5008)</span><span class="sxs-lookup"><span data-stu-id="bfffb-131"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="bfffb-132">Die Anforderung kann aufgrund von unzureichendem Arbeitsspeicher nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="bfffb-132">Cannot process the request because of insufficient memory.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span data-ttu-id="bfffb-133"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**Lserver \_ E \_ ungültige \_ Daten** (5009)</span><span class="sxs-lookup"><span data-stu-id="bfffb-133"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER\_E\_INVALID\_DATA** (5009)</span></span>


</dt> <dd>

<span data-ttu-id="bfffb-134">Die Daten im Suchparameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="bfffb-134">Data in the search parameter is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfffb-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bfffb-135">Return value</span></span>

<span data-ttu-id="bfffb-136">Diese Funktion gibt die folgenden möglichen Rückgabewerte zurück.</span><span class="sxs-lookup"><span data-stu-id="bfffb-136">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="bfffb-137">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="bfffb-137">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="bfffb-138">Der-Befehl wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bfffb-138">The call succeeded.</span></span> <span data-ttu-id="bfffb-139">Überprüfen Sie den Wert des Parameters " *pdwerrcode* ", um den Rückgabecode für den-Befehl abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bfffb-139">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="bfffb-140">**RPC \_ S \_ ungültig \_**</span><span class="sxs-lookup"><span data-stu-id="bfffb-140">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="bfffb-141">Das Argument war ungültig.</span><span class="sxs-lookup"><span data-stu-id="bfffb-141">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfffb-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfffb-142">Requirements</span></span>



| <span data-ttu-id="bfffb-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfffb-143">Requirement</span></span> | <span data-ttu-id="bfffb-144">Wert</span><span class="sxs-lookup"><span data-stu-id="bfffb-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfffb-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfffb-145">Minimum supported client</span></span><br/> | <span data-ttu-id="bfffb-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bfffb-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bfffb-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfffb-147">Minimum supported server</span></span><br/> | <span data-ttu-id="bfffb-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfffb-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bfffb-149">DLL</span><span class="sxs-lookup"><span data-stu-id="bfffb-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfffb-150"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfffb-150"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfffb-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfffb-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfffb-152">**Lschräypack**</span><span class="sxs-lookup"><span data-stu-id="bfffb-152">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="bfffb-153">**Tlsconnecttolsserver**</span><span class="sxs-lookup"><span data-stu-id="bfffb-153">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="bfffb-154">**Tlskeypackenumnext**</span><span class="sxs-lookup"><span data-stu-id="bfffb-154">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dt>

[<span data-ttu-id="bfffb-155">**Tlskeypackenumend**</span><span class="sxs-lookup"><span data-stu-id="bfffb-155">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

