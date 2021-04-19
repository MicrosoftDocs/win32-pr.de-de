---
description: Definiert das Format einer Datei mit Zertifikat Informationen.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: CAPICOM_CERTIFICATE_SAVE_AS_TYPE-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1e5365594a5a1cf1f06691c63b37c04f38530575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372050"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a><span data-ttu-id="33c55-103">\_ \_ \_ \_ Datentyp-Enumeration des CAPICOM-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="33c55-103">CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE enumeration</span></span>

<span data-ttu-id="33c55-104">Der Enumerationstyp " **CAPICOM- \_ Zertifikat \_ speichern \_ \_** unter" definiert das Format einer Datei mit Zertifikat Informationen.</span><span class="sxs-lookup"><span data-stu-id="33c55-104">The **CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE** enumeration type defines the format of a file containing certificate information.</span></span> <span data-ttu-id="33c55-105">Dieser Enumerationstyp wurde von CAPICOM 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="33c55-105">This enumeration type was introduced by CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="33c55-106">Member</span><span class="sxs-lookup"><span data-stu-id="33c55-106">Members</span></span>



| <span data-ttu-id="33c55-107">Member</span><span class="sxs-lookup"><span data-stu-id="33c55-107">Member</span></span>                                  | <span data-ttu-id="33c55-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33c55-108">Description</span></span>                                                                                                                                   | <span data-ttu-id="33c55-109">Wert</span><span class="sxs-lookup"><span data-stu-id="33c55-109">Value</span></span> |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="33c55-110">**CAPICOM \_ - \_ Zertifikat \_ als \_ PFX speichern**</span><span class="sxs-lookup"><span data-stu-id="33c55-110">**CAPICOM\_CERTIFICATE\_SAVE\_AS\_PFX**</span></span> | <span data-ttu-id="33c55-111">Die Ausgabedatei wird als PFX-Datei (PKCS 12) formatiert, und alle zugehörigen privaten Schlüssel, die exportierbar sind, werden ebenfalls gespeichert.</span><span class="sxs-lookup"><span data-stu-id="33c55-111">The output file will be formatted as a PFX (PKCS 12) file and any associated private keys which are exportable will also be saved.</span></span><br/> | <span data-ttu-id="33c55-112">0</span><span class="sxs-lookup"><span data-stu-id="33c55-112">0</span></span>     |
| <span data-ttu-id="33c55-113">**CAPICOM- \_ Zertifikat \_ speichern \_ als \_ CER**</span><span class="sxs-lookup"><span data-stu-id="33c55-113">**CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**</span></span> | <span data-ttu-id="33c55-114">Die Ausgabedatei wird als CER-Datei formatiert, ohne dass private Schlüssel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="33c55-114">The output file will be formatted as a CER file with no private keys saved.</span></span><br/>                                                        | <span data-ttu-id="33c55-115">1</span><span class="sxs-lookup"><span data-stu-id="33c55-115">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="33c55-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33c55-116">Remarks</span></span>

<span data-ttu-id="33c55-117">Der Enumerationstyp " **CAPICOM- \_ Zertifikat \_ speichern \_ als \_** " wird von der [**Certificate. Save**](certificate-save.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="33c55-117">The **CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE** enumeration type is used by the [**Certificate.Save**](certificate-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="33c55-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33c55-118">Requirements</span></span>



| <span data-ttu-id="33c55-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33c55-119">Requirement</span></span> | <span data-ttu-id="33c55-120">Wert</span><span class="sxs-lookup"><span data-stu-id="33c55-120">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="33c55-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="33c55-121">Redistributable</span></span><br/> | <span data-ttu-id="33c55-122">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="33c55-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="33c55-123">Header</span><span class="sxs-lookup"><span data-stu-id="33c55-123">Header</span></span><br/>          | <dl> <span data-ttu-id="33c55-124"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="33c55-124"><dt>Capicom.h</dt></span></span> </dl> |



 

 




