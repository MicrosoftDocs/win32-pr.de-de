---
title: Idomanager-Schnittstelle
description: Wird verwendet, um einen neuen Download zu erstellen und vorhandene Downloads aufzulisten.
keywords:
- Idomanager-Schnittstelle
topic_type:
- apiref
api_name:
- IDOManager
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a8755615e4d2f0fd074117438f8f305dce0cb681
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342153"
---
# <a name="idomanager-interface"></a><span data-ttu-id="16c75-104">Idomanager-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="16c75-104">IDOManager interface</span></span>

<span data-ttu-id="16c75-105">Die **idomanager** -Schnittstelle wird verwendet, um einen neuen Download zu erstellen und vorhandene Downloads aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="16c75-105">The **IDOManager** interface is used to create a new download, and to enumerate existing downloads.</span></span>

## <a name="methods"></a><span data-ttu-id="16c75-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="16c75-106">Methods</span></span>

<span data-ttu-id="16c75-107">Die **idomanager** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="16c75-107">The **IDOManager** interface has these methods.</span></span>

| <span data-ttu-id="16c75-108">Methode</span><span class="sxs-lookup"><span data-stu-id="16c75-108">Method</span></span> | <span data-ttu-id="16c75-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16c75-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="16c75-110">Idomanager:: kreatedownload</span><span class="sxs-lookup"><span data-stu-id="16c75-110">IDOManager::CreateDownload</span></span>](./nf-do-idomanager-createdownload.md) | <span data-ttu-id="16c75-111">Erstellt einen neuen Download.</span><span class="sxs-lookup"><span data-stu-id="16c75-111">Creates a new download.</span></span> |
| [<span data-ttu-id="16c75-112">Idomanager:: enumdownloads</span><span class="sxs-lookup"><span data-stu-id="16c75-112">IDOManager::EnumDownloads</span></span>](./nf-do-idomanager-enumdownloads.md) | <span data-ttu-id="16c75-113">Ruft einen Schnittstellen Zeiger auf ein Enumeratorobjekt ab, das verwendet wird, um vorhandene Downloads aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="16c75-113">Retrieves an interface pointer to an enumerator object that is used to enumerate existing downloads.</span></span> |

## <a name="requirements"></a><span data-ttu-id="16c75-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16c75-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="16c75-115">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="16c75-115">**Minimum supported client**</span></span> | <span data-ttu-id="16c75-116">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="16c75-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="16c75-117">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="16c75-117">**Minimum supported server**</span></span> | <span data-ttu-id="16c75-118">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="16c75-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="16c75-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="16c75-119">**Header**</span></span> | <span data-ttu-id="16c75-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="16c75-120">Do.h</span></span> |