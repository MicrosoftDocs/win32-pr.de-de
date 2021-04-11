---
description: Ruft die Größe des Arrays ab, das vor dem Aufrufen von createopmprotectedoutputs zugewiesen werden soll.
ms.assetid: 65edce14-f225-4b7f-b953-32b085e1cabf
title: Getvorschlags stedopmprotectedoutputarraysize-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSuggestedOPMProtectedOutputArraySize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 87139f0b485ef3c01e5196db85b36faeb662e4d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127877"
---
# <a name="getsuggestedopmprotectedoutputarraysize-function"></a><span data-ttu-id="9c194-103">Getvorschlags stedopmprotectedoutputarraysize-Funktion</span><span class="sxs-lookup"><span data-stu-id="9c194-103">GetSuggestedOPMProtectedOutputArraySize function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9c194-104">Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="9c194-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="9c194-105">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9c194-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="9c194-106">Ruft die Größe des Arrays ab, das vor dem Aufrufen von [**createopmprotectedoutputs**](createopmprotectedoutputs.md)zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c194-106">Gets the size of the array that should be allocated before calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9c194-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c194-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetSuggestedOPMProtectedOutputArraySize(
  _In_  PUNICODE_STRING pstrDeviceName,
  _Out_ DWORD           *pdwSuggestedOPMProtectedOutputArraySize
);
```



## <a name="parameters"></a><span data-ttu-id="9c194-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c194-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c194-109">*pstrindevicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c194-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c194-110">Ein Zeiger auf eine [**Unicode- \_ Zeichen**](/windows/win32/api/subauth/ns-subauth-unicode_string) folgen Struktur, die den Namen des Anzeige Geräts enthält, wie von der [**getmonitorinfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c194-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="9c194-111">*pdwvorschlags stedopmprotectedoutputarraysize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9c194-111">*pdwSuggestedOPMProtectedOutputArraySize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c194-112">Empfängt die Größe, die für das Array zugeordnet werden soll, als Anzahl von Array Elementen.</span><span class="sxs-lookup"><span data-stu-id="9c194-112">Receives the size that should be allocated for the array, in number of array elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c194-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c194-113">Return value</span></span>

<span data-ttu-id="9c194-114">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c194-114">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="9c194-115">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c194-115">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c194-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c194-116">Remarks</span></span>

<span data-ttu-id="9c194-117">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="9c194-117">This function has no associated import library.</span></span> <span data-ttu-id="9c194-118">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="9c194-118">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c194-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c194-119">Requirements</span></span>



| <span data-ttu-id="9c194-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c194-120">Requirement</span></span> | <span data-ttu-id="9c194-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9c194-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9c194-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c194-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9c194-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c194-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9c194-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c194-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9c194-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c194-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9c194-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9c194-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c194-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c194-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c194-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c194-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c194-129">OPM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9c194-129">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="9c194-130">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="9c194-130">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
