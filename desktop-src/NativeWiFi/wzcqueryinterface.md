---
description: Stellt ausführliche Informationen für eine drahtlose LAN-Schnittstelle bereit, die vom drahtlos Konfigurations Dienst für drahtlose Netzwerke verwaltet wird.
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: Wzcqueryinterface-Funktion (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCQueryInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 36457eebf5c38b32bb46eb8cfa44cae104f1bc6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867903"
---
# <a name="wzcqueryinterface-function"></a><span data-ttu-id="f9cfc-103">Wzcqueryinterface-Funktion</span><span class="sxs-lookup"><span data-stu-id="f9cfc-103">WZCQueryInterface function</span></span>

<span data-ttu-id="f9cfc-104">\[**Wzcqueryinterface** wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-104">\[**WZCQueryInterface** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="f9cfc-105">Verwenden Sie stattdessen die Funktion [**wlanqueryinterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) .</span><span class="sxs-lookup"><span data-stu-id="f9cfc-105">Use the [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) function instead.</span></span> <span data-ttu-id="f9cfc-106">Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).</span><span class="sxs-lookup"><span data-stu-id="f9cfc-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).</span></span> <span data-ttu-id="f9cfc-107">\]</span><span class="sxs-lookup"><span data-stu-id="f9cfc-107">\]</span></span>

<span data-ttu-id="f9cfc-108">Die **wzcqueryinterface** -Funktion stellt ausführliche Informationen für eine drahtlose LAN-Schnittstelle bereit, die vom drahtlos Konfigurations Dienst für drahtlose Daten verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-108">The **WZCQueryInterface** function provides detailed information for a wireless LAN interface managed by the Wireless Zero Configuration service.</span></span>

<span data-ttu-id="f9cfc-109">Stellt ausführliche Informationen für eine bestimmte Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-109">Provides detailed information for a given interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9cfc-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9cfc-110">Syntax</span></span>


