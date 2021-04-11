---
title: WINBIO_IDENTITY Struktur (winbio \_ types. h)
description: Enthält einen identifizierenden Wert, der einer biometrischen Vorlage zugeordnet ist.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- WINBIO_IDENTITY Struktur Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_IDENTITY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8092754b9107029e0be5800bbd5bc98bc3efb91c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103995"
---
# <a name="winbio_identity-structure"></a><span data-ttu-id="e0bd9-104">Winbio- \_ Identitäts Struktur</span><span class="sxs-lookup"><span data-stu-id="e0bd9-104">WINBIO\_IDENTITY structure</span></span>

<span data-ttu-id="e0bd9-105">Die **winbio- \_ Identitäts** Struktur enthält einen identifizierenden Wert, der einer biometrischen Vorlage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-105">The **WINBIO\_IDENTITY** structure contains an identifying value associated with a biometric template.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0bd9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0bd9-106">Syntax</span></span>


```C++
typedef struct _WINBIO_IDENTITY {
  WINBIO_IDENTITY_TYPE Type;
  union {
    ULONG  Null;
    ULONG  Wildcard;
    GUID   TemplateGuid;
    struct {
      ULONG Size;
      UCHAR Data[SECURITY_MAX_SID_SIZE];
    } AccountSid;
  } Value;
} WINBIO_IDENTITY;
```



## <a name="members"></a><span data-ttu-id="e0bd9-107">Member</span><span class="sxs-lookup"><span data-stu-id="e0bd9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e0bd9-108">**Type**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="e0bd9-109">Gibt das Format der Identitätsinformationen an, die in dieser Struktur enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-109">Specifies the format of the identity information contained in this structure.</span></span> <span data-ttu-id="e0bd9-110">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="e0bd9-110">This can be one of the following values:</span></span>



| <span data-ttu-id="e0bd9-111">Wert</span><span class="sxs-lookup"><span data-stu-id="e0bd9-111">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="e0bd9-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e0bd9-112">Meaning</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <span data-ttu-id="e0bd9-113"><dt>**winbio- \_ ID- \_ Typ \_ null**</dt></span><span class="sxs-lookup"><span data-stu-id="e0bd9-113"><dt>**WINBIO\_ID\_TYPE\_NULL**</dt></span></span> </dl>             | <span data-ttu-id="e0bd9-114">Der Vorlage ist keine ID zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-114">The template has no associated ID.</span></span><br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <span data-ttu-id="e0bd9-115"><dt>**winbio- \_ ID- \_ Typ Platzhalter \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0bd9-115"><dt>**WINBIO\_ID\_TYPE\_WILDCARD**</dt></span></span> </dl> | <span data-ttu-id="e0bd9-116">Die Struktur entspricht allen Vorlagen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-116">The structure matches all template identities.</span></span><br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <span data-ttu-id="e0bd9-117"><dt>**winbio- \_ ID- \_ \_ GUID-Typ**</dt></span><span class="sxs-lookup"><span data-stu-id="e0bd9-117"><dt>**WINBIO\_ID\_TYPE\_GUID**</dt></span></span> </dl>             | <span data-ttu-id="e0bd9-118">Die Struktur enthält eine GUID, die der Vorlage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-118">The structure contains a GUID associated with the template.</span></span><br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <span data-ttu-id="e0bd9-119"><dt>**winbio- \_ ID- \_ Typ- \_ sid**</dt></span><span class="sxs-lookup"><span data-stu-id="e0bd9-119"><dt>**WINBIO\_ID\_TYPE\_SID**</dt></span></span> </dl>                | <span data-ttu-id="e0bd9-120">Die Struktur enthält die der Vorlage zugeordnete Konto-SID.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-120">The structure contains the account SID associated with the template.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e0bd9-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-121">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="e0bd9-122">Eine Union, die einen der folgenden Werte enthalten kann:</span><span class="sxs-lookup"><span data-stu-id="e0bd9-122">A union that can contain one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="e0bd9-123">**NULL**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-123">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="e0bd9-124">Enthält 1, wenn der **Typmember** ein **winbio- \_ ID- \_ Typ \_ null** ist.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-124">Contains 1 if the **Type** member is **WINBIO\_ID\_TYPE\_NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e0bd9-125">**Platzhalter**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-125">**Wildcard**</span></span>
</dt> <dd>

