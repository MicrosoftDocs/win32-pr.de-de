---
description: Gewährt dem angegebenen Status "DDE-Freigabe vertrauenswürdig" im Kontext des aktuellen Benutzers.
ms.assetid: 508d3603-468c-4ecb-8e5c-0ab86c2ff3b4
title: Ndabsettrustedshare-Funktion (ndbeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetTrustedShare
- NDdeSetTrustedShareA
- NDdeSetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 459e1621848e212522064ff6f01316fc23183bc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524953"
---
# <a name="nddesettrustedshare-function"></a><span data-ttu-id="d9a49-103">Ndabsettrustedshare-Funktion</span><span class="sxs-lookup"><span data-stu-id="d9a49-103">NDdeSetTrustedShare function</span></span>

<span data-ttu-id="d9a49-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d9a49-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="d9a49-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="d9a49-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="d9a49-106">Gewährt der angegebenen DDE-Freigabe den vertrauenswürdigen Status im Kontext des aktuellen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="d9a49-106">Grants the specified DDE share trusted status within the current user's context.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a49-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9a49-107">Syntax</span></span>


```C++
UINT NDdeSetTrustedShare(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ DWORD  dwTrustOptions
);
```



## <a name="parameters"></a><span data-ttu-id="d9a49-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9a49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9a49-109">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9a49-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a49-110">Der Name des Servers, dessen DSDM geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9a49-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="d9a49-111">*lpszsharename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9a49-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a49-112">Der Name der Freigabe, der der vertrauenswürdige Status zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9a49-112">The name of the share to be granted trusted status.</span></span> <span data-ttu-id="d9a49-113">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="d9a49-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d9a49-114">*dwtrustoptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9a49-114">*dwTrustOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a49-115">Die Optionen, die sich auf den vertrauenswürdigen Status der DDE-Freigabe auswirken.</span><span class="sxs-lookup"><span data-stu-id="d9a49-115">The options affecting the trusted status of the DDE share.</span></span> <span data-ttu-id="d9a49-116">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="d9a49-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d9a49-117">Option</span><span class="sxs-lookup"><span data-stu-id="d9a49-117">Option</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="d9a49-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d9a49-118">Meaning</span></span>                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <span data-ttu-id="d9a49-119"><dt>**Ndde \_ Cmd \_ Show \_ Mask**</dt> <dt>0x0000ffffl</dt></span><span class="sxs-lookup"><span data-stu-id="d9a49-119"><dt>**NDDE\_CMD\_SHOW\_MASK**</dt> <dt>0x0000FFFFL</dt></span></span> </dl>             | <span data-ttu-id="d9a49-120">Maske, die zum Abrufen des Werts verwendet wird, mit dem der Status der DDE-Freigabe angezeigt wird, wenn ndde \_ Trust \_ cmd \_ Show festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d9a49-120">Mask used to obtain the value used to override the DDE share show state, if NDDE\_TRUST\_CMD\_SHOW is set.</span></span><br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <span data-ttu-id="d9a49-121"><dt>**Ndde \_ Trust \_ cmd \_ Show**</dt> <dt>0x10000000l</dt></span><span class="sxs-lookup"><span data-stu-id="d9a49-121"><dt>**NDDE\_TRUST\_CMD\_SHOW**</dt> <dt>0x10000000L</dt></span></span> </dl>          | <span data-ttu-id="d9a49-122">Überschreiben Sie den Anzeige Zustand, der in der DDE-Freigabe DSDM angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d9a49-122">Override the show state specified in the DDE share DSDM.</span></span><br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <span data-ttu-id="d9a49-123"><dt>**Ndde \_ Trust- \_ Freigabe \_ del**</dt> <dt>0x20000000l</dt></span><span class="sxs-lookup"><span data-stu-id="d9a49-123"><dt>**NDDE\_TRUST\_SHARE\_DEL**</dt> <dt>0x20000000L</dt></span></span> </dl>       | <span data-ttu-id="d9a49-124">Entfernen Sie den vertrauenswürdigen Status der Freigabe.</span><span class="sxs-lookup"><span data-stu-id="d9a49-124">Remove the share's trusted status.</span></span><br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <span data-ttu-id="d9a49-125"><dt>**Ndde \_ Vertrauens \_ Freigabe \_ Init**</dt> <dt>0x40000000l</dt></span><span class="sxs-lookup"><span data-stu-id="d9a49-125"><dt>**NDDE\_TRUST\_SHARE\_INIT**</dt> <dt>0x40000000L</dt></span></span> </dl>    | <span data-ttu-id="d9a49-126">Ermöglicht einem Client das Initiieren der Anwendung, wenn Sie bereits im Kontext des Benutzers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9a49-126">Allow a client to initiate to the application if it is already running in the user's context.</span></span><br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <span data-ttu-id="d9a49-127"><dt>**Ndde \_ Vertrauens \_ Freigabe \_ Start**</dt> <dt>0x80000000l</dt></span><span class="sxs-lookup"><span data-stu-id="d9a49-127"><dt>**NDDE\_TRUST\_SHARE\_START**</dt> <dt>0x80000000L</dt></span></span> </dl> | <span data-ttu-id="d9a49-128">Ermöglicht das Starten der Anwendung im Kontext des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="d9a49-128">Allow the application to be started in the user's context.</span></span><br/>                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9a49-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9a49-129">Return value</span></span>

<span data-ttu-id="d9a49-130">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".</span><span class="sxs-lookup"><span data-stu-id="d9a49-130">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="d9a49-131">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d9a49-131">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d9a49-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9a49-132">Remarks</span></span>

<span data-ttu-id="d9a49-133">Die DDE-Freigabe muss zunächst mit [**ndabshareadd**](nddeshareadd.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d9a49-133">The DDE share must first be created with [**NDdeShareAdd**](nddeshareadd.md).</span></span>

<span data-ttu-id="d9a49-134">Wenn **nddesettrustedshare** aufgerufen wird und *dwtrustoptions* auf NULL festgelegt ist, verliert die vertrauenswürdige Freigabe ihren vertrauenswürdigen Status.</span><span class="sxs-lookup"><span data-stu-id="d9a49-134">If **NDdeSetTrustedShare** is called with *dwTrustOptions* set to zero, the trusted share loses its trusted status.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9a49-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9a49-135">Requirements</span></span>



| <span data-ttu-id="d9a49-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9a49-136">Requirement</span></span> | <span data-ttu-id="d9a49-137">Wert</span><span class="sxs-lookup"><span data-stu-id="d9a49-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a49-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9a49-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d9a49-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9a49-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d9a49-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9a49-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d9a49-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9a49-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d9a49-142">Header</span><span class="sxs-lookup"><span data-stu-id="d9a49-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9a49-143"><dt>Ndde API. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9a49-143"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="d9a49-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d9a49-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9a49-145"><dt>Ndde API. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9a49-145"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d9a49-146">DLL</span><span class="sxs-lookup"><span data-stu-id="d9a49-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9a49-147"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9a49-147"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="d9a49-148">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="d9a49-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d9a49-149">**Ndabsettrustedsharew** (Unicode) und **ndabsettrustedsharea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d9a49-149">**NDdeSetTrustedShareW** (Unicode) and **NDdeSetTrustedShareA** (ANSI)</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="d9a49-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9a49-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9a49-151">Übersicht über das Netzwerk dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="d9a49-151">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="d9a49-152">Network DDE-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d9a49-152">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="d9a49-153">**Ndabshareadd**</span><span class="sxs-lookup"><span data-stu-id="d9a49-153">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




