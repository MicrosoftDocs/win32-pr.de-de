---
description: Gibt an, dass eine Suche abgeschlossen wurde.
title: 'Ishellfoldersearchablecallback:: RunEnd-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunEnd
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91700764-6cdf-488d-adc0-e34d9b4cb71d
ms.openlocfilehash: 73155e65f4b6edb4a4b4b9b0d52ab5b042fa68b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994151"
---
# <a name="ishellfoldersearchablecallbackrunend-method"></a><span data-ttu-id="3db44-103">Ishellfoldersearchablecallback:: RunEnd-Methode</span><span class="sxs-lookup"><span data-stu-id="3db44-103">IShellFolderSearchableCallback::RunEnd method</span></span>

<span data-ttu-id="3db44-104">Gibt an, dass eine Suche abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3db44-104">Indicates that a search has finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="3db44-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3db44-105">Syntax</span></span>


```C++
HRESULT RunEnd(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="3db44-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3db44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3db44-107">*dwReserved* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3db44-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3db44-108">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3db44-108">Type: **DWORD**</span></span>

<span data-ttu-id="3db44-109">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="3db44-109">Reserved.</span></span> <span data-ttu-id="3db44-110">Muss auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3db44-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3db44-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3db44-111">Return value</span></span>

<span data-ttu-id="3db44-112">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3db44-112">Type: **HRESULT**</span></span>

<span data-ttu-id="3db44-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="3db44-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3db44-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3db44-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3db44-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3db44-115">Requirements</span></span>



| <span data-ttu-id="3db44-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3db44-116">Requirement</span></span> | <span data-ttu-id="3db44-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3db44-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3db44-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3db44-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3db44-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3db44-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3db44-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3db44-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3db44-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3db44-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3db44-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3db44-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3db44-123"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3db44-123"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




