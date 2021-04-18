---
description: Die Put \_ localparticipanttypeer-Methode legt Teilnehmer Informationen fest.
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: Itlocalteilnehmer::p ut_LocalParticipantTypedInfo-Methode (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77809a9a3858b6a098fa3ff6a93878cf38518f92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354677"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a><span data-ttu-id="6af2c-103">Itlocalteilnehmer::p UT \_ localparticipanttypeer-Methode</span><span class="sxs-lookup"><span data-stu-id="6af2c-103">ITLocalParticipant::put\_LocalParticipantTypedInfo method</span></span>

<span data-ttu-id="6af2c-104">Die **Put \_ localparticipanttypeer** -Methode legt Teilnehmer Informationen fest.</span><span class="sxs-lookup"><span data-stu-id="6af2c-104">The **put\_LocalParticipantTypedInfo** method sets participant information.</span></span>

## <a name="syntax"></a><span data-ttu-id="6af2c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6af2c-105">Syntax</span></span>


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6af2c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6af2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6af2c-107">*InfoType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6af2c-107">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af2c-108">[**Teilnehmer \_ Der typisierte \_ Info**](participant-typed-info.md) Bezeichner des Typs der erforderlichen Informationen.</span><span class="sxs-lookup"><span data-stu-id="6af2c-108">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) identifier of the type of information required.</span></span>

</dd> <dt>

<span data-ttu-id="6af2c-109">*ppinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6af2c-109">*ppInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af2c-110">**BSTR** , das den für die Informationen erforderlichen neuen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="6af2c-110">**BSTR** containing the required new value for the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6af2c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6af2c-111">Return value</span></span>

<span data-ttu-id="6af2c-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6af2c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6af2c-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6af2c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6af2c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6af2c-114">Remarks</span></span>

<span data-ttu-id="6af2c-115">Die Anwendung muss " [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *ppinfo* -Parameter zuzuweisen, und " [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="6af2c-115">The application must use [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *ppInfo* parameter and use [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6af2c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6af2c-116">Requirements</span></span>



| <span data-ttu-id="6af2c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6af2c-117">Requirement</span></span> | <span data-ttu-id="6af2c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6af2c-118">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6af2c-119">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="6af2c-119">TAPI version</span></span><br/> | <span data-ttu-id="6af2c-120">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="6af2c-120">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6af2c-121">Header</span><span class="sxs-lookup"><span data-stu-id="6af2c-121">Header</span></span><br/>       | <dl> <span data-ttu-id="6af2c-122"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="6af2c-122"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="6af2c-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6af2c-123">Library</span></span><br/>      | <dl> <span data-ttu-id="6af2c-124"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6af2c-124"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6af2c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6af2c-125">DLL</span></span><br/>          | <dl> <span data-ttu-id="6af2c-126"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6af2c-126"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6af2c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6af2c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6af2c-128">**Itlocalteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="6af2c-128">**ITLocalParticipant**</span></span>](itlocalparticipant.md)
</dt> <dt>

[<span data-ttu-id="6af2c-129">**\_typisierte Teilnehmer \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="6af2c-129">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> </dl>

 