```C++
DWORD WZCQueryInterface(
  _In_    LPWSTR      pSrvAddr,
  _In_    DWORD       dwInFlags,
  _Inout_ PINTF_ENTRY pIntf,
  _Out_   LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f9cfc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9cfc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9cfc-112">*psrvaddr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9cfc-112">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9cfc-113">Ein Zeiger auf eine Zeichenfolge, die den Namen des Computers enthält, auf dem diese Funktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-113">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="f9cfc-114">Wenn dieser Parameter **null** ist, wird der Konfigurations Dienst für drahtlose NULL auf dem lokalen Computer abgefragt.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-114">If this parameter is **NULL**, then the Wireless Zero Configuration service is queried on the local computer.</span></span>

<span data-ttu-id="f9cfc-115">Wenn der angegebene *psrvaddr* -Parameter ein Remote Computer ist, muss der Remote Computer Remote-RPC-Aufrufe unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-115">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="f9cfc-116">*dwInFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9cfc-116">*dwInFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9cfc-117">Die Felder, die abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-117">The fields to be queried.</span></span> <span data-ttu-id="f9cfc-118">Dabei handelt es sich um eine Bitmaske, die eine beliebige Kombination der folgenden Flags enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-118">This is a bitmask that can contain any combination of the following flags.</span></span>



| <span data-ttu-id="f9cfc-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f9cfc-119">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="f9cfc-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f9cfc-120">Meaning</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <span data-ttu-id="f9cfc-121"><dt>**INTF \_ Dynflags**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-121"><dt>**INTF\_DYNFLAGS**</dt> <dt>0x00000010</dt></span></span> </dl>             | <span data-ttu-id="f9cfc-122">Gibt den Wert für den **dwdynflags** -Member in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf den der *pintf* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-122">Return the value for the **dwDynFlags** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <span data-ttu-id="f9cfc-123"><dt>**INTF \_ Descr**</dt> <dt>0x00010000 bis</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-123"><dt>**INTF\_DESCR**</dt> <dt>0x00010000</dt></span></span> </dl>                      | <span data-ttu-id="f9cfc-124">Gibt den Wert für den **wszdescr** -Member in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf den der *pintf* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-124">Return the value for the **wszDescr** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <span data-ttu-id="f9cfc-125"><dt>**INTF \_ Ndismedia**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-125"><dt>**INTF\_NDISMEDIA**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="f9cfc-126">Gibt die Werte für die Member **ulmediastate**, **ulmediatype** und **ulphysicalmediatype** in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf die durch den *pintf* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-126">Return the values for the **ulMediaState**, **ulMediaType**, and **ulPhysicalMediaType** members in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <span data-ttu-id="f9cfc-127"><dt>**INTF \_ Preflist**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-127"><dt>**INTF\_PREFLIST**</dt> <dt>0x00040000</dt></span></span> </dl>             | <span data-ttu-id="f9cfc-128">Gibt die bevorzugte Liste von Netzwerken im **rdstssidlist** -Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf die durch den *pintf* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-128">Return the preferred list of networks in the **rdStSSIDList** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <span data-ttu-id="f9cfc-129"><dt>**INTF \_ Funktionen**</dt> <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-129"><dt>**INTF\_CAPABILITIES**</dt> <dt>0x00080000</dt></span></span> </dl> | <span data-ttu-id="f9cfc-130">Gibt die Werte für die **DW-Funktionen** und die **rdniccapabili-** Elemente in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf die durch den *pintf* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-130">Return the values for the **dwCapabilities** and the **rdNicCapabilities** members in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <span data-ttu-id="f9cfc-131"><dt>**INTF \_ Inframode**</dt> <dt>0x00200000</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-131"><dt>**INTF\_INFRAMODE**</dt> <dt>0x00200000</dt></span></span> </dl>          | <span data-ttu-id="f9cfc-132">Gibt den Wert für das **ninframode** -Element in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf die durch den *pintf* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-132">Return the value for the **nInfraMode** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="f9cfc-133">Der **ninframode** -Member ist nur in einigen Schnittstellen Kontext Zuständen gültig.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-133">The **nInfraMode** member is valid only in some interface context states.</span></span><br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <span data-ttu-id="f9cfc-134"><dt>**INTF \_ Authmode**</dt> <dt>0x00400000</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-134"><dt>**INTF\_AUTHMODE**</dt> <dt>0x00400000</dt></span></span> </dl>             | <span data-ttu-id="f9cfc-135">Gibt den Wert für den **nauthmode** -Member in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf den der *pintf* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-135">Return the value for the **nAuthMode** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span> <br/> <span data-ttu-id="f9cfc-136">Der **nauthmode** -Member ist nur in einigen Schnittstellen Kontext Zuständen gültig.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-136">The **nAuthMode** member is valid only in some interface context states.</span></span><br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <span data-ttu-id="f9cfc-137"><dt>**INTF \_ Wepstatus**</dt> <dt>0x00800000</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-137"><dt>**INTF\_WEPSTATUS**</dt> <dt>0x00800000</dt></span></span> </dl>          | <span data-ttu-id="f9cfc-138">Gibt den Wert für den **nwepstatus** -Member in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf den der *pintf* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-138">Return the value for the **nWepStatus** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span> <br/> <span data-ttu-id="f9cfc-139">Der **nwepstatus** -Member ist nur in bestimmten Schnittstellen Kontext Zuständen gültig.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-139">The **nWepStatus** member is valid only in some interface context states.</span></span><br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <span data-ttu-id="f9cfc-140"><dt>**INTF \_ SSID**</dt> <dt>0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-140"><dt>**INTF\_SSID**</dt> <dt>0x01000000</dt></span></span> </dl>                         | <span data-ttu-id="f9cfc-141">Gibt den Wert für den **rdssid-** Member in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf den der *pintf* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-141">Return the value for the **rdSSID** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="f9cfc-142">Der **rdssid-** Member ist nur in einigen Schnittstellen Kontext Zuständen gültig.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-142">The **rdSSID** member is valid only in some interface context states.</span></span><br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <span data-ttu-id="f9cfc-143"><dt>**INTF \_ BSSID**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-143"><dt>**INTF\_BSSID**</dt> <dt>0x02000000</dt></span></span> </dl>                      | <span data-ttu-id="f9cfc-144">Gibt den Wert für den **rdbssid-** Member in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf den der *pintf* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-144">Return the value for the **rdBSSID** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="f9cfc-145">Der **rdbssid-** Member ist nur in einigen Schnittstellen Kontext Zuständen gültig.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-145">The **rdBSSID** member is valid only in some interface context states.</span></span><br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <span data-ttu-id="f9cfc-146"><dt>**INTF \_ Bssidlist**</dt> <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-146"><dt>**INTF\_BSSIDLIST**</dt> <dt>0x04000000</dt></span></span> </dl>          | <span data-ttu-id="f9cfc-147">Gibt die sichtbare Liste der Netzwerke im **rdbssidlist** -Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf die durch den *pintf* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-147">Return the visible list of networks in the **rdBSSIDList** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="f9cfc-148">Der **rdbssidlist** -Member ist nur in einigen Schnittstellen Kontext Zuständen gültig.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-148">The **rdBSSIDList** member is valid only in some interface context states.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f9cfc-149">*pintf* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f9cfc-149">*pIntf* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9cfc-150">Bei Eingabe ein Zeiger auf den Schlüssel der abzufragende Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-150">On input, a pointer to the key of the interface to query.</span></span> <span data-ttu-id="f9cfc-151">Bei der Ausgabe ein Zeiger auf die angeforderten Schnittstellen Daten.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-151">On output, a pointer to the requested interface data.</span></span> <span data-ttu-id="f9cfc-152">Dieser Parameter ist ein Zeiger auf eine [**INTF- \_ Eintrags**](intf-entry.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-152">This parameter is a pointer to an [**INTF\_ENTRY**](intf-entry.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f9cfc-153">*pdwOutFlags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f9cfc-153">*pdwOutFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9cfc-154">Eine Reihe von Feldern, die erfolgreich abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-154">A set of fields successfully retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9cfc-155">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9cfc-155">Return value</span></span>

<span data-ttu-id="f9cfc-156">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-156">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="f9cfc-157">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Rückgabecodes sein.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-157">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="f9cfc-158">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f9cfc-158">Return code</span></span>                                                                                               | <span data-ttu-id="f9cfc-159">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9cfc-159">Description</span></span>                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9cfc-160"><dt>**Fehler-Arena wurde durchlaufen \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-160"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>      | <span data-ttu-id="f9cfc-161">Die Speicher Kontroll Blöcke wurden zerstört.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-161">The storage control blocks were destroyed.</span></span> <span data-ttu-id="f9cfc-162">Dieser Fehler wird zurückgegeben, wenn der Konfigurations Dienst für drahtlose NULL keine internen Objekte initialisiert hat.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-162">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="f9cfc-163"><dt>**Fehler \_ Datei \_ nicht \_ gefunden.**</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-163"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="f9cfc-164">Die angegebene Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-164">The system cannot find the file specified.</span></span> <span data-ttu-id="f9cfc-165">Dieser Fehler wird zurückgegeben, wenn die GUID im **wszguid** -Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur, auf die durch den *pintf* -Parameter verwiesen wird, nicht mit einer der Drahtlos-LAN-Schnittstellen auf dem lokalen Computer entsprach.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-165">This error is returned if the GUID in the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter did not match any of the wireless LAN interfaces on the local computer.</span></span> <br/> |
| <dl> <span data-ttu-id="f9cfc-166"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-166"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>  | <span data-ttu-id="f9cfc-167">Ein Parameter ist falsch.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-167">A parameter is incorrect.</span></span> <span data-ttu-id="f9cfc-168">Dieser Fehler wird zurückgegeben, wenn der *pintf* -Parameter **null** ist.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-168">This error is returned if the *pIntf* parameter is **NULL**.</span></span> <span data-ttu-id="f9cfc-169">Dieser Fehler wird zurückgegeben, wenn das **wszguid** -Element der [**INTF- \_ Eintrags**](intf-entry.md) Struktur, auf die durch den *pintf* -Parameter verwiesen wird, **null** ist.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-169">This error is returned if the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter is **NULL**.</span></span> <br/>                            |
| <dl> <span data-ttu-id="f9cfc-170"><dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-170"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="f9cfc-171">Es ist nicht genügend Arbeitsspeicher verfügbar, um diese Anforderung zu verarbeiten und Arbeitsspeicher für die Abfrageergebnisse zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-171">Not enough memory is available to process this request and allocate memory for the query results.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="f9cfc-172"><dt>**RPC- \_ Status**</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-172"><dt>**RPC\_STATUS**</dt></span></span> </dl>                | <span data-ttu-id="f9cfc-173">Verschiedene Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-173">Various error codes.</span></span><br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="f9cfc-174">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9cfc-174">Remarks</span></span>

<span data-ttu-id="f9cfc-175">Der **wszguid** -Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur, auf den der *pintf* -Parameter verweist, muss eine Schnittstellen-GUID für eine drahtlose LAN-Schnittstelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-175">The **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter must contain an interface GUID for a wireless LAN interface.</span></span> <span data-ttu-id="f9cfc-176">Eine Liste der Drahtlos-LAN-Schnittstellen kann durch Aufrufen der [**wzcenumschlag Interfaces**](wzcenuminterfaces.md) -Funktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-176">A list of wireless LAN interfaces can be retrieved by calling the [**WZCEnumInterfaces**](wzcenuminterfaces.md) function.</span></span>

<span data-ttu-id="f9cfc-177">Die folgenden Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur, auf die von *pintf* verwiesen wird, müssen vor einem **wzcqueryinterface** -Befehl auf 0 festgelegt werden: **rdssid**, **rdbssid**, **rdbssidlist**, **rdstssidlist** und **rdctrldata**.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-177">The following members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by *pIntf* must be set to 0 before a call to the **WZCQueryInterface** function: **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList**, and **rdCtrlData**.</span></span>

<span data-ttu-id="f9cfc-178">Der Konfigurations Dienst für drahtlose NULL-Werte aktualisiert den Medien Status nicht in einer Weise, auch wenn Medien verbundene und getrennte Ereignisse empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-178">The Wireless Zero Configuration service does not automotically update media state, even when media connected and disconnected events are received.</span></span> <span data-ttu-id="f9cfc-179">Eine Anwendung sollte eine Medien Zustands Aktualisierung erzwingen, indem Sie die [**wzcrefreshinterface**](wzcrefreshinterface.md) -Funktion aufrufen, bevor Sie die **wzcqueryinterface** -Funktion aufrufen, wenn der NDIS-Medien Zustand angefordert werden soll (Das INTF \_ ndismedia-Bit wird im *dwInFlags* -Parameter festgelegt).</span><span class="sxs-lookup"><span data-stu-id="f9cfc-179">An application should force a media state refresh by calling the [**WZCRefreshInterface**](wzcrefreshinterface.md) function before calling the **WZCQueryInterface** function if the NDIS media state is to be requested (the INTF\_NDISMEDIA bit will be set in the *dwInFlags* parameter).</span></span>

<span data-ttu-id="f9cfc-180">Wenn der *dwInFlags* -Parameter **INTF- \_ bssidlist** enthält, legt die **wzcqueryinterface** -Funktion nicht die-Eigenschaft " *dwoutflags* " mit **INTF \_ bssidlist** fest, wenn die sichtbare Liste der Netzwerke leer ist.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-180">When the *dwInFlags* parameter contains **INTF\_BSSIDLIST**, the **WZCQueryInterface** function does not set the *dwOutFlags* with **INTF\_BSSIDLIST** if the visible list of networks is empty.</span></span> <span data-ttu-id="f9cfc-181">Wenn der *dwInFlags* -Parameter **INTF \_ SSID** enthält, werden die *dwoutflags* von der **wzcqueryinterface** -Funktion nicht mit **INTF \_ SSID** festgelegt, wenn keine SSID verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-181">When the *dwInFlags* parameter contains **INTF\_SSID**, the **WZCQueryInterface** function does not set the *dwOutFlags* with **INTF\_SSID** if no SSID is available.</span></span>

<span data-ttu-id="f9cfc-182">Wenn die **wzcqueryinterface** -Funktion den Fehler Erfolg zurückgibt \_ , sollte der Aufrufer die [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) -Funktion mit dem *pintf* -Parameter aufrufen, um die für die zurückgegebenen Daten zugewiesenen internen Puffer freizugeben, sobald diese Informationen nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-182">If the **WZCQueryInterface** function returns ERROR\_SUCCESS, the caller should call the [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) function with the *pIntf* parameter to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span> <span data-ttu-id="f9cfc-183">Dadurch werden die Puffer freigegeben, die von den Elementen **rdssid**, **rdbssid**, **rdbssidlist**, **rdstssidlist** und **rdctrldata** der [**INTF- \_ Eintrags**](intf-entry.md) Struktur verwendet werden, auf die durch den *pintf* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-183">This releases the buffers used by the **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList**, and **rdCtrlData** members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by *pIntf* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="f9cfc-184">Die Header Datei " *wzcsapi. h* " und die Datei " *wzcsapi. lib* Import Library" sind im Windows SDK nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-184">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f9cfc-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9cfc-185">Requirements</span></span>



| <span data-ttu-id="f9cfc-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9cfc-186">Requirement</span></span> | <span data-ttu-id="f9cfc-187">Wert</span><span class="sxs-lookup"><span data-stu-id="f9cfc-187">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9cfc-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9cfc-188">Minimum supported client</span></span><br/> | <span data-ttu-id="f9cfc-189">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9cfc-189">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f9cfc-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9cfc-190">Minimum supported server</span></span><br/> | <span data-ttu-id="f9cfc-191">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9cfc-191">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f9cfc-192">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f9cfc-192">End of client support</span></span><br/>    | <span data-ttu-id="f9cfc-193">Windows XP mit SP3</span><span class="sxs-lookup"><span data-stu-id="f9cfc-193">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="f9cfc-194">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f9cfc-194">End of server support</span></span><br/>    | <span data-ttu-id="f9cfc-195">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f9cfc-195">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="f9cfc-196">Header</span><span class="sxs-lookup"><span data-stu-id="f9cfc-196">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9cfc-197"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-197"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9cfc-198">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f9cfc-198">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9cfc-199"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-199"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f9cfc-200">DLL</span><span class="sxs-lookup"><span data-stu-id="f9cfc-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9cfc-201"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9cfc-201"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9cfc-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9cfc-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9cfc-203">**INTF- \_ Eintrag**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-203">**INTF\_ENTRY**</span></span>](intf-entry.md)
</dt> <dt>

[<span data-ttu-id="f9cfc-204">**Wzceapolgetinterfaceparametriams**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-204">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="f9cfc-205">**Wzcenumschlag-Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-205">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="f9cfc-206">**Wzkrefreshinterface**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-206">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
