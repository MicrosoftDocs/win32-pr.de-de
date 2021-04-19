---
description: Die \_ Methode Get participants erstellt eine Sammlung von Teilnehmern, die der aktuellen Konferenz zugeordnet sind.
ms.assetid: 643acc3f-3df1-4f3a-a8fe-5d46864f8cf7
title: 'Itparticipantcontrol:: get_Participants-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4a99e0efe7702a3358684b00af5e8faa96461c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370055"
---
# <a name="itparticipantcontrolget_participants-method"></a><span data-ttu-id="4a8b3-103">Itparticipantcontrol:: get- \_ Teilnehmer Methode</span><span class="sxs-lookup"><span data-stu-id="4a8b3-103">ITParticipantControl::get\_Participants method</span></span>

<span data-ttu-id="4a8b3-104">\[**get \_ Teilnehmer** sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-104">\[**get\_Participants** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4a8b3-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="4a8b3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4a8b3-106">Die Methode **get \_ participants** erstellt eine Sammlung von Teilnehmern, die der aktuellen Konferenz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-106">The **get\_Participants** method creates a collection of participants associated with the current conference.</span></span> <span data-ttu-id="4a8b3-107">Diese Methode wird für Automatisierungs Client Anwendungen bereitgestellt, wie z. b. in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-107">This method is provided for Automation client applications, such as those written in Visual Basic.</span></span> <span data-ttu-id="4a8b3-108">C-und C++-Anwendungen müssen die [**enumerateparticipants**](itparticipantcontrol-enumerateparticipants.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-108">C and C++ applications must use the [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a8b3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a8b3-109">Syntax</span></span>


```C++
HRESULT get_Participants(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a><span data-ttu-id="4a8b3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a8b3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a8b3-111">*pvariant* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4a8b3-111">*pVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a8b3-112">Ein Zeiger auf eine **Variante** , die eine [**itcollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) von [**itteilnehmer**](itparticipant.md) -Schnittstellen Zeigern enthält.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-112">Pointer to **VARIANT** containing an [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a8b3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a8b3-113">Return value</span></span>

<span data-ttu-id="4a8b3-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-114">This method can return one of these values.</span></span>



| <span data-ttu-id="4a8b3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4a8b3-115">Value</span></span>                                                                                         | <span data-ttu-id="4a8b3-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4a8b3-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="4a8b3-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4a8b3-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4a8b3-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4a8b3-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="4a8b3-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4a8b3-120">Der *pvariant* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-120">The *pVariant* parameter is not a valid pointer.</span></span><br/>     |
| <dl> <span data-ttu-id="4a8b3-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="4a8b3-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4a8b3-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a8b3-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a8b3-123">Remarks</span></span>

<span data-ttu-id="4a8b3-124">TAPI Ruft die **adressf** -Methode für die [**itparticipants**](itparticipant.md) -Schnittstelle auf, die von **itparticipantcontrol:: get- \_ Teilnehmern** zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="4a8b3-124">TAPI calls the **AddRef** method on the [**ITParticipant**](itparticipant.md) interface returned by **ITParticipantControl::get\_Participants**.</span></span> <span data-ttu-id="4a8b3-125">Die Anwendung muss Release auf der **itparticipants** -Schnittstelle aufzurufen, um Ihnen zugeordnete Ressourcen frei **zugeben** .</span><span class="sxs-lookup"><span data-stu-id="4a8b3-125">The application must call **Release** on the **ITParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a8b3-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a8b3-126">Requirements</span></span>



| <span data-ttu-id="4a8b3-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a8b3-127">Requirement</span></span> | <span data-ttu-id="4a8b3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="4a8b3-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a8b3-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="4a8b3-129">TAPI version</span></span><br/> | <span data-ttu-id="4a8b3-130">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4a8b3-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4a8b3-131">Header</span><span class="sxs-lookup"><span data-stu-id="4a8b3-131">Header</span></span><br/>       | <dl> <span data-ttu-id="4a8b3-132"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4a8b3-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="4a8b3-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4a8b3-133">Library</span></span><br/>      | <dl> <span data-ttu-id="4a8b3-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a8b3-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4a8b3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4a8b3-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="4a8b3-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a8b3-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4a8b3-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a8b3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a8b3-138">**Itparticipantcontrol**</span><span class="sxs-lookup"><span data-stu-id="4a8b3-138">**ITParticipantControl**</span></span>](itparticipantcontrol.md)
</dt> <dt>

[<span data-ttu-id="4a8b3-139">**Enumerateparticipants**</span><span class="sxs-lookup"><span data-stu-id="4a8b3-139">**EnumerateParticipants**</span></span>](itparticipantcontrol-enumerateparticipants.md)
</dt> <dt>

[<span data-ttu-id="4a8b3-140">**Itcollection**</span><span class="sxs-lookup"><span data-stu-id="4a8b3-140">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[<span data-ttu-id="4a8b3-141">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="4a8b3-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




