---
title: Getphysicalmonitors-Funktion
description: Ruft die physischen Monitore ab, die einem Anzeigegerät zugeordnet sind.
ms.assetid: 8bbbad0a-2e45-439c-9312-f922a920c7fd
keywords:
- Getphysicalmonitors-Funktions Monitor Konfiguration
topic_type:
- apiref
api_name:
- GetPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d95ccb801dbf06e096534754bd0adffbe36b5084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338334"
---
# <a name="getphysicalmonitors-function"></a><span data-ttu-id="21406-104">Getphysicalmonitors-Funktion</span><span class="sxs-lookup"><span data-stu-id="21406-104">GetPhysicalMonitors function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="21406-105">Diese Funktion wird von der Monitor Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="21406-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="21406-106">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="21406-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="21406-107">Ruft die physischen Monitore ab, die einem Anzeigegerät zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="21406-107">Gets the physical monitors associated with a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="21406-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="21406-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _In_  DWORD          dwPhysicalMonitorArraySize,
  _Out_ DWORD          *pdwNumPhysicalMonitorHandlesInArray,
  _Out_ HANDLE         *phPhysicalMonitorArray
);
```



## <a name="parameters"></a><span data-ttu-id="21406-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="21406-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21406-110">*pstrindevicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21406-110">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21406-111">Ein Zeiger auf eine [**Unicode- \_ Zeichen**](/windows/desktop/api/subauth/ns-subauth-unicode_string) folgen Struktur, die den Namen des Anzeige Geräts enthält, wie von der [**getmonitorinfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="21406-111">A pointer to a [**UNICODE\_STRING**](/windows/desktop/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="21406-112">*dwphysicalmonitorarraysize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21406-112">*dwPhysicalMonitorArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21406-113">Die Anzahl der Elemente im *pdwnumphysicalmonitorlenker* -Array.</span><span class="sxs-lookup"><span data-stu-id="21406-113">The number of elements in the *pdwNumPhysicalMonitorHandlesInArray* array.</span></span> <span data-ttu-id="21406-114">Um die erforderliche Größe des Arrays abzurufen, nennen Sie [**getnumofphysicalmonitors**](getnumberofphysicalmonitors.md).</span><span class="sxs-lookup"><span data-stu-id="21406-114">To get the required size of the array, call [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md).</span></span>

</dd> <dt>

<span data-ttu-id="21406-115">*pdwnumphysicalmonitorlenker-Array* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="21406-115">*pdwNumPhysicalMonitorHandlesInArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21406-116">Empfängt die Anzahl der Elemente, die die Funktion in das *phphysicalmonitorarray* -Array kopiert.</span><span class="sxs-lookup"><span data-stu-id="21406-116">Receives the number of items that the function copies to the *phPhysicalMonitorArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="21406-117">*phphysicalmonitorarray* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="21406-117">*phPhysicalMonitorArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21406-118">Ein Array, das Handles für die physischen Monitore empfängt.</span><span class="sxs-lookup"><span data-stu-id="21406-118">An array that receives handles to the physical monitors.</span></span> <span data-ttu-id="21406-119">Jedes Handle muss durch Aufrufen von [**destroyphysicalmonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="21406-119">Each handle must be released by calling [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21406-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21406-120">Return value</span></span>

<span data-ttu-id="21406-121">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="21406-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="21406-122">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="21406-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="21406-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21406-123">Remarks</span></span>

<span data-ttu-id="21406-124">Anstatt diese Funktion zu verwenden, sollten Anwendungen eine der folgenden Funktionen aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="21406-124">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="21406-125">**Getphysicalmonitorsfromhmonitor**</span><span class="sxs-lookup"><span data-stu-id="21406-125">**GetPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="21406-126">**GetPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="21406-126">**GetPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="21406-127">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="21406-127">This function has no associated import library.</span></span> <span data-ttu-id="21406-128">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="21406-128">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="21406-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21406-129">Requirements</span></span>



| <span data-ttu-id="21406-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21406-130">Requirement</span></span> | <span data-ttu-id="21406-131">Wert</span><span class="sxs-lookup"><span data-stu-id="21406-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="21406-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21406-132">Minimum supported client</span></span><br/> | <span data-ttu-id="21406-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21406-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="21406-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21406-134">Minimum supported server</span></span><br/> | <span data-ttu-id="21406-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21406-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="21406-136">DLL</span><span class="sxs-lookup"><span data-stu-id="21406-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21406-137"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21406-137"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21406-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21406-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21406-139">Überwachen von Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="21406-139">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

