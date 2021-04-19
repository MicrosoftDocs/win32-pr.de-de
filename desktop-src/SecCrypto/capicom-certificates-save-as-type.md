---
description: Definiert das Format einer Datei mit Zertifikat Informationen.
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: CAPICOM_CERTIFICATES_SAVE_AS_TYPE-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATES_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 3cbde0e8a64fa931ce50d2277d33b5fd5c27ee68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354174"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a><span data-ttu-id="d4c53-103">CAPICOM- \_ Zertifikate \_ Save-As-Type- \_ \_ Enumeration</span><span class="sxs-lookup"><span data-stu-id="d4c53-103">CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE enumeration</span></span>

<span data-ttu-id="d4c53-104">Der-Enumerationstyp " **CAPICOM- \_ Zertifikate \_ Save \_ As \_** " definiert das Format einer Datei mit Zertifikat Informationen.</span><span class="sxs-lookup"><span data-stu-id="d4c53-104">The **CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE** enumeration type defines the format of a file containing certificates information.</span></span> <span data-ttu-id="d4c53-105">Dieser Enumerationstyp wurde von CAPICOM 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d4c53-105">This enumeration type was introduced by CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="d4c53-106">Member</span><span class="sxs-lookup"><span data-stu-id="d4c53-106">Members</span></span>



| <span data-ttu-id="d4c53-107">Member</span><span class="sxs-lookup"><span data-stu-id="d4c53-107">Member</span></span>                                          | <span data-ttu-id="d4c53-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4c53-108">Description</span></span>                                          | <span data-ttu-id="d4c53-109">Wert</span><span class="sxs-lookup"><span data-stu-id="d4c53-109">Value</span></span> |
|-------------------------------------------------|------------------------------------------------------|-------|
| <span data-ttu-id="d4c53-110">**CAPICOM- \_ Zertifikate werden \_ \_ als \_ serialisiert gespeichert.**</span><span class="sxs-lookup"><span data-stu-id="d4c53-110">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_SERIALIZED**</span></span> | <span data-ttu-id="d4c53-111">Die gespeicherten Zertifikate werden serialisiert.</span><span class="sxs-lookup"><span data-stu-id="d4c53-111">The saved certificates are serialized.</span></span><br/>    | <span data-ttu-id="d4c53-112">0</span><span class="sxs-lookup"><span data-stu-id="d4c53-112">0</span></span>     |
| <span data-ttu-id="d4c53-113">**CAPICOM- \_ Zertifikate \_ speichern \_ als \_ PKCS7**</span><span class="sxs-lookup"><span data-stu-id="d4c53-113">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PKCS7**</span></span>      | <span data-ttu-id="d4c53-114">Die Zertifikate werden als PKCS 7 gespeichert \# .</span><span class="sxs-lookup"><span data-stu-id="d4c53-114">The certificates are saved as a PKCS \#7.</span></span><br/> | <span data-ttu-id="d4c53-115">1</span><span class="sxs-lookup"><span data-stu-id="d4c53-115">1</span></span>     |
| <span data-ttu-id="d4c53-116">**CAPICOM \_ - \_ Zertifikate \_ als \_ PFX speichern**</span><span class="sxs-lookup"><span data-stu-id="d4c53-116">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX**</span></span>        | <span data-ttu-id="d4c53-117">Die Zertifikate werden als PFX gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d4c53-117">The certificates are saved as a PFX.</span></span><br/>      | <span data-ttu-id="d4c53-118">2</span><span class="sxs-lookup"><span data-stu-id="d4c53-118">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="d4c53-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4c53-119">Remarks</span></span>

<span data-ttu-id="d4c53-120">Der- \_ Enumerationstyp "CAPICOM-Zertifikate" \_ \_ \_ wird von der " [**Zertifikats. Save**](certificates-save.md) "-Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4c53-120">The CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE enumeration type is used by the [**Certificates.Save**](certificates-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c53-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4c53-121">Requirements</span></span>



| <span data-ttu-id="d4c53-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4c53-122">Requirement</span></span> | <span data-ttu-id="d4c53-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d4c53-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c53-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d4c53-124">Redistributable</span></span><br/> | <span data-ttu-id="d4c53-125">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="d4c53-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="d4c53-126">Header</span><span class="sxs-lookup"><span data-stu-id="d4c53-126">Header</span></span><br/>          | <dl> <span data-ttu-id="d4c53-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4c53-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 




