---
description: Sendet eine zertifizierte COPP-Status Anforderung (Output Protection Protocol) an ein geschütztes Ausgabe Objekt.
ms.assetid: 24300591-c0c0-48a2-99d3-be98c0c1492a
title: Getcoppcompatibleopminformation-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCOPPCompatibleOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 7e5eac24dfcf08e45ce414090835792e594d7c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214308"
---
# <a name="getcoppcompatibleopminformation-function"></a><span data-ttu-id="664f0-103">Getcoppcompatibleopminformation-Funktion</span><span class="sxs-lookup"><span data-stu-id="664f0-103">GetCOPPCompatibleOPMInformation function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="664f0-104">Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="664f0-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="664f0-105">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="664f0-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="664f0-106">Sendet eine zertifizierte COPP-Status Anforderung (Output Protection Protocol) an ein geschütztes Ausgabe Objekt.</span><span class="sxs-lookup"><span data-stu-id="664f0-106">Sends a Certified Output Protection Protocol (COPP) status request to a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="664f0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="664f0-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCOPPCompatibleOPMInformation(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE                     opoOPMProtectedOutput,
  _In_  DXGKMDT_OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
  _Out_ DXGKMDT_OPM_REQUESTED_INFORMATION               *pRequestedInformation
);
```



## <a name="parameters"></a><span data-ttu-id="664f0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="664f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="664f0-109">" *opoopmprotectedoutput* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="664f0-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="664f0-110">Ein Handle für das geschützte Ausgabe Objekt.</span><span class="sxs-lookup"><span data-stu-id="664f0-110">A handle to the protected output object.</span></span> <span data-ttu-id="664f0-111">Dieses Handle wird durch Aufrufen von [**createopmprotectedoutputs**](createopmprotectedoutputs.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="664f0-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="664f0-112">*pparameters* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="664f0-112">*pParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="664f0-113">Ein Zeiger auf eine **dxgkmdt \_ OPM \_ COPP- \_ kompatible \_ get \_ Info \_ Parameters** -Struktur, die Eingabedaten für die Status Anforderung enthält.</span><span class="sxs-lookup"><span data-stu-id="664f0-113">A pointer to a **DXGKMDT\_OPM\_COPP\_COMPATIBLE\_GET\_INFO\_PARAMETERS** structure that contains input data for the status request.</span></span>

</dd> <dt>

<span data-ttu-id="664f0-114">*prequestedinformation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="664f0-114">*pRequestedInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="664f0-115">Ein Zeiger auf eine von **dxgkmdt \_ OPM \_ angeforderte \_ Informations** Struktur, die die Ergebnisse der Status Anforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="664f0-115">A pointer to a **DXGKMDT\_OPM\_REQUESTED\_INFORMATION** structure that receives the results of the status request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="664f0-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="664f0-116">Return value</span></span>

<span data-ttu-id="664f0-117">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="664f0-117">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="664f0-118">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="664f0-118">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="664f0-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="664f0-119">Remarks</span></span>

<span data-ttu-id="664f0-120">Anwendungen sollten [**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) aufrufen, anstatt diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="664f0-120">Applications should call [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) instead of calling this function.</span></span>

<span data-ttu-id="664f0-121">Das geschützte Ausgabe Objekt muss mit der COPP-Semantik erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="664f0-121">The protected output object must be created with COPP semantics.</span></span> <span data-ttu-id="664f0-122">Siehe " [**kreateopmprotectedoutputs**](createopmprotectedoutputs.md)".</span><span class="sxs-lookup"><span data-stu-id="664f0-122">See [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

<span data-ttu-id="664f0-123">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="664f0-123">This function has no associated import library.</span></span> <span data-ttu-id="664f0-124">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="664f0-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="664f0-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="664f0-125">Requirements</span></span>



| <span data-ttu-id="664f0-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="664f0-126">Requirement</span></span> | <span data-ttu-id="664f0-127">Wert</span><span class="sxs-lookup"><span data-stu-id="664f0-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="664f0-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="664f0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="664f0-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="664f0-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="664f0-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="664f0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="664f0-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="664f0-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="664f0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="664f0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="664f0-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="664f0-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="664f0-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="664f0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="664f0-135">OPM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="664f0-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="664f0-136">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="664f0-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
