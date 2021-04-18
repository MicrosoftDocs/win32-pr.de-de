---
title: 'Idodownload:: Finalize-Methode'
description: Schließt den Download ab.
keywords:
- 'Idodownload:: Finalize-Methode'
topic_type:
- apiref
api_name:
- IDODownload.Finalize
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 6befc9a7e64fb0963d45257d68d6bb8d2ba7a2cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106340474"
---
# <a name="idodownloadfinalize-method"></a><span data-ttu-id="1bc0e-104">Idodownload:: Finalize-Methode</span><span class="sxs-lookup"><span data-stu-id="1bc0e-104">IDODownload::Finalize method</span></span>

<span data-ttu-id="1bc0e-105">Schließt den Download ab.</span><span class="sxs-lookup"><span data-stu-id="1bc0e-105">Finalizes the download.</span></span> <span data-ttu-id="1bc0e-106">Nachdem der Download abgeschlossen ist, kann ein Download nicht mehr fortgesetzt **werden.**</span><span class="sxs-lookup"><span data-stu-id="1bc0e-106">Once finalized, a download cannot be resumed by calling **Start**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bc0e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bc0e-107">Syntax</span></span>

```cpp
HRESULT Finalize();
```

## <a name="return-value"></a><span data-ttu-id="1bc0e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1bc0e-108">Return Value</span></span>

<span data-ttu-id="1bc0e-109">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1bc0e-109">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="1bc0e-110">Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1bc0e-110">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="1bc0e-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1bc0e-111">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1bc0e-112">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="1bc0e-112">**Minimum supported client**</span></span> | <span data-ttu-id="1bc0e-113">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="1bc0e-113">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="1bc0e-114">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="1bc0e-114">**Minimum supported server**</span></span> | <span data-ttu-id="1bc0e-115">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="1bc0e-115">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="1bc0e-116">**Header**</span><span class="sxs-lookup"><span data-stu-id="1bc0e-116">**Header**</span></span> | <span data-ttu-id="1bc0e-117">Do. h</span><span class="sxs-lookup"><span data-stu-id="1bc0e-117">Do.h</span></span> |
