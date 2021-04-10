---
title: Wsdumpmemory-Funktion (webservicesdebug. h)
description: Diese Funktion sichert alle Speicher Belegungen in der Konsole.
ms.assetid: 84a4f1e7-7d62-48c2-a8a3-ee4573bde5e4
keywords:
- Wsdumpmemory-funktionsweb Dienste für Windows
topic_type:
- apiref
api_name:
- WsDumpMemory
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70af8d34b3ee04a9db4128ce1063bd31e81306eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956942"
---
# <a name="wsdumpmemory-function"></a><span data-ttu-id="bb835-104">Wsdumpmemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="bb835-104">WsDumpMemory function</span></span>

<span data-ttu-id="bb835-105">Diese Funktion sichert alle Speicher Belegungen in der Konsole.</span><span class="sxs-lookup"><span data-stu-id="bb835-105">This function dumps all memory allocations to the console.</span></span>

> [!Note]  
> <span data-ttu-id="bb835-106">Diese Funktion dient nur zum Debuggen.</span><span class="sxs-lookup"><span data-stu-id="bb835-106">This function is for DEBUG ONLY.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bb835-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb835-107">Syntax</span></span>


```C++
HRESULT WINAPI  WsDumpMemory(
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a><span data-ttu-id="bb835-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb835-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb835-109">*Fehler* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="bb835-109">*error* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bb835-110">Ein Zeiger auf ein [WS- \_ Fehler](ws-error.md) Objekt, in dem zusätzliche Informationen über den Fehler gespeichert werden sollen, wenn die Funktion fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="bb835-110">A pointer to a [WS\_ERROR](ws-error.md) object where additional information about the error should be stored if the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb835-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb835-111">Return value</span></span>

<span data-ttu-id="bb835-112">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="bb835-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb835-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bb835-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb835-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb835-114">Requirements</span></span>



| <span data-ttu-id="bb835-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb835-115">Requirement</span></span> | <span data-ttu-id="bb835-116">Wert</span><span class="sxs-lookup"><span data-stu-id="bb835-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb835-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb835-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bb835-118">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bb835-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                             |
| <span data-ttu-id="bb835-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb835-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bb835-120">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bb835-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="bb835-121">Header</span><span class="sxs-lookup"><span data-stu-id="bb835-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb835-122"><dt>Webservicesdebug. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb835-122"><dt>WebServicesDebug.h</dt></span></span> </dl> |



 

 





