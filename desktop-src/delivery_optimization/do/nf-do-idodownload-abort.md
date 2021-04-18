---
title: 'Idodownload:: Abort-Methode'
description: Bricht den Download ab.
keywords:
- 'Idodownload:: Abort-Methode'
topic_type:
- apiref
api_name:
- IDODownload.Abort
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: babcd5ee00689ac103288074467980777f644668
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106340878"
---
# <a name="idodownloadabort-method"></a><span data-ttu-id="2120a-104">Idodownload:: Abort-Methode</span><span class="sxs-lookup"><span data-stu-id="2120a-104">IDODownload::Abort method</span></span>

<span data-ttu-id="2120a-105">Bricht den Download ab.</span><span class="sxs-lookup"><span data-stu-id="2120a-105">Aborts the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="2120a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2120a-106">Syntax</span></span>

```cpp
HRESULT Abort();
```

## <a name="return-value"></a><span data-ttu-id="2120a-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2120a-107">Return Value</span></span>

<span data-ttu-id="2120a-108">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2120a-108">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="2120a-109">Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2120a-109">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="2120a-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2120a-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2120a-111">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="2120a-111">**Minimum supported client**</span></span> | <span data-ttu-id="2120a-112">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="2120a-112">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="2120a-113">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="2120a-113">**Minimum supported server**</span></span> | <span data-ttu-id="2120a-114">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="2120a-114">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="2120a-115">**Header**</span><span class="sxs-lookup"><span data-stu-id="2120a-115">**Header**</span></span> | <span data-ttu-id="2120a-116">Do. h</span><span class="sxs-lookup"><span data-stu-id="2120a-116">Do.h</span></span> |
