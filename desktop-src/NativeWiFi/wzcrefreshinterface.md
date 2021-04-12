---
description: Aktualisiert Schnittstellen Informationen für eine bestimmte drahtlose LAN-Schnittstelle.
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: Wzkrefreshinterface-Funktion (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCRefreshInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 3f2ac1bd546403dca781b3a132b44f96d80bb5c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348109"
---
# <a name="wzcrefreshinterface-function"></a><span data-ttu-id="75641-103">Wzkrefreshinterface-Funktion</span><span class="sxs-lookup"><span data-stu-id="75641-103">WZCRefreshInterface function</span></span>

<span data-ttu-id="75641-104">\[**Wzkrefreshinterface** wird ab Windows Vista und Windows Server 2008 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="75641-104">\[**WZCRefreshInterface** is not supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="75641-105">Verwenden Sie stattdessen die [native WiFi-API](native-wifi-reference.md), die eine ähnliche Funktionalität bietet.</span><span class="sxs-lookup"><span data-stu-id="75641-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="75641-106">Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="75641-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="75641-107">Die **wzkrefreshinterface** -Funktion aktualisiert Schnittstellen Informationen für eine bestimmte drahtlose LAN-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="75641-107">The **WZCRefreshInterface** function refreshes interface information for a specific wireless LAN interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="75641-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="75641-108">Syntax</span></span>


```C++
DWORD WZCRefreshInterface(
  _In_  LPWSTR      pSrvAddr,
  _In_  DWORD       dwInFlags,
  _In_  PINTF_ENTRY pIntf,
  _Out_ LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a><span data-ttu-id="75641-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="75641-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75641-110">*psrvaddr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75641-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75641-111">Ein Zeiger auf eine Zeichenfolge, die den Namen des Computers enthält, auf dem diese Funktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="75641-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="75641-112">Wenn dieser Parameter **null** ist, wird der Konfigurations Dienst für drahtlose NULL auf dem lokalen Computer aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="75641-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is called on the local computer.</span></span>

<span data-ttu-id="75641-113">Wenn der angegebene *psrvaddr* -Parameter ein Remote Computer ist, muss der Remote Computer Remote-RPC-Aufrufe unterstützen.</span><span class="sxs-lookup"><span data-stu-id="75641-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="75641-114">*dwInFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75641-114">*dwInFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75641-115">Eine Gruppe von Feldern, die zusammen mit bestimmten Aktualisierungs Aktionen aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="75641-115">A set of fields to be refreshed along with specific refresh actions to be taken.</span></span> <span data-ttu-id="75641-116">Dabei handelt es sich um eine Bitmaske, die eine beliebige Kombination der folgenden Flags enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="75641-116">This is a bitmask that can contain any combination of the following flags.</span></span>



| <span data-ttu-id="75641-117">Wert</span><span class="sxs-lookup"><span data-stu-id="75641-117">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="75641-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="75641-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <span data-ttu-id="75641-119"><dt>**INTF \_ Descr**</dt> <dt>0x00010000 bis</dt></span><span class="sxs-lookup"><span data-stu-id="75641-119"><dt>**INTF\_DESCR**</dt> <dt>0x00010000</dt></span></span> </dl>             | <span data-ttu-id="75641-120">Aktualisieren Sie die Schnittstellen Beschreibung für eine drahtlose LAN-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="75641-120">Refresh the interface description for a wireless LAN interface.</span></span><br/> <span data-ttu-id="75641-121">Die aktualisierte Schnittstellen Beschreibung kann abgerufen werden, indem Sie die [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion aufrufen, wobei das **INTF- \_ descr** -Bit im *dwInFlags* -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="75641-121">The refreshed interface description can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function with the **INTF\_DESCR** bit set in the *dwInFlags* parameter.</span></span> <span data-ttu-id="75641-122">Die Schnittstellen Beschreibung wird im **wszdescr** -Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurückgegeben, auf den der *pintf* -Parameter verweist, der von der **wzcqueryinterface** -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="75641-122">The interface description is returned in the **wszDescr** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter that is returned by the **WZCQueryInterface** function.</span></span><br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <span data-ttu-id="75641-123"><dt>**INTF \_ Ndismedia**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="75641-123"><dt>**INTF\_NDISMEDIA**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="75641-124">Aktualisieren Sie die NDIS-Medieninformationen für eine drahtlose LAN-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="75641-124">Refresh the NDIS media information for a wireless LAN interface.</span></span><br/> <span data-ttu-id="75641-125">Die aktualisierten NDIS-Medieninformationen können abgerufen werden, indem Sie die [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion mit dem **INTF \_ ndismedia** -Bit aufrufen, das im *dwInFlags* -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="75641-125">The refreshed NDIS media information can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function with the **INTF\_NDISMEDIA** bit set in the *dwInFlags* parameter.</span></span> <span data-ttu-id="75641-126">Die NDIS-Medieninformationen werden in den Elementen **ulmediastate**, **ulmediatype** und **ulphysicalmediatype** der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurückgegeben, auf die durch den *pintf* -Parameter verwiesen wird, der von der **wzcqueryinterface** -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="75641-126">The NDIS media information is returned in the **ulMediaState**, **ulMediaType**, and **ulPhysicalMediaType** members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter that is returned by the **WZCQueryInterface** function.</span></span><br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <span data-ttu-id="75641-127"><dt>**INTF \_ Alle \_ OIDs**</dt> <dt>0xfff00000</dt></span><span class="sxs-lookup"><span data-stu-id="75641-127"><dt>**INTF\_ALL\_OIDS**</dt> <dt>0xFFF00000</dt></span></span> </dl>   | <span data-ttu-id="75641-128">Aktualisieren Sie alle NDIS-OIDs für eine drahtlose LAN-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="75641-128">Refresh all of the NDIS OIDs for a wireless LAN interface.</span></span> <span data-ttu-id="75641-129">Mit dieser Option werden die meisten Daten für eine drahtlose LAN-Schnittstelle aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="75641-129">This option refreshes most of the data for a wireless LAN interface.</span></span><br/> <span data-ttu-id="75641-130">Die aktualisierten Informationen können durch Aufrufen der [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="75641-130">The refreshed information can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function.</span></span><br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="75641-131">*pintf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75641-131">*pIntf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75641-132">Ein Zeiger auf eine [**INTF- \_ Eintrags**](intf-entry.md) Struktur, die den Schlüssel der zu aktualisierenden Schnittstelle enthält.</span><span class="sxs-lookup"><span data-stu-id="75641-132">A pointer to an [**INTF\_ENTRY**](intf-entry.md) structure that contains the key of the interface to be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="75641-133">*pdwOutFlags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="75641-133">*pdwOutFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75641-134">Ein Satz von Feldern, die erfolgreich aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="75641-134">A set of fields that were successfully refreshed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75641-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75641-135">Return value</span></span>

<span data-ttu-id="75641-136">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="75641-136">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="75641-137">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Rückgabecodes sein.</span><span class="sxs-lookup"><span data-stu-id="75641-137">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="75641-138">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="75641-138">Return code</span></span>                                                                                              | <span data-ttu-id="75641-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75641-139">Description</span></span>                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="75641-140"><dt>**Fehler-Arena wurde durchlaufen \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="75641-140"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>     | <span data-ttu-id="75641-141">Die Speicher Kontroll Blöcke wurden zerstört.</span><span class="sxs-lookup"><span data-stu-id="75641-141">The storage control blocks were destroyed.</span></span> <span data-ttu-id="75641-142">Dieser Fehler wird zurückgegeben, wenn der Konfigurations Dienst für drahtlose NULL keine internen Objekte initialisiert hat.</span><span class="sxs-lookup"><span data-stu-id="75641-142">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="75641-143"><dt>**Fehler \_ Datei \_ nicht \_ gefunden.**</dt></span><span class="sxs-lookup"><span data-stu-id="75641-143"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="75641-144">Die angegebene Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="75641-144">The system cannot find the file specified.</span></span> <span data-ttu-id="75641-145">Dieser Fehler wird zurückgegeben, wenn die GUID im **wszguid** -Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur, auf die durch den *pintf* -Parameter verwiesen wird, nicht mit einer der Drahtlos-LAN-Schnittstellen auf dem lokalen Computer entsprach.</span><span class="sxs-lookup"><span data-stu-id="75641-145">This error is returned if the GUID in the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter did not match any of the wireless LAN interfaces on the local computer.</span></span> <br/> |
| <dl> <span data-ttu-id="75641-146"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="75641-146"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="75641-147">Ein Parameter ist falsch.</span><span class="sxs-lookup"><span data-stu-id="75641-147">A parameter is incorrect.</span></span> <span data-ttu-id="75641-148">Dieser Fehler wird zurückgegeben, wenn der *pintf* -Parameter **null** ist.</span><span class="sxs-lookup"><span data-stu-id="75641-148">This error is returned if the *pIntf* parameter is **NULL**.</span></span> <span data-ttu-id="75641-149">Dieser Fehler wird zurückgegeben, wenn das **wszguid** -Element der [**INTF- \_ Eintrags**](intf-entry.md) Struktur, auf die durch den *pintf* -Parameter verwiesen wird, **null** ist.</span><span class="sxs-lookup"><span data-stu-id="75641-149">This error is returned if the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter is **NULL**.</span></span> <br/>                            |
| <dl> <span data-ttu-id="75641-150"><dt>**RPC- \_ Status**</dt></span><span class="sxs-lookup"><span data-stu-id="75641-150"><dt>**RPC\_STATUS**</dt></span></span> </dl>               | <span data-ttu-id="75641-151">Verschiedene Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="75641-151">Various error codes.</span></span><br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="75641-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75641-152">Remarks</span></span>

<span data-ttu-id="75641-153">Der **wszguid** -Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur, auf den der *pintf* -Parameter verweist, muss eine Schnittstellen-GUID für eine drahtlose LAN-Schnittstelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="75641-153">The **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter must contain an interface GUID for a wireless LAN interface.</span></span> <span data-ttu-id="75641-154">Eine Liste der Drahtlos-LAN-Schnittstellen kann durch Aufrufen der [**wzcenumschlag Interfaces**](wzcenuminterfaces.md) -Funktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="75641-154">A list of wireless LAN interfaces can be retrieved by calling the [**WZCEnumInterfaces**](wzcenuminterfaces.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="75641-155">Die Header Datei " *wzcsapi. h* " und die Datei " *wzcsapi. lib* Import Library" sind im Windows SDK nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="75641-155">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="75641-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75641-156">Requirements</span></span>



| <span data-ttu-id="75641-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75641-157">Requirement</span></span> | <span data-ttu-id="75641-158">Wert</span><span class="sxs-lookup"><span data-stu-id="75641-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75641-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75641-159">Minimum supported client</span></span><br/> | <span data-ttu-id="75641-160">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75641-160">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="75641-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75641-161">Minimum supported server</span></span><br/> | <span data-ttu-id="75641-162">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75641-162">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="75641-163">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="75641-163">End of client support</span></span><br/>    | <span data-ttu-id="75641-164">Windows XP mit SP3</span><span class="sxs-lookup"><span data-stu-id="75641-164">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="75641-165">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="75641-165">End of server support</span></span><br/>    | <span data-ttu-id="75641-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="75641-166">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="75641-167">Header</span><span class="sxs-lookup"><span data-stu-id="75641-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="75641-168"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="75641-168"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="75641-169">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="75641-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="75641-170"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75641-170"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="75641-171">DLL</span><span class="sxs-lookup"><span data-stu-id="75641-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75641-172"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75641-172"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75641-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75641-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75641-174">**Wzceapolgetinterfaceparametriams**</span><span class="sxs-lookup"><span data-stu-id="75641-174">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="75641-175">**Wzcenumschlag-Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="75641-175">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="75641-176">**Wzcqueryinterface**</span><span class="sxs-lookup"><span data-stu-id="75641-176">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="75641-177">**INTF- \_ Eintrag**</span><span class="sxs-lookup"><span data-stu-id="75641-177">**INTF\_ENTRY**</span></span>](intf-entry.md)
</dt> </dl>

 

 




