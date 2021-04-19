---
title: DO_DOWNLOAD_ENUM_CATEGORY Struktur
description: 'Wird von **idomanager:: enumdownloads** verwendet, um die Downloads-Enumeration nach dem Wert der bestimmten Eigenschaft zu filtern.'
keywords:
- DO_DOWNLOAD_ENUM_CATEGORY Struktur
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_ENUM_CATEGORY
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a78c94cd9d8854453517976300e12a031f65b8cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106342105"
---
# <a name="do_download_enum_category-structure"></a><span data-ttu-id="812aa-104">DO_DOWNLOAD_ENUM_CATEGORY Struktur</span><span class="sxs-lookup"><span data-stu-id="812aa-104">DO_DOWNLOAD_ENUM_CATEGORY structure</span></span>

<span data-ttu-id="812aa-105">Die **DO_DOWNLOAD_ENUM_CATEGORY** Struktur wird von **idomanager:: enumdownloads** verwendet, um die Downloads-Enumeration nach dem Wert der bestimmten Eigenschaft zu filtern.</span><span class="sxs-lookup"><span data-stu-id="812aa-105">The **DO_DOWNLOAD_ENUM_CATEGORY** structure is used by **IDOManager::EnumDownloads** to filter the downloads enumeration by the specific property's value.</span></span>

## <a name="syntax"></a><span data-ttu-id="812aa-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="812aa-106">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_ENUM_CATEGORY
{
  DODownloadProperty Property;
  LPCWSTR Value;
} DO_DOWNLOAD_ENUM_CATEGORY;
```

## <a name="members"></a><span data-ttu-id="812aa-107">Member</span><span class="sxs-lookup"><span data-stu-id="812aa-107">Members</span></span>

`Property`

<span data-ttu-id="812aa-108">Der Eigenschaftsname, der für die Download-Enumeration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="812aa-108">The property name to be used for the download enumeration.</span></span> <span data-ttu-id="812aa-109">Diese Eigenschaften werden für Enumerationszwecke unterstützt.</span><span class="sxs-lookup"><span data-stu-id="812aa-109">These properties are supported for enumeration purposes.</span></span>
- <span data-ttu-id="812aa-110">**DODownloadProperty_Id**</span><span class="sxs-lookup"><span data-stu-id="812aa-110">**DODownloadProperty_Id**</span></span>
- <span data-ttu-id="812aa-111">**DODownloadProperty_Uri**</span><span class="sxs-lookup"><span data-stu-id="812aa-111">**DODownloadProperty_Uri**</span></span>
- <span data-ttu-id="812aa-112">**DODownloadProperty_ContentId**</span><span class="sxs-lookup"><span data-stu-id="812aa-112">**DODownloadProperty_ContentId**</span></span>
- <span data-ttu-id="812aa-113">**DODownloadProperty_DisplayName**</span><span class="sxs-lookup"><span data-stu-id="812aa-113">**DODownloadProperty_DisplayName**</span></span>
- <span data-ttu-id="812aa-114">**DODownloadProperty_LocalPath**</span><span class="sxs-lookup"><span data-stu-id="812aa-114">**DODownloadProperty_LocalPath**</span></span>

`Value`

<span data-ttu-id="812aa-115">Der Wert der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="812aa-115">The property's value.</span></span>

## <a name="requirements"></a><span data-ttu-id="812aa-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="812aa-116">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="812aa-117">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="812aa-117">**Minimum supported client**</span></span> | <span data-ttu-id="812aa-118">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="812aa-118">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="812aa-119">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="812aa-119">**Minimum supported server**</span></span> | <span data-ttu-id="812aa-120">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="812aa-120">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="812aa-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="812aa-121">**Header**</span></span> | <span data-ttu-id="812aa-122">Do. h</span><span class="sxs-lookup"><span data-stu-id="812aa-122">Do.h</span></span> |
