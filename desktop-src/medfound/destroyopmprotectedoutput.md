---
description: Gibt ein geschütztes Ausgabe Objekt frei.
ms.assetid: e9b09fd7-9db2-4189-b347-55f5fede2f80
title: Destroyopmprotectedoutput-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 0a7ce8551cc5e01e7a2801dd129d5dc6903af697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342622"
---
# <a name="destroyopmprotectedoutput-function"></a><span data-ttu-id="a10f7-103">Destroyopmprotectedoutput-Funktion</span><span class="sxs-lookup"><span data-stu-id="a10f7-103">DestroyOPMProtectedOutput function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a10f7-104">Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="a10f7-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="a10f7-105">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a10f7-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="a10f7-106">Gibt ein geschütztes Ausgabe Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="a10f7-106">Releases a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a10f7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a10f7-107">Syntax</span></span>


```C++
NTSTATUS WINAPI DestroyOPMProtectedOutput(
  _In_ OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput
);
```



## <a name="parameters"></a><span data-ttu-id="a10f7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a10f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a10f7-109">" *opoopmprotectedoutput* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="a10f7-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a10f7-110">Ein Handle für das geschützte Ausgabe Objekt.</span><span class="sxs-lookup"><span data-stu-id="a10f7-110">A handle to the protected output object.</span></span> <span data-ttu-id="a10f7-111">Dieses Handle wird durch Aufrufen von [**createopmprotectedoutputs**](createopmprotectedoutputs.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a10f7-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a10f7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a10f7-112">Return value</span></span>

<span data-ttu-id="a10f7-113">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a10f7-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="a10f7-114">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a10f7-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a10f7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a10f7-115">Remarks</span></span>

<span data-ttu-id="a10f7-116">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="a10f7-116">This function has no associated import library.</span></span> <span data-ttu-id="a10f7-117">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="a10f7-117">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="a10f7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a10f7-118">Requirements</span></span>



| <span data-ttu-id="a10f7-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a10f7-119">Requirement</span></span> | <span data-ttu-id="a10f7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a10f7-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a10f7-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a10f7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a10f7-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a10f7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a10f7-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a10f7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a10f7-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a10f7-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a10f7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a10f7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a10f7-126"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a10f7-126"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a10f7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a10f7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a10f7-128">OPM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a10f7-128">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="a10f7-129">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="a10f7-129">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