<span data-ttu-id="e0bd9-126">Enthält 1, wenn der **Typmember** ein **winbio- \_ ID- \_ Typplatzhalter \_** ist.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-126">Contains 1 if the **Type** member is **WINBIO\_ID\_TYPE\_WILDCARD**.</span></span>

</dd> <dt>

<span data-ttu-id="e0bd9-127">**Templateguid**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-127">**TemplateGuid**</span></span>
</dt> <dd>

<span data-ttu-id="e0bd9-128">Enthält einen 128-Bit-GUID-Wert, der die Vorlage identifiziert, wenn der **Typmember** eine **\_ \_ \_ GUID für den winbio-ID-Typ** ist.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-128">Contains a 128-bit GUID value that identifies the template if the **Type** member is **WINBIO\_ID\_TYPE\_GUID**.</span></span>

</dd> <dt>

<span data-ttu-id="e0bd9-129">**AccountSid**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-129">**AccountSid**</span></span>
</dt> <dd>

<span data-ttu-id="e0bd9-130">Eine-Struktur, die eine Konto-sid enthält, wenn der **Typmember** den **winbio- \_ ID- \_ Typ \_ sid** hat.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-130">A structure that contains an account SID if the **Type** member is **WINBIO\_ID\_TYPE\_SID**.</span></span>

<dl> <dt>

<span data-ttu-id="e0bd9-131">**Größe**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-131">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="e0bd9-132">Die Anzahl der Zeichen in der SID.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-132">The number of characters in the SID.</span></span>

</dd> <dt>

<span data-ttu-id="e0bd9-133">**Daten**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-133">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="e0bd9-134">Ein Array von Zeichen ohne Vorzeichen, die die SID enthalten.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-134">An array of unsigned characters that contain the SID.</span></span> <span data-ttu-id="e0bd9-135">Die aktuelle maximale Größe des Arrays beträgt 68 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-135">The current maximum size of the array is 68 characters.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0bd9-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0bd9-136">Remarks</span></span>

<span data-ttu-id="e0bd9-137">Diese Struktur wird in den folgenden Funktionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="e0bd9-137">This structure is used in the following functions:</span></span>

-   [<span data-ttu-id="e0bd9-138">**Winbiodeletetemplate**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-138">**WinBioDeleteTemplate**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)
-   [<span data-ttu-id="e0bd9-139">**Winbioregistricommit**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-139">**WinBioEnrollCommit**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)
-   [<span data-ttu-id="e0bd9-140">**Winbioenumregistrierungen**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-140">**WinBioEnumEnrollments**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)
-   [<span data-ttu-id="e0bd9-141">**Winbiogetkredentialstate**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-141">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
-   [<span data-ttu-id="e0bd9-142">**Winbioidentifizierung**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-142">**WinBioIdentify**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)
-   [<span data-ttu-id="e0bd9-143">**Winbioremovecredential**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-143">**WinBioRemoveCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
-   [<span data-ttu-id="e0bd9-144">**Winbioverify**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-144">**WinBioVerify**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioverify)
-   [<span data-ttu-id="e0bd9-145">**Winbioverifywithcallback**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-145">**WinBioVerifyWithCallback**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)

## <a name="requirements"></a><span data-ttu-id="e0bd9-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0bd9-146">Requirements</span></span>



| <span data-ttu-id="e0bd9-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0bd9-147">Requirement</span></span> | <span data-ttu-id="e0bd9-148">Wert</span><span class="sxs-lookup"><span data-stu-id="e0bd9-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0bd9-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0bd9-149">Minimum supported client</span></span><br/> | <span data-ttu-id="e0bd9-150">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0bd9-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="e0bd9-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0bd9-151">Minimum supported server</span></span><br/> | <span data-ttu-id="e0bd9-152">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0bd9-152">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e0bd9-153">Header</span><span class="sxs-lookup"><span data-stu-id="e0bd9-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0bd9-154"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0bd9-154"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0bd9-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0bd9-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0bd9-156">Client Anwendungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="e0bd9-156">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





