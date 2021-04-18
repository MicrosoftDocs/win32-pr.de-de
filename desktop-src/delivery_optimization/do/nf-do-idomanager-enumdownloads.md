---
title: 'Idomanager:: enumdownloads-Methode'
description: Ruft einen Schnittstellen Zeiger auf ein Enumeratorobjekt ab, das verwendet wird, um vorhandene Downloads aufzulisten.
keywords:
- 'Idomanager:: enumdownloads-Methode'
topic_type:
- apiref
api_name:
- IDOManager.EnumDownloads
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a1e7fed2955fdc1b5ac0c11cfebc34aa95517603
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106338037"
---
# <a name="idomanagerenumdownloads-method"></a><span data-ttu-id="c2016-104">Idomanager:: enumdownloads-Methode</span><span class="sxs-lookup"><span data-stu-id="c2016-104">IDOManager::EnumDownloads method</span></span>

<span data-ttu-id="c2016-105">Ruft einen Schnittstellen Zeiger auf ein Enumeratorobjekt ab, das verwendet wird, um vorhandene Downloads aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="c2016-105">Retrieves an interface pointer to an enumerator object that is used to enumerate existing downloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2016-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2016-106">Syntax</span></span>

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a><span data-ttu-id="c2016-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2016-107">Parameters</span></span>

`category`

<span data-ttu-id="c2016-108">Optional.</span><span class="sxs-lookup"><span data-stu-id="c2016-108">Optional.</span></span> <span data-ttu-id="c2016-109">Der Eigenschaftsname, der als Kategorie für die Aufzählung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2016-109">The property name to be used as a category to enumerate.</span></span> <span data-ttu-id="c2016-110">Durch die Übergabe `nullptr` werden alle vorhandenen Downloads abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c2016-110">Passing `nullptr` will retrieve all existing downloads.</span></span> <span data-ttu-id="c2016-111">Die folgenden Eigenschaften werden als Kategorie unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2016-111">The following properties are supported as a category.</span></span>

- <span data-ttu-id="c2016-112">**DODownloadProperty_Id**</span><span class="sxs-lookup"><span data-stu-id="c2016-112">**DODownloadProperty_Id**</span></span>
- <span data-ttu-id="c2016-113">**DODownloadProperty_Uri**</span><span class="sxs-lookup"><span data-stu-id="c2016-113">**DODownloadProperty_Uri**</span></span>
- <span data-ttu-id="c2016-114">**DODownloadProperty_ContentId**</span><span class="sxs-lookup"><span data-stu-id="c2016-114">**DODownloadProperty_ContentId**</span></span>
- <span data-ttu-id="c2016-115">**DODownloadProperty_DisplayName**</span><span class="sxs-lookup"><span data-stu-id="c2016-115">**DODownloadProperty_DisplayName**</span></span>
- <span data-ttu-id="c2016-116">**DODownloadProperty_LocalPath**</span><span class="sxs-lookup"><span data-stu-id="c2016-116">**DODownloadProperty_LocalPath**</span></span>

`ppEnum`

<span data-ttu-id="c2016-117">Die Adresse eines Schnittstellen Zeigers auf **IEnumUnknown**, der zum Aufzählen vorhandener Downloads verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2016-117">The address of an interface pointer to **IEnumUnknown**, which is used to enumerate existing downloads.</span></span> <span data-ttu-id="c2016-118">Der Inhalt des Enumerators hängt vom Wert der *Kategorie* ab.</span><span class="sxs-lookup"><span data-stu-id="c2016-118">The contents of the enumerator depend on the value of *category*.</span></span> <span data-ttu-id="c2016-119">Die Downloads, die in der Enumerationsschnittstelle enthalten sind, sind diejenigen, die zuvor vom gleichen Aufrufer dieser Funktion erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="c2016-119">The downloads included in the enumeration interface are the ones that were previously created by the same caller to this function.</span></span> 

## <a name="return-value"></a><span data-ttu-id="c2016-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2016-120">Return Value</span></span>

<span data-ttu-id="c2016-121">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c2016-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="c2016-122">Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c2016-122">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2016-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2016-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c2016-124">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="c2016-124">**Minimum supported client**</span></span> | <span data-ttu-id="c2016-125">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="c2016-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="c2016-126">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="c2016-126">**Minimum supported server**</span></span> | <span data-ttu-id="c2016-127">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="c2016-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="c2016-128">**Header**</span><span class="sxs-lookup"><span data-stu-id="c2016-128">**Header**</span></span> | <span data-ttu-id="c2016-129">Do. h</span><span class="sxs-lookup"><span data-stu-id="c2016-129">Do.h</span></span> |
