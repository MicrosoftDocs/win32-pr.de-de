---
description: Die "CAPICOM \_ Key \_ Storage Flag"- \_ Enumeration definiert Schlüsselspeicherflags.
ms.assetid: 326cef75-24a5-4dc9-a7e9-a63dd3d8de54
title: CAPICOM_KEY_STORAGE_FLAG-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_STORAGE_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 9edbc3a5ac3396e528ebbb5390c4b07c24770e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373745"
---
# <a name="capicom_key_storage_flag-enumeration"></a><span data-ttu-id="60e7c-103">CAPICOM \_ - \_ schlüsselspeicherungsflag- \_ Enumeration</span><span class="sxs-lookup"><span data-stu-id="60e7c-103">CAPICOM\_KEY\_STORAGE\_FLAG enumeration</span></span>

<span data-ttu-id="60e7c-104">Die " **CAPICOM \_ Key \_ Storage \_ Flag** "-Enumeration definiert Schlüsselspeicherflags.</span><span class="sxs-lookup"><span data-stu-id="60e7c-104">The **CAPICOM\_KEY\_STORAGE\_FLAG** enumeration defines key storage flags.</span></span>

## <a name="members"></a><span data-ttu-id="60e7c-105">Member</span><span class="sxs-lookup"><span data-stu-id="60e7c-105">Members</span></span>



| <span data-ttu-id="60e7c-106">Member</span><span class="sxs-lookup"><span data-stu-id="60e7c-106">Member</span></span>                                     | <span data-ttu-id="60e7c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60e7c-107">Description</span></span>                           | <span data-ttu-id="60e7c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="60e7c-108">Value</span></span> |
|--------------------------------------------|---------------------------------------|-------|
| <span data-ttu-id="60e7c-109">**Standardwert für CAPICOM- \_ Schlüssel \_ Speicher \_**</span><span class="sxs-lookup"><span data-stu-id="60e7c-109">**CAPICOM\_KEY\_STORAGE\_DEFAULT**</span></span>         | <span data-ttu-id="60e7c-110">Standardschlüssel Speicher.</span><span class="sxs-lookup"><span data-stu-id="60e7c-110">Default key storage.</span></span><br/>       | <span data-ttu-id="60e7c-111">0</span><span class="sxs-lookup"><span data-stu-id="60e7c-111">0</span></span>     |
| <span data-ttu-id="60e7c-112">**zu \_ \_ \_ exportier barer CAPICOM-Schlüsselspeicher**</span><span class="sxs-lookup"><span data-stu-id="60e7c-112">**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</span></span>      | <span data-ttu-id="60e7c-113">Der Schlüssel ist exportierbar.</span><span class="sxs-lookup"><span data-stu-id="60e7c-113">The key is exportable.</span></span><br/>     | <span data-ttu-id="60e7c-114">1</span><span class="sxs-lookup"><span data-stu-id="60e7c-114">1</span></span>     |
| <span data-ttu-id="60e7c-115">**Benutzer geschützter CAPICOM- \_ Schlüssel \_ Speicher \_ \_**</span><span class="sxs-lookup"><span data-stu-id="60e7c-115">**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</span></span> | <span data-ttu-id="60e7c-116">Der Schlüssel ist Benutzer geschützt.</span><span class="sxs-lookup"><span data-stu-id="60e7c-116">The key is user protected.</span></span><br/> | <span data-ttu-id="60e7c-117">2</span><span class="sxs-lookup"><span data-stu-id="60e7c-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="60e7c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60e7c-118">Remarks</span></span>

<span data-ttu-id="60e7c-119">Diese Enumeration wird von der folgenden Methode verwendet:</span><span class="sxs-lookup"><span data-stu-id="60e7c-119">This enumeration is used by the following method:</span></span>

-   [<span data-ttu-id="60e7c-120">**Zertifikat. Laden**</span><span class="sxs-lookup"><span data-stu-id="60e7c-120">**Certificate.Load**</span></span>](certificate-load.md)
-   [<span data-ttu-id="60e7c-121">**Store. Load**</span><span class="sxs-lookup"><span data-stu-id="60e7c-121">**Store.Load**</span></span>](store-load.md)

## <a name="requirements"></a><span data-ttu-id="60e7c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60e7c-122">Requirements</span></span>



| <span data-ttu-id="60e7c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60e7c-123">Requirement</span></span> | <span data-ttu-id="60e7c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="60e7c-124">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="60e7c-125">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="60e7c-125">Redistributable</span></span><br/> | <span data-ttu-id="60e7c-126">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="60e7c-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="60e7c-127">Header</span><span class="sxs-lookup"><span data-stu-id="60e7c-127">Header</span></span><br/>          | <dl> <span data-ttu-id="60e7c-128"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="60e7c-128"><dt>Capicom.h</dt></span></span> </dl> |



 

 




