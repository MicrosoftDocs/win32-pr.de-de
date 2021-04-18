---
title: Ddccigetcapabilitiesstring-Funktion
description: Ruft eine Zeichenfolge ab, die die Funktionen eines Monitors beschreibt.
ms.assetid: 54041126-b710-4448-a9f0-9b644d6b8186
keywords:
- Ddccigetcapabilitiesstring-Funktions Monitor Konfiguration
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesString
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a49a6d7672ee505b4095afd3c6603c719679f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338540"
---
# <a name="ddccigetcapabilitiesstring-function"></a><span data-ttu-id="fab51-104">Ddccigetcapabilitiesstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="fab51-104">DDCCIGetCapabilitiesString function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fab51-105">Diese Funktion wird von der Monitor Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="fab51-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="fab51-106">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="fab51-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="fab51-107">Ruft eine Zeichenfolge ab, die die Funktionen eines Monitors beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fab51-107">Gets a string that describes the capabilities of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab51-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fab51-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesString(
  _In_  HANDLE hMonitor,
  _Out_ LPSTR  pszString,
  _In_  DWORD  dwLength
);
```



## <a name="parameters"></a><span data-ttu-id="fab51-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fab51-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fab51-110">*Hmonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fab51-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fab51-111">Ein Handle für einen physischen Monitor.</span><span class="sxs-lookup"><span data-stu-id="fab51-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="fab51-112">*pszstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fab51-112">*pszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fab51-113">Ein Zeiger auf einen Puffer, der die Funktions Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="fab51-113">A pointer to a buffer that receives the capabilities string.</span></span> <span data-ttu-id="fab51-114">Um die Länge der Funktions Zeichenfolge abzurufen, nennen Sie [**ddccigetcapabilitiesstringlength**](ddccigetcapabilitiesstringlength.md).</span><span class="sxs-lookup"><span data-stu-id="fab51-114">To get the length of the capabilities string, call [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md).</span></span>

</dd> <dt>

<span data-ttu-id="fab51-115">*dwLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fab51-115">*dwLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fab51-116">Die Größe des *pszstring* -Puffers in Zeichen, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="fab51-116">The size of the *pszString* buffer, in characters, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fab51-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fab51-117">Return value</span></span>

<span data-ttu-id="fab51-118">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fab51-118">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="fab51-119">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fab51-119">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fab51-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fab51-120">Remarks</span></span>

<span data-ttu-id="fab51-121">Anwendungen sollten [**capabilitiesrequestandcapabilitiesreply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) aufrufen, anstatt diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="fab51-121">Applications should call [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) instead of calling this function.</span></span>

<span data-ttu-id="fab51-122">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="fab51-122">This function has no associated import library.</span></span> <span data-ttu-id="fab51-123">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="fab51-123">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="fab51-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fab51-124">Requirements</span></span>



| <span data-ttu-id="fab51-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fab51-125">Requirement</span></span> | <span data-ttu-id="fab51-126">Wert</span><span class="sxs-lookup"><span data-stu-id="fab51-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fab51-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fab51-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fab51-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fab51-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fab51-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fab51-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fab51-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fab51-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fab51-131">DLL</span><span class="sxs-lookup"><span data-stu-id="fab51-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fab51-132"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fab51-132"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fab51-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fab51-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab51-134">Überwachen von Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="fab51-134">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

