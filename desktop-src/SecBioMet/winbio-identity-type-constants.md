---
title: WINBIO_IDENTITY_TYPE Konstanten (winbio \_ types. h)
description: Geben Sie das Format der Identitätsinformationen an, die in der winbio- \_ Identitäts Struktur enthalten sind.
ms.assetid: 27A01538-9B26-4A29-8ADB-ED9C5D5808B3
topic_type:
- apiref
api_name:
- WINBIO_ID_TYPE_NULL
- WINBIO_ID_TYPE_WILDCARD
- WINBIO_ID_TYPE_GUID
- WINBIO_ID_TYPE_SID
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dad068c6838f0a3a675970b7c9359b12ea8faa2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949651"
---
# <a name="winbio_identity_type-constants"></a><span data-ttu-id="1b1fa-103">Winbio \_ - \_ Identitätstyp Konstanten</span><span class="sxs-lookup"><span data-stu-id="1b1fa-103">WINBIO\_IDENTITY\_TYPE Constants</span></span>

<span data-ttu-id="1b1fa-104">Die folgenden **winbio \_ - \_ Identitätstyp** Konstanten können verwendet werden, um das Format der Identitätsinformationen anzugeben, die in der [**winbio- \_ Identitäts**](winbio-identity.md) Struktur enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1b1fa-104">The following **WINBIO\_IDENTITY\_TYPE** constants can be used to specify the format of the identity information contained in the [**WINBIO\_IDENTITY**](winbio-identity.md) structure.</span></span>



| <span data-ttu-id="1b1fa-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="1b1fa-105">Constant</span></span>                                                                                                                                                                                      | <span data-ttu-id="1b1fa-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b1fa-106">Description</span></span>                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <span data-ttu-id="1b1fa-107"><dt>**winbio- \_ ID- \_ Typ \_ null**</dt></span><span class="sxs-lookup"><span data-stu-id="1b1fa-107"><dt>**WINBIO\_ID\_TYPE\_NULL**</dt></span></span> </dl>             | <span data-ttu-id="1b1fa-108">Der Vorlage ist keine ID zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1b1fa-108">The template has no associated ID.</span></span> <br/>            |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <span data-ttu-id="1b1fa-109"><dt>**winbio- \_ ID- \_ Typ Platzhalter \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b1fa-109"><dt>**WINBIO\_ID\_TYPE\_WILDCARD**</dt></span></span> </dl> | <span data-ttu-id="1b1fa-110">Die Struktur entspricht allen Vorlagen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="1b1fa-110">The structure matches all template identities.</span></span><br/> |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <span data-ttu-id="1b1fa-111"><dt>**winbio- \_ ID- \_ \_ GUID-Typ**</dt></span><span class="sxs-lookup"><span data-stu-id="1b1fa-111"><dt>**WINBIO\_ID\_TYPE\_GUID**</dt></span></span> </dl>             | <span data-ttu-id="1b1fa-112">Die Vorlage wird durch eine GUID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1b1fa-112">A GUID identifies the template.</span></span><br/>                |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <span data-ttu-id="1b1fa-113"><dt>**winbio- \_ ID- \_ Typ- \_ sid**</dt></span><span class="sxs-lookup"><span data-stu-id="1b1fa-113"><dt>**WINBIO\_ID\_TYPE\_SID**</dt></span></span> </dl>                | <span data-ttu-id="1b1fa-114">Eine Konto-SID identifiziert die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="1b1fa-114">An account SID identifies the template.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="1b1fa-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b1fa-115">Requirements</span></span>



| <span data-ttu-id="1b1fa-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b1fa-116">Requirement</span></span> | <span data-ttu-id="1b1fa-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1b1fa-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b1fa-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b1fa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1b1fa-119">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b1fa-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="1b1fa-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b1fa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1b1fa-121">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b1fa-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1b1fa-122">Header</span><span class="sxs-lookup"><span data-stu-id="1b1fa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b1fa-123"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b1fa-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b1fa-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b1fa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b1fa-125">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="1b1fa-125">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="1b1fa-126">**winbio- \_ Identität**</span><span class="sxs-lookup"><span data-stu-id="1b1fa-126">**WINBIO\_IDENTITY**</span></span>](winbio-identity.md)
</dt> </dl>

 

 





