---
description: Gibt den verwendeten Codierungstyp an.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: CAPICOM_ENCODING_TYPE-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCODING_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: a546831d6e88b3e35706df59adabe0627ad9fccb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356054"
---
# <a name="capicom_encoding_type-enumeration"></a><span data-ttu-id="72749-103">CAPICOM \_ Encoding \_ Type-Enumeration</span><span class="sxs-lookup"><span data-stu-id="72749-103">CAPICOM\_ENCODING\_TYPE enumeration</span></span>

<span data-ttu-id="72749-104">Der **CAPICOM- \_ Codierungstyp \_** Enumerationstyp gibt den verwendeten Codierungstyp an.</span><span class="sxs-lookup"><span data-stu-id="72749-104">The **CAPICOM\_ENCODING\_TYPE** enumeration type indicates the encoding type used.</span></span>

## <a name="members"></a><span data-ttu-id="72749-105">Member</span><span class="sxs-lookup"><span data-stu-id="72749-105">Members</span></span>



| <span data-ttu-id="72749-106">Member</span><span class="sxs-lookup"><span data-stu-id="72749-106">Member</span></span>                      | <span data-ttu-id="72749-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72749-107">Description</span></span>                                                                                                                                                                                 | <span data-ttu-id="72749-108">Wert</span><span class="sxs-lookup"><span data-stu-id="72749-108">Value</span></span>      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| <span data-ttu-id="72749-109">**CAPICOM \_ Codieren \_ Any**</span><span class="sxs-lookup"><span data-stu-id="72749-109">**CAPICOM\_ENCODE\_ANY**</span></span>    | <span data-ttu-id="72749-110">Daten werden als Base64-codierte Zeichenfolge oder reine binäre Sequenz gespeichert.</span><span class="sxs-lookup"><span data-stu-id="72749-110">Data is saved as a base64-encoded string or a pure binary sequence.</span></span> <span data-ttu-id="72749-111">Dieser Codierungstyp wird nur für Eingabedaten verwendet, die einen unbekannten Codierungstyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="72749-111">This encoding type is used only for input data that has an unknown encoding type.</span></span> <span data-ttu-id="72749-112">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="72749-112">Introduced in CAPICOM 2.0.</span></span><br/> | <span data-ttu-id="72749-113">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="72749-113">0xffffffff</span></span> |
| <span data-ttu-id="72749-114">**CAPICOM \_ Codieren \_ Base64**</span><span class="sxs-lookup"><span data-stu-id="72749-114">**CAPICOM\_ENCODE\_BASE64**</span></span> | <span data-ttu-id="72749-115">Daten werden als Base64-codierte Zeichenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="72749-115">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                        | <span data-ttu-id="72749-116">0</span><span class="sxs-lookup"><span data-stu-id="72749-116">0</span></span>          |
| <span data-ttu-id="72749-117">**CAPICOM- \_ Codierung ( \_ Binär)**</span><span class="sxs-lookup"><span data-stu-id="72749-117">**CAPICOM\_ENCODE\_BINARY**</span></span> | <span data-ttu-id="72749-118">Daten werden als reine binäre Sequenz gespeichert.</span><span class="sxs-lookup"><span data-stu-id="72749-118">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                         | <span data-ttu-id="72749-119">1</span><span class="sxs-lookup"><span data-stu-id="72749-119">1</span></span>          |



## <a name="remarks"></a><span data-ttu-id="72749-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72749-120">Remarks</span></span>

<span data-ttu-id="72749-121">Dieser Enumerationstyp wird von den folgenden CAPICOM-Methoden und-Eigenschaften verwendet:</span><span class="sxs-lookup"><span data-stu-id="72749-121">This enumeration type is used by the following CAPICOM methods and properties:</span></span>

-   <span data-ttu-id="72749-122">[**Certificate. Export**](certificate-export.md) -Methode</span><span class="sxs-lookup"><span data-stu-id="72749-122">[**Certificate.Export**](certificate-export.md) method</span></span>
-   <span data-ttu-id="72749-123">[**Encoddata. Value**](encodeddata-value.md) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="72749-123">[**EncodedData.Value**](encodeddata-value.md) property</span></span>
-   <span data-ttu-id="72749-124">[**Verschlüsselteddata. verschlüsseln**](encrypteddata-encrypt.md) -Methode</span><span class="sxs-lookup"><span data-stu-id="72749-124">[**EncryptedData.Encrypt**](encrypteddata-encrypt.md) method</span></span>
-   <span data-ttu-id="72749-125">[**EnvelopedData. verschlüsseln**](envelopeddata-encrypt.md) -Methode</span><span class="sxs-lookup"><span data-stu-id="72749-125">[**EnvelopedData.Encrypt**](envelopeddata-encrypt.md) method</span></span>
-   <span data-ttu-id="72749-126">[**ExtendedProperty. Value**](extendedproperty-value.md) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="72749-126">[**ExtendedProperty.Value**](extendedproperty-value.md) property</span></span>
-   <span data-ttu-id="72749-127">[**SignedData. Sign**](signeddata-sign.md) -Methode</span><span class="sxs-lookup"><span data-stu-id="72749-127">[**SignedData.Sign**](signeddata-sign.md) method</span></span>
-   <span data-ttu-id="72749-128">[**SignedData. cosign**](signeddata-cosign.md) -Methode</span><span class="sxs-lookup"><span data-stu-id="72749-128">[**SignedData.CoSign**](signeddata-cosign.md) method</span></span>
-   <span data-ttu-id="72749-129">[**Store. Export**](store-export.md) -Methode</span><span class="sxs-lookup"><span data-stu-id="72749-129">[**Store.Export**](store-export.md) method</span></span>
-   <span data-ttu-id="72749-130">[**Utilities. getrandom**](utilities-getrandom.md) -Methode</span><span class="sxs-lookup"><span data-stu-id="72749-130">[**Utilities.GetRandom**](utilities-getrandom.md) method</span></span>

## <a name="requirements"></a><span data-ttu-id="72749-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72749-131">Requirements</span></span>



| <span data-ttu-id="72749-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72749-132">Requirement</span></span> | <span data-ttu-id="72749-133">Wert</span><span class="sxs-lookup"><span data-stu-id="72749-133">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="72749-134">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="72749-134">Redistributable</span></span><br/> | <span data-ttu-id="72749-135">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="72749-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="72749-136">Header</span><span class="sxs-lookup"><span data-stu-id="72749-136">Header</span></span><br/>          | <dl> <span data-ttu-id="72749-137"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="72749-137"><dt>Capicom.h</dt></span></span> </dl> |



 

 




