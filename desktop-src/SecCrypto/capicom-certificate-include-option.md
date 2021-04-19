---
description: Definiert, welche Zertifikate in einer Kette gespeichert werden.
ms.assetid: 6f9e28e6-b01f-4803-8259-8ab73abeecf8
title: CAPICOM_CERTIFICATE_INCLUDE_OPTION-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_INCLUDE_OPTION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 45ea9ccf7d3a43e325073f04e28bbd392fa34998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361332"
---
# <a name="capicom_certificate_include_option-enumeration"></a><span data-ttu-id="17970-103">CAPICOM \_ Certificate \_ include- \_ Option-Enumeration</span><span class="sxs-lookup"><span data-stu-id="17970-103">CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION enumeration</span></span>

<span data-ttu-id="17970-104">Der " **CAPICOM \_ Certificate \_ include \_ Option** "-Enumerationstyp definiert, welche Zertifikate in einer Kette gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="17970-104">The **CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION** enumeration type defines which certificates in a chain are saved.</span></span> <span data-ttu-id="17970-105">Dieser Enumerationstyp wurde in CAPICOM 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="17970-105">This enumeration type was introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="17970-106">Member</span><span class="sxs-lookup"><span data-stu-id="17970-106">Members</span></span>



| <span data-ttu-id="17970-107">Member</span><span class="sxs-lookup"><span data-stu-id="17970-107">Member</span></span>                                                 | <span data-ttu-id="17970-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17970-108">Description</span></span>                                                                           | <span data-ttu-id="17970-109">Wert</span><span class="sxs-lookup"><span data-stu-id="17970-109">Value</span></span> |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="17970-110">**CAPICOM- \_ Zertifikats \_ include- \_ Kette \_ mit Ausnahme von \_ root**</span><span class="sxs-lookup"><span data-stu-id="17970-110">**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</span></span> | <span data-ttu-id="17970-111">Speichert alle Zertifikate in der Kette mit Ausnahme der Stamm Entität.</span><span class="sxs-lookup"><span data-stu-id="17970-111">Saves all certificates in the chain with the exception of the root entity.</span></span><br/> | <span data-ttu-id="17970-112">0</span><span class="sxs-lookup"><span data-stu-id="17970-112">0</span></span>     |
| <span data-ttu-id="17970-113">**CAPICOM- \_ Zertifikat \_ einschließlich \_ ganzer \_ Kette**</span><span class="sxs-lookup"><span data-stu-id="17970-113">**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</span></span>        | <span data-ttu-id="17970-114">Speichert die komplette Zertifikatskette.</span><span class="sxs-lookup"><span data-stu-id="17970-114">Saves the complete certificate chain.</span></span><br/>                                      | <span data-ttu-id="17970-115">1</span><span class="sxs-lookup"><span data-stu-id="17970-115">1</span></span>     |
| <span data-ttu-id="17970-116">**CAPICOM- \_ Zertifikat \_ schließt \_ nur End- \_ Entität \_ ein.**</span><span class="sxs-lookup"><span data-stu-id="17970-116">**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</span></span>   | <span data-ttu-id="17970-117">Speichert nur das Endentitäts Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="17970-117">Saves only the end entity certificate.</span></span><br/>                                     | <span data-ttu-id="17970-118">2</span><span class="sxs-lookup"><span data-stu-id="17970-118">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="17970-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17970-119">Remarks</span></span>

<span data-ttu-id="17970-120">Der Enumerationstyp " **CAPICOM \_ Certificate \_ include \_ Option** " wird von der [**Certificate. Save**](certificate-save.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="17970-120">The **CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION** enumeration type is used by the [**Certificate.Save**](certificate-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="17970-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17970-121">Requirements</span></span>



| <span data-ttu-id="17970-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17970-122">Requirement</span></span> | <span data-ttu-id="17970-123">Wert</span><span class="sxs-lookup"><span data-stu-id="17970-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="17970-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="17970-124">Redistributable</span></span><br/> | <span data-ttu-id="17970-125">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="17970-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="17970-126">Header</span><span class="sxs-lookup"><span data-stu-id="17970-126">Header</span></span><br/>          | <dl> <span data-ttu-id="17970-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="17970-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 




