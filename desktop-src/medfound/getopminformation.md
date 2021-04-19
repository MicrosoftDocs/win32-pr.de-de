---
description: Sendet eine OPM-Status Anforderung an ein geschütztes Ausgabe Objekt.
ms.assetid: 4b691b20-25de-4b9e-a725-674a57697b56
title: Getopminformation-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 450292c0f6352436d7df8c91afff0d08c8c31394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346660"
---
# <a name="getopminformation-function"></a><span data-ttu-id="230e1-103">Getopminformation-Funktion</span><span class="sxs-lookup"><span data-stu-id="230e1-103">GetOPMInformation function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="230e1-104">Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="230e1-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="230e1-105">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="230e1-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="230e1-106">Sendet eine OPM-Status Anforderung an ein geschütztes Ausgabe Objekt.</span><span class="sxs-lookup"><span data-stu-id="230e1-106">Sends an OPM status request to a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="230e1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="230e1-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetOPMInformation(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE       opoOPMProtectedOutput,
  _In_  const DXGKMDT_OPM_GET_INFO_PARAMETERS   *pParameters,
  _Out_       DXGKMDT_OPM_REQUESTED_INFORMATION *pRequestedInformation
);
```



## <a name="parameters"></a><span data-ttu-id="230e1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="230e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="230e1-109">" *opoopmprotectedoutput* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="230e1-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="230e1-110">Ein Handle für das geschützte Ausgabe Objekt.</span><span class="sxs-lookup"><span data-stu-id="230e1-110">A handle to the protected output object.</span></span> <span data-ttu-id="230e1-111">Dieses Handle wird durch Aufrufen von [**createopmprotectedoutputs**](createopmprotectedoutputs.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="230e1-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="230e1-112">*pparameters* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="230e1-112">*pParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="230e1-113">Ein Zeiger auf eine **dxgkmdt \_ OPM-Struktur \_ get \_ Info \_ Parameters** , die Eingabedaten für die Status Anforderung enthält.</span><span class="sxs-lookup"><span data-stu-id="230e1-113">A pointer to a **DXGKMDT\_OPM\_GET\_INFO\_PARAMETERS** structure that contains input data for the status request.</span></span>

</dd> <dt>

<span data-ttu-id="230e1-114">*prequestedinformation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="230e1-114">*pRequestedInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="230e1-115">Ein Zeiger auf eine von **dxgkmdt \_ OPM \_ angeforderte \_ Informations** Struktur, die die Ergebnisse der Status Anforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="230e1-115">A pointer to a **DXGKMDT\_OPM\_REQUESTED\_INFORMATION** structure that receives the results of the status request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="230e1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="230e1-116">Return value</span></span>

<span data-ttu-id="230e1-117">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="230e1-117">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="230e1-118">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="230e1-118">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="230e1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="230e1-119">Remarks</span></span>

<span data-ttu-id="230e1-120">Anwendungen sollten [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) aufrufen, anstatt diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="230e1-120">Applications should call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) instead of calling this function.</span></span>

<span data-ttu-id="230e1-121">Das geschützte Ausgabe Objekt muss mit OPM-Semantik erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="230e1-121">The protected output object must be created with OPM semantics.</span></span> <span data-ttu-id="230e1-122">Siehe " [**kreateopmprotectedoutputs**](createopmprotectedoutputs.md)".</span><span class="sxs-lookup"><span data-stu-id="230e1-122">See [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

<span data-ttu-id="230e1-123">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="230e1-123">This function has no associated import library.</span></span> <span data-ttu-id="230e1-124">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="230e1-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="230e1-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="230e1-125">Requirements</span></span>



| <span data-ttu-id="230e1-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="230e1-126">Requirement</span></span> | <span data-ttu-id="230e1-127">Wert</span><span class="sxs-lookup"><span data-stu-id="230e1-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="230e1-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="230e1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="230e1-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="230e1-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="230e1-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="230e1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="230e1-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="230e1-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="230e1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="230e1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="230e1-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="230e1-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="230e1-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="230e1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="230e1-135">OPM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="230e1-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="230e1-136">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="230e1-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
