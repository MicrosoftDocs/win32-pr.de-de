---
description: Ruft eine kryptografisch sichere Zufallszahl mit 128 Bit aus einem geschützten Ausgabe Objekt ab.
ms.assetid: d5adfa5c-ae61-43d5-916d-05085abea38b
title: Getopmrandomnumber-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMRandomNumber
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: f78b17dcf9ffff7a5fa26ce16e96299e5cf8386c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342449"
---
# <a name="getopmrandomnumber-function"></a><span data-ttu-id="bbc1c-103">Getopmrandomnumber-Funktion</span><span class="sxs-lookup"><span data-stu-id="bbc1c-103">GetOPMRandomNumber function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bbc1c-104">Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="bbc1c-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="bbc1c-105">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="bbc1c-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="bbc1c-106">Ruft eine kryptografisch sichere Zufallszahl mit 128 Bit aus einem geschützten Ausgabe Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="bbc1c-106">Gets a 128-bit, cryptographically secure random number from a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbc1c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbc1c-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetOPMRandomNumber(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput,
  _Out_ DXGKMDT_OPM_RANDOM_NUMBER   *prnRandomNumber
);
```



## <a name="parameters"></a><span data-ttu-id="bbc1c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bbc1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbc1c-109">" *opoopmprotectedoutput* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="bbc1c-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbc1c-110">Ein Handle für das geschützte Ausgabe Objekt.</span><span class="sxs-lookup"><span data-stu-id="bbc1c-110">A handle to the protected output object.</span></span> <span data-ttu-id="bbc1c-111">Dieses Handle wird durch Aufrufen von [**createopmprotectedoutputs**](createopmprotectedoutputs.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="bbc1c-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbc1c-112">*prnrandomnumber* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bbc1c-112">*prnRandomNumber* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbc1c-113">Ein Zeiger auf eine **dxgkmdt- \_ OPM- \_ Zufalls \_ Zahlen** Struktur, die die Zufallszahl empfängt.</span><span class="sxs-lookup"><span data-stu-id="bbc1c-113">A pointer to a **DXGKMDT\_OPM\_RANDOM\_NUMBER** structure that receives the random number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbc1c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bbc1c-114">Return value</span></span>

<span data-ttu-id="bbc1c-115">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bbc1c-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="bbc1c-116">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bbc1c-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbc1c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbc1c-117">Remarks</span></span>

<span data-ttu-id="bbc1c-118">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="bbc1c-118">This function has no associated import library.</span></span> <span data-ttu-id="bbc1c-119">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="bbc1c-119">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbc1c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbc1c-120">Requirements</span></span>



| <span data-ttu-id="bbc1c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbc1c-121">Requirement</span></span> | <span data-ttu-id="bbc1c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="bbc1c-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc1c-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bbc1c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bbc1c-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbc1c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bbc1c-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bbc1c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bbc1c-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbc1c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bbc1c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bbc1c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbc1c-128"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbc1c-128"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbc1c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbc1c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbc1c-130">OPM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="bbc1c-130">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="bbc1c-131">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="bbc1c-131">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
