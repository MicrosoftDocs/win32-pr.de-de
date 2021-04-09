---
title: Idodownloadinternal-Schnittstelle
description: Wird verwendet, um Erweiterte Download Eigenschaften zu erhalten oder festzulegen.
keywords:
- Idodownloadinternal-Schnittstelle
topic_type:
- apiref
api_name:
- IDODownloadInternal
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 89dcf0e397e9761c1b156a4ad4b245209cf50020
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102015"
---
# <a name="idodownloadinternal-interface"></a><span data-ttu-id="dc86a-104">Idodownloadinternal-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="dc86a-104">IDODownloadInternal interface</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dc86a-105">Die **idodownloadinternal** -Schnittstelle ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="dc86a-105">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="dc86a-106">Verwenden Sie stattdessen die [idodownload](../do/nn-do-idodownload.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dc86a-106">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="dc86a-107">Die **idodownloadinternal** -Schnittstelle wird verwendet, um Erweiterte Download Eigenschaften zu erhalten oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="dc86a-107">The **IDODownloadInternal** interface is used to get or set extended download properties.</span></span>

## <a name="methods"></a><span data-ttu-id="dc86a-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="dc86a-108">Methods</span></span>

<span data-ttu-id="dc86a-109">Die **idodownloadinternal** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="dc86a-109">The **IDODownloadInternal** interface has these methods.</span></span>

| <span data-ttu-id="dc86a-110">Methode</span><span class="sxs-lookup"><span data-stu-id="dc86a-110">Method</span></span> | <span data-ttu-id="dc86a-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc86a-111">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="dc86a-112">Idodownloadinternal:: getpropertyex</span><span class="sxs-lookup"><span data-stu-id="dc86a-112">IDODownloadInternal::GetPropertyEx</span></span>](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | <span data-ttu-id="dc86a-113">Ruft einen Zeiger auf einen **Variant** -Wert ab, der einen bestimmten erweiterten Download-Eigenschafts Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="dc86a-113">Retrieves a pointer to a **VARIANT** that contains a specific extended download property value.</span></span> |
| [<span data-ttu-id="dc86a-114">Idodownloadinternal:: setpropertyex</span><span class="sxs-lookup"><span data-stu-id="dc86a-114">IDODownloadInternal::SetPropertyEx</span></span>](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | <span data-ttu-id="dc86a-115">Legt eine erweiterte Download Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="dc86a-115">Sets an extended download property.</span></span> <span data-ttu-id="dc86a-116">Die-Methode akzeptiert einen Zeiger auf eine **Variante** , die einen bestimmten Eigenschafts Wert enthält, der auf den Download angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc86a-116">The method accepts a pointer to a **VARIANT** that contains a specific property value to apply to the download.</span></span> |

## <a name="requirements"></a><span data-ttu-id="dc86a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc86a-117">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="dc86a-118">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="dc86a-118">**Minimum supported client**</span></span> | <span data-ttu-id="dc86a-119">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="dc86a-119">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="dc86a-120">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="dc86a-120">**Minimum supported server**</span></span> | <span data-ttu-id="dc86a-121">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="dc86a-121">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="dc86a-122">**Header**</span><span class="sxs-lookup"><span data-stu-id="dc86a-122">**Header**</span></span> | <span data-ttu-id="dc86a-123">Dodownloadinternal. h</span><span class="sxs-lookup"><span data-stu-id="dc86a-123">DODownloadInternal.h</span></span> |