---
title: 'Idodownloadinternal:: setpropertyex-Methode'
description: Legt eine erweiterte Download Eigenschaft fest. Die-Methode akzeptiert einen Zeiger auf eine **Variante** , die einen bestimmten Eigenschafts Wert enthält, der auf den Download angewendet werden soll.
keywords:
- 'Idodownloadinternal:: setpropertyex-Methode'
topic_type:
- apiref
api_name:
- IDODownloadInternal.SetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: e6630cc3e767531dd94da39fe73d88284c9ca0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948790"
---
# <a name="idodownloadinternalsetpropertyex-method"></a><span data-ttu-id="24d89-105">Idodownloadinternal:: setpropertyex-Methode</span><span class="sxs-lookup"><span data-stu-id="24d89-105">IDODownloadInternal::SetPropertyEx method</span></span>

> [!IMPORTANT]
> <span data-ttu-id="24d89-106">Die **idodownloadinternal** -Schnittstelle ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="24d89-106">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="24d89-107">Verwenden Sie stattdessen die [idodownload](../do/nn-do-idodownload.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="24d89-107">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="24d89-108">Legt eine erweiterte Download Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="24d89-108">Sets an extended download property.</span></span> <span data-ttu-id="24d89-109">Die-Methode akzeptiert einen Zeiger auf eine **Variante** , die einen bestimmten Eigenschafts Wert enthält, der auf den Download angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="24d89-109">The method accepts a pointer to a **VARIANT** that contains a specific property value to apply to the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="24d89-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="24d89-110">Syntax</span></span>

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="24d89-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="24d89-111">Parameters</span></span>

`propId`

<span data-ttu-id="24d89-112">Die erforderliche eigen schafts-ID, die festgelegt werden soll (vom Typ **dodownloadpropertyex**).</span><span class="sxs-lookup"><span data-stu-id="24d89-112">The required property ID to set (of type **DODownloadPropertyEx**).</span></span>

`propVal`

<span data-ttu-id="24d89-113">Der festzulegende Eigenschafts Wert, der in einem **Variant** gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="24d89-113">The property value to set, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="24d89-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24d89-114">Return Value</span></span>

<span data-ttu-id="24d89-115">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="24d89-115">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="24d89-116">Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="24d89-116">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="24d89-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24d89-117">Return value</span></span>|<span data-ttu-id="24d89-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24d89-118">Description</span></span>|
|-|-|
|<span data-ttu-id="24d89-119">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="24d89-119">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="24d89-120">*PROPID* ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="24d89-120">*propId* is unknown.</span></span>|
|<span data-ttu-id="24d89-121">DO_E_INVALID_STATE</span><span class="sxs-lookup"><span data-stu-id="24d89-121">DO_E_INVALID_STATE</span></span>|<span data-ttu-id="24d89-122">Der Download befindet sich derzeit nicht in einem Zustand, der das Festlegen von Eigenschaften zulässt.</span><span class="sxs-lookup"><span data-stu-id="24d89-122">The download is not currently in a state that allows setting properties.</span></span>|

## <a name="requirements"></a><span data-ttu-id="24d89-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24d89-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="24d89-124">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="24d89-124">**Minimum supported client**</span></span> | <span data-ttu-id="24d89-125">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="24d89-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="24d89-126">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="24d89-126">**Minimum supported server**</span></span> | <span data-ttu-id="24d89-127">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="24d89-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="24d89-128">**Header**</span><span class="sxs-lookup"><span data-stu-id="24d89-128">**Header**</span></span> | <span data-ttu-id="24d89-129">Dodownloadinternal. h</span><span class="sxs-lookup"><span data-stu-id="24d89-129">DODownloadInternal.h</span></span> |