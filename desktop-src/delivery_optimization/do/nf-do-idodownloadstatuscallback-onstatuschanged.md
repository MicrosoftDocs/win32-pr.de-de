---
title: 'Idodownloadstatus Callback:: OnStatusChange-Methode'
description: Ruft die Implementierung dieser Methode immer dann auf, wenn sich ein Download Status geändert hat.
keywords:
- 'Idodownloadstatus Callback:: OnStatusChange-Methode'
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback.OnStatusChange
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 9abf13969a6183f98102792b9bcf7a3329ca243d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104038394"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a><span data-ttu-id="21ddf-104">Idodownloadstatus Callback:: OnStatusChange-Methode</span><span class="sxs-lookup"><span data-stu-id="21ddf-104">IDODownloadStatusCallback::OnStatusChange method</span></span>

<span data-ttu-id="21ddf-105">Ruft die Implementierung dieser Methode immer dann auf, wenn sich ein Download Status geändert hat.</span><span class="sxs-lookup"><span data-stu-id="21ddf-105">DO calls your implementation of this method any time a download status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="21ddf-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="21ddf-106">Syntax</span></span>

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a><span data-ttu-id="21ddf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="21ddf-107">Parameters</span></span>

`download`

<span data-ttu-id="21ddf-108">Ein Zeiger auf die **idodownload** -Schnittstelle, deren Status geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="21ddf-108">An pointer to the **IDODownload** interface whose status changed.</span></span>

`status`

<span data-ttu-id="21ddf-109">Ein Zeiger auf eine **DO_DOWNLOAD_STATUS** Struktur, die den Download Status enthält.</span><span class="sxs-lookup"><span data-stu-id="21ddf-109">A pointer to a **DO_DOWNLOAD_STATUS** structure containing the download's status.</span></span>

## <a name="return-value"></a><span data-ttu-id="21ddf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21ddf-110">Return Value</span></span>

<span data-ttu-id="21ddf-111">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="21ddf-111">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="21ddf-112">Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="21ddf-112">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="21ddf-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21ddf-113">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="21ddf-114">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="21ddf-114">**Minimum supported client**</span></span> | <span data-ttu-id="21ddf-115">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="21ddf-115">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="21ddf-116">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="21ddf-116">**Minimum supported server**</span></span> | <span data-ttu-id="21ddf-117">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="21ddf-117">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="21ddf-118">**Header**</span><span class="sxs-lookup"><span data-stu-id="21ddf-118">**Header**</span></span> | <span data-ttu-id="21ddf-119">Do. h</span><span class="sxs-lookup"><span data-stu-id="21ddf-119">Do.h</span></span> |
