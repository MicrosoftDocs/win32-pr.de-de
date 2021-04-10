---
description: Legt den Signatur Schlüssel und zwei Sequenznummern für ein geschütztes Ausgabe Objekt fest.
ms.assetid: 278a80f5-198d-4311-aa43-10b6dc33b3a4
title: Stopmsigningkeyandsequencenumbers-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetOPMSigningKeyAndSequenceNumbers
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: cbd088b83acd4e93cc186e6c7b5635ad1e3d8346
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215008"
---
# <a name="setopmsigningkeyandsequencenumbers-function"></a><span data-ttu-id="c6244-103">Stopmsigningkeyandsequencenumbers-Funktion</span><span class="sxs-lookup"><span data-stu-id="c6244-103">SetOPMSigningKeyAndSequenceNumbers function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c6244-104">Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c6244-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="c6244-105">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c6244-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="c6244-106">Legt den Signatur Schlüssel und zwei Sequenznummern für ein geschütztes Ausgabe Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="c6244-106">Sets the signing key and two sequence numbers on a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6244-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6244-107">Syntax</span></span>


```C++
NTSTATUS WINAPI SetOPMSigningKeyAndSequenceNumbers(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _Out_ const DXGKMDT_OPM_ENCRYPTED_PARAMETERS *pParameters
);
```



## <a name="parameters"></a><span data-ttu-id="c6244-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6244-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6244-109">" *opoopmprotectedoutput* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="c6244-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6244-110">Ein Handle für das geschützte Ausgabe Objekt.</span><span class="sxs-lookup"><span data-stu-id="c6244-110">A handle to the protected output object.</span></span> <span data-ttu-id="c6244-111">Dieses Handle wird durch Aufrufen von [**createopmprotectedoutputs**](createopmprotectedoutputs.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c6244-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6244-112">*pparameters* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c6244-112">*pParameters* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6244-113">Ein Zeiger auf eine [**dxgkmdt \_ OPM- \_ verschlüsselte \_ Parameter**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) Struktur, die ein 256-Byte-Array enthält.</span><span class="sxs-lookup"><span data-stu-id="c6244-113">A pointer to a [**DXGKMDT\_OPM\_ENCRYPTED\_PARAMETERS**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) structure that contains a 256-byte array.</span></span> <span data-ttu-id="c6244-114">Weitere Informationen zum Initialisieren dieses Arrays finden Sie unter [dxgkddiopmsetsigningkeyandsequencenumschlag](https://msdn.microsoft.com/library/aa906703.aspx).</span><span class="sxs-lookup"><span data-stu-id="c6244-114">For more information about how to initialize this array, see [DxgkDdiOPMSetSigningKeyAndSequenceNumbers](https://msdn.microsoft.com/library/aa906703.aspx).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6244-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6244-115">Return value</span></span>

<span data-ttu-id="c6244-116">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6244-116">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="c6244-117">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6244-117">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6244-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6244-118">Remarks</span></span>

<span data-ttu-id="c6244-119">Anwendungen sollten [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) aufrufen, anstatt diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c6244-119">Applications should call [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) instead of calling this function.</span></span>

<span data-ttu-id="c6244-120">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="c6244-120">This function has no associated import library.</span></span> <span data-ttu-id="c6244-121">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="c6244-121">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6244-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6244-122">Requirements</span></span>



| <span data-ttu-id="c6244-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6244-123">Requirement</span></span> | <span data-ttu-id="c6244-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c6244-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c6244-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6244-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c6244-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6244-126">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c6244-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6244-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c6244-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6244-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c6244-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c6244-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6244-130"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6244-130"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6244-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6244-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6244-132">OPM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c6244-132">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="c6244-133">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="c6244-133">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
