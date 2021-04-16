---
description: Erstellt geschützte Ausgabe Objekte für ein Anzeigegerät.
ms.assetid: 616ffb38-173b-48d0-9352-422a61e5bb15
title: Funktion "kreateopmprotectedoutputs"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateOPMProtectedOutputs
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 215cff4a76e7eb36e516e8fd2db312302763198e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524619"
---
# <a name="createopmprotectedoutputs-function"></a><span data-ttu-id="e5a66-103">Funktion "kreateopmprotectedoutputs"</span><span class="sxs-lookup"><span data-stu-id="e5a66-103">CreateOPMProtectedOutputs function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5a66-104">Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e5a66-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="e5a66-105">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e5a66-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="e5a66-106">Erstellt geschützte Ausgabe Objekte für ein Anzeigegerät.</span><span class="sxs-lookup"><span data-stu-id="e5a66-106">Creates protected output objects for a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a66-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5a66-107">Syntax</span></span>


```C++
NTSTATUS WINAPI CreateOPMProtectedOutputs(
  _In_  PUNICODE_STRING                    pstrDeviceName,
  _In_  DXGKMDT_OPM_VIDEO_OUTPUT_SEMANTICS vos,
  _In_  DWORD                              dwOPMProtectedOutputArraySize,
  _Out_ DWORD                              *pdwNumOPMProtectedOutputsInArray,
  _Out_ OPM_PROTECTED_OUTPUT_HANDLE        *pohOPMProtectedOutputArray
);
```



## <a name="parameters"></a><span data-ttu-id="e5a66-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5a66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5a66-109">*pstrindevicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5a66-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5a66-110">Ein Zeiger auf eine [**Unicode- \_ Zeichen**](/windows/win32/api/subauth/ns-subauth-unicode_string) folgen Struktur, die den Namen des Anzeige Geräts enthält, wie von der [**getmonitorinfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e5a66-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="e5a66-111">*vos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5a66-111">*vos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5a66-112">Ein Member der **dxgkmdt \_ OPM- \_ Video \_ Ausgabe \_ Semantik** -Enumeration, der angibt, ob für die geschützte Ausgabe eine zertifizierte COPP-Semantik (Output Protection Protocol) oder eine OPM-Semantik verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e5a66-112">A member of the **DXGKMDT\_OPM\_VIDEO\_OUTPUT\_SEMANTICS** enumeration, specifying whether the protected output will have Certified Output Protection Protocol (COPP) semantics or OPM semantics.</span></span>

</dd> <dt>

<span data-ttu-id="e5a66-113">*dwopmprotectedoutputarraysize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5a66-113">*dwOPMProtectedOutputArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5a66-114">Die Anzahl der Elemente im *pohopmprotectedoutputarray* -Array.</span><span class="sxs-lookup"><span data-stu-id="e5a66-114">The number of elements in the *pohOPMProtectedOutputArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="e5a66-115">*pdwnumopmprotectedoutputsinarray* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e5a66-115">*pdwNumOPMProtectedOutputsInArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5a66-116">Empfängt die Anzahl der Elemente, die die Funktion in das *pohopmprotectedoutputarray* -Array kopiert.</span><span class="sxs-lookup"><span data-stu-id="e5a66-116">Receives the number of items that the function copies to the *pohOPMProtectedOutputArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="e5a66-117">*pohopmprotectedoutputarray* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e5a66-117">*pohOPMProtectedOutputArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5a66-118">Ein Array, das Handles für die geschützten Ausgabe Objekte empfängt.</span><span class="sxs-lookup"><span data-stu-id="e5a66-118">An array that receives handles to the protected output objects.</span></span> <span data-ttu-id="e5a66-119">Jedes Handle muss durch Aufrufen von [**destroyopmprotectedoutput**](destroyopmprotectedoutput.md)freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e5a66-119">Each handle must be released by calling [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5a66-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5a66-120">Return value</span></span>

<span data-ttu-id="e5a66-121">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e5a66-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="e5a66-122">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e5a66-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5a66-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5a66-123">Remarks</span></span>

<span data-ttu-id="e5a66-124">Anstatt diese Funktion zu verwenden, sollten Anwendungen eine der folgenden Funktionen aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="e5a66-124">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="e5a66-125">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span><span class="sxs-lookup"><span data-stu-id="e5a66-125">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object)
-   [<span data-ttu-id="e5a66-126">**Opmgetvideooutputsfromhmonitor**</span><span class="sxs-lookup"><span data-stu-id="e5a66-126">**OPMGetVideoOutputsFromHMONITOR**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)

<span data-ttu-id="e5a66-127">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="e5a66-127">This function has no associated import library.</span></span> <span data-ttu-id="e5a66-128">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="e5a66-128">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5a66-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5a66-129">Requirements</span></span>



| <span data-ttu-id="e5a66-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5a66-130">Requirement</span></span> | <span data-ttu-id="e5a66-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e5a66-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a66-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5a66-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e5a66-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5a66-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e5a66-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5a66-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e5a66-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5a66-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e5a66-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e5a66-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5a66-137"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5a66-137"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5a66-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5a66-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5a66-139">OPM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e5a66-139">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="e5a66-140">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="e5a66-140">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
