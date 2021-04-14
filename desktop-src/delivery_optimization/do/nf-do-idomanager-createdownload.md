---
title: 'Idomanager:: kreatedownload-Methode'
description: Erstellt einen neuen Download.
keywords:
- 'Idomanager:: kreatedownload-Methode'
topic_type:
- apiref
api_name:
- IDOManager.CreateDownload
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b79bf0a1c5602fafea113585dfe6e8ca5b01057c
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104389650"
---
# <a name="idomanagercreatedownload-method"></a><span data-ttu-id="4f04b-104">Idomanager:: kreatedownload-Methode</span><span class="sxs-lookup"><span data-stu-id="4f04b-104">IDOManager::CreateDownload method</span></span>

<span data-ttu-id="4f04b-105">Erstellt einen neuen Download.</span><span class="sxs-lookup"><span data-stu-id="4f04b-105">Creates a new download.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f04b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f04b-106">Syntax</span></span>

```cpp
HRESULT CreateDownload(
  IDODownload **download
);
```

## <a name="parameters"></a><span data-ttu-id="4f04b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f04b-107">Parameters</span></span>

`download`

<span data-ttu-id="4f04b-108">Die Adresse eines **idodownload** -Schnittstellen Zeigers.</span><span class="sxs-lookup"><span data-stu-id="4f04b-108">The address of an **IDODownload** interface pointer.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f04b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f04b-109">Return Value</span></span>

<span data-ttu-id="4f04b-110">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f04b-110">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="4f04b-111">Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f04b-111">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f04b-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f04b-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4f04b-113">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="4f04b-113">**Minimum supported client**</span></span> | <span data-ttu-id="4f04b-114">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="4f04b-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="4f04b-115">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="4f04b-115">**Minimum supported server**</span></span> | <span data-ttu-id="4f04b-116">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="4f04b-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="4f04b-117">**Header**</span><span class="sxs-lookup"><span data-stu-id="4f04b-117">**Header**</span></span> | <span data-ttu-id="4f04b-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="4f04b-118">Do.h</span></span> |
