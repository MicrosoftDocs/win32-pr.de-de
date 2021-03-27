---
description: Definiert eine Methode, die bestimmt, ob die Shell einen Ordner im Synchronisierungs Stamm eines cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.
title: IStorageProviderCopyHook-Schnittstelle
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: 52f2a7fb7c8d7b37fc27fd1e91c93d716bc92086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391784"
---
# <a name="istorageprovidercopyhook-interface"></a><span data-ttu-id="37004-103">IStorageProviderCopyHook-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="37004-103">IStorageProviderCopyHook interface</span></span>

<span data-ttu-id="37004-104">Macht eine Methode verfügbar, die bestimmt, ob die Shell einen Ordner im Synchronisierungs Stamm eines cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.</span><span class="sxs-lookup"><span data-stu-id="37004-104">Exposes a method that determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>

## <a name="members"></a><span data-ttu-id="37004-105">Member</span><span class="sxs-lookup"><span data-stu-id="37004-105">Members</span></span>

<span data-ttu-id="37004-106">Die **istorageprovidercopyhook** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="37004-106">The **IStorageProviderCopyHook** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="37004-107">**Istorageprovidercopyhook** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="37004-107">**IStorageProviderCopyHook** also has these types of members:</span></span>

- [<span data-ttu-id="37004-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="37004-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="37004-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="37004-109">Methods</span></span>

<span data-ttu-id="37004-110">Die **istorageprovidercopyhook** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="37004-110">The **IStorageProviderCopyHook** interface has these methods.</span></span>



| <span data-ttu-id="37004-111">Methode</span><span class="sxs-lookup"><span data-stu-id="37004-111">Method</span></span>                                           | <span data-ttu-id="37004-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37004-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37004-113">**Copycallback**</span><span class="sxs-lookup"><span data-stu-id="37004-113">**CopyCallback**</span></span>](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  <span data-ttu-id="37004-114">Bestimmt, ob die Shell einen Ordner im Synchronisierungs Stamm eines cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.</span><span class="sxs-lookup"><span data-stu-id="37004-114">Determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>                                                           |


## <a name="requirements"></a><span data-ttu-id="37004-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="37004-115">Requirements</span></span>

| <span data-ttu-id="37004-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37004-116">Requirement</span></span> | <span data-ttu-id="37004-117">Wert</span><span class="sxs-lookup"><span data-stu-id="37004-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37004-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37004-118">Minimum supported client</span></span> | <span data-ttu-id="37004-119">Windows 10 Insider Preview-Build 19624</span><span class="sxs-lookup"><span data-stu-id="37004-119">Windows 10 Insider Preview Build 19624</span></span>                                                |
| <span data-ttu-id="37004-120">Header</span><span class="sxs-lookup"><span data-stu-id="37004-120">Header</span></span><br/>                   | <span data-ttu-id="37004-121">shobjidl. h</span><span class="sxs-lookup"><span data-stu-id="37004-121">shobjidl.h</span></span>   |
