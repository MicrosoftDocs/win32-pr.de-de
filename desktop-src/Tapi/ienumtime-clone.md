---
description: Die Clone-Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: 'Ienumtime:: Clone-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a030fcd90006047e35d9f661f2878dfbc42c112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369238"
---
# <a name="ienumtimeclone-method"></a><span data-ttu-id="8b3cb-103">Ienumtime:: Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="8b3cb-103">IEnumTime::Clone method</span></span>

<span data-ttu-id="8b3cb-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8b3cb-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8b3cb-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="8b3cb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8b3cb-106">Die **Clone** -Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="8b3cb-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b3cb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b3cb-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="8b3cb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b3cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b3cb-109">*ppum* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8b3cb-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b3cb-110">Zeiger auf das neue [**ienumtime**](ienumtime.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8b3cb-110">Pointer to the new [**IEnumTime**](ienumtime.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b3cb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b3cb-111">Return value</span></span>

<span data-ttu-id="8b3cb-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8b3cb-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8b3cb-113">Wert</span><span class="sxs-lookup"><span data-stu-id="8b3cb-113">Value</span></span>                                                                                         | <span data-ttu-id="8b3cb-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8b3cb-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8b3cb-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8b3cb-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8b3cb-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8b3cb-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8b3cb-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="8b3cb-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8b3cb-118">Der *ppum* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="8b3cb-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="8b3cb-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="8b3cb-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8b3cb-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8b3cb-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8b3cb-121"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="8b3cb-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="8b3cb-122">Aus unbekannten Gründen fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="8b3cb-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="8b3cb-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b3cb-123">Remarks</span></span>

<span data-ttu-id="8b3cb-124">TAPI Ruft die **adressf** -Methode für die [**ienumtime**](ienumtime.md) -Schnittstelle auf, die von **ienumtime:: Clone** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8b3cb-124">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **IEnumTime::Clone**.</span></span> <span data-ttu-id="8b3cb-125">Die Anwendung muss Release auf der **ienumtime** -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8b3cb-125">The application must call **Release** on the **IEnumTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b3cb-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b3cb-126">Requirements</span></span>



| <span data-ttu-id="8b3cb-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b3cb-127">Requirement</span></span> | <span data-ttu-id="8b3cb-128">Wert</span><span class="sxs-lookup"><span data-stu-id="8b3cb-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3cb-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="8b3cb-129">TAPI version</span></span><br/> | <span data-ttu-id="8b3cb-130">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="8b3cb-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8b3cb-131">Header</span><span class="sxs-lookup"><span data-stu-id="8b3cb-131">Header</span></span><br/>       | <dl> <span data-ttu-id="8b3cb-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b3cb-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b3cb-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8b3cb-133">Library</span></span><br/>      | <dl> <span data-ttu-id="8b3cb-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b3cb-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8b3cb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8b3cb-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="8b3cb-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b3cb-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b3cb-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b3cb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b3cb-138">**Ienumtime**</span><span class="sxs-lookup"><span data-stu-id="8b3cb-138">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




