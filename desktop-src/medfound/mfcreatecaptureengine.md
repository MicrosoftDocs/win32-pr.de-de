---
description: Erstellt eine Instanz der Erfassungs-Engine.
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: Mfikreatecaptureengine-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateCaptureEngine
api_type:
- DllExport
api_location:
- MFCaptureEngine.dll
ms.openlocfilehash: a2ff0dbf46ca464c11570c8fe78e0b3dbebe3248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343357"
---
# <a name="mfcreatecaptureengine-function"></a><span data-ttu-id="bc875-103">Mfikreatecaptureengine-Funktion</span><span class="sxs-lookup"><span data-stu-id="bc875-103">MFCreateCaptureEngine function</span></span>

<span data-ttu-id="bc875-104">\[Mfikreatecaptureengine wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="bc875-104">\[MFCreateCaptureEngine is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="bc875-105">\]</span><span class="sxs-lookup"><span data-stu-id="bc875-105">\]</span></span>

<span data-ttu-id="bc875-106">Erstellt eine Instanz der Erfassungs-Engine.</span><span class="sxs-lookup"><span data-stu-id="bc875-106">Creates an instance of the capture engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc875-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc875-107">Syntax</span></span>


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a><span data-ttu-id="bc875-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc875-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc875-109">*ppcaptureengine* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bc875-109">*ppCaptureEngine* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc875-110">Empfängt einen Zeiger auf die [**imfcaptureengine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bc875-110">Receives a pointer to the [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) interface.</span></span> <span data-ttu-id="bc875-111">Der Aufrufer muss die-Schnittstelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="bc875-111">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc875-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc875-112">Return value</span></span>

<span data-ttu-id="bc875-113">Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="bc875-113">If the function succeeds, it returns S\_OK.</span></span> <span data-ttu-id="bc875-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bc875-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc875-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc875-115">Remarks</span></span>

<span data-ttu-id="bc875-116">Diese Funktion verfügt über keine zugeordnete Import Bibliothek und ist nicht in einer öffentlichen Header Datei deklariert.</span><span class="sxs-lookup"><span data-stu-id="bc875-116">This function has no associated import library and is not declared in a public header file.</span></span> <span data-ttu-id="bc875-117">Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit MFCaptureEngine.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="bc875-117">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to MFCaptureEngine.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc875-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc875-118">Requirements</span></span>



| <span data-ttu-id="bc875-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc875-119">Requirement</span></span> | <span data-ttu-id="bc875-120">Wert</span><span class="sxs-lookup"><span data-stu-id="bc875-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc875-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc875-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bc875-122">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc875-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bc875-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc875-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bc875-124">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc875-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc875-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bc875-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc875-126"><dt>MFCaptureEngine.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc875-126"><dt>MFCaptureEngine.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc875-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc875-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc875-128">Media Foundation Funktionen</span><span class="sxs-lookup"><span data-stu-id="bc875-128">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
