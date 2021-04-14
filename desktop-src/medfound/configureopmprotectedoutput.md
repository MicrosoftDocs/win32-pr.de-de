---
description: Konfiguriert ein geschütztes Ausgabe Objekt.
ms.assetid: d22a378e-2d4e-4ff4-a18e-136932c24d2b
title: Funktion "konfigurireopmprotectedoutput"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: d72f3d8bbb7d3063fe6982c6d1de99b2f721f005
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393298"
---
# <a name="configureopmprotectedoutput-function"></a><span data-ttu-id="d206e-103">Funktion "konfigurireopmprotectedoutput"</span><span class="sxs-lookup"><span data-stu-id="d206e-103">ConfigureOPMProtectedOutput function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d206e-104">Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="d206e-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="d206e-105">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d206e-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="d206e-106">Konfiguriert ein geschütztes Ausgabe Objekt.</span><span class="sxs-lookup"><span data-stu-id="d206e-106">Configures a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d206e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d206e-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ConfigureOPMProtectedOutput(
  _In_       OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _In_ const DXGKMDT_OPM_CONFIGURE_PARAMETERS *pParameters,
  _In_       ULONG                            ulAdditionalParametersSize,
  _In_ const BYTE                             *pbAdditionalParameters
);
```



## <a name="parameters"></a><span data-ttu-id="d206e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d206e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d206e-109">" *opoopmprotectedoutput* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="d206e-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d206e-110">Ein Handle für das geschützte Ausgabe Objekt.</span><span class="sxs-lookup"><span data-stu-id="d206e-110">A handle to the protected output object.</span></span> <span data-ttu-id="d206e-111">Dieses Handle wird durch Aufrufen von [**createopmprotectedoutputs**](createopmprotectedoutputs.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d206e-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="d206e-112">*pparameters* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d206e-112">*pParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d206e-113">Ein Zeiger auf eine **dxgkmdt \_ OPM-Struktur zum \_ Konfigurieren von \_ Parametern** , die den Konfigurationsbefehl enthält.</span><span class="sxs-lookup"><span data-stu-id="d206e-113">A pointer to a **DXGKMDT\_OPM\_CONFIGURE\_PARAMETERS** structure that contains the configuration command.</span></span>

</dd> <dt>

<span data-ttu-id="d206e-114">*uladditionalparameterssize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d206e-114">*ulAdditionalParametersSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d206e-115">Die Größe des *pbadditionalparameters* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d206e-115">The size of the *pbAdditionalParameters* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d206e-116">*pbadditionalparameters* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d206e-116">*pbAdditionalParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d206e-117">Ein Zeiger auf einen Puffer, der zusätzliche Informationen für den Befehl enthält.</span><span class="sxs-lookup"><span data-stu-id="d206e-117">A pointer to a buffer that contains additional information for the command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d206e-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d206e-118">Return value</span></span>

<span data-ttu-id="d206e-119">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d206e-119">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="d206e-120">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d206e-120">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d206e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d206e-121">Remarks</span></span>

<span data-ttu-id="d206e-122">Anwendungen sollten [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) aufrufen, anstatt diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d206e-122">Applications should call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) instead of calling this function.</span></span>

<span data-ttu-id="d206e-123">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="d206e-123">This function has no associated import library.</span></span> <span data-ttu-id="d206e-124">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="d206e-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="d206e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d206e-125">Requirements</span></span>



| <span data-ttu-id="d206e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d206e-126">Requirement</span></span> | <span data-ttu-id="d206e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d206e-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d206e-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d206e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d206e-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d206e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d206e-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d206e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d206e-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d206e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d206e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d206e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d206e-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d206e-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d206e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d206e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d206e-135">OPM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d206e-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="d206e-136">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="d206e-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
