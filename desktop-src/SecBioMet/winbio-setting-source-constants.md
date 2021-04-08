---
title: WINBIO_SETTING_SOURCE Konstanten (winbio \_ types. h)
description: Bestimmen Sie, ob die Windows-Biometrieframework derzeit aktiviert ist.
ms.assetid: d95aa6cc-ddff-40fb-ab82-eac78dc0cb6b
topic_type:
- apiref
api_name:
- WINBIO_SETTING_SOURCE_INVALID
- WINBIO_SETTING_SOURCE_DEFAULT
- WINBIO_SETTING_SOURCE_POLICY
- WINBIO_SETTING_SOURCE_LOCAL
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54723612c7e0948e09baddf22ad4f4703ca5c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957156"
---
# <a name="winbio_setting_source-constants"></a><span data-ttu-id="94ef8-103">Winbio- \_ Einstellungs \_ Quellen Konstanten</span><span class="sxs-lookup"><span data-stu-id="94ef8-103">WINBIO\_SETTING\_SOURCE Constants</span></span>

<span data-ttu-id="94ef8-104">Die folgenden Konstanten werden von der [**winbiogetenabledsetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) -Funktion verwendet, um zu bestimmen, ob die Windows-Biometrieframework derzeit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="94ef8-104">The following constants are used by the [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) function to determine whether the Windows Biometric Framework is currently enabled.</span></span> <span data-ttu-id="94ef8-105">Die Konstanten geben an, woher die Einstellung stammt.</span><span class="sxs-lookup"><span data-stu-id="94ef8-105">The constants specify where the setting originated.</span></span>



| <span data-ttu-id="94ef8-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="94ef8-106">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="94ef8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94ef8-107">Description</span></span>                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <span data-ttu-id="94ef8-108"><dt>**winbio- \_ Einstellungs \_ Quelle \_ ungültig**</dt></span><span class="sxs-lookup"><span data-stu-id="94ef8-108"><dt>**WINBIO\_SETTING\_SOURCE\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="94ef8-109">Die Einstellung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="94ef8-109">The setting is not valid.</span></span><br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <span data-ttu-id="94ef8-110"><dt>**Standardeinstellung für winbio- \_ Einstellungs \_ Quelle \_**</dt></span><span class="sxs-lookup"><span data-stu-id="94ef8-110"><dt>**WINBIO\_SETTING\_SOURCE\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="94ef8-111">Die Einstellung stammt aus der integrierten Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="94ef8-111">The setting originated from built-in policy.</span></span><br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <span data-ttu-id="94ef8-112"><dt>**winbio- \_ Einstellungs \_ Quell \_ Richtlinie**</dt></span><span class="sxs-lookup"><span data-stu-id="94ef8-112"><dt>**WINBIO\_SETTING\_SOURCE\_POLICY**</dt></span></span> </dl>    | <span data-ttu-id="94ef8-113">Die Einstellung stammt aus der Registrierung des lokalen Computers.</span><span class="sxs-lookup"><span data-stu-id="94ef8-113">The setting originated in the local computer registry.</span></span><br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <span data-ttu-id="94ef8-114"><dt>**winbio- \_ Einstellungs \_ Quelle \_ lokal**</dt></span><span class="sxs-lookup"><span data-stu-id="94ef8-114"><dt>**WINBIO\_SETTING\_SOURCE\_LOCAL**</dt></span></span> </dl>       | <span data-ttu-id="94ef8-115">Die Einstellung wurde von Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="94ef8-115">The setting was created by Group Policy</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="94ef8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94ef8-116">Requirements</span></span>



| <span data-ttu-id="94ef8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94ef8-117">Requirement</span></span> | <span data-ttu-id="94ef8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="94ef8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94ef8-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94ef8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="94ef8-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94ef8-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="94ef8-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94ef8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="94ef8-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94ef8-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="94ef8-123">Header</span><span class="sxs-lookup"><span data-stu-id="94ef8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="94ef8-124"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94ef8-124"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94ef8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94ef8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ef8-126">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="94ef8-126">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





