---
description: Ruft die Optionen ab, die einer DDE-Freigabe in der Liste Server Benutzer vertrauenswürdiger Freigaben zugeordnet sind.
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: Ndbegettrustedshare-Funktion (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetTrustedShare
- NDdeGetTrustedShareA
- NDdeGetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 1f8d7e79c48e0409d8040f6d44159c473dd58ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345469"
---
# <a name="nddegettrustedshare-function"></a><span data-ttu-id="43ee3-103">Nddebug Share-Funktion</span><span class="sxs-lookup"><span data-stu-id="43ee3-103">NDdeGetTrustedShare function</span></span>

<span data-ttu-id="43ee3-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="43ee3-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="43ee3-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="43ee3-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="43ee3-106">Ruft die einer DDE-Freigabe zugeordneten Optionen ab, die sich in der Liste der vertrauenswürdigen Freigaben des Server Benutzers befinden.</span><span class="sxs-lookup"><span data-stu-id="43ee3-106">Retrieves the options associated with a DDE share that is in the server user's list of trusted shares.</span></span>

## <a name="syntax"></a><span data-ttu-id="43ee3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="43ee3-107">Syntax</span></span>


```C++
UINT NDdeGetTrustedShare(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _Out_ LPDWORD lpdwTrustOptions,
  _Out_ LPDWORD lpdwShareModId0,
  _Out_ LPDWORD lpdwShareModId1
);
```



## <a name="parameters"></a><span data-ttu-id="43ee3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="43ee3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43ee3-109">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43ee3-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ee3-110">Der Name des Servers, auf dem sich die DSDM befindet.</span><span class="sxs-lookup"><span data-stu-id="43ee3-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="43ee3-111">*lpszsharename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43ee3-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ee3-112">Der Freigabe Name, dessen vertrauenswürdiger Status abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="43ee3-112">The share name whose trusted status is being queried.</span></span> <span data-ttu-id="43ee3-113">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="43ee3-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="43ee3-114">*lpdwtrustoptions* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="43ee3-114">*lpdwTrustOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43ee3-115">Ein Zeiger auf eine Variable, die die Vertrauensstellungs Optionen empfängt.</span><span class="sxs-lookup"><span data-stu-id="43ee3-115">A pointer to a variable that receives the trust options.</span></span> <span data-ttu-id="43ee3-116">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="43ee3-116">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="43ee3-117">Die folgenden Vertrauensstellungs Optionen sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="43ee3-117">The following trust options are available.</span></span>



| <span data-ttu-id="43ee3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="43ee3-118">Value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="43ee3-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="43ee3-119">Meaning</span></span>                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <span data-ttu-id="43ee3-120"><dt>**Ndde \_ Cmd \_ Show \_ Mask**</dt> <dt>0x0000ffffl</dt></span><span class="sxs-lookup"><span data-stu-id="43ee3-120"><dt>**NDDE\_CMD\_SHOW\_MASK**</dt> <dt>0x0000FFFFL</dt></span></span> </dl>             | <span data-ttu-id="43ee3-121">Maske, die zum Abrufen des Werts verwendet wird, mit dem der Status der DDE-Freigabe angezeigt wird, wenn ndde \_ Trust \_ cmd \_ Show festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="43ee3-121">Mask used to obtain the value used to override the DDE share show state, if NDDE\_TRUST\_CMD\_SHOW is set.</span></span><br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <span data-ttu-id="43ee3-122"><dt>**Ndde \_ Trust \_ cmd \_ Show**</dt> <dt>0x10000000l</dt></span><span class="sxs-lookup"><span data-stu-id="43ee3-122"><dt>**NDDE\_TRUST\_CMD\_SHOW**</dt> <dt>0x10000000L</dt></span></span> </dl>          | <span data-ttu-id="43ee3-123">Überschreiben Sie den Anzeige Zustand, der in der DDE-Freigabe DSDM angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="43ee3-123">Override the show state specified in the DDE share DSDM.</span></span><br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <span data-ttu-id="43ee3-124"><dt>**Ndde \_ Trust- \_ Freigabe \_ del**</dt> <dt>0x20000000l</dt></span><span class="sxs-lookup"><span data-stu-id="43ee3-124"><dt>**NDDE\_TRUST\_SHARE\_DEL**</dt> <dt>0x20000000L</dt></span></span> </dl>       | <span data-ttu-id="43ee3-125">Entfernen Sie den vertrauenswürdigen Status der Freigabe.</span><span class="sxs-lookup"><span data-stu-id="43ee3-125">Remove the share's trusted status.</span></span><br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <span data-ttu-id="43ee3-126"><dt>**Ndde \_ Vertrauens \_ Freigabe \_ Init**</dt> <dt>0x40000000l</dt></span><span class="sxs-lookup"><span data-stu-id="43ee3-126"><dt>**NDDE\_TRUST\_SHARE\_INIT**</dt> <dt>0x40000000L</dt></span></span> </dl>    | <span data-ttu-id="43ee3-127">Ermöglicht einem Client das Initiieren der Anwendung, wenn Sie bereits im Kontext des Benutzers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43ee3-127">Allow a client to initiate to the application if it is already running in the user's context.</span></span><br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <span data-ttu-id="43ee3-128"><dt>**Ndde \_ Vertrauens \_ Freigabe \_ Start**</dt> <dt>0x80000000l</dt></span><span class="sxs-lookup"><span data-stu-id="43ee3-128"><dt>**NDDE\_TRUST\_SHARE\_START**</dt> <dt>0x80000000L</dt></span></span> </dl> | <span data-ttu-id="43ee3-129">Ermöglicht das Starten der Anwendung im Kontext des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="43ee3-129">Allow the application to be started in the user's context.</span></span><br/>                                                 |



 

</dd> <dt>

<span data-ttu-id="43ee3-130">*lpdwShareModId0* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="43ee3-130">*lpdwShareModId0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43ee3-131">Ein Zeiger auf eine Variable, die den ersten Teil des Bezeichner der vertrauenswürdigen Freigabe Änderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="43ee3-131">A pointer to a variable that receives the first part of the trusted share modify identifier.</span></span> <span data-ttu-id="43ee3-132">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="43ee3-132">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="43ee3-133">*lpdwShareModId1* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="43ee3-133">*lpdwShareModId1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43ee3-134">Ein Zeiger auf eine Variable, die den zweiten Teil des Bezeichner der vertrauenswürdigen Freigabe Änderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="43ee3-134">A pointer to a variable that receives the second part of the trusted share modify identifier.</span></span> <span data-ttu-id="43ee3-135">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="43ee3-135">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43ee3-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43ee3-136">Return value</span></span>

<span data-ttu-id="43ee3-137">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".</span><span class="sxs-lookup"><span data-stu-id="43ee3-137">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="43ee3-138">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="43ee3-138">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="43ee3-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43ee3-139">Remarks</span></span>

<span data-ttu-id="43ee3-140">Der Bezeichner der vertrauenswürdigen Freigabe Änderung gibt die Version der DDE-Freigabe in der DSDM zum Zeitpunkt an, zu dem die DDE-Freigabe anfänglich den vertrauenswürdigen Status erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="43ee3-140">The trusted share modify identifier reflects the version of the DDE share in the DSDM at the time the DDE share was initially granted trusted status.</span></span> <span data-ttu-id="43ee3-141">Der Bezeichner der vertrauenswürdigen Freigabe Änderung wird hauptsächlich zum Entfernen veralteter vertrauenswürdiger Freigaben verwendet</span><span class="sxs-lookup"><span data-stu-id="43ee3-141">The trusted share modify identifier is primarily used to remove obsolete trusted shares.</span></span> <span data-ttu-id="43ee3-142">Der Benutzer muss jedoch keine veralteten vertrauenswürdigen Freigaben Entfernen.</span><span class="sxs-lookup"><span data-stu-id="43ee3-142">However, the user does not need to remove obsolete trusted shares.</span></span> <span data-ttu-id="43ee3-143">Der Netzwerk-DDE-Agent entfernt veraltete Freigaben im Auftrag des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="43ee3-143">The network DDE agent removes obsolete shares on the user's behalf.</span></span>

## <a name="requirements"></a><span data-ttu-id="43ee3-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43ee3-144">Requirements</span></span>



| <span data-ttu-id="43ee3-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43ee3-145">Requirement</span></span> | <span data-ttu-id="43ee3-146">Wert</span><span class="sxs-lookup"><span data-stu-id="43ee3-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43ee3-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43ee3-147">Minimum supported client</span></span><br/> | <span data-ttu-id="43ee3-148">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43ee3-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="43ee3-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43ee3-149">Minimum supported server</span></span><br/> | <span data-ttu-id="43ee3-150">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43ee3-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="43ee3-151">Header</span><span class="sxs-lookup"><span data-stu-id="43ee3-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="43ee3-152"><dt>Ndde API. h</dt></span><span class="sxs-lookup"><span data-stu-id="43ee3-152"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="43ee3-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="43ee3-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="43ee3-154"><dt>Ndde API. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43ee3-154"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="43ee3-155">DLL</span><span class="sxs-lookup"><span data-stu-id="43ee3-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43ee3-156"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43ee3-156"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="43ee3-157">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="43ee3-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="43ee3-158">**Nddebug** (Unicode) und **ndde gettrustedsharea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="43ee3-158">**NDdeGetTrustedShareW** (Unicode) and **NDdeGetTrustedShareA** (ANSI)</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="43ee3-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43ee3-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43ee3-160">Übersicht über das Netzwerk dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="43ee3-160">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="43ee3-161">Network DDE-Funktionen</span><span class="sxs-lookup"><span data-stu-id="43ee3-161">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="43ee3-162">**Ndabsettrustedshare**</span><span class="sxs-lookup"><span data-stu-id="43ee3-162">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)
</dt> </dl>

 

 




