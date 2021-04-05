---
title: 'Idodownload:: SetProperty-Methode'
description: Legt eine Download Eigenschaft fest.
keywords:
- 'Idodownload:: SetProperty-Methode'
topic_type:
- apiref
api_name:
- IDODownload.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d496f49851aab665e49f3aaeb51e4b941d6c183
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "103719565"
---
# <a name="idodownloadsetproperty-method"></a><span data-ttu-id="69f31-104">Idodownload:: SetProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="69f31-104">IDODownload::SetProperty method</span></span>

<span data-ttu-id="69f31-105">Legt eine Download Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="69f31-105">Sets a download property.</span></span> <span data-ttu-id="69f31-106">Die-Methode akzeptiert einen Zeiger auf eine **Variante** , die eine bestimmte Eigenschaft enthält, die auf den Download angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="69f31-106">The method accepts a pointer to a **VARIANT** that contains a specific property to apply to the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f31-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="69f31-107">Syntax</span></span>

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="69f31-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="69f31-108">Parameters</span></span>

`propId`

<span data-ttu-id="69f31-109">Die erforderliche eigen schafts-ID, die festgelegt werden soll (vom Typ **dodownloadproperty**).</span><span class="sxs-lookup"><span data-stu-id="69f31-109">The required property ID to set (of type **DODownloadProperty**).</span></span>

`propVal`

<span data-ttu-id="69f31-110">Der festzulegende Eigenschafts Wert, der in einem **Variant** gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="69f31-110">The property value to set, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="69f31-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69f31-111">Return Value</span></span>

<span data-ttu-id="69f31-112">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="69f31-112">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="69f31-113">Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="69f31-113">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="69f31-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69f31-114">Return value</span></span>|<span data-ttu-id="69f31-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69f31-115">Description</span></span>|
|-|-|
|<span data-ttu-id="69f31-116">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="69f31-116">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="69f31-117">*PROPID* ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="69f31-117">*propId* is unknown.</span></span>|
|<span data-ttu-id="69f31-118">DO_E_INVALID_STATE</span><span class="sxs-lookup"><span data-stu-id="69f31-118">DO_E_INVALID_STATE</span></span>|<span data-ttu-id="69f31-119">Der Download befindet sich derzeit nicht in einem Zustand, der das Festlegen von Eigenschaften zulässt.</span><span class="sxs-lookup"><span data-stu-id="69f31-119">The download is not currently in a state that allows setting properties.</span></span>|

## <a name="requirements"></a><span data-ttu-id="69f31-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69f31-120">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="69f31-121">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="69f31-121">**Minimum supported client**</span></span> | <span data-ttu-id="69f31-122">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="69f31-122">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="69f31-123">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="69f31-123">**Minimum supported server**</span></span> | <span data-ttu-id="69f31-124">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="69f31-124">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="69f31-125">**Header**</span><span class="sxs-lookup"><span data-stu-id="69f31-125">**Header**</span></span> | <span data-ttu-id="69f31-126">Do. h</span><span class="sxs-lookup"><span data-stu-id="69f31-126">Do.h</span></span> |
