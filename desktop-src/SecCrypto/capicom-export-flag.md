---
description: Der \_ \_ Enumerationstyp CAPICOM-exportflag definiert, ob Export Fehler des privaten Schlüssels ignoriert werden.
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: CAPICOM_EXPORT_FLAG-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EXPORT_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: fe99b1123ae35083e5c59df37234821efd2db208
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369683"
---
# <a name="capicom_export_flag-enumeration"></a><span data-ttu-id="11888-103">CAPICOM \_ - \_ exportflag-Enumeration</span><span class="sxs-lookup"><span data-stu-id="11888-103">CAPICOM\_EXPORT\_FLAG enumeration</span></span>

<span data-ttu-id="11888-104">Der Enumerationstyp **CAPICOM- \_ \_ exportflag** definiert, ob Export Fehler des privaten Schlüssels ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="11888-104">The **CAPICOM\_EXPORT\_FLAG** enumeration type defines whether any private key export errors are ignored.</span></span>

## <a name="members"></a><span data-ttu-id="11888-105">Member</span><span class="sxs-lookup"><span data-stu-id="11888-105">Members</span></span>



| <span data-ttu-id="11888-106">Member</span><span class="sxs-lookup"><span data-stu-id="11888-106">Member</span></span>                                                            | <span data-ttu-id="11888-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11888-107">Description</span></span>                                               | <span data-ttu-id="11888-108">Wert</span><span class="sxs-lookup"><span data-stu-id="11888-108">Value</span></span> |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| <span data-ttu-id="11888-109">**Standardwert für CAPICOM- \_ Export \_**</span><span class="sxs-lookup"><span data-stu-id="11888-109">**CAPICOM\_EXPORT\_DEFAULT**</span></span>                                      | <span data-ttu-id="11888-110">Alle Export Fehler des privaten Schlüssels werden nicht ignoriert.</span><span class="sxs-lookup"><span data-stu-id="11888-110">Any private key export errors are not ignored.</span></span><br/> | <span data-ttu-id="11888-111">0</span><span class="sxs-lookup"><span data-stu-id="11888-111">0</span></span>     |
| <span data-ttu-id="11888-112">**CAPICOM \_ - \_ Export \_ \_ Fehler beim \_ nicht \_ exportierbaren privaten Schlüssel \_ ignorieren**</span><span class="sxs-lookup"><span data-stu-id="11888-112">**CAPICOM\_EXPORT\_IGNORE\_PRIVATE\_KEY\_NOT\_EXPORTABLE\_ERROR**</span></span> | <span data-ttu-id="11888-113">Alle Export Fehler des privaten Schlüssels werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="11888-113">Any private key export errors are ignored.</span></span><br/>     | <span data-ttu-id="11888-114">1</span><span class="sxs-lookup"><span data-stu-id="11888-114">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="11888-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11888-115">Remarks</span></span>

<span data-ttu-id="11888-116">Der \_ \_ Enumerationstyp CAPICOM-exportflag wird von der folgenden Methode verwendet:</span><span class="sxs-lookup"><span data-stu-id="11888-116">The CAPICOM\_EXPORT\_FLAG enumeration type is used by the following method:</span></span>

-   [<span data-ttu-id="11888-117">**Zertifikate. speichern**</span><span class="sxs-lookup"><span data-stu-id="11888-117">**Certificates.Save**</span></span>](certificates-save.md)

## <a name="requirements"></a><span data-ttu-id="11888-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11888-118">Requirements</span></span>



| <span data-ttu-id="11888-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11888-119">Requirement</span></span> | <span data-ttu-id="11888-120">Wert</span><span class="sxs-lookup"><span data-stu-id="11888-120">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="11888-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="11888-121">Redistributable</span></span><br/> | <span data-ttu-id="11888-122">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="11888-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="11888-123">Header</span><span class="sxs-lookup"><span data-stu-id="11888-123">Header</span></span><br/>          | <dl> <span data-ttu-id="11888-124"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="11888-124"><dt>Capicom.h</dt></span></span> </dl> |



 

 




