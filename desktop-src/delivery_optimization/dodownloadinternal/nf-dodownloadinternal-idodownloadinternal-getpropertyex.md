---
title: 'Idodownloadinternal:: getpropertyex-Methode'
description: Ruft einen Zeiger auf einen **Variant** -Wert ab, der einen bestimmten erweiterten Download-Eigenschafts Wert enthält.
keywords:
- 'Idodownloadinternal:: getpropertyex-Methode'
topic_type:
- apiref
api_name:
- IDODownloadInternal.GetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 908f9b15df5c0c4a2769149419ff12d545201e5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390577"
---
# <a name="idodownloadinternalgetpropertyex-method"></a><span data-ttu-id="563b3-104">Idodownloadinternal:: getpropertyex-Methode</span><span class="sxs-lookup"><span data-stu-id="563b3-104">IDODownloadInternal::GetPropertyEx method</span></span>

> [!IMPORTANT]
> <span data-ttu-id="563b3-105">Die **idodownloadinternal** -Schnittstelle ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="563b3-105">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="563b3-106">Verwenden Sie stattdessen die [idodownload](../do/nn-do-idodownload.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="563b3-106">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="563b3-107">Ruft einen Zeiger auf einen **Variant** -Wert ab, der einen bestimmten erweiterten Download-Eigenschafts Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="563b3-107">Retrieves a pointer to a **VARIANT** that contains a specific extended download property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="563b3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="563b3-108">Syntax</span></span>

```cpp
HRESULT GetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="563b3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="563b3-109">Parameters</span></span>

`propId`

<span data-ttu-id="563b3-110">Die erforderliche eigen schafts-ID (vom Typ " **dodownloadpropertyex**").</span><span class="sxs-lookup"><span data-stu-id="563b3-110">The required property ID to get (of type **DODownloadPropertyEx**).</span></span>

`propVal`

<span data-ttu-id="563b3-111">Der resultierende Eigenschafts Wert, der in einem **Variant**-Objekt gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="563b3-111">The resulting property value, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="563b3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="563b3-112">Return Value</span></span>

<span data-ttu-id="563b3-113">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="563b3-113">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="563b3-114">Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="563b3-114">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="563b3-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="563b3-115">Return value</span></span>|<span data-ttu-id="563b3-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="563b3-116">Description</span></span>|
|-|-|
|<span data-ttu-id="563b3-117">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="563b3-117">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="563b3-118">*PROPID* ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="563b3-118">*propId* is unknown.</span></span>|
|<span data-ttu-id="563b3-119">DO_E_WRITE_ONLY_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="563b3-119">DO_E_WRITE_ONLY_PROPERTY</span></span>|<span data-ttu-id="563b3-120">Die-Eigenschaft ist schreibgeschützt und kann nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="563b3-120">The property is write-only, and cannot be read.</span></span>|
|<span data-ttu-id="563b3-121">E_NOT_SET</span><span class="sxs-lookup"><span data-stu-id="563b3-121">E_NOT_SET</span></span>|<span data-ttu-id="563b3-122">Es wurde keine solche Eigenschaft über **setpropertyex** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="563b3-122">No such property was set via **SetPropertyEx**.</span></span>|

## <a name="requirements"></a><span data-ttu-id="563b3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="563b3-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="563b3-124">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="563b3-124">**Minimum supported client**</span></span> | <span data-ttu-id="563b3-125">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="563b3-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="563b3-126">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="563b3-126">**Minimum supported server**</span></span> | <span data-ttu-id="563b3-127">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="563b3-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="563b3-128">**Header**</span><span class="sxs-lookup"><span data-stu-id="563b3-128">**Header**</span></span> | <span data-ttu-id="563b3-129">Dodownloadinternal. h</span><span class="sxs-lookup"><span data-stu-id="563b3-129">DODownloadInternal.h</span></span> |