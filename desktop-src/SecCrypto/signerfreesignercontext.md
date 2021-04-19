---
description: Gibt eine Signatur Geber \_ Kontext Struktur frei, die durch einen vorherigen-Befehl der signersignetx-Funktion zugeordnet wurde.
ms.assetid: 190de302-50fe-488e-90ed-c9efd39dae70
title: Signerfresignercontext-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerFreeSignerContext
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 284b1cbf5755da06e9454b86ac9eacef5fbf613f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349526"
---
# <a name="signerfreesignercontext-function"></a><span data-ttu-id="772d2-103">Signerfresignercontext-Funktion</span><span class="sxs-lookup"><span data-stu-id="772d2-103">SignerFreeSignerContext function</span></span>

<span data-ttu-id="772d2-104">Die **signerfresignercontext** -Funktion gibt eine [**Signatur Geber \_ Kontext**](signer-context.md) Struktur frei, die durch einen vorherigen-Befehl der [**signersignetx**](signersignex.md) -Funktion zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="772d2-104">The **SignerFreeSignerContext** function frees a [**SIGNER\_CONTEXT**](signer-context.md) structure allocated by a previous call to the [**SignerSignEx**](signersignex.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="772d2-105">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="772d2-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="772d2-106">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="772d2-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="772d2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="772d2-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerFreeSignerContext(
  _In_ SIGNER_CONTEXT *pSignerContext
);
```



## <a name="parameters"></a><span data-ttu-id="772d2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="772d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="772d2-109">*psignercontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="772d2-109">*pSignerContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772d2-110">Ein Zeiger auf die frei verfügbaren Signatur Geber- [**\_ Kontext**](signer-context.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="772d2-110">A pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="772d2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="772d2-111">Return value</span></span>

<span data-ttu-id="772d2-112">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="772d2-112">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="772d2-113">Wenn die Funktion fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="772d2-113">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="772d2-114">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="772d2-114">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="772d2-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="772d2-115">Requirements</span></span>



| <span data-ttu-id="772d2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="772d2-116">Requirement</span></span> | <span data-ttu-id="772d2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="772d2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="772d2-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="772d2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="772d2-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="772d2-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="772d2-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="772d2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="772d2-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="772d2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="772d2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="772d2-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="772d2-123"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="772d2-123"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="772d2-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="772d2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="772d2-125">**Signatur Geber \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="772d2-125">**SIGNER\_CONTEXT**</span></span>](signer-context.md)
</dt> <dt>

[<span data-ttu-id="772d2-126">**Signersignetx**</span><span class="sxs-lookup"><span data-stu-id="772d2-126">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
