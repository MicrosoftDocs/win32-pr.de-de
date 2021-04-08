---
title: 'Idodownload:: GetProperty-Methode'
description: Ruft einen Zeiger auf eine **Variante** ab, die eine bestimmte Download Eigenschaft enthält.
keywords:
- 'Idodownload:: GetProperty-Methode'
topic_type:
- apiref
api_name:
- IDODownload.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e734f109e596663ee699c764ca85f1ee45ad7947
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "103857847"
---
# <a name="idodownloadgetproperty-method"></a><span data-ttu-id="18d2c-104">Idodownload:: GetProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="18d2c-104">IDODownload::GetProperty method</span></span>

<span data-ttu-id="18d2c-105">Ruft einen Zeiger auf eine **Variante** ab, die eine bestimmte Download Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="18d2c-105">Retrieves a pointer to a **VARIANT** that contains a specific download property.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d2c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="18d2c-106">Syntax</span></span>

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="18d2c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="18d2c-107">Parameters</span></span>

`propId`

<span data-ttu-id="18d2c-108">Die erforderliche Eigenschaften-ID, die (vom Typ " **dodownloadproperty**") erhalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="18d2c-108">The required property ID to get (of type **DODownloadProperty**).</span></span>

`propVal`

<span data-ttu-id="18d2c-109">Der resultierende Eigenschafts Wert, der in einem **Variant**-Objekt gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="18d2c-109">The resulting property value, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="18d2c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18d2c-110">Return Value</span></span>

<span data-ttu-id="18d2c-111">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18d2c-111">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="18d2c-112">Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18d2c-112">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="18d2c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18d2c-113">Return value</span></span>|<span data-ttu-id="18d2c-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18d2c-114">Description</span></span>|
|-|-|
|<span data-ttu-id="18d2c-115">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="18d2c-115">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="18d2c-116">*PROPID* ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="18d2c-116">*propId* is unknown.</span></span>|
|<span data-ttu-id="18d2c-117">DO_E_WRITE_ONLY_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="18d2c-117">DO_E_WRITE_ONLY_PROPERTY</span></span>|<span data-ttu-id="18d2c-118">Die-Eigenschaft ist schreibgeschützt und kann nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="18d2c-118">The property is write-only, and cannot be read.</span></span>|
|<span data-ttu-id="18d2c-119">E_NOT_SET</span><span class="sxs-lookup"><span data-stu-id="18d2c-119">E_NOT_SET</span></span>|<span data-ttu-id="18d2c-120">Es wurde keine solche Eigenschaft über " **SetProperty**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="18d2c-120">No such property was set via **SetProperty**.</span></span>|

## <a name="requirements"></a><span data-ttu-id="18d2c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18d2c-121">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="18d2c-122">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="18d2c-122">**Minimum supported client**</span></span> | <span data-ttu-id="18d2c-123">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="18d2c-123">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="18d2c-124">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="18d2c-124">**Minimum supported server**</span></span> | <span data-ttu-id="18d2c-125">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="18d2c-125">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="18d2c-126">**Header**</span><span class="sxs-lookup"><span data-stu-id="18d2c-126">**Header**</span></span> | <span data-ttu-id="18d2c-127">Do. h</span><span class="sxs-lookup"><span data-stu-id="18d2c-127">Do.h</span></span> |
