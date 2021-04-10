---
title: WINBIO_BIR_QUALITY Konstanten (winbio \_ types. h)
description: Geben Sie die relative Qualität der biometrischen Daten im Bir an, wenn kein ganzzahliger Wert zwischen 0 und 100 angegeben wurde.
ms.assetid: A42AA21B-9AA5-4DB6-B58F-0776BEC63E6C
topic_type:
- apiref
api_name:
- WINBIO_DATA_QUALITY_NOT_SET
- WINBIO_DATA_QUALITY_NOT_SUPPORTED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1eb0881672c9e3bf51214cff93cb3f68d802b04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106191"
---
# <a name="winbio_bir_quality-constants"></a><span data-ttu-id="33846-103">Winbio \_ Bir- \_ Qualitäts Konstanten</span><span class="sxs-lookup"><span data-stu-id="33846-103">WINBIO\_BIR\_QUALITY Constants</span></span>

<span data-ttu-id="33846-104">Die folgenden Flags werden vom **dataquality** -Member der [**winbio- \_ \_ Header**](winbio-bir-header.md) -Struktur verwendet, um die relative Qualität der biometrischen Daten im Bir anzugeben, wenn kein ganzzahliger Wert zwischen 0 und 100 angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="33846-104">The following flags are used by the **DataQuality** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure to specify the relative quality of biometric data in the BIR if an integer value from 0 to 100 has not been specified.</span></span>



| <span data-ttu-id="33846-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="33846-105">Constant/value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="33846-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33846-106">Description</span></span>                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <span data-ttu-id="33846-107"><dt>**Winbio \_ Data \_ Quality \_ nicht \_ festgelegt**</dt> <dt> 1</dt></span><span class="sxs-lookup"><span data-stu-id="33846-107"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SET**</dt> <dt> 1</dt></span></span> </dl>                   | <span data-ttu-id="33846-108">Qualitätsmessungen werden vom BIR-Ersteller unterstützt, aber im Bir ist kein Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="33846-108">Quality measurements are supported by the BIR creator, but no value is set in the BIR.</span></span><br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <span data-ttu-id="33846-109"><dt>**Winbio \_ Data \_ Quality \_ nicht \_ unterstützt**</dt> <dt> 2</dt></span><span class="sxs-lookup"><span data-stu-id="33846-109"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SUPPORTED**</dt> <dt> 2</dt></span></span> </dl> | <span data-ttu-id="33846-110">Qualitätsmessungen werden vom BIR-Ersteller nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="33846-110">Quality measurements are not supported by the BIR creator.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="33846-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33846-111">Requirements</span></span>



| <span data-ttu-id="33846-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33846-112">Requirement</span></span> | <span data-ttu-id="33846-113">Wert</span><span class="sxs-lookup"><span data-stu-id="33846-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33846-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33846-114">Minimum supported client</span></span><br/> | <span data-ttu-id="33846-115">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33846-115">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="33846-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33846-116">Minimum supported server</span></span><br/> | <span data-ttu-id="33846-117">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33846-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="33846-118">Header</span><span class="sxs-lookup"><span data-stu-id="33846-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="33846-119"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33846-119"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33846-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33846-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33846-121">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="33846-121">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





