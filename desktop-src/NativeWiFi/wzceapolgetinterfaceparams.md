---
description: Ruft EAPOL-Konfigurationsparameter für die angegebene Wireless LAN-Schnittstelle ab.
ms.assetid: 3dce15be-879d-42e9-b8eb-96d52c004acb
title: Wzceapolgetinterfacesamams-Funktion (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEapolGetInterfaceParams
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: bc89fd2defb75662fa90b5ed00c7969d483da590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356993"
---
# <a name="wzceapolgetinterfaceparams-function"></a><span data-ttu-id="a148d-103">Wzceapolgetinterfaceparser-Funktion</span><span class="sxs-lookup"><span data-stu-id="a148d-103">WZCEapolGetInterfaceParams function</span></span>

<span data-ttu-id="a148d-104">\[**Wzceapolgetinterfaceparser** wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a148d-104">\[**WZCEapolGetInterfaceParams** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="a148d-105">Verwenden Sie stattdessen die [native WiFi-API](native-wifi-reference.md), die eine ähnliche Funktionalität bietet.</span><span class="sxs-lookup"><span data-stu-id="a148d-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="a148d-106">Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="a148d-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="a148d-107">Die **wzceapolgetinterfaceparser** -Funktion ruft EAPOL-Konfigurationsparameter für die angegebene drahtlose LAN-Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="a148d-107">The **WZCEapolGetInterfaceParams** function gets EAPOL configuration parameters for the specified wireless LAN interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a148d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a148d-108">Syntax</span></span>


```C++
DWORD WZCEapolGetInterfaceParams(
  _In_    LPWSTR            pSrvAddr,
  _In_    PWCHAR            pwszGuid,
  _In_    DWORD             dwSizeOfSSID,
  _In_    BYTE              *pbSSID,
  _Inout_ EAPOL_INTF_PARAMS *pIntfParams
);
```



## <a name="parameters"></a><span data-ttu-id="a148d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a148d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a148d-110">*psrvaddr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a148d-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a148d-111">Ein Zeiger auf eine Zeichenfolge, die den Namen des Computers enthält, auf dem diese Funktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a148d-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="a148d-112">Wenn dieser Parameter **null** ist, wird der Konfigurations Dienst für drahtlose NULL auf dem lokalen Computer aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a148d-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is called on the local computer.</span></span>

<span data-ttu-id="a148d-113">Wenn der angegebene *psrvaddr* -Parameter ein Remote Computer ist, muss der Remote Computer Remote-RPC-Aufrufe unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a148d-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="a148d-114">*pwszguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a148d-114">*pwszGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a148d-115">Der GUID der Schnittstelle, für die Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a148d-115">The GUID of the interface for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="a148d-116">*dwsizeofssid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a148d-116">*dwSizeOfSSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a148d-117">Die Größe des Netzwerk Bezeichners, für den die Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a148d-117">The size of the network identifier for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="a148d-118">*pbssid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a148d-118">*pbSSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a148d-119">Ein Zeiger auf den Netzwerk Bezeichner, für den Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a148d-119">A pointer to the network identifier for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="a148d-120">*pintfparametriams* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a148d-120">*pIntfParams* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a148d-121">Ein Zeiger auf eine [**EAPOL \_ INTF \_**](eapol-intf-params.md) -Parameter Struktur, die Schnittstellenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="a148d-121">A pointer to a [**EAPOL\_INTF\_PARAMS**](eapol-intf-params.md) structure that contains interface parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a148d-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a148d-122">Return value</span></span>

<span data-ttu-id="a148d-123">Gibt den Erfolg des Fehlers zurück, \_ Wenn der Vorgang erfolgreich abgeschlossen wurde. andernfalls wird einer der Windows-Systemfehler Codes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a148d-123">Returns ERROR\_SUCCESS if the operation completes successfully; otherwise, returns one of the Windows system error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="a148d-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a148d-124">Remarks</span></span>

<span data-ttu-id="a148d-125">Wenn **wzceapolgetinterfaceparser** einen Fehler Erfolg zurückgibt \_ , sollte der Aufrufer [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) aufrufen, um die für die zurückgegebenen Daten zugewiesenen internen Puffer freizugeben, sobald diese Informationen nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="a148d-125">If the **WZCEapolGetInterfaceParams** returns ERROR\_SUCCESS, the caller should call [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="a148d-126">Die Header Datei " *wzcsapi. h* " und die Datei " *wzcsapi. lib* Import Library" sind im Windows SDK nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a148d-126">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a148d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a148d-127">Requirements</span></span>



| <span data-ttu-id="a148d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a148d-128">Requirement</span></span> | <span data-ttu-id="a148d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="a148d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a148d-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a148d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a148d-131">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a148d-131">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a148d-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a148d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a148d-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a148d-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a148d-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a148d-134">End of client support</span></span><br/>    | <span data-ttu-id="a148d-135">Windows XP mit SP3</span><span class="sxs-lookup"><span data-stu-id="a148d-135">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="a148d-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="a148d-136">End of server support</span></span><br/>    | <span data-ttu-id="a148d-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a148d-137">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="a148d-138">Header</span><span class="sxs-lookup"><span data-stu-id="a148d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a148d-139"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a148d-139"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="a148d-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a148d-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="a148d-141"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a148d-141"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a148d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a148d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a148d-143"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a148d-143"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a148d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a148d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a148d-145">**Wzcenumschlag-Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="a148d-145">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="a148d-146">**Wzcqueryinterface**</span><span class="sxs-lookup"><span data-stu-id="a148d-146">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="a148d-147">**Wzkrefreshinterface**</span><span class="sxs-lookup"><span data-stu-id="a148d-147">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
