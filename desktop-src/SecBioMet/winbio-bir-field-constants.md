---
title: WINBIO_BIR_FIELD Konstanten (winbio \_ types. h)
description: Geben Sie eine Bitmaske an.
ms.assetid: D8D12BCF-FEB3-4E02-B751-9F3AE5048BC1
topic_type:
- apiref
api_name:
- WINBIO_BIR_FIELD_SUBHEAD_COUNT
- WINBIO_BIR_FIELD_PRODUCT_ID
- WINBIO_BIR_FIELD_PATRON_ID
- WINBIO_BIR_FIELD_INDEX
- WINBIO_BIR_FIELD_CREATION_DATE
- WINBIO_BIR_FIELD_VALIDITY_PERIOD
- WINBIO_BIR_FIELD_BIOMETRIC_TYPE
- WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE
- WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION
- WINBIO_BIR_FIELD_PATRON_HEADER_VERSION
- WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE
- WINBIO_BIR_FIELD_BIOMETRIC_CONDITION
- WINBIO_BIR_FIELD_QUALITY
- WINBIO_BIR_FIELD_CREATOR
- WINBIO_BIR_FIELD_CHALLENGE
- WINBIO_BIR_FIELD_PAYLOAD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104710f1686f13227fbe65782c2baf9c13149650
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340728"
---
# <a name="winbio_bir_field-constants"></a><span data-ttu-id="c6df4-103">Winbio \_ Bir- \_ Feld Konstanten</span><span class="sxs-lookup"><span data-stu-id="c6df4-103">WINBIO\_BIR\_FIELD Constants</span></span>

<span data-ttu-id="c6df4-104">Die folgenden Konstanten werden verwendet, um eine Bitmaske für den **validfields** -Member der [**winbio- \_ \_ Header**](winbio-bir-header.md) Struktur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6df4-104">The following constants are used to create a bitmask for the **ValidFields** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure.</span></span>



