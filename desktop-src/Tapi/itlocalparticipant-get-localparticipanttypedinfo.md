---
description: Die get \_ localparticipanttypeer-Methode ruft Teilnehmer Informationen ab, wie z. b. den e-Mail-Namen oder den geografischen Standort.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: 'Itlocalteilnehmer:: get_LocalParticipantTypedInfo-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabaf503963c09898c06659884fd3ac3858e704
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355979"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a><span data-ttu-id="b4b72-103">Itlocalteilnehmer:: get \_ localparticipanttypdinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="b4b72-103">ITLocalParticipant::get\_LocalParticipantTypedInfo method</span></span>

<span data-ttu-id="b4b72-104">Die **get \_ localparticipanttypeer** -Methode ruft Teilnehmer Informationen ab, wie z. b. den e-Mail-Namen oder den geografischen Standort.</span><span class="sxs-lookup"><span data-stu-id="b4b72-104">The **get\_LocalParticipantTypedInfo** method gets participant information, such as e-mail name or geographical location.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b72-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4b72-105">Syntax</span></span>


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b4b72-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4b72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4b72-107">*InfoType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4b72-107">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4b72-108">[**Teilnehmer \_ Der typisierte \_ Info**](participant-typed-info.md) Bezeichner vom Typ der erforderlichen Informationen.</span><span class="sxs-lookup"><span data-stu-id="b4b72-108">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) identifier of type of information required.</span></span>

</dd> <dt>

<span data-ttu-id="b4b72-109">*ppinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b4b72-109">*ppInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4b72-110">Zeiger auf einen **BSTR** -Wert, der die erforderlichen Informationen nach der erfolgreichen Rückgabe der Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="b4b72-110">Pointer to a **BSTR** that will contain the required information following a successful return of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4b72-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4b72-111">Return value</span></span>

<span data-ttu-id="b4b72-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b4b72-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b4b72-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b4b72-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4b72-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4b72-114">Remarks</span></span>

<span data-ttu-id="b4b72-115">Die Anwendung muss [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppinfo* -Parameter zugewiesenen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b4b72-115">The application must use [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4b72-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4b72-116">Requirements</span></span>



| <span data-ttu-id="b4b72-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4b72-117">Requirement</span></span> | <span data-ttu-id="b4b72-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b4b72-118">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b72-119">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="b4b72-119">TAPI version</span></span><br/> | <span data-ttu-id="b4b72-120">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b4b72-120">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b4b72-121">Header</span><span class="sxs-lookup"><span data-stu-id="b4b72-121">Header</span></span><br/>       | <dl> <span data-ttu-id="b4b72-122"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b4b72-122"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="b4b72-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b4b72-123">Library</span></span><br/>      | <dl> <span data-ttu-id="b4b72-124"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4b72-124"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b4b72-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b4b72-125">DLL</span></span><br/>          | <dl> <span data-ttu-id="b4b72-126"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4b72-126"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b4b72-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4b72-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b72-128">**Itlocalteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="b4b72-128">**ITLocalParticipant**</span></span>](itlocalparticipant.md)
</dt> <dt>

[<span data-ttu-id="b4b72-129">**\_typisierte Teilnehmer \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="b4b72-129">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> </dl>

 

