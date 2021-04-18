---
description: Gibt an, was überprüft wird, wenn eine digitale Signatur überprüft wird.
ms.assetid: e6259c3f-caed-42f4-832c-250365caa0d7
title: CAPICOM_SIGNED_DATA_VERIFY_FLAG-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_SIGNED_DATA_VERIFY_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bc8db48ee067e8d12bffa9dbff433384058013b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371461"
---
# <a name="capicom_signed_data_verify_flag-enumeration"></a><span data-ttu-id="3cc6f-103">Von CAPICOM \_ signierte Datenüberprüfung- \_ \_ Flag- \_ Enumeration</span><span class="sxs-lookup"><span data-stu-id="3cc6f-103">CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG enumeration</span></span>

<span data-ttu-id="3cc6f-104">Die in **CAPICOM \_ signierte \_ datenüberprüfungsflag \_ \_** -Enumeration gibt an, was überprüft wird, wenn eine [*digitale Signatur*](../secgloss/d-gly.md) überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="3cc6f-104">The **CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG** enumeration indicates what is checked when a [*digital signature*](../secgloss/d-gly.md) is verified.</span></span>

## <a name="members"></a><span data-ttu-id="3cc6f-105">Member</span><span class="sxs-lookup"><span data-stu-id="3cc6f-105">Members</span></span>



| <span data-ttu-id="3cc6f-106">Member</span><span class="sxs-lookup"><span data-stu-id="3cc6f-106">Member</span></span>                                           | <span data-ttu-id="3cc6f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3cc6f-107">Description</span></span>                                                                                                 | <span data-ttu-id="3cc6f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="3cc6f-108">Value</span></span> |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="3cc6f-109">**nur CAPICOM- \_ Signatur überprüfen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3cc6f-109">**CAPICOM\_VERIFY\_SIGNATURE\_ONLY**</span></span>             | <span data-ttu-id="3cc6f-110">Nur die Signatur wird geprüft.</span><span class="sxs-lookup"><span data-stu-id="3cc6f-110">Only the signature is checked.</span></span><br/>                                                                   | <span data-ttu-id="3cc6f-111">0</span><span class="sxs-lookup"><span data-stu-id="3cc6f-111">0</span></span>     |
| <span data-ttu-id="3cc6f-112">**CAPICOM \_ \_ -Signatur \_ und \_ Zertifikat überprüfen**</span><span class="sxs-lookup"><span data-stu-id="3cc6f-112">**CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE**</span></span> | <span data-ttu-id="3cc6f-113">Sowohl die Signatur als auch die Gültigkeit des Zertifikats, das zum Erstellen der Signatur verwendet wird, werden überprüft.</span><span class="sxs-lookup"><span data-stu-id="3cc6f-113">Both the signature and the validity of the certificate used to create the signature are checked.</span></span><br/> | <span data-ttu-id="3cc6f-114">1</span><span class="sxs-lookup"><span data-stu-id="3cc6f-114">1</span></span>     |



## <a name="requirements"></a><span data-ttu-id="3cc6f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cc6f-115">Requirements</span></span>



| <span data-ttu-id="3cc6f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3cc6f-116">Requirement</span></span> | <span data-ttu-id="3cc6f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3cc6f-117">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3cc6f-118">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="3cc6f-118">Redistributable</span></span><br/> | <span data-ttu-id="3cc6f-119">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="3cc6f-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="3cc6f-120">Header</span><span class="sxs-lookup"><span data-stu-id="3cc6f-120">Header</span></span><br/>          | <dl> <span data-ttu-id="3cc6f-121"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cc6f-121"><dt>Capicom.h</dt></span></span> </dl> |



 

 
