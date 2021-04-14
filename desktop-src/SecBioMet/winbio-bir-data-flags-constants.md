---
title: WINBIO_BIR_DATA_FLAGS Konstanten (winbio \_ types. h)
description: Geben Sie die Bedingung für die Daten an.
ms.assetid: F6F7F68A-3294-4AF8-A1A7-C6A869A2CC3C
topic_type:
- apiref
api_name:
- WINBIO_DATA_FLAG_PRIVACY
- WINBIO_DATA_FLAG_INTEGRITY
- WINBIO_DATA_FLAG_SIGNED
- WINBIO_DATA_FLAG_RAW
- WINBIO_DATA_FLAG_INTERMEDIATE
- WINBIO_DATA_FLAG_PROCESSED
- WINBIO_DATA_FLAG_OPTION_MASK_PRESENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8195cf17040c35b9e42f8977b36c5ddc6f2ea33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392214"
---
# <a name="winbio_bir_data_flags-constants"></a><span data-ttu-id="0a1db-103">Winbio \_ - \_ \_ datenflags-Konstanten</span><span class="sxs-lookup"><span data-stu-id="0a1db-103">WINBIO\_BIR\_DATA\_FLAGS Constants</span></span>

<span data-ttu-id="0a1db-104">Die folgenden Konstanten werden vom **dataflags** -Member der [**winbio- \_ \_ Header**](winbio-bir-header.md) Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="0a1db-104">The following constants are used by the **DataFlags** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure.</span></span>



| <span data-ttu-id="0a1db-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="0a1db-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="0a1db-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a1db-106">Description</span></span>                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <span data-ttu-id="0a1db-107"><dt>**Winbio \_ Data \_ Flag \_ Privacy**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="0a1db-107"><dt>**WINBIO\_DATA\_FLAG\_PRIVACY**</dt> <dt>0x02</dt></span></span> </dl>                                       | <span data-ttu-id="0a1db-108">Die Daten sind verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="0a1db-108">The data is encrypted.</span></span><br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <span data-ttu-id="0a1db-109"><dt>**Winbio \_ Datenflag- \_ \_ Integrität**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="0a1db-109"><dt>**WINBIO\_DATA\_FLAG\_INTEGRITY**</dt> <dt>0x01</dt></span></span> </dl>                                 | <span data-ttu-id="0a1db-110">Die Daten sind digital signiert oder durch einen Nachrichten Authentifizierungscode (Message Authentication Code, Mac) geschützt.</span><span class="sxs-lookup"><span data-stu-id="0a1db-110">The data is digitally signed or is protected by a message authentication code (MAC).</span></span><br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <span data-ttu-id="0a1db-111"><dt>**Winbio \_ \_Datenflag \_ signiert**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="0a1db-111"><dt>**WINBIO\_DATA\_FLAG\_SIGNED**</dt> <dt>0x04</dt></span></span> </dl>                                          | <span data-ttu-id="0a1db-112">Wenn dieses Flag und das **integritätsflag für die winbio- \_ \_ datenflag \_** festgelegt sind, werden die Daten signiert.</span><span class="sxs-lookup"><span data-stu-id="0a1db-112">If this flag and the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag are set, the data is signed.</span></span> <span data-ttu-id="0a1db-113">Wenn dieses Flag nicht festgelegt ist, aber das integritätsflag für die **winbio- \_ \_ \_ datenflag** festgelegt ist, wird ein Mac für die Daten berechnet.</span><span class="sxs-lookup"><span data-stu-id="0a1db-113">If this flag is not set but the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag is set, a MAC is computed on the data.</span></span><br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <span data-ttu-id="0a1db-114"><dt>**Winbio \_ Data \_ Flag \_ RAW**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="0a1db-114"><dt>**WINBIO\_DATA\_FLAG\_RAW**</dt> <dt>0x20</dt></span></span> </dl>                                                   | <span data-ttu-id="0a1db-115">Die Daten haben das Format, in dem Sie aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="0a1db-115">The data is in the format with which it was captured.</span></span><br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <span data-ttu-id="0a1db-116"><dt>**Winbio \_ \_Datenflag \_ zwischen**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="0a1db-116"><dt>**WINBIO\_DATA\_FLAG\_INTERMEDIATE**</dt> <dt>0x40</dt></span></span> </dl>                        | <span data-ttu-id="0a1db-117">Die Daten sind nicht RAW, aber wurden nicht vollständig verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0a1db-117">The data is not raw but has not been completely processed.</span></span><br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <span data-ttu-id="0a1db-118"><dt>**Winbio \_ \_Datenflag \_ verarbeitet**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="0a1db-118"><dt>**WINBIO\_DATA\_FLAG\_PROCESSED**</dt> <dt>0x80</dt></span></span> </dl>                                 | <span data-ttu-id="0a1db-119">Die Daten wurden verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0a1db-119">The data has been processed.</span></span><br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <span data-ttu-id="0a1db-120"><dt>**Winbio \_ Datenflag- \_ \_ options \_ Maske \_ vorhanden**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="0a1db-120"><dt>**WINBIO\_DATA\_FLAG\_OPTION\_MASK\_PRESENT**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="0a1db-121">Die flagmaske.</span><span class="sxs-lookup"><span data-stu-id="0a1db-121">The flag mask.</span></span> <span data-ttu-id="0a1db-122">Dieser Wert ist immer eins (1).</span><span class="sxs-lookup"><span data-stu-id="0a1db-122">This value is always one (1).</span></span><br/>                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="0a1db-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a1db-123">Requirements</span></span>



| <span data-ttu-id="0a1db-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a1db-124">Requirement</span></span> | <span data-ttu-id="0a1db-125">Wert</span><span class="sxs-lookup"><span data-stu-id="0a1db-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a1db-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a1db-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0a1db-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a1db-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="0a1db-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a1db-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0a1db-129">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a1db-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0a1db-130">Header</span><span class="sxs-lookup"><span data-stu-id="0a1db-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a1db-131"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a1db-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a1db-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a1db-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a1db-133">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="0a1db-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





