---
title: Getnumofphysicalmonitors-Funktion
description: Ruft die Anzahl der einem Anzeigegerät zugeordneten physischen Monitore ab.
ms.assetid: 498404e7-867d-4971-bea1-16e9f8fd9838
keywords:
- Getnumofphysicalmonitors-Funktions Monitor Konfiguration
topic_type:
- apiref
api_name:
- GetNumberOfPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bec6abf296d807f80ab77cdc7ad8b4062fea9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858870"
---
# <a name="getnumberofphysicalmonitors-function"></a><span data-ttu-id="7d035-104">Getnumofphysicalmonitors-Funktion</span><span class="sxs-lookup"><span data-stu-id="7d035-104">GetNumberOfPhysicalMonitors function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d035-105">Diese Funktion wird von der Monitor Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="7d035-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="7d035-106">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7d035-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="7d035-107">Ruft die Anzahl der einem Anzeigegerät zugeordneten physischen Monitore ab.</span><span class="sxs-lookup"><span data-stu-id="7d035-107">Gets the number of phyical monitors associated with a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d035-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d035-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetNumberOfPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _Out_ LPDWORD        pdwNumberOfPhysicalMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="7d035-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d035-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d035-110">*pstrindevicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d035-110">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d035-111">Ein Zeiger auf eine [**Unicode- \_ Zeichen**](/windows/desktop/api/subauth/ns-subauth-unicode_string) folgen Struktur, die den Namen des Anzeige Geräts enthält, wie von der [**getmonitorinfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7d035-111">A pointer to a [**UNICODE\_STRING**](/windows/desktop/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="7d035-112">*pdwnumofphysicalmonitors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7d035-112">*pdwNumberOfPhysicalMonitors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d035-113">Empfängt die Anzahl der physischen Monitore.</span><span class="sxs-lookup"><span data-stu-id="7d035-113">Receives the number of physical monitors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d035-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d035-114">Return value</span></span>

<span data-ttu-id="7d035-115">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7d035-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="7d035-116">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7d035-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d035-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d035-117">Remarks</span></span>

<span data-ttu-id="7d035-118">Anstatt diese Funktion zu verwenden, sollten Anwendungen eine der folgenden Funktionen aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="7d035-118">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="7d035-119">**Getnumofphysicalmonitorsfromhmonitor**</span><span class="sxs-lookup"><span data-stu-id="7d035-119">**GetNumberOfPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="7d035-120">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="7d035-120">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="7d035-121">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="7d035-121">This function has no associated import library.</span></span> <span data-ttu-id="7d035-122">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="7d035-122">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d035-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d035-123">Requirements</span></span>



| <span data-ttu-id="7d035-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d035-124">Requirement</span></span> | <span data-ttu-id="7d035-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7d035-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7d035-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d035-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7d035-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d035-127">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7d035-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d035-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7d035-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d035-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7d035-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7d035-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d035-131"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d035-131"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d035-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d035-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d035-133">Überwachen von Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="7d035-133">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

