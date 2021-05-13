---
description: Gibt an, dass eine Suche abgeschlossen wurde.
title: IShellFolderSearchableCallback::RunEnd-Methode
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
ms.openlocfilehash: c23d461fdbd175a80a8fa94fcc238f6cf2f89869
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842821"
---
# <a name="ishellfoldersearchablecallbackrunend-method"></a><span data-ttu-id="7b75d-103">IShellFolderSearchableCallback::RunEnd-Methode</span><span class="sxs-lookup"><span data-stu-id="7b75d-103">IShellFolderSearchableCallback::RunEnd method</span></span>

<span data-ttu-id="7b75d-104">Gibt an, dass eine Suche abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7b75d-104">Indicates that a search has finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b75d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b75d-105">Syntax</span></span>


```C++
HRESULT RunEnd(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="7b75d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b75d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b75d-107">*dwReserved* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7b75d-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b75d-108">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7b75d-108">Type: **DWORD**</span></span>

<span data-ttu-id="7b75d-109">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="7b75d-109">Reserved.</span></span> <span data-ttu-id="7b75d-110">Muss auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7b75d-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b75d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b75d-111">Return value</span></span>

<span data-ttu-id="7b75d-112">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7b75d-112">Type: **HRESULT**</span></span>

<span data-ttu-id="7b75d-113">Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7b75d-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7b75d-114">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7b75d-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b75d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b75d-115">Requirements</span></span>



| <span data-ttu-id="7b75d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b75d-116">Requirement</span></span> | <span data-ttu-id="7b75d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7b75d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b75d-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b75d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7b75d-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b75d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7b75d-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b75d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7b75d-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b75d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7b75d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7b75d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b75d-123"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b75d-123"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




