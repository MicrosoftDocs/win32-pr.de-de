---
title: 'Idodownload:: GetStatus-Methode'
description: Ruft einen Zeiger auf eine **DO_DOWNLOAD_STATUS** -Struktur ab, die den aktuellen Status des Downloads widerspiegelt.
keywords:
- 'Idodownload:: GetStatus-Methode'
topic_type:
- apiref
api_name:
- IDODownload.GetStatus
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 8b9b2603354bbb5345cf866ee0c94785a254952d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104389652"
---
# <a name="idodownloadgetstatus-method"></a><span data-ttu-id="d4d16-104">Idodownload:: GetStatus-Methode</span><span class="sxs-lookup"><span data-stu-id="d4d16-104">IDODownload::GetStatus method</span></span>

<span data-ttu-id="d4d16-105">Ruft einen Zeiger auf eine **DO_DOWNLOAD_STATUS** -Struktur ab, die den aktuellen Status des Downloads widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="d4d16-105">Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d16-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4d16-106">Syntax</span></span>

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a><span data-ttu-id="d4d16-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4d16-107">Parameters</span></span>

`status`

<span data-ttu-id="d4d16-108">Ein Zeiger auf eine **DO_DOWNLOAD_STATUS** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d4d16-108">A pointer to a **DO_DOWNLOAD_STATUS** structure.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4d16-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4d16-109">Return Value</span></span>

<span data-ttu-id="d4d16-110">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d4d16-110">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="d4d16-111">Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d4d16-111">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4d16-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4d16-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d4d16-113">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="d4d16-113">**Minimum supported client**</span></span> | <span data-ttu-id="d4d16-114">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="d4d16-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d4d16-115">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="d4d16-115">**Minimum supported server**</span></span> | <span data-ttu-id="d4d16-116">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="d4d16-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d4d16-117">**Header**</span><span class="sxs-lookup"><span data-stu-id="d4d16-117">**Header**</span></span> | <span data-ttu-id="d4d16-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="d4d16-118">Do.h</span></span> |
