---
title: WINBIO_BIOMETRIC_SUBTYPE Konstanten (winbio \_ types. h)
description: Stellen Sie Informationen zu einer biometrischen Messung bereit.
ms.assetid: 019569A9-6184-4E75-9B82-C98F4F45F61A
topic_type:
- apiref
api_name:
- WINBIO_SUBTYPE_NO_INFORMATION
- WINBIO_SUBTYPE_ANY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba1bc25337bf49a48b54b6b2426673daf8a15bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956690"
---
# <a name="winbio_biometric_subtype-constants"></a><span data-ttu-id="ea8fe-103">Subtypkonstanten von winbio- \_ Biometrie \_</span><span class="sxs-lookup"><span data-stu-id="ea8fe-103">WINBIO\_BIOMETRIC\_SUBTYPE Constants</span></span>

<span data-ttu-id="ea8fe-104">**Winbio \_ Biometrische \_ subtypkonstanten** werden im gesamten Windows-Biometrieframework verwendet, um zusätzliche Informationen zu einer biometrischen Messung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-104">**WINBIO\_BIOMETRIC\_SUBTYPE** constants are used throughout the Windows Biometric Framework to provide additional information about a biometric measurement.</span></span> <span data-ttu-id="ea8fe-105">Die folgenden Konstanten können verwendet werden, wenn kein Untertyp erforderlich ist oder wenn ein beliebiger Untertyp erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-105">The following constants can be used when no subtype is required or when any subtype is required.</span></span>



| <span data-ttu-id="ea8fe-106">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="ea8fe-106">Constant/value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="ea8fe-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea8fe-107">Description</span></span>                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <span data-ttu-id="ea8fe-108"><dt>**Winbio \_ Untertyp \_ keine \_ Informationen**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="ea8fe-108"><dt>**WINBIO\_SUBTYPE\_NO\_INFORMATION**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="ea8fe-109">Keine Untertyp Informationen.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-109">No subtype information.</span></span><br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <span data-ttu-id="ea8fe-110"><dt>**Winbio \_ Untertyp \_ beliebiger**</dt> <dt>0xFF</dt></span><span class="sxs-lookup"><span data-stu-id="ea8fe-110"><dt>**WINBIO\_SUBTYPE\_ANY**</dt> <dt>0xFF</dt></span></span> </dl>                                   | <span data-ttu-id="ea8fe-111">Ein beliebiger Untertyp.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-111">Any subtype.</span></span><br/>            |



## <a name="remarks"></a><span data-ttu-id="ea8fe-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea8fe-112">Remarks</span></span>

