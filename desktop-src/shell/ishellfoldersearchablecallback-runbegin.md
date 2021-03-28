---
description: Gibt an, dass eine Suche gestartet wurde.
title: 'Ishellfoldersearchablecallback:: RunBegin-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunBegin
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6e3ae592-a0cb-4d9d-b186-241a757da5ea
ms.openlocfilehash: 2bef0f29486143f97f886c0d31ab456a070ed857
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527314"
---
# <a name="ishellfoldersearchablecallbackrunbegin-method"></a><span data-ttu-id="c75f3-103">Ishellfoldersearchablecallback:: RunBegin-Methode</span><span class="sxs-lookup"><span data-stu-id="c75f3-103">IShellFolderSearchableCallback::RunBegin method</span></span>

<span data-ttu-id="c75f3-104">Gibt an, dass eine Suche gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="c75f3-104">Indicates that a search was started.</span></span>

## <a name="syntax"></a><span data-ttu-id="c75f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c75f3-105">Syntax</span></span>


```C++
HRESULT RunBegin(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="c75f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c75f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c75f3-107">*dwReserved* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c75f3-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c75f3-108">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c75f3-108">Type: **DWORD**</span></span>

<span data-ttu-id="c75f3-109">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="c75f3-109">Reserved.</span></span> <span data-ttu-id="c75f3-110">Muss auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c75f3-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c75f3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c75f3-111">Return value</span></span>

<span data-ttu-id="c75f3-112">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c75f3-112">Type: **HRESULT**</span></span>

<span data-ttu-id="c75f3-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c75f3-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c75f3-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c75f3-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c75f3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c75f3-115">Remarks</span></span>

<span data-ttu-id="c75f3-116">Als Reaktion auf diesen Rückruf kann die Anwendung z. b. die Schaltfläche " **Abbrechen** " aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c75f3-116">In response to this callback, the application may enable the **Cancel** button, for example.</span></span>

## <a name="requirements"></a><span data-ttu-id="c75f3-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c75f3-117">Requirements</span></span>



| <span data-ttu-id="c75f3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c75f3-118">Requirement</span></span> | <span data-ttu-id="c75f3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c75f3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c75f3-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c75f3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c75f3-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c75f3-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c75f3-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c75f3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c75f3-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c75f3-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c75f3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c75f3-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c75f3-125"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c75f3-125"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




