---
title: Allgemeine Konstanten (winbio \_ types. h)
description: Geben Sie maximale SID-Länge, Handles, IDs, maximale Zeichen folgen Länge und maximale Puffergröße an.
ms.assetid: 62e87bd8-a708-4d00-aaa8-9cac8e3736a7
topic_type:
- apiref
api_name:
- SECURITY_MAX_SID_SIZE
- WINBIO_UNIT_ID
- WINBIO_SESSION_HANDLE
- WINBIO_FRAMEWORK_HANDLE
- WINBIO_UUID
- WINBIO_STRING
- WINBIO_MAX_STRING_LEN
- WINBIO_MAX_SAMPLE_BUFFER_SIZE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e35aa4c2cc676935cfb80fdec8729daf64d5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956465"
---
# <a name="general-constants-winbio_typesh"></a><span data-ttu-id="11c61-103">Allgemeine Konstanten (winbio \_ types. h)</span><span class="sxs-lookup"><span data-stu-id="11c61-103">General Constants (Winbio\_types.h)</span></span>

<span data-ttu-id="11c61-104">Die folgenden Konstanten werden in der Windows-Biometrieframework verwendet.</span><span class="sxs-lookup"><span data-stu-id="11c61-104">The following constants are used throughout the Windows Biometric Framework.</span></span>



| <span data-ttu-id="11c61-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="11c61-105">Constant/value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="11c61-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11c61-106">Description</span></span>                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <span data-ttu-id="11c61-107"><dt>**\_Maximale \_ sid- \_ Größe der Sicherheit**</dt></span><span class="sxs-lookup"><span data-stu-id="11c61-107"><dt>**SECURITY\_MAX\_SID\_SIZE**</dt></span></span> </dl>                                                                                          | <span data-ttu-id="11c61-108">Die maximale Länge eines SID-Werts (Security Identifier).</span><span class="sxs-lookup"><span data-stu-id="11c61-108">The maximum length of a security identifier (SID) value.</span></span> <span data-ttu-id="11c61-109">Derzeit ist dies 68.</span><span class="sxs-lookup"><span data-stu-id="11c61-109">Currently this is 68.</span></span><br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <span data-ttu-id="11c61-110"><dt>**winbio- \_ Einheits- \_ ID**</dt></span><span class="sxs-lookup"><span data-stu-id="11c61-110"><dt>**WINBIO\_UNIT\_ID**</dt></span></span> </dl>                                                                                                                | <span data-ttu-id="11c61-111">ID-Nummer einer biometrischen Einheit.</span><span class="sxs-lookup"><span data-stu-id="11c61-111">ID number of a biometric unit.</span></span><br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <span data-ttu-id="11c61-112"><dt>**winbio- \_ Sitzungs \_ handle**</dt></span><span class="sxs-lookup"><span data-stu-id="11c61-112"><dt>**WINBIO\_SESSION\_HANDLE**</dt></span></span> </dl>                                                                                           | <span data-ttu-id="11c61-113">Eine lange ganze Zahl ohne Vorzeichen, die das Handle für eine geöffnete biometrische Sitzung enthält.</span><span class="sxs-lookup"><span data-stu-id="11c61-113">An unsigned long integer that contains the handle for an open biometric session.</span></span><br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <span data-ttu-id="11c61-114"><dt>**winbio \_ Framework- \_ handle**</dt></span><span class="sxs-lookup"><span data-stu-id="11c61-114"><dt>**WINBIO\_FRAMEWORK\_HANDLE**</dt></span></span> </dl>                                                                                     | <span data-ttu-id="11c61-115">Eine lange ganze Zahl ohne Vorzeichen, die das Handle für eine geöffnete Framework-Sitzung enthält.</span><span class="sxs-lookup"><span data-stu-id="11c61-115">An unsigned long integer that contains the handle for an open framework session.</span></span><br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <span data-ttu-id="11c61-116"><dt>**winbio- \_ UUID**</dt></span><span class="sxs-lookup"><span data-stu-id="11c61-116"><dt>**WINBIO\_UUID**</dt></span></span> </dl>                                                                                                                          | <span data-ttu-id="11c61-117">Ein GUID.</span><span class="sxs-lookup"><span data-stu-id="11c61-117">A GUID.</span></span><br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <span data-ttu-id="11c61-118"><dt>**winbio- \_ Zeichenfolge**</dt></span><span class="sxs-lookup"><span data-stu-id="11c61-118"><dt>**WINBIO\_STRING**</dt></span></span> </dl>                                                                                                                    | <span data-ttu-id="11c61-119">Ein Bytearray, das eine NULL-terminierte Unicode-Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="11c61-119">A byte array that contains a null-terminated Unicode string.</span></span><br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <span data-ttu-id="11c61-120"><dt>**Winbio \_ Max. \_ Zeichenfolge \_ len**</dt></span><span class="sxs-lookup"><span data-stu-id="11c61-120"><dt>**WINBIO\_MAX\_STRING\_LEN** </dt></span></span> </dl>                                                                                       | <span data-ttu-id="11c61-121">Die maximale Länge eines **winbio- \_ Zeichen** folgen Werts.</span><span class="sxs-lookup"><span data-stu-id="11c61-121">The maximum length of a **WINBIO\_STRING** value.</span></span> <span data-ttu-id="11c61-122">Derzeit ist dies 256.</span><span class="sxs-lookup"><span data-stu-id="11c61-122">Currently this is 256.</span></span><br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <span data-ttu-id="11c61-123"><dt>**Winbio \_ Maximale \_ \_ Puffer \_ Größe**</dt> <dt>0x7FFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="11c61-123"><dt>**WINBIO\_MAX\_SAMPLE\_BUFFER\_SIZE**</dt> <dt>0x7FFFFFFF</dt></span></span> </dl> | <span data-ttu-id="11c61-124">Die maximale Anzahl von Bytes in einer einzelnen biometrischen Datenerfassung.</span><span class="sxs-lookup"><span data-stu-id="11c61-124">The maximum number of bytes in a single biometric data capture.</span></span><br/>                  |



## <a name="requirements"></a><span data-ttu-id="11c61-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11c61-125">Requirements</span></span>



| <span data-ttu-id="11c61-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11c61-126">Requirement</span></span> | <span data-ttu-id="11c61-127">Wert</span><span class="sxs-lookup"><span data-stu-id="11c61-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c61-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11c61-128">Minimum supported client</span></span><br/> | <span data-ttu-id="11c61-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11c61-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="11c61-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11c61-130">Minimum supported server</span></span><br/> | <span data-ttu-id="11c61-131">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11c61-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="11c61-132">Header</span><span class="sxs-lookup"><span data-stu-id="11c61-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="11c61-133"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11c61-133"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11c61-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11c61-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11c61-135">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="11c61-135">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