<span data-ttu-id="ea8fe-113">Verwenden Sie die folgende Tabelle, um die verfügbaren biometrischen Untertypen für einen bestimmten biometrischen Typ zu finden:</span><span class="sxs-lookup"><span data-stu-id="ea8fe-113">To find the available biometric subtypes for a particular biometric type, use the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea8fe-114"><strong>WINBIO_BIOMETRIC_TYPE</strong> Wert</span><span class="sxs-lookup"><span data-stu-id="ea8fe-114"><strong>WINBIO_BIOMETRIC_TYPE</strong> value</span></span></th>
<th><span data-ttu-id="ea8fe-115">Thema (e) zum Suchen nach <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> Werten</span><span class="sxs-lookup"><span data-stu-id="ea8fe-115">Topic(s) to find <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ea8fe-116"><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></span><span class="sxs-lookup"><span data-stu-id="ea8fe-116"><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></span></span></td>
<td><span data-ttu-id="ea8fe-117"><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE Konstanten</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="ea8fe-117"><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="ea8fe-118">Diese Werte gelten nur für Windows 10 und höher.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-118">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea8fe-119"><strong>WINBIO_TYPE_FINGERPRINT</strong></span><span class="sxs-lookup"><span data-stu-id="ea8fe-119"><strong>WINBIO_TYPE_FINGERPRINT</strong></span></span></td>
<td><span data-ttu-id="ea8fe-120">Eines der folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="ea8fe-120">One of the following topics:</span></span>
<ul>
<li><span data-ttu-id="ea8fe-121"><a href="winbio-ansi-381-format-constants.md"><strong>WINBIO_ANSI_381_FORMAT Konstanten</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea8fe-121"><a href="winbio-ansi-381-format-constants.md"><strong>WINBIO_ANSI_381_FORMAT Constants</strong></a></span></span></li>
<li><span data-ttu-id="ea8fe-122"><a href="winbio-ansi-381-img-constants.md"><strong>WINBIO_ANSI_381_IMG Konstanten</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea8fe-122"><a href="winbio-ansi-381-img-constants.md"><strong>WINBIO_ANSI_381_IMG Constants</strong></a></span></span></li>
<li><span data-ttu-id="ea8fe-123"><a href="winbio-ansi-381-img-acq-constants.md"><strong>WINBIO_ANSI_381_IMG_ACQ Konstanten</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea8fe-123"><a href="winbio-ansi-381-img-acq-constants.md"><strong>WINBIO_ANSI_381_IMG_ACQ Constants</strong></a></span></span></li>
<li><span data-ttu-id="ea8fe-124"><a href="winbio-ansi-381-imp-type-constants.md"><strong>WINBIO_ANSI_381_IMP_TYPE Konstanten</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea8fe-124"><a href="winbio-ansi-381-imp-type-constants.md"><strong>WINBIO_ANSI_381_IMP_TYPE Constants</strong></a></span></span></li>
<li><span data-ttu-id="ea8fe-125"><a href="winbio-ansi-381-pixels-constants.md"><strong>WINBIO_ANSI_381_PIXELS Konstanten</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea8fe-125"><a href="winbio-ansi-381-pixels-constants.md"><strong>WINBIO_ANSI_381_PIXELS Constants</strong></a></span></span></li>
<li><span data-ttu-id="ea8fe-126"><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS Fingerabdruck Konstanten</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea8fe-126"><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS Fingerprint Constants</strong></a></span></span></li>
<li><span data-ttu-id="ea8fe-127"><a href="winbio-ansi-381-pos-palm-constants.md"><strong>WINBIO_ANSI_381_POS_Palm Konstanten</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea8fe-127"><a href="winbio-ansi-381-pos-palm-constants.md"><strong>WINBIO_ANSI_381_POS_Palm Constants</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ea8fe-128"><strong>WINBIO_TYPE_IRIS</strong></span><span class="sxs-lookup"><span data-stu-id="ea8fe-128"><strong>WINBIO_TYPE_IRIS</strong></span></span></td>
<td><span data-ttu-id="ea8fe-129"><a href="winbio-iris-constants.md"><strong>WINBIO_IRIS Konstanten</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="ea8fe-129"><a href="winbio-iris-constants.md"><strong>WINBIO_IRIS Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="ea8fe-130">Diese Werte gelten nur für Windows 10 und höher.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-130">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea8fe-131"><strong>WINBIO_TYPE_VOICE</strong></span><span class="sxs-lookup"><span data-stu-id="ea8fe-131"><strong>WINBIO_TYPE_VOICE</strong></span></span></td>
<td><span data-ttu-id="ea8fe-132"><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>WINBIO_VOICE Konstanten</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="ea8fe-132"><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>WINBIO_VOICE Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="ea8fe-133">Diese Werte gelten nur für Windows 10 und höher.</span><span class="sxs-lookup"><span data-stu-id="ea8fe-133">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ea8fe-134">Weitere Informationen finden Sie unter [Client Anwendungs Konstanten](client-application-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ea8fe-134">For more information, see [Client Application Constants](client-application-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea8fe-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea8fe-135">Requirements</span></span>



| <span data-ttu-id="ea8fe-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea8fe-136">Requirement</span></span> | <span data-ttu-id="ea8fe-137">Wert</span><span class="sxs-lookup"><span data-stu-id="ea8fe-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8fe-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea8fe-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ea8fe-139">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea8fe-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="ea8fe-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea8fe-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ea8fe-141">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea8fe-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ea8fe-142">Header</span><span class="sxs-lookup"><span data-stu-id="ea8fe-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea8fe-143"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea8fe-143"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