| <span data-ttu-id="c6df4-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="c6df4-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="c6df4-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6df4-106">Description</span></span>                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <span data-ttu-id="c6df4-107"><dt>**Winbio \_ Bir \_ - \_ feldsubkopfanzahl \_**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-107"><dt>**WINBIO\_BIR\_FIELD\_SUBHEAD\_COUNT**</dt> <dt>0x0001</dt></span></span> </dl>                          | <span data-ttu-id="c6df4-108">Wird für die Konformität mit nistir 6529-a bereitgestellt, das allgemeine Framework für biometrische Austauschformate (CBEFF) a, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6df4-108">Provided for conformity with NISTIR 6529-A, the Common Biometric Exchange Formats Framework (CBEFF) Patron Format A, but not used.</span></span><br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <span data-ttu-id="c6df4-109"><dt>**Winbio \_ Bir \_ - \_ feldprodukt- \_ ID**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-109"><dt>**WINBIO\_BIR\_FIELD\_PRODUCT\_ID**</dt> <dt>0x0002</dt></span></span> </dl>                                   | <span data-ttu-id="c6df4-110">Der **ProductID-** Member ist gültig.</span><span class="sxs-lookup"><span data-stu-id="c6df4-110">The **ProductId** member is valid.</span></span><br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <span data-ttu-id="c6df4-111"><dt>**Winbio \_ Bir- \_ Feld- \_ Patron- \_ ID**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-111"><dt>**WINBIO\_BIR\_FIELD\_PATRON\_ID**</dt> <dt>0x0004</dt></span></span> </dl>                                      | <span data-ttu-id="c6df4-112">Wird für die Konformität mit nistir 6529-a bereitgestellt, das CBEFF-patronenformat A, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6df4-112">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <span data-ttu-id="c6df4-113"><dt>**Winbio \_ Bir \_ - \_ Feldindex**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-113"><dt>**WINBIO\_BIR\_FIELD\_INDEX**</dt> <dt>0x0008</dt></span></span> </dl>                                                   | <span data-ttu-id="c6df4-114">Wird für die Konformität mit nistir 6529-a bereitgestellt, das CBEFF-patronenformat A, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6df4-114">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <span data-ttu-id="c6df4-115"><dt>**Winbio \_ Bir \_ - \_ felderstellungs \_ Datum**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-115"><dt>**WINBIO\_BIR\_FIELD\_CREATION\_DATE**</dt> <dt>0x0010</dt></span></span> </dl>                          | <span data-ttu-id="c6df4-116">Der Member " **kreationdate** " ist gültig.</span><span class="sxs-lookup"><span data-stu-id="c6df4-116">The **CreationDate** member is valid.</span></span><br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <span data-ttu-id="c6df4-117"><dt>**Winbio \_ \_ \_ Gültigkeits \_ Dauer des BIR-Felds**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-117"><dt>**WINBIO\_BIR\_FIELD\_VALIDITY\_PERIOD**</dt> <dt>0x0020</dt></span></span> </dl>                    | <span data-ttu-id="c6df4-118">Der **ValidityPeriod** -Member ist gültig.</span><span class="sxs-lookup"><span data-stu-id="c6df4-118">The **ValidityPeriod** member is valid.</span></span><br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <span data-ttu-id="c6df4-119"><dt>**Winbio \_ \_ \_ Biometrischer \_ Typ des BIR-Felds**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-119"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_TYPE**</dt> <dt>0x0040</dt></span></span> </dl>                       | <span data-ttu-id="c6df4-120">Der **Typmember** ist gültig.</span><span class="sxs-lookup"><span data-stu-id="c6df4-120">The **Type** member is valid.</span></span><br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <span data-ttu-id="c6df4-121"><dt>**Winbio \_ \_ \_ Biometrischer \_ Untertyp "Bir Field**</dt> " <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-121"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_SUBTYPE**</dt> <dt>0x0080</dt></span></span> </dl>              | <span data-ttu-id="c6df4-122">Der **Untertyp** Member ist gültig.</span><span class="sxs-lookup"><span data-stu-id="c6df4-122">The **Subtype** member is valid.</span></span><br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <span data-ttu-id="c6df4-123"><dt>**Winbio \_ Bir \_ Field \_ CBEFF- \_ Header \_ Version**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-123"><dt>**WINBIO\_BIR\_FIELD\_CBEFF\_HEADER\_VERSION**</dt> <dt>0x0100</dt></span></span> </dl>    | <span data-ttu-id="c6df4-124">Der **Header Version** -Member ist gültig.</span><span class="sxs-lookup"><span data-stu-id="c6df4-124">The **HeaderVersion** member is valid.</span></span><br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <span data-ttu-id="c6df4-125"><dt>**Winbio \_ Bir- \_ Feld- \_ \_ patronieheader \_ Version**</dt> <dt>0x0200</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-125"><dt>**WINBIO\_BIR\_FIELD\_PATRON\_HEADER\_VERSION**</dt> <dt>0x0200</dt></span></span> </dl> | <span data-ttu-id="c6df4-126">Der **patronheaderversion** -Member ist gültig.</span><span class="sxs-lookup"><span data-stu-id="c6df4-126">The **PatronHeaderVersion** member is valid.</span></span><br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <span data-ttu-id="c6df4-127"><dt>**Winbio \_ \_ \_ \_ Biometriezweck des biometrischen Felds**</dt> <dt>0x0400</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-127"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_PURPOSE**</dt> <dt>0x0400</dt></span></span> </dl>              | <span data-ttu-id="c6df4-128">Der **Purpose** -Member ist gültig.</span><span class="sxs-lookup"><span data-stu-id="c6df4-128">The **Purpose** member is valid.</span></span><br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <span data-ttu-id="c6df4-129"><dt>**Winbio \_ \_ \_ Biometrische \_ Bedingung "Bir Field**</dt> " <dt>0x0800</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-129"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_CONDITION**</dt> <dt>0x0800</dt></span></span> </dl>        | <span data-ttu-id="c6df4-130">Wird für die Konformität mit nistir 6529-a bereitgestellt, das CBEFF-patronenformat A, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6df4-130">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <span data-ttu-id="c6df4-131"><dt>**Winbio \_ Bir- \_ Feld \_ Qualität**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-131"><dt>**WINBIO\_BIR\_FIELD\_QUALITY**</dt> <dt>0x1000</dt></span></span> </dl>                                             | <span data-ttu-id="c6df4-132">Der **dataquality** -Member ist gültig.</span><span class="sxs-lookup"><span data-stu-id="c6df4-132">The **DataQuality** member is valid.</span></span><br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <span data-ttu-id="c6df4-133"><dt>**Winbio \_ Bir \_ Field \_ Creator**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-133"><dt>**WINBIO\_BIR\_FIELD\_CREATOR**</dt> <dt>0x2000</dt></span></span> </dl>                                             | <span data-ttu-id="c6df4-134">Wird für die Konformität mit nistir 6529-a bereitgestellt, das CBEFF-patronenformat A, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6df4-134">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <span data-ttu-id="c6df4-135"><dt>**Winbio \_ Bir \_ Field \_ Challenge**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-135"><dt>**WINBIO\_BIR\_FIELD\_CHALLENGE**</dt> <dt>0x4000</dt></span></span> </dl>                                       | <span data-ttu-id="c6df4-136">Wird für die Konformität mit nistir 6529-a bereitgestellt, das CBEFF-patronenformat A, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6df4-136">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <span data-ttu-id="c6df4-137"><dt>**Winbio \_ Bir \_ - \_ feldnutzlast**</dt> <dt>0X8000</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-137"><dt>**WINBIO\_BIR\_FIELD\_PAYLOAD**</dt> <dt>0x8000</dt></span></span> </dl>                                             | <span data-ttu-id="c6df4-138">Wird für die Konformität mit nistir 6529-a bereitgestellt, das CBEFF-patronenformat A, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6df4-138">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="c6df4-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6df4-139">Requirements</span></span>



| <span data-ttu-id="c6df4-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6df4-140">Requirement</span></span> | <span data-ttu-id="c6df4-141">Wert</span><span class="sxs-lookup"><span data-stu-id="c6df4-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6df4-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6df4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c6df4-143">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6df4-143">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="c6df4-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6df4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c6df4-145">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6df4-145">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c6df4-146">Header</span><span class="sxs-lookup"><span data-stu-id="c6df4-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6df4-147"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-147"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6df4-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6df4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6df4-149">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="c6df4-149">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





