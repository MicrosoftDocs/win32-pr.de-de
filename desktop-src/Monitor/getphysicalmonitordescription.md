---
title: Getphysicalmonitordescription-Funktion
description: Ruft eine Beschreibung eines physischen Monitors ab.
ms.assetid: 81789eaf-7831-4833-87e1-7f318f831c96
keywords:
- Getphysicalmonitordescription-Funktions Monitor Konfiguration
topic_type:
- apiref
api_name:
- GetPhysicalMonitorDescription
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 259ced1185e229fccd426adfbf94fa47af22b170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103599"
---
# <a name="getphysicalmonitordescription-function"></a><span data-ttu-id="4ac56-104">Getphysicalmonitordescription-Funktion</span><span class="sxs-lookup"><span data-stu-id="4ac56-104">GetPhysicalMonitorDescription function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4ac56-105">Diese Funktion wird von der Monitor Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="4ac56-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="4ac56-106">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4ac56-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="4ac56-107">Ruft eine Beschreibung eines physischen Monitors ab.</span><span class="sxs-lookup"><span data-stu-id="4ac56-107">Gets a description of a physical monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ac56-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ac56-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetPhysicalMonitorDescription(
  _In_  HANDLE hMonitor,
  _In_  DWORD  dwPhysicalMonitorDescriptionSizeInChars,
  _Out_ LPWSTR szPhysicalMonitorDescription
);
```



## <a name="parameters"></a><span data-ttu-id="4ac56-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ac56-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ac56-110">*Hmonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ac56-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac56-111">Ein Handle für einen physischen Monitor.</span><span class="sxs-lookup"><span data-stu-id="4ac56-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="4ac56-112">*dwphysicalmonitordescriptionsizone chars* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ac56-112">*dwPhysicalMonitorDescriptionSizeInChars* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac56-113">Die Anzahl der Zeichen im *szphysicalmonitordescription* -Array.</span><span class="sxs-lookup"><span data-stu-id="4ac56-113">The number of characters in the *szPhysicalMonitorDescription* array.</span></span>

</dd> <dt>

<span data-ttu-id="4ac56-114">*szphysicalmonitordescription* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4ac56-114">*szPhysicalMonitorDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac56-115">Ein Zeiger auf ein Array, das die Beschreibung empfängt.</span><span class="sxs-lookup"><span data-stu-id="4ac56-115">A pointer to an array that receives the description.</span></span> <span data-ttu-id="4ac56-116">Die Anzahl der Elemente im Array sollte mindestens die Größe des **physischen \_ Monitors \_ \_** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4ac56-116">The number of elements in the array should be at least **PHYSICAL\_MONITOR\_DESCRIPTION\_SIZE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ac56-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ac56-117">Return value</span></span>

<span data-ttu-id="4ac56-118">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4ac56-118">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="4ac56-119">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4ac56-119">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ac56-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ac56-120">Remarks</span></span>

<span data-ttu-id="4ac56-121">Anstatt diese Funktion zu verwenden, sollten Anwendungen eine der folgenden Funktionen aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="4ac56-121">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="4ac56-122">**Getphysicalmonitorsfromhmonitor**</span><span class="sxs-lookup"><span data-stu-id="4ac56-122">**GetPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="4ac56-123">**GetPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="4ac56-123">**GetPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="4ac56-124">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="4ac56-124">This function has no associated import library.</span></span> <span data-ttu-id="4ac56-125">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="4ac56-125">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ac56-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ac56-126">Requirements</span></span>



| <span data-ttu-id="4ac56-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ac56-127">Requirement</span></span> | <span data-ttu-id="4ac56-128">Wert</span><span class="sxs-lookup"><span data-stu-id="4ac56-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4ac56-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ac56-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4ac56-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ac56-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4ac56-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ac56-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4ac56-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ac56-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4ac56-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4ac56-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ac56-134"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ac56-134"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ac56-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ac56-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ac56-136">Überwachen von Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="4ac56-136">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

