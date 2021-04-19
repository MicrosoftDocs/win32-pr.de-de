---
title: Ddccigetcapabilitiesstringlength-Funktion
description: Ruft die Länge einer Funktions Zeichenfolge für einen Monitor ab.
ms.assetid: 8a26d17b-1535-49c7-8cfb-48feb283a3c4
keywords:
- Ddccigetcapabilitiesstringlength-Funktions Monitor Konfiguration
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesStringLength
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d82e2f0667d542c8fa4c9255fde765e4cea81d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339547"
---
# <a name="ddccigetcapabilitiesstringlength-function"></a><span data-ttu-id="25147-104">Ddccigetcapabilitiesstringlength-Funktion</span><span class="sxs-lookup"><span data-stu-id="25147-104">DDCCIGetCapabilitiesStringLength function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25147-105">Diese Funktion wird von der Monitor Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="25147-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="25147-106">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="25147-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="25147-107">Ruft die Länge einer Funktions Zeichenfolge für einen Monitor ab.</span><span class="sxs-lookup"><span data-stu-id="25147-107">Gets the length of a capabilities string for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="25147-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="25147-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesStringLength(
  _In_  HANDLE hMonitor,
  _Out_ DWORD  *pdwLength
);
```



## <a name="parameters"></a><span data-ttu-id="25147-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="25147-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25147-110">*Hmonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25147-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25147-111">Ein Handle für einen physischen Monitor.</span><span class="sxs-lookup"><span data-stu-id="25147-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="25147-112">*pdwLength* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="25147-112">*pdwLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25147-113">Empfängt die Länge der Funktions Zeichenfolge in Zeichen, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="25147-113">Receives the length of the capabilities string, in characters, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25147-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25147-114">Return value</span></span>

<span data-ttu-id="25147-115">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="25147-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="25147-116">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="25147-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="25147-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25147-117">Remarks</span></span>

<span data-ttu-id="25147-118">Anwendungen sollten [**getcapabilitiesstringlength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) aufrufen, anstatt diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="25147-118">Applications should call [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) instead of calling this function.</span></span>

<span data-ttu-id="25147-119">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="25147-119">This function has no associated import library.</span></span> <span data-ttu-id="25147-120">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="25147-120">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="25147-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25147-121">Requirements</span></span>



| <span data-ttu-id="25147-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25147-122">Requirement</span></span> | <span data-ttu-id="25147-123">Wert</span><span class="sxs-lookup"><span data-stu-id="25147-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="25147-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25147-124">Minimum supported client</span></span><br/> | <span data-ttu-id="25147-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25147-125">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="25147-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25147-126">Minimum supported server</span></span><br/> | <span data-ttu-id="25147-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25147-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="25147-128">DLL</span><span class="sxs-lookup"><span data-stu-id="25147-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25147-129"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25147-129"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25147-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25147-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25147-131">Überwachen von Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="25147-131">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

