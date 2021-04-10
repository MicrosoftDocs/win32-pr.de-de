---
title: Idodownload::P ause-Methode
description: Hält den Download an.
keywords:
- Idodownload::P ause-Methode
topic_type:
- apiref
api_name:
- IDODownload.Pause
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a7239253238b0d9b7e606329b10f05b3645b7e16
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104101134"
---
# <a name="idodownloadpause-method"></a><span data-ttu-id="2f646-104">Idodownload::P ause-Methode</span><span class="sxs-lookup"><span data-stu-id="2f646-104">IDODownload::Pause method</span></span>

<span data-ttu-id="2f646-105">Hält den Download an.</span><span class="sxs-lookup"><span data-stu-id="2f646-105">Pauses the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f646-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f646-106">Syntax</span></span>

```cpp
HRESULT Pause();
```

## <a name="return-value"></a><span data-ttu-id="2f646-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f646-107">Return Value</span></span>

<span data-ttu-id="2f646-108">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f646-108">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="2f646-109">Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f646-109">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f646-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f646-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2f646-111">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="2f646-111">**Minimum supported client**</span></span> | <span data-ttu-id="2f646-112">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="2f646-112">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="2f646-113">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="2f646-113">**Minimum supported server**</span></span> | <span data-ttu-id="2f646-114">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="2f646-114">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="2f646-115">**Header**</span><span class="sxs-lookup"><span data-stu-id="2f646-115">**Header**</span></span> | <span data-ttu-id="2f646-116">Do. h</span><span class="sxs-lookup"><span data-stu-id="2f646-116">Do.h</span></span> |
